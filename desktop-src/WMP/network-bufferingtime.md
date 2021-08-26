---
title: Network.bufferingTime
description: Die bufferingTime-Eigenschaft gibt die Zeit in Millisekunden an, die zum Puffern eingehender Daten vor Beginn der Wiedergabe zugeordnet ist, oder ruft sie ab.
ms.assetid: b52b7f44-6be1-4299-94da-c37d758795af
keywords:
- Network.bufferingTime-Windows Media Player
topic_type:
- apiref
api_name:
- Network.bufferingTime
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afe4a68a7ad1ae8a1444f1e2f31ad09461e05d221e8fceae52960bd5927aac0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901730"
---
# <a name="networkbufferingtime"></a>Network.bufferingTime

Die **bufferingTime-Eigenschaft** gibt die Zeit in Millisekunden an, die zum Puffern eingehender Daten vor Beginn der Wiedergabe zugeordnet ist, oder ruft sie ab.

## <a name="syntax"></a>Syntax

*Player*. *network*. **bufferingTime**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese-/Schreibnummer **(** **long**) im Bereich von 0 bis 60.000 mit einem Standardwert von 5.000.

## <a name="examples"></a>Beispiele

Im folgenden beispiel JScript Netzwerk *verwendet.* **bufferingTime,** um die Anzahl der Sekunden anzugeben, die für die Pufferung eingehender Daten zugeordnet sind. Die Informationen werden aus einem HTML TEXT INPUT-Element abgerufen, das mit id = "bufText" erstellt wurde. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


```JScript
<!-- Create a BUTTON element to change the bufferingTime value. -->
<INPUT TYPE = "BUTTON" NAME = "bufTime" ID = "bufTime" 
       VALUE = "Change Buffer Time"

    onClick = "
       /* Test whether the user entered a valid value. */
       if (bufText.value >= 0 & bufText.value <= 60) 
           Player.network.bufferingTime = bufText.value * 1000;
       else
           alert('Buffering time must be between 0 and 60.');
">

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerkobjekt**](network-object.md)
</dt> </dl>

 

 





