---
description: Das Format der virtuellen Festplatte (VHD) ist eine öffentlich verfügbare Abbild Format Spezifikation, die die Kapselung der Festplatte in einer einzelnen Datei ermöglicht, die vom Betriebssystem als virtueller Datenträger verwendet wird, und zwar auf die gleiche Weise wie physische Festplatten verwendet werden.
MS-HAID: vhd.about\_vhd
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Informationen zu VHD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ea37851360e70c1108e0715a47c77163c2c2fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751521"
---
# <a name="span-idvhdabout_vhdspanabout-vhd"></a><span id="vhd.about_vhd"></span>Informationen zu VHD

Das Format der virtuellen Festplatte (VHD) ist eine öffentlich verfügbare Abbild Format [Spezifikation](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc) , die die Kapselung der Festplatte in einer einzelnen Datei ermöglicht, die vom Betriebssystem als *virtueller* Datenträger verwendet wird, und zwar auf die gleiche Weise wie physische Festplatten verwendet werden. Diese virtuellen Datenträger sind in der Lage, Native Dateisysteme (NTFS, FAT, exFAT und UDFs) zu Hosting, während Standard-Datenträger-und Datei Vorgänge unterstützt werden. Die Unterstützung der VHD-API ermöglicht die Verwaltung der virtuellen Datenträger. Mit der VHD-API erstellte virtuelle Datenträger können als Start Datenträger fungieren.

