---
description: Tritt auf, wenn der Cursor über den Tablet-Digitalisierer bewegt wird.
ms.assetid: cd2863af-59a9-4dd0-a679-84861a70ef53
title: 'Itableteventsink:: Cursor move-Methode'
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
ms.openlocfilehash: f6950e0b30c1b8fc8ccf3e60a8aaa05b9eeb3215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364231"
---
# <a name="itableteventsinkcursormove-method"></a>Itableteventsink:: Cursor move-Methode

Tritt auf, wenn der Cursor über den Tablet-Digitalisierer bewegt wird.

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

*TCID* 
</dt> <dd>

Eindeutiger dentifier des Tablet-Digitalisierungsprogramms.

</dd> <dt>

*zid* 
</dt> <dd>

Eindeutiger Bezeichner des Tablettstifts.

</dd> <dt>

*hWnd* 
</dt> <dd>

Das Fenster, in dem der Cursor verschoben wurde.

</dd> <dt>

*XPos* 
</dt> <dd>

Die X-Position des Tablettstifts.

</dd> <dt>

*YPos* 
</dt> <dd>

Die Y-Position des Tablettstifts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                            | Beschreibung                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                       |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Es ist ein unbekannter Fehler aufgetreten.<br/> |



 

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

 

 




