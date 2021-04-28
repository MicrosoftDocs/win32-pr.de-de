---
description: 'CDynamicOutputPin.Disconnect-Methode: Die Disconnect-Methode unterbricht die aktuelle Pinverbindung. Diese Methode implementiert die IPin::D isconnect-Methode.'
ms.assetid: 8d92a504-98ad-4f8f-89a4-f0c80763db44
title: CDynamicOutputPin.Disconnect-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a775146973b353413fa2e74584a6c763b721e7b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099298"
---
# <a name="cdynamicoutputpindisconnect-method"></a><span data-ttu-id="05d81-104">CDynamicOutputPin.Disconnect-Methode</span><span class="sxs-lookup"><span data-stu-id="05d81-104">CDynamicOutputPin.Disconnect method</span></span>

<span data-ttu-id="05d81-105">Die `Disconnect` -Methode unterbricht die aktuelle Pinverbindung.</span><span class="sxs-lookup"><span data-stu-id="05d81-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="05d81-106">Diese Methode implementiert die [**IPin::D isconnect-Methode.**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect)</span><span class="sxs-lookup"><span data-stu-id="05d81-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="05d81-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="05d81-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="05d81-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="05d81-108">Parameters</span></span>

<span data-ttu-id="05d81-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="05d81-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="05d81-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05d81-110">Return value</span></span>

<span data-ttu-id="05d81-111">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="05d81-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="05d81-112">Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.</span><span class="sxs-lookup"><span data-stu-id="05d81-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="05d81-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="05d81-113">Return code</span></span>                                                                             | <span data-ttu-id="05d81-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05d81-114">Description</span></span>                           |
|-----------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="05d81-115"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="05d81-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="05d81-116">Die Stecknadel wurde nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="05d81-116">The pin was not connected.</span></span><br/> |
| <dl> <span data-ttu-id="05d81-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="05d81-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="05d81-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="05d81-118">Success.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="05d81-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05d81-119">Remarks</span></span>

<span data-ttu-id="05d81-120">Diese Methode überschreibt die [**CBasePin::D isconnect-Methode,**](cbasepin-disconnect.md) um das Trennen der Verbindung zu aktivieren, während der Filter aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="05d81-120">This method overrides the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method to enable disconnecting while the filter is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="05d81-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05d81-121">Requirements</span></span>



| <span data-ttu-id="05d81-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05d81-122">Requirement</span></span> | <span data-ttu-id="05d81-123">Wert</span><span class="sxs-lookup"><span data-stu-id="05d81-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05d81-124">Header</span><span class="sxs-lookup"><span data-stu-id="05d81-124">Header</span></span><br/>  | <dl> <span data-ttu-id="05d81-125"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="05d81-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="05d81-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="05d81-126">Library</span></span><br/> | <dl> <span data-ttu-id="05d81-127"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="05d81-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05d81-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="05d81-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05d81-129">**CDynamicOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="05d81-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




