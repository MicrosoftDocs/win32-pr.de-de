---
description: 'Die setpagesite-Methode initialisiert die Eigenschaften Seite und stellt einen Zeiger auf die ipropertypagesite-Schnittstelle des Eigenschaften Frames bereit. Diese Methode implementiert die IPropertyPage:: setpagesite-Methode.'
ms.assetid: 16c4633f-2f91-4b1b-a47c-4ef945c3af00
title: Cbasepropertypage. setpagesite-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.SetPageSite
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a165ff60971cef3d2373e0f07b2abee554308279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370984"
---
# <a name="cbasepropertypagesetpagesite-method"></a>Cbasepropertypage. setpagesite-Methode

Die `SetPageSite` -Methode initialisiert die Eigenschaften Seite und stellt einen Zeiger auf die **ipropertypagesite** -Schnittstelle des Eigenschaften Frames bereit. Diese Methode implementiert die **IPropertyPage:: setpagesite** -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPageSite(
   IPropertyPageSite *pPageSite
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppagesite* 
</dt> <dd>

Zeiger auf die **ipropertypagesite** -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                  | Beschreibung                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>            |
| <dl> <dt>**E \_ unerwartet**</dt> </dl> | Unerwarteter Fehler.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die-Methode speichert den *ppagesite* -Zeiger in der Member-Variable [**cbasepropertypage:: m \_ ppagesite**](cbasepropertypage-m-ppagesite.md) .

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepropertypage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




