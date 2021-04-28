---
description: 'CBaseOutputPin.CompleteConnect-Methode: Die CompleteConnect-Methode schließt eine Verbindung mit einem Eingabepin ab.'
ms.assetid: 44c28c71-2c69-40ca-9bc4-c10394475a0f
title: CBaseOutputPin.CompleteConnect-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd4bc52db99b88c4d6f16c549fbb558bb6423730
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099538"
---
# <a name="cbaseoutputpincompleteconnect-method"></a><span data-ttu-id="31d5e-103">CBaseOutputPin.CompleteConnect-Methode</span><span class="sxs-lookup"><span data-stu-id="31d5e-103">CBaseOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="31d5e-104">Die `CompleteConnect` -Methode schließt eine Verbindung mit einem Eingabepin ab.</span><span class="sxs-lookup"><span data-stu-id="31d5e-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="31d5e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="31d5e-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="31d5e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="31d5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31d5e-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="31d5e-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="31d5e-108">Zeiger auf den Eingabepin.</span><span class="sxs-lookup"><span data-stu-id="31d5e-108">Pointer to the input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31d5e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31d5e-109">Return value</span></span>

<span data-ttu-id="31d5e-110">Gibt S \_ OK zurück, wenn erfolgreich, oder ein **HRESULT-Wert,** der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="31d5e-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="31d5e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31d5e-111">Remarks</span></span>

<span data-ttu-id="31d5e-112">Diese Methode überschreibt die [**CBasePin::CompleteConnect-Methode.**](cbasepin-completeconnect.md)</span><span class="sxs-lookup"><span data-stu-id="31d5e-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="31d5e-113">Sie ruft die [**DecideAllocator-Methode**](cbaseoutputpin-decideallocator.md) auf, die die Speicherzuweisung auswählt, die für diese Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="31d5e-113">It calls the [**DecideAllocator**](cbaseoutputpin-decideallocator.md) method, which selects the memory allocator to use for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="31d5e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31d5e-114">Requirements</span></span>



| <span data-ttu-id="31d5e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31d5e-115">Requirement</span></span> | <span data-ttu-id="31d5e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="31d5e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31d5e-117">Header</span><span class="sxs-lookup"><span data-stu-id="31d5e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="31d5e-118"><dt>Amfilter.h (streams.h enthalten)</dt></span><span class="sxs-lookup"><span data-stu-id="31d5e-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="31d5e-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="31d5e-119">Library</span></span><br/> | <dl> <span data-ttu-id="31d5e-120"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="31d5e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31d5e-121">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="31d5e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31d5e-122">**CBaseOutputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="31d5e-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




