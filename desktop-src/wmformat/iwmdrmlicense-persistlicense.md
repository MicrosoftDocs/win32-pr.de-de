---
title: Iwmdrmlicense persistlicense-Methode (wmdrmsdk. h)
description: Die persistlicense-Methode speichert die aktuelle Lizenz aus dem temporären Speicher im permanenten lokalen Lizenz Speicher.
ms.assetid: 80a0f932-2800-416b-9dfe-97654a76c19b
keywords:
- Persistlicense-Methode Windows Media-Format
- Persistlicense-Methode Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, persistlicense-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.PersistLicense
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41b61cdf448d757d13917ca22af0c3d9d9d390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370073"
---
# <a name="iwmdrmlicensepersistlicense-method"></a><span data-ttu-id="107a5-106">Iwmdrmlicense::P ersistlicense-Methode</span><span class="sxs-lookup"><span data-stu-id="107a5-106">IWMDRMLicense::PersistLicense method</span></span>

<span data-ttu-id="107a5-107">Die **persistlicense** -Methode speichert die aktuelle Lizenz aus dem temporären Speicher im permanenten lokalen Lizenz Speicher.</span><span class="sxs-lookup"><span data-stu-id="107a5-107">The **PersistLicense** method saves the current license from the temporary store into the permanent local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="107a5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="107a5-108">Syntax</span></span>


```C++
HRESULT PersistLicense();
```



## <a name="parameters"></a><span data-ttu-id="107a5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="107a5-109">Parameters</span></span>

<span data-ttu-id="107a5-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="107a5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="107a5-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="107a5-111">Return value</span></span>

<span data-ttu-id="107a5-112">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="107a5-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="107a5-113">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="107a5-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="107a5-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="107a5-114">Return code</span></span>                                                                          | <span data-ttu-id="107a5-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="107a5-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="107a5-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="107a5-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="107a5-117">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="107a5-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="107a5-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="107a5-118">Remarks</span></span>

<span data-ttu-id="107a5-119">Wenn sich die aktuelle Lizenz nicht im temporären Speicher befindet, schlägt diese Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="107a5-119">If the current license is not in the temporary store, this method will fail.</span></span>

<span data-ttu-id="107a5-120">Sie können [**canpersistent**](iwmdrmlicense-canpersist.md) aufzurufen, um abzufragen, ob die Lizenz beibehalten werden darf.</span><span class="sxs-lookup"><span data-stu-id="107a5-120">You can call [**CanPersist**](iwmdrmlicense-canpersist.md) to query whether the license is allowed to be persisted.</span></span>

## <a name="requirements"></a><span data-ttu-id="107a5-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="107a5-121">Requirements</span></span>



| <span data-ttu-id="107a5-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="107a5-122">Requirement</span></span> | <span data-ttu-id="107a5-123">Wert</span><span class="sxs-lookup"><span data-stu-id="107a5-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="107a5-124">Header</span><span class="sxs-lookup"><span data-stu-id="107a5-124">Header</span></span><br/> | <dl> <span data-ttu-id="107a5-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="107a5-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="107a5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="107a5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="107a5-127">**Iwmdrmlicense-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="107a5-127">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





