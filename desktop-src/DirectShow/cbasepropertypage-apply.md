---
description: 'Die Apply-Methode wendet die aktuellen Eigenschaften Seiten Werte auf das-Objekt an, das der Eigenschaften Seite zugeordnet ist. Diese Methode implementiert die IPropertyPage:: Apply-Methode.'
ms.assetid: 9fe759d1-2b46-4489-b7b8-b5a35330091d
title: Cbasepropertypage. Apply-Methode (cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Apply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21d1208979cca167b059cb720c492ac51c362c39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372563"
---
# <a name="cbasepropertypageapply-method"></a>Cbasepropertypage. Apply-Methode

Die- `Apply` Methode wendet die aktuellen Eigenschaften Seiten Werte auf das-Objekt an, das der Eigenschaften Seite zugeordnet ist. Diese Methode implementiert die **IPropertyPage:: apply** -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT Apply();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                                  | Beschreibung                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>            |
| <dl> <dt>**E \_ unerwartet**</dt> </dl> | Unerwarteter Fehler.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn das [**\_ bdirty-Flag "cbasepropertypage:: m**](cbasepropertypage-m-bdirty.md) " auf " **true**" festgelegt ist, ruft diese Methode die [**cbasepropertypage:: onapplychanges**](cbasepropertypage-onapplychanges.md) -Methode auf. Überschreiben Sie **onapplychanges** , um die Änderungen auf das-Objekt anzuwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Cprop. h (Include Streams. h)</dt> </dl>                                                                                     |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasepropertypage-Klasse**](cbasepropertypage.md)
</dt> </dl>

 

 




