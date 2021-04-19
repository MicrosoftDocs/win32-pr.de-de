---
title: INapComponentConfig3 setconfigtoid-Methode (napcommon. h)
description: Wird von System Integritätsprüfungen (SHVs) implementiert, um die Konfigurationsdaten für eine bestimmte Konfigurations-ID festzulegen.
ms.assetid: 1fa0b8e7-b597-4ab1-bb61-2cab47b92ce3
keywords:
- Setconfigtoid-Methode NAP
- Setconfigtoid-Methode NAP, INapComponentConfig3-Schnittstelle
- INapComponentConfig3 Interface NAP, setconfigtoid-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig3.SetConfigToID
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3158a216ba4fd4f82f3e4fc21fc1e0043b16a46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342674"
---
# <a name="inapcomponentconfig3setconfigtoid-method"></a><span data-ttu-id="315fd-106">INapComponentConfig3:: setconfigtoid-Methode</span><span class="sxs-lookup"><span data-stu-id="315fd-106">INapComponentConfig3::SetConfigToID method</span></span>

> [!Note]  
> <span data-ttu-id="315fd-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="315fd-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="315fd-108">Die **setconfigtoid** -Methode wird von System Integritätsprüfungen (SHVs) implementiert, um die Konfigurationsdaten für eine bestimmte Konfigurations-ID festzulegen.</span><span class="sxs-lookup"><span data-stu-id="315fd-108">The **SetConfigToID** method is implemented by system health validators (SHVs) to provide a way to set the configuration data for a specific configuration ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="315fd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="315fd-109">Syntax</span></span>


```C++
HRESULT SetConfigToID(
  [in] UINT32 configID,
  [in] UINT16 count,
  [in] BYTE   *data
);
```



## <a name="parameters"></a><span data-ttu-id="315fd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="315fd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="315fd-111">*ConfigID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="315fd-111">*configID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="315fd-112">Ein-Wert, der die Konfiguration darstellt.</span><span class="sxs-lookup"><span data-stu-id="315fd-112">A value that represents the configuration.</span></span> <span data-ttu-id="315fd-113">*ConfigID* wird vom Netzwerk Richtlinien Server-Dienst (Network Policy Server, NPS) zugewiesen und ist innerhalb des SHV eindeutig.</span><span class="sxs-lookup"><span data-stu-id="315fd-113">*ConfigID* is assigned by the Network Policy Server (NPS) service and is unique within the SHV.</span></span> <span data-ttu-id="315fd-114">Wenn *ConfigID* den Wert 0 hat, wird die Standardkonfiguration des SHV festgelegt.</span><span class="sxs-lookup"><span data-stu-id="315fd-114">If *ConfigID* is 0, the default configuration of the SHV is set.</span></span>

</dd> <dt>

<span data-ttu-id="315fd-115">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="315fd-115">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="315fd-116">Die Größe der Konfigurationsdaten in *Daten* in Bytes.</span><span class="sxs-lookup"><span data-stu-id="315fd-116">The size, in bytes, of the configuration data in *data*.</span></span>

</dd> <dt>

<span data-ttu-id="315fd-117">*Daten* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="315fd-117">*data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="315fd-118">Bei Eingabe ein Bytearray, das das Konfigurations DataSet auf *ConfigID* enthält.</span><span class="sxs-lookup"><span data-stu-id="315fd-118">On input, a BYTE array that contains the configuration data set to *ConfigID*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="315fd-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="315fd-119">Return value</span></span>

<span data-ttu-id="315fd-120">Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="315fd-120">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="315fd-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="315fd-121">Return code</span></span>                                                                                                    | <span data-ttu-id="315fd-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="315fd-122">Description</span></span>                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="315fd-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="315fd-123"><dt>**S\_OK** </dt></span></span> </dl>                          | <span data-ttu-id="315fd-124">Der Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="315fd-124">The operation is successful.</span></span><br/> |
| <dl> <span data-ttu-id="315fd-125"><dt>**NAP- \_ E- \_ SHV- \_ Konfiguration \_ nicht \_ gefunden**</dt></span><span class="sxs-lookup"><span data-stu-id="315fd-125"><dt>**NAP\_E\_SHV\_CONFIG\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="315fd-126">*ConfigID* kann nicht gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="315fd-126">*ConfigID* cannot be found.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="315fd-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="315fd-127">Remarks</span></span>

<span data-ttu-id="315fd-128">Die [**newconfig**](inapcomponentconfig3-newconfig.md) -Methode muss verwendet werden, um Konfigurationsdaten für die *ConfigID* zuzuordnen, bevor diese Methode aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="315fd-128">The [**NewConfig**](inapcomponentconfig3-newconfig.md) method must be used to allocate configuration data for *ConfigID* before this method can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="315fd-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="315fd-129">Requirements</span></span>



| <span data-ttu-id="315fd-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="315fd-130">Requirement</span></span> | <span data-ttu-id="315fd-131">Wert</span><span class="sxs-lookup"><span data-stu-id="315fd-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="315fd-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="315fd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="315fd-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="315fd-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="315fd-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="315fd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="315fd-135">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="315fd-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="315fd-136">Header</span><span class="sxs-lookup"><span data-stu-id="315fd-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="315fd-137"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="315fd-137"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="315fd-138">IDL</span><span class="sxs-lookup"><span data-stu-id="315fd-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="315fd-139"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="315fd-139"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="315fd-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="315fd-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="315fd-141">**INapComponentConfig3**</span><span class="sxs-lookup"><span data-stu-id="315fd-141">**INapComponentConfig3**</span></span>](inapcomponentconfig3.md)
</dt> </dl>

 

 





