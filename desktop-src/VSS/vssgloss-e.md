---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7eb1d433-21db-45cc-a141-13a89993e30c
title: E (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 305a02633e8ed2aca1e372f250d6d91a8560ef1cb7a9f565e64aea6924397ebb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905130"
---
# <a name="e-volume-shadow-copy-service"></a>E (Volumeschattenkopie-Dienst)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E F [G](vssgloss-f.md) [](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) T [U](vssgloss-t.md) [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**Explizites Einschluss von Komponenten**
</dt> <dd>

Hinzufügen der Informationen einer Komponente zum Sicherungskomponentendokument eines An anfordernden, wenn es an einem Sicherungs- oder Wiederherstellungsvorgang beteiligt ist. Anfordernde benutzer verwenden [**IVssBackupComponents::AddComponent,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) um eine Komponente explizit in einen Sicherungsvorgang einbetten, und [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) oder [**IVssBackupComponents::AddRestoreSubcomponent,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) um eine Komponente explizit in einen Wiederherstellungsvorgang einbetten.

Wenn eine Komponente eines Writer gesichert oder wiederhergestellt wird, müssen alle nicht auswählbaren Komponenten ohne auswählbare Vorgänger explizit in einen Sicherungs- oder Wiederherstellungsvorgang eingeschlossen werden.

Auswählbare Komponenten ohne auswählbare Vorgänger, die von einem Anfordernden für die Teilnahme an einer Sicherung oder Wiederherstellung ausgewählt wurden, müssen explizit in den Vorgang eingeschlossen werden.

Nicht auswählbare Komponenten mit einem auswählbaren Vorgänger werden nie explizit eingeschlossen.

Auswählbare Komponenten mit einem auswählbaren Vorgänger können explizit eingeschlossen oder implizit eingeschlossen werden, wenn der Vorgänger explizit eingeschlossen wird.

</dd> <dt>

<span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**Verfügbar gemachte Schattenkopie**
</dt> <dd>

Eine Volumeschattenkopie, die auf einem System bereitgestellt wird und für andere Prozesse als die, die sie verwalten, verfügbar ist. Ein Schattenkopie-Volume, das unter einem Laufwerkbuchstaben oder einem Verzeichnisspeicherort bereitgestellt wird, wird als "lokal verfügbar gemacht" bezeichnet. Ein Schattenkopie-Volume, auf das über eine Freigabe zugegriffen werden kann (mit Ausnahme von clientzugezugriffsbasierten Schattenkopien), wird als "remote verfügbar gemacht" bezeichnet. Alle verfügbar gemachten Schattenkopien sind ebenfalls als Schattenkopien verfügbar gemacht. Siehe auch [*Clientzugriff auf Schattenkopie*](vssgloss-c.md), [*Schattenkopie*](vssgloss-s.md).

</dd> </dl>

 

 



