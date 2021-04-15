---
title: EAPHost-API-Referenz
description: Erfahren Sie mehr über EAPHost-APIs und deren Komponenten. Siehe Referenzinformationen zu verschiedenen API-Themen, wie z. b. das XML-Schema von EAPHost.
ms.assetid: ac2f074f-b525-42a2-8637-c96a08d77714
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6c4d80c402f963a05bbcfb79ca451541603489e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104390999"
---
# <a name="eaphost-api-reference"></a><span data-ttu-id="43fe2-104">EAPHost-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="43fe2-104">EAPHost API Reference</span></span>

<span data-ttu-id="43fe2-105">Die EAPHost-APIs sind in drei Komponenten unterteilt: die Supplicant-APIs, die direkt von einer EAP-fähigen Anwendung aufgerufen werden können. die APIs der EAP-Peer Methode, die Supplicant-Anforderungen für einen bestimmten EAP-Authentifizierungstyp verwalten und interaktive Elemente auf dem Client aufrufen. und die EAP Authenticator-APIs, die die serverseitige Authentifizierung eines Supplicant ausführen.</span><span class="sxs-lookup"><span data-stu-id="43fe2-105">The EAPHost APIs are divided into three components: the supplicant APIs, which are directly callable from an EAP-enabled application; the EAP peer method APIs, which manage supplicant requests for a specific EAP authentication type and raise interactive elements on the client; and the EAP authenticator APIS, which perform the server-side authentication of a supplicant.</span></span>

<span data-ttu-id="43fe2-106">Die beiden letzten API-Komponenten (die EAP-Peer Methode und die EAP Authenticator-Methoden-APIs) erfordern eine benutzerdefinierte und konforme Implementierung in DLLs, die Sie für den EAPHost-Dienst verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="43fe2-106">The latter two API components -- the EAP Peer Method and EAP Authenticator Method APIs -- require custom and conformant implementation in DLLs that expose them to the EAPHost service.</span></span> <span data-ttu-id="43fe2-107">Sie können nicht direkt aus dem Anwendungscode aufgerufen werden. Stattdessen werden Sie von EAPHost (auf Clientseite für EAP-Peer Methoden und auf der Serverseite für EAP Authenticator-Methoden) aufgerufen, wenn die Implementierung den in der entsprechenden Dokumentation angegebenen API-Signaturen entspricht.</span><span class="sxs-lookup"><span data-stu-id="43fe2-107">They cannot be called directly from application code; instead, they are called by EAPHost (on client side for EAP peer methods, and on the server side for EAP authenticator methods) if the implementation matches the API signatures specified in the corresponding documentation.</span></span> <span data-ttu-id="43fe2-108">Spezifische Informationen zur API-Implementierung werden auf jeder Funktionsreferenz Seite bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="43fe2-108">API implementation specific information is provided on each function reference page.</span></span>

## <a name="eaphost-registry-settings"></a><span data-ttu-id="43fe2-109">EAPHost-Registrierungs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="43fe2-109">EAPHost Registry Settings</span></span>



| <span data-ttu-id="43fe2-110">Thema</span><span class="sxs-lookup"><span data-stu-id="43fe2-110">Topic</span></span>                                                      | <span data-ttu-id="43fe2-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43fe2-111">Description</span></span>                                      |
|------------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="43fe2-112">EAPHost-Registrierungs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="43fe2-112">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md) | <span data-ttu-id="43fe2-113">Beschreibt die von EAPHost genutzten Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="43fe2-113">Describes the registry keys consumed by EAPHost.</span></span> |



 

## <a name="eaphost-xml-schema"></a><span data-ttu-id="43fe2-114">EAPHost-XML-Schema</span><span class="sxs-lookup"><span data-stu-id="43fe2-114">EAPHost XML Schema</span></span>



| <span data-ttu-id="43fe2-115">Thema</span><span class="sxs-lookup"><span data-stu-id="43fe2-115">Topic</span></span>                                            | <span data-ttu-id="43fe2-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43fe2-116">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43fe2-117">EAPHost und Legacy Schema</span><span class="sxs-lookup"><span data-stu-id="43fe2-117">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md) | <span data-ttu-id="43fe2-118">Beschreibt das EAPHost-Schema und das Legacy Schema zum Erstellen von XML-Konfigurationsdateien und Anmelde Informationen.</span><span class="sxs-lookup"><span data-stu-id="43fe2-118">Describes the EAPHost schema and legacy schema for creating configuration XML and credential XML.</span></span> |



 

