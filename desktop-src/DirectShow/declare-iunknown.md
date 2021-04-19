---
description: Das "Declare \_ IUnknown"-Makro deklariert die drei Methoden der Basisschnittstelle für eine neue Schnittstelle.
ms.assetid: 3bf8e830-c923-4c31-8855-88fa08f80422
title: DECLARE_IUNKNOWN (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DECLARE_IUNKNOWN
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4823c1b4bd4832b1047a732bc503f04b4da65483
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367712"
---
# <a name="declare_iunknown"></a>\_IUnknown deklarieren

Das " **Declare \_ IUnknown** "-Makro deklariert die drei Methoden der Basisschnittstelle für eine neue Schnittstelle.

**Syntax**

``` syntax
#define DECLARE_IUNKNOWN                                        \
    STDMETHODIMP QueryInterface(REFIID riid, void **ppv) {      \
        return GetOwner()->QueryInterface(riid,ppv);            \
    };                                                          \
    STDMETHODIMP_(ULONG) AddRef() {                             \
        return GetOwner()->AddRef();                            \
    };                                                          \
    STDMETHODIMP_(ULONG) Release() {                            \
        return GetOwner()->Release();                           \
    };
```

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine neue Schnittstelle erstellen, muss Sie von **IUnknown** abgeleitet werden, die drei Methoden aufweist: **QueryInterface**, **adressf** und **Release**. Dieses Makro vereinfacht den Deklarations Prozess durch Deklarieren jeder dieser Methoden für die neue Schnittstelle.

Dieses Makro funktioniert nur mit Klassen, die direkt oder indirekt von der [**cunknown**](cunknown.md) -Klasse abgeleitet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COM-Hilfsfunktionen**](com-helper-functions.md)
</dt> <dt>

[**Cunknown:: GetOwner**](cunknown-getowner.md)
</dt> <dt>

[Implementieren von IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 