Ein Beispiel für die Verwendung von VHD-Dateien ist das [Hyper-V-](https://www.microsoft.com/windowsserver2008/en/us/hyperv.aspx) Feature in Windows 7, Windows Server 2008, Virtual Server und Windows Virtual PC. Diese Produkte verwenden die VHD-API, um das Windows-Betriebssystem Image zu enthalten, das von einem virtuellen Computer als Systemstart Datenträger verwendet wird.

Das Microsoft Windows Software Development Kit (SDK) integriert systemeigene VHD-Unterstützung für die Arbeit mit virtuellen Datenträgern und erleichtert Entwicklern und Administratoren die Erstellung, Verwaltung und Bereitstellung von Windows-Images in VHD-Dateien mithilfe der Platform-API-Unterstützung oder der Verwaltungs Tools. Es ist nicht erforderlich, separate Anwendungen zu installieren oder einen Parser für den VHD-Format zu implementieren, um diese Vorgänge zu aktivieren. Diese APIs ermöglichen die generische Verwendung von virtuellen Datenträgern unabhängig von anderen Virtualisierungstechnologien.

## <a name="span-idterminologyspanspan-idterminologyspanspan-idterminologyspanterminology"></a><span id="Terminology"></span><span id="terminology"></span><span id="TERMINOLOGY"></span>Begriffs

Der Begriff " *Sicherungs Speicher* " wird verwendet, um auf die physische Datei zu verweisen, die auf der eigentlichen Festplatte vorhanden ist. Der Sicherungs Speicher wird durch eine *VHD-Abbild Datei* dargestellt.

Die Begriffe " *Dynamic*", " *erweiterbare*" und " *Sparse* " werden häufig austauschbar verwendet, wenn Sie auf dynamisch erweiterbare virtuelle Datenträger verweisen. Bei der VHD-Technologie sind diese Begriffe identisch.

## <a name="span-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanspan-idvhd_system_features_overviewspanvhd-system-features-overview"></a><span id="VHD_System_Features_Overview"></span><span id="vhd_system_features_overview"></span><span id="VHD_SYSTEM_FEATURES_OVERVIEW"></span>Übersicht über die VHD-System Funktionen

Das folgende Diagramm enthält eine Übersicht über die VHD-Features und deren Beziehungen.

![VHD-Blockdiagramm](images/vhd.png)

Im folgenden finden Sie eine Zusammenfassung der zuvor beschriebenen Features.

Native Windows-APIs im Benutzermodus:

-   VirtDisk.dll-allgemeine Bibliothek für VHD-Verwaltungs-APIs.

Domänenspezifische Verwaltungs-Wrapper für den Benutzermodus:

-   [VDS-VHD-APIs](/windows/desktop/VDS/about-vds) : VDS-Objektmodell-Wrapper für die VHD-Windows-APIs.

Kernelmodustreiber:

-   Der Enumerator für virtuelle Laufwerke mit VDrvRoot.sys Stamm.
-   FsDepends.sys-die Verwaltung von Volumeabhängigkeiten.
-   Vhdmp.sys-VHD-Parser und Abhängigkeits Eigenschaften Anbieter.

Die SDK-Dokumentation in diesem Abschnitt befasst sich mit den nativen Windows-VHD-APIs im Benutzermodus.

## <a name="span-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanspan-idvirtual_disk_typesspanvirtual-disk-types"></a><span id="Virtual_Disk_Types"></span><span id="virtual_disk_types"></span><span id="VIRTUAL_DISK_TYPES"></span>Virtuelle Datenträger Typen

Es gibt Überlegungen zur Verwendung von virtuellen Datenträgern und zu den verfügbaren Typen von virtuellen Datenträgern:

-   **Korrigiert**– die VHD-Abbild Datei wird im Sicherungs Speicher für die maximal angeforderte Größe vorab zugeordnet.
-   **Erweiterbare**– auch als "dynamisch", "dynamisch erweiterbar" und "geringer Dichte" bezeichnet, verwendet die VHD-Abbild Datei nur so viel Speicherplatz wie erforderlich, um die eigentlichen Daten zu speichern, die der virtuelle Datenträger zurzeit enthält. Wenn Sie diese Art von virtuellem Datenträger erstellen, testet die VHD-API auf dem physischen Datenträger auf der Grundlage der maximal angeforderten Größe keinen freien Speicherplatz. Daher ist es möglich, einen dynamischen virtuellen Datenträger mit einer maximalen Größe zu erstellen, die größer ist als der verfügbare freie Speicherplatz auf dem physischen Datenträger. Weitere Informationen finden Sie unter [**expandvirtualdisk**](/windows/win32/api/virtdisk/nf-virtdisk-expandvirtualdisk).
    **Hinweis**  Die maximale Größe einer dynamischen virtuellen Festplatte beträgt 2.040 GB.

     

-   **Differenzierung**– ein übergeordneter virtueller Datenträger wird als Grundlage für diesen Typ verwendet, wobei alle nachfolgenden Schreibvorgänge auf den virtuellen Datenträger als Unterschiede zur neuen differenzierenden VHD-Abbild Datei und die übergeordnete VHD-Abbild Datei nicht geändert werden. Wenn Sie z. b. einen virtuellen Datenträger für das Systemstart-Betriebssystem als übergeordnetes Element installieren und den differenzierenden virtuellen Datenträger als aktuellen virtuellen Datenträger festlegen, der vom System verwendet werden soll, verbleibt das Betriebssystem auf dem übergeordneten virtuellen Datenträger in seinem ursprünglichen Zustand für die schnelle Wiederherstellung oder das schnelle Erstellen von Start Abbildern basierend auf zusätzlichen differenzierenden virtuellen Datenträgern Weitere Informationen finden Sie unter [**mergevirtualdisk**](/windows/win32/api/virtdisk/nf-virtdisk-mergevirtualdisk).
    **Hinweis**  Die maximale Größe einer differenzierenden virtuellen Festplatte beträgt 2.040 GB.

     

Alle virtuellen Datenträger Typen haben eine Mindestgröße von 3 MB.

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Verwandte Themen

[Informationen zu VDS](/windows/desktop/VDS/about-vds)

[VHD-Referenz](vhd-reference.md)

[Format Spezifikation des virtuellen Festplatten Abbilds](https://download.microsoft.com/download/f/f/e/ffef50a5-07dd-4cf8-aaa3-442c0673a029/Virtual%20Hard%20Disk%20Format%20Spec_10_18_06.doc)

 

 
