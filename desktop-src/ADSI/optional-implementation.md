---
title: Optionale Implementierung
description: Die folgenden Funktionen sind optional, werden jedoch empfohlen.
ms.assetid: 6123bdda-06cf-4b8b-b2a8-89882b6341b4
ms.tgt_platform: multiple
keywords:
- Optionaler Implementierungs-ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043b07f3a9bcfaef4bde8e95458d64828d4e46be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515458"
---
# <a name="optional-implementation"></a><span data-ttu-id="18d1d-104">Optionale Implementierung</span><span class="sxs-lookup"><span data-stu-id="18d1d-104">Optional Implementation</span></span>

<span data-ttu-id="18d1d-105">Die folgenden Funktionen sind optional, werden jedoch empfohlen:</span><span class="sxs-lookup"><span data-stu-id="18d1d-105">The following features are optional, but recommended:</span></span>

-   <span data-ttu-id="18d1d-106">Die [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle für nicht-Automatisierungs Clients.</span><span class="sxs-lookup"><span data-stu-id="18d1d-106">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface for non-Automation clients.</span></span> <span data-ttu-id="18d1d-107">Da der ADSI OLE DB-Anbieter **IDirectorySearch** verwendet, um Abfragen zu präsentieren und Ergebnisse aus dem zugrunde liegenden Verzeichnisdienst zu erfassen, ermöglichen Anbieter, die diese Schnittstelle implementieren, automatisch den Zugriff auf OLE DB Format Datenbanken, ohne dass zusätzliche Schnittstellen implementiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="18d1d-107">Because the ADSI OLE DB provider uses **IDirectorySearch** to present queries and collect results from the underlying directory service, providers that implement this interface automatically provide access to OLE DB style databases without having to implement any additional interfaces.</span></span>
-   <span data-ttu-id="18d1d-108">Die Schnittstellen [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)und [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) .</span><span class="sxs-lookup"><span data-stu-id="18d1d-108">The [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist), and [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) interfaces.</span></span> <span data-ttu-id="18d1d-109">Anbieter für Verzeichnisdienste, die die ACL-basierte Objektsicherheit unterstützen, werden empfohlen, diese zusätzlichen Features zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="18d1d-109">Providers for directory services that support ACL-based object security are encouraged to implement these additional features.</span></span>

 

 




