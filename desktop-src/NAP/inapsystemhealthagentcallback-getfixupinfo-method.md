---
title: Inapsystemhealthagentcallback getfixupinfo-Methode (napsystemhealthagent. h)
description: Wird von NAPAgent aufgerufen, um den Zustand des Systemintegritäts-Agents zu ermitteln, während er eine sohresponse verarbeitet.
ms.assetid: cf919b56-3d40-4c49-9c91-25c20ae5ccda
keywords:
- Getfixupinfo-Methode NAP
- Getfixupinfo-Methode NAP, inapsystemhealthagentcallback-Schnittstelle
- Inapsystemhealthagentcallback-Schnittstelle NAP, getfixupinfo-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.GetFixupInfo
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227cbe870c722189c995bff0c967eb187548cd1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104139"
---
# <a name="inapsystemhealthagentcallbackgetfixupinfo-method"></a><span data-ttu-id="fb9e3-106">Inapsystemhealthagentcallback:: getfixupinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="fb9e3-106">INapSystemHealthAgentCallback::GetFixupInfo method</span></span>

> [!Note]  
> <span data-ttu-id="fb9e3-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fb9e3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fb9e3-108">Die **inapsystemhealthagentcallback:: getfixupinfo** -Methode wird vom NAPAgent aufgerufen, um den Status des Systemintegritäts-Agents zu ermitteln, während er eine [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-soh)verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="fb9e3-108">The **INapSystemHealthAgentCallback::GetFixupInfo** method is called by the NapAgent to determine the state of the system health agent, while it is processing a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb9e3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb9e3-109">Syntax</span></span>


```C++
HRESULT GetFixupInfo(
  [out] FixupInfo **info
);
```



## <a name="parameters"></a><span data-ttu-id="fb9e3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb9e3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb9e3-111">*Info* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fb9e3-111">*info* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb9e3-112">Ein Zeiger auf einen Zeiger auf eine [**fixupinfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) -Struktur, die den Korrektur Status des Agents enthält.</span><span class="sxs-lookup"><span data-stu-id="fb9e3-112">A pointer to a pointer to a [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) structure that contains the fix-up status of the agent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb9e3-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb9e3-113">Return value</span></span>

<span data-ttu-id="fb9e3-114">Diese Methode kann einen dieser Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fb9e3-114">This method can return one of these values.</span></span>



| <span data-ttu-id="fb9e3-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="fb9e3-115">Return code</span></span>                                                                          | <span data-ttu-id="fb9e3-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb9e3-116">Description</span></span>                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <span data-ttu-id="fb9e3-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fb9e3-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fb9e3-118">Gibt die erfolgreiche Ausführung an.</span><span class="sxs-lookup"><span data-stu-id="fb9e3-118">Indicates success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fb9e3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fb9e3-119">Remarks</span></span>

<span data-ttu-id="fb9e3-120">Diese Rückruf Methode wird vom NAP-System deklariert und muss vom SHA-Writer implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="fb9e3-120">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="fb9e3-121">Der Systemintegritäts-Agent muss " **S \_ OK** " sofort ohne Blockierung zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="fb9e3-121">The system health agent must return **S\_OK** immediately without blocking.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb9e3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb9e3-122">Requirements</span></span>



| <span data-ttu-id="fb9e3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb9e3-123">Requirement</span></span> | <span data-ttu-id="fb9e3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="fb9e3-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9e3-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb9e3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fb9e3-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb9e3-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fb9e3-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb9e3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fb9e3-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fb9e3-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fb9e3-129">Header</span><span class="sxs-lookup"><span data-stu-id="fb9e3-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb9e3-130"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb9e3-130"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb9e3-131">IDL</span><span class="sxs-lookup"><span data-stu-id="fb9e3-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb9e3-132"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb9e3-132"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb9e3-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb9e3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb9e3-134">**Inapsystemhealthagentcallback**</span><span class="sxs-lookup"><span data-stu-id="fb9e3-134">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





