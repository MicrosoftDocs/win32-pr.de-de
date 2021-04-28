---
description: 'Microsoft Message Queuing (MSMQ): Entfernen des Windows 2000-Clientsupportdiensts'
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: 'Microsoft Message Queuing (MSMQ): Entfernen des Windows 2000-Clientsupportdiensts'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be68d40271153567bdaf6b04d73218aaf3d3977
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088148"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a><span data-ttu-id="5ddfa-103">Microsoft Message Queuing (MSMQ): Entfernen des Windows 2000-Clientsupportdiensts</span><span class="sxs-lookup"><span data-stu-id="5ddfa-103">Microsoft Message Queuing (MSMQ) - Removal of Windows 2000 Client Support Service</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="5ddfa-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="5ddfa-104">Affected Platforms</span></span>

<span data-ttu-id="5ddfa-105">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5ddfa-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="5ddfa-106">Auswirkungen auf Das Feature</span><span class="sxs-lookup"><span data-stu-id="5ddfa-106">Feature Impact</span></span>

 <span data-ttu-id="5ddfa-107">**Schweregrad –** Hoch</span><span class="sxs-lookup"><span data-stu-id="5ddfa-107">**Severity** - High</span></span>  
<span data-ttu-id="5ddfa-108">**Häufigkeit** : Niedrig</span><span class="sxs-lookup"><span data-stu-id="5ddfa-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="5ddfa-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ddfa-109">Description</span></span>

<span data-ttu-id="5ddfa-110">Der Windows 2000-Clientsupportdienst ist eine optionale Komponente des Message Queuing-Servers, die Sie auf einem Windows 2003- oder Windows 2008-Domänencontrollercomputer installieren können.</span><span class="sxs-lookup"><span data-stu-id="5ddfa-110">The Windows 2000 Client Support Service is an optional component of the Message Queuing Server that you can install on a Windows 2003 or Windows 2008 domain controller machine.</span></span> <span data-ttu-id="5ddfa-111">Dieser Dienst ermöglicht Windows 2000-Clients den Betrieb in einem domänenintegrierten Modus mit einem beliebigen Message Queuing Server, der auf Windows 2003/2008-Computern installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5ddfa-111">This service allows Windows 2000 clients to operate in a domain-integrated mode with any Message Queuing server installed on Windows 2003/2008 machines.</span></span> <span data-ttu-id="5ddfa-112">MSMQ-Clients, die unter Windows XP aufwärts arbeiten, benötigen diesen Dienst nicht.</span><span class="sxs-lookup"><span data-stu-id="5ddfa-112">MSMQ Clients operating on Windows XP upwards do not need this service.</span></span>

### <a name="manifestation-of-impact"></a><span data-ttu-id="5ddfa-113">Wirkungserz weiter</span><span class="sxs-lookup"><span data-stu-id="5ddfa-113">Manifestation of Impact</span></span>

<span data-ttu-id="5ddfa-114">Diese Änderung wirkt sich auf Windows 2000 aus, wenn in einer Windows 7-Domäne interoperiert wird, in der alle Domänencontroller Windows Server 2008 R2 sind.</span><span class="sxs-lookup"><span data-stu-id="5ddfa-114">This change impacts Windows 2000 when interoperating in a Windows 7 domain where all domain controllers are Windows Server 2008 R2.</span></span> <span data-ttu-id="5ddfa-115">Wenn ein Kunde ein Upgrade auf die Windows 7-Domäne vorliegt, können die vorhandenen MSMQ-Anwendungen auf allen Windows 2000-Computern in der Domäne nicht in einem in die Domäne integrierten Modus ausgeführt werden, es sei denn, diese Clients führen ein Upgrade auf eine höhere Windows-Version durch.</span><span class="sxs-lookup"><span data-stu-id="5ddfa-115">If a customer upgrades to the Windows 7 domain, the existing MSMQ applications on any Windows 2000 machines in the domain will not be able to operate in a domain-integrated mode unless these clients upgrade to a higher Windows version.</span></span>

### <a name="mitigation"></a><span data-ttu-id="5ddfa-116">Minderung</span><span class="sxs-lookup"><span data-stu-id="5ddfa-116">Mitigation</span></span>

<span data-ttu-id="5ddfa-117">Benutzer mit Windows 2000-Clientcomputern in einer Windows 7-Domäne können einen Windows 2003/2008-Domänencontroller in der Domäne konfigurieren und den MSMQ Windows 2000-Clientsupportdienst auf diesem Domänencontroller installieren.</span><span class="sxs-lookup"><span data-stu-id="5ddfa-117">Users who have Windows 2000 Client machines on a Windows 7 domain can configure a Windows 2003/2008 domain controller in the domain and install the MSMQ Windows 2000 Client Support Service on this domain controller.</span></span>

### <a name="leveraging-feature-capabilities"></a><span data-ttu-id="5ddfa-118">Nutzen von Featurefunktionen</span><span class="sxs-lookup"><span data-stu-id="5ddfa-118">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="5ddfa-119">Benutzer mit Windows 2000-Clientcomputern, auf denen MSMQ ausgeführt wird, sollten ein Upgrade auf eine höhere Windows-Version durchführen, um die Active Directory-basierte Implementierung des MSMQ-Servers nutzen zu können.</span><span class="sxs-lookup"><span data-stu-id="5ddfa-119">Users who have Windows 2000 Client machines running MSMQ should upgrade to a higher Windows version in order to take advantage of the Active Directory-based implementation of the MSMQ Server.</span></span>

### <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="5ddfa-120">Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Benutzerfreundlichkeitstests</span><span class="sxs-lookup"><span data-stu-id="5ddfa-120">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="5ddfa-121">Benutzer, die über Windows 2000-Clientcomputer verfügen, auf denen MSMQ in einer Windows 7-Domäne mit einem oder mehreren downleveln Domänencontrollern ausgeführt wird, sollten überprüfen, ob ihre Anwendungen in dieser gemischten Domäne funktionieren.</span><span class="sxs-lookup"><span data-stu-id="5ddfa-121">Users who have Windows 2000 Client machines running MSMQ on a Windows 7 domain with one or more down-level domain controllers should verify that their applications are functional on this mixed domain.</span></span>

 

 



