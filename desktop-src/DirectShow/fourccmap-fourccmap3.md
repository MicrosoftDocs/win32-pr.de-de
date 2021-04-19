---
description: Eine Konstruktormethode, die die Zuordnung zwischen den DWORD-Typen für das Format "im Stil" und "GUID" im alten Stil ermöglicht. Diese Methode verwendet den pguid-Parameter.
ms.assetid: 4de6cb49-938e-42f8-8687-dc60a0f23e87
title: 'Fourccmap:: fourccmap-Konstruktor (FourCC. h)-pguid-Parameter'
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
ms.openlocfilehash: 3e36f0ea58c99930d4c6c2e0929f27a43184c6be
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2021
ms.locfileid: "106357294"
---
# <a name="fourccmapfourccmap-constructor-fourcch---pguid-parameter"></a><span data-ttu-id="c5e19-104">Fourccmap:: fourccmap-Konstruktor (FourCC. h)-pguid-Parameter</span><span class="sxs-lookup"><span data-stu-id="c5e19-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - pguid parameter</span></span>

<span data-ttu-id="c5e19-105">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="c5e19-105">Constructor method.</span></span> <span data-ttu-id="c5e19-106">Der-konstuktor stellt die Zuordnung zwischen den **DWORD** -Typen für das Multimedia-Format im alten Stil und **GUID** -Untertypen bereit.</span><span class="sxs-lookup"><span data-stu-id="c5e19-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5e19-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5e19-107">Syntax</span></span>


```C++
FOURCCMap(
   const GUID *pguid
);
```



## <a name="parameters"></a><span data-ttu-id="c5e19-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5e19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5e19-109">*pguid*</span><span class="sxs-lookup"><span data-stu-id="c5e19-109">*pguid*</span></span> 
</dt> <dd>

<span data-ttu-id="c5e19-110">Zeiger auf den Globally Unique Identifier (**GUID**).</span><span class="sxs-lookup"><span data-stu-id="c5e19-110">Pointer to the globally unique identifier (**GUID**).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5e19-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5e19-111">Remarks</span></span>

<span data-ttu-id="c5e19-112">Wenn dieses Objekt mit dem **FourCC** -Code erstellt wird, wird eine **GUID** erstellt, um Sie abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="c5e19-112">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="c5e19-113">Wenn dieses Objekt mit einer vorhandenen **GUID** erstellt wird, wird der **FourCC** -Wert des-Objekts auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c5e19-113">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="c5e19-114">Danach kann der **FourCC** -Wert mit den Element Funktionen [**setfourcc**](fourccmap-setfourcc.md) und [**getfourcc**](fourccmap-getfourcc.md) festgelegt oder abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c5e19-114">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5e19-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c5e19-115">Requirements</span></span>

| <span data-ttu-id="c5e19-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5e19-116">Requirement</span></span> | <span data-ttu-id="c5e19-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c5e19-117">Value</span></span> |
|-|-|
| <span data-ttu-id="c5e19-118">Header</span><span class="sxs-lookup"><span data-stu-id="c5e19-118">Header</span></span>  | <span data-ttu-id="c5e19-119">FourCC. h (Include Streams. h)</span><span class="sxs-lookup"><span data-stu-id="c5e19-119">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="c5e19-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c5e19-120">Library</span></span> | <span data-ttu-id="c5e19-121">"Straumbase. lib" (Einzelhandels Builds); "Straumbasd. lib" (Debugbuilds)</span><span class="sxs-lookup"><span data-stu-id="c5e19-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="c5e19-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5e19-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5e19-123">**Fourccmap-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c5e19-123">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




