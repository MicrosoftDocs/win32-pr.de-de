---
description: Definiert den Typ von Endpunkten, die zum Herstellen einer Verbindung mit einem Dienst verwendet werden können.
ms.assetid: 50397D25-7C71-4AA2-89BF-F90CBDCFFA91
title: Updateendpointtype-Enumeration (updateendpointauth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: 942bcb5275c6a4f39d6e2828025e5b9a40e52c46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525073"
---
# <a name="updateendpointtype-enumeration"></a><span data-ttu-id="abe1a-103">Updateendpointtype-Enumeration</span><span class="sxs-lookup"><span data-stu-id="abe1a-103">UpdateEndpointType enumeration</span></span>

<span data-ttu-id="abe1a-104">Definiert den Typ von Endpunkten, die zum Herstellen einer Verbindung mit einem Dienst verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="abe1a-104">Defines the type of endpoints that can be used to connect to a service.</span></span>

## <a name="syntax"></a><span data-ttu-id="abe1a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="abe1a-105">Syntax</span></span>


```C++
typedef enum tagEndpointType { 
  uetClientServer          = 0,
  uetReporting             = ( uetClientServer + 1 ),
  uetWuaSelfUpdate         = ( uetReporting + 1 ),
  uetRegulation            = ( uetWuaSelfUpdate + 1 ),
  uetSimpleTargeting       = ( uetRegulation + 1 ),
  uetSecuredClientServer   = ( uetSimpleTargeting + 1 ),
  uetSecondaryServiceAuth  = ( uetSecuredClientServer + 1 )
} UpdateEndpointType;
```



## <a name="constants"></a><span data-ttu-id="abe1a-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="abe1a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="abe1a-107"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetclientserver**</span><span class="sxs-lookup"><span data-stu-id="abe1a-107"><span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**</span></span>
</dt> <dd>

<span data-ttu-id="abe1a-108">Ein Client/Server-Endpunkt, der zum Herstellen der Verbindung mit dem Aktualisierungs Dienst verwendet wird, z. b. Windows Update, Microsoft Update und WSUS-Server in einer Unternehmensumgebung, um Informationen zu Updates zu erhalten, die möglicherweise für den Computer gelten.</span><span class="sxs-lookup"><span data-stu-id="abe1a-108">A client-server endpoint that is used to connect to the update service, such as Windows Update, Microsoft Update, and WSUS server in a corporate environment, to find information on updates that may be applicable to the computer.</span></span>

<span data-ttu-id="abe1a-109">Der Aktualisierungs Dienst gibt Informationen zu Updates zurück, die seit der letzten Synchronisierung des Clients mit dem Server veröffentlicht, überarbeitet oder zurückgezogen wurden.</span><span class="sxs-lookup"><span data-stu-id="abe1a-109">The update service returns information on updates that have been published, revised, or withdrawn since the last time that client performed a sync with the server.</span></span>

</dd> <dt>

<span data-ttu-id="abe1a-110"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetreporting**</span><span class="sxs-lookup"><span data-stu-id="abe1a-110"><span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**</span></span>
</dt> <dd>

<span data-ttu-id="abe1a-111">Ein Berichterstattungs Endpunkt, der verwendet wird, wenn der Client die Ergebnisse von Scans, Downloads und Installationen zurück an den Aktualisierungs Dienst meldet.</span><span class="sxs-lookup"><span data-stu-id="abe1a-111">A reporting endpoint that is used when the client reports the results of scans, downloads, and installs back to the update service.</span></span>

<span data-ttu-id="abe1a-112">Im Fall von öffentlichen Diensten (Windows Update und Microsoft Update) erfolgt dies für Qualitäts Überwachungszwecke.</span><span class="sxs-lookup"><span data-stu-id="abe1a-112">In the case of public services (Windows Update and Microsoft Update), this is done for quality monitoring purposes.</span></span>

<span data-ttu-id="abe1a-113">Bei privaten Diensten, z. b. bei einem WSUS-Server des Unternehmens, kann der Server mit thhis-Endpunkt auch Inventur Daten und andere Informationen zu den Client Computern, die verwaltet werden, erfassen.</span><span class="sxs-lookup"><span data-stu-id="abe1a-113">In the case of private services, such as a corporate WSUS server, thhis type of endpoint also allows the server to collect inventory and other information about the client computers under management.</span></span>

</dd> <dt>

<span data-ttu-id="abe1a-114"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetwuaselfupdate**</span><span class="sxs-lookup"><span data-stu-id="abe1a-114"><span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="abe1a-115">Ein selbst Aktualisierungs Endpunkt, der verwendet wird, wenn der Client Computer einen Update Dienst kontaktiert, um festzustellen, ob eine neue Version der Windows Update-Agent-Client Software vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="abe1a-115">A self-update endpoint that is used when the client computer contacts an update service to see whether there is a new version of the Windows Update Agent client software.</span></span>

<span data-ttu-id="abe1a-116">Der Self-Update-Endpunkt verwendet ein anderes Protokoll als den Client-Server Endpunkt, sodass selbst Updates verteilt werden können, auch wenn es einen Fehlerzustand gibt, der möglicherweise verhindert, dass die normale Client/Server-Synchronisierung auf einem bestimmten Client Computer funktioniert.</span><span class="sxs-lookup"><span data-stu-id="abe1a-116">The Self-update endpoint uses a different protocol then the Client-Server endpoint so that self-updates can be distributed even if there is an error condition that might be preventing the normal client-server sync from working on a particular client computer.</span></span>

</dd> <dt>

<span data-ttu-id="abe1a-117"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetregulations**</span><span class="sxs-lookup"><span data-stu-id="abe1a-117"><span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**</span></span>
</dt> <dd>

<span data-ttu-id="abe1a-118">Ein-Regel Endpunkt, der verwendet wird, wenn der Client Computer eine Verbindung mit dem-Verwaltungs Endpunkt hergestellt hat, um ein bestimmtes Update zu ergreifen, das auf den Zielcomputer anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="abe1a-118">A regulation endpoint that is used when the client computer contacts the regulation service to act on a particular update that is applicable to the target computer.</span></span>

<span data-ttu-id="abe1a-119">Der-Regulierungs Dienst kann angeben, ob das Update "reguliert" (auch als "gedrosselt" bezeichnet) – mit anderen Worten: der-Regulierungs Dienst kann dem Client Computer mitteilen, dass er nicht auf ein bestimmtes Update angewendet werden soll, obwohl dieses Update zutreffend ist.</span><span class="sxs-lookup"><span data-stu-id="abe1a-119">The regulation service can indicate whether the update is “regulated” (also known as “throttled”) – in other words, the regulation service can tell the client computer that it should not act on a particular update, even though that update appears to be applicable.</span></span>

</dd> <dt>

<span data-ttu-id="abe1a-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetsimpletargeting**</span><span class="sxs-lookup"><span data-stu-id="abe1a-120"><span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**</span></span>
</dt> <dd>

<span data-ttu-id="abe1a-121">Ein Endpunkt für die einfache Ausrichtung, der nur mit privaten Diensten (WSUS-Server in Unternehmensumgebungen) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="abe1a-121">A simple-targeting endpoint that is used only with private services (WSUS servers in corporate environments).</span></span> <span data-ttu-id="abe1a-122">In einer Unternehmensumgebung können Client Computer bestimmten Zielgruppen zugewiesen werden, und Updates können für die Installation auf Computern in einigen Gruppen, aber nicht für andere Personen genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="abe1a-122">In a corporate environment, client computers can be assigned to particular target groups, and updates can be approved for installation on computers in some groups but not others.</span></span>

<span data-ttu-id="abe1a-123">Beispielsweise kann der WSUS-Administrator eine "Test"-Gruppe für Computer erstellen, die zum Testen neuer Updates verwendet werden, und der Administrator kann neu veröffentlichte Updates für die Installation auf Computern in der Testgruppe genehmigen, ohne Sie für die Installation auf anderen Computern in der Organisation genehmigen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="abe1a-123">For example, the WSUS administrator may create a “Testing” group for computers that are used to test new updates, and the administrator may approve newly-released updates for installation on computers in the Testing group without approving them for installation on other computers in the organization.</span></span> <span data-ttu-id="abe1a-124">Die einfache Zielgruppe wird verwendet, um einem Client Computer die Registrierung beim WSUS-Server zu ermöglichen und dem Server zu gestatten, dem Client Computer mitzuteilen, in welcher Gruppe er sich befindet.</span><span class="sxs-lookup"><span data-stu-id="abe1a-124">The simple targeting exchange is used to allow a client computer to register itself with the WSUS server, and to allow the server to tell the client computer what group it is in.</span></span>

</dd> <dt>

<span data-ttu-id="abe1a-125"><span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetsecuredclientserver**</span><span class="sxs-lookup"><span data-stu-id="abe1a-125"><span id="uetSecuredClientServer"></span><span id="uetsecuredclientserver"></span><span id="UETSECUREDCLIENTSERVER"></span>**uetSecuredClientServer**</span></span>
</dt> <dd>

<span data-ttu-id="abe1a-126">Einen gesicherten Client/Server-Endpunkt, mit dem ein Client Informationen zu apps abrufen kann, die eine Lizenzierung benötigen, damit Sie auf einem Client Computer verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="abe1a-126">A secured-client-server endpoint that allows a client to obtain info on apps that need licensing so they can be used on a client computer.</span></span> <span data-ttu-id="abe1a-127">Dieses Lizenzierungs Framework wird zurzeit nur von Windows 8 verwendet, um apps und Updates bereitzustellen, die über den Windows Store abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="abe1a-127">This licensing framework is currently only used by Windows 8 to deploy apps and updates that are obtained through the Windows Store.</span></span> <span data-ttu-id="abe1a-128">Der gesicherte Client-Server-Endpunkt wird derzeit nicht von Windows Update, Microsoft Update oder WSUS verwendet.</span><span class="sxs-lookup"><span data-stu-id="abe1a-128">The secured-client-server endpoint is currently not used by Windows Update, Microsoft Update, or WSUS.</span></span>

</dd> <dt>

<span data-ttu-id="abe1a-129"><span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetsecondaryserviceauth**</span><span class="sxs-lookup"><span data-stu-id="abe1a-129"><span id="uetSecondaryServiceAuth"></span><span id="uetsecondaryserviceauth"></span><span id="UETSECONDARYSERVICEAUTH"></span>**uetSecondaryServiceAuth**</span></span>
</dt> <dd>

<span data-ttu-id="abe1a-130">Der Endpunkt für die sekundäre Dienst Authentifizierung wird von einem Client verwendet, um die Authentifizierung bereitzustellen, bevor er Informationen zu apps erhält, die eine Lizenzierung benötigen, damit Sie auf einem Client Computer verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="abe1a-130">The secondary-service-authentication endpoint is used by a client to provide authentication before it obtains info on apps that need licensing so they can be used on a client computer.</span></span> <span data-ttu-id="abe1a-131">Dieses Lizenzierungs Framework wird derzeit nur von Windows 8 verwendet, um apps und Updates bereitzustellen, die über den Windows Store abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="abe1a-131">This licensing framework is currently only utilized by Windows 8 to deploy apps and updates that are obtained through the Windows Store.</span></span> <span data-ttu-id="abe1a-132">Der Endpunkt für die sekundäre Dienst Authentifizierung wird derzeit von Windows Update, Microsoft Update oder WSUS nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="abe1a-132">The secondary-service-authentication endpoint is currently not used by Windows Update, Microsoft Update, or WSUS.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abe1a-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abe1a-133">Requirements</span></span>



| <span data-ttu-id="abe1a-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abe1a-134">Requirement</span></span> | <span data-ttu-id="abe1a-135">Wert</span><span class="sxs-lookup"><span data-stu-id="abe1a-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abe1a-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abe1a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="abe1a-137">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abe1a-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="abe1a-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abe1a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="abe1a-139">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abe1a-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="abe1a-140">Header</span><span class="sxs-lookup"><span data-stu-id="abe1a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="abe1a-141"><dt>Updateendpointauth. h</dt></span><span class="sxs-lookup"><span data-stu-id="abe1a-141"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="abe1a-142">IDL</span><span class="sxs-lookup"><span data-stu-id="abe1a-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="abe1a-143"><dt>Updateendpointauth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="abe1a-143"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



 

 




