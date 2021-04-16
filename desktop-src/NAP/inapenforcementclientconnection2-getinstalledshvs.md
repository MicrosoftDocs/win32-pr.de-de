---
title: INapEnforcementClientConnection2 getinstalledshvs-Methode (napforcementclient. h)
description: Wird vom NAP-Agent verwendet, um die installierten System Integritätsprüfungen (SHVs) auf dem Client abzufragen.
ms.assetid: b2e3ab29-90bf-4117-bc2e-2ff2827ee15c
keywords:
- Getinstalledshvs-Methode NAP
- Getinstalledshvs-Methode NAP, INapEnforcementClientConnection2-Schnittstelle
- INapEnforcementClientConnection2 Interface NAP, getinstalledshvs-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa54d09a0c3d3c524262231982f662c497920a0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479356"
---
# <a name="inapenforcementclientconnection2getinstalledshvs-method"></a><span data-ttu-id="2d433-106">INapEnforcementClientConnection2:: getinstalledshvs-Methode</span><span class="sxs-lookup"><span data-stu-id="2d433-106">INapEnforcementClientConnection2::GetInstalledShvs method</span></span>

> [!Note]  
> <span data-ttu-id="2d433-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2d433-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2d433-108">Die **getinstalledshvs** -Methode wird vom NAP-Agent verwendet, um die installierten System Integritätsprüfungen (SHVs) auf dem Client abzufragen.</span><span class="sxs-lookup"><span data-stu-id="2d433-108">The **GetInstalledShvs** method is used by the NAP Agent to query the installed System Health Validators (SHVs) on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d433-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d433-109">Syntax</span></span>


```C++
HRESULT GetInstalledShvs(
  [out] SystemHealthEntityCount *count,
  [out] SystemHealthEntityId    **ids
) const;
```



## <a name="parameters"></a><span data-ttu-id="2d433-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d433-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d433-111">*Anzahl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2d433-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d433-112">Ein Zeiger auf einen [systemhealthentitycount](nap-datatypes.md) -Wert, der die Anzahl der installierten SHVs in *IDs* angibt.</span><span class="sxs-lookup"><span data-stu-id="2d433-112">A pointer to a [SystemHealthEntityCount](nap-datatypes.md) value that specifies the number of installed SHVs in *ids*.</span></span>

</dd> <dt>

<span data-ttu-id="2d433-113">*IDs* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2d433-113">*ids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2d433-114">Ein Zeiger auf ein Array von [systemhealthentityid](nap-datatypes.md) -Werten, die die installierten SHV-IDs enthalten.</span><span class="sxs-lookup"><span data-stu-id="2d433-114">A pointer to an array of [SystemHealthEntityId](nap-datatypes.md) values that contain the installed SHV IDs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d433-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d433-115">Return value</span></span>

<span data-ttu-id="2d433-116">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2d433-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="2d433-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2d433-117">Return code</span></span>                                                                                   | <span data-ttu-id="2d433-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2d433-118">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="2d433-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2d433-119"><dt>**S\_OK** </dt></span></span> </dl>         | <span data-ttu-id="2d433-120">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2d433-120">Operation succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="2d433-121"><dt>**E \_ InvalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="2d433-121"><dt>**E\_INVALIDARG** </dt></span></span> </dl> | <span data-ttu-id="2d433-122">Ein ungültiges Argument wurde an die-Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="2d433-122">An invalid argument was passed to the method.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2d433-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d433-123">Requirements</span></span>



| <span data-ttu-id="2d433-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d433-124">Requirement</span></span> | <span data-ttu-id="2d433-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2d433-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d433-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d433-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2d433-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d433-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2d433-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d433-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2d433-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d433-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2d433-130">Header</span><span class="sxs-lookup"><span data-stu-id="2d433-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d433-131"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d433-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="2d433-132">IDL</span><span class="sxs-lookup"><span data-stu-id="2d433-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2d433-133"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2d433-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="2d433-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2d433-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d433-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d433-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="2d433-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d433-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d433-137">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="2d433-137">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





