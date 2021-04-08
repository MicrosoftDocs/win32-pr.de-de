---
description: Ein appcontainer wird implementiert, indem dem Prozess Token neue Informationen hinzugefügt werden, wobei seaccesscheck () so geändert wird, dass alle veralteten, nicht geänderten Zugriffs Steuerungs Listen (ACL-Objekte) Zugriffs Anforderungen von appcontainer-Prozessen standardmäßig blockieren, sowie für appcontainers verfügbare reacl-Objekte.
ms.assetid: C70A2F8C-27CB-4298-AA31-8F5099616625
title: Implementieren eines appcontainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a6fc4c8d807d6a45f27f4f7a79d69ceb97edeb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867811"
---
# <a name="implementing-an-appcontainer"></a><span data-ttu-id="e4ad2-103">Implementieren eines appcontainer</span><span class="sxs-lookup"><span data-stu-id="e4ad2-103">Implementing an AppContainer</span></span>

<span data-ttu-id="e4ad2-104">Ein appcontainer wird implementiert, indem dem Prozess Token neue Informationen hinzugefügt werden, wobei [**seaccesscheck ()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) so geändert wird, dass alle veralteten, nicht geänderten Zugriffs Steuerungs Listen (ACL-Objekte) Zugriffs Anforderungen von appcontainer-Prozessen standardmäßig blockieren, sowie für appcontainers verfügbare reacl-Objekte.</span><span class="sxs-lookup"><span data-stu-id="e4ad2-104">An AppContainer is implemented by adding new information to the process token, changing [**SeAccessCheck()**](/windows-hardware/drivers/ddi/content/wdm/nf-wdm-seaccesscheck) so that all legacy, unmodified access control list (ACL) objects block access requests from AppContainer processes by default, and re-ACL objects that should be available to AppContainers.</span></span>

## <a name="the-process"></a><span data-ttu-id="e4ad2-105">Der Prozess</span><span class="sxs-lookup"><span data-stu-id="e4ad2-105">The process</span></span>

<span data-ttu-id="e4ad2-106">Fügen Sie zunächst neue Informationen für das Prozess Token hinzu.</span><span class="sxs-lookup"><span data-stu-id="e4ad2-106">Begin by adding new information for the process token.</span></span> <span data-ttu-id="e4ad2-107">Ändern Sie dann **seaccesscheck ()** , damit alle veralteten, nicht geänderten ACLs standardmäßig Zugriffs Anforderungen von appcontainer-Prozessen blockieren.</span><span class="sxs-lookup"><span data-stu-id="e4ad2-107">Then change **SeAccessCheck()** so that all legacy, unmodified ACLs will block access requests from AppContainer processes by default.</span></span> <span data-ttu-id="e4ad2-108">Zum Schluss sollten Sie Ressourcen für die Ressourcen bereitstellungscontainer bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e4ad2-108">Finally, re-ACL resources that should be available to AppContainers</span></span>

<span data-ttu-id="e4ad2-109">Die appcontainer-sid ist ein beständiger eindeutiger Bezeichner für den appcontainer.</span><span class="sxs-lookup"><span data-stu-id="e4ad2-109">The AppContainer SID is a persistent unique identifier for the appcontainer.</span></span> <span data-ttu-id="e4ad2-110">Funktionen-SIDs gewähren Zugriff auf Gruppen von Ressourcen für Gruppen von appcontainers.</span><span class="sxs-lookup"><span data-stu-id="e4ad2-110">Capability SIDs grant access to groups of resources to groups of AppContainers.</span></span> <span data-ttu-id="e4ad2-111">Eine appcontainernumber ist ein vorübergehendes **DWORD** , mit dem zwischen appcontainers unterschieden werden kann.</span><span class="sxs-lookup"><span data-stu-id="e4ad2-111">An AppContainerNumber is a transient **DWORD** used to distinguish between AppContainers.</span></span> <span data-ttu-id="e4ad2-112">Es sollte jedoch nicht als Identität für den appcontainer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e4ad2-112">However, it should not be used as an identity for the AppContainer.</span></span>

<span data-ttu-id="e4ad2-113">Damit ein einzelner appcontainer auf eine Ressource zugreifen kann, fügen Sie seine appcontainersid der ACL für diese Ressource hinzu.</span><span class="sxs-lookup"><span data-stu-id="e4ad2-113">To allow a single AppContainer to access a resource, add its AppContainerSID to the ACL for that resource.</span></span>

<span data-ttu-id="e4ad2-114">Fügen Sie alle zugehörigen appcontainersids der ACL für diese Ressource hinzu, damit mehrere bestimmte appcontainers auf eine Ressource zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="e4ad2-114">To allow several specific AppContainers to access a resource, add all of their AppContainerSIDs to the ACL for that resource.</span></span>

<span data-ttu-id="e4ad2-115">Erstellen Sie zum Verwalten von Berechtigungs Gruppen eine Funktions-sid (GUID), und legen Sie diese Funktions-sid für alle Ressourcen fest, die gewährt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e4ad2-115">To manage groups of permissions, create a Capability SID (a GUID) and put that Capability SID on all of the resources to be granted.</span></span> <span data-ttu-id="e4ad2-116">Fügen Sie dann die Funktions-sid zum Prozess Token hinzu.</span><span class="sxs-lookup"><span data-stu-id="e4ad2-116">Then add the Capability SID to your process token.</span></span>

<span data-ttu-id="e4ad2-117">Damit alle appcontainers auf eine Ressource zugreifen können, fügen Sie die SID **alle Anwendungspakete** der ACL für diese Ressource hinzu.</span><span class="sxs-lookup"><span data-stu-id="e4ad2-117">To allow all AppContainers to access a resource, add the **ALL APPLICATION PACKAGES** SID to the ACL for that resource.</span></span> <span data-ttu-id="e4ad2-118">Dies verhält sich wie ein Platzhalter.</span><span class="sxs-lookup"><span data-stu-id="e4ad2-118">This acts like a wildcard.</span></span>

<span data-ttu-id="e4ad2-119">Sowohl appcontainersid als auch capabilitysid unterstützen Zugriffs Masken in Access Control Einträgen (ACE).</span><span class="sxs-lookup"><span data-stu-id="e4ad2-119">Both AppContainerSID and CapabilitySID support access masks in Access Control Entries (ACE).</span></span> <span data-ttu-id="e4ad2-120">Legen Sie nach Bedarf fest.</span><span class="sxs-lookup"><span data-stu-id="e4ad2-120">Set as appropriate.</span></span>

 

 
