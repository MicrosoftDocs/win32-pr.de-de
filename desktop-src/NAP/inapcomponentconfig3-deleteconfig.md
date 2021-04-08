---
title: INapComponentConfig3 DeleteConfig-Methode (napcommon. h)
description: Wird von System Integritätsprüfungen (SHVs) implementiert, um eine Möglichkeit zum Löschen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.
ms.assetid: 9740c122-86c8-4b77-9268-faa90e84d8aa
keywords:
- DeleteConfig-Methode NAP
- DeleteConfig-Methode, NAP, INapComponentConfig3-Schnittstelle
- INapComponentConfig3 Interface NAP, DeleteConfig-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig3.DeleteConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a9b9a6838616f0892b45df34d9a7c5ed63ff16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740945"
---
# <a name="inapcomponentconfig3deleteconfig-method"></a><span data-ttu-id="40627-106">INapComponentConfig3::D eleteconfig-Methode</span><span class="sxs-lookup"><span data-stu-id="40627-106">INapComponentConfig3::DeleteConfig method</span></span>

> [!Note]  
> <span data-ttu-id="40627-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="40627-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="40627-108">Die **DeleteConfig** -Methode wird von System Integritätsprüfungen (SHVs) implementiert, um eine Möglichkeit zum Löschen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.</span><span class="sxs-lookup"><span data-stu-id="40627-108">The **DeleteConfig** method is implemented by system health validators (SHVs) to provide a way to delete configuration data for a specific configuration ID.</span></span> <span data-ttu-id="40627-109">Die ID kann wieder verwendet werden, nachdem die Konfigurationsdaten gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="40627-109">The ID may be reused after the configuration data has been deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="40627-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="40627-110">Syntax</span></span>


```C++
HRESULT DeleteConfig(
   UINT32 configID
);
```



## <a name="parameters"></a><span data-ttu-id="40627-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="40627-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40627-112">*ConfigID*</span><span class="sxs-lookup"><span data-stu-id="40627-112">*configID*</span></span> 
</dt> <dd>

<span data-ttu-id="40627-113">Ein-Wert, der die zu löschenden Konfigurationsdaten darstellt.</span><span class="sxs-lookup"><span data-stu-id="40627-113">A value that represents the configuration data to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40627-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40627-114">Return value</span></span>

<span data-ttu-id="40627-115">Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="40627-115">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="40627-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="40627-116">Return code</span></span>                                                                                                    | <span data-ttu-id="40627-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40627-117">Description</span></span>                                                                  |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="40627-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="40627-118"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="40627-119">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="40627-119">The operation is successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="40627-120"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="40627-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                   | <span data-ttu-id="40627-121">*ConfigID* ist 0 (ein Wert, der für die Standardkonfiguration reserviert ist).</span><span class="sxs-lookup"><span data-stu-id="40627-121">*ConfigID* is 0 (a value reserved for the default configuration).</span></span><br/> |
| <dl> <span data-ttu-id="40627-122"><dt>**NAP- \_ E- \_ SHV- \_ Konfiguration \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="40627-122"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="40627-123">*ConfigID* kann nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="40627-123">*ConfigID* cannot be found.</span></span><br/>                                       |



 

## <a name="requirements"></a><span data-ttu-id="40627-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40627-124">Requirements</span></span>



| <span data-ttu-id="40627-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40627-125">Requirement</span></span> | <span data-ttu-id="40627-126">Wert</span><span class="sxs-lookup"><span data-stu-id="40627-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="40627-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40627-127">Minimum supported client</span></span><br/> | <span data-ttu-id="40627-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="40627-128">None supported</span></span><br/>                                                                |
| <span data-ttu-id="40627-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40627-129">Minimum supported server</span></span><br/> | <span data-ttu-id="40627-130">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40627-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="40627-131">Header</span><span class="sxs-lookup"><span data-stu-id="40627-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="40627-132"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="40627-132"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="40627-133">IDL</span><span class="sxs-lookup"><span data-stu-id="40627-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="40627-134"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="40627-134"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40627-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40627-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40627-136">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="40627-136">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





