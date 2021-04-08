---
title: INapComponentConfig2 isremoteconfigsupported-Methode (napcommon. h)
description: Wird von System Integritätsprüfungen (SHVs) implementiert, um anzugeben, ob die Remote Konfiguration unterstützt wird.
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- Isremoteconfigsupported-Methode NAP
- Isremoteconfigsupported-Methode, NAP, INapComponentConfig2-Schnittstelle
- INapComponentConfig2 Interface NAP, isremoteconfigsupported-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig2.IsRemoteConfigSupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d144926aafff6f5ad7e243efe2a81a2955f497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949673"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a><span data-ttu-id="68584-106">INapComponentConfig2:: isremoteconfigsupported-Methode</span><span class="sxs-lookup"><span data-stu-id="68584-106">INapComponentConfig2::IsRemoteConfigSupported method</span></span>

> [!Note]  
> <span data-ttu-id="68584-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="68584-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="68584-108">Die **isremoteconfigsupported** -Methode wird von System Integritätsprüfungen (SHVs) implementiert, um anzugeben, ob die Remote Konfiguration unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="68584-108">The **IsRemoteConfigSupported** method is implemented by system health validators (SHVs) to indicate whether remote configuration is supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="68584-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="68584-109">Syntax</span></span>


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a><span data-ttu-id="68584-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="68584-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68584-111">*IsSupported* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="68584-111">*isSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68584-112">Ein Zeiger auf einen booleschen Wert, der auf **true** festgelegt ist, wenn die Komponente die Remote Konfiguration unterstützt, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="68584-112">A pointer to a BOOL that is set to **TRUE** if the component supports remote configuration, and **FALSE** if it does not.</span></span>

</dd> <dt>

<span data-ttu-id="68584-113">*remoteconfigtype* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="68584-113">*remoteConfigType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68584-114">Gibt den Typ der Remote Konfiguration an, der mit dem Wert aus der [**remoteconfigurationtype**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) -Enumeration unterstützt wird:</span><span class="sxs-lookup"><span data-stu-id="68584-114">Indicates the type of remote configuration supported using value from the [**RemoteConfigurationType**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) enumeration:</span></span>



| <span data-ttu-id="68584-115">Wert</span><span class="sxs-lookup"><span data-stu-id="68584-115">Value</span></span>                                                                                                 | <span data-ttu-id="68584-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="68584-116">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="68584-117"><dt>remoteconfigtypemachine</dt></span><span class="sxs-lookup"><span data-stu-id="68584-117"><dt>remoteConfigTypeMachine</dt></span></span> </dl>    | <span data-ttu-id="68584-118">[**Invokeuiformachine**](inapcomponentconfig2-invokeuiformachine.md) ist implementiert.</span><span class="sxs-lookup"><span data-stu-id="68584-118">[**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) is implemented.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="68584-119"><dt>remoteconfigtypeconfigblob</dt></span><span class="sxs-lookup"><span data-stu-id="68584-119"><dt>remoteConfigTypeConfigBlob</dt></span></span> </dl> | <span data-ttu-id="68584-120">[**Invokeuifromconfigblob**](inapcomponentconfig2-invokeuifromconfigblob.md) ist implementiert.</span><span class="sxs-lookup"><span data-stu-id="68584-120">[**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) is implemented.</span></span> <span data-ttu-id="68584-121">[**Inapcomponentconfig:: GetConfig**](inapcomponentconfig-getconfig.md) und [**inapcomponentconfig:: setconfig**](inapcomponentconfig-setconfig.md) können mithilfe von DCOM Remote aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="68584-121">[**INapComponentConfig::GetConfig**](inapcomponentconfig-getconfig.md) and [**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md) can be called remotely using DCOM.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68584-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68584-122">Return value</span></span>

<span data-ttu-id="68584-123">Gibt \_ bei Erfolg S OK oder einen der standardmäßigen Windows-Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="68584-123">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="68584-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68584-124">Remarks</span></span>

<span data-ttu-id="68584-125">Wenn weder [**invokeuiformachine**](inapcomponentconfig2-invokeuiformachine.md) noch [**invokeuifromconfigblob**](inapcomponentconfig2-invokeuifromconfigblob.md) implementiert ist, ist die Remote Konfiguration des SHV nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="68584-125">If neither [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) nor [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) are implemented, remote configuration of the SHV is not possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="68584-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68584-126">Requirements</span></span>



| <span data-ttu-id="68584-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68584-127">Requirement</span></span> | <span data-ttu-id="68584-128">Wert</span><span class="sxs-lookup"><span data-stu-id="68584-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="68584-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="68584-129">Minimum supported client</span></span><br/> | <span data-ttu-id="68584-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="68584-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="68584-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="68584-131">Minimum supported server</span></span><br/> | <span data-ttu-id="68584-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="68584-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="68584-133">Header</span><span class="sxs-lookup"><span data-stu-id="68584-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="68584-134"><dt>Napcommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="68584-134"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="68584-135">IDL</span><span class="sxs-lookup"><span data-stu-id="68584-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="68584-136"><dt>Napcommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="68584-136"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68584-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68584-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68584-138">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="68584-138">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





