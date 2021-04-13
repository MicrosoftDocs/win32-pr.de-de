---
title: Inapclientmanagement getnapclientinfo-Methode (napmanagement. h)
description: Ruft Informationen zum NAP-Client ab.
ms.assetid: c0b57cab-729b-40b2-81d2-32a961e377a5
keywords:
- Getnapclientinfo-Methode NAP
- Getnapclientinfo-Methode NAP, inapclientmanagement-Schnittstelle
- Inapclientmanagement Interface NAP, getnapclientinfo-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.GetNapClientInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11fc496374f2a7f0b7842e22212013149f44f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518245"
---
# <a name="inapclientmanagementgetnapclientinfo-method"></a><span data-ttu-id="e486e-106">Inapclientmanagement:: getnapclientinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="e486e-106">INapClientManagement::GetNapClientInfo method</span></span>

> [!Note]  
> <span data-ttu-id="e486e-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e486e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e486e-108">Die **getnapclientinfo** -Methode ruft Informationen zum NAP-Client ab.</span><span class="sxs-lookup"><span data-stu-id="e486e-108">The **GetNapClientInfo** method retrieves information about the NAP client.</span></span>

## <a name="syntax"></a><span data-ttu-id="e486e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e486e-109">Syntax</span></span>


```C++
HRESULT GetNapClientInfo(
  [out] BOOL          *isNapEnabled,
  [out] CountedString **clientName,
  [out] CountedString **clientDescription,
  [out] CountedString **protocolVersion
) const;
```



## <a name="parameters"></a><span data-ttu-id="e486e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e486e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e486e-111">*isnapabled* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e486e-111">*isNapEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e486e-112">Ein Zeiger auf einen booleschen Wert, der auf **true** festgelegt ist, wenn NAP aktiviert ist. Andernfalls wird Sie auf " **false**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e486e-112">A pointer to a BOOL that is set to **TRUE** if NAP is enabled; otherwise it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e486e-113">*Client Name* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e486e-113">*clientName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e486e-114">Ein Zeiger auf einen Zeiger auf eine [**zählstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur, die den Client Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="e486e-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the client name.</span></span>

</dd> <dt>

<span data-ttu-id="e486e-115">*clientdescription* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e486e-115">*clientDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e486e-116">Ein Zeiger auf einen Zeiger auf eine [**zählstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur, die die Client Beschreibung enthält.</span><span class="sxs-lookup"><span data-stu-id="e486e-116">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the client description.</span></span>

</dd> <dt>

<span data-ttu-id="e486e-117">*ProtocolVersion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e486e-117">*protocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e486e-118">Ein Zeiger auf einen Zeiger auf eine [**zählstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur, die die Protokollversion enthält.</span><span class="sxs-lookup"><span data-stu-id="e486e-118">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e486e-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e486e-119">Return value</span></span>

<span data-ttu-id="e486e-120">Die-Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.</span><span class="sxs-lookup"><span data-stu-id="e486e-120">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="e486e-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e486e-121">Return code</span></span>                                                                                         | <span data-ttu-id="e486e-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e486e-122">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e486e-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e486e-123"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="e486e-124">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e486e-124">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e486e-125"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="e486e-125"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="e486e-126">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="e486e-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="e486e-127"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="e486e-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="e486e-128">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e486e-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e486e-129"><dt>**RPC- \_ E \_ getrennt**</dt></span><span class="sxs-lookup"><span data-stu-id="e486e-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="e486e-130">Der NAPAgent wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e486e-130">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="e486e-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e486e-131">Requirements</span></span>



| <span data-ttu-id="e486e-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e486e-132">Requirement</span></span> | <span data-ttu-id="e486e-133">Wert</span><span class="sxs-lookup"><span data-stu-id="e486e-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e486e-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e486e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e486e-135">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e486e-135">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e486e-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e486e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e486e-137">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e486e-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e486e-138">Header</span><span class="sxs-lookup"><span data-stu-id="e486e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e486e-139"><dt>Napmanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="e486e-139"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="e486e-140">IDL</span><span class="sxs-lookup"><span data-stu-id="e486e-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e486e-141"><dt>Napmanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e486e-141"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="e486e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e486e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e486e-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e486e-143"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="e486e-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e486e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e486e-145">**Inapclientmanagement**</span><span class="sxs-lookup"><span data-stu-id="e486e-145">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





