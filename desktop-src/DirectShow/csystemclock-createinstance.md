---
description: Die Methode "kreateinstance" erstellt eine neue Instanz dieses Objekts.
ms.assetid: 5c62f781-0f22-4d8f-8517-272405dd07c5
title: Csystemclock. kreateinstance-Methode (sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.CreateInstance
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 264997448aea028c5725d207ce4b301d369a092c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365428"
---
# <a name="csystemclockcreateinstance-method"></a><span data-ttu-id="123fc-103">Csystemclock. kreatzustance-Methode</span><span class="sxs-lookup"><span data-stu-id="123fc-103">CSystemClock.CreateInstance method</span></span>

<span data-ttu-id="123fc-104">Die- `CreateInstance` Methode erstellt eine neue Instanz dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="123fc-104">The `CreateInstance` method creates a new instance of this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="123fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="123fc-105">Syntax</span></span>


```C++
static CUnknown* WINAPI CreateInstance(
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="123fc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="123fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="123fc-107">*Kro*</span><span class="sxs-lookup"><span data-stu-id="123fc-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="123fc-108">Zeiger auf die Aggregations- **IUnknown** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="123fc-108">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="123fc-109">*PHR*</span><span class="sxs-lookup"><span data-stu-id="123fc-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="123fc-110">Ein Zeiger auf eine Variable, die einen **HRESULT** -Wert empfängt, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="123fc-110">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="123fc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="123fc-111">Return value</span></span>

<span data-ttu-id="123fc-112">Gibt einen Zeiger auf eine neue Instanz dieses-Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="123fc-112">Returns a pointer to a new instance of this object.</span></span>

## <a name="remarks"></a><span data-ttu-id="123fc-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="123fc-113">Remarks</span></span>

<span data-ttu-id="123fc-114">Die Klassenfactory ruft diese Methode auf, um das Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="123fc-114">The class factory calls this method to create the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="123fc-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="123fc-115">Requirements</span></span>



| <span data-ttu-id="123fc-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="123fc-116">Requirement</span></span> | <span data-ttu-id="123fc-117">Wert</span><span class="sxs-lookup"><span data-stu-id="123fc-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="123fc-118">Header</span><span class="sxs-lookup"><span data-stu-id="123fc-118">Header</span></span><br/>  | <dl> <span data-ttu-id="123fc-119"><dt>Sysclock. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="123fc-119"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="123fc-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="123fc-120">Library</span></span><br/> | <dl> <span data-ttu-id="123fc-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="123fc-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




