---
description: .
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: Microsoft Message Queuing (MSMQ)-Entfernen des Windows 2000-Client Unterstützungs Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54688ee4ad24eb691c95e4d70ce0acb881e212eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050306"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a><span data-ttu-id="4cf2c-103">Microsoft Message Queuing (MSMQ)-Entfernen des Windows 2000-Client Unterstützungs Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="4cf2c-103">Microsoft Message Queuing (MSMQ) - Removal of Windows 2000 Client Support Service</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="4cf2c-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="4cf2c-104">Affected Platforms</span></span>

<span data-ttu-id="4cf2c-105">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4cf2c-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="4cf2c-106">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="4cf2c-106">Feature Impact</span></span>

 <span data-ttu-id="4cf2c-107">**Schweregrad** -hoch</span><span class="sxs-lookup"><span data-stu-id="4cf2c-107">**Severity** - High</span></span>  
<span data-ttu-id="4cf2c-108">**Häufigkeit** -niedrig</span><span class="sxs-lookup"><span data-stu-id="4cf2c-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="4cf2c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4cf2c-109">Description</span></span>

<span data-ttu-id="4cf2c-110">Der Windows 2000-Client Support Dienst ist eine optionale Komponente des Message Queuing Servers, den Sie auf einem Windows 2003-oder Windows 2008-Domänen Controller Computer installieren können.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-110">The Windows 2000 Client Support Service is an optional component of the Message Queuing Server that you can install on a Windows 2003 or Windows 2008 domain controller machine.</span></span> <span data-ttu-id="4cf2c-111">Dieser Dienst ermöglicht den Betrieb von Windows 2000-Clients in einem Domänen integrierten Modus mit jedem Message Queuing Server, der auf Windows 2003/2008-Computern installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-111">This service allows Windows 2000 clients to operate in a domain-integrated mode with any Message Queuing server installed on Windows 2003/2008 machines.</span></span> <span data-ttu-id="4cf2c-112">MSMQ-Clients, die unter Windows XP aufwärts betrieben werden, benötigen diesen Dienst nicht.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-112">MSMQ Clients operating on Windows XP upwards do not need this service.</span></span>

### <a name="manifestation-of-impact"></a><span data-ttu-id="4cf2c-113">Erscheinung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="4cf2c-113">Manifestation of Impact</span></span>

<span data-ttu-id="4cf2c-114">Diese Änderung wirkt sich auf Windows 2000 aus, wenn Sie in einer Windows 7-Domäne interagiert, in der alle Domänen Controller Windows Server 2008 R2 sind.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-114">This change impacts Windows 2000 when interoperating in a Windows 7 domain where all domain controllers are Windows Server 2008 R2.</span></span> <span data-ttu-id="4cf2c-115">Wenn ein Kunde ein Upgrade auf die Windows 7-Domäne durchführt, können die vorhandenen MSMQ-Anwendungen auf allen Windows 2000-Computern in der Domäne nicht in einem Domänen integrierten Modus ausgeführt werden, es sei denn, diese Clients führen ein Upgrade auf eine höhere Windows-Version durch.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-115">If a customer upgrades to the Windows 7 domain, the existing MSMQ applications on any Windows 2000 machines in the domain will not be able to operate in a domain-integrated mode unless these clients upgrade to a higher Windows version.</span></span>

### <a name="mitigation"></a><span data-ttu-id="4cf2c-116">Minderung</span><span class="sxs-lookup"><span data-stu-id="4cf2c-116">Mitigation</span></span>

<span data-ttu-id="4cf2c-117">Benutzer mit Windows 2000-Client Computern in einer Windows 7-Domäne können einen Windows 2003/2008-Domänen Controller in der Domäne konfigurieren und den MSMQ Windows 2000-Client Unterstützungsdienst auf diesem Domänen Controller installieren.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-117">Users who have Windows 2000 Client machines on a Windows 7 domain can configure a Windows 2003/2008 domain controller in the domain and install the MSMQ Windows 2000 Client Support Service on this domain controller.</span></span>

### <a name="leveraging-feature-capabilities"></a><span data-ttu-id="4cf2c-118">Nutzen von Featurefunktionen</span><span class="sxs-lookup"><span data-stu-id="4cf2c-118">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="4cf2c-119">Benutzer mit Windows 2000-Client Computern, auf denen MSMQ ausgeführt wird, sollten auf eine höhere Windows-Version aktualisieren, um die Active Directory basierte Implementierung des MSMQ-Servers zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-119">Users who have Windows 2000 Client machines running MSMQ should upgrade to a higher Windows version in order to take advantage of the Active Directory-based implementation of the MSMQ Server.</span></span>

### <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="4cf2c-120">Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="4cf2c-120">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="4cf2c-121">Benutzer mit Windows 2000-Client Computern, auf denen MSMQ in einer Windows 7-Domäne mit einem oder mehreren untergeordneten Domänen Controllern ausgeführt wird, sollten überprüfen, ob Ihre Anwendungen in dieser gemischten Domäne funktionsfähig sind.</span><span class="sxs-lookup"><span data-stu-id="4cf2c-121">Users who have Windows 2000 Client machines running MSMQ on a Windows 7 domain with one or more down-level domain controllers should verify that their applications are functional on this mixed domain.</span></span>

 

 



