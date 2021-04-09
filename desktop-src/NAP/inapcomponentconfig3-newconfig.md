---
title: INapComponentConfig3 newconfig-Methode (napcommon. h)
description: Wird von System Integritätsprüfungen (SHVs) implementiert, um eine Möglichkeit zum Erstellen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.
ms.assetid: cea762d3-815d-4034-94c1-5fa9a859cce8
keywords:
- Newconfig-Methode, NAP
- Newconfig-Methode, NAP, INapComponentConfig3-Schnittstelle
- INapComponentConfig3 Interface NAP, newconfig-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig3.NewConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 924204068dbb66b22cc06d28966511d8922e0068
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103298"
---
# <a name="inapcomponentconfig3newconfig-method"></a><span data-ttu-id="7f08d-106">INapComponentConfig3:: newconfig-Methode</span><span class="sxs-lookup"><span data-stu-id="7f08d-106">INapComponentConfig3::NewConfig method</span></span>

> [!Note]  
> <span data-ttu-id="7f08d-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7f08d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7f08d-108">Die **newconfig** -Methode wird von System Integritätsprüfungen (SHVs) implementiert, um eine Möglichkeit zum Erstellen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.</span><span class="sxs-lookup"><span data-stu-id="7f08d-108">The **NewConfig** method is implemented by system health validators (SHVs) to provide a way to create configuration data for a specific configuration ID.</span></span> <span data-ttu-id="7f08d-109">Wenn diese Funktion aufgerufen wird, muss ein SHV neue Konfigurationsdaten zuordnen und diese mit einer Kopie der Standard Konfigurationsdaten auffüllen.</span><span class="sxs-lookup"><span data-stu-id="7f08d-109">When this function is called, an SHV must allocate new configuration data and populate it with a copy of the default configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f08d-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f08d-110">Syntax</span></span>


```C++
HRESULT NewConfig(
   UINT32 configID
);
```



## <a name="parameters"></a><span data-ttu-id="7f08d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f08d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f08d-112">*ConfigID*</span><span class="sxs-lookup"><span data-stu-id="7f08d-112">*configID*</span></span> 
</dt> <dd>

<span data-ttu-id="7f08d-113">Ein-Wert, der die Konfiguration darstellt.</span><span class="sxs-lookup"><span data-stu-id="7f08d-113">A value that represents the configuration.</span></span> <span data-ttu-id="7f08d-114">*ConfigID* wird vom Netzwerk Richtlinien Server-Dienst (Network Policy Server, NPS) zugewiesen und ist innerhalb des SHV eindeutig.</span><span class="sxs-lookup"><span data-stu-id="7f08d-114">*ConfigID* is assigned by the Network Policy Server (NPS) service and is unique within the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f08d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f08d-115">Return value</span></span>

<span data-ttu-id="7f08d-116">Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="7f08d-116">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="7f08d-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7f08d-117">Return code</span></span>                                                                                                 | <span data-ttu-id="7f08d-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f08d-118">Description</span></span>                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7f08d-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7f08d-119"><dt>**S\_OK** </dt></span></span> </dl>                       | <span data-ttu-id="7f08d-120">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="7f08d-120">The operation is successful.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="7f08d-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="7f08d-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="7f08d-122">*ConfigID* ist 0 (ein Wert, der für die Standardkonfiguration reserviert ist).</span><span class="sxs-lookup"><span data-stu-id="7f08d-122">*ConfigID* is 0 (a value reserved for the default configuration).</span></span><br/>                  |
| <dl> <span data-ttu-id="7f08d-123"><dt>**NAP- \_ E- \_ SHV- \_ Konfiguration \_ vorhanden**</dt></span><span class="sxs-lookup"><span data-stu-id="7f08d-123"><dt>**NAP\_E\_SHV\_CONFIG\_EXISTED**</dt></span></span> </dl> | <span data-ttu-id="7f08d-124">Die *ConfigID* ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7f08d-124">*ConfigID* already exists.</span></span> <span data-ttu-id="7f08d-125">Die Liste der IDs, die NPS bekannt sind, unterscheidet sich vom SHV.</span><span class="sxs-lookup"><span data-stu-id="7f08d-125">The list of IDs known to NPS is different from the SHV.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7f08d-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f08d-126">Remarks</span></span>

<span data-ttu-id="7f08d-127">Nachdem die neue Konfiguration von **newconfig** erstellt wurde, sollten die Methoden [**getconfigfromid**](inapcomponentconfig3-getconfigfromid.md), [**invokeuifromconfigblob**](inapcomponentconfig2-invokeuifromconfigblob.md)und [**setconfigtoid**](inapcomponentconfig3-setconfigtoid.md) verwendet werden, um die Konfiguration nach Bedarf zu ändern.</span><span class="sxs-lookup"><span data-stu-id="7f08d-127">After the new configuration is created by **NewConfig**, the [**GetConfigFromID**](inapcomponentconfig3-getconfigfromid.md), [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md), and [**SetConfigToID**](inapcomponentconfig3-setconfigtoid.md) methods should be used to alter the configuration as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f08d-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f08d-128">Requirements</span></span>



| <span data-ttu-id="7f08d-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f08d-129">Requirement</span></span> | <span data-ttu-id="7f08d-130">Wert</span><span class="sxs-lookup"><span data-stu-id="7f08d-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f08d-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f08d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="7f08d-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7f08d-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="7f08d-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f08d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="7f08d-134">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f08d-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7f08d-135">Header</span><span class="sxs-lookup"><span data-stu-id="7f08d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f08d-136"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f08d-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="7f08d-137">IDL</span><span class="sxs-lookup"><span data-stu-id="7f08d-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7f08d-138"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7f08d-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f08d-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f08d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f08d-140">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="7f08d-140">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





