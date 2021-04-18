---
description: Verweis Zähler.
ms.assetid: be619a85-ca73-4cee-9df7-20e7be21853b
title: 'Cunknown:: m_cRef Member (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cRef
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94ff5d88ca48feeb46a8b0411a55d6261aefcf6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372207"
---
# <a name="cunknownm_cref-member"></a><span data-ttu-id="e514d-103">Cunknown:: m- \_ kref-Member</span><span class="sxs-lookup"><span data-stu-id="e514d-103">CUnknown::m\_cRef member</span></span>

<span data-ttu-id="e514d-104">Verweis Zähler.</span><span class="sxs-lookup"><span data-stu-id="e514d-104">Reference count.</span></span>

## <a name="syntax"></a><span data-ttu-id="e514d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e514d-105">Syntax</span></span>


```C++
LONG m_cRef;
```



## <a name="remarks"></a><span data-ttu-id="e514d-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e514d-106">Remarks</span></span>

<span data-ttu-id="e514d-107">Verwenden Sie diese Member-Variable, wenn Sie die [**nondelegatingadressf**](cunknown-nondelegatingaddref.md) -oder [**nondelegatingrelease**](cunknown-nondelegatingrelease.md) -Methode außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="e514d-107">Use this member variable if you override the [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) or [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e514d-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e514d-108">Requirements</span></span>



| <span data-ttu-id="e514d-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e514d-109">Requirement</span></span> | <span data-ttu-id="e514d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="e514d-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e514d-111">Header</span><span class="sxs-lookup"><span data-stu-id="e514d-111">Header</span></span><br/>  | <dl> <span data-ttu-id="e514d-112"><dt>ComBase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e514d-112"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e514d-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e514d-113">Library</span></span><br/> | <dl> <span data-ttu-id="e514d-114">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e514d-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




