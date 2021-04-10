---
title: Com+-Dienste werden veröffentlicht.
description: COM-basierte Dienste stellen einen Anwendungs Proxy in Form eines Windows Installer (MSI)-Pakets bereit.
ms.assetid: 38200a22-bea5-4967-a51a-e777b34f299d
ms.tgt_platform: multiple
keywords:
- Com+-Dienste werden veröffentlicht.
- Active Directory, verwenden, Veröffentlichen eines Diensts, com+-Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9044b72b4a604a4d863315963cd097be67f6afce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036348"
---
# <a name="publishing-com-services"></a><span data-ttu-id="4844a-105">Com+-Dienste werden veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="4844a-105">Publishing COM+ Services</span></span>

<span data-ttu-id="4844a-106">COM-basierte Dienste stellen einen Anwendungs Proxy in Form eines Windows Installer (MSI)-Pakets bereit.</span><span class="sxs-lookup"><span data-stu-id="4844a-106">COM-based services provide an application-proxy in the form of a Windows installer (MSI) package.</span></span> <span data-ttu-id="4844a-107">Diese MSI-Datei enthält den zu verwendenden Servernamen und andere erforderliche Elemente, wie z. b. Proxy/Stub und Typbibliotheken, die für das Marshalling erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4844a-107">This .msi file contains the server name to be used and other required elements, such as proxy/stubs and type libraries required for marshalling.</span></span> <span data-ttu-id="4844a-108">Das Snap-in "Komponenten Dienste" generiert automatisch diese Anwendungs Proxys für com+-Server Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="4844a-108">The Component Services snap-in auto-generate these application proxies for COM+ Server applications.</span></span>

<span data-ttu-id="4844a-109">Die Anwendungs Proxys werden in Active Directory mithilfe des Gruppenrichtlinie-Editors in-Richtlinien Objekten veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="4844a-109">The application proxies are published into policy objects in Active Directory using the Group Policy Editor.</span></span> <span data-ttu-id="4844a-110">In der Client Anwendung ist kein spezieller Eingriff erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4844a-110">No special intervention is required in the client application.</span></span> <span data-ttu-id="4844a-111">Das Computer-/Benutzerkonto auf dem Client Computer muss sich in einer OE befinden, die für die Verwendung des Richtlinien Objekts konfiguriert ist, in dem die Anwendungs Proxys veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="4844a-111">The computer/user account on the client computer must be in an OU configured to use the policy object in which the application proxies are published.</span></span> <span data-ttu-id="4844a-112">Der com-Binder verwendet den Server automatisch mithilfe des Verzeichnisses, wenn der Client eine Instanz der betroffenen Objekte festlegt.</span><span class="sxs-lookup"><span data-stu-id="4844a-112">The COM binder automatically locates the server by means of the directory when the client establishes an instance of the objects concerned.</span></span>

 

 




