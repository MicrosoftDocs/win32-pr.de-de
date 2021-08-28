---
description: Die TranslateAccelerator-Methode weist die Eigenschaftenseite an, eine Tastatureingabe zu verarbeiten. Diese Methode implementiert die IPropertyPage::TranslateAccelerator-Methode.
ms.assetid: 2da214c9-35dc-470c-9b7f-2f4ef6bcd40a
title: CBasePropertyPage.TranslateAccelerator-Methode (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.TranslateAccelerator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc86d50c5692f48c7fb00b45228b13c88c96137473cee3609013f782a0a2d7ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502840"
---
# <a name="cbasepropertypagetranslateaccelerator-method"></a>CBasePropertyPage.TranslateAccelerator-Methode

Die `TranslateAccelerator` -Methode weist die Eigenschaftenseite an, eine Tastatureingabe zu verarbeiten. Diese Methode implementiert die **IPropertyPage::TranslateAccelerator-Methode.**

## <a name="syntax"></a>Syntax


```C++
HRESULT TranslateAccelerator(
   LPMSG lpMsg
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpMsg* 
</dt> <dd>

Zeiger auf eine **MSG-Struktur,** die die zu verarbeitende Tastatureingabe beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ NOTIMPL zurück.

## <a name="remarks"></a>Hinweise

Überschreiben Sie diese Methode, wenn Sie Zugriffstasten für die Eigenschaftenseite bereitstellen möchten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop.h (include Streams.h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePropertyPage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




