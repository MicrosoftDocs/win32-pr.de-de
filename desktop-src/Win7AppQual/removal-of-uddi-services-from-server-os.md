---
description: Entfernen von UDDI-Diensten aus dem Serverbetriebssystem
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Entfernen von UDDI-Diensten aus dem Serverbetriebssystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 960a4063d990a3b2cdac45cd933a1e7dfef41f88
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116328"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a><span data-ttu-id="1b34f-103">Entfernen von UDDI-Diensten aus dem Serverbetriebssystem</span><span class="sxs-lookup"><span data-stu-id="1b34f-103">Removal of UDDI Services from Server Operating System</span></span>

## <a name="affected-platform"></a><span data-ttu-id="1b34f-104">Betroffene Plattform</span><span class="sxs-lookup"><span data-stu-id="1b34f-104">Affected Platform</span></span>

<span data-ttu-id="1b34f-105">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1b34f-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="1b34f-106">Auswirkungen auf Das Feature</span><span class="sxs-lookup"><span data-stu-id="1b34f-106">Feature Impact</span></span>

<span data-ttu-id="1b34f-107">**Schweregrad –** Mittel</span><span class="sxs-lookup"><span data-stu-id="1b34f-107">**Severity** - Medium</span></span>  
<span data-ttu-id="1b34f-108">**Häufigkeit** : Niedrig</span><span class="sxs-lookup"><span data-stu-id="1b34f-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="1b34f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b34f-109">Description</span></span>

<span data-ttu-id="1b34f-110">Microsoft hat die Serverrolle UDDI -Dienste (Universelle Beschreibung, Ermittlung und Integration) aus Windows Server 2008 R2 entfernt.</span><span class="sxs-lookup"><span data-stu-id="1b34f-110">Microsoft has removed the UDDI (Universal Description, Discovery, and Integration) Services server role from Windows Server 2008 R2.</span></span> <span data-ttu-id="1b34f-111">Zukünftige Releases von UDDI Services werden Teil des Microsoft BizTalk-Produkts sein.</span><span class="sxs-lookup"><span data-stu-id="1b34f-111">Future releases of UDDI Services will be part of the Microsoft BizTalk product.</span></span> <span data-ttu-id="1b34f-112">Diese Neuausrichtung und Konsolidierung des Produkts positioniert Microsoft, um den Markt der dienstorientierten Architektur (SERVICE-Oriented Architecture, SOA) besser bedienen zu können.</span><span class="sxs-lookup"><span data-stu-id="1b34f-112">This product realignment and consolidation positions Microsoft to better serve the services-oriented architecture (SOA) market.</span></span>

<span data-ttu-id="1b34f-113">Das erste Release von UDDI-Diensten nach Windows Server 2008 wird mit DEN STANDARDS von UDDI v3.0 konform sein.</span><span class="sxs-lookup"><span data-stu-id="1b34f-113">The first post-Windows Server 2008 release of UDDI Services will be UDDI v3.0 standards compliant.</span></span> <span data-ttu-id="1b34f-114">Es wird als Teil des BizTalk Server 2009-Release geliefert.</span><span class="sxs-lookup"><span data-stu-id="1b34f-114">It will ship as part of the BizTalk Server 2009 release.</span></span> <span data-ttu-id="1b34f-115">Um unsere Verpflichtung zur Bereitstellung einer zufriedenstellenden Benutzererfahrung zu erfüllen, bieten wir ein UDDI Services v3-Installationspaket für Windows Server 2008 R2 an.</span><span class="sxs-lookup"><span data-stu-id="1b34f-115">To meet our commitment to provide a satisfactory user experience, we will offer a UDDI Services v3 installation package for Windows Server 2008 R2.</span></span>

## <a name="manifestation"></a><span data-ttu-id="1b34f-116">Manifestation</span><span class="sxs-lookup"><span data-stu-id="1b34f-116">Manifestation</span></span>

<span data-ttu-id="1b34f-117">Das Vorhandensein früherer Versionen von UDDI Services-Komponenten im System blockiert ein Upgrade auf Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1b34f-117">The presence of previous versions of UDDI Services components on the system blocks an upgrade to Windows Server 2008 R2.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="1b34f-118">Entschärfung der Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="1b34f-118">Mitigation of Impact</span></span>

