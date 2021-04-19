---
title: Iwmdrmlicense canpersistent-Methode (wmdrmsdk. h)
description: Die canpersistent-Methode fragt ab, ob die Lizenz in einem lokalen Lizenz Speicher persistent gespeichert werden kann.
ms.assetid: 040b30d8-4e47-44a3-8b09-e81cc30e8a53
keywords:
- Canpersistent-Methode Windows Media-Format
- Canpersistent-Methode Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, canpersistent-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.CanPersist
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7772dac73b99443626b1eeec6f5e90851f92c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354194"
---
# <a name="iwmdrmlicensecanpersist-method"></a><span data-ttu-id="3455a-106">Iwmdrmlicense:: canpersistent-Methode</span><span class="sxs-lookup"><span data-stu-id="3455a-106">IWMDRMLicense::CanPersist method</span></span>

<span data-ttu-id="3455a-107">Die **canpersistent** -Methode fragt ab, ob die Lizenz in einem lokalen Lizenz Speicher persistent gespeichert werden kann.</span><span class="sxs-lookup"><span data-stu-id="3455a-107">The **CanPersist** method queries whether the license can be persisted on in a local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="3455a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3455a-108">Syntax</span></span>


```C++
HRESULT CanPersist(
  [out] BOOL *pfCanPersist
);
```



## <a name="parameters"></a><span data-ttu-id="3455a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3455a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3455a-110">*pfcanpersistent* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3455a-110">*pfCanPersist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3455a-111">TRUE gibt an, dass die Lizenz beibehalten werden kann.</span><span class="sxs-lookup"><span data-stu-id="3455a-111">TRUE indicates that the license can be persisted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3455a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3455a-112">Return value</span></span>

<span data-ttu-id="3455a-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="3455a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3455a-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3455a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3455a-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3455a-115">Return code</span></span>                                                                          | <span data-ttu-id="3455a-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3455a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3455a-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3455a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3455a-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3455a-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3455a-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3455a-119">Remarks</span></span>

<span data-ttu-id="3455a-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="3455a-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="3455a-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3455a-121">Requirements</span></span>



| <span data-ttu-id="3455a-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3455a-122">Requirement</span></span> | <span data-ttu-id="3455a-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3455a-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3455a-124">Header</span><span class="sxs-lookup"><span data-stu-id="3455a-124">Header</span></span><br/> | <dl> <span data-ttu-id="3455a-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="3455a-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3455a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3455a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3455a-127">**Iwmdrmlicense-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="3455a-127">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





