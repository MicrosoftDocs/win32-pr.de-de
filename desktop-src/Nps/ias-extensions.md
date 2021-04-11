---
title: Erweiterungen für Netzwerk Richtlinien Server
description: Mit der NPS-Erweiterungs-API können Softwareentwickler Erweiterungs-DLLs schreiben, die für Authentifizierung, Autorisierung und Kontoführung verwendet werden können. Die NPS-Erweiterungs-API unterstützt das RADIUS-Protokoll (Remote Authentication Dial-in User Service).
ms.assetid: f459025f-fe5e-4ffa-a651-c70a4f8234ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd6f9bd0be7479726110b41d6060a7e5c836bb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948968"
---
# <a name="network-policy-server-extensions"></a><span data-ttu-id="ed61d-104">Erweiterungen für Netzwerk Richtlinien Server</span><span class="sxs-lookup"><span data-stu-id="ed61d-104">Network Policy Server Extensions</span></span>

> [!Note]  
> <span data-ttu-id="ed61d-105">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="ed61d-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="ed61d-106">Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS.</span><span class="sxs-lookup"><span data-stu-id="ed61d-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="ed61d-107">Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="ed61d-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="ed61d-108">Mit der NPS-Erweiterungs-API können Softwareentwickler Erweiterungs-DLLs schreiben, die für Authentifizierung, Autorisierung und Kontoführung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="ed61d-108">The NPS Extensions API enables software developers to write extension DLLs that can be used for authentication, authorization, and accounting.</span></span> <span data-ttu-id="ed61d-109">Die NPS-Erweiterungs-API unterstützt das RADIUS-Protokoll (Remote Authentication Dial-in User Service).</span><span class="sxs-lookup"><span data-stu-id="ed61d-109">NPS Extensions API supports the Remote Authentication Dial-In User Service (RADIUS) protocol.</span></span>

<span data-ttu-id="ed61d-110">Die mit der NPS-Erweiterungs-API implementierten Erweiterungs-DLLs können eine verbesserte Sitzungssteuerung und-Kontoführung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ed61d-110">The extension DLLs implemented using the NPS Extensions API can provide enhanced session control and accounting.</span></span> <span data-ttu-id="ed61d-111">Diese DLLs können für Szenarien wie z. b. das Steuern der Anzahl von Netzwerksitzungen des Endbenutzers, die Verwendung eines Zustands Servers und das Herstellen einer Verbindung mit Domänen Authentifizierungs Datenbanken und Active Directory Diensten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ed61d-111">These DLLs can be used for scenarios such as controlling the number of end-user network sessions, using a state server, and connecting to domain authentication databases and Active Directory services.</span></span> <span data-ttu-id="ed61d-112">Die Erweiterungs-DLLs können die von NPS bereitgestellten Remote Zugriffs Autorisierungen erweitern, indem Sie Ihre eigenen Autorisierungen hinzufügen, wenn Sie eine Accept-Antwort an einen authentifizier enden Client zurücksenden.</span><span class="sxs-lookup"><span data-stu-id="ed61d-112">The extension DLLs can expand the remote access authorizations provided by NPS by adding their own authorizations when sending an Accept response back to an authenticating client.</span></span>

<span data-ttu-id="ed61d-113">Die NPS-Erweiterungs-API ist in jeder Computerumgebung anwendbar, in der Sie die Effizienz bei der Authentifizierung von einwählbenutzern über einen Remote Server verbessern.</span><span class="sxs-lookup"><span data-stu-id="ed61d-113">NPS Extensions API is applicable in any computing environment where it would improve efficiency to authenticate dial-in users through a remote server.</span></span> <span data-ttu-id="ed61d-114">Diese Technologie ist besonders nützlich für Internet Dienstanbieter (Internet Service Providers, ISPs).</span><span class="sxs-lookup"><span data-stu-id="ed61d-114">This technology is especially useful for Internet Service Providers (ISPs).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ed61d-115">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ed61d-115">In This Section</span></span>

[<span data-ttu-id="ed61d-116">Übersicht</span><span class="sxs-lookup"><span data-stu-id="ed61d-116">Overview</span></span>](/windows/desktop/Nps/ias-about-internet-authentication-service)

<span data-ttu-id="ed61d-117">Allgemeine Informationen zu RADIUS und der NPS-Erweiterungs-API.</span><span class="sxs-lookup"><span data-stu-id="ed61d-117">General information about RADIUS and the NPS Extensions API.</span></span>

[<span data-ttu-id="ed61d-118">Genutzt</span><span class="sxs-lookup"><span data-stu-id="ed61d-118">Using</span></span>](/windows/desktop/Nps/ias-using-internet-authentication-service)

<span data-ttu-id="ed61d-119">Beispielcode, der die Verwendung der NPS-Erweiterungs-API veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="ed61d-119">Sample code that demonstrates how to use the NPS Extensions API.</span></span>

[<span data-ttu-id="ed61d-120">Verweis</span><span class="sxs-lookup"><span data-stu-id="ed61d-120">Reference</span></span>](/windows/desktop/Nps/ias-internet-authentication-service-reference)

<span data-ttu-id="ed61d-121">Dokumentation von enumerierten Typen, Funktionen und Strukturen, die die NPS-Erweiterungs-API bilden.</span><span class="sxs-lookup"><span data-stu-id="ed61d-121">Documentation of enumerated types, functions, and structures that compose the NPS Extensions API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed61d-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ed61d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed61d-123">Netzwerk Richtlinien Server (Internet Authentication Service)</span><span class="sxs-lookup"><span data-stu-id="ed61d-123">Network Policy Server (Internet Authentication Service)</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="ed61d-124">Extensible Authentication-Protokoll (EAP)</span><span class="sxs-lookup"><span data-stu-id="ed61d-124">Extensible Authentication Protocol (EAP)</span></span>](../eap/eap-start-page.md)
</dt> </dl>

 

 