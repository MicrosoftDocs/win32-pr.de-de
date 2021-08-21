---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44279c0e-17f4-4109-bc12-af9064cd321e
title: P (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3dbcf3f9d4938e407b82c58482cabab08156c3b9fabac6c1770ec20d0a40394
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121610"
---
# <a name="p-volume-shadow-copy-service"></a>P (Volumeschattenkopie-Dienst)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-f.md) [](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) P Q [R](vssgloss-r.md) [S](vssgloss-s.md) T [U](vssgloss-t.md) [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_partial_file_support"></span><span id="BASE.VSSGLOSS_PARTIAL_FILE_SUPPORT"></span>**Teilweise Dateiunterstützung**
</dt> <dd>

Die Kapazität zum Implementieren von Sicherungsvorgängen, indem Unterabschnitte der beteiligten Dateien geändert werden, anstatt mit den gesamten Dateien zu arbeiten. Siehe auch [*gerichtetes Ziel.*](vssgloss-d.md)

</dd> <dt>

<span id="base.vssgloss_persistent_shadow_copy"></span><span id="BASE.VSSGLOSS_PERSISTENT_SHADOW_COPY"></span>**Persistente Schattenkopie**
</dt> <dd>

Eine Schattenkopie, die nicht automatisch gelöscht wird, wenn der Anfordernde ein [**IVssBackupComponents-Objekt**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) frei gibt oder wenn der Computer neu gestartet wird. Weitere Informationen finden [*Sie unter Automatisches Veröffentlichen von Schattenkopien*](vssgloss-a.md)und [*Schattenkopien.*](vssgloss-s.md)

</dd> <dt>

<span id="base.vssgloss_plex"></span><span id="BASE.VSSGLOSS_PLEX"></span>**Plex**
</dt> <dd>

Ein spezieller Typ von Schattenkopievolumen, das ein Schattenkopie-Volume vollständig darstellt, ohne dass ein originales Volume benötigt wird. Dies wird auch als Split-Mirror bezeichnet, aber in dieser Dokumentation wird der Begriff Plex verwendet.

</dd> <dt>

<span id="base.vssgloss_postrestore_event"></span><span id="BASE.VSSGLOSS_POSTRESTORE_EVENT"></span>**PostRestore-Ereignis**
</dt> <dd>

Ein VSS-Ereignis, das angibt, dass eine VSS-Wiederherstellung abgeschlossen wurde.

</dd> <dt>

<span id="base.vssgloss_postsnapshot_event"></span><span id="BASE.VSSGLOSS_POSTSNAPSHOT_EVENT"></span>**PostSnapshot-Ereignis**
</dt> <dd>

Ein VSS-Ereignis, das angibt, dass eine Schattenkopie abgeschlossen wurde. Siehe auch [*Schattenkopie*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_preparebackup_event"></span><span id="BASE.VSSGLOSS_PREPAREBACKUP_EVENT"></span>**PrepareForBackup-Ereignis**
</dt> <dd>

Ein VSS-Ereignis, das angibt, dass ein Sicherungsvorgang durchgeführt wird.

</dd> <dt>

<span id="base.vssgloss_preparesnapshot_event"></span><span id="BASE.VSSGLOSS_PREPARESNAPSHOT_EVENT"></span>**PrepareForSnapshot-Ereignis**
</dt> <dd>

Ein VSS-Ereignis, das angibt, dass Writer Schritte zur Vorbereitung auf einen bevorstehenden Schattenkopievorgang ausführen sollten. Siehe auch [*Schattenkopie*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_prerestore_event"></span><span id="BASE.VSSGLOSS_PRERESTORE_EVENT"></span>**PreRestore-Ereignis**
</dt> <dd>

Ein VSS-Ereignis, das angibt, dass ein Wiederherstellungsvorgang durchgeführt werden soll.

</dd> <dt>

<span id="base.vssgloss_provider"></span><span id="BASE.VSSGLOSS_PROVIDER"></span>**Anbieter**
</dt> <dd>

Ein Betriebssystemobjekt, das E/A-Anforderungen zum Erstellen und Darstellen von Volumeschattenkopien im Dateisystem abfing und verwaltet. Siehe auch [*Hardwareanbieter*](vssgloss-h.md), [*Softwareanbieter*](vssgloss-s.md).

</dd> </dl>

 

 



