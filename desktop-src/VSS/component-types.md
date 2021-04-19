---
description: Komponenten geben die Art der Daten an, die Sie durch einen Typ darstellen.
ms.assetid: 19d785d5-09a7-48b9-a0a2-eca3049d67fe
title: Komponenten Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f89355b4b26090b7d43f9753c086b4ccc79df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352359"
---
# <a name="component-types"></a><span data-ttu-id="68b52-103">Komponenten Typen</span><span class="sxs-lookup"><span data-stu-id="68b52-103">Component Types</span></span>

<span data-ttu-id="68b52-104">Komponenten geben die Art der Daten an, die Sie durch einen Typ darstellen.</span><span class="sxs-lookup"><span data-stu-id="68b52-104">Components indicate the sort of data they represent through a type.</span></span>

<span data-ttu-id="68b52-105">Derzeit sind Komponenten Typen (siehe [**VSS \_ - \_ Komponententyp**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) auf Folgendes beschränkt:</span><span class="sxs-lookup"><span data-stu-id="68b52-105">Currently, component types (see [**VSS\_COMPONENT\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_type)) are limited to the following:</span></span>

-   <span data-ttu-id="68b52-106">Datenbankkomponenten</span><span class="sxs-lookup"><span data-stu-id="68b52-106">Database components</span></span>
-   <span data-ttu-id="68b52-107">Dateigruppen</span><span class="sxs-lookup"><span data-stu-id="68b52-107">File groups</span></span>

<span data-ttu-id="68b52-108">Implementierungs Informationen zum Festlegen von Komponenten Typen finden Sie unter [Definition von Komponenten durch Writer](definition-of-components-by-writers.md).</span><span class="sxs-lookup"><span data-stu-id="68b52-108">For implementation information about setting component types, see [Definition of Components by Writers](definition-of-components-by-writers.md).</span></span>

<span data-ttu-id="68b52-109">Writer verfügen über eine Typisierung, die ihre Verwendung angibt (siehe [**VSS- \_ \_ Quelltyp**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)). Dies kann wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="68b52-109">Writers have a data typing that indicates their usage (see [**VSS\_SOURCE\_TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type)), which can be the following:</span></span>

-   <span data-ttu-id="68b52-110">Eine transaktionale Datenbank (z. b. ein SQL Server)</span><span class="sxs-lookup"><span data-stu-id="68b52-110">A transactional database (such as an SQL server)</span></span>
-   <span data-ttu-id="68b52-111">Eine nicht transaktionale Datenbank (z. b. ein Tabellen-Client)</span><span class="sxs-lookup"><span data-stu-id="68b52-111">A nontransactional database (such as a spreadsheet client)</span></span>
-   <span data-ttu-id="68b52-112">Datei Gruppe (sonstige)</span><span class="sxs-lookup"><span data-stu-id="68b52-112">File group (other)</span></span>

<span data-ttu-id="68b52-113">Wenn Sie einen Komponententyp als Datenbank angeben, kann der Inhalt leichter identifiziert werden, und es wird eine separate Verarbeitung von Protokoll-und Datendateien ermöglicht (Weitere Informationen finden Sie unter [**ivsskreateschreitermetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) und [**ivssexaminewrite Metadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) ). und erzwingt eine größere Sorgfalt in der Dateiauswahl, indem weder eine rekursive Dateiauswahl noch ein [*Alternativer Pfad*](vssgloss-a.md) verwendet wird (siehe [**ivsskreateschreitermetadata:: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) und [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)).</span><span class="sxs-lookup"><span data-stu-id="68b52-113">Specifying a component type as database allows for easier identification of its content, allows for separate handling of log and data files (see [**IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) and [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) for details), and enforces greater rigor in file selection by not allowing either recursive file selection or using an [*alternate path*](vssgloss-a.md) (see [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) and [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)).</span></span>

<span data-ttu-id="68b52-114">Wenn eine Dateigruppen Komponente andererseits nicht weiß, welche Daten Sie enthält, haben Sie mehr Freiheit, wie Dateien eingefügt werden, da Sie rekursive Spezifikationen und alternative Pfade verwenden können.</span><span class="sxs-lookup"><span data-stu-id="68b52-114">With a file group component, on the other hand, at the price of not knowing what data it contains, you have greater freedom about how files are inserted, because you can use recursive specification and alternate paths.</span></span>

<span data-ttu-id="68b52-115">In Zukunft können zusätzliche Komponenten Typen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="68b52-115">Additional component types may be added in the future.</span></span>

 

 



