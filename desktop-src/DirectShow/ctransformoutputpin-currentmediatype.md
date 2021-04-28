---
description: 'CTransformOutputPin.CurrentMediaType-Methode: Die CurrentMediaType-Methode ruft den Medientyp für die aktuelle Pinverbindung ab.'
ms.assetid: 1c42664d-160a-4f76-9d7a-40414c5c1704
title: CTransformOutputPin.CurrentMediaType-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cb40310afb1c22d00a5394c0a0667fc8d22eb03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094908"
---
# <a name="ctransformoutputpincurrentmediatype-method"></a><span data-ttu-id="edbcb-103">CTransformOutputPin.CurrentMediaType-Methode</span><span class="sxs-lookup"><span data-stu-id="edbcb-103">CTransformOutputPin.CurrentMediaType method</span></span>

<span data-ttu-id="edbcb-104">Die `CurrentMediaType` -Methode ruft den Medientyp für die aktuelle Pinverbindung ab.</span><span class="sxs-lookup"><span data-stu-id="edbcb-104">The `CurrentMediaType` method retrieves the media type for the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="edbcb-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="edbcb-105">Syntax</span></span>


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a><span data-ttu-id="edbcb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="edbcb-106">Parameters</span></span>

<span data-ttu-id="edbcb-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="edbcb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="edbcb-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="edbcb-108">Return value</span></span>

<span data-ttu-id="edbcb-109">Gibt einen Verweis auf die [**CBasePin::m \_ mt-Membervariable**](cbasepin-m-mt.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="edbcb-109">Returns a reference to the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="edbcb-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="edbcb-110">Requirements</span></span>



| <span data-ttu-id="edbcb-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="edbcb-111">Requirement</span></span> | <span data-ttu-id="edbcb-112">Wert</span><span class="sxs-lookup"><span data-stu-id="edbcb-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edbcb-113">Header</span><span class="sxs-lookup"><span data-stu-id="edbcb-113">Header</span></span><br/>  | <dl> <span data-ttu-id="edbcb-114"><dt>Transfrm.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="edbcb-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="edbcb-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="edbcb-115">Library</span></span><br/> | <dl> <span data-ttu-id="edbcb-116"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="edbcb-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




