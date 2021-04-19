---
description: 'Die TranslateAccelerator-Methode weist die Eigenschaften Seite an, eine Tastatureingabe zu verarbeiten. Diese Methode implementiert die IPropertyPage:: TranslateAccelerator-Methode.'
ms.assetid: 2da214c9-35dc-470c-9b7f-2f4ef6bcd40a
title: Cbasepropertypage. TranslateAccelerator-Methode (cprop. h)
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
ms.openlocfilehash: 3116e85eec8fbf3a00bf434a1f88c8cac662ed0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355272"
---
# <a name="cbasepropertypagetranslateaccelerator-method"></a>Cbasepropertypage. TranslateAccelerator-Methode

Die- `TranslateAccelerator` Methode weist die Eigenschaften Seite an, eine Tastatureingabe zu verarbeiten. Diese Methode implementiert die **IPropertyPage:: TranslateAccelerator** -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT TranslateAccelerator(
   LPMSG lpMsg
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lpmsg* 
</dt> <dd>

Zeiger auf eine **msg** -Struktur, die den zu verarbeitenden Tastatur Strich beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "E \_ notimpl" zurück.

## <a name="remarks"></a>Bemerkungen

Überschreiben Sie diese Methode, wenn Sie für die Eigenschaften Seite Tastaturbeschleuniger bereitstellen möchten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepropertypage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




