---
description: Ruft ein Rechteck ab, das den maximalen Eingabebereich des Tabletts darstellt.
ms.assetid: 98facd24-b019-40d1-afe1-28c9a78cae80
title: ITablet::GetMaxInputRect-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetMaxInputRect
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 422c64a8f5f77b354f02ab9601f7a0c888669d61783afb636816efbdc2e13b27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883540"
---
# <a name="itabletgetmaxinputrect-method"></a>ITablet::GetMaxInputRect-Methode

Ruft ein Rechteck ab, das den maximalen Eingabebereich des Tabletts darstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMaxInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*prcInput* \[ out\]
</dt> <dd>

Zeiger auf das Rechteck, das den maximalen Eingabebereich des Tablets darstellt.

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

[**ITablet-Schnittstelle**](itablet.md)
</dt> </dl>

 

 




