---
description: Ruft das angegebene Schaltflächen Objekt aus einem Tablet Tablettstift ab.
ms.assetid: 83a26703-4501-4f43-9e86-c5c753347012
title: 'Itabletcursor:: getbutton-Methode'
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
ms.openlocfilehash: 0b9e8e1337cacdb26d8c124d10e0a886748e70fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349352"
---
# <a name="itabletcursorgetbutton-method"></a>Itabletcursor:: getbutton-Methode

Ruft das angegebene Schaltflächen Objekt aus einem Tablet Tablettstift ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetButton(
  [in]  ULONG               iButton,
  [out] ITabletCursorButton **ppButton
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iButton* \[ in\]
</dt> <dd>

Der Bezeichner der abzurufenden Schaltfläche.

</dd> <dt>

*ppbutton* \[ vorgenommen\]
</dt> <dd>

Das durch den *iButton* -Parameter angegebene Schaltflächen Objekt.

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

[**Itabletcursor-Schnittstelle**](itabletcursor.md)
</dt> </dl>

 

 




