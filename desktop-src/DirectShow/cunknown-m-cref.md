---
description: CUnknown::m_cRef Member – Verweisanzahl.
ms.assetid: be619a85-ca73-4cee-9df7-20e7be21853b
title: CUnknown::m_cRef Member (Combase.h)
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
ms.openlocfilehash: a3f6be7d09149f651bce8d1042b7f3e3a5dc9307
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084578"
---
# <a name="cunknownm_cref-member"></a><span data-ttu-id="73715-103">CUnknown::m \_ cRef-Member</span><span class="sxs-lookup"><span data-stu-id="73715-103">CUnknown::m\_cRef member</span></span>

<span data-ttu-id="73715-104">Verweisanzahl.</span><span class="sxs-lookup"><span data-stu-id="73715-104">Reference count.</span></span>

## <a name="syntax"></a><span data-ttu-id="73715-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="73715-105">Syntax</span></span>


```C++
LONG m_cRef;
```



## <a name="remarks"></a><span data-ttu-id="73715-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73715-106">Remarks</span></span>

<span data-ttu-id="73715-107">Verwenden Sie diese Membervariable, wenn Sie [**die NonDelegatingAddRef-**](cunknown-nondelegatingaddref.md) oder [**NonDelegatingRelease-Methode**](cunknown-nondelegatingrelease.md) überschreiben.</span><span class="sxs-lookup"><span data-stu-id="73715-107">Use this member variable if you override the [**NonDelegatingAddRef**](cunknown-nondelegatingaddref.md) or [**NonDelegatingRelease**](cunknown-nondelegatingrelease.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="73715-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73715-108">Requirements</span></span>



| <span data-ttu-id="73715-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73715-109">Requirement</span></span> | <span data-ttu-id="73715-110">Wert</span><span class="sxs-lookup"><span data-stu-id="73715-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73715-111">Header</span><span class="sxs-lookup"><span data-stu-id="73715-111">Header</span></span><br/>  | <dl> <span data-ttu-id="73715-112"><dt>Combase.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="73715-112"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="73715-113">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="73715-113">Library</span></span><br/> | <dl> <span data-ttu-id="73715-114"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="73715-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




