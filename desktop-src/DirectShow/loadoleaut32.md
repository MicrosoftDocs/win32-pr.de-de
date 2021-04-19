---
description: Die LoadOLEAut32-Funktion lädt die Automation Dynamic-Link Library (OleAut32.dll).
ms.assetid: af907341-1e2c-4c63-bf4e-d6c49b4f6a6e
title: LoadOLEAut32-Funktion (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadOLEAut32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b23bad7e445eebc78ecf8a849ddde8fc23746131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369949"
---
# <a name="loadoleaut32-function"></a><span data-ttu-id="1f5b5-103">LoadOLEAut32-Funktion</span><span class="sxs-lookup"><span data-stu-id="1f5b5-103">LoadOLEAut32 function</span></span>

<span data-ttu-id="1f5b5-104">Die **LoadOLEAut32** -Funktion lädt die Automation Dynamic-Link Library (OleAut32.dll).</span><span class="sxs-lookup"><span data-stu-id="1f5b5-104">The **LoadOLEAut32** function loads the Automation dynamic-link library (OleAut32.dll).</span></span>

## <a name="syntax"></a><span data-ttu-id="1f5b5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f5b5-105">Syntax</span></span>


```C++
HINSTANCE LoadOLEAut32(void);
```



## <a name="parameters"></a><span data-ttu-id="1f5b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f5b5-106">Parameters</span></span>

<span data-ttu-id="1f5b5-107">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1f5b5-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f5b5-108">Return value</span></span>

<span data-ttu-id="1f5b5-109">Gibt ein Handle für eine Automation-dll-Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-109">Returns a handle to an Automation DLL instance.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f5b5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f5b5-110">Remarks</span></span>

<span data-ttu-id="1f5b5-111">Wenn der [**cbaseobject-debugtor**](cbaseobject.md) das Objekt zerstört, das OleAut32.dll geladen hat, wird die Bibliothek entladen, wenn Sie noch geladen ist.</span><span class="sxs-lookup"><span data-stu-id="1f5b5-111">When the [**CBaseObject**](cbaseobject.md) destructor destroys the object that loaded OleAut32.dll, it will unload the library if it is still loaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f5b5-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f5b5-112">Requirements</span></span>



| <span data-ttu-id="1f5b5-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f5b5-113">Requirement</span></span> | <span data-ttu-id="1f5b5-114">Wert</span><span class="sxs-lookup"><span data-stu-id="1f5b5-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f5b5-115">Header</span><span class="sxs-lookup"><span data-stu-id="1f5b5-115">Header</span></span><br/>  | <dl> <span data-ttu-id="1f5b5-116"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f5b5-116"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1f5b5-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1f5b5-117">Library</span></span><br/> | <dl> <span data-ttu-id="1f5b5-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1f5b5-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f5b5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f5b5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f5b5-120">**COM-Hilfsfunktionen**</span><span class="sxs-lookup"><span data-stu-id="1f5b5-120">**COM Helper Functions**</span></span>](com-helper-functions.md)
</dt> </dl>

 

 




