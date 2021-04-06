---
title: Inapenforcementclientbinding-Schnittstelle (napforcementclient. h)
description: Erzwingungs Clients verwenden, um mit dem NAPAgent zu kommunizieren.
ms.assetid: 73c5c9ad-f213-4d34-9262-996acb570a55
keywords:
- Inapenforcementclientbinding-Schnittstelle NAP
- Inapenforcementclientbinding-Schnittstelle NAP, beschrieben
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23db912c08e68adb1411527c90580a5620601752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859286"
---
# <a name="inapenforcementclientbinding-interface"></a><span data-ttu-id="05a06-105">Inapenforcementclientbinding-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="05a06-105">INapEnforcementClientBinding interface</span></span>

> [!Note]  
> <span data-ttu-id="05a06-106">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="05a06-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="05a06-107">**Inapenforcementclientbinding** stellt Methoden bereit, die von Erzwingungs Clients für die Kommunikation mit dem NAPAgent verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="05a06-107">The **INapEnforcementClientBinding** provides methods that enforcement clients use to communicate with the NapAgent.</span></span>

## <a name="members"></a><span data-ttu-id="05a06-108">Member</span><span class="sxs-lookup"><span data-stu-id="05a06-108">Members</span></span>

<span data-ttu-id="05a06-109">Die **inapenforcementclientbinding** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="05a06-109">The **INapEnforcementClientBinding** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="05a06-110">**Inapenforcementclientbinding** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="05a06-110">**INapEnforcementClientBinding** also has these types of members:</span></span>

