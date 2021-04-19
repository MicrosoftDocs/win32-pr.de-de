---
description: .
ms.assetid: 5ebc8c4c-acee-4658-8d36-30fbb17b1ef1
title: Entfernen der UDDI-Dienste aus dem Server Betriebssystem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7681167177b850ba44ac0fc26e019c7393008b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353930"
---
# <a name="removal-of-uddi-services-from-server-operating-system"></a><span data-ttu-id="b85f7-103">Entfernen der UDDI-Dienste aus dem Server Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="b85f7-103">Removal of UDDI Services from Server Operating System</span></span>

## <a name="affected-platform"></a><span data-ttu-id="b85f7-104">Betroffene Plattform</span><span class="sxs-lookup"><span data-stu-id="b85f7-104">Affected Platform</span></span>

<span data-ttu-id="b85f7-105">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b85f7-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="b85f7-106">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="b85f7-106">Feature Impact</span></span>

<span data-ttu-id="b85f7-107">**Schweregrad** -Mittel</span><span class="sxs-lookup"><span data-stu-id="b85f7-107">**Severity** - Medium</span></span>  
<span data-ttu-id="b85f7-108">**Häufigkeit** -niedrig</span><span class="sxs-lookup"><span data-stu-id="b85f7-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="b85f7-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b85f7-109">Description</span></span>

<span data-ttu-id="b85f7-110">Die UDDI-Server Rolle (universelle Beschreibung, Ermittlung und Integration) von Windows Server 2008 R2 wurde von Microsoft entfernt.</span><span class="sxs-lookup"><span data-stu-id="b85f7-110">Microsoft has removed the UDDI (Universal Description, Discovery, and Integration) Services server role from Windows Server 2008 R2.</span></span> <span data-ttu-id="b85f7-111">Zukünftige Versionen der UDDI-Dienste sind Teil des Microsoft BizTalk-Produkts.</span><span class="sxs-lookup"><span data-stu-id="b85f7-111">Future releases of UDDI Services will be part of the Microsoft BizTalk product.</span></span> <span data-ttu-id="b85f7-112">Durch die Neuausrichtung und Konsolidierung von Produkten wird Microsoft zur Verbesserung der Dienst orientierten Architektur (Service-Oriented Architecture, SOA).</span><span class="sxs-lookup"><span data-stu-id="b85f7-112">This product realignment and consolidation positions Microsoft to better serve the services-oriented architecture (SOA) market.</span></span>

<span data-ttu-id="b85f7-113">Die erste Version nach Windows Server 2008 der UDDI-Dienste wird mit UDDI v 3.0-Standards kompatibel sein.</span><span class="sxs-lookup"><span data-stu-id="b85f7-113">The first post-Windows Server 2008 release of UDDI Services will be UDDI v3.0 standards compliant.</span></span> <span data-ttu-id="b85f7-114">Sie wird als Teil der Version BizTalk Server 2009 ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="b85f7-114">It will ship as part of the BizTalk Server 2009 release.</span></span> <span data-ttu-id="b85f7-115">Um unsere Verpflichtung zu erfüllen, eine zufriedenstellende Benutzerfunktion bereitzustellen, bieten wir ein UDDI Services V3-Installationspaket für Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="b85f7-115">To meet our commitment to provide a satisfactory user experience, we will offer a UDDI Services v3 installation package for Windows Server 2008 R2.</span></span>

## <a name="manifestation"></a><span data-ttu-id="b85f7-116">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="b85f7-116">Manifestation</span></span>

<span data-ttu-id="b85f7-117">Wenn frühere Versionen der UDDI-Dienstekomponenten auf dem System vorhanden sind, wird ein Upgrade auf Windows Server 2008 R2 blockiert.</span><span class="sxs-lookup"><span data-stu-id="b85f7-117">The presence of previous versions of UDDI Services components on the system blocks an upgrade to Windows Server 2008 R2.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="b85f7-118">Minderung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="b85f7-118">Mitigation of Impact</span></span>

