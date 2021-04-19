---
description: Ruft die maximale Bytegröße ab, die für den aktuellen Stream benötigt wird, ohne die Versionsnummer.
ms.assetid: ca1a68e2-02b4-4eea-916a-e0418ae811ae
title: Cpersiststream. sizemax-Methode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.SizeMax
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afa29e2c81cc454a9e85b9038486221f6f44aaf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370740"
---
# <a name="cpersiststreamsizemax-method"></a><span data-ttu-id="8b9cd-103">Cpersiststream. sizemax-Methode</span><span class="sxs-lookup"><span data-stu-id="8b9cd-103">CPersistStream.SizeMax method</span></span>

<span data-ttu-id="8b9cd-104">Ruft die maximale Bytegröße ab, die für den aktuellen Stream benötigt wird, ohne die Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="8b9cd-104">Retrieves the maximum byte size needed for the current stream, not including the version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b9cd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b9cd-105">Syntax</span></span>


```C++
virtual int SizeMax();
```



## <a name="parameters"></a><span data-ttu-id="8b9cd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b9cd-106">Parameters</span></span>

<span data-ttu-id="8b9cd-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="8b9cd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8b9cd-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b9cd-108">Return value</span></span>

<span data-ttu-id="8b9cd-109">Gibt die Anzahl von Bytes zurück, die für Daten benötigt werden, ohne die Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="8b9cd-109">Returns the number of bytes needed for data, not including the version number.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b9cd-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b9cd-110">Remarks</span></span>

<span data-ttu-id="8b9cd-111">Die Standardversion gibt 0 (null) zurück. Er sollte überschrieben werden, um einen anderen passenden Wert bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8b9cd-111">The default version returns zero; it should be overridden to provide some other appropriate value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b9cd-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b9cd-112">Requirements</span></span>



| <span data-ttu-id="8b9cd-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b9cd-113">Requirement</span></span> | <span data-ttu-id="8b9cd-114">Wert</span><span class="sxs-lookup"><span data-stu-id="8b9cd-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b9cd-115">Header</span><span class="sxs-lookup"><span data-stu-id="8b9cd-115">Header</span></span><br/>  | <dl> <span data-ttu-id="8b9cd-116"><dt>PStream. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b9cd-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8b9cd-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8b9cd-117">Library</span></span><br/> | <dl> <span data-ttu-id="8b9cd-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8b9cd-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b9cd-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b9cd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b9cd-120">**Cpersiststream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8b9cd-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




