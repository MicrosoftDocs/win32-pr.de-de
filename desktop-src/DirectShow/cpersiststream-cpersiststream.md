---
description: Konstruktormethode.
ms.assetid: 48143a61-5ba7-4bf9-bffa-244f2769144d
title: Cpersiststream. cpersiststream-Konstruktor (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.CPersistStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cdb736a191f64099b8c0310a5b3ac3dad3cbe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354215"
---
# <a name="cpersiststreamcpersiststream-constructor"></a><span data-ttu-id="aa775-103">Cpersiststream. cpersiststream-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="aa775-103">CPersistStream.CPersistStream constructor</span></span>

<span data-ttu-id="aa775-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="aa775-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa775-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa775-105">Syntax</span></span>


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a><span data-ttu-id="aa775-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa775-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa775-107">*Kro*</span><span class="sxs-lookup"><span data-stu-id="aa775-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="aa775-108">Ein Zeiger auf die **IUnknown** -Schnittstelle des Delegatenobjekts.</span><span class="sxs-lookup"><span data-stu-id="aa775-108">Pointer to the **IUnknown** interface of the delegating object.</span></span>

</dd> <dt>

<span data-ttu-id="aa775-109">*PHR*</span><span class="sxs-lookup"><span data-stu-id="aa775-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="aa775-110">Zeiger auf den allgemeinen com-Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="aa775-110">Pointer to the general COM return value.</span></span> <span data-ttu-id="aa775-111">Dieser Wert wird nur geändert, wenn diese Funktion fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="aa775-111">This value is changed only if this function fails.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa775-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa775-112">Requirements</span></span>



| <span data-ttu-id="aa775-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa775-113">Requirement</span></span> | <span data-ttu-id="aa775-114">Wert</span><span class="sxs-lookup"><span data-stu-id="aa775-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa775-115">Header</span><span class="sxs-lookup"><span data-stu-id="aa775-115">Header</span></span><br/>  | <dl> <span data-ttu-id="aa775-116"><dt>PStream. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa775-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aa775-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aa775-117">Library</span></span><br/> | <dl> <span data-ttu-id="aa775-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="aa775-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa775-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa775-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa775-120">**Cpersiststream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="aa775-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




