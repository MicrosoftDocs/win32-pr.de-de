---
title: EN_ENDCOMPOSITION Benachrichtigungs Code (RichEdit. h)
description: Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Benutzer neue Daten eingegeben hat oder die Eingabe von Daten während der Verwendung von IME oder Text Services Framework abgeschlossen hat.
ms.assetid: 3956313F-F82F-41A2-AEDA-52E63218977C
keywords:
- Windows-Steuerelemente für EN_ENDCOMPOSITION Benachrichtigungs
topic_type:
- apiref
api_name:
- EN_ENDCOMPOSITION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df1c2b5d08b2da73c67edeb6fe7ca4ac639000c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475390"
---
# <a name="en_endcomposition-notification-code"></a>EN \_ endcomposition-Benachrichtigungs Code

Benachrichtigt das übergeordnete Fenster eines Rich-Edit-Steuer Elements, dass der Benutzer neue Daten eingegeben hat oder die Eingabe von Daten während der Verwendung von IME oder [Text Services Framework](/windows/desktop/TSF/text-services-framework)abgeschlossen hat.


```C++
EN_ENDCOMPOSITION

     pEndComp = (ENDCOMPOSITIONNOTIFY *)lParam;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Eine [**endcompositionnotify**](/windows/win32/api/richedit/ns-richedit-endcompositionnotify) -Struktur, die Informationen über die End-Kompositions Bedingung empfängt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

