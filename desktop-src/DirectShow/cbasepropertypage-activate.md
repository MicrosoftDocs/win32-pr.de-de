---
description: 'Mit der Methode "aktivieren" wird das Dialogfeld Fenster erstellt. Diese Methode implementiert die IPropertyPage:: Aktivierungs-Methode.'
ms.assetid: 8f030dc5-1d14-46b5-9d40-7f07a1177dbe
title: Cbasepropertypage. Aktivierungs-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Activate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b851cfc4490d25e7e30dfd2cf0e7c33b0e76224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368425"
---
# <a name="cbasepropertypageactivate-method"></a>Cbasepropertypage. Aktivierungs-Methode

Mit der- `Activate` Methode wird das Dialogfeld Fenster erstellt. Diese Methode implementiert die **IPropertyPage:: Aktivierungs** -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Activate(
   HWND    hwndParent,
   LPCRECT prect,
   BOOL    fModal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* 
</dt> <dd>

Handle für das übergeordnete Fenster des Dialog Felds.

</dd> <dt>

*vorab ausführen* 
</dt> <dd>

Ein Zeiger auf eine **Rect** -Struktur, die Positionsinformationen für das Dialogfeld enthält.

</dd> <dt>

*für den modalen* 
</dt> <dd>

Boolescher Wert, der angibt, ob der Dialogfeld Rahmen Modal (**true**) oder nicht modelliert (**false**) ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                   | Beschreibung                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                   |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>       |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>     | **Null** -Zeigerargument.<br/> |
| <dl> <dt>**E \_ unerwartet**</dt> </dl>  | Unerwarteter Fehler.<br/>        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepropertypage-Klasse**](cbasepropertypage.md)
</dt> <dt>

[**Cbasepropertypage:: onaktivierungs**](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




