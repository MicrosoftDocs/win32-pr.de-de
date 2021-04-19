---
description: Die Methode "kreateinstance" erstellt eine Instanz des-Objekts. Diese Methode unterstützt die Erstellung des Objekts über eine Klassenfactory. Weitere Informationen finden Sie unter cfactoriytemplate.
ms.assetid: 88dfa933-6fa1-4b57-8b0d-579233fa960c
title: Cseekingpassthru. kreateinzustance-Methode (seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3640cbd6a0a3e582899e7f5cd349ca48498f3532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359360"
---
# <a name="cseekingpassthrucreateinstance-method"></a>Cseekingpassthru. kreateinzustance-Methode

Die- `CreateInstance` Methode erstellt eine Instanz des-Objekts. Diese Methode unterstützt die Erstellung des Objekts über eine Klassenfactory. Weitere Informationen finden Sie unter [**cfactoriytemplate**](cfactorytemplate.md).

## <a name="syntax"></a>Syntax


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Kro* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts. Andernfalls legen Sie diesen Parameter auf **null** fest.

</dd> <dt>

*PHR* 
</dt> <dd>

Zeiger auf einen **HRESULT** -Wert. Ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf ein neues **cseekingpassthru** -Objekt zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Seekpt. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cseekingpassthru-Klasse**](cseekingpassthru.md)
</dt> </dl>

 

 




