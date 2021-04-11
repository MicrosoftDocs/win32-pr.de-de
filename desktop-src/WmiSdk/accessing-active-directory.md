---
description: Active Directory ist der Verzeichnisdienst für Windows und ist die Grundlage für verteilte Windows-Netzwerke.
ms.assetid: e7569754-87c3-4a18-bfed-a03a32a2ee22
ms.tgt_platform: multiple
title: Zugreifen auf Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbad433f1f189d68c8a7ab2f312cbb678b15ee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217969"
---
# <a name="accessing-active-directory"></a><span data-ttu-id="b4724-103">Zugreifen auf Active Directory</span><span class="sxs-lookup"><span data-stu-id="b4724-103">Accessing Active Directory</span></span>

<span data-ttu-id="b4724-104">Active Directory ist der Verzeichnisdienst für Windows und ist die Grundlage für verteilte Windows-Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="b4724-104">Active Directory is the directory service for Windows and is the foundation of Windows distributed networks.</span></span> <span data-ttu-id="b4724-105">Sie können Active Directory verwenden, um Objekte in einer Computernetzwerk Domäne wie z. b. Benutzer, Sicherheitsrichtlinien, Drucker, verteilte Komponenten und andere Ressourcen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="b4724-105">You can use Active Directory to locate objects in a computer network domain, such as users, security policies, printers, distributed components, and other resources.</span></span> <span data-ttu-id="b4724-106">Der Name Active Directory verweist sowohl auf den Verzeichnisdienst als auch auf das Verzeichnis selbst.</span><span class="sxs-lookup"><span data-stu-id="b4724-106">The name Active Directory refers both to the directory service and the directory itself.</span></span>

> [!Note]  
> <span data-ttu-id="b4724-107">Weitere Informationen zur Unterstützung und Installation dieser Komponente auf einem bestimmten Betriebssystem finden Sie unter [Betriebssystem Verfügbarkeit von WMI-Komponenten](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="b4724-107">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

<span data-ttu-id="b4724-108">Windows macht Active Directory über WMI zugänglich, indem eine Reihe von Verweisen auf alle Klassen und Objekte erstellt werden, die in Active Directory enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b4724-108">Windows makes Active Directory accessible through WMI by creating a set of references to every class and object contained in Active Directory.</span></span> <span data-ttu-id="b4724-109">Durch den Zugriff auf den Verzeichnisdienst Anbieter über WMI können Sie WMI-fähige Anwendungen erstellen, die auf die umfangreichen Informationen zugreifen können, die in Active Directory enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b4724-109">By accessing the Directory Services provider through WMI, you can create WMI-enabled applications that can access the wealth of information contained in Active Directory.</span></span>

<span data-ttu-id="b4724-110">Mit diesen Schnittstellen können Sie folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="b4724-110">With these interfaces, you can:</span></span>

-   <span data-ttu-id="b4724-111">Abrufen von Klassen und Instanzen.</span><span class="sxs-lookup"><span data-stu-id="b4724-111">Retrieve classes and instances.</span></span>
-   <span data-ttu-id="b4724-112">Auflisten von Klassen und Instanzen.</span><span class="sxs-lookup"><span data-stu-id="b4724-112">Enumerate classes and instances.</span></span>
-   <span data-ttu-id="b4724-113">Erstellen Sie neue Instanzen.</span><span class="sxs-lookup"><span data-stu-id="b4724-113">Create new instances.</span></span>
-   <span data-ttu-id="b4724-114">Ändern vorhandener Instanzen.</span><span class="sxs-lookup"><span data-stu-id="b4724-114">Modify existing instances.</span></span>
-   <span data-ttu-id="b4724-115">Löschen Sie vorhandene Instanzen.</span><span class="sxs-lookup"><span data-stu-id="b4724-115">Delete existing instances.</span></span>
-   <span data-ttu-id="b4724-116">Abfrage Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b4724-116">Query Active Directory.</span></span>

<span data-ttu-id="b4724-117">Die folgenden Themen unterstützen Sie bei der Verwendung von Active Directory mit WMI:</span><span class="sxs-lookup"><span data-stu-id="b4724-117">The following topics can assist you in using Active Directory with WMI:</span></span>

-   [<span data-ttu-id="b4724-118">Verwenden der richtigen Active Directory Syntax</span><span class="sxs-lookup"><span data-stu-id="b4724-118">Using the Proper Active Directory Syntax</span></span>](using-the-proper-active-directory-syntax.md)
-   [<span data-ttu-id="b4724-119">Zuordnung von Active Directory zu WMI</span><span class="sxs-lookup"><span data-stu-id="b4724-119">Mapping Active Directory to WMI</span></span>](mapping-active-directory-to-wmi.md)

 

 



