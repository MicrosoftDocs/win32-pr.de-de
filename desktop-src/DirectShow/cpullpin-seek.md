---
description: Die Seek-Methode legt die Anfangs-und Endposition des Streams fest.
ms.assetid: d84476f5-688c-429d-a51b-7020a6316e35
title: Cpullpin. Seek-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Seek
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f1a82ec549b5ceb888acc194a7abc2cd3eace47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362045"
---
# <a name="cpullpinseek-method"></a><span data-ttu-id="65c9d-103">Cpullpin. Seek-Methode</span><span class="sxs-lookup"><span data-stu-id="65c9d-103">CPullPin.Seek method</span></span>

<span data-ttu-id="65c9d-104">Die `Seek` -Methode legt die Anfangs-und Endposition des Streams fest.</span><span class="sxs-lookup"><span data-stu-id="65c9d-104">The `Seek` method sets the start and stop positions of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="65c9d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="65c9d-105">Syntax</span></span>


```C++
HRESULT Seek(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop
);
```



## <a name="parameters"></a><span data-ttu-id="65c9d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="65c9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65c9d-107">*tSTART*</span><span class="sxs-lookup"><span data-stu-id="65c9d-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="65c9d-108">Gibt die Startposition in Bytes multipliziert mit 10 Millionen an.</span><span class="sxs-lookup"><span data-stu-id="65c9d-108">Specifies the start position, in bytes multiplied by 10,000,000.</span></span>

</dd> <dt>

<span data-ttu-id="65c9d-109">*tstopps*</span><span class="sxs-lookup"><span data-stu-id="65c9d-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="65c9d-110">Gibt die Position des Stopps in Bytes multipliziert mit 10 Millionen an.</span><span class="sxs-lookup"><span data-stu-id="65c9d-110">Specifies the stop position, in bytes multiplied by 10,000,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65c9d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65c9d-111">Return value</span></span>

<span data-ttu-id="65c9d-112">Gibt S \_ OK zurück, wenn die Methode erfolgreich ist, andernfalls einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="65c9d-112">Returns S\_OK if the method succeeds, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="65c9d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65c9d-113">Remarks</span></span>

<span data-ttu-id="65c9d-114">Wenn der Arbeits Thread ausgeführt wird, hält die Methode den Thread an, leert das Filter Diagramm und setzt den Thread fort.</span><span class="sxs-lookup"><span data-stu-id="65c9d-114">If the worker thread is running, the method pauses the thread, flushes the filter graph, and resumes the thread.</span></span> <span data-ttu-id="65c9d-115">Der Thread beginnt mit dem Abrufen von Daten von der neuen Startposition.</span><span class="sxs-lookup"><span data-stu-id="65c9d-115">The thread begins pulling data from the new start position.</span></span> <span data-ttu-id="65c9d-116">Andernfalls werden die neuen Positionswerte immer dann wirksam, wenn der Thread gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="65c9d-116">Otherwise, the new position values become effective whenever the thread is started.</span></span>

<span data-ttu-id="65c9d-117">Positionen sind relativ zum Anfang der ursprünglichen Quelle.</span><span class="sxs-lookup"><span data-stu-id="65c9d-117">Positions are relative to the start of the original source.</span></span> <span data-ttu-id="65c9d-118">Multiplizieren Sie die gewünschten Byte Offsets um die Konstanten Einheiten, die in der Basisklassen Bibliothek als 10 Millionen definiert sind.</span><span class="sxs-lookup"><span data-stu-id="65c9d-118">Multiply the desired byte offsets by the constant UNITS, which is defined in the base class library as 10,000,000.</span></span>

<span data-ttu-id="65c9d-119">Wenn die PIN zum ersten Mal eine Verbindung herstellt, werden die Start-und Startpositionen standardmäßig auf den Anfang und das Ende des Streams eingestellt.</span><span class="sxs-lookup"><span data-stu-id="65c9d-119">When the pin first connects, the stop and start positions default to the beginning and end of the stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="65c9d-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65c9d-120">Requirements</span></span>



| <span data-ttu-id="65c9d-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65c9d-121">Requirement</span></span> | <span data-ttu-id="65c9d-122">Wert</span><span class="sxs-lookup"><span data-stu-id="65c9d-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65c9d-123">Header</span><span class="sxs-lookup"><span data-stu-id="65c9d-123">Header</span></span><br/>  | <dl> <span data-ttu-id="65c9d-124"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="65c9d-124"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="65c9d-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="65c9d-125">Library</span></span><br/> | <dl> <span data-ttu-id="65c9d-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="65c9d-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65c9d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65c9d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65c9d-128">**Cpullpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="65c9d-128">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




