---
description: Die Connect-Methode schließt eine Verbindung mit der Ausgabepin ab.
ms.assetid: fb20ef5d-e00a-4154-a6da-25bef663c0e7
title: Cpullpin. Connect-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 97e3b0b676e02dee0e3ebd82de9def56edc2ea28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369188"
---
# <a name="cpullpinconnect-method"></a><span data-ttu-id="b789e-103">Cpullpin. Connect-Methode</span><span class="sxs-lookup"><span data-stu-id="b789e-103">CPullPin.Connect method</span></span>

<span data-ttu-id="b789e-104">Die- `Connect` Methode schließt eine Verbindung mit der Ausgabepin ab.</span><span class="sxs-lookup"><span data-stu-id="b789e-104">The `Connect` method completes a connection to the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="b789e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b789e-105">Syntax</span></span>


```C++
HRESULT Connect(
   IUnknown      *pUnk,
   IMemAllocator *pAlloc,
   BOOL          bSync
);
```



## <a name="parameters"></a><span data-ttu-id="b789e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b789e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b789e-107">*Kro*</span><span class="sxs-lookup"><span data-stu-id="b789e-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="b789e-108">Ein Zeiger auf die **IUnknown** -Schnittstelle der Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="b789e-108">Pointer to the **IUnknown** interface of the output pin.</span></span>

</dd> <dt>

<span data-ttu-id="b789e-109">*palloc*</span><span class="sxs-lookup"><span data-stu-id="b789e-109">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="b789e-110">Ein Zeiger auf die [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle der bevorzugten Zuweisung der Eingabe-PIN oder **null**.</span><span class="sxs-lookup"><span data-stu-id="b789e-110">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface of the input pin's preferred allocator, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b789e-111">*bsync*</span><span class="sxs-lookup"><span data-stu-id="b789e-111">*bSync*</span></span> 
</dt> <dd>

<span data-ttu-id="b789e-112">Boolescher Wert, der angibt, ob synchrone Lesevorgänge verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b789e-112">Boolean value that specifies whether to use synchronous reads.</span></span> <span data-ttu-id="b789e-113">Wenn der Wert **true** ist, führt die PIN synchrone Lesevorgänge für die Ausgabe-PIN aus.</span><span class="sxs-lookup"><span data-stu-id="b789e-113">If **TRUE**, the pin performs synchronous read operations on the output pin.</span></span> <span data-ttu-id="b789e-114">**False** gibt an, dass die PIN asynchrone Lese Anforderungen ausführt.</span><span class="sxs-lookup"><span data-stu-id="b789e-114">If **FALSE**, the pin makes asynchronous read requests.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b789e-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b789e-115">Return value</span></span>

<span data-ttu-id="b789e-116">Gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="b789e-116">Returns an **HRESULT**.</span></span> <span data-ttu-id="b789e-117">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="b789e-117">Possible values include the following.</span></span>



| <span data-ttu-id="b789e-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b789e-118">Return code</span></span>                                                                                               | <span data-ttu-id="b789e-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b789e-119">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b789e-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b789e-120"><dt>**S\_OK**</dt></span></span> </dl>                      | <span data-ttu-id="b789e-121">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="b789e-121">Success.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="b789e-122"><dt>**VFW \_ E \_ bereits \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="b789e-122"><dt>**VFW\_E\_ALREADY\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="b789e-123">Die eingabepin ist bereits verbunden.</span><span class="sxs-lookup"><span data-stu-id="b789e-123">The input pin is already connected.</span></span><br/>                                  |
| <dl> <span data-ttu-id="b789e-124"><dt>**E \_ nointerface**</dt></span><span class="sxs-lookup"><span data-stu-id="b789e-124"><dt>**E\_NOINTERFACE**</dt></span></span> </dl>             | <span data-ttu-id="b789e-125">Der Ausgabepin macht [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader)nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b789e-125">The output pin does not expose [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b789e-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b789e-126">Remarks</span></span>

<span data-ttu-id="b789e-127">Ruft diese Methode während des Verbindungs Vorgangs der Eingabe-PIN auf.</span><span class="sxs-lookup"><span data-stu-id="b789e-127">Call this method during the input pin's connection process.</span></span> <span data-ttu-id="b789e-128">Wenn die Methode fehlschlägt, sollte die PIN die Verbindung nicht herstellen.</span><span class="sxs-lookup"><span data-stu-id="b789e-128">If the method fails, the pin should fail the connection.</span></span>

<span data-ttu-id="b789e-129">Diese Methode fragt die Ausgabe-PIN für die **iasynkreader** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="b789e-129">This method queries the output pin for the **IAsyncReader** interface.</span></span> <span data-ttu-id="b789e-130">Bei erfolgreicher Ausführung wird [**cpullpin::D-ecidezuordcator**](cpullpin-decideallocator.md) aufgerufen, um die Zuweisung für die Verbindung auszuhandeln.</span><span class="sxs-lookup"><span data-stu-id="b789e-130">If successful, it calls [**CPullPin::DecideAllocator**](cpullpin-decideallocator.md) to negotiate the allocator for the connection.</span></span> <span data-ttu-id="b789e-131">Wenn Ihre Eingabe-PIN über einen bevorzugten Zuweiser verfügt, geben Sie Sie im *palloc* -Parameter an. die **decidezuzuordcator** -Methode übergibt diesen Zeiger an die [**iasynkreader:: Request-**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) Methode der Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="b789e-131">If your input pin has a preferred allocator, specify it in the *pAlloc* parameter; the **DecideAllocator** method passes this pointer to the output pin's [**IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) method.</span></span> <span data-ttu-id="b789e-132">Andernfalls legen Sie *palloc* auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="b789e-132">Otherwise, set *pAlloc* to **NULL**.</span></span>

<span data-ttu-id="b789e-133">Wenn der Wert von *bsync* **true** ist, führt das **cpullpin** -Objekt synchrone Lese Anforderungen durch Aufrufen des [**iasyncreader:: syncreadausgerichteten**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned)-Objekts der Ausgabe-PIN aus.</span><span class="sxs-lookup"><span data-stu-id="b789e-133">If the value of *bSync* is **TRUE**, the **CPullPin** object makes synchronous read requests, by calling the output pin's [**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span></span> <span data-ttu-id="b789e-134">Andernfalls wird die [**iasynkreader:: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) -Methode aufgerufen, um überlappende Lese Anforderungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b789e-134">Otherwise, it calls the [**IAsyncReader::Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request) method to make overlapping read requests.</span></span>

## <a name="requirements"></a><span data-ttu-id="b789e-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b789e-135">Requirements</span></span>



| <span data-ttu-id="b789e-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b789e-136">Requirement</span></span> | <span data-ttu-id="b789e-137">Wert</span><span class="sxs-lookup"><span data-stu-id="b789e-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b789e-138">Header</span><span class="sxs-lookup"><span data-stu-id="b789e-138">Header</span></span><br/>  | <dl> <span data-ttu-id="b789e-139"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="b789e-139"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="b789e-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b789e-140">Library</span></span><br/> | <dl> <span data-ttu-id="b789e-141">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b789e-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b789e-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b789e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b789e-143">**Cpullpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b789e-143">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




