---
title: Inapsohconstructor Validate-Methode (napprotocol. h)
description: Überprüft die Gültigkeit des SoH-Pakets.
ms.assetid: 66338213-43c0-461a-a794-5f18d56bd505
keywords:
- Validate-Methode für NAP
- Validate-Methode, NAP, inapsohconstructor-Schnittstelle
- Inapsohconstructor-Schnittstelle NAP, Validate-Methode
topic_type:
- apiref
api_name:
- INapSoHConstructor.Validate
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7db8a52d7986348e85c724171b6d417996c7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742608"
---
# <a name="inapsohconstructorvalidate-method"></a><span data-ttu-id="ab16a-106">Inapsohconstructor:: Validate-Methode</span><span class="sxs-lookup"><span data-stu-id="ab16a-106">INapSoHConstructor::Validate method</span></span>

> [!Note]  
> <span data-ttu-id="ab16a-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ab16a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ab16a-108">Die **inapsohconstructor:: Validate** -Methode überprüft die Gültigkeit des SoH-Pakets.</span><span class="sxs-lookup"><span data-stu-id="ab16a-108">The **INapSoHConstructor::Validate** method checks the validity of the SoH packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab16a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab16a-109">Syntax</span></span>


```C++
HRESULT Validate(
  [in] const SoH  *soh,
  [in]       BOOL isRequest
);
```



## <a name="parameters"></a><span data-ttu-id="ab16a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab16a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab16a-111">*SoH* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab16a-111">*soh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab16a-112">Ein Zeiger auf das erstellte [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket.</span><span class="sxs-lookup"><span data-stu-id="ab16a-112">A pointer to the constructed [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="ab16a-113">*isrequest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab16a-113">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab16a-114">Ein **boolescher** Wert, der **true** ist, wenn das Paket ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) und **false** ist, wenn es sich um eine **sohresponse** handelt.</span><span class="sxs-lookup"><span data-stu-id="ab16a-114">A **BOOL** that is **TRUE** if the packet is an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is an **SoHResponse**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab16a-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ab16a-115">Return value</span></span>

<span data-ttu-id="ab16a-116">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ab16a-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="ab16a-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ab16a-117">Return code</span></span>                                                                                            | <span data-ttu-id="ab16a-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab16a-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="ab16a-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ab16a-119"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="ab16a-120">Das SoH-Paket ist gültig.</span><span class="sxs-lookup"><span data-stu-id="ab16a-120">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="ab16a-121"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="ab16a-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="ab16a-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="ab16a-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="ab16a-123"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="ab16a-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="ab16a-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ab16a-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ab16a-125"><dt>**\_ \_ Ungültiges NAP- \_ Paket**</dt></span><span class="sxs-lookup"><span data-stu-id="ab16a-125"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="ab16a-126">Das SoH-Paket ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="ab16a-126">The SoH packet is invalid.</span></span><br/>                              |



 

## <a name="requirements"></a><span data-ttu-id="ab16a-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab16a-127">Requirements</span></span>



| <span data-ttu-id="ab16a-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab16a-128">Requirement</span></span> | <span data-ttu-id="ab16a-129">Wert</span><span class="sxs-lookup"><span data-stu-id="ab16a-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab16a-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ab16a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ab16a-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab16a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ab16a-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ab16a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ab16a-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ab16a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ab16a-134">Header</span><span class="sxs-lookup"><span data-stu-id="ab16a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab16a-135"><dt>Napprotocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab16a-135"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="ab16a-136">IDL</span><span class="sxs-lookup"><span data-stu-id="ab16a-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ab16a-137"><dt>Napprotocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ab16a-137"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="ab16a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ab16a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab16a-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab16a-139"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="ab16a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab16a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab16a-141">**Inapsohconstructor**</span><span class="sxs-lookup"><span data-stu-id="ab16a-141">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





