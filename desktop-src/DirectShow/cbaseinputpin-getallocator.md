---
description: 'CBaseInputPin.GetAllocator-Methode: Die GetAllocator-Methode ruft die von dieser Stecknadel vorgeschlagene Speicherzuweisung ab. Diese Methode implementiert die IMemInputPin::GetAllocator-Methode.'
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: CBaseInputPin.GetAllocator-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72aaf6bb4c1ff8bf108086a8a42a618267c4bc06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099709"
---
# <a name="cbaseinputpingetallocator-method"></a><span data-ttu-id="95708-104">CBaseInputPin.GetAllocator-Methode</span><span class="sxs-lookup"><span data-stu-id="95708-104">CBaseInputPin.GetAllocator method</span></span>

<span data-ttu-id="95708-105">Die `GetAllocator` -Methode ruft die von dieser Stecknadel vorgeschlagene Speicherbelegung ab.</span><span class="sxs-lookup"><span data-stu-id="95708-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="95708-106">Diese Methode implementiert die [**IMemInputPin::GetAllocator-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator)</span><span class="sxs-lookup"><span data-stu-id="95708-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="95708-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="95708-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="95708-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="95708-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95708-109">*ppAllocator*</span><span class="sxs-lookup"><span data-stu-id="95708-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="95708-110">Adresse einer Variablen, die einen Zeiger auf die [**IMemAllocator-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) der Zuweisung empfängt.</span><span class="sxs-lookup"><span data-stu-id="95708-110">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95708-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95708-111">Return value</span></span>

<span data-ttu-id="95708-112">Gibt bei Erfolg S \_ OK oder einen Fehlercode aus der **CoCreateInstance-Funktion** zurück.</span><span class="sxs-lookup"><span data-stu-id="95708-112">Returns S\_OK if successful, or an error code from the **CoCreateInstance** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="95708-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95708-113">Remarks</span></span>

<span data-ttu-id="95708-114">Diese Methode erstellt ein [**CMemAllocator-Objekt.**](cmemallocator.md)</span><span class="sxs-lookup"><span data-stu-id="95708-114">This method creates a [**CMemAllocator**](cmemallocator.md) object.</span></span> <span data-ttu-id="95708-115">Überschreiben Sie diese Methode, wenn Ihr Filter eine Zuweisung aus einem Downstreampin oder eine benutzerdefinierte Zuweisung verwendet.</span><span class="sxs-lookup"><span data-stu-id="95708-115">Override this method if your filter uses an allocator from a downstream pin, or a custom allocator.</span></span>

<span data-ttu-id="95708-116">Wenn die Methode erfolgreich ist, verfügt die **IMemAllocator-Schnittstelle** über einen ausstehenden Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="95708-116">If the method succeeds, the **IMemAllocator** interface has an outstanding reference count.</span></span> <span data-ttu-id="95708-117">Stellen Sie sicher, dass Sie es freigeben, wenn Sie fertig sind.</span><span class="sxs-lookup"><span data-stu-id="95708-117">Be sure to release it when you are done.</span></span>

## <a name="requirements"></a><span data-ttu-id="95708-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95708-118">Requirements</span></span>



| <span data-ttu-id="95708-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95708-119">Requirement</span></span> | <span data-ttu-id="95708-120">Wert</span><span class="sxs-lookup"><span data-stu-id="95708-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95708-121">Header</span><span class="sxs-lookup"><span data-stu-id="95708-121">Header</span></span><br/>  | <dl> <span data-ttu-id="95708-122"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="95708-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="95708-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95708-123">Library</span></span><br/> | <dl> <span data-ttu-id="95708-124"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="95708-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95708-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="95708-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95708-126">**CBaseInputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="95708-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




