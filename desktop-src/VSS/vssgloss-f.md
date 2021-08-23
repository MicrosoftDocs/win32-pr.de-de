---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9d59b2f6-c3d9-40d4-be89-ae7283794eb3
title: F (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56eef69a16a77fce7f557ae0ff02ff0e5d84d0225d082fd486af629b9804aeb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056198"
---
# <a name="f-volume-shadow-copy-service"></a>F (Volumeschattenkopie-Dienst)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**Dateigruppenkomponente**
</dt> <dd>

Eine Gruppe von Dateien, die nicht als Datenbank verwendet werden und von einem Writer definiert werden, die während Sicherungs- und Wiederherstellungsvorgängen als Einheit behandelt werden müssen. Siehe auch [*Komponente*](vssgloss-c.md), [*Datenbankkomponente*](vssgloss-d.md).

</dd> <dt>

<span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**Dateisatz**
</dt> <dd>

Die Kombination aus Pfad, Dateispezifikation und rekursivem Flag, das eine Datei oder Gruppe von Dateien beschreibt. Beispielsweise werden Dateien komponenten in Dateisätzen hinzugefügt.

Sofern nicht anders angegeben, sind die Pfade eines Dateisatzes standard Windows Pfade und können Umgebungsvariablen (z. B. %SystemRoot%) enthalten, aber keine Platzhalterzeichen enthalten. Es ist nicht erforderlich, dass der Pfad mit einem umgekehrten Schrägstrich \\ ("") endet. Es liegt an Anwendungen, die diese Informationen abrufen, um sie zu überprüfen.

Die in einem Dateisatz enthaltene Dateispezifikation gibt den Namen der enthaltenen Datei an. Diese Dateispezifikation darf keine Verzeichnisspezifikationen (z. B. keine umgekehrten Schrägstriche) enthalten, kann aber die ? und \* Platzhalterzeichen.

Das rekursive Tag ist ein boolescher Wert, der angibt, ob der Pfad des Dateisatzes nur als einzelnes Verzeichnis behandelt werden soll oder ob eine Hierarchie von Verzeichnissen angegeben wird, die rekursiv durchlaufen werden sollen. Der boolesche Wert ist **TRUE,** wenn der Pfad als Hierarchie von Verzeichnissen behandelt wird, die rekursiv durchlaufen werden sollen, oder **false,** wenn dies nicht der Fall ist.

Informationen zu einem Dateisatz werden über Instanzen der **IVssWMFiledesc-Schnittstelle** zurückgegeben und können zusätzliche Informationen enthalten, einschließlich alternativer Pfade, alternativer Speicherortzuordnungen und Schemaunterstützungseinstellungen auf Dateiebene.

Weitere Informationen finden Sie unter [*alternativer Pfad,*](vssgloss-a.md) [*Zuordnung alternativer Speicherorte,*](vssgloss-a.md) [*Komponente*](vssgloss-c.md)und *Dateispezifikation.*

</dd> <dt>

<span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**Dateispezifikation**
</dt> <dd>

Wird verwendet, um Dateien in einem Verzeichnis abzugleichen und einen Dateisatz zu definieren. Sie darf keine Verzeichnisspezifikationen (z. B. keine umgekehrten Schrägstriche) enthalten, aber sie kann die ? und \* Platzhalterzeichen.

</dd> <dt>

<span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**Dateireplikationsdienst**
</dt> <dd>

Wird verwendet, um Systemdateien in einem redundanten Systemvolumeverzeichnis (SysVol) zu replizieren, um die Dateisystemüberlebenbarkeit zu unterstützen, insbesondere für verteilte Dateisysteme.

</dd> <dt>

<span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**Einfrieren**
</dt> <dd>

Ein Zeitraum während der Erstellung von Schattenkopien, in dem alle Writer ihre Schreibvorgänge auf die Volumes geleert haben und keine zusätzlichen Schreibvorgänge initiieren.

</dd> <dt>

<span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Freeze-Ereignis**
</dt> <dd>

Ein VSS-Ereignis, das angibt, dass ein Einfrieren der Schattenkopie ausgeführt wird. Siehe auch *Einfrieren* von , [*Schattenkopie*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**Front-End-Anwendungen**
</dt> <dd>

Gibt den Punkt an, an dem ein Writer über ein Einfrieren durch VSS benachrichtigt wird. Writer, die als Front-End-Anwendungen initialisiert wurden, werden benachrichtigt, bevor Writer entweder als Back-End-Anwendungen oder als Anwendungen auf Systemebene initialisiert werden. Siehe auch [*Anwendungsebene,*](vssgloss-a.md) [*Back-End-Anwendungen,*](vssgloss-b.md) [*Anwendungen auf Systemebene,*](vssgloss-s.md) [*Writer*](vssgloss-w.md).

</dd> </dl>

 

 



