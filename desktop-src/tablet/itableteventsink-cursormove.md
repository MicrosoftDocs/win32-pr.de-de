---
description: Tritt ein, wenn der Cursor über den Tablettdiger bewegt wird.
ms.assetid: cd2863af-59a9-4dd0-a679-84861a70ef53
title: ITabletEventSink::CursorMove-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.CursorMove
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 030fa5ba4adc725288d5135ccd24409d4fc02cddbc16da52aa375a275a73be5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843490"
---
# <a name="itableteventsinkcursormove-method"></a>ITabletEventSink::CursorMove-Methode

Tritt ein, wenn der Cursor über den Tablettdiger bewegt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT CursorMove(
   TABLET_CONTEXT_ID tcid,
   CURSOR_ID         cid,
   HWND              hWnd,
   LONG              xPos,
   LONG              yPos
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*tcid* 
</dt> <dd>

Eindeutiger Dentifizierer des Tablett digitalisierers.

</dd> <dt>

*Cid* 
</dt> <dd>

Eindeutiger Bezeichner des Tablettstifts.

</dd> <dt>

*hWnd* 
</dt> <dd>

Das Fenster, über das sich der Cursor bewegt hat.

</dd> <dt>

*xPos* 
</dt> <dd>

Die X-Position des Stifts.

</dd> <dt>

*yPos* 
</dt> <dd>

Die Y-Position des Stifts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                              |
| Bibliothek<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITabletEventSink-Schnittstelle**](itableteventsink.md)
</dt> </dl>

 

 




