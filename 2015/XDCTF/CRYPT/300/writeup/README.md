这题要求用户指定index和ckey，然后用某些复杂操作计算sha512的hash值，涉及我们不知道的password和某个随机数。

因为题目里存在有限域上的求幂操作，而且N给定，所以可以考虑让求幂结果相对较少，对ckey的检查只要求模N不为0，所以我们可以取1让它计算时不来添麻烦。对index的检查要求它在2-N/2之间，我们希望index的阶尽量小，后来把N-1分解了一下发现有2*2*5*bignum，所以就找了个阶为5的index，这样index不管多少次方最多应该就5个结果，于是其中随便猜一个不停跑就是了。

这题好歹python程序没丢……见crypt300.py