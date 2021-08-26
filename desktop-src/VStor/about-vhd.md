---
description: Das Format der virtuellen Festplatte (Virtual Hard Disk, VHD) ist eine öffentlich verfügbare Imageformatspezifikation, die die Kapselung der Festplatte in eine einzelne Datei zur Verwendung durch das Betriebssystem als virtuelle Festplatte auf die gleiche Weise ermöglicht, wie physische Festplatten verwendet werden.
MS-HAID: vhd.about\_vhd
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Informationen zu VHD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a79bd7695144811a1ec98f79e736760bbaddc8ef4b7460e55c5a66353a0b2ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865955"
---
# <a name="span-idvhdabout_vhdspanabout-vhd"></a><span id="vhd.about_vhd"></span>Informationen zur VHD

Das Format der virtuellen Festplatte (Virtual Hard Disk, VHD) ist eine öffentlich verfügbare [Imageformatspezifikation,](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) die die Kapselung der Festplatte in eine einzelne Datei zur Verwendung durch das Betriebssystem als *virtuelle Festplatte* auf die gleiche Weise ermöglicht, wie physische Festplatten verwendet werden. Diese virtuellen Datenträger können native Dateisysteme (NTFS, FAT, exFAT und UDFS) hosten und gleichzeitig Standarddatenträger- und Dateivorgänge unterstützen. Die VHD-API-Unterstützung ermöglicht die Verwaltung der virtuellen Datenträger. Virtuelle Datenträger, die mit der VHD-API erstellt wurden, können als Startdatenträger fungieren.

Ein Beispiel für die Verwendung von VHD-Dateien ist das [Hyper-V-Feature](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) in Windows 7, Windows Server 2008, Virtual Server und Windows Virtual PC. Diese Produkte verwenden die VHD-API, um das Windows Betriebssystemimage zu enthalten, das von einem virtuellen Computer als Systemstartdatenträger verwendet wird.

Das Microsoft Windows Software Development Kit (SDK) integriert native VHD-Unterstützung für die Arbeit mit virtuellen Datenträgern und erleichtert Entwicklern und Administratoren das Erstellen, Verwalten und Bereitstellen Windows Images in VHD-Dateien mithilfe der Plattform-API-Unterstützung oder verwaltungstools. Es ist nicht erforderlich, separate Anwendungen zu installieren oder einen VHD-Formatparser zu implementieren, um diese Vorgänge zu aktivieren. Diese APIs ermöglichen die generische Verwendung virtueller Datenträger unabhängig von anderen Virtualisierungstechnologien.

## <a name="span-idterminologyspanspan-idterminologyspanspan-idterminologyspanterminology"></a><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>Terminologie

Der Begriff *Sicherungsspeicher* wird verwendet, um auf die physische Datei zu verweisen, die auf der tatsächlichen Festplatte vorhanden ist. Der Sicherungsspeicher wird durch eine *VHD-Imagedatei* dargestellt.

Die Begriffe *dynamic,* *expandable* und *sparse* werden häufig austauschbar verwendet, wenn auf dynamisch erweiterbare virtuelle Datenträger verwiesen wird. Bei der VHD-Technologie sind diese Begriffe identisch.

## <a name="span-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanvhd-system-features-overview"></a><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>Übersicht über VHD-Systemfeatures

Das folgende Diagramm zeigt eine Übersicht über die VHD-Features und deren Beziehungen.

![vhd-Blockdiagramm](images/vhd.png)

Im Folgenden werden die zuvor beschriebenen Features zusammengefasst.

Nativ Windows-APIs im Benutzermodus:

-   VirtDisk.dll: Allgemeine Bibliothek für VHD-Verwaltungs-APIs.

Domänenspezifische Verwaltungswrapper im Benutzermodus:

-   [VDS-VHD-APIs:](/windows/desktop/VDS/about-vds) VDS-Objektmodellwrapper für die VHD-Windows-APIs.

Kernelmodustreiber:

-   VDrvRoot.sys: Enumerator des virtuellen Stammlaufwerks.
-   FsDepends.sys: Verwaltung geschachtelter Volumeabhängigkeiten.
-   Vhdmp.sys: VHD-Parser und Abhängigkeitseigenschaftenanbieter.

In der SDK-Dokumentation in diesem Abschnitt werden die nativen Windows VHD-APIs im Benutzermodus behandelt.

## <a name="span-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanvirtual-disk-types"></a><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>Virtuelle Datenträgertypen

Es gibt Überlegungen zur Verwendung virtueller Datenträger und zu den verfügbaren Arten von virtuellen Datenträgern:

-   **Behoben:** Die VHD-Imagedatei wird im Sicherungsspeicher für die angeforderte maximale Größe vorab zugeordnet.
-   **Erweiterbar**: Die VHD-Imagedatei wird auch als "dynamisch", "dynamisch erweiterbar" und "platzsparend" bezeichnet und verwendet nur so viel Speicherplatz im Sicherungsspeicher wie erforderlich, um die tatsächlichen Daten zu speichern, die der virtuelle Datenträger derzeit enthält. Beim Erstellen dieses virtuellen Datenträgertyps wird von der VHD-API basierend auf der angeforderten maximalen Größe kein freier Speicherplatz auf dem physischen Datenträger getestet. Daher ist es möglich, erfolgreich einen dynamischen virtuellen Datenträger mit einer maximalen Größe zu erstellen, die größer als der verfügbare freie Speicherplatz des physischen Datenträgers ist. Weitere Informationen finden Sie unter [**ExpandVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk).
    **Hinweis**  Die maximale Größe eines dynamischen virtuellen Datenträgers beträgt 2.040 GB.

     

-   **Differenzieren:** Ein übergeordneter virtueller Datenträger wird als Grundlage dieses Typs verwendet, wobei alle nachfolgenden Schreibvorgänge auf den virtuellen Datenträger als Unterschiede zur neuen differenzierenden VHD-Imagedatei geschrieben werden und die übergeordnete VHD-Imagedatei nicht geändert wird. Wenn Sie z. B. einen virtuellen Startbetriebssystem-Datenträger des Systems neu installieren als übergeordneten Datenträger haben und den differenzierenden virtuellen Datenträger als aktuellen virtuellen Datenträger für das Zu verwendende System festlegen, verbleibt das Betriebssystem auf dem übergeordneten virtuellen Datenträger im ursprünglichen Zustand, um eine schnelle Wiederherstellung oder das schnelle Erstellen weiterer Startimages basierend auf zusätzlichen differenzierenden virtuellen Datenträgern zu erhalten. Weitere Informationen finden Sie unter [**MergeVirtualDisk**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk).
    **Hinweis**  Die maximale Größe eines differenzierenden virtuellen Datenträgers beträgt 2.040 GB.

     

Alle Virtuellen Datenträgertypen haben eine Mindestgröße von 3 MB.

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Verwandte Themen

[Informationen zu VDS](/windows/desktop/VDS/about-vds)

[VHD-Referenz](vhd-reference.md)

[Spezifikation des Imageformats für virtuelle Festplatten](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc)

 

 
