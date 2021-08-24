---
description: Ruft das angegebene Schaltflächenobjekt aus einem Tablettstift ab.
ms.assetid: 83a26703-4501-4f43-9e86-c5c753347012
title: ITabletCursor::GetButton-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor.GetButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 49306160a0c14badc23cb2f359400d0fb2947012078a9318315a6697050f48dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938630"
---
# <a name="itabletcursorgetbutton-method"></a>ITabletCursor::GetButton-Methode

Ruft das angegebene Schaltflächenobjekt aus einem Tablettstift ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetButton(
  [in]  ULONG               iButton,
  [out] ITabletCursorButton **ppButton
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iButton* \[ In\]
</dt> <dd>

Bezeichner der abzurufenden Schaltfläche.

</dd> <dt>

*ppButton* \[ out\]
</dt> <dd>

Das durch den *iButton-Parameter angegebene Schaltflächenobjekt.*

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

[**ITabletCursor-Schnittstelle**](itabletcursor.md)
</dt> </dl>

 

 




