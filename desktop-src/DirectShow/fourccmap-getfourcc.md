---
description: Ruft das FourCC&\# 160; DWORD aus dem fourccmap-Objekt ab.
ms.assetid: bb382a57-8499-44c0-b287-2d31f5f5d1d0
title: 'Fourccmap:: getfourcc-Methode (FourCC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.GetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c76493ff172f7a5611367fd50aa3b7957cf5441b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369448"
---
# <a name="fourccmapgetfourcc-method"></a><span data-ttu-id="4b4fd-103">Fourccmap:: getfourcc-Methode</span><span class="sxs-lookup"><span data-stu-id="4b4fd-103">FOURCCMap::GetFOURCC method</span></span>

<span data-ttu-id="4b4fd-104">Ruft das **FourCC** **DWORD** aus dem [**fourccmap**](fourccmap.md) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="4b4fd-104">Retrieves the **FOURCC** **DWORD** from the [**FOURCCMap**](fourccmap.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b4fd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b4fd-105">Syntax</span></span>


```C++
DWORD GetFOURCC();
```



## <a name="parameters"></a><span data-ttu-id="4b4fd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b4fd-106">Parameters</span></span>

<span data-ttu-id="4b4fd-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4b4fd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b4fd-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4b4fd-108">Return value</span></span>

<span data-ttu-id="4b4fd-109">Gibt den **FourCC** **DWORD** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4b4fd-109">Returns the **FOURCC** **DWORD** value.</span></span> <span data-ttu-id="4b4fd-110">Beachten Sie Folgendes: Wenn Sie eine **GUID** erstellen, die ursprünglich nicht von einem **FourCC** abgeleitet wurde, ist der Rückgabewert im Grunde zufällig.</span><span class="sxs-lookup"><span data-stu-id="4b4fd-110">Note that if you construct a **GUID** that was not originally derived from a **FOURCC**, the return value will be essentially random.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b4fd-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b4fd-111">Requirements</span></span>



| <span data-ttu-id="4b4fd-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b4fd-112">Requirement</span></span> | <span data-ttu-id="4b4fd-113">Wert</span><span class="sxs-lookup"><span data-stu-id="4b4fd-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b4fd-114">Header</span><span class="sxs-lookup"><span data-stu-id="4b4fd-114">Header</span></span><br/>  | <dl> <span data-ttu-id="4b4fd-115"><dt>FourCC. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b4fd-115"><dt>Fourcc.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="4b4fd-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4b4fd-116">Library</span></span><br/> | <dl> <span data-ttu-id="4b4fd-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4b4fd-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b4fd-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b4fd-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b4fd-119">**Fourccmap-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4b4fd-119">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




