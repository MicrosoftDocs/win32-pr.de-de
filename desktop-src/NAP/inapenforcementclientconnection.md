---
title: Inapenforcementclientconnection-Schnittstelle (napforcementclient. h)
description: Ermöglicht die clientverbindungsverwaltung. | Inapenforcementclientconnection-Schnittstelle (napforcementclient. h)
ms.assetid: 96b94995-24b8-47ed-880e-6182d1bfe925
keywords:
- Inapenforcementclientconnection-Schnittstelle NAP
- Inapenforcementclientconnection-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5f132da021e7970ec2f15a872091c101cd5c42
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219184"
---
# <a name="inapenforcementclientconnection-interface"></a><span data-ttu-id="1e168-106">Inapenforcementclientconnection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="1e168-106">INapEnforcementClientConnection interface</span></span>

> [!Note]  
> <span data-ttu-id="1e168-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1e168-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1e168-108">Die **inapenforcementclientconnection** stellt Methoden bereit, die die Client Verbindungs Verwaltung ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="1e168-108">The **INapEnforcementClientConnection** provides methods that allow for client connection management.</span></span>

> [!Note]  
> <span data-ttu-id="1e168-109">[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) erbt alle Methoden dieser Schnittstelle und sollte stattdessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e168-109">[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="1e168-110">Member</span><span class="sxs-lookup"><span data-stu-id="1e168-110">Members</span></span>

<span data-ttu-id="1e168-111">Die **inapenforcementclientconnection** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1e168-111">The **INapEnforcementClientConnection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1e168-112">**Inapenforcementclientconnection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1e168-112">**INapEnforcementClientConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="1e168-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="1e168-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1e168-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="1e168-114">Methods</span></span>

<span data-ttu-id="1e168-115">Die **inapenforcementclientconnection** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1e168-115">The **INapEnforcementClientConnection** interface has these methods.</span></span>