<span data-ttu-id="1b34f-119">Benutzer, die eine UDDI Services-Website von Windows Server 2003 oder Windows Server 2008 bereitgestellt haben, können die Server, auf denen die UDDI-Dienste ausgeführt werden, nicht auf Windows Server 2008 R2 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1b34f-119">Users who have deployed a UDDI Services site from Windows Server 2003 or Windows Server 2008 can choose not to upgrade the servers running the UDDI Services to Windows Server 2008 R2.</span></span> <span data-ttu-id="1b34f-120">Sie können die UDDI-Dienste auch in dedizierte Windows Server 2003- oder Windows Server 2008-Felder verschieben, wenn sie die aktuellen UDDI-Dienste aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="1b34f-120">They can also move the UDDI Services to dedicated Windows Server 2003 or Windows Server 2008 boxes if they have to upgrade the current UDDI Services boxes.</span></span>

## <a name="solution"></a><span data-ttu-id="1b34f-121">Lösung</span><span class="sxs-lookup"><span data-stu-id="1b34f-121">Solution</span></span>

<span data-ttu-id="1b34f-122">Die empfohlene Lösung besteht darin, UDDI Services v3.0 von BizTalk Server 2009 auf einem Windows Server 2008 R2-Computer bereitzustellen und dann den alten Standort zum neuen Standort zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="1b34f-122">The recommended solution is to deploy UDDI Services v3.0 from BizTalk Server 2009 onto a Windows Server 2008 R2 machine, and then to migrate the old site to the new site.</span></span> <span data-ttu-id="1b34f-123">UDDI Services v3.0 bietet Abwärtskompatibilität mit UDDI Services 2.0, sodass alle Anwendungen, die UDDI-Dienste verwenden, davon nicht betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="1b34f-123">UDDI Services v3.0 provides backward compatibility with UDDI Services 2.0, so any applications that are using UDDI Services will be unaffected.</span></span>

<span data-ttu-id="1b34f-124">Gehen Sie hierzu folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="1b34f-124">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="1b34f-125">Richten Sie einen neuen UDDI Services v3.0-Standort auf einem Computer ein, der bereits mit Windows Server 2008 R2 geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="1b34f-125">Set up a new UDDI Services v3.0 site on a machine already loaded with Windows Server 2008 R2.</span></span> <span data-ttu-id="1b34f-126">(Hinweis: In einem verteilten Setup kann ein UDDI v3.0-Standort aus mehr als einem Windows Server 2008 R2-Computer bestehen.)</span><span class="sxs-lookup"><span data-stu-id="1b34f-126">(Note: In a distributed setup, a UDDI v3.0 site can consist of more than one Windows Server 2008 R2 machines.)</span></span>
2.  <span data-ttu-id="1b34f-127">Verwenden Sie das UDDI-Datenmigrationstool, um die Daten aus der alten UDDI Services-Datenbank zur neuen Datenbank zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="1b34f-127">Use the UDDI data migration tool to migrate the data from the old UDDI Services database to the new database.</span></span>
3.  <span data-ttu-id="1b34f-128">Sichern Sie die alte UDDI Services-Datenbank, um die Rollbackfunktion sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="1b34f-128">Back up the old UDDI Services database to ensure rollback capability.</span></span>
4.  <span data-ttu-id="1b34f-129">Deinstallieren Sie die alte UDDI Services-Software, und aktualisieren Sie diese Felder auf Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1b34f-129">Uninstall the old UDDI Services software and then upgrade those boxes to Windows Server 2008 R2.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="1b34f-130">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1b34f-130">Links to Other Resources</span></span>

-   [<span data-ttu-id="1b34f-131">Microsoft UDDI Services-Website</span><span class="sxs-lookup"><span data-stu-id="1b34f-131">Microsoft UDDI Services website</span></span>](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [<span data-ttu-id="1b34f-132">UDDI-Spezifikationen</span><span class="sxs-lookup"><span data-stu-id="1b34f-132">UDDI specifications</span></span>](http://uddi.xml.org/specification)
-   [<span data-ttu-id="1b34f-133">UDDI Services v3.0 download for Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1b34f-133">UDDI Services v3.0 download for Windows Server 2008 R2</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