<span data-ttu-id="b85f7-119">Benutzer, die eine UDDI-Dienst Website von Windows Server 2003 oder Windows Server 2008 bereitgestellt haben, können die Server, auf denen die UDDI-Dienste ausgeführt werden, nicht auf Windows Server 2008 R2 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b85f7-119">Users who have deployed a UDDI Services site from Windows Server 2003 or Windows Server 2008 can choose not to upgrade the servers running the UDDI Services to Windows Server 2008 R2.</span></span> <span data-ttu-id="b85f7-120">Sie können die UDDI-Dienste auch in dedizierte Windows Server 2003-oder Windows Server 2008-Felder verschieben, wenn Sie die aktuellen UDDI-Dienst Felder aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="b85f7-120">They can also move the UDDI Services to dedicated Windows Server 2003 or Windows Server 2008 boxes if they have to upgrade the current UDDI Services boxes.</span></span>

## <a name="solution"></a><span data-ttu-id="b85f7-121">Lösung</span><span class="sxs-lookup"><span data-stu-id="b85f7-121">Solution</span></span>

<span data-ttu-id="b85f7-122">Die empfohlene Lösung besteht darin, die UDDI-Dienste v 3.0 von BizTalk Server 2009 auf einem Windows Server 2008 R2-Computer bereitzustellen und dann den alten Standort zum neuen Standort zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="b85f7-122">The recommended solution is to deploy UDDI Services v3.0 from BizTalk Server 2009 onto a Windows Server 2008 R2 machine, and then to migrate the old site to the new site.</span></span> <span data-ttu-id="b85f7-123">UDDI Services v 3.0 bietet Abwärtskompatibilität mit den UDDI-Diensten 2,0, sodass alle Anwendungen, die UDDI-Dienste verwenden, nicht betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="b85f7-123">UDDI Services v3.0 provides backward compatibility with UDDI Services 2.0, so any applications that are using UDDI Services will be unaffected.</span></span>

<span data-ttu-id="b85f7-124">Gehen Sie hierzu folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="b85f7-124">To do this, follow these steps:</span></span>

1.  <span data-ttu-id="b85f7-125">Richten Sie eine neue UDDI-Dienste v 3.0-Website auf einem Computer ein, der bereits mit Windows Server 2008 R2 geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="b85f7-125">Set up a new UDDI Services v3.0 site on a machine already loaded with Windows Server 2008 R2.</span></span> <span data-ttu-id="b85f7-126">(Hinweis: in einem verteilten Setup kann ein UDDI v 3.0-Standort aus mehr als einem Windows Server 2008 R2-Computer bestehen.)</span><span class="sxs-lookup"><span data-stu-id="b85f7-126">(Note: In a distributed setup, a UDDI v3.0 site can consist of more than one Windows Server 2008 R2 machines.)</span></span>
2.  <span data-ttu-id="b85f7-127">Verwenden Sie das Daten Migrationstool von UDDI zum Migrieren der Daten aus der alten Datenbank der UDDI-Dienste in die neue Datenbank.</span><span class="sxs-lookup"><span data-stu-id="b85f7-127">Use the UDDI data migration tool to migrate the data from the old UDDI Services database to the new database.</span></span>
3.  <span data-ttu-id="b85f7-128">Sichern Sie die alte Datenbank der UDDI-Dienste, um die Rollback-Funktion sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="b85f7-128">Back up the old UDDI Services database to ensure rollback capability.</span></span>
4.  <span data-ttu-id="b85f7-129">Deinstallieren Sie die alte UDDI-Dienst Software, und führen Sie ein Upgrade dieser Felder auf Windows Server 2008 R2 aus.</span><span class="sxs-lookup"><span data-stu-id="b85f7-129">Uninstall the old UDDI Services software and then upgrade those boxes to Windows Server 2008 R2.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="b85f7-130">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b85f7-130">Links to Other Resources</span></span>

-   [<span data-ttu-id="b85f7-131">Website für Microsoft UDDI-Dienste</span><span class="sxs-lookup"><span data-stu-id="b85f7-131">Microsoft UDDI Services website</span></span>](https://msdn.microsoft.com/biztalk/dd789428.aspx)
-   [<span data-ttu-id="b85f7-132">UDDI-Spezifikationen</span><span class="sxs-lookup"><span data-stu-id="b85f7-132">UDDI specifications</span></span>](http://uddi.xml.org/specification)
-   [<span data-ttu-id="b85f7-133">Download der UDDI-Dienste v 3.0 für Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b85f7-133">UDDI Services v3.0 download for Windows Server 2008 R2</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=e4761835-70f0-4e8d-96c5-64818d54e06e)

 

 



