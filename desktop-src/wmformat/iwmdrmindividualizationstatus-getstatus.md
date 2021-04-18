---
title: Iwmdrmindividualizationstatus GetStatus-Methode (wmdrmsdk. h)
description: Mit der GetStatus-Methode werden ausführliche Informationen zum Individualisierungs Fortschritt abgerufen.
ms.assetid: 8985f3cc-006d-4fd5-b218-d3af3473b8e3
keywords:
- GetStatus-Methode Windows Media-Format
- GetStatus-Methode Windows Media-Format, iwmdrmindividualizationstatus-Schnittstelle
- Iwmdrmindividualizationstatus-Schnittstelle Windows Media-Format, GetStatus-Methode
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus.GetStatus
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f144f188de46d17702dd22aa12e2245156b59a21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371130"
---
# <a name="iwmdrmindividualizationstatusgetstatus-method"></a><span data-ttu-id="811ed-106">Iwmdrmindividualizationstatus:: GetStatus-Methode</span><span class="sxs-lookup"><span data-stu-id="811ed-106">IWMDRMIndividualizationStatus::GetStatus method</span></span>

<span data-ttu-id="811ed-107">Mit der **GetStatus** -Methode werden ausführliche Informationen zum Individualisierungs Fortschritt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="811ed-107">The **GetStatus** method retrieves detailed information about individualization progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="811ed-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="811ed-108">Syntax</span></span>


```C++
HRESULT GetStatus(
  [out] WM_INDIVIDUALIZE_STATUS *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="811ed-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="811ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="811ed-110">*pstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="811ed-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="811ed-111">Empfängt eine [**WM \_ Individual- \_ Status**](drmwm-individualize-status.md) Struktur, die ausführliche Informationen zum Status des Individualisierungs Versuchs enthält.</span><span class="sxs-lookup"><span data-stu-id="811ed-111">Receives a [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure containing detailed information about the status of the individualization attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="811ed-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="811ed-112">Return value</span></span>

<span data-ttu-id="811ed-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="811ed-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="811ed-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="811ed-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="811ed-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="811ed-115">Return code</span></span>                                                                          | <span data-ttu-id="811ed-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="811ed-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="811ed-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="811ed-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="811ed-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="811ed-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="811ed-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="811ed-119">Remarks</span></span>

<span data-ttu-id="811ed-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="811ed-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="811ed-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="811ed-121">Requirements</span></span>



| <span data-ttu-id="811ed-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="811ed-122">Requirement</span></span> | <span data-ttu-id="811ed-123">Wert</span><span class="sxs-lookup"><span data-stu-id="811ed-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="811ed-124">Header</span><span class="sxs-lookup"><span data-stu-id="811ed-124">Header</span></span><br/> | <dl> <span data-ttu-id="811ed-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="811ed-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="811ed-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="811ed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="811ed-127">**Iwmdrmindividualizationstatus-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="811ed-127">**IWMDRMIndividualizationStatus Interface**</span></span>](iwmdrmindividualizationstatus.md)
</dt> </dl>

 

 





