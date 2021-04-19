---
description: Die decidezuordcator-Methode wählt eine Speicherzuweisung aus.
ms.assetid: cdc15b0e-ea1b-43aa-9267-95fa9db56ed5
title: Cbaseoutputpin. decidezuordcator-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e587562341118b904803302f0fd7249ebf8e507
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366754"
---
# <a name="cbaseoutputpindecideallocator-method"></a><span data-ttu-id="2de11-103">Cbaseoutputpin. decidezuzuordcator-Methode</span><span class="sxs-lookup"><span data-stu-id="2de11-103">CBaseOutputPin.DecideAllocator method</span></span>

<span data-ttu-id="2de11-104">Die- `DecideAllocator` Methode wählt eine Speicherzuweisung aus.</span><span class="sxs-lookup"><span data-stu-id="2de11-104">The `DecideAllocator` method selects a memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="2de11-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2de11-105">Syntax</span></span>


```C++
virtual HRESULT DecideAllocator(
   IMemInputPin  *pPin,
   IMemAllocator **pAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="2de11-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2de11-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2de11-107">*ppin*</span><span class="sxs-lookup"><span data-stu-id="2de11-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="2de11-108">Ein Zeiger auf die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle der Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="2de11-108">Pointer to the input pin's [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2de11-109">*palloc*</span><span class="sxs-lookup"><span data-stu-id="2de11-109">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="2de11-110">Adresse einer Variablen, die einen Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners empfängt.</span><span class="sxs-lookup"><span data-stu-id="2de11-110">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2de11-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2de11-111">Return value</span></span>

<span data-ttu-id="2de11-112">Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="2de11-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="2de11-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2de11-113">Remarks</span></span>

<span data-ttu-id="2de11-114">Diese Methode wird am Ende des PIN-Verbindungsprozesses aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="2de11-114">This method is called at the end of the pin connection process.</span></span> <span data-ttu-id="2de11-115">Sie führt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="2de11-115">It performs the following steps:</span></span>

1.  <span data-ttu-id="2de11-116">Ruft die [**IMemInputPin:: getalloerrequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) -Methode auf, um die Puffer Anforderungen der Eingabe-PIN (sofern vorhanden) abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2de11-116">Calls the [**IMemInputPin::GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) method to retrieve the input pin's buffer requirements, if any.</span></span>
2.  <span data-ttu-id="2de11-117">Ruft die [**IMemInputPin:: getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) -Methode auf, um eine Zuweisung von der eingabepin anzufordern.</span><span class="sxs-lookup"><span data-stu-id="2de11-117">Calls the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method to request an allocator from the input pin.</span></span> <span data-ttu-id="2de11-118">Wenn die eingabepin keine Zuweisung bereitstellt, erstellt die Ausgabe-PIN eine, indem Sie die [**cbaseoutputpin:: initaccesscator**](cbaseoutputpin-initallocator.md) -Klassenmethode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2de11-118">If the input pin does not provide an allocator, the output pin creates one by calling the [**CBaseOutputPin::InitAllocator**](cbaseoutputpin-initallocator.md) class method.</span></span>
3.  <span data-ttu-id="2de11-119">Ruft die [**cbaseoutputpin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) -Klassenmethode auf, mit der die zuordnereigenschaften festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2de11-119">Calls the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) class method, which sets the allocator properties.</span></span> <span data-ttu-id="2de11-120">Dies ist eine reine virtuelle Methode. Diese Klasse muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="2de11-120">This is a pure virtual method; the derived class must implement it.</span></span>
4.  <span data-ttu-id="2de11-121">Ruft die [**IMemInputPin:: notifyzucator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) -Methode auf, die die Eingabe-PIN der verwendeten Zuweisung benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="2de11-121">Calls the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method, which notifies the input pin of the allocator being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2de11-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2de11-122">Requirements</span></span>



| <span data-ttu-id="2de11-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2de11-123">Requirement</span></span> | <span data-ttu-id="2de11-124">Wert</span><span class="sxs-lookup"><span data-stu-id="2de11-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2de11-125">Header</span><span class="sxs-lookup"><span data-stu-id="2de11-125">Header</span></span><br/>  | <dl> <span data-ttu-id="2de11-126"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2de11-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2de11-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2de11-127">Library</span></span><br/> | <dl> <span data-ttu-id="2de11-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2de11-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2de11-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2de11-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2de11-130">**Cbaseoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2de11-130">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




