---
description: 'CSystemClock.CSystemClock-Konstruktor : Konstruktormethode.'
ms.assetid: facc2c9d-034a-4fed-b6fe-77a40e36c305
title: CSystemClock.CSystemClock-Konstruktor (Sysclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CSystemClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 11ba7449b086f84dc2caff19da922c03f9c7103b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095198"
---
# <a name="csystemclockcsystemclock-constructor"></a><span data-ttu-id="0e802-103">CSystemClock.CSystemClock-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="0e802-103">CSystemClock.CSystemClock constructor</span></span>

<span data-ttu-id="0e802-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="0e802-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e802-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e802-105">Syntax</span></span>


```C++
CSystemClock(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="0e802-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e802-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e802-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="0e802-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0e802-108">Eine Zeichenfolge, die den Debugnamen des Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="0e802-108">String containing the debug name of the object.</span></span> <span data-ttu-id="0e802-109">Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="0e802-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="0e802-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="0e802-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="0e802-111">Zeiger auf den Besitzer dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="0e802-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="0e802-112">Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle des aggregierenden** Objekts.</span><span class="sxs-lookup"><span data-stu-id="0e802-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="0e802-113">Legen Sie andernfalls diesen Parameter auf **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="0e802-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0e802-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="0e802-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="0e802-115">Zeiger auf den **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="0e802-115">Pointer to the **HRESULT** value.</span></span> <span data-ttu-id="0e802-116">Wenn ein Fehler auftritt, gibt die Methode einen Fehlercode in diesem Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="0e802-116">If an error occurs, the method returns an error code in this parameter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e802-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e802-117">Requirements</span></span>



| <span data-ttu-id="0e802-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e802-118">Requirement</span></span> | <span data-ttu-id="0e802-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0e802-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e802-120">Header</span><span class="sxs-lookup"><span data-stu-id="0e802-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0e802-121"><dt>Sysclock.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-121"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0e802-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0e802-122">Library</span></span><br/> | <dl> <span data-ttu-id="0e802-123"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0e802-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




