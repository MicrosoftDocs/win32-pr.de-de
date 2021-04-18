---
description: Verwalten von transaktiven Datei Handles in Transaktions-NTFS.
ms.assetid: 29879a3f-14b4-462c-a001-46c3c3eb74d1
title: Verwenden von transaktionalen NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43681f0d5b27f0db03d8b6c44564b792fce4b467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351520"
---
# <a name="how-to-use-transactional-ntfs"></a>Verwenden von transaktionalen NTFS

## <a name="transacted-file-handles"></a>Transaktive Datei Handles

Transaktionale NTFS (TxF) bindet ein Datei Handle an eine Transaktion. Bei Vorgängen, die an einem Handle arbeiten (z. b. die Funktionen "read [**File**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) " und " [**Write File**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) "), wird der tatsächliche API-Funktions Aufrufwert nicht geändert. Bei Datei Vorgängen, die einen Namen annehmen, gibt es explizite transaktive Funktionen für diese Vorgänge. Rufen Sie z. b. [**createfiletranshandelten**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)auf, anstatt [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)aufzurufen. Dadurch wird ein transaktives Datei Handle erstellt, das dann für alle Datei Vorgänge verwendet werden kann, die ein Handle erfordern. Alle nachfolgenden Vorgänge, die dieses Handle verwenden, sind transaktive Vorgänge.

## <a name="basic-txf-usage"></a>Grundlegende TxF-Verwendung

Die folgenden Schritte sind die grundlegende Verwendung von TxF. Komplexere Szenarien werden auch unter dem Ermessen des Anwendungs-Designers unterstützt.

1.  Erstellen Sie eine Transaktion, indem Sie die KTM-Funktion [**CreateTransaction**](/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction) aufrufen, oder indem Sie die **IKernelTransaction** -Schnittstelle des [Distributed Transaction Coordinator](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC) verwenden.
2.  Abrufen von transaktiven Datei Handles durch Aufrufen von [**createfiletranshandelten**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).
3.  Ändern Sie die Dateien nach Bedarf mithilfe der transaktiven Datei Handle (en).
4.  Schließen Sie alle Transaktions Datei Handles, die mit der in Schritt 1 erstellten Transaktion verknüpft sind.
5.  Commit oder Abbruch der Transaktion durch Aufrufen der entsprechenden KTM-oder DTC-Funktion.

## <a name="key-points-of-the-txf-programming-model"></a>Wichtige Punkte des TxF-Programmiermodells

Das TxF-Programmiermodell bietet die folgenden wichtigen Punkte, die Sie beim Entwickeln einer TxF-Anwendung beachten sollten:

-   Es wird dringend empfohlen, dass eine Anwendung alle Transaktions Datei Handles schließt, bevor ein Commit oder Rollback einer Transaktion ausgeführt wird. Das System macht alle Transaktions Handles ungültig, wenn eine Transaktion beendet wird. Jeder Vorgang, außer Close, wird für ein transaktives Handle nach Ende der Transaktion ausgeführt, gibt den folgenden Fehler zurück: das **Fehler \_ handle ist \_ nicht \_ mehr \_ gültig**.
-   Eine Datei wird als Speichereinheit angezeigt. Teil Updates und vollständige über schreibungen von Dateien werden unterstützt. Mehrere Transaktionen können dieselbe Datei nicht gleichzeitig ändern.
-   Die Speicher Abbild-e/a ist transparent und konsistent mit der regulären Datei-e/a. Eine Anwendung muss einen geöffneten Abschnitt leeren und schließen, bevor ein Commit für eine Transaktion ausgeführt wird. Wenn dies nicht der Fall ist, kann dies zu partiellen Änderungen an der zugeordneten Datei innerhalb der Transaktion führen. Ein Rollback schlägt fehl, wenn dies nicht der Fall ist.

## <a name="common-programming-errors"></a>Allgemeine Programmierfehler

Folgende häufige Fehler können bei der Entwicklung von transaktiven Anwendungen auftreten:

-   Verwenden eines Datei Handles, nachdem eine Transaktion abgeschlossen wurde.
-   Fehler beim Schließen von Handles in gelöschten Dateien und Verzeichnissen, bevor ein Commit für eine Transaktion ausgeführt wird. Dadurch wird verhindert, dass Löschvorgänge ausgeführt werden. Dieses Ereignis muss eintreten, bevor der Commit für den Löschvorgang ausgeführt wird, um als Teil der Transaktion angesehen zu werden. Dies liegt daran, dass das System eine Datei erst dann löscht, wenn das letzte Handle geschlossen wurde, auch wenn der Vorgang nicht als Teil des Windows-Datei-e/a-Subsystems behandelt wird.
-   Fehler beim berücksichtigen der vom System initiierten Transaktions Rollbacks, die zu einem beliebigen Zeitpunkt auftreten können. Beispielsweise wird für eine Transaktion ein Rollback ausgeführt, wenn die Systemressourcen erschöpft sind.

 

 
