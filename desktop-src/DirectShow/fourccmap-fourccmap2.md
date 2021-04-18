---
description: Eine Konstruktormethode, die die Zuordnung zwischen den DWORD-Typen für das Format "im Stil" und "GUID" im alten Stil ermöglicht. Diese Methode verwendet den Parameter "FourCC".
ms.assetid: 35344aae-ed87-4e5e-8824-84f5482b332e
title: 'Fourccmap:: fourccmap-Konstruktor (FourCC. h)-FourCC-Parameter'
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
ms.openlocfilehash: cbcd5e8a7c37d3265f508ac7632ffd4b18c8a00f
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106364406"
---
# <a name="fourccmapfourccmap-constructor-fourcch---fourcc-parameter"></a><span data-ttu-id="4a6e0-104">Fourccmap:: fourccmap-Konstruktor (FourCC. h)-FourCC-Parameter</span><span class="sxs-lookup"><span data-stu-id="4a6e0-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - Fourcc parameter</span></span>

<span data-ttu-id="4a6e0-105">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="4a6e0-105">Constructor method.</span></span> <span data-ttu-id="4a6e0-106">Der-konstuktor stellt die Zuordnung zwischen den **DWORD** -Typen für das Multimedia-Format im alten Stil und **GUID** -Untertypen bereit.</span><span class="sxs-lookup"><span data-stu-id="4a6e0-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a6e0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a6e0-107">Syntax</span></span>


```C++
FOURCCMap(
   DWORD Fourcc
);
```



## <a name="parameters"></a><span data-ttu-id="4a6e0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a6e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a6e0-109">*FourCC*</span><span class="sxs-lookup"><span data-stu-id="4a6e0-109">*Fourcc*</span></span> 
</dt> <dd>

<span data-ttu-id="4a6e0-110">**DWORD** , das den FourCC angibt.</span><span class="sxs-lookup"><span data-stu-id="4a6e0-110">**DWORD** that specifies the FOURCC.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4a6e0-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a6e0-111">Remarks</span></span>

<span data-ttu-id="4a6e0-112">Wenn dieses Objekt mit dem **FourCC** -Code erstellt wird, wird eine **GUID** erstellt, um Sie abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="4a6e0-112">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="4a6e0-113">Wenn dieses Objekt mit einer vorhandenen **GUID** erstellt wird, wird der **FourCC** -Wert des-Objekts auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4a6e0-113">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="4a6e0-114">Danach kann der **FourCC** -Wert mit den Element Funktionen [**setfourcc**](fourccmap-setfourcc.md) und [**getfourcc**](fourccmap-getfourcc.md) festgelegt oder abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="4a6e0-114">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a6e0-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a6e0-115">Requirements</span></span>

| <span data-ttu-id="4a6e0-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a6e0-116">Requirement</span></span> | <span data-ttu-id="4a6e0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4a6e0-117">Value</span></span> |
|-|-|
| <span data-ttu-id="4a6e0-118">Header</span><span class="sxs-lookup"><span data-stu-id="4a6e0-118">Header</span></span>  | <span data-ttu-id="4a6e0-119">FourCC. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="4a6e0-119">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="4a6e0-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4a6e0-120">Library</span></span> | <span data-ttu-id="4a6e0-121">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="4a6e0-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="4a6e0-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a6e0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a6e0-123">**Fourccmap-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4a6e0-123">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




