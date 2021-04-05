---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9d59b2f6-c3d9-40d4-be89-ae7283794eb3
title: F (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f60a456ce6ea795dc8376c0f707d028523cec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751544"
---
# <a name="f-volume-shadow-copy-service"></a>F (Volumeschattenkopie-Dienst)

[a](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) F [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_file_group_component"></span><span id="BASE.VSSGLOSS_FILE_GROUP_COMPONENT"></span>**Dateigruppen Komponente**
</dt> <dd>

Eine Gruppe von Dateien, die nicht als Datenbank verwendet und von einem Writer definiert werden, da Sie während Sicherungs-und Wiederherstellungs Vorgängen als Einheit behandelt werden müssen. Siehe auch [*Komponente*](vssgloss-c.md), [*Datenbankkomponente*](vssgloss-d.md).

</dd> <dt>

<span id="base.vssgloss_file_set"></span><span id="BASE.VSSGLOSS_FILE_SET"></span>**Dateisatz**
</dt> <dd>

Die Kombination aus einem Pfad, einer Datei Spezifikation und einem rekursiven Flag, das eine Datei oder eine Gruppe von Dateien beschreibt. Dateien werden z. b. den Komponenten in Datei Sätzen hinzugefügt.

Sofern nicht anders angegeben, sind die Pfade eines Datei Satzes standardmäßige Windows-Pfade und können Umgebungsvariablen (z. b .% systemroot%) enthalten. darf jedoch keine Platzhalter Zeichen enthalten. Es ist nicht erforderlich, dass der Pfad mit einem umgekehrten Schrägstrich (" \\ ") endet. Es gibt Anwendungen, die diese Informationen abrufen, um Sie zu überprüfen.

Die in einem Datei Satz enthaltene Datei Spezifikation gibt den Namen der Datei oder Dateien an, die Sie enthält. Diese Datei Spezifikation darf keine Verzeichnis Spezifikationen (z. b. keine umgekehrten Schrägstriche) enthalten, kann aber auch das enthalten? und Platzhalter \* Zeichen.

Das rekursive Tag ist ein boolescher Wert, der angibt, ob der Pfad des Datei Satzes als nur ein einzelnes Verzeichnis behandelt werden soll oder ob er eine Hierarchie von Verzeichnissen angibt, die rekursiv durchlaufen werden soll. Der boolesche Wert ist **true** , wenn der Pfad als eine Hierarchie von Verzeichnissen behandelt wird, die rekursiv durchlaufen werden sollen, andernfalls **false** .

Informationen zu einem Dateisatz werden durch Instanzen der **ivsswmfiledesc** -Schnittstelle zurückgegeben und können zusätzliche Informationen enthalten, einschließlich alternativer Pfade, alternativer Speicherort Zuordnungen und Schema Unterstützungs Einstellungen auf Dateiebene.

Siehe auch [*Alternativer Pfad*](vssgloss-a.md), [*Zuordnung alternativer Speicherorte*](vssgloss-a.md), [*Komponente*](vssgloss-c.md), *Datei Spezifikation*.

</dd> <dt>

<span id="base.vssgloss_file_specification"></span><span id="BASE.VSSGLOSS_FILE_SPECIFICATION"></span>**Datei Spezifikation**
</dt> <dd>

Wird verwendet, um Dateien innerhalb eines Verzeichnisses abzugleichen und einen Datei Satz zu definieren. Er darf keine Verzeichnis Spezifikationen (z. b. keine umgekehrten Schrägstriche) enthalten, kann aber auch das enthalten? und Platzhalter \* Zeichen.

</dd> <dt>

<span id="base.vssgloss_file_system_replication"></span><span id="BASE.VSSGLOSS_FILE_SYSTEM_REPLICATION"></span>**Datei Replikations Dienst**
</dt> <dd>

Wird verwendet, um Systemdateien in einem SYSVOL-Verzeichnis (Redundant System Volume) zu replizieren, um die Survivability des Dateisystems zu unterstützen, insbesondere für verteilte Dateisysteme.

</dd> <dt>

<span id="base.vssgloss_freeze"></span><span id="BASE.VSSGLOSS_FREEZE"></span>**ge**
</dt> <dd>

Ein Zeitraum während des Erstellungs Prozesses der Schatten Kopie, wenn alle Writer ihre Schreibvorgänge auf die Volumes geleert haben und keine weiteren Schreibvorgänge einleiten.

</dd> <dt>

<span id="base.vssgloss_freeze_event"></span><span id="BASE.VSSGLOSS_FREEZE_EVENT"></span>**Ereignis Einfrieren**
</dt> <dd>

Ein VSS-Ereignis, das angibt, dass eine schattenkopiesperre ausgeführt wird. Siehe auch *Einfrieren*, [*Schatten Kopie*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_front_end_level_applications"></span><span id="BASE.VSSGLOSS_FRONT_END_LEVEL_APPLICATIONS"></span>**Anwendungen auf Front-End-Ebene**
</dt> <dd>

Gibt den Punkt an, an dem ein Writer über eine Sperre durch den VSS benachrichtigt wird. Writer, die als Anwendungen auf Front-End-Ebene initialisiert wurden, werden vor Writer benachrichtigt, die als Back-End-Ebene-Anwendungen oder als Anwendungen auf Systemebene initialisiert werden. Weitere Informationen finden Sie auch auf [*Anwendungsebene*](vssgloss-a.md), [*Back-End-Anwendungen*](vssgloss-b.md), Anwendungen auf [*Systemebene*](vssgloss-s.md)und [*Writer*](vssgloss-w.md).

</dd> </dl>

 

 



