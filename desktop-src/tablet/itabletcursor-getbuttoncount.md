---
description: Ruft die Anzahl der Schaltflächen auf dem Tablettstift ab.
ms.assetid: ae4ce670-769a-4f00-b728-285020f09934
title: ITabletCursor::GetButtonCount-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButtonCount
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 82a0825d64bc93601b933a98b3a7e0e3f321954d2fb2d7aa285d8d08a315545c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119336020"
---
# <a name="itabletcursorgetbuttoncount-method"></a>ITabletCursor::GetButtonCount-Methode

Ruft die Anzahl der Schaltflächen auf dem Tablettstift ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetButtonCount(
  [out] ULONG *pcButtons
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcButtons* \[ out\]
</dt> <dd>

Die Anzahl der Schaltflächen auf dem Tablettstift.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ITabletCursor-Schnittstelle**](itabletcursor.md)
</dt> </dl>

 

 




