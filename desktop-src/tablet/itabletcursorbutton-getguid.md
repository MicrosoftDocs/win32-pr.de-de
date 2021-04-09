---
description: Ruft den eindeutigen Bezeichner der Tablettstiftschaltfläche ab.
ms.assetid: 06bd6a84-46cd-4c62-92d6-50caae359e43
title: 'Itabletcurrsorbutton:: GetGuid-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton.GetGuid
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 21d63ef0c934e96bc93b5384cab1e67f9dd452d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042717"
---
# <a name="itabletcursorbuttongetguid-method"></a>Itabletcurrsorbutton:: GetGuid-Methode

Ruft den eindeutigen Bezeichner der Tablettstiftschaltfläche ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetGuid(
  [out] GUID *pguidBtn
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pguidbtn* \[ vorgenommen\]
</dt> <dd>

Ein eindeutiger Wert, der die Tablettstiftschaltfläche identifiziert.

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

[**Itabletcursor Button-Schnittstelle**](itabletcursorbutton.md)
</dt> </dl>

 

 




