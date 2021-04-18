---
description: Erstellt ein CMSG-Objekt.
ms.assetid: b7ee0643-73e4-450d-bff4-ca5006fdcc14
title: CMSG. CMSG-Konstruktor (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg.CMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b26a9572b51d4a476b70c3dd7ddae8c896a4d648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358119"
---
# <a name="cmsgcmsg-constructor"></a><span data-ttu-id="40717-103">CMSG. CMSG-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="40717-103">CMsg.CMsg constructor</span></span>

<span data-ttu-id="40717-104">Erstellt ein [**CMSG**](cmsg.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="40717-104">Constructs a [**CMsg**](cmsg.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="40717-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="40717-105">Syntax</span></span>


```C++
CMsg(
   UINT     u,
   DWORD    dw,
   LPVOID   lp,
   CAMEvent *pEvent
);
```



## <a name="parameters"></a><span data-ttu-id="40717-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="40717-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40717-107">*n*</span><span class="sxs-lookup"><span data-stu-id="40717-107">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="40717-108">Anforderungs Code, der vom Client der Thread Klasse definiert und von der überschriebenen Arbeits Thread Funktion verstanden wird.</span><span class="sxs-lookup"><span data-stu-id="40717-108">Request code, defined by the client of the thread class and understood by the overridden worker thread function.</span></span>

</dd> <dt>

<span data-ttu-id="40717-109">*dw*</span><span class="sxs-lookup"><span data-stu-id="40717-109">*dw*</span></span> 
</dt> <dd>

<span data-ttu-id="40717-110">Markieren Sie den Parameter für den Anforderungs Code.</span><span class="sxs-lookup"><span data-stu-id="40717-110">Flag parameter to the request code.</span></span>

</dd> <dt>

<span data-ttu-id="40717-111">*LP*</span><span class="sxs-lookup"><span data-stu-id="40717-111">*lp*</span></span> 
</dt> <dd>

<span data-ttu-id="40717-112">Zeiger auf Daten, die vom Arbeits Thread als Parameter oder Rückgabewerte benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="40717-112">Pointer to data required by the worker thread as parameter or return values.</span></span> <span data-ttu-id="40717-113">Diese Daten sollten nicht Stapel basiert sein, da nach Abschluss des Warteschlangen Vorgangs einige Zeit darauf verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="40717-113">This data should not be stack-based, as it will be referenced some time after completing the queuing operation.</span></span>

</dd> <dt>

<span data-ttu-id="40717-114">*Peer Event*</span><span class="sxs-lookup"><span data-stu-id="40717-114">*pEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="40717-115">Zeiger auf das Ereignis Objekt, das ein Arbeits Thread signalisieren kann, um den Abschluss des Vorgangs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="40717-115">Pointer to the event object that a worker thread can signal to indicate the completion of the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40717-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40717-116">Remarks</span></span>

<span data-ttu-id="40717-117">Diese Member-Funktion enthält eine Anforderung für einen [**cmsgthread**](cmsgthread.md) -Arbeits Thread, der ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="40717-117">This member function contains a request for a [**CMsgThread**](cmsgthread.md) worker thread to act on.</span></span> <span data-ttu-id="40717-118">Alle Parameter werden als Parameter an die Arbeits Thread Funktion als Parameter übermittelt, wenn diese Nachricht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="40717-118">All the parameters are passed to the worker thread function as parameters when this message gets processed.</span></span> <span data-ttu-id="40717-119">Die Bedeutungen der Parameter werden von der Client Funktion definiert, die den Arbeits Thread aufruft, und von der abgeleiteten Klasse, die die Ausführungs Funktion des Arbeitsthreads bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="40717-119">The meanings of the parameters are defined by the client function that calls the worker thread and the derived class that supplies the worker thread's execution function.</span></span>

## <a name="requirements"></a><span data-ttu-id="40717-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40717-120">Requirements</span></span>



| <span data-ttu-id="40717-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40717-121">Requirement</span></span> | <span data-ttu-id="40717-122">Wert</span><span class="sxs-lookup"><span data-stu-id="40717-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40717-123">Header</span><span class="sxs-lookup"><span data-stu-id="40717-123">Header</span></span><br/>  | <dl> <span data-ttu-id="40717-124"><dt>Msgthrd. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40717-124"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="40717-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="40717-125">Library</span></span><br/> | <dl> <span data-ttu-id="40717-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="40717-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




