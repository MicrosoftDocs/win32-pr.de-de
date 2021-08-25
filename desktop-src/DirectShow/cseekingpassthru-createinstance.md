---
description: Die CreateInstance-Methode erstellt eine Instanz des -Objekts. Diese Methode unterstützt die Erstellung des Objekts über eine Klassenfactory. Weitere Informationen finden Sie unter CFactoryTemplate.
ms.assetid: 88dfa933-6fa1-4b57-8b0d-579233fa960c
title: CSeekingPassThru.CreateInstance-Methode (Seekpt.h)
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
ms.openlocfilehash: 5060e2e9842022d89c49e01b56967a92b71c5752e01239fd970c881ccb509cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908060"
---
# <a name="cseekingpassthrucreateinstance-method"></a>CSeekingPassThru.CreateInstance-Methode

Die `CreateInstance` -Methode erstellt eine Instanz des -Objekts. Diese Methode unterstützt die Erstellung des Objekts über eine Klassenfactory. Weitere Informationen finden Sie unter [**CFactoryTemplate**](cfactorytemplate.md).

## <a name="syntax"></a>Syntax


```C++
static CUnknown* CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Punk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle** des aggregierenden Objekts. Legen Sie andernfalls diesen Parameter auf **NULL** fest.

</dd> <dt>

*Phr* 
</dt> <dd>

Zeiger auf einen **HRESULT-Wert.** Ignoriert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Zeiger auf ein neues **CSeekingPassThru-Objekt zurück.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Seekpt.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CSeekingPassThru-Klasse**](cseekingpassthru.md)
</dt> </dl>

 

 




