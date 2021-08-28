---
description: Kapseln Sie die Festplatte in einer einzelnen Datei, um sie vom Betriebssystem als virtuellen Datenträger zu verwenden. Virtuelle Datenträger können als Startdatenträger fungieren und native Dateisysteme (NTFS, FAT, exFAT und UDFS) hosten und gleichzeitig Standarddatenträger- und Dateivorgänge unterstützen.
MS-HAID: vhd.portal
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Virtueller Datenträger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfa2d39ea786029e8be319d7affaa2214682ce05
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480986"
---
# <a name="span-idvhdportalspanvirtual-disk"></a><span id="vhd.portal"></span>Virtueller Datenträger

## <a name="span-idpurposespanpurpose"></a><span id="purpose"></span>Zweck

Das Format der virtuellen Festplatte (Virtual Hard Disk, VHD) ist eine öffentlich verfügbare Imageformatspezifikation, die eine virtuelle Festplatte angibt, die in einer einzelnen Datei gekapselt ist und native Dateisysteme hosten kann, während Standard-Datenträger- und Dateivorgänge unterstützt werden. Ein Beispiel für die Verwendung von VHD-Dateien ist das [Hyper-V-Feature](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) in Windows Server 2008, Virtual Server und Windows Virtual PC. Diese Produkte verwenden VHDs, um das Windows Betriebssystemimage zu enthalten, das von einem virtuellen Computer als Systemstartdatenträger verwendet wird.

## <a name="span-iddeveloper_audience_headingspandeveloper-audience"></a><span id="developer_audience_heading"></span>Entwicklergruppe

Das Microsoft Windows Software Development Kit (SDK) integriert native VHD-Unterstützung für die Arbeit mit VHDs und erleichtert Entwicklern und Administratoren das Erstellen, Verwalten und Bereitstellen Windows Images auf VHDs mithilfe der Api-Unterstützung oder verwaltungstools der Plattform. Es ist nicht erforderlich, separate Anwendungen zu installieren oder einen VHD-Formatparser zu implementieren, um diese Vorgänge zu aktivieren. Diese APIs ermöglichen die generische Verwendung von VHDs, unabhängig von anderen Virtualisierungstechnologien.

## <a name="span-idrun_time_requirements_headingspanrun-time-requirements"></a><span id="run_time_requirements_heading"></span>Laufzeitanforderungen

VHD wird auf Windows 7 und Windows Server 2008 R2 unterstützt.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>In diesem Abschnitt


| Thema | BESCHREIBUNG | 
|-------|-------------|
| <p><a href="about-vhd.md">Informationen zu VHD</a></p> | <p>Beschreibt das VHD-Format mit Tipps und Vorschlägen zur API-Nutzung.</p> | 
| <p><a href="vhd-reference.md">VHD-Referenz</a></p> | <p>Beschreibt die VHD-API-Funktionen, -Strukturen und -Enumerationen.</p> | 


 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Verwandte Themen

[Dienst für virtuelle Datenträger](/windows/desktop/VDS/virtual-disk-service-portal)

 

 