## <a name="common-eaphost-api-reference"></a><span data-ttu-id="43fe2-119">Allgemeine EAPHost-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="43fe2-119">Common EAPHost API Reference</span></span>



| <span data-ttu-id="43fe2-120">Thema</span><span class="sxs-lookup"><span data-stu-id="43fe2-120">Topic</span></span>                                                                   | <span data-ttu-id="43fe2-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43fe2-121">Description</span></span>                                  |
|-------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="43fe2-122">Allgemeine EAPHost-API-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="43fe2-122">Common EAPHost API Enumerations</span></span>](common-eap-host-api-enumerations.md) | <span data-ttu-id="43fe2-123">Listet Konstanten auf, die allen EAPHost-APIs gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="43fe2-123">Lists constants common to all EAPHost APIs.</span></span>  |
| [<span data-ttu-id="43fe2-124">Allgemeine EAPHost-API-Strukturen</span><span class="sxs-lookup"><span data-stu-id="43fe2-124">Common EAPHost API Structures</span></span>](common-eap-host-api-structures.md)     | <span data-ttu-id="43fe2-125">Listet Strukturen auf, die allen EAPHost-APIs gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="43fe2-125">Lists structures common to all EAPHost APIs.</span></span> |
| [<span data-ttu-id="43fe2-126">Allgemeine EAPHost-API-Konstanten</span><span class="sxs-lookup"><span data-stu-id="43fe2-126">Common EAPHost API Constants</span></span>](common-eap-host-error-constants.md)     | <span data-ttu-id="43fe2-127">Listet Konstanten auf, die allen EAPHost-APIs gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="43fe2-127">Lists constants common to all EAPHost APIs.</span></span>  |



 

## <a name="eaphost-api-reference"></a><span data-ttu-id="43fe2-128">EAPHost-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="43fe2-128">EAPHost API Reference</span></span>



| <span data-ttu-id="43fe2-129">Thema</span><span class="sxs-lookup"><span data-stu-id="43fe2-129">Topic</span></span>                                                                       | <span data-ttu-id="43fe2-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43fe2-130">Description</span></span>                                                                                                                                      |
|-----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43fe2-131">EAPHost-Supplicant-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="43fe2-131">EAPHost Supplicant API Reference</span></span>](eap-host-supplicant-api-reference.md)   | <span data-ttu-id="43fe2-132">Beschreibt die verfügbaren API-Elemente, um Supplicant Aufrufe von EAPHost zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="43fe2-132">Describes the API elements available to enable supplicant calls to EAPHost.</span></span>                                                                      |
| [<span data-ttu-id="43fe2-133">API-Referenz für die EAPHost-Peer Methode</span><span class="sxs-lookup"><span data-stu-id="43fe2-133">EAPHost Peer Method API Reference</span></span>](eap-host-peer-method-api-reference.md) | <span data-ttu-id="43fe2-134">Beschreibt die API-Elemente, die implementiert werden müssen, um eine EAP-Peer Methoden-dll zu erstellen, die von einem Client-EAPHost geladen und aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="43fe2-134">Describes the API elements that must be implemented to create an EAP peer method DLL that can be loaded and called by a client EAPHost.</span></span>          |
| [<span data-ttu-id="43fe2-135">EAPHost-Authenticator-Methoden-APIs</span><span class="sxs-lookup"><span data-stu-id="43fe2-135">EAPHost Authenticator Method APIs</span></span>](eaphost-authenticator-method-apis.md)  | <span data-ttu-id="43fe2-136">Beschreibt die API-Elemente, die implementiert werden müssen, um eine EAP Authenticator-Methoden-dll zu erstellen, die von einem Server EAPHost geladen und aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="43fe2-136">Describes the API elements that must be implemented to create an EAP authenticator method DLL that can be loaded and called by a server EAPHost.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="43fe2-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43fe2-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43fe2-138">Informationen zu EAPHost</span><span class="sxs-lookup"><span data-stu-id="43fe2-138">About EAPHost</span></span>](about-eap-host.md)
</dt> <dt>

[<span data-ttu-id="43fe2-139">Verwenden von EAPHost</span><span class="sxs-lookup"><span data-stu-id="43fe2-139">Using EAPHost</span></span>](using-eap-host.md)
</dt> </dl>

 

 




