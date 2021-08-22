---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ebf8d0a7-e465-4f9f-9e3d-b97dbcf321b8
title: I (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a672a8cd25792dedb6e32e0916e85ddf50634824b00491733e19bab2c30ece4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056172"
---
# <a name="i-volume-shadow-copy-service"></a>I (Volumeschattenkopie-Dienst)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) I J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_identify_event"></span><span id="BASE.VSSGLOSS_IDENTIFY_EVENT"></span>**Identifizieren des Ereignisses**
</dt> <dd>

Ein VSS-Ereignis, das angibt, dass ein Writer oder ein Anforderer den aktuellen Writer abfragen muss. Sie wird verwendet, um die Metadateninformationen des aktuellen Writers zu erstellen. Siehe auch [*anfordernde*](vssgloss-r.md), [*Writer.*](vssgloss-w.md)

</dd> <dt>

<span id="base.vssgloss_implicit_component_inclusion"></span><span id="BASE.VSSGLOSS_IMPLICIT_COMPONENT_INCLUSION"></span>**Implizite Komponenteneinschluss**
</dt> <dd>

Die Informationen einer Komponente werden dem Sicherungskomponentendokument eines Anforderers nicht hinzugefügt, wenn es an einem Sicherungs- oder Wiederherstellungsvorgang beteiligt ist.

Nicht auswählbare Komponenten mit einem auswählbaren Vorgänger sind nur implizit enthalten, wenn ihr Vorgänger eingeschlossen ist.

Auswählbare Komponenten mit einem auswählbaren Vorgänger können implizit eingeschlossen werden, wenn der Vorgänger enthalten ist, oder explizit eingeschlossen werden.

Nicht auswählbare Komponenten ohne auswählbare Vorgänger sind nie implizit in einen Sicherungs- oder Wiederherstellungsvorgang eingeschlossen. Alle diese Komponenten müssen dem Sicherungskomponentendokument explizit hinzugefügt werden, wenn eine der Komponenten des Writers beteiligt ist.

Auswählbare Komponenten ohne auswählbare Vorgänger, die von einem Anforderer für die Teilnahme an einer Sicherung oder Wiederherstellung ausgewählt wurden, können nicht implizit in den Vorgang einbezogen werden, müssen jedoch explizit dem Dokument sicherungskomponenten hinzugefügt werden.

</dd> <dt>

<span id="base.vssgloss_incremental_backup_operations"></span><span id="BASE.VSSGLOSS_INCREMENTAL_BACKUP_OPERATIONS"></span>**Inkrementelle Sicherungsvorgänge**
</dt> <dd>

Ein Sicherungs- oder Wiederherstellungsvorgang wird nur für Dateien ausgeführt, die seit dem Speichern der letzten vollständigen, inkrementellen oder differenziellen Sicherung erstellt oder geändert wurden. Siehe auch [*differenzielle Sicherungsvorgänge.*](vssgloss-d.md)

</dd> </dl>

 

 



