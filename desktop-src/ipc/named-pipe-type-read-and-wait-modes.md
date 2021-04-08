---
description: Der Pipeserver gibt den pipetypmodus, den Lesemodus und den Wartemodus im dwpipemode-Parameter der Funktion "up-amedpipe" an. Pipeclients können diese Pipe-Modi für Ihre Pipehandles mithilfe der Funktion "-Funktion" (Funktion) angeben.
ms.assetid: 07cf9d06-6265-47f4-a9f1-c19c06cc5f9f
title: Named Pipe-Typ, Lese-und warte Modi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b116e5ca9357a65a6d63549b96065843b046d479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861920"
---
# <a name="named-pipe-type-read-and-wait-modes"></a>Named Pipe-Typ, Lese-und warte Modi

Der Pipeserver gibt den pipetypmodus, den Lesemodus und den Wartemodus im *dwpipemode* -Parameter der Funktion "up- [**amedpipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) " an. Pipeclients können diese Pipe-Modi für Ihre Pipehandles [**mithilfe der Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "-Funktion" (Funktion) angeben.

## <a name="type-mode"></a>Typmodus

Der typmodus einer Pipe bestimmt, wie Daten in eine Named Pipe geschrieben werden. Daten können über eine Named Pipe entweder als Bytestream oder als Nachrichtenstrom übertragen werden. Der Pipeserver gibt den Pipetyp an, wenn [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) aufgerufen wird, um eine Instanz einer Named Pipe zu erstellen. Die typmodi müssen für alle Instanzen einer Pipe identisch sein.

Um eine Bytetyp-Pipe zu erstellen, geben Sie Pipe- \_ Typ Byte an, \_ oder verwenden Sie den Standardwert. Die Daten werden in die Pipe als Bytestream geschrieben, und das System unterscheidet nicht zwischen den bytes, die in verschiedenen Schreibvorgängen geschrieben werden.

Geben Sie zum Erstellen einer Pipe für den Nachrichtentyp die Pipe- \_ \_ typnachricht an. Das System behandelt die in jedem Schreibvorgang geschriebenen Bytes als Nachrichten Einheit an die Pipe. Das System führt immer Schreibvorgänge für Nachrichtentyp Pipes aus, als ob der Lese-/Schreibmodus aktiviert wäre.

## <a name="read-mode"></a>Lesemodus

Der Lesemodus einer Pipe bestimmt, wie Daten aus einem Named Pipe gelesen werden. Der Pipeserver gibt den anfänglichen Lesemodus für ein Pipehandle an, wenn [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)aufgerufen wird. Daten können im Byte Lese Modus oder im Nachrichten Lese Modus gelesen werden. Ein Handle für eine Bytetyp-Pipe kann nur im Byte Lese Modus vorliegen. Ein Handle für eine Nachrichtentyp Pipe kann entweder im Byte-Lese-oder im Nachrichten Lese Modus vorliegen. Bei einer Pipe für den Nachrichtentyp kann der Lesemodus für die Server-und Client Handles der gleichen Pipe-Instanz unterschiedlich sein.

Um das Pipehandle im Byte Lese Modus zu erstellen, geben Sie Pipe- \_ lesemodusbyte an, \_ oder verwenden Sie den Standardwert. Daten werden aus der Pipe als Byte Datenstrom gelesen. Ein Lesevorgang wurde erfolgreich abgeschlossen, wenn alle verfügbaren Bytes in der Pipe gelesen wurden oder wenn die angegebene Anzahl von Bytes gelesen wird.

Um das Pipehandle im Nachrichten Lese Modus zu erstellen, geben Sie eine Pipe- \_ lesemodusmeldung an \_ . Daten werden aus der Pipe als Nachrichtenstrom gelesen. Ein Lesevorgang wurde nur erfolgreich abgeschlossen, wenn die gesamte Nachricht gelesen wurde. Wenn die angegebene Anzahl der zu lesenden Bytes kleiner ist als die Größe der nächsten Nachricht, liest die Funktion so viel von der Nachricht wie möglich vor der Rückgabe von NULL (die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt Fehler \_ Weitere \_ Daten zurück). Der Rest der Nachricht kann mit einem anderen Lesevorgang gelesen werden.

Bei einem Pipe-Client wird das von " [**kreatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " zurückgegebene Pipehandle zunächst immer im Byte Lese Modus ausgeführt. Sowohl Pipeclients als auch Pipe-Server können die [**setnamedpipelenker State**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) -Funktion verwenden, um den Lesemodus eines Pipehandles zu ändern. Das Pipehandle muss über das \_ \_ Zugriffsrecht Datei Schreib Attribute verfügen.

## <a name="wait-mode"></a>Wartemodus

Der Wartemodus eines Pipehandles bestimmt, wie die Funktionen [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile)und [**connectnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) lange Vorgänge verarbeiten. Im blockierenden Wartemodus warten die Funktionen unbegrenzt, bis ein Prozess am anderen Ende der Pipe abgeschlossen ist, um einen Vorgang abzuschließen. Im nicht blockierenden Wartemodus geben die Funktionen in Situationen, in denen andernfalls eine unbegrenzte Wartezeit erforderlich wäre, sofort zurück.

Ein Vorgang zum [**Lesen von Dateien**](/windows/desktop/api/fileapi/nf-fileapi-readfile) wird vom Wartemodus eines Pipehandles beeinflusst, wenn die Pipe leer ist. Bei einem blockierenden Wait-Handle wird der Vorgang nicht erfolgreich abgeschlossen, bis Daten von einem Thread verfügbar sind, der an das andere Ende der Pipe schreibt. Wenn ein nicht blockierendes Wait-Handle verwendet wird, gibt die Funktion sofort NULL zurück, und die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt fehlerhafte \_ \_ Daten zurück.

Der Wartemodus eines Pipehandles wirkt sich auf einen Vorgang zum Schreiben von [**Schreib Dateien**](/windows/desktop/api/fileapi/nf-fileapi-writefile) aus, wenn nicht genügend Speicherplatz im Puffer der Pipe vorhanden ist. Bei einem blockierenden Wait-Handle kann der Schreibvorgang erst erfolgreich ausgeführt werden, wenn im Puffer von einem Thread, der vom anderen Ende der Pipe liest, genügend Speicherplatz erstellt wird. Bei einem nicht blockierenden Wait-Handle gibt der Schreibvorgang einen Wert ungleich 0 (null) zurück, ohne dass bytes (für eine Nachrichtentyp Pipe) geschrieben werden, oder nachdem so viele Bytes geschrieben wurden, wie der Puffer enthält (für eine Pipe im Bytetyp).

Der Wartemodus eines Pipehandles wirkt sich auf einen [**connectnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) -Vorgang aus, wenn kein Client verbunden ist oder darauf wartet, eine Verbindung mit der Pipe-Instanz herzustellen. Bei einem blockierenden Wait-Handle ist der Verbindungsvorgang erst erfolgreich, wenn ein Pipe-Client eine Verbindung mit der Pipe-Instanz herstellt, indem er entweder die [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) -oder die [**callnamedpipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) -Funktion aufruft. Bei einem nicht blockierenden Wait-Handle gibt der Verbindungsvorgang NULL sofort zurück, und die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion gibt die fehlerpipe zurück, die überwacht wird \_ \_ .

Standardmäßig werden alle Named Pipe Handles [**, die von**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) [**der Funktion "**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " von "" von "" "" "" "" "" "" "" "" "," "" Um die Pipe im nicht blockierenden Wartemodus zu erstellen, gibt der Pipeserver \_ beim Aufrufen von **CreateNamedPipe** den Wert Pipe nowait an.

Sowohl Pipeclients als auch Pipe-Server können den Wartemodus eines Pipehandles ändern, indem Sie entweder Pipe- \_ Wait oder Pipe \_ nowait in einem Aufrufen der [**setnamedpipelenker State**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) -Funktion angeben.

> [!Note]  
> Der nicht blockierende Wartemodus wird aus Kompatibilitätsgründen mit der Microsoft LAN Manager-Version 2,0 unterstützt. Dieser Modus sollte nicht verwendet werden, um überlappende Eingaben und Ausgaben (e/a) mit Named Pipes zu erzielen. Überlappende e/a-Vorgänge sollten stattdessen verwendet werden, da zeitaufwändige Vorgänge im Hintergrund ausgeführt werden können, nachdem die Funktion zurückgegeben wurde. Weitere Informationen zu überlappenden e/a-Vorgängen finden Sie unter [synchrone und überlappende Eingabe und Ausgabe](synchronous-and-overlapped-input-and-output.md).

 

 

 
