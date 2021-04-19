---
title: Iwmdrmlicense getanalogvideorestrictionlevels-Methode (wmdrmsdk. h)
description: Die getanalogvideorestrictionlevels-Methode ruft alle analogen Video Einschränkungen ab, die für die aktuelle Lizenz festgelegt sind.
ms.assetid: cf0ac7c0-236d-4d60-8850-81dc6754cf01
keywords:
- Getanalogvideorestrictionlevels-Methode Windows Media-Format
- Getanalogvideorestrictionlevels-Methode Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, getanalogvideorestrictionlevels-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetAnalogVideoRestrictionLevels
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a168f25381b807cc8c0cd17f7ba6764c3591513
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355895"
---
# <a name="iwmdrmlicensegetanalogvideorestrictionlevels-method"></a><span data-ttu-id="cf4f9-106">Iwmdrmlicense:: getanalogvideorestrictionlevels-Methode</span><span class="sxs-lookup"><span data-stu-id="cf4f9-106">IWMDRMLicense::GetAnalogVideoRestrictionLevels method</span></span>

<span data-ttu-id="cf4f9-107">Die **getanalogvideorestrictionlevels** -Methode ruft alle analogen Video Einschränkungen ab, die für die aktuelle Lizenz festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="cf4f9-107">The **GetAnalogVideoRestrictionLevels** method retrieves all analog video restrictions set on the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf4f9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf4f9-108">Syntax</span></span>


```C++
HRESULT GetAnalogVideoRestrictionLevels(
  [out]     WMDRM_ANALOG_VIDEO_RESTRICTIONS rgAnalogVideoRestrictions[],
  [in, out] DWORD                           *pcRestrictions
);
```



## <a name="parameters"></a><span data-ttu-id="cf4f9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf4f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf4f9-110">*rganalogvideorestrictions \[ \]* \[out\]</span><span class="sxs-lookup"><span data-stu-id="cf4f9-110">*rgAnalogVideoRestrictions\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf4f9-111">Empfängt ein Array von [**WMDRM-Strukturen für \_ analoge \_ Video \_ Einschränkungen**](wmdrm-analog-video-restrictions.md) .</span><span class="sxs-lookup"><span data-stu-id="cf4f9-111">Receives an array of [**WMDRM\_ANALOG\_VIDEO\_RESTRICTIONS**](wmdrm-analog-video-restrictions.md) structures.</span></span> <span data-ttu-id="cf4f9-112">Legen Sie diesen Wert auf **null** fest, um die Anzahl der Elemente im Array in " *PUP*" zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="cf4f9-112">Set to **NULL** to get the number of elements in the array in *pcResctrictions*.</span></span>

</dd> <dt>

<span data-ttu-id="cf4f9-113">*pkrestriktionen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cf4f9-113">*pcRestrictions* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf4f9-114">Die Anzahl der Elemente im Array von Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="cf4f9-114">The number of elements in the array of restrictions.</span></span> <span data-ttu-id="cf4f9-115">Wenn *rganalogvideorestrictions* auf **null** festgelegt ist, wird dieser Wert auf die Anzahl der Elemente festgelegt, die im Array benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="cf4f9-115">If *rgAnalogVideoRestrictions* is set to **NULL**, this value is set to the number of elements needed in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf4f9-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf4f9-116">Return value</span></span>

<span data-ttu-id="cf4f9-117">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="cf4f9-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cf4f9-118">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cf4f9-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cf4f9-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cf4f9-119">Return code</span></span>                                                                          | <span data-ttu-id="cf4f9-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf4f9-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="cf4f9-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cf4f9-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="cf4f9-122">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cf4f9-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cf4f9-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf4f9-123">Remarks</span></span>

<span data-ttu-id="cf4f9-124">Sie müssen für das Array von Einschränkungen Arbeitsspeicher zuweisen.</span><span class="sxs-lookup"><span data-stu-id="cf4f9-124">You must allocate memory for the array of restrictions.</span></span> <span data-ttu-id="cf4f9-125">Um dies zu tun, müssen Sie zuerst die-Methode aufrufen, wobei *rganalogvideorestrictions* auf **null** festgelegt ist, wodurch der Wert bei *pkrestrictions* auf die Anzahl der erforderlichen Elemente festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="cf4f9-125">To do so, first call the method with *rgAnalogVideoRestrictions* set to **NULL**, which will set the value at *pcRestrictions* to the number of required elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf4f9-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf4f9-126">Requirements</span></span>



| <span data-ttu-id="cf4f9-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf4f9-127">Requirement</span></span> | <span data-ttu-id="cf4f9-128">Wert</span><span class="sxs-lookup"><span data-stu-id="cf4f9-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4f9-129">Header</span><span class="sxs-lookup"><span data-stu-id="cf4f9-129">Header</span></span><br/>  | <dl> <span data-ttu-id="cf4f9-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf4f9-130"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf4f9-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cf4f9-131">Library</span></span><br/> | <dl> <span data-ttu-id="cf4f9-132"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf4f9-132"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf4f9-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf4f9-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf4f9-134">**Iwmdrmlicense-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cf4f9-134">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





