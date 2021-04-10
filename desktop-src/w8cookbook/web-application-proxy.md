---
title: Webanwendungsproxy
description: Webanwendungsproxy
ms.assetid: DE47843C-D58B-4C71-99C2-D54073CBA531
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220ac5f52a8f5130cdb6fb21649ff302e6693b1b
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104102466"
---
# <a name="web-application-proxy"></a><span data-ttu-id="04df3-103">Webanwendungsproxy</span><span class="sxs-lookup"><span data-stu-id="04df3-103">Web Application Proxy</span></span>

## <a name="platform"></a><span data-ttu-id="04df3-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="04df3-104">Platform</span></span>

<span data-ttu-id="04df3-105">**Server:** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="04df3-105">**Servers -** Windows Server 2012 R2</span></span>  






## <a name="description"></a><span data-ttu-id="04df3-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04df3-106">Description</span></span>

<span data-ttu-id="04df3-107">In Windows Server 2012 R2 haben wir einen neuen Dienst mit dem Namen "webanwendungsproxy" unter der Remote Zugriffs Rolle hinzugefügt, mit dem Administratoren Anwendungen für den externen Zugriff veröffentlichen können.</span><span class="sxs-lookup"><span data-stu-id="04df3-107">In Windows Server 2012 R2, we added a new service called the Web Application Proxy under the Remote Access role that allows administrators to publish applications for external access.</span></span> <span data-ttu-id="04df3-108">Dieser Dienst fungiert als Reverseproxy und als Active Directory-Verbunddienste (AD FS)-Proxy (AD FS).</span><span class="sxs-lookup"><span data-stu-id="04df3-108">This service acts as a reverse proxy and as an Active Directory Federation Services (AD FS) proxy.</span></span> <span data-ttu-id="04df3-109">Tatsächlich ersetzt dieser Dienst den AD FS Proxy Dienst, wie er in Windows Server 2012 bekannt war.</span><span class="sxs-lookup"><span data-stu-id="04df3-109">In fact, this service replaces the AD FS proxy service as it was known in Windows Server 2012.</span></span>

<span data-ttu-id="04df3-110">Mit dem webanwendungsproxy kann eine Organisation lokale Webressourcen für den externen Zugriff verfügbar machen, während gleichzeitig das Risiko dieses Zugriffs durch Steuern der Authentifizierungs-und Autorisierungs Richtlinien auf dem AD FS verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="04df3-110">With the Web Application Proxy, an organization can make on-premises web resources available for external access while at the same time managing the risk of this access by controlling authentication and authorization policies on the AD FS.</span></span>

## <a name="manifestation"></a><span data-ttu-id="04df3-111">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="04df3-111">Manifestation</span></span>

<span data-ttu-id="04df3-112">Der AD FS Proxy Dienst befindet sich nicht mehr in der Active Directory-Verbunddienste (AD FS)-Rolle (AD FS), sondern wurde durch den webanwendungsproxy unter der Remote Zugriffs Rolle ersetzt.</span><span class="sxs-lookup"><span data-stu-id="04df3-112">The AD FS proxy service is no longer under the Active Directory Federation Services role (AD FS), but has been replaced by the Web Application Proxy under the Remote Access role.</span></span> <span data-ttu-id="04df3-113">Dies stellt eine Erweiterung des AD FS Proxy Dienstanbieter durch Einschließen von Reverseproxyfunktionen für die Anwendungs Veröffentlichung dar.</span><span class="sxs-lookup"><span data-stu-id="04df3-113">This represents an expansion of the AD FS proxy service by including reverse proxy functionality for application publishing.</span></span>

## <a name="solution"></a><span data-ttu-id="04df3-114">Lösung</span><span class="sxs-lookup"><span data-stu-id="04df3-114">Solution</span></span>

<span data-ttu-id="04df3-115">Für den Zugriff auf den webanwendungsproxy können Administratoren zu Server-Manager wechseln und eine neue Rolle/einen neuen Rollen Dienst hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="04df3-115">To access the Web Application Proxy, administrators can go to Server Manager and add a new role/role service.</span></span> <span data-ttu-id="04df3-116">Der Administrator findet den webanwendungsproxy unter der Remote Zugriffs Rolle.</span><span class="sxs-lookup"><span data-stu-id="04df3-116">The administrator will find the Web Application Proxy under the Remote Access role.</span></span>

## <a name="resources"></a><span data-ttu-id="04df3-117">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="04df3-117">Resources</span></span>

-   <span data-ttu-id="04df3-118">[Lösungsanleitung](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="04df3-118">[Solution guide](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/dn280942(v=ws.11))</span></span>

 

 