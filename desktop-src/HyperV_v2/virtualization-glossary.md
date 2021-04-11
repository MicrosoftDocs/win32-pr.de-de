---
description: Glossar der Begriffe, die in der Dokumentation zum Windows Virtualization SDK verwendet werden.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 365D0295-EA0B-4B40-8272-DFF62B2A6F3D
title: Hyper-V-Glossar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: badb8fdfd25c4b7e11529778ab2cbd3c8cee5f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217810"
---
# <a name="hyper-v-glossary"></a>Hyper-V-Glossar

Dieses Thema enthält ein Glossar der Begriffe, die in der Dokumentation zum Windows Virtualization SDK verwendet werden.

<dl> <dt>

<span id="hyperv.virtualization_glossary_binding"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_BINDING"></span>**lichere**
</dt> <dd>

Ein Prozess, mit dem Software Dienste und Ebenen miteinander verknüpft werden. Wenn ein Netzwerkdienst installiert wird, werden die Bindungs Beziehungen und die Abhängigkeiten für die Dienste festgelegt.

</dd> <dt>

<span id="hyperv.virtualization_glossary_checkpoint"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_CHECKPOINT"></span>**Kal**
</dt> <dd>

Eine Momentaufnahme eines virtuellen Computers, der es einem Administrator ermöglicht, den Rollback des virtuellen Computers zum Zeitpunkt der Erstellung des Prüf Punkts wieder in seinen Zustand auszuführen.

</dd> <dt>

<span id="hyperv.virtualization_glossary_compact"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_COMPACT"></span>**theit**
</dt> <dd>

Um die Größe einer dynamisch erweiterbaren virtuellen Festplatte zu verringern, indem Sie nicht verwendeten Speicherplatz aus der VHD-Datei entfernen.

</dd> <dt>

<span id="hyperv.virtualization_glossary_dvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DVHD"></span>**differenzierende virtuelle Festplatte**
</dt> <dd>

Eine virtuelle Festplatte, auf der die Änderungen an einer zugeordneten übergeordneten virtuellen Festplatte gespeichert werden, um das übergeordnete Element intakt zu lassen. Der differenzierende Datenträger ist eine separate VHD-Datei, die mit der VHD-Datei des übergeordneten Datenträgers verknüpft ist. Änderungen werden auf der differenzierenden Festplatte weiterhin gesammelt, bis Sie mit dem übergeordneten Datenträger zusammengeführt werden.

</dd> <dt>

<span id="hyperv.virtualization_glossary_devhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_DEVHD"></span>**dynamisch erweiterbare virtuelle Festplatte**
</dt> <dd>

Eine virtuelle Festplatte, die bei jeder Änderung der Größe zunimmt. Diese Art virtueller Festplatte wird als 3-KB-VHD-Datei gestartet und kann so groß werden, wie die maximale Größe, die beim Erstellen der Datei angegeben wurde. Die einzige Möglichkeit, die Dateigröße zu reduzieren, besteht darin, die gelöschten Daten zu löschen und dann die virtuelle Festplatte zu komprimieren.

</dd> <dt>

<span id="hyperv.virtualization_glossary_fvhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_FVHD"></span>**virtuelle Festplatte mit fester Größe**
</dt> <dd>

Eine virtuelle Festplatte mit fester Größe, die festgelegt wird und für die beim Erstellen des Datenträgers der gesamte Speicherplatz zugewiesen wird. Die Größe des Datenträgers ändert sich nicht, wenn Daten hinzugefügt oder gelöscht werden.

</dd> <dt>

<span id="hyperv.virtualization_glossary_gen1vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN1VM"></span>**Virtueller Computer der Generation 1**
</dt> <dd>

Ein virtueller Computer (VM), der die gleiche virtuelle Hardware enthält, die in Hyper-V-Versionen vor Windows 8.1 und Windows Server 2012 R2 vorhanden ist.

</dd> <dt>

<span id="hyperv.virtualization_glossary_gen2vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GEN2VM"></span>**Virtueller Computer der Generation 2**
</dt> <dd>

Ein virtueller Computer (VM), der ein vereinfachtes virtuelles Hardware Modell enthält und UEFI-Firmware anstelle von BIOS verwendet. Auf diesem virtuellen Computer werden die meisten der emulierten Geräte entfernt, was die Komplexität der Verwaltung und die Angriffsfläche für Sicherheitsangriffe reduziert.

</dd> <dt>

<span id="hyperv.virtualization_glossary_guestos"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_GUESTOS"></span>**Gast Betriebssystem**
</dt> <dd>

Das auf der virtuellen Maschine ausgeführte Betriebssystem

</dd> <dt>

<span id="hyperv.virtualization_glossary_integration_services"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_INTEGRATION_SERVICES"></span>**Integration Services**
</dt> <dd>

Eine Auflistung der Dienste und Software Treiber, die die Leistung maximieren und eine bessere Benutzer Leistung innerhalb eines virtuellen Computers ermöglichen. Integration Services sind nur für unterstützte Gast Betriebssysteme verfügbar.

