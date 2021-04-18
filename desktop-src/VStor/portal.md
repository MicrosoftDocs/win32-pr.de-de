---
description: Kapseln Sie die Festplatte in einer einzelnen Datei, die vom Betriebssystem als virtueller Datenträger verwendet werden soll. Virtuelle Datenträger können als Start Datenträger fungieren und systemeigene Dateisysteme (NTFS, FAT, exFAT und UDFs) hosten, bei denen standardmäßige Datenträger-und Datei Vorgänge unterstützt werden.
MS-HAID: vhd.portal
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Virtueller Datenträger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 044145f5d631b878b533bbd409fad5eda5b4863f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214612"
---
# <a name="span-idvhdportalspanvirtual-disk"></a><span data-ttu-id="ab728-104"><span id="vhd.portal"></span>Virtueller Datenträger</span><span class="sxs-lookup"><span data-stu-id="ab728-104"><span id="vhd.portal"></span>Virtual Disk</span></span>

## <a name="span-idpurposespanpurpose"></a><span data-ttu-id="ab728-105"><span id="purpose"></span>Zweck</span><span class="sxs-lookup"><span data-stu-id="ab728-105"><span id="purpose"></span>Purpose</span></span>

<span data-ttu-id="ab728-106">Das Format der virtuellen Festplatte (VHD) ist eine öffentlich verfügbare Abbild Format Spezifikation, die eine virtuelle Festplatte angibt, die in einer einzelnen Datei gekapselt ist</span><span class="sxs-lookup"><span data-stu-id="ab728-106">The Virtual Hard Disk (VHD) format is a publicly-available image format specification that specifies a virtual hard disk encapsulated in a single file, capable of hosting native file systems while supporting standard disk and file operations.</span></span> <span data-ttu-id="ab728-107">Ein Beispiel für die Verwendung von VHD-Dateien ist das [Hyper-V-](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) Feature in Windows Server 2008, Virtual Server und Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="ab728-107">An example of how VHD files are used is the [Hyper-V](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) feature in Windows Server 2008, Virtual Server, and Windows Virtual PC.</span></span> <span data-ttu-id="ab728-108">Diese Produkte verwenden VHDs, um das Windows-Betriebssystem Abbild zu enthalten, das von einem virtuellen Computer als Systemstart Datenträger verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ab728-108">These products use VHDs to contain the Windows operating system image utilized by a virtual machine as its system boot disk.</span></span>

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span data-ttu-id="ab728-109"><span id="developer_audience_heading"></span>Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="ab728-109"><span id="developer_audience_heading"></span>Developer audience</span></span>

<span data-ttu-id="ab728-110">Das Microsoft Windows Software Development Kit (SDK) integriert systemeigene VHD-Unterstützung für die Arbeit mit VHDs und erleichtert Entwicklern und Administratoren die Erstellung, Verwaltung und Bereitstellung von Windows-Abbildern in VHDs mithilfe der Platform-API-Unterstützung oder der Verwaltungs Tools.</span><span class="sxs-lookup"><span data-stu-id="ab728-110">The Microsoft Windows Software Development Kit (SDK) integrates Native VHD support for working with VHDs, making it easier for developers and administrators to create, manage, and deploy Windows images in VHDs using the platform API support or management tools.</span></span> <span data-ttu-id="ab728-111">Es ist nicht erforderlich, separate Anwendungen zu installieren oder einen Parser für den VHD-Format zu implementieren, um diese Vorgänge zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ab728-111">It is not necessary to install separate applications or implement a VHD format parser to enable these operations.</span></span> <span data-ttu-id="ab728-112">Diese APIs ermöglichen die generische Verwendung von VHDs unabhängig von anderen Virtualisierungstechnologien.</span><span class="sxs-lookup"><span data-stu-id="ab728-112">These APIs allow for generic use of VHDs independent of any other virtualization technologies.</span></span>

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span data-ttu-id="ab728-113"><span id="run_time_requirements_heading"></span>Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="ab728-113"><span id="run_time_requirements_heading"></span>Run-time requirements</span></span>

<span data-ttu-id="ab728-114">VHD wird unter Windows 7 und Windows Server 2008 R2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab728-114">VHD is supported on Windows 7 and Windows Server 2008 R2.</span></span>

## <a name="span-idin_this_sectionspanin-this-section"></a><span data-ttu-id="ab728-115"><span id="in_this_section"></span>In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ab728-115"><span id="in_this_section"></span>In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ab728-116">Thema</span><span class="sxs-lookup"><span data-stu-id="ab728-116">Topic</span></span></th>
<th><span data-ttu-id="ab728-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab728-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab728-118"><a href="about-vhd.md">Informationen zu VHD</a></span><span class="sxs-lookup"><span data-stu-id="ab728-118"><a href="about-vhd.md">About VHD</a></span></span></p></td>
<td><p><span data-ttu-id="ab728-119">Beschreibt das VHD-Format mit Tipps und Vorschlägen zur API-Verwendung.</span><span class="sxs-lookup"><span data-stu-id="ab728-119">Describes the VHD format with API usage tips and suggestions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab728-120"><a href="vhd-reference.md">VHD-Referenz</a></span><span class="sxs-lookup"><span data-stu-id="ab728-120"><a href="vhd-reference.md">VHD Reference</a></span></span></p></td>
<td><p><span data-ttu-id="ab728-121">Beschreibt die VHD-API-Funktionen,-Strukturen und-Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="ab728-121">Describes the VHD API functions, structures, and enumerations.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span data-ttu-id="ab728-122"><span id="related_topics"></span>Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="ab728-122"><span id="related_topics"></span>Related topics</span></span>

[<span data-ttu-id="ab728-123">Dienst für virtuelle Datenträger</span><span class="sxs-lookup"><span data-stu-id="ab728-123">Virtual Disk Service</span></span>](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
