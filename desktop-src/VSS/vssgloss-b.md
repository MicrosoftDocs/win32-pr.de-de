---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d7d9c8bf-993f-469c-aea1-5d86ca856690
title: B (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f20bbe9f858066d7fca09a3f263aa618c79c4174664b9a4e0994c900fb81c75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998050"
---
# <a name="b-volume-shadow-copy-service"></a>B (Volumeschattenkopie-Dienst)

[A](vssgloss-a.md) B [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) T [U](vssgloss-t.md) [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_back_end_level_applications"></span><span id="BASE.VSSGLOSS_BACK_END_LEVEL_APPLICATIONS"></span>**Back-End-Anwendungen**
</dt> <dd>

Gibt den Punkt an, an dem ein Writer über ein Einfrieren durch VSS benachrichtigt wird. Writer, die als Back-End-Anwendungen initialisiert werden, werden benachrichtigt, nachdem Writer als Anwendungen auf Front-End-Ebene initialisiert wurden, und vor denen, die als Anwendungen auf Systemebene initialisiert wurden. Siehe auch [*Anwendungsebene,*](vssgloss-a.md) [*Front-End-Anwendungen,*](vssgloss-f.md) [*Anwendungen auf Systemebene,*](vssgloss-s.md) [*Writer*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_backupcomplete_event"></span><span id="BASE.VSSGLOSS_BACKUPCOMPLETE_EVENT"></span>**BackupComplete-Ereignis**
</dt> <dd>

Ein VSS-Ereignis, das angibt, dass eine VSS-Sicherung abgeschlossen wurde. Auf dieses Ereignis sollte im normalen Betrieb ein BackupShutdown-Ereignis folgen. Siehe auch *BackupShutdown-Ereignis*.

</dd> <dt>

<span id="base.vssgloss_backup_components_document"></span><span id="BASE.VSSGLOSS_BACKUP_COMPONENTS_DOCUMENT"></span>**Dokument zu Sicherungskomponenten**
</dt> <dd>

Ein XML-Dokument, das von einem Anfordernden (mithilfe der **IVssBackupComponents-Schnittstelle)** während der Einrichtung eines Wiederherstellungs- oder Sicherungsvorgang erstellt wird. Das Sicherungskomponentendokument enthält eine Liste der Komponenten, die von mindestens einem Writer, der an einem Sicherungs- oder Wiederherstellungsvorgang beteiligt ist, explizit hinzugefügt wurden. Es enthält keine implizit enthaltenen Komponenteninformationen. Ein Writer-Metadatendokument enthält nur Writer-Komponenten, die an einer Sicherung beteiligt sein können.

Ein Sicherungskomponentendokument kann auf dem Datenträger gespeichert werden. Siehe auch [*explizite Komponenteneinschluss,*](vssgloss-e.md) [*implizite Komponenteneinschluss*](vssgloss-i.md).

</dd> <dt>

<span id="base.vssgloss_backup_set"></span><span id="BASE.VSSGLOSS_BACKUP_SET"></span>**Sicherungssatz**
</dt> <dd>

Die zu sichernden Dateien. Sie enthält Dateien, die durch die Aufnahme in eine Komponente ausgewählt wurden, die durch include-Anweisungen auf Writerebene angegeben sind, und nicht die Dateien, die explizit eingeschlossen wurden.

</dd> <dt>

<span id="base.vssgloss_backupshutdown_event"></span><span id="BASE.VSSGLOSS_BACKUPSHUTDOWN_EVENT"></span>**BackupShutdown-Ereignis**
</dt> <dd>

Ein VSS-Ereignis, das angibt, dass eine kompatible Sicherungsanwendung heruntergefahren wurde. Normalerweise wird diesem Ereignis ein BackupComplete-Ereignis voran gestellt. Wenn eine Sicherung jedoch unerwartet beendet wird, kann dieses Ereignis ohne vorheriges BackupComplete-Ereignis generiert werden. Siehe auch *BackupComplete-Ereignis.*

</dd> <dt>

<span id="base.vssgloss_backup_stamp"></span><span id="BASE.VSSGLOSS_BACKUP_STAMP"></span>**Sicherungsstempel**
</dt> <dd>

Eine Zeichenfolge, die Informationen darüber enthält, wann eine Sicherung stattgefunden hat. VSS legt keine Einschränkungen für das Format dieser Zeichenfolge fest, außer dass es für alle Writerinstanzen einer bestimmten Klasse verständlich ist. Sie kann Zeit- und Datumsinformationen, logische Sequenznummern oder andere Informationen enthalten, die es einem Writer derselben Klasse ermöglichen, zu bestimmen, wann die letzte Sicherung stattgefunden hat.

</dd> </dl>

 

 



