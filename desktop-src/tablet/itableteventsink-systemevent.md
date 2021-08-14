---
description: Tritt ein, wenn ein Systemereignis verfügbar ist.
ms.assetid: 3d9e98f0-b11e-4a65-a544-9e1998a80d5f
title: ITabletEventSink::SystemEvent-Methode
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
ms.openlocfilehash: 6d2e636b5e0b70d13ae33850518e744fbc9425bd65c20002a89b6d38e56dbc50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041742"
---
# <a name="itableteventsinksystemevent-method"></a>ITabletEventSink::SystemEvent-Methode

Tritt ein, wenn ein Systemereignis verfügbar ist.

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

*tcid* \[ In\]
</dt> <dd>

Der Bezeichner des Tablets.

</dd> <dt>

*cid* \[ in\]
</dt> <dd>

Der Bezeichner des Stifts.

</dd> <dt>

*event* \[ In\]
</dt> <dd>

Der Systemereigniscode.

</dd> <dt>

*eventdata* \[ In\]
</dt> <dd>

Die Systemereignisdaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="remarks"></a>Hinweise

Die folgende Liste enthält die gültigen Werte für den Ereignisparameter.

-   \_SE Tippen
-   \_SE DBL \_ TAP
-   \_SE TIPPEN \_ MIT DER RECHTEN
-   \_SE Ziehen
-   \_SE ZIEHEN NACH \_ RECHTS
-   \_SE HALTEN SIE DIE \_ EINGABETASTE.
-   \_SE HOLD \_ LEAVE
-   \_SE \_HOVER-EINGABETASTE
-   \_SE HOVER \_ LEAVE
-   \_SE MITTLERES \_ KLICKEN
-   \_SE Schlüssel
-   \_SE MODIFIZIERERTASTE \_
-   \_SE \_GESTENMODUS
-   \_SE Cursor

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITabletEventSink-Schnittstelle**](itableteventsink.md)
</dt> </dl>

 

 




