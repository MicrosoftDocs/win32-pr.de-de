---
title: Remote Datendienst entfernt
description: Remote Data Service-Serverkomponenten werden in Windows 8 entfernt
ms.assetid: 53ECB92C-8868-4A1A-82BD-4ADE75F7BB59
keywords:
- RDS-Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6588b029fe37f1312c709be168fd695bdc5738
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "103949183"
---
# <a name="remote-data-service-server-components-are-removed-in-windows-8"></a><span data-ttu-id="b4722-104">Remote Data Service-Serverkomponenten werden in Windows 8 entfernt</span><span class="sxs-lookup"><span data-stu-id="b4722-104">Remote data service server components are removed in Windows 8</span></span>

## <a name="platforms"></a><span data-ttu-id="b4722-105">Plattformen</span><span class="sxs-lookup"><span data-stu-id="b4722-105">Platforms</span></span>

 <span data-ttu-id="b4722-106">**Clients** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="b4722-106">**Clients** - Windows 8</span></span>  
<span data-ttu-id="b4722-107">**Server** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b4722-107">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="b4722-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4722-108">Description</span></span>

<span data-ttu-id="b4722-109">Der Remote Data Service (RDS)-Server ist in Windows 8 nicht verfügbar:</span><span class="sxs-lookup"><span data-stu-id="b4722-109">The remote data service (RDS) server is not available in Windows 8:</span></span>

-   <span data-ttu-id="b4722-110">Die Datei msadcf.dll, die das standardmäßige "Geschäftsobjekt" RDSServer. DataFactory hostet, wird entfernt, und die zugehörigen Dateien (msadcfr.dll, msadcfr.dll. MUI, Handler. reg und handsafe. reg) werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="b4722-110">File msadcf.dll, which hosts the default "business object" RDSServer.DataFactory, is removed, and its associated files (msadcfr.dll, msadcfr.dll.mui, handler.reg and handsafe.reg) are removed</span></span>
-   <span data-ttu-id="b4722-111">Die Datei msdfmap.dll, die der Standard Handler ist, wird entfernt, und die Datei msdfmap.ini wird entfernt.</span><span class="sxs-lookup"><span data-stu-id="b4722-111">File msdfmap.dll, which is the default Handler, is removed, and the file msdfmap.ini is removed</span></span>
-   <span data-ttu-id="b4722-112">Die Datei msadcs.dll, die ISAPI, wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="b4722-112">File msadcs.dll, the ISAPI, is removed</span></span>

## <a name="manifestation"></a><span data-ttu-id="b4722-113">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="b4722-113">Manifestation</span></span>

<span data-ttu-id="b4722-114">Kunden können keinen RDS-Server unter Windows 8 hosten.</span><span class="sxs-lookup"><span data-stu-id="b4722-114">Customers cannot host an RDS server on Windows 8.</span></span>

## <a name="mitigation"></a><span data-ttu-id="b4722-115">Minderung</span><span class="sxs-lookup"><span data-stu-id="b4722-115">Mitigation</span></span>

<span data-ttu-id="b4722-116">Kunden können Ihren RDS-Server auf einem Computer mit Windows 7 oder anderen untergeordneten Betriebssystemen aufbewahren.</span><span class="sxs-lookup"><span data-stu-id="b4722-116">Customers can keep their RDS server on a machine with Windows 7 or other down-level operating systems.</span></span>

## <a name="solution"></a><span data-ttu-id="b4722-117">Lösung</span><span class="sxs-lookup"><span data-stu-id="b4722-117">Solution</span></span>

<span data-ttu-id="b4722-118">Kunden können Ihren RDS-Server auf einem Computer mit Windows 7 oder anderen untergeordneten Betriebssystemen aufbewahren.</span><span class="sxs-lookup"><span data-stu-id="b4722-118">Customers can keep their RDS server on a machine with Windows 7 or other down-level operating systems.</span></span>

## <a name="resources"></a><span data-ttu-id="b4722-119">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b4722-119">Resources</span></span>

[<span data-ttu-id="b4722-120">Roadmap für Datenzugriffs Technologien</span><span class="sxs-lookup"><span data-stu-id="b4722-120">Data Access Technologies Roadmap</span></span>](/sql/connect/connect-history?view=sqlallproducts-allversions)

 

 