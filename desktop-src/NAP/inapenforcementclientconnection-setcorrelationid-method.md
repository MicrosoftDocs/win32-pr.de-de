---
title: Inapenforcementclientconnection setcorrelationid-Methode (napforcementclient. h)
description: Legt die ID fest, die verwendet wird, um SoH-Anforderungen und SoH-Antworten zu korrelieren.
ms.assetid: 8f9d5bde-95b1-4566-84ee-31c6ed5e8986
keywords:
- Setcorrelationid-Methode NAP
- Setcorrelationid-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, setcorrelationid-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c99576b8302f7fcf949f132cf110a5ac5f675ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517576"
---
# <a name="inapenforcementclientconnectionsetcorrelationid-method"></a><span data-ttu-id="868d0-106">Inapenforcementclientconnection:: setcorrelationid-Methode</span><span class="sxs-lookup"><span data-stu-id="868d0-106">INapEnforcementClientConnection::SetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="868d0-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="868d0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="868d0-108">Die **inapenforcementclientconnection:: setcorrelationid** -Methode legt die ID fest, die verwendet wird, um SoH-Requests und SoH-Antworten zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="868d0-108">The **INapEnforcementClientConnection::SetCorrelationId** method sets the ID used to correlate SoH-requests and SoH-responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="868d0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="868d0-109">Syntax</span></span>


```C++
HRESULT SetCorrelationId(
  [in] CorrelationId correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="868d0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="868d0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="868d0-111">*correlationId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="868d0-111">*correlationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="868d0-112">Eine eindeutige [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) -Struktur, die einen bestimmten SoH-Austausch identifiziert.</span><span class="sxs-lookup"><span data-stu-id="868d0-112">A unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure that identifies a specific SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="868d0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="868d0-113">Return value</span></span>

<span data-ttu-id="868d0-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="868d0-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="868d0-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="868d0-115">Return code</span></span>                                                                                     | <span data-ttu-id="868d0-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="868d0-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="868d0-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="868d0-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="868d0-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="868d0-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="868d0-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="868d0-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="868d0-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="868d0-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="868d0-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="868d0-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="868d0-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="868d0-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="868d0-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="868d0-123">Remarks</span></span>

<span data-ttu-id="868d0-124">Die Korrelations-ID wird vom NAPAgent und auf der Grundlage der Verbindungs-ID festgelegt.</span><span class="sxs-lookup"><span data-stu-id="868d0-124">The correlation-id is set by the NapAgent and based on the connection-id.</span></span>

<span data-ttu-id="868d0-125">Diese ID wird verwendet, um Anforderungen und Antworten zu korrelieren, d. h., Sie beschreibt einen SoH-Austausch eindeutig und enthält immer die ID des letzten SoH, die für das Verbindungs Objekt festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="868d0-125">This id is used to correlate requests and responses, i.e. it uniquely describes an SoH exchange and always contains the id of the most recent SoH set on the connection object.</span></span>

<span data-ttu-id="868d0-126">Wenn ein SoH-Response empfangen wird, stellt der NAPAgent zunächst sicher, dass die IDs Stimmen. Wenn dies nicht der Fall ist, wird ein Fehler zurückgegeben, und der Enforcer muss das Paket löschen.</span><span class="sxs-lookup"><span data-stu-id="868d0-126">When an SoH-Response is received, the NapAgent first ensures the IDs match; if not, an error is returned and the enforcer must drop the packet.</span></span> <span data-ttu-id="868d0-127">Weitere Informationen finden Sie unter [**inapenforcementclientbinding::P rocesssohresponse**](inapenforcementclientbinding-processsohresponse-method.md) .</span><span class="sxs-lookup"><span data-stu-id="868d0-127">See [**INapEnforcementClientBinding::ProcessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md) for more details.</span></span>

## <a name="requirements"></a><span data-ttu-id="868d0-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="868d0-128">Requirements</span></span>



| <span data-ttu-id="868d0-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="868d0-129">Requirement</span></span> | <span data-ttu-id="868d0-130">Wert</span><span class="sxs-lookup"><span data-stu-id="868d0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="868d0-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="868d0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="868d0-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="868d0-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="868d0-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="868d0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="868d0-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="868d0-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="868d0-135">Header</span><span class="sxs-lookup"><span data-stu-id="868d0-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="868d0-136"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="868d0-136"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="868d0-137">IDL</span><span class="sxs-lookup"><span data-stu-id="868d0-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="868d0-138"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="868d0-138"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="868d0-139">DLL</span><span class="sxs-lookup"><span data-stu-id="868d0-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="868d0-140"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="868d0-140"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="868d0-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="868d0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="868d0-142">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="868d0-142">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





