---
description: 'Die Move-Methode positioniert und ändert die Größe des Dialog Felds. Diese Methode implementiert die IPropertyPage:: Move-Methode.'
ms.assetid: b6cabb5c-196d-489b-9dd4-194d26f4de83
title: Cbasepropertypage. Move-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Move
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d293f6ccb6a1bcd730ce997367c179f1747f66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366748"
---
# <a name="cbasepropertypagemove-method"></a>Cbasepropertypage. Move-Methode

Die `Move` -Methode positioniert und ändert die Größe des Dialog Felds. Diese Methode implementiert die **IPropertyPage:: Move** -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Move(
   LPCRECT prect
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vorab ausführen* 
</dt> <dd>

Ein Zeiger auf eine **Rect** -Struktur, die die Positionsinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                  | Beschreibung                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>                   |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>    | **Null** -Zeigerargument.<br/> |
| <dl> <dt>**E \_ unerwartet**</dt> </dl> | Unerwarteter Fehler.<br/>        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepropertypage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




