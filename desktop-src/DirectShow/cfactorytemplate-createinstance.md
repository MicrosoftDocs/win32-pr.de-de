---
description: Die Methode "kreateinstance" Ruft die Objekt Erstellungs Funktion für die-Klasse auf.
ms.assetid: 8a7d5c56-867d-432d-a0c2-97b8e3cf8a69
title: Cfactorytemplate. kreateinstance-Methode (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CFactoryTemplate.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0f67ba528943bc2a468419fc84db44359745d4a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355954"
---
# <a name="cfactorytemplatecreateinstance-method"></a>Cfactorytemplate. kreateinstance-Methode

Die `CreateInstance` -Methode ruft die Objekt Erstellungs Funktion für die-Klasse auf.

## <a name="syntax"></a>Syntax


```C++
CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Kro* 
</dt> <dd>

Zeiger auf die Aggregations- **IUnknown** -Schnittstelle.

</dd> <dt>

*PHR* 
</dt> <dd>

Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine Instanz des-Klassen Objekts zurück.

## <a name="remarks"></a>Bemerkungen

Die **IClassFactory:: deateinstance** -Methode ruft diese Klassenmethode auf. Diese Methode ruft die-Funktion auf, auf die von der [**cfactorytemplate:: m \_ lpfnnew**](cfactorytemplate-m-lpfnnew.md) -Member-Variable verwiesen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cfactorytemplate-Klasse**](cfactorytemplate.md)
</dt> </dl>

 

 




