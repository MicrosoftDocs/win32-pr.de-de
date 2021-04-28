---
description: CBaseStreamControl.CBaseStreamControl-Konstruktor – Konstruktormethode.
ms.assetid: c0eff80f-04d3-4919-bb27-1b76c1bd1cce
title: CBaseStreamControl.CBaseStreamControl-Konstruktor (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4c6521bec65e0182b8eb48eb5d3efe9ea609c6a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095848"
---
# <a name="cbasestreamcontrolcbasestreamcontrol-constructor"></a><span data-ttu-id="d871e-103">CBaseStreamControl.CBaseStreamControl-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="d871e-103">CBaseStreamControl.CBaseStreamControl constructor</span></span>

<span data-ttu-id="d871e-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="d871e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d871e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d871e-105">Syntax</span></span>


```C++
CBaseStreamControl(
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="d871e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d871e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d871e-107">*Phr*</span><span class="sxs-lookup"><span data-stu-id="d871e-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d871e-108">Zeiger auf einen **HRESULT-Wert.**</span><span class="sxs-lookup"><span data-stu-id="d871e-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="d871e-109">Wenn der Konstruktor fehlschlägt, empfängt dieser Parameter einen Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d871e-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="d871e-110">In diesem Fall befindet sich das Objekt nicht in einem gültigen Zustand.</span><span class="sxs-lookup"><span data-stu-id="d871e-110">If this occurs, the object is not in a valid state.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d871e-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d871e-111">Requirements</span></span>



| <span data-ttu-id="d871e-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d871e-112">Requirement</span></span> | <span data-ttu-id="d871e-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d871e-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d871e-114">Header</span><span class="sxs-lookup"><span data-stu-id="d871e-114">Header</span></span><br/>  | <dl> <span data-ttu-id="d871e-115"><dt>Strmctl.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d871e-115"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d871e-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d871e-116">Library</span></span><br/> | <dl> <span data-ttu-id="d871e-117"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d871e-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d871e-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d871e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d871e-119">**CBaseStreamControl-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d871e-119">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




