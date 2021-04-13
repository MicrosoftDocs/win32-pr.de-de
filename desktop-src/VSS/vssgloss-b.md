---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d7d9c8bf-993f-469c-aea1-5d86ca856690
title: B (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20cabdfa5260f65d1176f6f1d12ac1d805b9dd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343569"
---
# <a name="b-volume-shadow-copy-service"></a>B (Volumeschattenkopie-Dienst)

[a](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**Anwendungen auf Back-End-Ebene**
</dt> <dd>

Gibt den Punkt an, an dem ein Writer über eine Sperre durch den VSS benachrichtigt wird. Writer, die als Back-End-Anwendungen initialisiert werden, werden benachrichtigt, nachdem Writer als Anwendungen auf Front-End-Ebene initialisiert wurden und bevor Sie als Anwendungen auf Systemebene initialisiert wurden. Weitere Informationen finden Sie auch auf [*Anwendungsebene*](vssgloss-a.md), [*Front-End-Anwendungen*](vssgloss-f.md), Anwendungen auf [*Systemebene*](vssgloss-s.md)und [*Writer*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**BackupComplete-Ereignis**
</dt> <dd>

Ein VSS-Ereignis, das angibt, dass eine VSS-Sicherung abgeschlossen wurde. Auf dieses Ereignis sollte ein BackupShutdown-Ereignis im normalen Betrieb folgen. Siehe auch *BackupShutdown-Ereignis*.

</dd> <dt>

<span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Dokument mit Sicherungs Komponenten**
</dt> <dd>

Ein XML-Dokument, das von einem Anforderer (mithilfe der **IVssBackupComponents** -Schnittstelle) im Rahmen der Einrichtung eines Wiederherstellungs-oder Sicherungs Vorgangs erstellt wurde. Das Sicherungskomponentendokument enthält eine Liste der Komponenten, die von mindestens einem Writer, der an einem Sicherungs- oder Wiederherstellungsvorgang beteiligt ist, explizit hinzugefügt wurden. Es enthält keine implizit enthaltenen Komponenteninformationen. Ein Writer-Metadatendokument enthält nur Writer-Komponenten, die an einer Sicherung beteiligt sein können.

Ein Sicherungs Komponenten Dokument kann auf einem Datenträger gespeichert werden. Siehe auch [*explizite Komponenten Einbindung*](vssgloss-e.md), [*impliziter Komponenten Einbindung*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**Sicherungs Satz**
</dt> <dd>

Die zu sichernden Dateien. Es umfasst Dateien, die durch einschließen in eine Komponente ausgewählt werden, und die von include-Anweisungen auf Writer-Ebene angegeben werden, weniger die explizit enthaltenen Dateien.

</dd> <dt>

<span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**BackupShutdown-Ereignis**
</dt> <dd>

Ein VSS-Ereignis, das angibt, dass eine kompatible Sicherungs Anwendung heruntergefahren wurde. Normalerweise wird diesem ein BackupComplete-Ereignis vorangestellt. Wenn eine Sicherung jedoch unerwartet beendet wird, kann dieses Ereignis ohne ein vorangestelltem BackupComplete-Ereignis generiert werden. Siehe auch *BackupComplete-Ereignis*.

</dd> <dt>

<span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**Sicherungs Stempel**
</dt> <dd>

Eine Zeichenfolge, die Informationen zu dem Zeitpunkt enthält, zu dem eine Sicherung stattfindet. VSS legt keine Einschränkung für das Format dieser Zeichenfolge fest, mit dem Unterschied, dass es für alle Writer-Instanzen einer bestimmten Klasse verständlich ist. Sie enthält möglicherweise Zeit-und Datumsinformationen, logische Sequenznummern oder andere Informationen, die es einem Writer der gleichen Klasse ermöglichen, zu bestimmen, wann die letzte Sicherung stattfindet.

</dd> </dl>

 

 



