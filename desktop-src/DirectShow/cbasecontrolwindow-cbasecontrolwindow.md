---
description: Konstruktormethode.
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: Cbasecontrolwindow. cbasecontrolwindow-Konstruktor (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.CBaseControlWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9eb3e50daef8ec4ad11bf96a8f0b605f4c8fe679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364858"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a><span data-ttu-id="e2f36-103">Cbasecontrolwindow. cbasecontrolwindow-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="e2f36-103">CBaseControlWindow.CBaseControlWindow constructor</span></span>

<span data-ttu-id="e2f36-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="e2f36-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f36-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2f36-105">Syntax</span></span>


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a><span data-ttu-id="e2f36-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2f36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2f36-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="e2f36-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="e2f36-108">Zeiger auf das besitzende Medienfilter Objekt.</span><span class="sxs-lookup"><span data-stu-id="e2f36-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="e2f36-109">*pinterfakelock*</span><span class="sxs-lookup"><span data-stu-id="e2f36-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="e2f36-110">Zeiger auf den kritischen Abschnitt, der zum Sperren verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2f36-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="e2f36-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="e2f36-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="e2f36-112">Zeiger auf die Objektbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="e2f36-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="e2f36-113">*Kro*</span><span class="sxs-lookup"><span data-stu-id="e2f36-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="e2f36-114">Ein Zeiger auf die steuernde **IUnknown** -Schnittstelle, wenn das Objekt Teil eines Aggregats ist. Andernfalls muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="e2f36-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e2f36-115">*PHR*</span><span class="sxs-lookup"><span data-stu-id="e2f36-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="e2f36-116">Ein Zeiger auf eine Variable, die einen HRESULT-Wert empfängt, der angibt, ob die Konstruktormethode erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="e2f36-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2f36-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2f36-117">Requirements</span></span>



| <span data-ttu-id="e2f36-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2f36-118">Requirement</span></span> | <span data-ttu-id="e2f36-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e2f36-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f36-120">Header</span><span class="sxs-lookup"><span data-stu-id="e2f36-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e2f36-121"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2f36-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e2f36-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e2f36-122">Library</span></span><br/> | <dl> <span data-ttu-id="e2f36-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e2f36-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2f36-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2f36-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f36-125">**Cbasecontrolwindow-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e2f36-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




