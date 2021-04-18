---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26e7eaae-f540-47d1-99ec-6af0fd223039
title: D (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25af02bd43c5130fa7ce60ed08ec4ab822ff1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354483"
---
# <a name="d-volume-shadow-copy-service"></a>D (Volumeschattenkopie-Dienst)

[a](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) D [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) [T](vssgloss-t.md) U [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_database_component"></span><span id="BASE.VSSGLOSS_DATABASE_COMPONENT"></span>**Datenbankkomponente**
</dt> <dd>

Eine Gruppe von Dateien, die von einer Datenbank verwendet und von einem Writer so definiert werden, dass Sie während Sicherungs-und Wiederherstellungs Vorgängen als Einheit behandelt werden muss. Siehe auch [*Komponente*](vssgloss-c.md), [*Dateigruppen Komponente*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_default_provider"></span><span id="BASE.VSSGLOSS_DEFAULT_PROVIDER"></span>**Standardanbieter**
</dt> <dd>

Siehe [*Systemanbieter*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_deleted_shadow_copy"></span><span id="BASE.VSSGLOSS_DELETED_SHADOW_COPY"></span>**Schatten Kopie gelöscht**
</dt> <dd>

Auf gelöschte Schatten Kopien kann nicht zugegriffen werden, und Sie dürfen nicht zu einem späteren Zeitpunkt zugänglich gemacht werden.

</dd> <dt>

<span id="base.vssgloss_dependency"></span><span id="BASE.VSSGLOSS_DEPENDENCY"></span>**gkeit**
</dt> <dd>

Siehe [*Komponenten Abhängigkeit*](vssgloss-c.md).

</dd> <dt>

<span id="base.vssgloss_device_object"></span><span id="BASE.VSSGLOSS_DEVICE_OBJECT"></span>**Geräte Objekt**
</dt> <dd>

Eine Zeichenfolge, die den "Stamm" eines schattenkopierten Volumes angibt. Auf Dateien und Verzeichnisse auf einem schattenkopierten Volume kann verwiesen werden, indem die Geräte Objekt Zeichenfolge einem entsprechenden Pfad auf dem ursprünglichen Volume vorangestellt wird. Wie das Element **m \_ pwszsnapshotdeviceobject** der VSS-momentaufnahmenstruktur, hat das Geräte Objekt keinen umgekehrten Schrägstrich (" [**\_ \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) \\ ").

</dd> <dt>

<span id="base.vssgloss_diff_area"></span><span id="BASE.VSSGLOSS_DIFF_AREA"></span>**Vergleichs Bereich**
</dt> <dd>

Der Speicherort auf dem Volume, auf dem die *differenziellen Daten* gespeichert werden. Dies wird auch als Schatten Kopie-Speicherplatz bezeichnet.

</dd> <dt>

<span id="base.vssgloss_differenced_files"></span><span id="BASE.VSSGLOSS_DIFFERENCED_FILES"></span>**differenzierte Dateien**
</dt> <dd>

Dateien, die an einem inkrementellen oder differenziellen Sicherungs Vorgang beteiligt sind, der durch Aktualisieren ganzer Dateien implementiert wird (im Gegensatz zum Ändern von Abschnitten dieser Dateien mithilfe von teilweiser Dateiunterstützung Wenn beispielsweise eine differenzielle Sicherung implementiert werden soll, wird eine gesamte Datei (anstatt nur der geänderte Abschnitt) auf ein Sicherungsmedium kopiert. diese Datei ist eine differenzielle Datei. Siehe auch [*inkrementelle Sicherungs Vorgänge*](vssgloss-i.md), *differenzielle Sicherungs Vorgänge*, [*Unterstützung von Teil Dateien*](vssgloss-p.md).

</dd> <dt>

<span id="base.vssgloss_differential_backup_operations"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_BACKUP_OPERATIONS"></span>**differenzielle Sicherungs Vorgänge**
</dt> <dd>

Ein Sicherungs-oder Wiederherstellungs Vorgang wurde nur für Dateien durchgeführt, die seit der letzten vollständigen Sicherung erstellt oder geändert wurden. Siehe auch [*inkrementelle Sicherungs Vorgänge*](vssgloss-i.md), [*Unterstützung von Teil Dateien*](vssgloss-p.md), *differenzierte Dateien*.

</dd> <dt>

<span id="base.vssgloss_differential_data"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_DATA"></span>**differenzielle Daten**
</dt> <dd>

Daten, die auf ein ursprüngliches Volume angewendet werden können, um ein Schattenkopievolume zu generieren. Dies wird auch als Kopier-on-Write-Daten bezeichnet, aber in dieser Dokumentation wird der Begriff "differenzielle Daten" verwendet.

</dd> <dt>

<span id="base.vssgloss_directed_targeting"></span><span id="BASE.VSSGLOSS_DIRECTED_TARGETING"></span>**gesteuerte Ziel Ausrichtung**
</dt> <dd>

Ein Wiederherstellungs Modus, durch den ein Writer anzeigt, dass er (die Quelldatei) neu zugeordnet werden soll, wenn eine Datei wieder hergestellt werden soll. Die Datei kann an einem neuen Wiederherstellungs Speicherort wieder hergestellt werden, und/oder Bereiche der Daten werden an einem anderen Offset mit dem Wiederherstellungs Speicherort wieder hergestellt.

</dd> </dl>

 

 



