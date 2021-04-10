---
title: Inapenforcementclientconnection getcorrelationid-Methode (napforcementclient. h)
description: Ruft die ID ab, die verwendet wird, um SoH-Anforderungen und SoH-Antworten zu korrelieren.
ms.assetid: f59880d4-5de6-4163-ae01-1095ff52bf38
keywords:
- Getcorrelationid-Methode NAP
- Getcorrelationid-Methode NAP, inapenforcementclientconnection-Schnittstelle
- Inapenforcementclientconnection-Schnittstelle NAP, getcorrelationid-Methode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82572cc499a61d453a70c47391e48f2004dca24d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104041003"
---
# <a name="inapenforcementclientconnectiongetcorrelationid-method"></a><span data-ttu-id="9f397-106">Inapenforcementclientconnection:: getcorrelationid-Methode</span><span class="sxs-lookup"><span data-stu-id="9f397-106">INapEnforcementClientConnection::GetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="9f397-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9f397-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9f397-108">Die **inapenforcementclientconnection:: getcorrelationid** -Methode ruft die ID ab, die verwendet wird, um SoH-Anforderungen und SoH-Antworten zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="9f397-108">The **INapEnforcementClientConnection::GetCorrelationId** method gets the ID used to correlate SoH-requests and SoH-responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f397-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f397-109">Syntax</span></span>


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="9f397-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f397-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f397-111">*correlationId* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9f397-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f397-112">Eine eindeutige [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) -Struktur, die diesen SoH-Austausch identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9f397-112">A unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure that identifies this SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f397-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f397-113">Return value</span></span>

<span data-ttu-id="9f397-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9f397-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="9f397-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9f397-115">Return code</span></span>                                                                                     | <span data-ttu-id="9f397-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f397-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9f397-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9f397-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="9f397-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9f397-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9f397-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="9f397-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="9f397-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="9f397-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="9f397-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="9f397-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="9f397-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9f397-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9f397-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f397-123">Remarks</span></span>

<span data-ttu-id="9f397-124">Die Korrelations-ID wird vom NAPAgent und auf der Grundlage der Verbindungs-ID festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9f397-124">The correlation-id is set by the NapAgent and based on the connection-id.</span></span>

<span data-ttu-id="9f397-125">Diese ID wird verwendet, um Anforderungen und Antworten zu korrelieren, d. h., Sie beschreibt einen SoH-Austausch eindeutig und enthält immer die ID des letzten SoH, die für das Verbindungs Objekt festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="9f397-125">This id is used to correlate requests and responses, i.e. it uniquely describes an SoH exchange and always contains the id of the most recent SoH set on the connection object.</span></span>

<span data-ttu-id="9f397-126">Wenn ein SoH-Response empfangen wird, stellt der NAPAgent zunächst sicher, dass die IDs Stimmen. Wenn dies nicht der Fall ist, wird ein Fehler zurückgegeben, und der Enforcer muss das Paket löschen.</span><span class="sxs-lookup"><span data-stu-id="9f397-126">When an SoH-Response is received, the NapAgent first ensures the IDs match; if not, an error is returned and the enforcer must drop the packet.</span></span> <span data-ttu-id="9f397-127">Weitere Informationen finden Sie unter [**inapenforcementclientbinding::P rocesssohresponse**](inapenforcementclientbinding-processsohresponse-method.md) .</span><span class="sxs-lookup"><span data-stu-id="9f397-127">See [**INapEnforcementClientBinding::ProcessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md) for more details.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f397-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f397-128">Requirements</span></span>



| <span data-ttu-id="9f397-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f397-129">Requirement</span></span> | <span data-ttu-id="9f397-130">Wert</span><span class="sxs-lookup"><span data-stu-id="9f397-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f397-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f397-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9f397-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f397-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9f397-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f397-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9f397-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9f397-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9f397-135">Header</span><span class="sxs-lookup"><span data-stu-id="9f397-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f397-136"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f397-136"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="9f397-137">IDL</span><span class="sxs-lookup"><span data-stu-id="9f397-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9f397-138"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f397-138"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="9f397-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9f397-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f397-140"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f397-140"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="9f397-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f397-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f397-142">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="9f397-142">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





