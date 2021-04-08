---
title: INapComponentConfig3 getconfigfromid-Methode (napcommon. h)
description: Wird von System Integritätsprüfungen (SHVs) implementiert, um eine Möglichkeit zum Abrufen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.
ms.assetid: 5c91681d-16d6-42f3-b1e0-c4b6e7561a73
keywords:
- Getconfigfromid-Methode NAP
- Getconfigfromid-Methode NAP, INapComponentConfig3-Schnittstelle
- INapComponentConfig3 Interface NAP, getconfigfromid-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig3.GetConfigFromID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce3a0e20f19c73271cdcba4070972649fe25aea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740937"
---
# <a name="inapcomponentconfig3getconfigfromid-method"></a><span data-ttu-id="76bda-106">INapComponentConfig3:: getconfigfromid-Methode</span><span class="sxs-lookup"><span data-stu-id="76bda-106">INapComponentConfig3::GetConfigFromID method</span></span>

> [!Note]  
> <span data-ttu-id="76bda-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="76bda-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="76bda-108">Die **getconfigfromid** -Methode wird von System Integritätsprüfungen (SHVs) implementiert, um eine Möglichkeit zum Abrufen von Konfigurationsdaten für eine bestimmte Konfigurations-ID zu bieten.</span><span class="sxs-lookup"><span data-stu-id="76bda-108">The **GetConfigFromID** method is implemented by system health validators (SHVs) to provide a way to obtain configuration data for a specific configuration ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="76bda-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="76bda-109">Syntax</span></span>


```C++
HRESULT GetConfigFromID(
  [in]  UINT32 configID,
  [out] UINT16 *count,
  [out] BYTE   **outdata
);
```



## <a name="parameters"></a><span data-ttu-id="76bda-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="76bda-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76bda-111">*ConfigID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76bda-111">*configID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76bda-112">Ein-Wert, der die Konfiguration darstellt.</span><span class="sxs-lookup"><span data-stu-id="76bda-112">A value that represents the configuration.</span></span> <span data-ttu-id="76bda-113">Wenn *ConfigID* den Wert **0** hat, sollte der SHV die Standard Konfigurationsdaten in *OutData* zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="76bda-113">If *ConfigID* is **0**, the SHV should return the default configuration data in *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="76bda-114">*Anzahl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="76bda-114">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76bda-115">Die Größe (in Bytes) der Konfigurationsdaten, die in *OutData* zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="76bda-115">The size, in bytes, of the configuration data returned in *outdata*.</span></span>

</dd> <dt>

<span data-ttu-id="76bda-116">*OutData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="76bda-116">*outdata* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76bda-117">Bei der Rückgabe ein Bytearray, das die von der *ConfigID* dargestellten Konfigurationsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="76bda-117">On return, a BYTE array that contains the configuration data represented by *ConfigID*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76bda-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76bda-118">Return value</span></span>

<span data-ttu-id="76bda-119">Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="76bda-119">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="76bda-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="76bda-120">Return code</span></span>                                                                                                    | <span data-ttu-id="76bda-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76bda-121">Description</span></span>                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="76bda-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="76bda-122"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="76bda-123">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="76bda-123">The operation is successful.</span></span><br/> |
| <dl> <span data-ttu-id="76bda-124"><dt>**NAP- \_ E- \_ SHV- \_ Konfiguration \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="76bda-124"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="76bda-125">*ConfigID* kann nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="76bda-125">*ConfigID* cannot be found.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="76bda-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76bda-126">Remarks</span></span>

<span data-ttu-id="76bda-127">Die [**newconfig**](inapcomponentconfig3-newconfig.md) -Methode muss verwendet werden, um Konfigurationsdaten für die *ConfigID* zuzuordnen, bevor diese Methode aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="76bda-127">The [**NewConfig**](inapcomponentconfig3-newconfig.md) method must be used to allocate configuration data for *ConfigID* before this method can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="76bda-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76bda-128">Requirements</span></span>



| <span data-ttu-id="76bda-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76bda-129">Requirement</span></span> | <span data-ttu-id="76bda-130">Wert</span><span class="sxs-lookup"><span data-stu-id="76bda-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="76bda-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76bda-131">Minimum supported client</span></span><br/> | <span data-ttu-id="76bda-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="76bda-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="76bda-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76bda-133">Minimum supported server</span></span><br/> | <span data-ttu-id="76bda-134">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76bda-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76bda-135">Header</span><span class="sxs-lookup"><span data-stu-id="76bda-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="76bda-136"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="76bda-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="76bda-137">IDL</span><span class="sxs-lookup"><span data-stu-id="76bda-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="76bda-138"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="76bda-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76bda-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76bda-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76bda-140">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="76bda-140">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





