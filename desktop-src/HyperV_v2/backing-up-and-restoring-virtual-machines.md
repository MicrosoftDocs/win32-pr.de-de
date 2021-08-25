---
description: Hyper-V verwendet die Volumeschattenkopie-Dienst (VSS) zum Sichern und Wiederherstellen virtueller Computer.
ms.assetid: 94C67F22-658D-49DD-9588-6BB4FCF7ADA9
title: Sichern und Wiederherstellen virtueller Computer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf5a0db5bf6956557c22445d5745dbaede03389cf6ead7467b32b65e76c59b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914040"
---
# <a name="backing-up-and-restoring-virtual-machines"></a>Sichern und Wiederherstellen virtueller Computer

Hyper-V verwendet die Volumeschattenkopie-Dienst (VSS) zum Sichern und Wiederherstellen virtueller Computer. Wenn die Integrationsdienste für die Sicherung (Volumemomentaufnahme) im Gastbetriebssystem installiert sind, wird ein VSS-Anfordernde installiert, der VSS Writern im Gastbetriebssystem die Teilnahme an der Sicherung des virtuellen Computers ermöglicht. Weitere Informationen finden Sie in den folgenden Abschnitten:

-   [Sichern der virtuellen Computer](#backing-up-the-virtual-machines)
-   [Wiederherstellen der virtuellen Computer](#restoring-the-virtual-machines)
-   [Failoverclustering und Hyper-V VSS](#failover-clustering-and-hyper-v-vss)
-   [Details zum Hyper-V VSS Writer](#details-on-the-hyper-v-vss-writer)
-   [Zugehörige Themen](#related-topics)

## <a name="backing-up-the-virtual-machines"></a>Sichern der virtuellen Computer

Hyper-V verwendet einen von zwei Mechanismen, um jeden virtuellen Computer zu sichern. Der Standardsicherungsmechanismus wird als "Saved State"-Methode bezeichnet, bei der der virtuelle Computer während der Verarbeitung des PrepareForSnapshot-Ereignisses in einen gespeicherten Zustand aufgenommen wird, Momentaufnahmen der entsprechenden Volumes erstellt werden und der virtuelle Computer während der Verarbeitung des PostSnapshot-Ereignisses in den vorherigen Zustand zurückverknappt wird.

Der andere Sicherungsmechanismus wird als "Child VM Snapshot"-Methode bezeichnet, bei der VSS auf dem untergeordneten virtuellen Computer verwendet wird, um an der Sicherung teilzunehmen. Damit die Methode "Momentaufnahme des untergeordneten virtuellen Computers" unterstützt wird, müssen alle folgenden Bedingungen erfüllt sein:

-   Der Integrationsdienst für die Sicherung (Volumemomentaufnahme) wird auf dem untergeordneten virtuellen Computer installiert und ausgeführt. Der Dienstname ist "Hyper-V Volume Shadow Copy Requestor".
-   Der untergeordnete virtuelle Computer muss sich im Ausgeführt-Zustand zustanden.
-   Der Speicherort der Momentaufnahmedatei für den virtuellen Computer ist auf das gleiche Volume im Hostbetriebssystem wie die VHD-Dateien für den virtuellen Computer festgelegt.
-   Alle Volumes auf dem untergeordneten virtuellen Computer sind Basisdatenträger, und es sind keine dynamischen Datenträger vorhanden.
-   Alle Datenträger auf dem untergeordneten virtuellen Computer müssen ein Dateisystem verwenden, das Momentaufnahmen unterstützt (z. B. NTFS).

Im Allgemeinen ist der Prozess zum Sichern virtueller Computer identisch mit dem unter Übersicht über die Verarbeitung einer Sicherung unter [VSS beschriebenen Prozess.](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss) Das eindeutige Verhalten tritt auf, wenn der Hyper-V VSS Writer (Teil des Diensts "Hyper-V Virtual Machine Management") das PrepareForSnapshot-Ereignis verarbeitet. Wenn die Sicherung mit der Methode "Momentaufnahme des untergeordneten virtuellen Computers" durchgeführt wurde, erfolgt eine zusätzliche Verarbeitung, die jedoch für den untergeordneten virtuellen Computer nicht sichtbar ist.

Im folgenden Verfahren wird das Sichern virtueller Computer beschrieben.

**So sichern Sie virtuelle Computer**

1.  Wenn für jeden virtuellen Computer in den Writermetadaten die "Saved State"-Methode verwendet wird, wird der virtuelle Computer in einen gespeicherten Zustand übertzustand. Bei virtuellen Computern, die die Methode "Momentaufnahme einer untergeordneten VM" verwenden, verarbeitet der Hyper-V-Volumeschattenkopie-Anforderungsdienst auf dem untergeordneten virtuellen Computer die Sicherung wie unter Übersicht über die Verarbeitung einer Sicherung unter [VSS ausführlich erläutert.](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss) Alle VSS-Ereignisse auf dem untergeordneten virtuellen Computer treten während der Hostbetriebssystemverarbeitung des PrepareForSnapshot-Ereignisses auf.
2.  Nachdem alle virtuellen Computer entweder in den gespeicherten Zustand aufgenommen wurden oder Momentaufnahmen erstellt wurden, kehrt der Hyper-V VSS Writer vom PrepareForSnapshot-Ereignis zurück. Während der Freeze- und Thaw-Ereignisse wird vom Hyper-V VSS Writer keine Verarbeitung durchgeführt.
3.  Wenn der Hyper-V VSS Writer das PostSnapshot-Ereignis verarbeitet, werden virtuelle Computer, die mit der Methode "Saved State" gesichert wurden und vom Hyper-V VSS Writer in einen gespeicherten Zustand überführen, in den Zustand zurückgegeben, in dem sie sich vor dem Start der Sicherung befinden. Für die virtuellen Computer, die mit der Methode "Momentaufnahme des untergeordneten virtuellen Computers" sichern wurden, wird für das Hostimage der VHD-Dateien, auf denen die Momentaufnahmen erstellt wurden, ein Rollback auf die Momentaufnahme ausgeführt, die während der Verarbeitung des PrepareForSnapshot-Ereignisses erstellt wurde. Diese Verarbeitung erfolgt unabhängig von den VSS Writern auf den untergeordneten virtuellen Computern, sodass die erstellten Momentaufnahmen automatisch wiederhergestellt werden können. (**VSS \_ VOLSNAP \_ ATTR \_ NO \_ AUTORECOVERY** ist nicht im Kontext festgelegt.)

Teilsicherungen werden nicht unterstützt. Wenn ein virtueller Computer keine Momentaufnahme erstellen kann, werden keine virtuellen Computer sichern.

> [!Note]  
> Pass-Through- und iSCSI-Datenträger sind für das Hostbetriebssystem nicht sichtbar und werden daher nicht durch den Hyper-V VSS Writer sichern. Sicherungen dieser Volumes müssen vollständig auf dem virtuellen Computer erfolgen.

 

## <a name="restoring-the-virtual-machines"></a>Wiederherstellen der virtuellen Computer

Die Wiederherstellung der virtuellen Computer erfolgt vollständig über das Hostbetriebssystem. Die VSS Writer auf den untergeordneten virtuellen Computern sind nicht beteiligt.

Im folgenden Verfahren wird beschrieben, wie Virtuelle Computer wiederhergestellt werden.

**So stellen Sie virtuelle Computer wieder**

1.  Während der Verarbeitung des PreRestore-Ereignisses wird der Hyper-V VSS Writer deaktiviert und löscht alle virtuellen Computer, die wiederhergestellt werden sollen.
2.  Nachdem alle VSS Writer das PreRestore-Ereignis verarbeitet haben, werden die Dateien wiederhergestellt.
3.  Während der Verarbeitung des PostRestore-Ereignisses ruft der Hyper-V VSS Writer die [**IVssComponent::GetFileRestoreStatus-Methode**](/windows/desktop/api/vswriter/nf-vswriter-ivsscomponent-getfilerestorestatus) auf. Wenn die Rückgabe nicht **VSS \_ RS \_ ALL** ist, ruft der Hyper-V VSS Writer die [**SetWriterFailure-Methode**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-setwriterfailure) auf und gibt **False** von der [**OnPostRestore-Methode**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-onpostrestore) zurück.
4.  Für jeden wiederhergestellten virtuellen Computer registriert der Hyper-V VSS Writer den virtuellen Computer beim Hyper-V-Verwaltungsdienst. Wenn der virtuelle Computer an einem nicht standardmäßigen Speicherort wiederhergestellt wird, wird eine symbolische Verknüpfung am Standardspeicherort erstellt, der mit diesem Standort verlinkt wird.
5.  Für jede wiederhergestellte VHD wird der Speicherort mit der für diesen virtuellen Computer angegebenen verglichen. Wenn der Standort anders ist, wird die Konfiguration mit dem richtigen Speicherort aktualisiert.
6.  Die Netzwerkkonfiguration wird aktualisiert. Wenn die virtuellen Switches, mit denen der virtuelle Computer beim Sichern verbunden war, weiterhin beendet werden, werden neue Ports erstellt und mit dem virtuellen Computer verbunden.

## <a name="failover-clustering-and-hyper-v-vss"></a>Failoverclustering und Hyper-V VSS

Der Hyper-V VSS Writer berücksichtigt keine virtuellen Computer, die Teil eines Failoverclusters sind. Während der Sicherungen der "Saved State"-Methode und aller Wiederherstellungen wird der virtuelle Computer in den gespeicherten Zustand bzw. vollständig gelöscht. Dies wird vom Clusteringdienst als Fehler bezeichnet und dazu führen, dass für die Anwendungen auf diesen Knoten ein Failover auf andere Knoten ausgeführt wird. Um dies bei Sicherungen des gespeicherten Zustands zu vermeiden, muss der Status des virtuellen Computers mithilfe des Clusteringdiensts gespeichert werden. Um dies während einer Wiederherstellung zu vermeiden, müssen die Ressourcen auf dem virtuellen Computer offline geschaltet werden.

## <a name="details-on-the-hyper-v-vss-writer"></a>Details zum Hyper-V VSS Writer

Writername: Microsoft Hyper-V VSS Writer

Writer-ID: 66841cd4-6ded-4f4b-8f17-fd23f8ddc3de

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die Verarbeitung einer Sicherung unter VSS](/windows/desktop/VSS/overview-of-processing-a-backup-under-vss)
</dt> <dt>

[Übersicht über die Verarbeitung einer Wiederherstellung unter VSS](/windows/desktop/VSS/overview-of-processing-a-restore-under-vss)
</dt> </dl>

 

 
