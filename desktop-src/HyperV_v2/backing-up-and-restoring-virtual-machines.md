---
description: Hyper-V verwendet die Volumeschattenkopie-Dienst (VSS) zum Sichern und Wiederherstellen virtueller Maschinen.
ms.assetid: 94C67F22-658D-49DD-9588-6BB4FCF7ADA9
title: Sichern und Wiederherstellen von virtuellen Computern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9cf6d5b80a4c7392fb38e893a4fafad3f90435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359054"
---
# <a name="backing-up-and-restoring-virtual-machines"></a>Sichern und Wiederherstellen von virtuellen Computern

Hyper-V verwendet die Volumeschattenkopie-Dienst (VSS) zum Sichern und Wiederherstellen virtueller Maschinen. Wenn die Sicherungsdienste (volumemomentaufnahme) im Gast Betriebssystem installiert sind, wird ein VSS-Anforderer installiert, mit dem VSS Writer im Gast Betriebssystem an der Sicherung der virtuellen Maschine teilnehmen können. Weitere Informationen finden Sie in den folgenden Abschnitten:

-   [Sichern der virtuellen Computer](#backing-up-the-virtual-machines)
-   [Wiederherstellen der virtuellen Computer](#restoring-the-virtual-machines)
-   [Failoverclustering und Hyper-V-VSS](#failover-clustering-and-hyper-v-vss)
-   [Details zum Hyper-V-VSS-Writer](#details-on-the-hyper-v-vss-writer)
-   [Zugehörige Themen](#related-topics)

## <a name="backing-up-the-virtual-machines"></a>Sichern der virtuellen Computer

Hyper-V verwendet einen von zwei Mechanismen, um jeden virtuellen Computer zu sichern. Der Standard Sicherungsmechanismus wird als "gespeicherte Zustands Methode" bezeichnet, bei der der virtuelle Computer während der Verarbeitung des prepareforsnapshot-Ereignisses in einen gespeicherten Zustand versetzt wird, Momentaufnahmen der entsprechenden Volumes entnommen werden und der virtuelle Computer während der Verarbeitung des PostSnapshot-Ereignisses in den vorherigen Zustand zurückversetzt wird.

Der andere Sicherungsmechanismus wird als "untergeordnete VM-Momentaufnahme"-Methode bezeichnet, die VSS innerhalb des untergeordneten virtuellen Computers verwendet, um an der Sicherung teilzunehmen. Damit die "untergeordnete VM-Momentaufnahme"-Methode unterstützt wird, müssen alle folgenden Bedingungen erfüllt sein:

-   Der Integrations Dienst für Sicherungen (volumemomentaufnahme) ist installiert und wird auf dem untergeordneten virtuellen Computer ausgeführt. Der Dienst Name lautet "Hyper-V-Volumeschattenkopie-Requestor".
-   Der untergeordnete virtuelle Computer muss sich im Status wird ausgeführt befinden.
-   Der Speicherort der Momentaufnahme Dateien für den virtuellen Computer ist auf das gleiche Volume im Host Betriebssystem als die VHD-Dateien für den virtuellen Computer festgelegt.
-   Alle Volumes auf dem untergeordneten virtuellen Computer sind Basis Datenträger, und es sind keine dynamischen Datenträger vorhanden.
-   Alle Datenträger auf dem untergeordneten virtuellen Computer müssen ein Dateisystem verwenden, das Momentaufnahmen unterstützt (z. b. NTFS).

Im Allgemeinen ist der Vorgang zum Sichern virtueller Computer identisch mit der Beschreibung unter [Übersicht über die Verarbeitung einer Sicherung unter VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss). Das einmalige Verhalten tritt auf, wenn der Hyper-v-VSS Writer (Teil des "Hyper-v-Verwaltungsdienst für virtuelle Computer") das prepareforsnapshot-Ereignis verarbeitet. Wenn die Sicherung mithilfe der Methode "untergeordneter VM-Momentaufnahme" durchgeführt wurde, wird eine zusätzliche Verarbeitung ausgeführt, Sie ist jedoch für den untergeordneten virtuellen Computer nicht sichtbar.

Im folgenden Verfahren wird beschrieben, wie Sie virtuelle Computer sichern.

**So sichern Sie virtuelle Computer**

1.  Wenn die Methode "gespeicherter Zustand" verwendet wird, wird die virtuelle Maschine für jeden virtuellen Computer in den Writer-Metadaten in einen gespeicherten Zustand versetzt. Bei virtuellen Computern, die die "untergeordnete VM-Momentaufnahme"-Methode verwenden, verarbeitet der Hyper-V-Volumeschattenkopie-Requestor-Dienst auf dem untergeordneten virtuellen Computer die Sicherung, wie in [Übersicht über die Verarbeitung einer Sicherung unter VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss)beschrieben Alle VSS-Ereignisse auf dem untergeordneten virtuellen Computer treten während der Verarbeitung des Host Betriebssystems des prepareforsnapshot-Ereignisses auf.
2.  Nachdem alle virtuellen Computer entweder in den gespeicherten Zustand versetzt wurden oder Momentaufnahmen erstellt wurden, wird die Hyper-V-VSS Writer vom prepareforsnapshot-Ereignis zurückgegeben. Die Hyper-V-VSS Writer werden während der Freeze-und der Thaw-Ereignisse nicht verarbeitet.
3.  Wenn der Hyper-v-VSS Writer das PostSnapshot-Ereignis verarbeitet, werden virtuelle Computer, die mithilfe der Methode "gespeicherter Zustand" gesichert wurden und von der Hyper-v-VSS Writer in einen gespeicherten Zustand versetzt wurden, in den Zustand zurückversetzt, in dem Sie sich vor dem Start der Sicherung befanden. Bei den virtuellen Computern, die mithilfe der Methode "untergeordneter VM-Momentaufnahme" gesichert wurden, wird für das Host Image der VHD-Dateien, für die die Momentaufnahmen erstellt wurden, ein Rollback auf die Momentaufnahme ausgeführt, die während der Verarbeitung des prepareforsnapshot-Ereignisses erstellt wurde. Diese Verarbeitung erfolgt unabhängig von den VSS-Writern auf den untergeordneten virtuellen Computern, sodass die erstellten Momentaufnahmen automatisch wiederherstellbar sein müssen. (**VSS \_ Volsnap \_ attr \_ No \_ AutoRecovery** ist nicht im Kontext festgelegt.)

Teil Sicherungen werden nicht unterstützt. Wenn von einem virtuellen Computer keine Momentaufnahme erstellt werden kann, werden keine virtuellen Computer gesichert.

> [!Note]  
> Pass-Through-und iSCSI-Datenträger sind für das Host Betriebssystem nicht sichtbar und werden daher nicht durch die Hyper-V-VSS Writer gesichert. Sicherungen dieser Volumes müssen vollständig auf dem virtuellen Computer durchgeführt werden.

 

## <a name="restoring-the-virtual-machines"></a>Wiederherstellen der virtuellen Computer

Die Wiederherstellung der virtuellen Maschinen erfolgt vollständig durch das Host Betriebssystem. die VSS-Writer auf den untergeordneten virtuellen Maschinen sind nicht beteiligt.

Im folgenden Verfahren wird beschrieben, wie virtuelle Computer wieder hergestellt werden.

**So stellen Sie virtuelle Maschinen wieder her**

1.  Während der Verarbeitung des vorab-Ereignisses wird das Hyper-V-VSS Writer ausgeschaltet, und alle virtuellen Computer, die wieder hergestellt werden sollen, werden gelöscht.
2.  Nachdem alle VSS-Writer das PreRestore-Ereignis verarbeitet haben, werden die Dateien wieder hergestellt.
3.  Während der Verarbeitung des postrestore-Ereignisses Ruft das Hyper-V-VSS Writer die [**IVssComponent:: getfilerestorestatus**](/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getfilerestorestatus) -Methode auf. Wenn die Rückgabe nicht **VSS \_ RS \_ all** ist, ruft das Hyper-V-VSS Writer die [**setschreiterfailure**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure) -Methode auf und gibt **false** aus der [**OnPostRestore**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore) -Methode zurück.
4.  Für jeden virtuellen Computer, der wieder hergestellt wurde, wird der virtuelle Computer vom Hyper-v-VSS Writer beim Hyper-v-Verwaltungsdienst registriert. Wenn die virtuelle Maschine an einem nicht standardmäßigen Speicherort wieder hergestellt wird, wird im Standard Speicherort, der mit diesem Speicherort verknüpft wird, eine symbolische Verknüpfung erstellt.
5.  Für jede wiederhergestellte VHD wird der Speicherort mit dem für diesen virtuellen Computer angegebenen virtuellen Computer verglichen. Wenn sich der Speicherort unterscheidet, wird die Konfiguration mit dem richtigen Speicherort aktualisiert.
6.  Die Netzwerkkonfiguration wird aktualisiert. Wenn die virtuellen Switches, mit denen der virtuelle Computer bei der Sicherung verbunden war, weiterhin beendet werden, werden neue Ports erstellt und mit dem virtuellen Computer verbunden.

## <a name="failover-clustering-and-hyper-v-vss"></a>Failoverclustering und Hyper-V-VSS

Die Hyper-V-VSS Writer berücksichtigt keine Überlegungen zu virtuellen Computern, die Teil eines Failoverclusters sind. Während der Sicherung und Wiederherstellung des gespeicherten Zustands wird die virtuelle Maschine in den gespeicherten Zustand versetzt oder vollständig gelöscht. Dies wird als Fehler des Clustering-Dienstanbieter angesehen und bewirkt, dass für die Anwendungen auf diesen Knoten ein Failover auf andere Knoten durchgeführt wird. Um dies bei Sicherungen mit dem Status "gespeichert" zu vermeiden, muss der Zustand der virtuellen Maschine mithilfe des Clustering-Dienstanbieter gespeichert werden. Um dies während einer Wiederherstellung zu vermeiden, müssen die Ressourcen auf dem virtuellen Computer offline geschaltet werden.

## <a name="details-on-the-hyper-v-vss-writer"></a>Details zum Hyper-V-VSS-Writer

Writer-Name: Microsoft Hyper-V VSS Writer

Writer-ID: 66841cd04ded-4l4b-8F 17-bd23f 8ddc3de

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Verarbeitung einer Sicherung unter VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss)
</dt> <dt>

[Übersicht über die Verarbeitung einer Wiederherstellung unter VSS](/windows/desktop/VSS/overview-of-processing-a-restore-under-vss)
</dt> </dl>

 

 
