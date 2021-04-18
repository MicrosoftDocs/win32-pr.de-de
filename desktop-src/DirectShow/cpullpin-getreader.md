---
description: Die GetReader-Methode gibt einen Zeiger auf die iasynkreader-Schnittstelle der Ausgabe-PIN zurück.
ms.assetid: bb7ed3f2-a5bc-496c-8a52-f9915a75105e
title: Cpullpin. GetReader-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.GetReader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a20bbb689c4ee5e3ac12c510098163d9fbb224e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365574"
---
# <a name="cpullpingetreader-method"></a><span data-ttu-id="2ab83-103">Cpullpin. GetReader-Methode</span><span class="sxs-lookup"><span data-stu-id="2ab83-103">CPullPin.GetReader method</span></span>

<span data-ttu-id="2ab83-104">Die `GetReader` -Methode gibt einen Zeiger auf die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle der Ausgabe-PIN zurück.</span><span class="sxs-lookup"><span data-stu-id="2ab83-104">The `GetReader` method returns a pointer to the output pin's [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ab83-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ab83-105">Syntax</span></span>


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a><span data-ttu-id="2ab83-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ab83-106">Parameters</span></span>

<span data-ttu-id="2ab83-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2ab83-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2ab83-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ab83-108">Return value</span></span>

<span data-ttu-id="2ab83-109">Gibt einen Zeiger auf die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle zurück.</span><span class="sxs-lookup"><span data-stu-id="2ab83-109">Returns a pointer to the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ab83-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ab83-110">Remarks</span></span>

<span data-ttu-id="2ab83-111">Die zurückgegebene Schnittstelle weist einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="2ab83-111">The returned interface has an outstanding reference count.</span></span> <span data-ttu-id="2ab83-112">Der Aufrufer muss die-Schnittstelle freigeben.</span><span class="sxs-lookup"><span data-stu-id="2ab83-112">The caller must release the interface.</span></span>

<span data-ttu-id="2ab83-113">Die-Methode überprüft nicht den Wert des Schnittstellen Zeigers vor dem Aufrufen von " **adressf**". Rufen Sie diese Methode erst auf, wenn Sie die [**cpullpin:: Connect**](cpullpin-connect.md) -Methode erfolgreich aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="2ab83-113">The method does not check the value of the interface pointer before calling **AddRef**, so do not call this until you have successfully called the [**CPullPin::Connect**](cpullpin-connect.md) method.</span></span> <span data-ttu-id="2ab83-114">Andernfalls ist der Schnittstellen Zeiger möglicherweise **null** , und der Aufruf von **adressf** löst eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="2ab83-114">Otherwise, the interface pointer might be **NULL** and calling **AddRef** will throw an exception.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ab83-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ab83-115">Requirements</span></span>



| <span data-ttu-id="2ab83-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ab83-116">Requirement</span></span> | <span data-ttu-id="2ab83-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2ab83-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab83-118">Header</span><span class="sxs-lookup"><span data-stu-id="2ab83-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2ab83-119"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ab83-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="2ab83-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2ab83-120">Library</span></span><br/> | <dl> <span data-ttu-id="2ab83-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2ab83-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ab83-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ab83-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ab83-123">**Cpullpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2ab83-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




