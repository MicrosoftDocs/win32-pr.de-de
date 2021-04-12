---
title: Inapsohconstructor-Initialisierungs Methode (napprotocol. h)
description: Initialisiert ein SoH-Protokoll Paket im NAP-System.
ms.assetid: 1678b677-c8c8-465c-a412-9b929e39bbac
keywords:
- Methode "NAP initialisieren"
- Initialize-Methode, NAP, inapsohconstructor-Schnittstelle
- Inapsohconstructor-Schnittstelle NAP, Initialize-Methode
topic_type:
- apiref
api_name:
- INapSoHConstructor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab8d6b27547be6e7c7e9abb59f7edb7b49e716e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949805"
---
# <a name="inapsohconstructorinitialize-method"></a><span data-ttu-id="efcdb-106">Inapsohconstructor:: Initialize-Methode</span><span class="sxs-lookup"><span data-stu-id="efcdb-106">INapSoHConstructor::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="efcdb-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="efcdb-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="efcdb-108">Die **inapsohconstructor:: Initialize** -Methode initialisiert ein SoH-Protokoll Paket im NAP-System.</span><span class="sxs-lookup"><span data-stu-id="efcdb-108">The **INapSoHConstructor::Initialize** method initializes a SoH protocol packet in the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="efcdb-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="efcdb-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId id,
  [in] BOOL                 isRequest
);
```



## <a name="parameters"></a><span data-ttu-id="efcdb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="efcdb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efcdb-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="efcdb-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efcdb-112">Eine eindeutige [systemhealthentityid](nap-datatypes.md) , die die ID des SHA-oder SHV-Pakets enthält, von dem das Paket erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="efcdb-112">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA or SHV that is constructing the packet.</span></span>

</dd> <dt>

<span data-ttu-id="efcdb-113">*isrequest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="efcdb-113">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efcdb-114">Ein **boolescher** Wert, der **true** ist, wenn das Paket ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) sein soll, und **false** , wenn es sich um einen **sohresponse**-Wert handeln soll.</span><span class="sxs-lookup"><span data-stu-id="efcdb-114">A **BOOL** that is **TRUE** if the packet is to be an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is to be an **SoHResponse**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efcdb-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="efcdb-115">Return value</span></span>

<span data-ttu-id="efcdb-116">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="efcdb-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="efcdb-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="efcdb-117">Return code</span></span>                                                                                     | <span data-ttu-id="efcdb-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="efcdb-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="efcdb-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="efcdb-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="efcdb-120">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="efcdb-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="efcdb-121"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="efcdb-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="efcdb-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="efcdb-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="efcdb-123"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="efcdb-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="efcdb-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="efcdb-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="efcdb-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="efcdb-125">Remarks</span></span>

<span data-ttu-id="efcdb-126">Diese Methode muss genau einmal pro Paket aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="efcdb-126">This method must be called exactly once per packet.</span></span>

<span data-ttu-id="efcdb-127">Die in *ID* angegebene [systemhealthentityid](nap-datatypes.md) ist der erste TLV im neu erstellten SoH-Paket und hat den Attributtyp [**sohattributetypesystemhealthid**](sohattributetype-enum.md).</span><span class="sxs-lookup"><span data-stu-id="efcdb-127">The [SystemHealthEntityId](nap-datatypes.md) specified in *id*, is the first TLV in the newly constructed SOH packet and has the attribute type [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="efcdb-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="efcdb-128">Requirements</span></span>



| <span data-ttu-id="efcdb-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="efcdb-129">Requirement</span></span> | <span data-ttu-id="efcdb-130">Wert</span><span class="sxs-lookup"><span data-stu-id="efcdb-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="efcdb-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="efcdb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="efcdb-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="efcdb-132">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="efcdb-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="efcdb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="efcdb-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="efcdb-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="efcdb-135">Header</span><span class="sxs-lookup"><span data-stu-id="efcdb-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="efcdb-136"><dt>Napprotocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="efcdb-136"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="efcdb-137">IDL</span><span class="sxs-lookup"><span data-stu-id="efcdb-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="efcdb-138"><dt>Napprotocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="efcdb-138"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="efcdb-139">DLL</span><span class="sxs-lookup"><span data-stu-id="efcdb-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efcdb-140"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efcdb-140"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="efcdb-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efcdb-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efcdb-142">**Inapsohconstructor**</span><span class="sxs-lookup"><span data-stu-id="efcdb-142">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





