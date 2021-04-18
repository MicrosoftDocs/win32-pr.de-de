---
description: Die checkstreaming-Methode bestimmt, ob die PIN Beispiele annehmen kann.
ms.assetid: fa063966-4c72-466e-933c-def6a6818621
title: Ctransforminputpin. checkstreaming-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e5c49a00054547193e3f492f0731f77af8331a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364742"
---
# <a name="ctransforminputpincheckstreaming-method"></a><span data-ttu-id="6d33e-103">Ctransforminputpin. checkstreaming-Methode</span><span class="sxs-lookup"><span data-stu-id="6d33e-103">CTransformInputPin.CheckStreaming method</span></span>

<span data-ttu-id="6d33e-104">Die- `CheckStreaming` Methode bestimmt, ob die PIN Beispiele annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="6d33e-104">The `CheckStreaming` method determines whether the pin can accept samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d33e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d33e-105">Syntax</span></span>


```C++
HRESULT CheckStreaming();
```



## <a name="parameters"></a><span data-ttu-id="6d33e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d33e-106">Parameters</span></span>

<span data-ttu-id="6d33e-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6d33e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d33e-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6d33e-108">Return value</span></span>

<span data-ttu-id="6d33e-109">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="6d33e-109">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="6d33e-110">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6d33e-110">Return code</span></span>                                                                                           | <span data-ttu-id="6d33e-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d33e-111">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="6d33e-112"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6d33e-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="6d33e-113">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="6d33e-113">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="6d33e-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="6d33e-114"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="6d33e-115">Die PIN wird zurzeit geleert.</span><span class="sxs-lookup"><span data-stu-id="6d33e-115">Pin is currently flushing.</span></span><br/>       |
| <dl> <span data-ttu-id="6d33e-116"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="6d33e-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="6d33e-117">Die Ausgabe-PIN ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="6d33e-117">The output pin is not connected.</span></span><br/> |
| <dl> <span data-ttu-id="6d33e-118"><dt>**VFW \_ E \_ Lauf \_ Zeitfehler**</dt></span><span class="sxs-lookup"><span data-stu-id="6d33e-118"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="6d33e-119">Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="6d33e-119">A run-time error occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="6d33e-120"><dt>**VFW \_ E \_ falscher \_ Zustand**</dt></span><span class="sxs-lookup"><span data-stu-id="6d33e-120"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="6d33e-121">Die PIN wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="6d33e-121">The pin is stopped.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="6d33e-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d33e-122">Remarks</span></span>

<span data-ttu-id="6d33e-123">Diese Methode überschreibt die [**cbaseinputpin:: checkstreaming**](cbaseinputpin-checkstreaming.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="6d33e-123">This method overrides the [**CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d33e-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d33e-124">Requirements</span></span>



| <span data-ttu-id="6d33e-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d33e-125">Requirement</span></span> | <span data-ttu-id="6d33e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6d33e-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d33e-127">Header</span><span class="sxs-lookup"><span data-stu-id="6d33e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6d33e-128"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d33e-128"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6d33e-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6d33e-129">Library</span></span><br/> | <dl> <span data-ttu-id="6d33e-130">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6d33e-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