-   [<span data-ttu-id="05a06-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="05a06-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="05a06-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="05a06-112">Methods</span></span>

<span data-ttu-id="05a06-113">Die **inapenforcementclientbinding** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="05a06-113">The **INapEnforcementClientBinding** interface has these methods.</span></span>



| <span data-ttu-id="05a06-114">Methode</span><span class="sxs-lookup"><span data-stu-id="05a06-114">Method</span></span>                                                                                                                           | <span data-ttu-id="05a06-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05a06-115">Description</span></span>                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05a06-116">**Inapenforcementclientbinding:: kreateconnetction**</span><span class="sxs-lookup"><span data-stu-id="05a06-116">**INapEnforcementClientBinding::CreateConnection**</span></span>](inapenforcementclientbinding-createconnection-method.md)                   | <span data-ttu-id="05a06-117">Wird von enforcern zum Erstellen von Verbindungs Objekten verwendet.</span><span class="sxs-lookup"><span data-stu-id="05a06-117">Used by enforcers to create connection objects.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="05a06-118">**Inapenforcementclientbinding:: getsohrequest**</span><span class="sxs-lookup"><span data-stu-id="05a06-118">**INapEnforcementClientBinding::GetSoHRequest**</span></span>](inapenforcementclientbinding-getsohrequest-method.md)                         | <span data-ttu-id="05a06-119">Wird vom Erzwingungs Client verwendet, wenn er eine SoH-Anforderung für eine bestimmte Verbindung benötigt.</span><span class="sxs-lookup"><span data-stu-id="05a06-119">Used by the enforcement client when it needs an SoH-request for a particular connection.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="05a06-120">**Inapenforcementclientbinding:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="05a06-120">**INapEnforcementClientBinding::Initialize**</span></span>](inapenforcementclientbinding-initialize-method.md)                               | <span data-ttu-id="05a06-121">Startet den NAPAgent-Dienst.</span><span class="sxs-lookup"><span data-stu-id="05a06-121">Starts up the NapAgent service.</span></span> <span data-ttu-id="05a06-122">Der Erzwingungs Client muss diese Methode aufrufen, bevor eine andere Methode dieser Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="05a06-122">The enforcement client must call this method before calling any other method of this interface.</span></span><br/>                                                                            |
| [<span data-ttu-id="05a06-123">**Inapenforcementclientbinding:: notifyconnectionstatedown**</span><span class="sxs-lookup"><span data-stu-id="05a06-123">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span></span>](inapenforcementclientbinding-notifyconnectionstatedown-method.md) | <span data-ttu-id="05a06-124">Wird verwendet, um den NAPAgent darüber zu informieren, dass eine Verbindung zu einem Erzwingungs Client nicht mehr besteht.</span><span class="sxs-lookup"><span data-stu-id="05a06-124">Used to inform the NapAgent that a connection to an enforcement client has gone down.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="05a06-125">**Inapenforcementclientbinding:: notifysohchangefailure**</span><span class="sxs-lookup"><span data-stu-id="05a06-125">**INapEnforcementClientBinding::NotifySoHChangeFailure**</span></span>](inapenforcementclientbinding-notifysohchangefailure-method.md)       | <span data-ttu-id="05a06-126">Wird vom Erzwingungs Client verwendet, um den NAPAgent darüber zu informieren, dass ein vorheriger [**inapenforcementclientcallback:: notifysohchange**](inapenforcementclientcallback-notifysohchange-method.md)nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="05a06-126">Used by the enforcement client to inform the NapAgent that it could not process a previous [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).</span></span><br/> |
| [<span data-ttu-id="05a06-127">**Inapenforcementclientbinding::P rocesssohresponse**</span><span class="sxs-lookup"><span data-stu-id="05a06-127">**INapEnforcementClientBinding::ProcessSoHResponse**</span></span>](inapenforcementclientbinding-processsohresponse-method.md)               | <span data-ttu-id="05a06-128">Wird von Erzwingungs Clients immer dann verwendet, wenn Sie ein SoH-Response Data BLOB vom Erzwingungs Server erhalten.</span><span class="sxs-lookup"><span data-stu-id="05a06-128">Used by enforcement clients whenever they get an SoH-Response data blob from the enforcement server.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="05a06-129">**Inapenforcementclientbinding:: Uninitialize**</span><span class="sxs-lookup"><span data-stu-id="05a06-129">**INapEnforcementClientBinding::Uninitialize**</span></span>](inapenforcementclientbinding-uninitialize-method.md)                           | <span data-ttu-id="05a06-130">Schließt den NAPAgent-Dienst für diese Client Verbindung ab.</span><span class="sxs-lookup"><span data-stu-id="05a06-130">Concludes the NapAgent service for this client connection.</span></span><br/>                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="05a06-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05a06-131">Remarks</span></span>

<span data-ttu-id="05a06-132">Alle APIs in dieser Schnittstelle geben RPC \_ E getrennt zurück, \_ Wenn der NAPAgent angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="05a06-132">All the APIs in this interface will return RPC\_E\_DISCONNECTED if the NapAgent is stopped.</span></span> <span data-ttu-id="05a06-133">Dieses Objekt wird nach dem Neustart automatisch wieder hergestellt und an den NAPAgent gebunden.</span><span class="sxs-lookup"><span data-stu-id="05a06-133">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="05a06-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05a06-134">Requirements</span></span>



| <span data-ttu-id="05a06-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05a06-135">Requirement</span></span> | <span data-ttu-id="05a06-136">Wert</span><span class="sxs-lookup"><span data-stu-id="05a06-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05a06-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05a06-137">Minimum supported client</span></span><br/> | <span data-ttu-id="05a06-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05a06-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="05a06-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05a06-139">Minimum supported server</span></span><br/> | <span data-ttu-id="05a06-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="05a06-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="05a06-141">Header</span><span class="sxs-lookup"><span data-stu-id="05a06-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="05a06-142"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="05a06-142"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="05a06-143">IDL</span><span class="sxs-lookup"><span data-stu-id="05a06-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="05a06-144"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="05a06-144"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="05a06-145">DLL</span><span class="sxs-lookup"><span data-stu-id="05a06-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05a06-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05a06-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="05a06-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05a06-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05a06-148">NAP-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="05a06-148">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="05a06-149">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="05a06-149">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

