---
description: Wenn die Schatten Kopie abgeschlossen ist, ist der wichtigste Mechanismus für den Zugriff auf die darin enthaltenen Datei Daten die Verwendung des Geräte Objekts der Schatten Kopie.
ms.assetid: 21efdbd6-a487-4e6f-8e3c-b9224bcf92da
title: Zugriff auf Schatten Kopien von Daten Anforderer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6265586f70054277170b44f23efc52d56842e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131265"
---
# <a name="requester-access-to-shadow-copied-data"></a>Zugriff auf Schatten Kopien von Daten Anforderer

Wenn die Schatten Kopie abgeschlossen ist, ist der wichtigste Mechanismus für den Zugriff auf die darin enthaltenen Datei Daten die Verwendung des [*Geräte Objekts*](vssgloss-d.md)der Schatten Kopie.

Der **m \_ pwszsnapshotdeviceobject** -Member einer [**VSS \_ \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) -momentaufnahmenstruktur ist eine Zeichenfolge, die das Geräte Objekt eines schattenkopierten Volumes enthält. Ein Anforderer kann das **VSS \_ Snapshot \_ Prop** -Objekt eines schattenkopierten Volumes abrufen, wenn es die **VSS- \_ ID** des Volumes kennt (Identifikations-GUID), und es an [**IVssBackupComponents:: getionnapshotproperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties)übergibt.

Ein Anforderer kann mithilfe des **obj. Snap** -Members der [**VSS- \_ Objekt- \_ Prop**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) -Struktur (bei der es sich um eine [**VSS \_ \_**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) -momentaufnahmenstruktur handelt) auch Informationen über die Eigenschaften der Schatten Kopie [**abrufen, um**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) die Liste der Objekte zu durchlaufen, die durch einen-Befehl von [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)zurückgegeben werden.

Das Geräte Objekt sollte als Stamm eines schattenkopierten Volumes interpretiert werden. Aus diesem Grund enthält das Device-Objekt keinen umgekehrten Schrägstrich (" \\ ").

Pfade im schattenkopierten Volume werden abgerufen, indem der Stamm des ursprünglichen Pfads durch das Geräte Objekt ersetzt wird. Wenn Sie z. b. einen Pfad zum ursprünglichen Volume von "C: \\ Database \\ \* . mdb" und eine [**VSS- \_ Momentaufnahme- \_ Prop**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) -Instanz von snapprop erhalten, erhalten Sie den Pfad auf dem schattenkopierten Volume durch Verkettung von snappropm " \_ pwszshadow copydeviceobject", " \\ " und " \\ Database \\ \* . mdb".

Die VSS-Datei Sätze enthalten möglicherweise Platzhalter Zeichen in ihren Dateideskriptoren, sodass das Abrufen einer vollständigen Liste der Dateien in einer Schatten Kopie, die von einer Komponente verwaltet wird, möglicherweise die Verwendung von Methoden wie " **FindFileFirst**", " **findfilefirstex**" und " **FindNextFile**" erfordert.

 

 



