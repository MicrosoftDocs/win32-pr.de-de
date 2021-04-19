---
title: Iwmdrmlicense reantenumeration-Methode (wmdrmsdk. h)
description: Die resetenumeration-Methode setzt die Lizenz Liste auf ihren ursprünglichen Zustand zurück. Die aktive Lizenz wird zur ersten Lizenz in der Liste.
ms.assetid: cb5a31a8-ee25-44d6-81ca-746c379cb99e
keywords:
- Resegtenumeration-Methode Windows Media-Format
- Resegtenumeration-Methode Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, rerentenumeration-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.ResetEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6510c05b4c974051d9902ed2d30d9cdf99956af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367645"
---
# <a name="iwmdrmlicenseresetenumeration-method"></a><span data-ttu-id="9a568-107">Iwmdrmlicense:: resstenumeration-Methode</span><span class="sxs-lookup"><span data-stu-id="9a568-107">IWMDRMLicense::ResetEnumeration method</span></span>

<span data-ttu-id="9a568-108">Die **resetenumeration** -Methode setzt die Lizenz Liste auf ihren ursprünglichen Zustand zurück.</span><span class="sxs-lookup"><span data-stu-id="9a568-108">The **ResetEnumeration** method resets the license list to its original state.</span></span> <span data-ttu-id="9a568-109">Die aktive Lizenz wird zur ersten Lizenz in der Liste.</span><span class="sxs-lookup"><span data-stu-id="9a568-109">The active license becomes the first license in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a568-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a568-110">Syntax</span></span>


```C++
HRESULT ResetEnumeration();
```



## <a name="parameters"></a><span data-ttu-id="9a568-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a568-111">Parameters</span></span>

<span data-ttu-id="9a568-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9a568-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a568-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a568-113">Return value</span></span>

<span data-ttu-id="9a568-114">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="9a568-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9a568-115">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9a568-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9a568-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9a568-116">Return code</span></span>                                                                                                | <span data-ttu-id="9a568-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a568-117">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="9a568-118"><dt>**NS \_ E \_ DRM- \_ RIV \_ zu \_ klein**</dt></span><span class="sxs-lookup"><span data-stu-id="9a568-118"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="9a568-119">Es wird eine aktualisierte Inhalts Sperr Liste benötigt.</span><span class="sxs-lookup"><span data-stu-id="9a568-119">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="9a568-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9a568-120"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="9a568-121">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a568-121">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="9a568-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a568-122">Remarks</span></span>

<span data-ttu-id="9a568-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="9a568-123">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a568-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a568-124">Requirements</span></span>



| <span data-ttu-id="9a568-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a568-125">Requirement</span></span> | <span data-ttu-id="9a568-126">Wert</span><span class="sxs-lookup"><span data-stu-id="9a568-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a568-127">Header</span><span class="sxs-lookup"><span data-stu-id="9a568-127">Header</span></span><br/>  | <dl> <span data-ttu-id="9a568-128"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a568-128"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a568-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9a568-129">Library</span></span><br/> | <dl> <span data-ttu-id="9a568-130"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a568-130"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a568-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a568-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a568-132">**Iwmdrmlicense-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9a568-132">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





