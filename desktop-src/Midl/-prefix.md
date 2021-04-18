---
title: /Prefix-Schalter
description: Der/prefix-Schalter leitet den mittelmäßigen Compiler zum Hinzufügen von Präfix Zeichenfolgen zu den Namen der Client-und/oder serverstubroutinen.
ms.assetid: 5530e972-08bf-4cca-9bb4-9631db824bdb
keywords:
- /Prefix-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /prefix
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79885a57f257fe2648a27fd67a014421b2c1c13a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516353"
---
# <a name="prefix-switch"></a>/Prefix-Schalter

Der **/prefix** -Schalter leitet den mittelmäßigen Compiler zum Hinzufügen von Präfix Zeichenfolgen zu den Namen der Client-und/oder serverstubroutinen. Dies kann verwendet werden, um zuzulassen, dass ein einzelnes Programm sowohl ein Client als auch ein Server derselben Schnittstelle ist, ohne dass die Namen von Client-und serverseitigen Routinen miteinander in Konflikt stehen.

``` syntax
midl /prefix { client | cstub | server | sstub | switch | all }
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="client"></span><span id="CLIENT"></span>

<span id="client"></span><span id="CLIENT"></span>Client * * * *


</dt> <dd>

Wirkt sich nur auf die Namen der Clientstub-Routine aus.

</dd> <dt>

<span id="cstub"></span><span id="CSTUB"></span>

<span id="cstub"></span><span id="CSTUB"></span>cstub * * * *


</dt> <dd>

Identisch mit dem *Client*. Wirkt sich nur auf die Namen der Clientstub-Routine aus.

</dd> <dt>

<span id="server"></span><span id="SERVER"></span>

<span id="server"></span><span id="SERVER"></span>Server * * * *


</dt> <dd>

Wirkt sich nur auf die Routine Namen aus, die von der Server-stubroutine aufgerufen werden.

</dd> <dt>

<span id="sstub"></span><span id="SSTUB"></span>

<span id="sstub"></span><span id="SSTUB"></span>sstub * * * *


</dt> <dd>

Identisch mit dem *Server*. Wirkt sich nur auf die Routine Namen aus, die von der Server-stubroutine aufgerufen werden.

</dd> <dt>

<span id="switch"></span><span id="SWITCH"></span>

<span id="switch"></span><span id="SWITCH"></span>Switch * * * *


</dt> <dd>

Hat Auswirkungen auf einen zusätzlichen Prototyp, der der Header Datei hinzugefügt wurde.

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>Alle * * * *


</dt> <dd>

Wirkt sich auf die Namen von Client-und Server-Stub-Routine aus

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn sich das Präfix für die Client seitigen Routinen vom Präfix für die serverseitigen Routinen unterscheidet, enthält die generierte Header Datei sowohl Client seitige Routine Prototypen als auch serverseitige Routine Prototypen.

Der **/prefix** -Schalter ist nützlich, wenn eine einzelne Header Datei mit stubläufen aus mehreren Ausführungen des Mittelwert Compilers verwendet wird. Dies erzwingt zusätzliche Routine Prototypen in der Header Datei.

In allen Fällen überschreiben die Client-, Server-und switchpräfixe ein all-Präfix.

## <a name="examples"></a>Beispiele

**Mittel l/Prefix Client "c \_ " Server "s \_ "**

**Mittel l/Prefix alle "moo \_ "**

**Mittel l/Prefix Client "Bark \_ "**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




