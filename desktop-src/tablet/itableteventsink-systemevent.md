---
description: Tritt auf, wenn ein System Ereignis verfügbar ist.
ms.assetid: 3d9e98f0-b11e-4a65-a544-9e1998a80d5f
title: 'Itableteventsink:: systemevent-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.SystemEvent
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 71b5882fd9e19df43581e00cce55c2af5faa432b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359165"
---
# <a name="itableteventsinksystemevent-method"></a>Itableteventsink:: systemevent-Methode

Tritt auf, wenn ein System Ereignis verfügbar ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT SystemEvent(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] SYSTEM_EVENT      event,
  [in] SYSTEM_EVENT_DATA eventdata
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TCID* \[ in\]
</dt> <dd>

Der Bezeichner des Tablets.

</dd> <dt>

*CID* \[ in\]
</dt> <dd>

Der Bezeichner des Tablettstifts.

</dd> <dt>

*Ereignis* \[ in\]
</dt> <dd>

Der System Ereignis Code.

</dd> <dt>

*EventData* \[ in\]
</dt> <dd>

Die System Ereignisdaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die folgende Liste enthält die gültigen Werte für den Ereignis Parameter.

-   SE \_ tippen
-   SE \_ DBL \_ Tap
-   SE \_ right \_ Tap
-   SE \_ ziehen
-   \_Drag right \_ Drag
-   SE \_ Hold- \_ EINGABETASTE
-   SE \_ Hold \_ Leave
-   SE \_ Hover \_ EINGABETASTE
-   SE- \_ Hover \_ verlassen
-   SE \_ mittlere \_ Maustaste
-   SE- \_ Taste
-   SE- \_ \_ Modifizierertaste
-   SE- \_ Gesten \_ Modus
-   SE- \_ Cursor

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itableteventsink-Schnittstelle**](itableteventsink.md)
</dt> </dl>

 

 