</dd> <dt>

<span id="hyperv.virtualization_glossary_kvp"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_KVP"></span>**Schlüssel-Wert-Paar**
</dt> <dd>

Ein Satz von Datenelementen, der einen eindeutigen Bezeichner enthält, der als Schlüssel bezeichnet wird, sowie einen Wert, der die eigentlichen Daten für den Schlüssel ist.

</dd> <dt>

<span id="hyperv.virtualization_glossary_physical_computer"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_PHYSICAL_COMPUTER"></span>**physischer Computer**
</dt> <dd>

Einen hardwarebasierten Computer im Gegensatz zu einer softwarebasierten virtuellen Maschine.

</dd> <dt>

<span id="hyperv.virtualization_glossary_saved_state"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_SAVED_STATE"></span>**gespeicherter Zustand**
</dt> <dd>

Eine Möglichkeit, eine virtuelle Maschine so zu speichern, dass Sie schnell fortgesetzt werden kann, ähnlich wie bei einem Laptop im Ruhezustand. Wenn Sie einen aktiven virtuellen Computer in einem gespeicherten Zustand platzieren, beenden Virtual Server und Hyper-V den virtuellen Computer, schreiben die Daten, die im Arbeitsspeicher vorhanden sind, in temporäre Dateien und beenden den Verbrauch von Systemressourcen. Beim Wiederherstellen einer virtuellen Maschine aus einem gespeicherten Zustand wird diese an die gleiche Bedingung zurückgegeben, in der Sie sich beim Speichern des Zustands befand.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vfd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VFD"></span>**virtuelle Diskette**
</dt> <dd>

Eine dateibasierte Version einer physischen Diskette. Eine virtuelle Diskette wird als Datei mit der Dateinamenerweiterung ". VFD" gespeichert.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vhd"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHD"></span>**virtuelle Festplatte**
</dt> <dd>

Das Speichermedium für eine virtuelle Maschine. Sie kann sich in einer beliebigen Speicher Topologie befinden, auf die das Host Betriebssystem zugreifen kann, einschließlich externer Geräte, Storage Area Networks und Network-Attached Storage. Die Dateinamenerweiterung ist ". VHD".

</dd> <dt>

<span id="hyperv.virtualization_glossary_vm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM"></span>**virtueller Computer**
</dt> <dd>

Ein in Software implementierter Computer in einem Computer. Eine virtuelle Maschine emuliert ein vollständiges Hardwaresystem vom Prozessor bis zur Netzwerkkarte in einer abgeschlossenen Softwareumgebung und ermöglicht so die parallele Ausführung von normalerweise inkompatiblen Betriebssystemen. Jedes untergeordnete Betriebssystem wird in einem eigenen virtuellen Computer für isolierte Software ausgeführt.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vm_config"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VM_CONFIG"></span>**Konfiguration der virtuellen Maschine**
</dt> <dd>

Die Konfiguration der Ressourcen, die einem virtuellen Computer zugewiesen sind. Beispiele hierfür sind Geräte wie Datenträger und Netzwerkadapter sowie Arbeitsspeicher und Prozessoren.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vmms"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMMS"></span>**Verwaltungsdienst für virtuelle Computer**
</dt> <dd>

Der Hyper-V-Dienst, der Verwaltungs Zugriff auf virtuelle Computer bereitstellt.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vmss"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VMSS"></span>**Momentaufnahme des virtuellen Computers**
</dt> <dd>

Eine dateibasierte Momentaufnahme des Zustands, der Datenträger Daten und der Konfiguration einer virtuellen Maschine zu einem bestimmten Zeitpunkt.

</dd> <dt>

<span id="hyperv.virtualization_glossary_virtual_network"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_NETWORK"></span>**virtuelles Netzwerk**
</dt> <dd>

Eine virtuelle Version eines physischen Netzwerk Schalters. ein virtuelles Netzwerk kann so konfiguriert werden, dass es für eine oder mehrere virtuelle Maschinen den Zugriff auf lokale oder externe Netzwerkressourcen bereitstellt.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vnm"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VNM"></span>**Virtual Network-Manager**
</dt> <dd>

Ein Hyper-V-Dienst zum Erstellen und Verwalten virtueller Netzwerke.

</dd> <dt>

<span id="hyperv.virtualization_glossary_virtual_switch"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VIRTUAL_SWITCH"></span>**virtueller Switch**
</dt> <dd>

Siehe virtuelles Netzwerk.

</dd> <dt>

<span id="hyperv.virtualization_glossary_vhdx_resize"></span><span id="HYPERV.VIRTUALIZATION_GLOSSARY_VHDX_RESIZE"></span>**Vhdx-Größe ändern**
</dt> <dd>

Der Vorgang, mit dem eine virtuelle Festplatte verkleinert oder erweitert wird.

</dd> </dl>

 

 



