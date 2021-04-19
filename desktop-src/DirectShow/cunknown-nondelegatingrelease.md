---
description: 'Dekremente den Verweis Zähler für das Objekt. Diese Methode implementiert die inondelegatingunknown:: nondelegatingrelease-Methode.'
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: Cunknown. nondelegatingrelease-Methode (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingRelease
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec709d4b636eea6a145f9a24a868ad5c495e4477
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372667"
---
# <a name="cunknownnondelegatingrelease-method"></a><span data-ttu-id="06df5-104">Cunknown. nondelegatingrelease-Methode</span><span class="sxs-lookup"><span data-stu-id="06df5-104">CUnknown.NonDelegatingRelease method</span></span>

<span data-ttu-id="06df5-105">Dekremente den Verweis Zähler für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="06df5-105">Decrements the reference count on the object.</span></span> <span data-ttu-id="06df5-106">Diese Methode implementiert die **inondelegatingunknown:: nondelegatingrelease** -Methode.</span><span class="sxs-lookup"><span data-stu-id="06df5-106">This method implements the **INonDelegatingUnknown::NonDelegatingRelease** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="06df5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="06df5-107">Syntax</span></span>


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a><span data-ttu-id="06df5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="06df5-108">Parameters</span></span>

<span data-ttu-id="06df5-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="06df5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="06df5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06df5-110">Return value</span></span>

<span data-ttu-id="06df5-111">Gibt den Verweis Zähler zurück.</span><span class="sxs-lookup"><span data-stu-id="06df5-111">Returns the reference count.</span></span>

## <a name="remarks"></a><span data-ttu-id="06df5-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06df5-112">Remarks</span></span>

<span data-ttu-id="06df5-113">Wenn der Verweis Zähler Null erreicht, löscht das Objekt sich selbst.</span><span class="sxs-lookup"><span data-stu-id="06df5-113">When the reference count reaches zero, the object deletes itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="06df5-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06df5-114">Requirements</span></span>



| <span data-ttu-id="06df5-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06df5-115">Requirement</span></span> | <span data-ttu-id="06df5-116">Wert</span><span class="sxs-lookup"><span data-stu-id="06df5-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06df5-117">Header</span><span class="sxs-lookup"><span data-stu-id="06df5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="06df5-118"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06df5-118"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="06df5-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="06df5-119">Library</span></span><br/> | <dl> <span data-ttu-id="06df5-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="06df5-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




