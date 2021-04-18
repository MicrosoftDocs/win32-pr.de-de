---
description: Die GetInterface-Funktion Ruft einen Schnittstellen Zeiger ab.
ms.assetid: 75fe8849-c779-4d47-a5ff-5a23308c8a21
title: GetInterface-Funktion (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetInterface
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 317f08af2a4ff0e9410c61da8b19d14735a14f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360962"
---
# <a name="getinterface-function"></a>GetInterface-Funktion

Die- `GetInterface` Funktion Ruft einen Schnittstellen Zeiger ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetInterface(
   LPUNKNOWN pUnk,
   void      **ppv
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Kro* 
</dt> <dd>

Zeiger auf die **IUnknown** -Schnittstelle.

</dd> <dt>

*PPV* 
</dt> <dd>

Adresse eines Zeigers auf die abgerufene Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion führt ein Thread sicheres Inkrement des Verweis zählungs Elements aus. Um die Schnittstelle abzurufen und einen Verweis hinzuzufügen, rufen Sie diese Funktion von der über schreibenden Implementierung der **inondelegatingunknown:: nondelegatingqueryinterface** -Methode auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COM-Hilfsfunktionen**](com-helper-functions.md)
</dt> <dt>

[**Inondelegatingunknown**](inondelegatingunknown.md)
</dt> </dl>

 

 




