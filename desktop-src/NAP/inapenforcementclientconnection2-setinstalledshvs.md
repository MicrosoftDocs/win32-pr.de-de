---
title: INapEnforcementClientConnection2 setinstalledshvs-Methode (napforcementclient. h)
description: Wird vom NAP-Agent verwendet, um die installierten System Integritätsprüfungen (SHVs) auf dem Client festzulegen.
ms.assetid: 38aa99b9-a15a-414d-91fc-128de8f5a654
keywords:
- Setinstalledshvs-Methode NAP
- Setinstalledshvs-Methode NAP, INapEnforcementClientConnection2-Schnittstelle
- INapEnforcementClientConnection2 Interface NAP, setinstalledshvs-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6651cd5248094f82d9faa1862492f82648e94125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106514"
---
# <a name="inapenforcementclientconnection2setinstalledshvs-method"></a><span data-ttu-id="0f000-106">INapEnforcementClientConnection2:: setinstalledshvs-Methode</span><span class="sxs-lookup"><span data-stu-id="0f000-106">INapEnforcementClientConnection2::SetInstalledShvs method</span></span>

> [!Note]  
> <span data-ttu-id="0f000-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0f000-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0f000-108">Die **setinstalledshvs** -Methode wird vom NAP-Agent verwendet, um die installierten System Integritätsprüfungen (SHVs) auf dem Client festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0f000-108">The **SetInstalledShvs** method is used by the NAP Agent to set the installed System Health Validators (SHVs) on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f000-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f000-109">Syntax</span></span>


```C++
HRESULT SetInstalledShvs(
  [in] SystemHealthEntityCount count,
  [in] SystemHealthEntityId    *ids
);
```



## <a name="parameters"></a><span data-ttu-id="0f000-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f000-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f000-111">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f000-111">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f000-112">Ein [systemhealthentitycount](nap-datatypes.md) -Wert, der die Anzahl der SHVs angibt, die in *IDs* installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0f000-112">A [SystemHealthEntityCount](nap-datatypes.md) value that specifies the number of SHVs to install in *ids*.</span></span>

</dd> <dt>

<span data-ttu-id="0f000-113">*IDs* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f000-113">*ids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f000-114">Ein Zeiger auf einen [systemhealthentityid](nap-datatypes.md) -Wert, der eine Liste der zu installierenden SHV-IDs enthält.</span><span class="sxs-lookup"><span data-stu-id="0f000-114">A pointer to a [SystemHealthEntityId](nap-datatypes.md) value that contains a list of SHV IDs to install.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f000-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f000-115">Return value</span></span>

<span data-ttu-id="0f000-116">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0f000-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="0f000-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0f000-117">Return code</span></span>                                                                                  | <span data-ttu-id="0f000-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f000-118">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="0f000-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0f000-119"><dt>**S\_OK** </dt></span></span> </dl>        | <span data-ttu-id="0f000-120">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0f000-120">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="0f000-121"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="0f000-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0f000-122">Der *count* -Parameter war 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0f000-122">The *count* parameter was 0 (zero).</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0f000-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f000-123">Requirements</span></span>



| <span data-ttu-id="0f000-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f000-124">Requirement</span></span> | <span data-ttu-id="0f000-125">Wert</span><span class="sxs-lookup"><span data-stu-id="0f000-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f000-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0f000-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0f000-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f000-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="0f000-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0f000-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0f000-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0f000-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="0f000-130">Header</span><span class="sxs-lookup"><span data-stu-id="0f000-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f000-131"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f000-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f000-132">IDL</span><span class="sxs-lookup"><span data-stu-id="0f000-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f000-133"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f000-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="0f000-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0f000-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f000-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f000-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="0f000-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f000-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f000-137">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="0f000-137">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





