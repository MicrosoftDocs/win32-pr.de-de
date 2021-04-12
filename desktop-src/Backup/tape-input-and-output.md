---
title: Band Eingabe und-Ausgabe
description: Es gibt mehrere Funktionen, die Anwendungen verwenden können, um Eingabe-und Ausgabe Vorgänge (e/a) auf einem Bandlaufwerk auszuführen. Die Band-e/a ähnelt der e/a-Vorgänge, die auf einem Kommunikationsgerät ausgeführt werden.
ms.assetid: 1862c267-0070-4fe8-bb77-40167913978a
keywords:
- Band Eingabe und Ausgabe Sicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5946659f1ad0246e37981201e4e08611b45b70b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315897"
---
# <a name="tape-input-and-output"></a>Band Eingabe und-Ausgabe

Es gibt mehrere Funktionen, die Anwendungen verwenden können, um Eingabe-und Ausgabe Vorgänge (e/a) auf einem Bandlaufwerk auszuführen. Die Band-e/a ähnelt der e/a-Vorgänge, die auf einem Kommunikationsgerät ausgeführt werden.

Beim Durchführen von Band-e/a-Vorgängen werden Band Firmwareinformationen in den ersten Blöcken auf einem Band gespeichert. in der Regel wird ein Teil der ersten 100-Blöcke verwendet. Anwendungen sollten diese Blöcke nicht verwenden. Spezifischere Informationen zu diesem Betreff sind von den einzelnen Band Systemherstellern verfügbar. Im Allgemeinen werden von einer Anwendung, die die ersten 100-Blöcke auf einem Band überspringt, das Bandlaufwerk idiosyncraasen vermieden.

Die Funktionen [**gettapeposition**](/windows/desktop/api/Winbase/nf-winbase-gettapeposition) und [**settapeposition**](/windows/desktop/api/Winbase/nf-winbase-settapeposition) rufen die aktuelle Band Position ab und verschieben diese. Die Funktion " [**schreitetapemark**](/windows/desktop/api/Winbase/nf-winbase-writetapemark) " schreibt eine angegebene Anzahl von setmarkierungen, Datei Markierungen, kurzen Datei Markierungen und langen Datei Markierungen. Die [**erasetape**](/windows/desktop/api/Winbase/nf-winbase-erasetape) -Funktion löscht den gesamten oder einen Teil eines Bands.

Die Funktionen " [**Infofile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " und " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile) " lesen und schreiben Datei Daten von und auf dem Band. Die Daten werden in kompletten Blöcken gelesen und geschrieben. Wenn die Blockgröße des Bands 512 Bytes beträgt, müssen bei allen Lese-und Schreibvorgängen Puffer verwendet werden, bei denen es sich um einfache ganzzahlige Vielfache dieser Blockgröße handelt: 512, 1024, 1536, 2048 usw. Bei den meisten, wenn nicht allen, dürfen Laufwerke nur einen Schreibvorgang zulassen, nachdem das Band zurückgesetzt oder ein Lesevorgang eine Daten Ende-Fehlermeldung erzeugt hat.

Führen Sie die folgenden Schritte aus, um Datei Daten im Block Modus variabler Länge in ein Band zu schreiben oder von einem Band zu schreiben:

1.  Bestimmen Sie, ob das Bandlaufwerk den Block Modus variabler Länge unterstützt, indem Sie die [**gettapeparameters**](/windows/desktop/api/Winbase/nf-winbase-gettapeparameters) -Funktion aufrufen und das Block-Bit der Band \_ Laufwerk \_ Variablen des \_ **featureslow** -Members der zurückgegebenen [**Tape \_ get \_ Drive \_ Parameters**](/windows/desktop/api/Winnt/ns-winnt-tape_get_drive_parameters) -Struktur überprüfen.
2.  Geben Sie den Blockgrößen Modus der Variablen an, indem Sie die [**settapeparameters**](/windows/desktop/api/Winbase/nf-winbase-settapeparameters) -Funktion aufrufen, und legen Sie den **Block Size** -Member der [**Tape \_ Set \_ Media \_ Parameters**](/windows/desktop/api/Winnt/ns-winnt-tape_set_media_parameters) -Struktur auf NULL fest. Verwenden Sie dann " [**Infofile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " oder " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile) ", um die Datei Daten zu lesen oder zu schreiben.

Wenn die [**Datei "Infofile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " auf ein Datei Zeichen stößt, werden die Daten bis zum Datei Zeichen gelesen, und die Funktion schlägt fehl. (Die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt einen Fehlercode zurück, der den Typ der gefundenen Datei Markierung angibt.) Das Betriebssystem verschiebt das Band hinter das Datei Zeichen, und eine Anwendung kann die **ReadFile-Datei** erneut abrufen, um den Vorgang fortzusetzen.

" [**Infofile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " und "Write [**File**](/windows/desktop/api/fileapi/nf-fileapi-writefile) " lesen und schreiben nur den Datenstrom. Die Funktionen [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) und [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) lesen und schreiben alle Streams, die einer Datei zugeordnet sind. Dazu zählen Daten, erweiterte Attribute, Sicherheit und alternative Datenströme. Die Sicherheits-und alternativen Datenströme sind nur für die NTFS-Dateisystem Partition relevant.

Die [**BackupSeek**](/windows/desktop/api/Winbase/nf-winbase-backupseek) -Funktion sucht vorwärts in einer Datei, auf die zunächst von [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) oder [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite)zugegriffen wurde. Diese Funktion ermöglicht einer Anwendung das Überspringen von Informationen, die Zugriffsfehler verursachen.

Wenn eine Anwendung nur auf die Datei Daten zugreifen muss, sollte Sie "read [**File**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " und " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile)" verwenden. Diese Funktionen können auch alternative Datenströme lesen, [**Wenn die Streams mithilfe der Funktion "**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) -Funktion" erstellt wurden.

Eine Band Sicherungs Anwendung muss [**BackupRead**](/windows/desktop/api/Winbase/nf-winbase-backupread) und [**BackupWrite**](/windows/desktop/api/Winbase/nf-winbase-backupwrite) verwenden, um alle Informationen in einer Datei zu kopieren. Diese Funktionen lesen oder schreiben jedoch keine Datei Merkmale, wie z. b. Attribute, Datei Erstellungszeit usw. Anwendungen müssen die Dateieingabe-und-Ausgabefunktionen, wie z. b. [**getfileattribute**](/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa) und [**setfileattribute**](/windows/desktop/api/fileapi/nf-fileapi-setfileattributesa), verwenden, um diese Werte abzurufen und festzulegen.

 

 