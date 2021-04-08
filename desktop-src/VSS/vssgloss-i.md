---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ebf8d0a7-e465-4f9f-9e3d-b97dbcf321b8
title: I (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b043c340de5d1703587b83f72851db76d367832a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751537"
---
# <a name="i-volume-shadow-copy-service"></a>I (Volumeschattenkopie-Dienst)

[a](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) I J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Ereignis ermitteln**
</dt> <dd>

Ein VSS-Ereignis, das angibt, dass ein Writer oder eine Anforderer den aktuellen Writer Abfragen muss. Sie wird verwendet, um die Metadateninformationen des aktuellen Writers zu erstellen. Siehe auch [*anfordernde Person*](vssgloss-r.md), [*Writer*](vssgloss-w.md).

</dd> <dt>

<span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**implizite Komponenten Einbindung**
</dt> <dd>

Das Hinzufügen von Informationen zu einer Komponente zum Sicherungs Komponenten Dokument eines Anforderers, wenn es an einem Sicherungs-oder Wiederherstellungs Vorgang beteiligt ist.

Nicht auswählbare Komponenten mit einem auswählbaren Vorgänger werden nur implizit eingeschlossen, wenn ihr Vorgänger eingeschlossen ist.

Auswählbare Komponenten mit einem auswählbaren Vorgänger können implizit eingeschlossen werden, wenn der Vorgänger eingeschlossen ist oder explizit eingeschlossen werden kann.

Nicht auswählbare Komponenten ohne auswählbare Vorgänger sind nicht implizit in einem Sicherungs-oder Wiederherstellungs Vorgang enthalten – alle Komponenten müssen explizit dem Dokument mit den Sicherungs Komponenten hinzugefügt werden, wenn eine der Komponenten des Writers beteiligt ist.

Auswählbare Komponenten ohne auswählbare Vorgänger, die von einem Anforderer für die Teilnahme an einer Sicherung oder Wiederherstellung ausgewählt werden, können nicht implizit in den Vorgang eingeschlossen werden, sondern müssen explizit dem Sicherungs Komponenten Dokument hinzugefügt werden

</dd> <dt>

<span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**inkrementelle Sicherungs**
</dt> <dd>

Ein Sicherungs-oder Wiederherstellungs Vorgang wird nur für Dateien ausgeführt, die seit der letzten vollständigen, inkrementellen oder differenziellen Sicherung erstellt oder geändert wurden. Siehe auch [*differenzielle Sicherungs Vorgänge*](vssgloss-d.md).

</dd> </dl>

 

 



