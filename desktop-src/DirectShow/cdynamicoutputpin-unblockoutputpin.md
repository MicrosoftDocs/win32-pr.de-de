---
description: Die unblockoutputpin-Methode hebt die Blockierung der PIN auf. Wenn die Blockierung der PIN aufgehoben wird, kann Sie Beispiele liefern, das Ausgabeformat ändern und die Verbindung wiederherstellen.
ms.assetid: ea6e6312-8c7f-44db-ac7f-165dc45dec23
title: Cdynamicoutputpin. unblockoutputpin-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.UnblockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60bcde3ccad01e19f3802e2cd19f0f6b873380ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370284"
---
# <a name="cdynamicoutputpinunblockoutputpin-method"></a><span data-ttu-id="a4b24-104">Cdynamicoutputpin. unblockoutputpin-Methode</span><span class="sxs-lookup"><span data-stu-id="a4b24-104">CDynamicOutputPin.UnblockOutputPin method</span></span>

<span data-ttu-id="a4b24-105">Die- `UnblockOutputPin` Methode hebt die Blockierung der PIN auf.</span><span class="sxs-lookup"><span data-stu-id="a4b24-105">The `UnblockOutputPin` method unblocks the pin.</span></span> <span data-ttu-id="a4b24-106">Wenn die Blockierung der PIN aufgehoben wird, kann Sie Beispiele liefern, das Ausgabeformat ändern und die Verbindung wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="a4b24-106">When the pin is unblocked, it can deliver samples, change its output format, and reconnect itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b24-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4b24-107">Syntax</span></span>


```C++
HRESULT UnblockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="a4b24-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4b24-108">Parameters</span></span>

<span data-ttu-id="a4b24-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="a4b24-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4b24-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4b24-110">Return value</span></span>

<span data-ttu-id="a4b24-111">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="a4b24-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="a4b24-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a4b24-112">Return code</span></span>                                                                             | <span data-ttu-id="a4b24-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4b24-113">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="a4b24-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="a4b24-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="a4b24-115">Die Blockierung der PIN war bereits aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="a4b24-115">Pin was already unblocked.</span></span><br/> |
| <dl> <span data-ttu-id="a4b24-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a4b24-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="a4b24-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="a4b24-117">Success.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="a4b24-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4b24-118">Requirements</span></span>



| <span data-ttu-id="a4b24-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4b24-119">Requirement</span></span> | <span data-ttu-id="a4b24-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a4b24-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b24-121">Header</span><span class="sxs-lookup"><span data-stu-id="a4b24-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a4b24-122"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a4b24-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a4b24-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a4b24-123">Library</span></span><br/> | <dl> <span data-ttu-id="a4b24-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="a4b24-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4b24-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4b24-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4b24-126">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="a4b24-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




