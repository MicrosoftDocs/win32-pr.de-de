---
description: 'Die beginflush-Methode startet einen Löschvorgang. Diese Methode implementiert die IPin:: beginflush-Methode.'
ms.assetid: 7c76ca06-dc3c-4f9a-9761-32aea7db4c7e
title: Ctransforminputpin. beginflush-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4d028634364ca59ae293d9ebb60a464974ccd74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356494"
---
# <a name="ctransforminputpinbeginflush-method"></a><span data-ttu-id="d6913-104">Ctransforminputpin. beginflush-Methode</span><span class="sxs-lookup"><span data-stu-id="d6913-104">CTransformInputPin.BeginFlush method</span></span>

<span data-ttu-id="d6913-105">Die- `BeginFlush` Methode startet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="d6913-105">The `BeginFlush` method begins a flush operation.</span></span> <span data-ttu-id="d6913-106">Diese Methode implementiert die [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) -Methode.</span><span class="sxs-lookup"><span data-stu-id="d6913-106">This method implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6913-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d6913-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="d6913-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d6913-108">Parameters</span></span>

<span data-ttu-id="d6913-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d6913-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d6913-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d6913-110">Return value</span></span>

<span data-ttu-id="d6913-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d6913-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d6913-112">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d6913-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="d6913-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d6913-113">Return code</span></span>                                                                                           | <span data-ttu-id="d6913-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d6913-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="d6913-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d6913-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="d6913-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="d6913-116">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="d6913-117"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="d6913-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d6913-118">Die Ausgabepin ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="d6913-118">Output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d6913-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6913-119">Remarks</span></span>

<span data-ttu-id="d6913-120">Diese Methode ruft die [**cbaseiniputpin:: beginflush**](cbaseinputpin-beginflush.md) -Methode der PIN auf.</span><span class="sxs-lookup"><span data-stu-id="d6913-120">This method calls the pin's [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md) method.</span></span> <span data-ttu-id="d6913-121">Anschließend wird die [**ctransformfilter:: beginflush**](ctransformfilter-beginflush.md) -Methode des Filters aufgerufen, um den Aufruf Downstream zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="d6913-121">Then it calls the filter's [**CTransformFilter::BeginFlush**](ctransformfilter-beginflush.md) method to deliver the call downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6913-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d6913-122">Requirements</span></span>



| <span data-ttu-id="d6913-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d6913-123">Requirement</span></span> | <span data-ttu-id="d6913-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d6913-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6913-125">Header</span><span class="sxs-lookup"><span data-stu-id="d6913-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d6913-126"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6913-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d6913-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d6913-127">Library</span></span><br/> | <dl> <span data-ttu-id="d6913-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d6913-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




