---
title: INapEnforcementClientConnection2 getisolationinfoex-Methode (natzforcementclient. h)
description: Wird verwendet, um Isolations Informationen über den Client zu erhalten.
ms.assetid: ebacd056-5ab8-4096-821c-8f2987d853c4
keywords:
- Getisolationinfoex-Methode NAP
- Getisolationinfoex-Methode NAP, INapEnforcementClientConnection2-Schnittstelle
- INapEnforcementClientConnection2 Interface NAP, getisolationinfoex-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6586dd5fc277e62d4478e685f49ac132e744bcc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479347"
---
# <a name="inapenforcementclientconnection2getisolationinfoex-method"></a><span data-ttu-id="6ca01-106">INapEnforcementClientConnection2:: getisolationinfoex-Methode</span><span class="sxs-lookup"><span data-stu-id="6ca01-106">INapEnforcementClientConnection2::GetIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="6ca01-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6ca01-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6ca01-108">Die **INapEnforcementClientConnection2:: getisolationinfoex** -Methode wird verwendet, um Isolations Informationen über den Client zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6ca01-108">The **INapEnforcementClientConnection2::GetIsolationInfoEx** method is used to get isolation information about the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ca01-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ca01-109">Syntax</span></span>


```C++
HRESULT GetIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo
) const;
```



## <a name="parameters"></a><span data-ttu-id="6ca01-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ca01-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ca01-111">*IsolationInfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6ca01-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ca01-112">Ein Zeiger auf einen Zeiger auf eine [**isolationinfoex**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) -Struktur, die die Konnektivität und die erweiterten Zustandsinformationen des Clients enthält.</span><span class="sxs-lookup"><span data-stu-id="6ca01-112">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the connectivity and extended state information of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ca01-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ca01-113">Return value</span></span>

<span data-ttu-id="6ca01-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6ca01-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="6ca01-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6ca01-115">Return code</span></span>                                                                                     | <span data-ttu-id="6ca01-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ca01-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="6ca01-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6ca01-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="6ca01-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6ca01-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6ca01-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="6ca01-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="6ca01-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="6ca01-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="6ca01-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="6ca01-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="6ca01-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6ca01-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6ca01-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ca01-123">Remarks</span></span>

<span data-ttu-id="6ca01-124">Diese Informationen werden von NAPAgent nach der Verarbeitung von [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh) festgelegt und dürfen nicht vom-Enforcer festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6ca01-124">This information is set by NapAgent after processing an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

<span data-ttu-id="6ca01-125">Der SHA muss die [**isolationinfoex**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) -Struktur durch Aufrufen von [**freeisolationinfoex**](freeisolationinfoex.md)freigeben.</span><span class="sxs-lookup"><span data-stu-id="6ca01-125">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ca01-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ca01-126">Requirements</span></span>



| <span data-ttu-id="6ca01-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ca01-127">Requirement</span></span> | <span data-ttu-id="6ca01-128">Wert</span><span class="sxs-lookup"><span data-stu-id="6ca01-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca01-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ca01-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6ca01-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ca01-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6ca01-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ca01-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6ca01-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ca01-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6ca01-133">Header</span><span class="sxs-lookup"><span data-stu-id="6ca01-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ca01-134"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ca01-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ca01-135">IDL</span><span class="sxs-lookup"><span data-stu-id="6ca01-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ca01-136"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ca01-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="6ca01-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6ca01-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ca01-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ca01-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="6ca01-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ca01-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ca01-140">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="6ca01-140">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





