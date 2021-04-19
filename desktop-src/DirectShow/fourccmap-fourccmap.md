---
description: Eine Konstruktormethode, die die Zuordnung zwischen den DWORD-Typen für das Format "im Stil" und "GUID" im alten Stil ermöglicht. Diese Methode verwendet keine Parameter.
ms.assetid: 2152803c-f45f-43b0-9207-4eaeddf5eeb6
title: 'Fourccmap:: fourccmap-Konstruktor (FourCC. h)-keine Parameter'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.FOURCCMap
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd37ac842ab46c0d46fb3db1567d42274a026c47
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106360250"
---
# <a name="fourccmapfourccmap-constructor-fourcch---no-parameters"></a><span data-ttu-id="e0da1-104">Fourccmap:: fourccmap-Konstruktor (FourCC. h)-keine Parameter</span><span class="sxs-lookup"><span data-stu-id="e0da1-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - No parameters</span></span>

<span data-ttu-id="e0da1-105">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="e0da1-105">Constructor method.</span></span> <span data-ttu-id="e0da1-106">Der-konstuktor stellt die Zuordnung zwischen den **DWORD** -Typen für das Multimedia-Format im alten Stil und **GUID** -Untertypen bereit.</span><span class="sxs-lookup"><span data-stu-id="e0da1-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0da1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0da1-107">Syntax</span></span>


```C++
FOURCCMap();
```



## <a name="parameters"></a><span data-ttu-id="e0da1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0da1-108">Parameters</span></span>

<span data-ttu-id="e0da1-109">Dieser Konstruktor weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="e0da1-109">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0da1-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0da1-110">Remarks</span></span>

<span data-ttu-id="e0da1-111">Wenn dieses Objekt mit dem **FourCC** -Code erstellt wird, wird eine **GUID** erstellt, um Sie abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="e0da1-111">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="e0da1-112">Wenn dieses Objekt mit einer vorhandenen **GUID** erstellt wird, wird der **FourCC** -Wert des-Objekts auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e0da1-112">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="e0da1-113">Danach kann der **FourCC** -Wert mit den Element Funktionen [**setfourcc**](fourccmap-setfourcc.md) und [**getfourcc**](fourccmap-getfourcc.md) festgelegt oder abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e0da1-113">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0da1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e0da1-114">Requirements</span></span>


| <span data-ttu-id="e0da1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e0da1-115">Requirement</span></span> | <span data-ttu-id="e0da1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e0da1-116">Value</span></span> |
|-|-|
| <span data-ttu-id="e0da1-117">Header</span><span class="sxs-lookup"><span data-stu-id="e0da1-117">Header</span></span>  | <span data-ttu-id="e0da1-118">FourCC. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="e0da1-118">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="e0da1-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e0da1-119">Library</span></span> | <span data-ttu-id="e0da1-120">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="e0da1-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



## <a name="see-also"></a><span data-ttu-id="e0da1-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0da1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0da1-122">**Fourccmap-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e0da1-122">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




