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
# <a name="declare_iunknown"></a><span data-ttu-id="824f0-103">\_IUnknown deklarieren</span><span class="sxs-lookup"><span data-stu-id="824f0-103">DECLARE\_IUNKNOWN</span></span>

<span data-ttu-id="824f0-104">Das " **Declare \_ IUnknown** "-Makro deklariert die drei Methoden der Basisschnittstelle für eine neue Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="824f0-104">The **DECLARE\_IUNKNOWN** macro declares the three methods of the base interface for a new interface.</span></span>

<span data-ttu-id="824f0-105">**Syntax**</span><span class="sxs-lookup"><span data-stu-id="824f0-105">**Syntax**</span></span>

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

## <a name="remarks"></a><span data-ttu-id="824f0-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="824f0-106">Remarks</span></span>

<span data-ttu-id="824f0-107">Wenn Sie eine neue Schnittstelle erstellen, muss Sie von **IUnknown** abgeleitet werden, die drei Methoden aufweist: **QueryInterface**, **adressf** und **Release**.</span><span class="sxs-lookup"><span data-stu-id="824f0-107">When you create a new interface, it must derive from **IUnknown**, which has three methods: **QueryInterface**, **AddRef**, and **Release**.</span></span> <span data-ttu-id="824f0-108">Dieses Makro vereinfacht den Deklarations Prozess durch Deklarieren jeder dieser Methoden für die neue Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="824f0-108">This macro simplifies the declaration process by declaring each of these methods for the new interface.</span></span>

<span data-ttu-id="824f0-109">Dieses Makro funktioniert nur mit Klassen, die direkt oder indirekt von der [**cunknown**](cunknown.md) -Klasse abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="824f0-109">This macro works only with classes that derive, directly or indirectly, from the [**CUnknown**](cunknown.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="824f0-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="824f0-110">Requirements</span></span>



| <span data-ttu-id="824f0-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="824f0-111">Requirement</span></span> | <span data-ttu-id="824f0-112">Wert</span><span class="sxs-lookup"><span data-stu-id="824f0-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="824f0-113">Header</span><span class="sxs-lookup"><span data-stu-id="824f0-113">Header</span></span><br/>  | <dl> <span data-ttu-id="824f0-114"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="824f0-114"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="824f0-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="824f0-115">Library</span></span><br/> | <dl> <span data-ttu-id="824f0-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="824f0-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="824f0-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="824f0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="824f0-118">**COM-Hilfsfunktionen**</span><span class="sxs-lookup"><span data-stu-id="824f0-118">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="824f0-119">**Cunknown:: GetOwner**</span><span class="sxs-lookup"><span data-stu-id="824f0-119">**CUnknown::GetOwner**</span></span>](cunknown-getowner.md)
</dt> <dt>

[<span data-ttu-id="824f0-120">Implementieren von IUnknown</span><span class="sxs-lookup"><span data-stu-id="824f0-120">How to Implement IUnknown</span></span>](how-to-implement-iunknown.md)
</dt> </dl>

 

 




