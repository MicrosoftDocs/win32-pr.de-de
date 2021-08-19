---
description: Verwalten von Transaktionsdateihandles in Transaktional NTFS.
ms.assetid: 29879a3f-14b4-462c-a001-46c3c3eb74d1
title: Verwenden von transaktionalem NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8daafd2bc2ee0e695ee3bdede4ac2f62be1000c111d0c544dec877c357f42629
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015278"
---
# <a name="how-to-use-transactional-ntfs"></a>Verwenden von transaktionalem NTFS

## <a name="transacted-file-handles"></a>Handles für transaktive Dateien

Transaktionales NTFS (TxF) bindet ein Dateihandle an eine Transaktion. Bei Vorgängen, die für ein Handle funktionieren (z. B. die [**ReadFile-**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) und [**WriteFile-Funktionen),**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) ändert sich der tatsächliche API-Funktionsaufruf nicht. Für Dateivorgänge, die einen Namen annehmen, gibt es explizite transaktive Funktionen für diese Vorgänge. Anstatt beispielsweise [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)aufzurufen, rufen [**Sie CreateFileTransacted auf.**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) Dadurch wird ein Transaktionsdateihandle erstellt, das dann für alle Dateivorgänge verwendet werden kann, die ein Handle erfordern. Alle nachfolgenden Vorgänge, die dieses Handle verwenden, sind transaktive Vorgänge.

## <a name="basic-txf-usage"></a>Grundlegende TxF-Nutzung

Die folgende Reihe von Schritten stellt die grundlegendste Verwendung für TxF dar. Komplexere Szenarien werden ebenfalls unterstützt, und zwar im Ermessen des Anwendungs-Designers.

1.  Erstellen Sie eine Transaktion, indem Sie die [**CREATETransaction-FUNKTION**](/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction) VON DER FUNKTION aufrufen oder die **IKernelTransaction-Schnittstelle** des [Distributed Transaction Coordinator](/previous-versions/windows/desktop/mscs/distributed-transaction-coordinator) (DTC) verwenden.
2.  Rufen Sie Transaktionsdateihandle ab, indem [**Sie CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)aufrufen.
3.  Ändern Sie die Datei(en) nach Bedarf mithilfe der transaktionsierten Dateihandle.
4.  Schließen Sie alle Transaktionsdateihandles, die der in Schritt 1 erstellten Transaktion zugeordnet sind.
5.  Committen oder abbrechen Sie die Transaktion, indem Sie die entsprechende FUNKTIONALITÄT ODER DTC-Funktion aufrufen.

## <a name="key-points-of-the-txf-programming-model"></a>Wichtige Punkte des TxF-Programmiermodells

Das TxF-Programmiermodell verfügt über die folgenden wichtigen Punkte, die Sie beim Entwickeln einer TxF-Anwendung berücksichtigen sollten:

-   Es wird dringend empfohlen, dass eine Anwendung alle Transaktionsdateihandles schließt, bevor ein Commit oder Rollback für eine Transaktion ausgeführt wird. Das System macht alle transaktiven Handles ungültig, wenn eine Transaktion endet. Jeder Vorgang mit Ausnahme von close, der für ein transaktives Handle ausgeführt wird, nachdem die Transaktion beendet wurde, gibt den folgenden Fehler zurück: **ERROR HANDLE NO LONGER \_ \_ \_ \_ VALID**.
-   Eine Datei wird als Speichereinheit angezeigt. Teilupdates und vollständige Dateiüberschreibungen werden unterstützt. Mehrere Transaktionen können die gleiche Datei nicht gleichzeitig ändern.
-   Speicherzuordnungs-E/A ist transparent und konsistent mit den regulären Datei-E/A-Auslastungen. Eine Anwendung muss einen geöffneten Abschnitt leeren und schließen, bevor ein Commit für eine Transaktion ausgeführt wird. Wenn sie nicht ausgeführt werden, kann dies zu Teiländerungen an der zugeordneten Datei innerhalb der Transaktion führen. Ein Rollback schlägt fehl, wenn dies nicht erfolgt.

## <a name="common-programming-errors"></a>Häufige Programmierfehler

Die folgenden allgemeinen Fehler können beim Entwickeln von transaktiven Anwendungen auftreten:

-   Verwenden eines Dateihandle nach Abschluss einer Transaktion.
-   Wenn keine Handles für gelöschte Dateien und Verzeichnisse geschlossen werden können, bevor ein Commit für eine Transaktion ausgeführt wird, wird verhindert, dass die Löschvorgänge ausgeführt werden. Dieses Ereignis muss auftreten, bevor der Commit ausgeführt wird, damit der Löschvorgang als Teil der Transaktion betrachtet wird. Dies liegt daran, dass das System eine Datei erst dann löscht, wenn das letzte Handle für sie geschlossen wird, selbst wenn der Vorgang nicht als Teil des Windows Datei-E/A-Subsystems ausgeführt wird.
-   Systeminitiierte Transaktionsrollbacks, die jederzeit auftreten können, können nicht berücksichtigt werden. Beispielsweise wird für eine Transaktion ein Rollback ausgeführt, wenn die Systemressourcen erschöpft sind.

 

 
