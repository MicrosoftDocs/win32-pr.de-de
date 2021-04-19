---
title: Network. BufferingTime
description: Die BufferingTime-Eigenschaft gibt den Zeitraum in Millisekunden an, der für die Pufferung eingehender Daten reserviert ist, bevor die Wiedergabe beginnt.
ms.assetid: b52b7f44-6be1-4299-94da-c37d758795af
keywords:
- Network. BufferingTime-Windows-Media Player
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
ms.openlocfilehash: 27b805173403268afff473db427b58193382afe6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369604"
---
# <a name="networkbufferingtime"></a>Network. BufferingTime

Die **BufferingTime** -Eigenschaft gibt den Zeitraum in Millisekunden an, der für die Pufferung eingehender Daten reserviert ist, bevor die Wiedergabe beginnt.

## <a name="syntax"></a>Syntax

*Player*. *Netzwerk*. **BufferingTime**

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine Lese-/schreibzahl (**Long**) im Bereich von 0 (null) bis 60.000 mit dem Standardwert 5.000. 

## <a name="examples"></a>Beispiele

Im folgenden JScript-Beispiel wird *Network* verwendet. **BufferingTime** zum Angeben der Anzahl von Sekunden, die für die Pufferung eingehender Daten reserviert werden. Die Informationen werden aus einem HTML-Text Eingabe Element abgerufen, das mit ID = "buftext" erstellt wurde. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


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
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Netzwerk Objekt**](network-object.md)
</dt> </dl>

 

 





