---
description: Festlegen von Administratorrechten für eine Partition
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Festlegen von Administratorrechten für eine Partition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421b37dd50fa21ee9cf146749ec00b0c91d98c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748280"
---
# <a name="setting-administrative-rights-for-a-partition"></a><span data-ttu-id="2a7c4-103">Festlegen von Administratorrechten für eine Partition</span><span class="sxs-lookup"><span data-stu-id="2a7c4-103">Setting Administrative Rights for a Partition</span></span>

<span data-ttu-id="2a7c4-104">Benutzer, denen die Administrator Rolle der com+-System Anwendung zugewiesen ist, können COM+-Partitionen erstellen, ändern und löschen.</span><span class="sxs-lookup"><span data-stu-id="2a7c4-104">Users assigned the Administrator role of the COM+ System Application are allowed to create, modify, and delete COM+ partitions.</span></span> <span data-ttu-id="2a7c4-105">Im Verwaltungs Programmkomponenten Dienste können den Benutzern administrative Rollen zugewiesen werden, indem der Ordner **Rollen** der com+-System Anwendung erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="2a7c4-105">Within the Component Services administrative tool, administrative roles can be assigned to users by expanding the **Roles** folder of the COM+ System Application.</span></span>

<span data-ttu-id="2a7c4-106">Ab Windows Server 2003 enthält die Authentifizierungsfunktion für die com+-System Anwendung den Wert eoac- \_ deaktivierte \_ AAA.</span><span class="sxs-lookup"><span data-stu-id="2a7c4-106">As of Windows Server 2003, the authentication capability for the COM+ System Application includes the value EOAC\_DISABLE\_AAA.</span></span> <span data-ttu-id="2a7c4-107">Dieser Wert, der Aktivierungen von Aktivierungen durch aktivierte Aktivierungen deaktiviert, wird beim Starten der System Anwendung im [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -Befehl verwendet.</span><span class="sxs-lookup"><span data-stu-id="2a7c4-107">This value, which disables activate-as-activator (AAA) activations, is used in the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) call when launching the System Application.</span></span> <span data-ttu-id="2a7c4-108">Wenn Sie die Authentifizierungsfunktion auf eoac \_ deaktivieren, \_ kann eine Anwendung, die unter einem privilegierten Konto (z. b. LocalSystem) ausgeführt wird, verhindern, dass Ihre Identität verwendet wird, um nicht vertrauenswürdige Komponenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="2a7c4-108">Setting the authentication capability to EOAC\_DISABLE\_AAA allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a7c4-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2a7c4-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a7c4-110">Sammeln von Partitions Metriken</span><span class="sxs-lookup"><span data-stu-id="2a7c4-110">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="2a7c4-111">Konfigurieren des Partitions Caches</span><span class="sxs-lookup"><span data-stu-id="2a7c4-111">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="2a7c4-112">Gruppieren von Anwendungen in Partitionen</span><span class="sxs-lookup"><span data-stu-id="2a7c4-112">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="2a7c4-113">Verwalten von lokalen Partitionen</span><span class="sxs-lookup"><span data-stu-id="2a7c4-113">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="2a7c4-114">Verwalten von Partitionen in Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a7c4-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> </dl>

 

 
