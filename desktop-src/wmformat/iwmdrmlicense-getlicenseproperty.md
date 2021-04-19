---
title: Iwmdrmlicense getlicencproperty-Methode (wmdrmsdk. h)
description: Die getlicencproperty-Methode ruft eine Eigenschaft aus der aktuellen Lizenz ab.
ms.assetid: 5431f849-b37e-40b7-8bdb-ee30948aeff1
keywords:
- Getlicentproperty-Methode, Windows Media-Format
- Getlicentproperty-Methode, Windows Media-Format, iwmdrmlicense-Schnittstelle
- Iwmdrmlicense-Schnittstelle Windows Media-Format, getlicentproperty-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicenseProperty
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf7fe91c57b9c69934f093cdd504b5e6d35efb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370591"
---
# <a name="iwmdrmlicensegetlicenseproperty-method"></a><span data-ttu-id="0fdd6-106">Iwmdrmlicense:: getlicencproperty-Methode</span><span class="sxs-lookup"><span data-stu-id="0fdd6-106">IWMDRMLicense::GetLicenseProperty method</span></span>

<span data-ttu-id="0fdd6-107">Die **getlicencproperty** -Methode ruft eine Eigenschaft aus der aktuellen Lizenz ab.</span><span class="sxs-lookup"><span data-stu-id="0fdd6-107">The **GetLicenseProperty** method retrieves a property from the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fdd6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fdd6-108">Syntax</span></span>


```C++
HRESULT GetLicenseProperty(
  [in]  BSTR        bstrName,
  [out] PROPVARIANT *ppropVariant
);
```



## <a name="parameters"></a><span data-ttu-id="0fdd6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fdd6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fdd6-110">*bstrinname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0fdd6-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0fdd6-111">Der Name der abzurufenden Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0fdd6-111">Name of the property to retrieve.</span></span> <span data-ttu-id="0fdd6-112">Legen Sie auf eine der Konstanten in der folgenden Tabelle fest:</span><span class="sxs-lookup"><span data-stu-id="0fdd6-112">Set to one of the constants in the following table:</span></span>



| <span data-ttu-id="0fdd6-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="0fdd6-113">Constant</span></span>                   | <span data-ttu-id="0fdd6-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fdd6-114">Description</span></span>                                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fdd6-115">g \_ wszwmdrmnet-Sperrung \_</span><span class="sxs-lookup"><span data-stu-id="0fdd6-115">g\_wszWMDRMNet\_Revocation</span></span> | <span data-ttu-id="0fdd6-116">Verwenden Sie, um die Sperr Liste für Windows Media DRM für Netzwerkgeräte für die aktuelle Lizenz zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0fdd6-116">Use to get the Windows Media DRM for Network Devices revocation list for the current license.</span></span>                        |
| <span data-ttu-id="0fdd6-117">g \_ wszwmdrm ( \_ saplevel)</span><span class="sxs-lookup"><span data-stu-id="0fdd6-117">g\_wszWMDRM\_SAPLEVEL</span></span>      | <span data-ttu-id="0fdd6-118">Verwenden Sie, um die SAP-Ebene (Secure audiopath) zu erhalten, die zur Wiedergabe von Inhalten erforderlich ist, die von der aktuellen</span><span class="sxs-lookup"><span data-stu-id="0fdd6-118">Use to get the Secure Audio Path (SAP) level required to play content covered by the current license.</span></span>                |
| <span data-ttu-id="0fdd6-119">g \_ wszwmdrm \_ saprequired</span><span class="sxs-lookup"><span data-stu-id="0fdd6-119">g\_wszWMDRM\_SAPRequired</span></span>   | <span data-ttu-id="0fdd6-120">Verwenden Sie, um zu überprüfen, ob für die aktuelle Lizenz SAP zum Wiedergeben des Inhalts erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="0fdd6-120">Use to ascertain whether the current license requires SAP be used to play the content.</span></span>                               |
| <span data-ttu-id="0fdd6-121">g \_ wszwmdrm \_ SourceID</span><span class="sxs-lookup"><span data-stu-id="0fdd6-121">g\_wszWMDRM\_SOURCEID</span></span>      | <span data-ttu-id="0fdd6-122">Verwenden Sie, um den Quell Bezeichner für die aktuelle Lizenz zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0fdd6-122">Use to get the source identifier for the current license.</span></span>                                                            |
| <span data-ttu-id="0fdd6-123">g \_ wszwmdrm- \_ Priorität</span><span class="sxs-lookup"><span data-stu-id="0fdd6-123">g\_wszWMDRM\_PRIORITY</span></span>      | <span data-ttu-id="0fdd6-124">Verwenden Sie, um die Priorität der aktuellen Lizenz zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="0fdd6-124">Use to get the priority of the current license.</span></span> <span data-ttu-id="0fdd6-125">Lizenzen mit höherer Priorität werden vor Lizenzen mit niedrigerer Priorität angewendet.</span><span class="sxs-lookup"><span data-stu-id="0fdd6-125">Higher priority licenses are applied before lower priority licenses.</span></span> |
| <span data-ttu-id="0fdd6-126">g \_ wszwmdrm \_ uplinkid</span><span class="sxs-lookup"><span data-stu-id="0fdd6-126">g\_wszWMDRM\_UplinkID</span></span>      | <span data-ttu-id="0fdd6-127">Verwenden Sie, um die Schlüssel-ID der Stamm Lizenz in der Lizenz Kette zu erhalten, zu der die aktuelle Lizenz gehört.</span><span class="sxs-lookup"><span data-stu-id="0fdd6-127">Use to get the key ID of the root license in the license chain that the current license belongs to.</span></span>                  |



 

</dd> <dt>

<span data-ttu-id="0fdd6-128">*ppropvariant* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0fdd6-128">*ppropVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fdd6-129">Empfängt den-Eigenschafts Wert.</span><span class="sxs-lookup"><span data-stu-id="0fdd6-129">Receives the property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fdd6-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0fdd6-130">Return value</span></span>

<span data-ttu-id="0fdd6-131">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="0fdd6-131">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0fdd6-132">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0fdd6-132">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0fdd6-133">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0fdd6-133">Return code</span></span>                                                                          | <span data-ttu-id="0fdd6-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fdd6-134">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0fdd6-135"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0fdd6-135"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0fdd6-136">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0fdd6-136">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0fdd6-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0fdd6-137">Remarks</span></span>

<span data-ttu-id="0fdd6-138">Keine.</span><span class="sxs-lookup"><span data-stu-id="0fdd6-138">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fdd6-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fdd6-139">Requirements</span></span>



| <span data-ttu-id="0fdd6-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fdd6-140">Requirement</span></span> | <span data-ttu-id="0fdd6-141">Wert</span><span class="sxs-lookup"><span data-stu-id="0fdd6-141">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fdd6-142">Header</span><span class="sxs-lookup"><span data-stu-id="0fdd6-142">Header</span></span><br/>  | <dl> <span data-ttu-id="0fdd6-143"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fdd6-143"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="0fdd6-144">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0fdd6-144">Library</span></span><br/> | <dl> <span data-ttu-id="0fdd6-145"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fdd6-145"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fdd6-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fdd6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fdd6-147">**GetLicense**</span><span class="sxs-lookup"><span data-stu-id="0fdd6-147">**GetLicense**</span></span>](iwmdrmlicense-getlicense.md)
</dt> <dt>

[<span data-ttu-id="0fdd6-148">**Iwmdrmlicense-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0fdd6-148">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





