---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 7eb1d433-21db-45cc-a141-13a89993e30c
title: E (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e97425100d8e2e3d0add6ea0e6fd1de67bc6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343682"
---
# <a name="e-volume-shadow-copy-service"></a>E (Volumeschattenkopie-Dienst)

[a](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) E [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_explicit_component_inclusion"></span><span id="BASE.VSSGLOSS_EXPLICIT_COMPONENT_INCLUSION"></span>**explizite Komponenten Einbindung**
</dt> <dd>

Das Hinzufügen der Informationen einer Komponente zum Sicherungs Komponenten Dokument eines Anforderers, wenn es an einem Sicherungs-oder Wiederherstellungs Vorgang beteiligt ist. Anforderer verwenden [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) , um eine Komponente explizit in einen Sicherungs Vorgang einzubeziehen, und [**IVssBackupComponents:: setselectedforrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) oder [**IVssBackupComponents:: adressstoresubcomponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addrestoresubcomponent) , um explizit eine Komponente in einen Wiederherstellungs Vorgang einzubeziehen.

Wenn eine beliebige Komponente eines Writers gesichert oder wieder hergestellt wird, müssen alle nicht auswählbaren Komponenten ohne auswählbare Vorgänger explizit in einen Sicherungs-oder Wiederherstellungs Vorgang eingeschlossen werden.

Auswählbare Komponenten ohne auswählbare Vorgänger, die von einem Anforderer für die Teilnahme an einer Sicherung oder Wiederherstellung ausgewählt wurden, müssen explizit in den Vorgang eingeschlossen

Nicht auswählbare Komponenten mit einem auswählbaren Vorgänger werden nie explizit eingeschlossen.

Auswählbare Komponenten mit einem auswählbaren Vorgänger können explizit eingeschlossen werden oder implizit eingeschlossen werden, wenn der Vorgänger explizit eingeschlossen wird.

</dd> <dt>

<span id="base.vssgloss_exposed_shadow_copy"></span><span id="BASE.VSSGLOSS_EXPOSED_SHADOW_COPY"></span>**offengelegte Schatten Kopie**
</dt> <dd>

Eine Volumeschattenkopie, die auf einem System bereitgestellt wird und für andere Prozesse als die zur Verfügung steht, die Sie verwaltet. Ein Schattenkopievolume, das unter einem Laufwerk Buchstaben oder einem Verzeichnis Speicherort eingebunden ist, wird als "lokal verfügbar gemacht" bezeichnet. Ein über eine Freigabe verfügbarer Schattenkopievolume (mit Ausnahme von Client zugänglichen Schatten Kopien) wird als "Remote verfügbar gemacht" bezeichnet. Alle verfügbar gemachten Schatten Kopien sind auch Schatten Kopien. Weitere Informationen finden Sie auch auf der [*Client zugänglichen Schatten Kopie*](vssgloss-c.md), [*Schatten Kopie*](vssgloss-s.md).

</dd> </dl>

 

 



