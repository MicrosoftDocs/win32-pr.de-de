---
title: Iwmdrmlicencmanagement | atelicenabenumeration-Methode (wmdrmsdk. h)
description: Die Methode "samatelicenseenumeration" erstellt ein Lizenz-Enumeratorobjekt, mit dem Sie Informationen zu Lizenzen im lokalen Lizenz Speicher erhalten können.
ms.assetid: 48da1ef4-89bc-4cba-b5c9-0e202eb2986f
keywords:
- Windows Media-Format für die Methode "samatelicenabenumeration"
- Methode "kreatelicenabenumeration" Windows Media-Format, iwmdrmlicensitzungsschnittstelle
- Iwmdrmlicencmanagement-Schnittstelle Windows Media-Format, Methode "kreatelicenabenumeration"
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb75d21cc640da39c3679ac118ead629b24f719
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364586"
---
# <a name="iwmdrmlicensemanagementcreatelicenseenumeration-method"></a><span data-ttu-id="c4446-106">Iwmdrmlicenaberation-Methode</span><span class="sxs-lookup"><span data-stu-id="c4446-106">IWMDRMLicenseManagement::CreateLicenseEnumeration method</span></span>

<span data-ttu-id="c4446-107">Die Methode " **samatelicenseenumeration** " erstellt ein Lizenz-Enumeratorobjekt, mit dem Sie Informationen zu Lizenzen im lokalen Lizenz Speicher erhalten können.</span><span class="sxs-lookup"><span data-stu-id="c4446-107">The **CreateLicenseEnumeration** method creates a license enumerator object with which you can get information about licenses in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4446-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4446-108">Syntax</span></span>


```C++
HRESULT CreateLicenseEnumeration(
  [in]  WMDRM_LICENSE_FILTER *pLicenseFilter,
  [out] IWMDRMLicense        **pEnumerator
);
```



## <a name="parameters"></a><span data-ttu-id="c4446-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4446-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4446-110">*plicenabfilter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4446-110">*pLicenseFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4446-111">Zeiger auf eine [**WMDRM- \_ Lizenz \_ Filter**](wmdrm-license-filter.md) Struktur, die die Filter Parameter für die Liste der Lizenzen im Enumerator enthält.</span><span class="sxs-lookup"><span data-stu-id="c4446-111">Pointer to a [**WMDRM\_LICENSE\_FILTER**](wmdrm-license-filter.md) structure containing the filtering parameters for the list of licenses in the enumerator.</span></span>

</dd> <dt>

<span data-ttu-id="c4446-112">*Pendler* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c4446-112">*pEnumerator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4446-113">Ein Zeiger, der die Adresse der [**iwmdrmlicense**](iwmdrmlicense.md) -Schnittstelle des neu erstellten License-Enumeratorobjekts empfängt.</span><span class="sxs-lookup"><span data-stu-id="c4446-113">Pointer that receives the address of the [**IWMDRMLicense**](iwmdrmlicense.md) interface of the newly created license enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4446-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4446-114">Return value</span></span>

<span data-ttu-id="c4446-115">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="c4446-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c4446-116">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c4446-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c4446-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c4446-117">Return code</span></span>                                                                                                | <span data-ttu-id="c4446-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4446-118">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="c4446-119"><dt>**NS \_ E \_ DRM- \_ RIV \_ zu \_ klein**</dt></span><span class="sxs-lookup"><span data-stu-id="c4446-119"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="c4446-120">Es wird eine aktualisierte Inhalts Sperr Liste benötigt.</span><span class="sxs-lookup"><span data-stu-id="c4446-120">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="c4446-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c4446-121"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="c4446-122">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4446-122">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="c4446-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4446-123">Remarks</span></span>

<span data-ttu-id="c4446-124">Keine.</span><span class="sxs-lookup"><span data-stu-id="c4446-124">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4446-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4446-125">Requirements</span></span>



| <span data-ttu-id="c4446-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4446-126">Requirement</span></span> | <span data-ttu-id="c4446-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c4446-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4446-128">Header</span><span class="sxs-lookup"><span data-stu-id="c4446-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c4446-129"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4446-129"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4446-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c4446-130">Library</span></span><br/> | <dl> <span data-ttu-id="c4446-131"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4446-131"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4446-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4446-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4446-133">**Auflisten von Lizenzen im lokalen Lizenz Speicher**</span><span class="sxs-lookup"><span data-stu-id="c4446-133">**Enumerating Licenses in the Local License Store**</span></span>](enumerating-licenses-in-the-local-license-store.md)
</dt> <dt>

[<span data-ttu-id="c4446-134">**Iwmdrmlicenabmanagement-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c4446-134">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





