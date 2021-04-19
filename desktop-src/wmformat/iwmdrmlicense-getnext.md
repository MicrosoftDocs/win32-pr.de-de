---
title: Iwmdrmlicense GetNext-Methode (wmdrmsdk. h)
description: Die GetNext-Methode lädt die Informationen zum nächsten Element in der Liste.
ms.assetid: 5ef91751-2883-4a8e-9908-7a6dfe6d2af3
keywords:
- GetNext-Methode (Windows Media-Format)
- GetNext-Methode Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, GetNext-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetNext
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da1dd1f8ce41648c7a67730d909058d10d616e7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354092"
---
# <a name="iwmdrmlicensegetnext-method"></a><span data-ttu-id="4e76f-106">Iwmdrmlicense:: GetNext-Methode</span><span class="sxs-lookup"><span data-stu-id="4e76f-106">IWMDRMLicense::GetNext method</span></span>

<span data-ttu-id="4e76f-107">Die **GetNext** -Methode lädt die Informationen zum nächsten Element in der Liste.</span><span class="sxs-lookup"><span data-stu-id="4e76f-107">The **GetNext** method loads the information about the next item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e76f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e76f-108">Syntax</span></span>


```C++
HRESULT GetNext();
```



## <a name="parameters"></a><span data-ttu-id="4e76f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e76f-109">Parameters</span></span>

<span data-ttu-id="4e76f-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4e76f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e76f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4e76f-111">Return value</span></span>

<span data-ttu-id="4e76f-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="4e76f-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4e76f-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4e76f-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4e76f-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4e76f-114">Return code</span></span>                                                                                                | <span data-ttu-id="4e76f-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e76f-115">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="4e76f-116"><dt>**NS \_ E \_ DRM- \_ RIV \_ zu \_ klein**</dt></span><span class="sxs-lookup"><span data-stu-id="4e76f-116"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="4e76f-117">Es wird eine aktualisierte Inhalts Sperr Liste benötigt.</span><span class="sxs-lookup"><span data-stu-id="4e76f-117">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="4e76f-118"><dt>**Fehler \_ keine \_ weiteren \_ Elemente**</dt></span><span class="sxs-lookup"><span data-stu-id="4e76f-118"><dt>**ERROR\_NO\_MORE\_ITEMS**</dt></span></span> </dl>      | <span data-ttu-id="4e76f-119">In der Liste sind keine Elemente mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="4e76f-119">There are no more items in the list.</span></span><br/>          |
| <dl> <span data-ttu-id="4e76f-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4e76f-120"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="4e76f-121">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e76f-121">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="4e76f-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4e76f-122">Remarks</span></span>

<span data-ttu-id="4e76f-123">Die Methoden der [**iwmdrmlicense**](iwmdrmlicense.md) -Schnittstelle stellen jeweils Daten zu einer einzelnen Lizenz bereit.</span><span class="sxs-lookup"><span data-stu-id="4e76f-123">The methods of the [**IWMDRMLicense**](iwmdrmlicense.md) interface provide data about a single license at a time.</span></span> <span data-ttu-id="4e76f-124">Das zugrunde liegende-Objekt enthält eine Liste mit mindestens einer Lizenz.</span><span class="sxs-lookup"><span data-stu-id="4e76f-124">The underlying object contains a list of one or more licenses.</span></span> <span data-ttu-id="4e76f-125">Wenn Sie diese Methode aufgerufen haben, verschiebt die-Schnittstelle Ihre internen Verweise auf die nächste Lizenz in der Liste.</span><span class="sxs-lookup"><span data-stu-id="4e76f-125">When you call this method, the interface moves its internal references to the next license in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e76f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e76f-126">Requirements</span></span>



| <span data-ttu-id="4e76f-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4e76f-127">Requirement</span></span> | <span data-ttu-id="4e76f-128">Wert</span><span class="sxs-lookup"><span data-stu-id="4e76f-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e76f-129">Header</span><span class="sxs-lookup"><span data-stu-id="4e76f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4e76f-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e76f-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="4e76f-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4e76f-131">Library</span></span><br/> | <dl> <span data-ttu-id="4e76f-132"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e76f-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e76f-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e76f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e76f-134">**Iwmdrmlicense-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="4e76f-134">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





