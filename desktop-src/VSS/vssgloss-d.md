---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 26e7eaae-f540-47d1-99ec-6af0fd223039
title: D (Volumeschattenkopie-Dienst)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3910a2fb09688e26b33b586f4558c05cb804688645486dfec751c9839fcff278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998030"
---
# <a name="d-volume-shadow-copy-service"></a>D (Volumeschattenkopie-Dienst)

[A](vssgloss-a.md) [B](vssgloss-b.md) [C](vssgloss-c.md) D [E](vssgloss-e.md) [F](vssgloss-f.md) [G](vssgloss-g.md) [H](vssgloss-h.md) [I](vssgloss-i.md) J K [L](vssgloss-l.md) M [N](vssgloss-n.md) [O](vssgloss-o.md) [P](vssgloss-p.md) Q [R](vssgloss-r.md) [S](vssgloss-s.md) T [U](vssgloss-t.md) [V](vssgloss-v.md) [W](vssgloss-w.md) X Y Z

<dl> <dt>

<span id="base.vssgloss_database_component"></span><span id="BASE.VSSGLOSS_DATABASE_COMPONENT"></span>**Datenbankkomponente**
</dt> <dd>

Eine Gruppe von Dateien, die von einer Datenbank verwendet und von einem Writer so definiert werden, dass sie während Sicherungs- und Wiederherstellungsvorgängen als Einheit behandelt werden muss. Siehe auch [*Komponente*](vssgloss-c.md), [*Dateigruppenkomponente*](vssgloss-f.md).

</dd> <dt>

<span id="base.vssgloss_default_provider"></span><span id="BASE.VSSGLOSS_DEFAULT_PROVIDER"></span>**Standardanbieter**
</dt> <dd>

Weitere Informationen [*finden Sie unter Systemanbieter*](vssgloss-s.md).

</dd> <dt>

<span id="base.vssgloss_deleted_shadow_copy"></span><span id="BASE.VSSGLOSS_DELETED_SHADOW_COPY"></span>**Gelöschte Schattenkopie**
</dt> <dd>

Auf gelöschte Schattenkopien kann überhaupt nicht zugegriffen werden, und sie dürfen nicht zu einem beliebigen Zeitpunkt in der Zukunft zugänglich gemacht werden.

</dd> <dt>

<span id="base.vssgloss_dependency"></span><span id="BASE.VSSGLOSS_DEPENDENCY"></span>**Abhängigkeit**
</dt> <dd>

Weitere Informationen finden [*Sie unter Komponentenabhängigkeit.*](vssgloss-c.md)

</dd> <dt>

<span id="base.vssgloss_device_object"></span><span id="BASE.VSSGLOSS_DEVICE_OBJECT"></span>**Geräteobjekt**
</dt> <dd>

Eine Zeichenfolge, die den "Stamm" eines kopierten Schattenvolumens angibt. Auf Dateien und Verzeichnisse auf einem schattenkopierten Volume kann verwiesen werden, indem die Geräteobjektzeichenfolge einem entsprechenden Pfad auf dem ursprünglichen Volume vorausgeschrieben wird. Wie als **m \_ pwszSnapshotDeviceObject-Member** der [**VSS \_ SNAPSHOT \_ PROP-Struktur**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) erhalten, hat das Geräteobjekt keinen zurücken Schrägstrich (" \\ ").

</dd> <dt>

<span id="base.vssgloss_diff_area"></span><span id="BASE.VSSGLOSS_DIFF_AREA"></span>**Diff-Bereich**
</dt> <dd>

Der Speicherort auf dem Volume, an dem *die differenziellen* Daten gespeichert werden. Dies wird auch als Schattenkopiespeicherplatz bezeichnet.

</dd> <dt>

<span id="base.vssgloss_differenced_files"></span><span id="BASE.VSSGLOSS_DIFFERENCED_FILES"></span>**Differenzierte Dateien**
</dt> <dd>

Dateien, die an einem inkrementellen oder differenziellen Sicherungsvorgang beteiligt sind, der durch Aktualisieren ganzer Dateien implementiert wird (im Gegensatz zum Ändern von Abschnitten dieser Dateien mit teilweiser Dateiunterstützung). Wenn Sie beispielsweise eine differenzielle Sicherung implementieren möchten, wird eine gesamte Datei (anstelle des geänderten Abschnitts) auf ein Sicherungsmedium kopiert. Diese Datei ist eine Differenzdatei. Siehe auch [*inkrementelle Sicherungsvorgänge,*](vssgloss-i.md) *differenzielle Sicherungsvorgänge,* [*Teilweise Dateiunterstützung.*](vssgloss-p.md)

</dd> <dt>

<span id="base.vssgloss_differential_backup_operations"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_BACKUP_OPERATIONS"></span>**Differenzielle Sicherungsvorgänge**
</dt> <dd>

Ein Sicherungs- oder Wiederherstellungsvorgang wird nur für Dateien ausgeführt, die seit dem Speichern der letzten vollständigen Sicherung erstellt oder geändert wurden. Siehe auch [*inkrementelle Sicherungsvorgänge,*](vssgloss-i.md) [*Teilweise Dateiunterstützung,*](vssgloss-p.md) *Differenzdateien*.

</dd> <dt>

<span id="base.vssgloss_differential_data"></span><span id="BASE.VSSGLOSS_DIFFERENTIAL_DATA"></span>**Differenzielle Daten**
</dt> <dd>

Daten, die auf ein ursprüngliches Volume angewendet werden können, um ein Schattenkopie-Volume zu generieren. Dies wird auch als Copy-on-Write-Daten bezeichnet, aber in dieser Dokumentation wird der Begriff differenzielle Daten verwendet.

</dd> <dt>

<span id="base.vssgloss_directed_targeting"></span><span id="BASE.VSSGLOSS_DIRECTED_TARGETING"></span>**Gerichtete Zielgruppenadressierung**
</dt> <dd>

Ein Wiederherstellungsmodus, in dem ein Writer angibt, dass eine Datei (die Quelldatei) neu zugeordnet werden soll, wenn sie wiederhergestellt werden soll. Die Datei kann an einem neuen Wiederherstellungsspeicherort und/oder an einem anderen Datenbereich wiederhergestellt werden, der in einem anderen Offset mit dem Wiederherstellungsspeicherort wiederhergestellt wird.

</dd> </dl>

 

 



