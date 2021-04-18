---
description: Der Verzeichnisdienst Anbieter spiegelt Klassen und Instanzen von Active Directory in den WMI Lightweight Directory Access Protocol (LDAP)-Namespace.
ms.assetid: 0215b614-cb10-4195-837d-bf81d523c560
ms.tgt_platform: multiple
title: Zuordnung von Active Directory zu WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e0162f722eb8a053270ac2a8e75eaed4f1cd405
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351789"
---
# <a name="mapping-active-directory-to-wmi"></a><span data-ttu-id="98696-103">Zuordnung von Active Directory zu WMI</span><span class="sxs-lookup"><span data-stu-id="98696-103">Mapping Active Directory to WMI</span></span>

<span data-ttu-id="98696-104">Der Verzeichnisdienst Anbieter spiegelt Klassen und Instanzen von Active Directory in den WMI Lightweight Directory Access Protocol (LDAP)-Namespace.</span><span class="sxs-lookup"><span data-stu-id="98696-104">The Directory Services Provider mirrors classes and instances from Active Directory into the WMI Lightweight Directory Access Protocol (LDAP) namespace.</span></span> <span data-ttu-id="98696-105">Aufgrund grundlegender Unterschiede in den beiden Umgebungen können Sie nicht einfach die Active Directory Klassen und Instanzen umbenennen und hoffen, ordnungsgemäß auf diese Klassen und Instanzen in WMI zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="98696-105">Because of fundamental differences in the two environments, you cannot simply rename the Active Directory classes and instances and hope to properly access those classes and instances in WMI.</span></span> <span data-ttu-id="98696-106">Stattdessen befolgt der Verzeichnisdienst Anbieter Benennungs Regeln, um die Beziehungen beizubehalten, die zwischen den Active Directory-Klassen und-Instanzen bestehen.</span><span class="sxs-lookup"><span data-stu-id="98696-106">Instead, the Directory Services provider follows naming rules to preserve the relationships that exist between the Active Directory classes and instances.</span></span>

<span data-ttu-id="98696-107">Die folgenden Themen enthalten Informationen zum Mapping von Active Directory Klassen und Instanzen:</span><span class="sxs-lookup"><span data-stu-id="98696-107">The following topics provide information about mapping Active Directory classes and instances:</span></span>

-   [<span data-ttu-id="98696-108">Zuordnung von Active Directory Klassen</span><span class="sxs-lookup"><span data-stu-id="98696-108">Mapping Active Directory Classes</span></span>](mapping-active-directory-classes.md)
-   [<span data-ttu-id="98696-109">Zuordnung von Active Directory Instanzen</span><span class="sxs-lookup"><span data-stu-id="98696-109">Mapping Active Directory Instances</span></span>](mapping-active-directory-instances.md)

> [!Note]  
> <span data-ttu-id="98696-110">Weitere Informationen zur Unterstützung und Installation dieser Komponente auf einem bestimmten Betriebssystem finden Sie unter [Betriebssystem Verfügbarkeit von WMI-Komponenten](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="98696-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



