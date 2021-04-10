---
title: INapClientManagement2 getsystemisolationinfoex-Methode (napmanagement. h)
description: Ruft Informationen zum Isolations Status und zum erweiterten Isolations Status des napclient ab.
ms.assetid: 614bcf19-873e-4043-98b2-dcb152bae3e2
keywords:
- Getsystemisolationinfoex-Methode NAP
- Getsystemisolationinfoex-Methode NAP, INapClientManagement2-Schnittstelle
- INapClientManagement2 Interface NAP, getsystemisolationinfoex-Methode
topic_type:
- apiref
api_name:
- INapClientManagement2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e75a6554ea7e55c3bebe35b797f888494a55627
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040406"
---
# <a name="inapclientmanagement2getsystemisolationinfoex-method"></a><span data-ttu-id="6b11d-106">INapClientManagement2:: getsystemisolationinfoex-Methode</span><span class="sxs-lookup"><span data-stu-id="6b11d-106">INapClientManagement2::GetSystemIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="6b11d-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6b11d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6b11d-108">Die **getsystemisolationinfoex** -Methode ruft Informationen über den Isolations Status und den erweiterten Isolations Status des napclient ab.</span><span class="sxs-lookup"><span data-stu-id="6b11d-108">The **GetSystemIsolationInfoEx** method retrieves information about the isolation state and extended isolation state of the NapClient.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b11d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b11d-109">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="6b11d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b11d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b11d-111">*IsolationInfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6b11d-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b11d-112">Ein Zeiger auf einen Zeiger auf eine [**isolationinfoex**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) -Struktur, die Isolations Zustandsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="6b11d-112">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains isolation state information.</span></span>

</dd> <dt>

<span data-ttu-id="6b11d-113">*unknownconnections* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6b11d-113">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b11d-114">Ein Zeiger auf einen booleschen Wert, der **true** ist, wenn sich eine der Verbindungen in einem unbekannten Zustand befindet, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="6b11d-114">A pointer to a BOOL that is **TRUE** if any of the connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b11d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b11d-115">Return value</span></span>

<span data-ttu-id="6b11d-116">Die-Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.</span><span class="sxs-lookup"><span data-stu-id="6b11d-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="6b11d-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6b11d-117">Return code</span></span>                                                                                         | <span data-ttu-id="6b11d-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b11d-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b11d-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6b11d-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="6b11d-120">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6b11d-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="6b11d-121"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="6b11d-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="6b11d-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="6b11d-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="6b11d-123"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="6b11d-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="6b11d-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6b11d-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="6b11d-125"><dt>**RPC- \_ E \_ getrennt**</dt></span><span class="sxs-lookup"><span data-stu-id="6b11d-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="6b11d-126">Der NAPAgent wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b11d-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="6b11d-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b11d-127">Remarks</span></span>

<span data-ttu-id="6b11d-128">Die abgerufenen Isolations Informationen spiegeln keine unbekannten Zustände wider.</span><span class="sxs-lookup"><span data-stu-id="6b11d-128">The isolation information that is retrieved does not reflect unknown states.</span></span>

<span data-ttu-id="6b11d-129">Der SHA muss die [**isolationinfoex**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) -Struktur durch Aufrufen von [**freeisolationinfoex**](freeisolationinfoex.md)freigeben.</span><span class="sxs-lookup"><span data-stu-id="6b11d-129">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b11d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b11d-130">Requirements</span></span>



| <span data-ttu-id="6b11d-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b11d-131">Requirement</span></span> | <span data-ttu-id="6b11d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="6b11d-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b11d-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b11d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6b11d-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b11d-134">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6b11d-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b11d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6b11d-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b11d-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6b11d-137">Header</span><span class="sxs-lookup"><span data-stu-id="6b11d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b11d-138"><dt>Napmanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b11d-138"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="6b11d-139">IDL</span><span class="sxs-lookup"><span data-stu-id="6b11d-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6b11d-140"><dt>Napmanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6b11d-140"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="6b11d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6b11d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b11d-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b11d-142"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="6b11d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b11d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b11d-144">**INapClientManagement2**</span><span class="sxs-lookup"><span data-stu-id="6b11d-144">**INapClientManagement2**</span></span>](inapclientmanagement2.md)
</dt> </dl>

 

 





