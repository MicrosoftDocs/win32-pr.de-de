---
title: Iwmdrmlicenabmanagement-Methode "Delta-eLicense" (wmdrmsdk. h)
description: Mit der Methode "Delta-eLicense" wird eine Lizenz aus dem temporären lokalen Lizenz Speicher entfernt.
ms.assetid: 0aa7143a-845a-41a4-8b3c-a04c68ee280a
keywords:
- Delta-eLicense-Methode, Windows Media-Format
- Delta-eLicense-Methode, Windows Media-Format, iwmdrmlicencmanagement-Schnittstelle
- Iwmdrmlicencmanagement-Schnittstelle Windows Media-Format, Delta eLicense-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.DeleteLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d5b52f6277459f147285f46fc791669e56061a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373816"
---
# <a name="iwmdrmlicensemanagementdeletelicense-method"></a><span data-ttu-id="55c3e-106">Iwmdrmlicensmanagement::D eletelicense-Methode</span><span class="sxs-lookup"><span data-stu-id="55c3e-106">IWMDRMLicenseManagement::DeleteLicense method</span></span>

<span data-ttu-id="55c3e-107">Mit der Methode " **Delta-eLicense** " wird eine Lizenz aus dem temporären lokalen Lizenz Speicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="55c3e-107">The **DeleteLicense** method removes a license from the temporary local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="55c3e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="55c3e-108">Syntax</span></span>


```C++
HRESULT DeleteLicense(
  [in] BSTR  bstrKID,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="55c3e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="55c3e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55c3e-110">*bstrinkid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55c3e-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55c3e-111">Die Schlüssel-ID (Kid) der zu löschenden Lizenz.</span><span class="sxs-lookup"><span data-stu-id="55c3e-111">Key ID (KID) of the license to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="55c3e-112">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="55c3e-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55c3e-113">Options Flags zum Löschen von Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="55c3e-113">License deletion option flags.</span></span> <span data-ttu-id="55c3e-114">Legen Sie auf einen der Werte in der folgenden Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="55c3e-114">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="55c3e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="55c3e-115">Value</span></span>                                    | <span data-ttu-id="55c3e-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55c3e-116">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55c3e-117">WMDRM \_ - \_ Lizenz \_ sofort löschen</span><span class="sxs-lookup"><span data-stu-id="55c3e-117">WMDRM\_DELETE\_LICENSE\_IMMEDIATELY</span></span>      | <span data-ttu-id="55c3e-118">Gibt an, dass die Lizenz sofort aus dem Speicher entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="55c3e-118">Specifies that the license should be removed from the store immediately.</span></span>                                                                                                                              |
| <span data-ttu-id="55c3e-119">WMDRM \_ - \_ Lizenz \_ Markierung \_ zum \_ Löschen löschen</span><span class="sxs-lookup"><span data-stu-id="55c3e-119">WMDRM\_DELETE\_LICENSE\_MARK\_FOR\_PURGE</span></span> | <span data-ttu-id="55c3e-120">Gibt an, dass die Lizenz zum Löschen markiert werden soll, jedoch nicht aus dem Speicher entfernt werden soll, bis die [**cleanlicencstore**](iwmdrmlicensemanagement-cleanlicensestore.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="55c3e-120">Specifies that the license should be marked for deletion, but should not be removed from the store until the [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md) method is called.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55c3e-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="55c3e-121">Return value</span></span>

<span data-ttu-id="55c3e-122">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="55c3e-122">The method returns an **HRESULT**.</span></span> <span data-ttu-id="55c3e-123">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="55c3e-123">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="55c3e-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="55c3e-124">Return code</span></span>                                                                                            | <span data-ttu-id="55c3e-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="55c3e-125">Description</span></span>                                                                                                         |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="55c3e-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="55c3e-126"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="55c3e-127">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="55c3e-127">The method succeeded.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="55c3e-128"><dt>**DRM- \_ E \_ licensenotfound**</dt></span><span class="sxs-lookup"><span data-stu-id="55c3e-128"><dt>**DRM\_E\_LICENSENOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="55c3e-129">Die angegebene Lizenz ist nicht im Speicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="55c3e-129">The specified license does not exist in the store.</span></span><br/> <span data-ttu-id="55c3e-130">-ODER-</span><span class="sxs-lookup"><span data-stu-id="55c3e-130">- OR -</span></span><br/> <span data-ttu-id="55c3e-131">Der Speicher wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="55c3e-131">The store was not found.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="55c3e-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55c3e-132">Remarks</span></span>

<span data-ttu-id="55c3e-133">Zum Löschen von Lizenzen aus dem permanenten lokalen Lizenz Speicher müssen Sie die Lizenz Sperrung verwenden.</span><span class="sxs-lookup"><span data-stu-id="55c3e-133">To delete licenses from the permanent local license store, you must use license revocation.</span></span>

## <a name="requirements"></a><span data-ttu-id="55c3e-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55c3e-134">Requirements</span></span>



| <span data-ttu-id="55c3e-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55c3e-135">Requirement</span></span> | <span data-ttu-id="55c3e-136">Wert</span><span class="sxs-lookup"><span data-stu-id="55c3e-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55c3e-137">Header</span><span class="sxs-lookup"><span data-stu-id="55c3e-137">Header</span></span><br/>  | <dl> <span data-ttu-id="55c3e-138"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="55c3e-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="55c3e-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="55c3e-139">Library</span></span><br/> | <dl> <span data-ttu-id="55c3e-140"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55c3e-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55c3e-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55c3e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55c3e-142">**Iwmdrmlicenabmanagement-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="55c3e-142">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





