---
description: Die isusingdefaultsource-Methode bestimmt, ob der Renderer das standardmäßige Quell Code Fenster verwendet.
ms.assetid: f68d47e7-6602-4321-8e9e-373d354077a1
title: Cbasecontrolvideo. isusingdefaultsource-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94768cb098183654b7a0fa9464221989b407d880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370932"
---
# <a name="cbasecontrolvideoisusingdefaultsource-method"></a><span data-ttu-id="111f3-103">Cbasecontrolvideo. isusingdefaultsource-Methode</span><span class="sxs-lookup"><span data-stu-id="111f3-103">CBaseControlVideo.IsUsingDefaultSource method</span></span>

<span data-ttu-id="111f3-104">Die- `IsUsingDefaultSource` Methode bestimmt, ob der Renderer das standardmäßige Quell Code Fenster verwendet.</span><span class="sxs-lookup"><span data-stu-id="111f3-104">The `IsUsingDefaultSource` method determines if the renderer is using the default source window.</span></span>

## <a name="syntax"></a><span data-ttu-id="111f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="111f3-105">Syntax</span></span>


```C++
virtual HRESULT IsUsingDefaultSource() = 0;
```



## <a name="parameters"></a><span data-ttu-id="111f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="111f3-106">Parameters</span></span>

<span data-ttu-id="111f3-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="111f3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="111f3-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="111f3-108">Return value</span></span>

<span data-ttu-id="111f3-109">Gibt s \_ OK zurück, wenn der Renderer die Standard Quelle verwendet; andernfalls wird s \_ false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="111f3-109">Returns S\_OK if the renderer is using the default source; otherwise, returns S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="111f3-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="111f3-110">Requirements</span></span>



| <span data-ttu-id="111f3-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="111f3-111">Requirement</span></span> | <span data-ttu-id="111f3-112">Wert</span><span class="sxs-lookup"><span data-stu-id="111f3-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="111f3-113">Header</span><span class="sxs-lookup"><span data-stu-id="111f3-113">Header</span></span><br/>  | <dl> <span data-ttu-id="111f3-114"><dt>Ctlutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="111f3-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="111f3-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="111f3-115">Library</span></span><br/> | <dl> <span data-ttu-id="111f3-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="111f3-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="111f3-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="111f3-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="111f3-118">**Cbasecontrolvideo-Klasse**</span><span class="sxs-lookup"><span data-stu-id="111f3-118">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




