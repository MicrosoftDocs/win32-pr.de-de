---
description: Die CreateInstance-Methode ruft die Objekterstellungsfunktion für die -Klasse auf.
ms.assetid: 8a7d5c56-867d-432d-a0c2-97b8e3cf8a69
title: CFactoryTemplate.CreateInstance-Methode (Combase.h)
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
ms.openlocfilehash: 816d690a7e57df83b3f521f4591c3334269d0fccebbaeac480e7aacb46253273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074204"
---
# <a name="cfactorytemplatecreateinstance-method"></a>CFactoryTemplate.CreateInstance-Methode

Die `CreateInstance` -Methode ruft die Objekterstellungsfunktion für die -Klasse auf.

## <a name="syntax"></a>Syntax


```C++
CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Punk* 
</dt> <dd>

Zeiger auf die aggregierende **IUnknown-Schnittstelle.**

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf eine Variable, die einen **HRESULT-Wert** empfängt, der den Erfolg oder Fehler der Methode angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt eine Instanz des Klassenobjekts zurück.

## <a name="remarks"></a>Hinweise

Die **IClassFactory::CreateInstance-Methode ruft** diese Klassenmethode auf. Diese Methode ruft die Funktion auf, auf die die [**CFactoryTemplate::m \_ lpfnNew-Membervariable**](cfactorytemplate-m-lpfnnew.md) verweist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CFactoryTemplate-Klasse**](cfactorytemplate.md)
</dt> </dl>

 

 




