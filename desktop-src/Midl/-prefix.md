---
title: /prefix-Schalter
description: Der Schalter /prefix leitet den MIDL-Compiler an, den Namen der Client- und/oder Serverstubroutine Präfixzeichenfolgen hinzuzufügen.
ms.assetid: 5530e972-08bf-4cca-9bb4-9631db824bdb
keywords:
- /prefix switch MIDL
topic_type:
- apiref
api_name:
- /prefix
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 366417b66838a6c55a207effbf6e8e5913cd2206b5288cf1790343789330b9ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808818"
---
# <a name="prefix-switch"></a>/prefix-Schalter

Der **Schalter /prefix** leitet den MIDL-Compiler an, den Namen der Client- und/oder Serverstubroutine Präfixzeichenfolgen hinzuzufügen. Dies kann verwendet werden, damit ein einzelnes Programm sowohl ein Client als auch ein Server mit derselben Schnittstelle sein kann, ohne dass die client- und serverseitigen Routinenamen miteinander in Konflikt stehen.

``` syntax
midl /prefix { client | cstub | server | sstub | switch | all }
```

## <a name="switch-options"></a>Switch-Optionen

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="client"></span><span id="CLIENT"></span>

<span id="client"></span><span id="CLIENT"></span>client**


</dt> <dd>

Wirkt sich nur auf die Namen der Clientstubroutinen aus.

</dd> <dt>

<span id="cstub"></span><span id="CSTUB"></span>

<span id="cstub"></span><span id="CSTUB"></span>cstub**


</dt> <dd>

Identisch mit *client*. Wirkt sich nur auf die Namen der Clientstubroutinen aus.

</dd> <dt>

<span id="server"></span><span id="SERVER"></span>

<span id="server"></span><span id="SERVER"></span>server**


</dt> <dd>

Wirkt sich nur auf die Routinenamen aus, die von der Serverstubroutine aufgerufen werden.

</dd> <dt>

<span id="sstub"></span><span id="SSTUB"></span>

<span id="sstub"></span><span id="SSTUB"></span>sstub**


</dt> <dd>

Identisch mit *Server*. Wirkt sich nur auf die Routinenamen aus, die von der Serverstubroutine aufgerufen werden.

</dd> <dt>

<span id="switch"></span><span id="SWITCH"></span>

<span id="switch"></span><span id="SWITCH"></span>switch**


</dt> <dd>

Wirkt sich auf einen zusätzlichen Prototyp aus, der der Headerdatei hinzugefügt wurde.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>all**


</dt> <dd>

Wirkt sich sowohl auf die Namen der Client- als auch der Serverstubroutine aus.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn sich das Präfix für die clientseitigen Routinen vom Präfix für die serverseitigen Routinen abwechselt, enthält die generierte Headerdatei sowohl clientseitige Routineprototypen als auch serverseitige Routineprototypen.

Der **Schalter /prefix** ist nützlich, wenn eine einzelne Headerdatei mit Stubs aus mehreren Durchläufen des MIDL-Compilers verwendet wird. Dadurch werden zusätzliche Routineprototypen in der Headerdatei erzwingt.

In jedem Fall überschreiben client-, server- und switch-Präfixe alle Präfixe.

## <a name="examples"></a>Beispiele

**midl /prefix client "c \_ " server "s \_ "**

**midl /prefix all \_ "moo"**

**midl /prefix client \_ "suffix"**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




