---
description: Ruft den Klassen Bezeichner für diesen Filter ab.
ms.assetid: f0559437-5d0d-4522-a3dc-947e3494b576
title: Cpersiststream. GetClassID-Methode (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7603541eae4f431327a91777488a740afb7f628b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368459"
---
# <a name="cpersiststreamgetclassid-method"></a><span data-ttu-id="930c0-103">Cpersiststream. GetClassID-Methode</span><span class="sxs-lookup"><span data-stu-id="930c0-103">CPersistStream.GetClassID method</span></span>

<span data-ttu-id="930c0-104">Ruft den Klassen Bezeichner für diesen Filter ab.</span><span class="sxs-lookup"><span data-stu-id="930c0-104">Retrieves the class identifier for this filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="930c0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="930c0-105">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="930c0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="930c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="930c0-107">*pclsid*</span><span class="sxs-lookup"><span data-stu-id="930c0-107">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="930c0-108">Zeiger auf eine CLSID-Struktur.</span><span class="sxs-lookup"><span data-stu-id="930c0-108">Pointer to a CLSID structure.</span></span> <span data-ttu-id="930c0-109">Kopieren Sie die Klassen-ID hier.</span><span class="sxs-lookup"><span data-stu-id="930c0-109">Copy your class ID to here.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="930c0-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="930c0-110">Return value</span></span>

<span data-ttu-id="930c0-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="930c0-111">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="930c0-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="930c0-112">Requirements</span></span>



| <span data-ttu-id="930c0-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="930c0-113">Requirement</span></span> | <span data-ttu-id="930c0-114">Wert</span><span class="sxs-lookup"><span data-stu-id="930c0-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="930c0-115">Header</span><span class="sxs-lookup"><span data-stu-id="930c0-115">Header</span></span><br/>  | <dl> <span data-ttu-id="930c0-116"><dt>PStream. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="930c0-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="930c0-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="930c0-117">Library</span></span><br/> | <dl> <span data-ttu-id="930c0-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="930c0-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="930c0-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="930c0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="930c0-120">**Cpersiststream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="930c0-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