| <span data-ttu-id="1e168-116">Methode</span><span class="sxs-lookup"><span data-stu-id="1e168-116">Method</span></span>                                                                                                                           | <span data-ttu-id="1e168-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1e168-117">Description</span></span>                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1e168-118">**Inapenforcementclientconnection:: GetConnectionID**</span><span class="sxs-lookup"><span data-stu-id="1e168-118">**INapEnforcementClientConnection::GetConnectionId**</span></span>](inapenforcementclientconnection-getconnectionid-method.md)               | <span data-ttu-id="1e168-119">Ruft die Verbindungs-ID des Clients ab.</span><span class="sxs-lookup"><span data-stu-id="1e168-119">Gets the connection ID of the client.</span></span><br/>                                                                                          |
| [<span data-ttu-id="1e168-120">**Inapenforcementclientconnection:: getcorrelationid**</span><span class="sxs-lookup"><span data-stu-id="1e168-120">**INapEnforcementClientConnection::GetCorrelationId**</span></span>](inapenforcementclientconnection-getcorrelationid-method.md)             | <span data-ttu-id="1e168-121">Ruft die ID ab, die verwendet wird, um SoH-Anforderungen und SoH-Antworten zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="1e168-121">Gets the ID used to correlate SoH-requests and SoH-responses.</span></span><br/>                                                                  |
| [<span data-ttu-id="1e168-122">**Inapenforcementclientconnection:: getenforcerprivatedata**</span><span class="sxs-lookup"><span data-stu-id="1e168-122">**INapEnforcementClientConnection::GetEnforcerPrivateData**</span></span>](inapenforcementclientconnection-getenforcerprivatedata-method.md) | <span data-ttu-id="1e168-123">Wird vom-Enforcer verwendet, um private Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1e168-123">Used by the enforcer to get private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="1e168-124">**Inapenforcementclientconnection:: GetFlags**</span><span class="sxs-lookup"><span data-stu-id="1e168-124">**INapEnforcementClientConnection::GetFlags**</span></span>](inapenforcementclientconnection-getflags-method.md)                             | <span data-ttu-id="1e168-125">Ruft den Wert des Flags ab, das erstmalige Antworten von Antworten aufgrund von sohrequests unterscheidet, die von den-enforcern zwischengespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="1e168-125">Gets the value of the flag that differentiates first-time responses from responses due to SoHRequests cached by the enforcers.</span></span><br/> |
| [<span data-ttu-id="1e168-126">**Inapenforcementclientconnection:: getisolationinfo**</span><span class="sxs-lookup"><span data-stu-id="1e168-126">**INapEnforcementClientConnection::GetIsolationInfo**</span></span>](inapenforcementclientconnection-getisolationinfo-method.md)             | <span data-ttu-id="1e168-127">Wird verwendet, um die Isolations Informationen des Clients zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1e168-127">Used get the isolation information of the client.</span></span><br/>                                                                              |
| [<span data-ttu-id="1e168-128">**Inapenforcementclientconnection:: getmaxsize**</span><span class="sxs-lookup"><span data-stu-id="1e168-128">**INapEnforcementClientConnection::GetMaxSize**</span></span>](inapenforcementclientconnection-getmaxsize-method.md)                         | <span data-ttu-id="1e168-129">Ruft die maximale Größe des SoH-Pakets für diesen Client ab.</span><span class="sxs-lookup"><span data-stu-id="1e168-129">Gets the maximum size of the SoH packet for this client.</span></span><br/>                                                                       |
| [<span data-ttu-id="1e168-130">**Inapenforcementclientconnection:: getprivatedata**</span><span class="sxs-lookup"><span data-stu-id="1e168-130">**INapEnforcementClientConnection::GetPrivateData**</span></span>](inapenforcementclientconnection-getprivatedata-method.md)                 | <span data-ttu-id="1e168-131">Wird vom NAPAgent verwendet, um private Daten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1e168-131">Used by the NapAgent to get private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="1e168-132">**Inapenforcementclientconnection:: getsohrequest**</span><span class="sxs-lookup"><span data-stu-id="1e168-132">**INapEnforcementClientConnection::GetSoHRequest**</span></span>](inapenforcementclientconnection-getsohrequest-method.md)                   | <span data-ttu-id="1e168-133">Ruft die SoH-Anforderung ab.</span><span class="sxs-lookup"><span data-stu-id="1e168-133">Gets the SoH Request.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="1e168-134">**Inapenforcementclientconnection:: getsohresponse**</span><span class="sxs-lookup"><span data-stu-id="1e168-134">**INapEnforcementClientConnection::GetSoHResponse**</span></span>](inapenforcementclientconnection-getsohresponse-method.md)                 | <span data-ttu-id="1e168-135">Ruft den SoH-Response ab, der vom Erzwingungs Client empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="1e168-135">Gets the SoH-Response received by the enforcement client.</span></span><br/>                                                                      |
| [<span data-ttu-id="1e168-136">**Inapenforcementclientconnection:: getstringcorrelationid**</span><span class="sxs-lookup"><span data-stu-id="1e168-136">**INapEnforcementClientConnection::GetStringCorrelationId**</span></span>](inapenforcementclientconnection-getstringcorrelationid-method.md) | <span data-ttu-id="1e168-137">Ruft die Zeichen folgen Version von CorrelationId ab.</span><span class="sxs-lookup"><span data-stu-id="1e168-137">Gets the string version of the CorrelationId.</span></span> <span data-ttu-id="1e168-138">Wird hauptsächlich für Protokollierungs Zwecke verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e168-138">Used primarily for logging purposes.</span></span><br/>                                             |
| [<span data-ttu-id="1e168-139">**Inapenforcementclientconnection:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="1e168-139">**INapEnforcementClientConnection::Initialize**</span></span>](inapenforcementclientconnection-initialize-method.md)                         | <span data-ttu-id="1e168-140">Initialisiert die Verbindung</span><span class="sxs-lookup"><span data-stu-id="1e168-140">Initializes the connection.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="1e168-141">**Inapenforcementclientconnection:: setconnectionid**</span><span class="sxs-lookup"><span data-stu-id="1e168-141">**INapEnforcementClientConnection::SetConnectionId**</span></span>](inapenforcementclientconnection-setconnectionid-method.md)               | <span data-ttu-id="1e168-142">Legt die Verbindungs-ID des Clients fest.</span><span class="sxs-lookup"><span data-stu-id="1e168-142">Sets the connection ID of the client.</span></span><br/>                                                                                          |
| [<span data-ttu-id="1e168-143">**Inapenforcementclientconnection:: setcorrelationid**</span><span class="sxs-lookup"><span data-stu-id="1e168-143">**INapEnforcementClientConnection::SetCorrelationId**</span></span>](inapenforcementclientconnection-setcorrelationid-method.md)             | <span data-ttu-id="1e168-144">Legt die ID fest, die verwendet wird, um SoH-Anforderungen und SoH-Antworten zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="1e168-144">Sets the ID used to correlate SoH-requests and SoH-responses.</span></span><br/>                                                                  |
| [<span data-ttu-id="1e168-145">**Inapenforcementclientconnection:: Setup Data**</span><span class="sxs-lookup"><span data-stu-id="1e168-145">**INapEnforcementClientConnection::SetEnforcerPrivateData**</span></span>](inapenforcementclientconnection-setenforcerprivatedata-method.md) | <span data-ttu-id="1e168-146">Wird vom-Enforcer verwendet, um private Daten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1e168-146">Used by the enforcer to set private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="1e168-147">**Inapenforcementclientconnection:: setFlags**</span><span class="sxs-lookup"><span data-stu-id="1e168-147">**INapEnforcementClientConnection::SetFlags**</span></span>](inapenforcementclientconnection-setflags-method.md)                             | <span data-ttu-id="1e168-148">Legt das Flag fest, das erstmalige Antworten von Antworten aufgrund von sohrequests unterscheidet, die von enforcern zwischengespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="1e168-148">Sets the flag that differentiates first-time responses from responses due to SoHRequests cached by enforcers.</span></span><br/>                  |
| [<span data-ttu-id="1e168-149">**Inapenforcementclientconnection:: Setup Info**</span><span class="sxs-lookup"><span data-stu-id="1e168-149">**INapEnforcementClientConnection::SetIsolationInfo**</span></span>](inapenforcementclientconnection-setisolationinfo-method.md)             | <span data-ttu-id="1e168-150">Wird von NAPAgent zum Festlegen der Isolations Informationen des Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e168-150">Used by the NapAgent to set the isolation information of the client.</span></span><br/>                                                           |
| [<span data-ttu-id="1e168-151">**Inapenforcementclientconnection:: setmaxsize**</span><span class="sxs-lookup"><span data-stu-id="1e168-151">**INapEnforcementClientConnection::SetMaxSize**</span></span>](inapenforcementclientconnection-setmaxsize-method.md)                         | <span data-ttu-id="1e168-152">Legt die maximale Größe des SoH-Pakets für diesen Client fest.</span><span class="sxs-lookup"><span data-stu-id="1e168-152">Sets the maximum size of the SoH packet for this client.</span></span><br/>                                                                       |
| [<span data-ttu-id="1e168-153">**Inapenforcementclientconnection:: setprivatedata**</span><span class="sxs-lookup"><span data-stu-id="1e168-153">**INapEnforcementClientConnection::SetPrivateData**</span></span>](inapenforcementclientconnection-setprivatedata-method.md)                 | <span data-ttu-id="1e168-154">Wird vom NAPAgent verwendet, um private Daten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1e168-154">Used by the NapAgent to set private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="1e168-155">**Inapenforcementclientconnection:: setsohrequest**</span><span class="sxs-lookup"><span data-stu-id="1e168-155">**INapEnforcementClientConnection::SetSoHRequest**</span></span>](inapenforcementclientconnection-setsohrequest-method.md)                   | <span data-ttu-id="1e168-156">Legt die SoH-Anforderung fest.</span><span class="sxs-lookup"><span data-stu-id="1e168-156">Sets the SoH Request.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="1e168-157">**Inapenforcementclientconnection:: setsohresponse**</span><span class="sxs-lookup"><span data-stu-id="1e168-157">**INapEnforcementClientConnection::SetSoHResponse**</span></span>](inapenforcementclientconnection-setsohresponse-method.md)                 | <span data-ttu-id="1e168-158">Legt den SoH-Response fest und wird vom Erzwingungs Client beim Empfang eines Pakets verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e168-158">Sets the SoH-Response and is used by the enforcement client on receiving a packet.</span></span><br/>                                             |



 

## <a name="requirements"></a><span data-ttu-id="1e168-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e168-159">Requirements</span></span>



| <span data-ttu-id="1e168-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e168-160">Requirement</span></span> | <span data-ttu-id="1e168-161">Wert</span><span class="sxs-lookup"><span data-stu-id="1e168-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e168-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e168-162">Minimum supported client</span></span><br/> | <span data-ttu-id="1e168-163">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e168-163">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1e168-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e168-164">Minimum supported server</span></span><br/> | <span data-ttu-id="1e168-165">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e168-165">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1e168-166">Header</span><span class="sxs-lookup"><span data-stu-id="1e168-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e168-167"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e168-167"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="1e168-168">IDL</span><span class="sxs-lookup"><span data-stu-id="1e168-168">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1e168-169"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1e168-169"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="1e168-170">DLL</span><span class="sxs-lookup"><span data-stu-id="1e168-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e168-171"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e168-171"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="1e168-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e168-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e168-173">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="1e168-173">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="1e168-174">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="1e168-174">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

