---
title: Iwmdrmsecurity getrevocationdataversion-Methode (wmdrmsdk. h)
description: Die getrevocationdataversion-Methode ruft die Versionsnummer einer Zertifikat Sperr Liste im lokalen Speicher ab.
ms.assetid: 2fa13b38-02c2-4c81-938b-409cadca00fb
keywords:
- Getrevocationdataversion-Methode Windows Media-Format
- Getrevocationdataversion-Methode Windows Media-Format, iwmdrmsecurity-Schnittstelle
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, getrevocationdataversion-Methode
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationDataVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705f02622b7298134328b513aa038804995eb1c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356357"
---
# <a name="iwmdrmsecuritygetrevocationdataversion-method"></a><span data-ttu-id="ef771-106">Iwmdrmsecurity:: getrevocationdataversion-Methode</span><span class="sxs-lookup"><span data-stu-id="ef771-106">IWMDRMSecurity::GetRevocationDataVersion method</span></span>

<span data-ttu-id="ef771-107">Die **getrevocationdataversion** -Methode ruft die Versionsnummer einer Zertifikat Sperr Liste im lokalen Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="ef771-107">The **GetRevocationDataVersion** method retrieves the version number of a certificate revocation list in the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef771-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef771-108">Syntax</span></span>


```C++
HRESULT GetRevocationDataVersion(
  [in]  REFGUID   f_guidRevocationType,
  [out] ULONGLONG *f_pdwCRLVersion
);
```



## <a name="parameters"></a><span data-ttu-id="ef771-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef771-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef771-110">*f \_ guidrevocationtype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ef771-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef771-111">GUID, die den Typ der Sperr Liste angibt.</span><span class="sxs-lookup"><span data-stu-id="ef771-111">GUID specifying the type of revocation list.</span></span> <span data-ttu-id="ef771-112">Legen Sie auf eine der Konstanten in der folgenden Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="ef771-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="ef771-113">GUID-Konstante</span><span class="sxs-lookup"><span data-stu-id="ef771-113">GUID constant</span></span>                 | <span data-ttu-id="ef771-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef771-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ef771-115">WMDRM- \_ revocationtype- \_ App</span><span class="sxs-lookup"><span data-stu-id="ef771-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="ef771-116">Gibt die Sperr Liste für das Anwendungs Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="ef771-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="ef771-117">WMDRM- \_ revocationtype- \_ Gerät</span><span class="sxs-lookup"><span data-stu-id="ef771-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="ef771-118">Gibt die Zertifikat Sperr Liste für das Gerät an.</span><span class="sxs-lookup"><span data-stu-id="ef771-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="ef771-119">WMDRM \_ revocationtype \_ Cardea</span><span class="sxs-lookup"><span data-stu-id="ef771-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="ef771-120">Gibt die Zertifikat Sperr Liste für Windows Media DRM für Netzwerkgeräte an.</span><span class="sxs-lookup"><span data-stu-id="ef771-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="ef771-121">*f \_ pdwcrlversion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ef771-121">*f\_pdwCRLVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef771-122">Variable, die die Versionsnummer empfängt.</span><span class="sxs-lookup"><span data-stu-id="ef771-122">Variable that receives the version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef771-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ef771-123">Return value</span></span>

<span data-ttu-id="ef771-124">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="ef771-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ef771-125">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ef771-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ef771-126">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ef771-126">Return code</span></span>                                                                          | <span data-ttu-id="ef771-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef771-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ef771-128"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ef771-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ef771-129">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef771-129">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ef771-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef771-130">Requirements</span></span>



| <span data-ttu-id="ef771-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef771-131">Requirement</span></span> | <span data-ttu-id="ef771-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ef771-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef771-133">Header</span><span class="sxs-lookup"><span data-stu-id="ef771-133">Header</span></span><br/>  | <dl> <span data-ttu-id="ef771-134"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef771-134"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef771-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ef771-135">Library</span></span><br/> | <dl> <span data-ttu-id="ef771-136"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef771-136"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef771-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef771-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef771-138">**Automatisierte Sperrung und Erneuerung von Komponenten**</span><span class="sxs-lookup"><span data-stu-id="ef771-138">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="ef771-139">**Getrevocationdata**</span><span class="sxs-lookup"><span data-stu-id="ef771-139">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[<span data-ttu-id="ef771-140">**Iwmdrmsecurity-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ef771-140">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="ef771-141">**"Abtrevocationdata"**</span><span class="sxs-lookup"><span data-stu-id="ef771-141">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





