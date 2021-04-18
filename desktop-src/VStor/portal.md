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
# <a name="span-idvhdportalspanvirtual-disk"></a><span id="vhd.portal"></span>Virtueller Datenträger

## <a name="span-idpurposespanpurpose"></a><span id="purpose"></span>Zweck

Das Format der virtuellen Festplatte (VHD) ist eine öffentlich verfügbare Abbild Format Spezifikation, die eine virtuelle Festplatte angibt, die in einer einzelnen Datei gekapselt ist Ein Beispiel für die Verwendung von VHD-Dateien ist das [Hyper-V-](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) Feature in Windows Server 2008, Virtual Server und Windows Virtual PC. Diese Produkte verwenden VHDs, um das Windows-Betriebssystem Abbild zu enthalten, das von einem virtuellen Computer als Systemstart Datenträger verwendet wird.

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span id="developer_audience_heading"></span>Entwicklergruppe

Das Microsoft Windows Software Development Kit (SDK) integriert systemeigene VHD-Unterstützung für die Arbeit mit VHDs und erleichtert Entwicklern und Administratoren die Erstellung, Verwaltung und Bereitstellung von Windows-Abbildern in VHDs mithilfe der Platform-API-Unterstützung oder der Verwaltungs Tools. Es ist nicht erforderlich, separate Anwendungen zu installieren oder einen Parser für den VHD-Format zu implementieren, um diese Vorgänge zu aktivieren. Diese APIs ermöglichen die generische Verwendung von VHDs unabhängig von anderen Virtualisierungstechnologien.

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span id="run_time_requirements_heading"></span>Laufzeitanforderungen

VHD wird unter Windows 7 und Windows Server 2008 R2 unterstützt.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>In diesem Abschnitt

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Thema</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="about-vhd.md">Informationen zu VHD</a></p></td>
<td><p>Beschreibt das VHD-Format mit Tipps und Vorschlägen zur API-Verwendung.</p></td>
</tr>
<tr class="even">
<td><p><a href="vhd-reference.md">VHD-Referenz</a></p></td>
<td><p>Beschreibt die VHD-API-Funktionen,-Strukturen und-Enumerationen.</p></td>
</tr>
</tbody>
</table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Verwandte Themen

[Dienst für virtuelle Datenträger](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
