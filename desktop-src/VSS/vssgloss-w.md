---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: daa383ba-994e-4986-9979-119576cecd1c
title: W (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9295be608f81d82104c1d55f3656d1a24243a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526267"
---
# <a name="w-volume-shadow-copy-service"></a>W (Volumeschattenkopie-Dienst)

[a](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) [D](vssgloss-d.md) [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) W X Y Z

<dl> <dt>

<span id="base.vssgloss_windows_file_protection"></span><span id="BASE.VSSGLOSS_WINDOWS_FILE_PROTECTION"></span>**Windows-Datei Schutz**
</dt> <dd>

Ein-Systemdienst, der spezielle Betriebssystemdateien schützt. Wenn eine dieser Dateien gelöscht oder überschrieben wird, ersetzt der Windows-Datei Schutz die Datei durch den ursprünglichen aus dem Cache.

</dd> <dt>

<span id="base.vssgloss_writer"></span><span id="BASE.VSSGLOSS_WRITER"></span>**Maschine**
</dt> <dd>

Eine Anwendung, die die e/a-Vorgänge mit VSS-schattenkopievorgängen (z. b. Sicherungen und Wiederherstellungen) koordiniert, sodass sich die auf dem schattenkopierten Volume enthaltenen Daten in einem konsistenten Zustand befinden.

Zur Unterstützung dieser Koordination muss ein Writer eine Instanz einer Klasse implementieren, die von der abstrakten Basisklasse **CVssWriter** abgeleitet ist, um mit der VSS-Infrastruktur zu kommunizieren. Siehe auch [*Schatten Kopie*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_writer_class"></span><span id="BASE.VSSGLOSS_WRITER_CLASS"></span>**Writer-Klasse**
</dt> <dd>

Eine Globally Unique Identifier (GUID), die von einem Writer während der Initialisierung bereitgestellt wird, um anzugeben, dass er zu einem bestimmten Typ von Writern gehört. Beispielsweise können mehrere Implementierungen eines Writers dieselbe Writer-Klassen-ID verwenden.

Writer derselben Klasse können von ihren Writer-Instanzen unterschieden werden. Es liegt an einem Anwendungsentwickler, Writer-Klassen anzugeben. Siehe auch *Writer-Instanz*.

</dd> <dt>

<span id="base.vssgloss_writer_instance"></span><span id="BASE.VSSGLOSS_WRITER_INSTANCE"></span>**Writer-Instanz**
</dt> <dd>

Eine Globally Unique Identifier (GUID), die von VSS für jeden Writer-Prozess bereitgestellt wird, der auf einem System ausgeführt wird. Bei jedem Start des Writers wird ein eindeutiger Wert für die Writer-Instanz generiert.

</dd> <dt>

<span id="base.vssgloss_writer_metadata_document"></span><span id="BASE.VSSGLOSS_WRITER_METADATA_DOCUMENT"></span>**Writer-Metadatendokument**
</dt> <dd>

Ein XML-Dokument, das von einem Writer erstellt wurde (mithilfe der **ivsskreatewrite Metadata** -Schnittstelle), das Informationen über den Zustand und die Komponenten des Writers enthält. Ein Anforderer kann Writer-Metadatendokumente (mithilfe der **ivssexaminewrite Metadata** -Schnittstelle) Abfragen, wenn ein Wiederherstellungs-oder Sicherungs Vorgang durchgeführt wird.

Ein Writer-Metadatendokument enthält die Liste aller Komponenten eines Writers, von denen jedes möglicherweise an einer Sicherung beteiligt ist. Dies unterscheidet sich vom Dokument mit den Sicherungs Komponenten der Anforderer, das nur die Komponenten enthält, die explizit für einen Sicherungs-oder Wiederherstellungs Vorgang eingeschlossen wurden.

Nachdem das Writer-Metadatendokument erstellt wurde, sollte es als Schreib geschütztes Objekt angezeigt werden. Sie kann auf einem Datenträger gespeichert werden. Weitere Informationen finden Sie im [*Dokument zu Sicherungs Komponenten*](vssgloss-b.md), [*explizite Komponenten Einbindung*](vssgloss-e.md), [*impliziter Komponenten Einbindung*](vssgloss-i.md).

</dd> </dl>

 

 



