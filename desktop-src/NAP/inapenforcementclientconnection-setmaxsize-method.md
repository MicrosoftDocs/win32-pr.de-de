---
title: Inapenforcementclientconnection setmaxsize-Methode (napforcementclient. h)
description: Legt die maximale Größe des SoH-Pakets für diesen Client fest.
ms.assetid: 30d3747d-bcf8-41b3-b0af-29f20d48417b
keywords:
- Setmaxsize-Methode NAP
- Setmaxsize-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, setmaxsize-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b10d7bc1a023371683f17bb3e6e12cd578fa964
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391776"
---
# <a name="inapenforcementclientconnectionsetmaxsize-method"></a><span data-ttu-id="db6e7-106">Inapenforcementclientconnection:: setmaxsize-Methode</span><span class="sxs-lookup"><span data-stu-id="db6e7-106">INapEnforcementClientConnection::SetMaxSize method</span></span>

> [!Note]  
> <span data-ttu-id="db6e7-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="db6e7-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="db6e7-108">Mit der **inapenforcementclientconnection:: setmaxsize** -Methode wird die maximale Größe des SoH-Pakets für diesen Client festgelegt.</span><span class="sxs-lookup"><span data-stu-id="db6e7-108">The **INapEnforcementClientConnection::SetMaxSize** method sets the maximum size of the SoH packet for this client.</span></span>

## <a name="syntax"></a><span data-ttu-id="db6e7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="db6e7-109">Syntax</span></span>


```C++
HRESULT SetMaxSize(
  [in] ProtocolMaxSize maxSize
);
```



## <a name="parameters"></a><span data-ttu-id="db6e7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="db6e7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db6e7-111">*MaxSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db6e7-111">*maxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db6e7-112">Eine [**protocolmaxsize**](nap-datatypes.md) -Struktur, die die maximale Größe des SoH-Pakets in Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="db6e7-112">A [**ProtocolMaxSize**](nap-datatypes.md) structure that indicates the maximum size, in bytes, of the SoH packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db6e7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db6e7-113">Return value</span></span>

<span data-ttu-id="db6e7-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="db6e7-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="db6e7-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="db6e7-115">Return code</span></span>                                                                                     | <span data-ttu-id="db6e7-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="db6e7-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="db6e7-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="db6e7-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="db6e7-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="db6e7-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="db6e7-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="db6e7-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="db6e7-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="db6e7-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="db6e7-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="db6e7-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="db6e7-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="db6e7-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db6e7-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db6e7-123">Remarks</span></span>

<span data-ttu-id="db6e7-124">Dieser Wert wird durch den Erzwingungs Client festgelegt.</span><span class="sxs-lookup"><span data-stu-id="db6e7-124">This value is set by the enforcement client.</span></span>

## <a name="requirements"></a><span data-ttu-id="db6e7-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db6e7-125">Requirements</span></span>



| <span data-ttu-id="db6e7-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db6e7-126">Requirement</span></span> | <span data-ttu-id="db6e7-127">Wert</span><span class="sxs-lookup"><span data-stu-id="db6e7-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db6e7-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db6e7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="db6e7-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db6e7-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="db6e7-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db6e7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="db6e7-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db6e7-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="db6e7-132">Header</span><span class="sxs-lookup"><span data-stu-id="db6e7-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="db6e7-133"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="db6e7-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="db6e7-134">IDL</span><span class="sxs-lookup"><span data-stu-id="db6e7-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="db6e7-135"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="db6e7-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="db6e7-136">DLL</span><span class="sxs-lookup"><span data-stu-id="db6e7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db6e7-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db6e7-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="db6e7-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db6e7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db6e7-139">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="db6e7-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





