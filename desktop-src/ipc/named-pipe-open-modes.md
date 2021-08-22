---
description: Der Pipeserver gibt den Pipezugriffs-, Überlappungs- und Schreibmodus im dwOpenMode-Parameter der CreateNamedPipe-Funktion an. Die Pipeclients können diese offenen Modi für ihre Pipehandles mithilfe der CreateFile-Funktion angeben.
ms.assetid: 88824566-93c7-4941-a4fc-3a7ae9a332a4
title: Named Pipe Open Modes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d7fe3f843a157e69d8b938630e5eb9efa95035960cb6578325be6bddd5d93c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451260"
---
# <a name="named-pipe-open-modes"></a>Named Pipe Open Modes

Der Pipeserver gibt den Pipezugriffs-, Überlappungs- und Schreibmodus im *dwOpenMode-Parameter* der [**CreateNamedPipe-Funktion**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) an. Die Pipeclients können diese offenen Modi für ihre Pipehandles mithilfe der [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) angeben.

## <a name="access-mode"></a>Zugriffsmodus

Das Festlegen des Pipezugriffsmodus entspricht der Angabe des Lese- oder Schreibzugriffs, der den Handles des Pipeservers zugeordnet ist. Die folgende Tabelle zeigt das entsprechende generische Zugriffsrecht für jeden Zugriffsmodus, den Sie mit [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)angeben können.



| Zugriffsmodus            | Entsprechendes generisches Zugriffsrecht |
|------------------------|---------------------------------|
| EINGEHENDER \_ PIPEZUGRIFF \_  | GENERISCHER \_ LESE-                   |
| AUSGEHENDER \_ PIPEZUGRIFF \_ | GENERISCHER \_ SCHREIBVORGANG                  |
| PIPEZUGRIFF \_ \_ DUPLEX   | GENERISCHER \_ \| GENERISCHER \_ LESESCHREIBVORGANG |



 

Wenn der Pipeserver eine Pipe mit PIPE \_ ACCESS \_ INBOUND erstellt, ist die Pipe für den Pipeserver schreibgeschützt und für den Pipeclient schreibgeschützt. Wenn der Pipeserver eine Pipe mit PIPE \_ ACCESS \_ OUTBOUND erstellt, ist die Pipe schreibgeschützt für den Pipeserver und schreibgeschützt für den Pipeclient. Eine Pipe, die mit PIPE ACCESS DUPLEX erstellt \_ \_ wurde, ist sowohl für den Pipeserver als auch für den Pipeclient lese-/schreibgeschützt.

Pipeclients, die [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) zum Herstellen einer Verbindung mit einer Named Pipe verwenden, müssen ein Zugriffsrecht im *dwDesiredAccess-Parameter* angeben, der mit dem vom Pipeserver angegebenen Zugriffsmodus kompatibel ist. Beispielsweise muss ein Client GENERIC READ-Zugriff angeben, \_ um ein Handle für eine Pipe zu öffnen, die der Pipeserver mit PIPE ACCESS OUTBOUND erstellt \_ \_ hat. Die Zugriffsmodi müssen für alle Instanzen einer Pipe identisch sein.

Um Pipeattribute wie den Lese- oder Blockierungsmodus zu lesen, muss das Pipehandle über das \_ FILE READ \_ ATTRIBUTES-Zugriffsrecht verfügen. Zum Schreiben von Pipeattributen muss das Pipehandle über das \_ FILE WRITE \_ ATTRIBUTES-Zugriffsrecht verfügen. Diese Zugriffsrechte können mit dem generischen Zugriffsrecht kombiniert werden, das für die Pipe geeignet ist: GENERISCHES \_ LESEN mit FILE WRITE ATTRIBUTES für eine \_ \_ schreibgeschützte Pipe oder GENERISCHES \_ SCHREIBEN mit FILE READ ATTRIBUTES für eine \_ \_ schreibgeschützte Pipe. Das Einschränken von Zugriffsrechten auf diese Weise bietet eine höhere Sicherheit für die Pipe.

## <a name="overlapped-mode"></a>Überlappender Modus

Im überlappenden Modus können Funktionen, die lange Lese-, Schreib- und Verbindungsvorgänge ausführen, sofort zurückgeben. Dadurch kann der Thread andere Vorgänge ausführen, während ein zeitaufwändiger Vorgang im Hintergrund ausgeführt wird. Verwenden Sie das FLAG FILE \_ FLAG OVERLAPPED, um den Überlappungsmodus \_ anzugeben. Weitere Informationen finden Sie unter [Synchrone und überlappende Eingabe und Ausgabe.](synchronous-and-overlapped-input-and-output.md)

Mit der [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) kann der Pipeclient den überlappenden Modus (FILE \_ FLAG \_ OVERLAPPED) für seine Pipehandles mithilfe des *parameters dwFlagsAndAttributes* festlegen.

## <a name="write-through-mode"></a>Write-Through-Modus

Geben Sie den Schreibmodus mit FILE \_ FLAG \_ WRITE THROUGH \_ an. Dieser Modus wirkt sich nur auf Schreibvorgänge in Bytetyppipes zwischen Pipeclients und Pipeservern auf verschiedenen Computern aus. Im Schreibmodus geben die Funktionen, die in eine Named Pipe schreiben, erst dann zurück, wenn die Daten über das Netzwerk und in den Puffer der Pipe auf dem Remotecomputer übertragen werden. Der Schreibmodus ist nützlich für Anwendungen, die für jeden Schreibvorgang eine Synchronisierung erfordern.

Wenn der Schreibmodus nicht aktiviert ist, erhöht das System die Effizienz von Netzwerkvorgängen, indem Daten gepuffert werden, bis sich eine Mindestanzahl von Bytes angesammelt hat oder bis ein maximaler Zeitraum abgelaufen ist. Die Pufferung ermöglicht es dem System, mehrere Schreibvorgänge in einer einzigen Netzwerkübertragung zu kombinieren. Dies bedeutet, dass ein Schreibvorgang erfolgreich abgeschlossen werden kann, nachdem das System die Daten in den ausgehenden Puffer gestellt hat, aber bevor das System sie über das Netzwerk überträgt.

Mit der [**CreateFile-Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) kann der Pipeclient den Schreibmodus (FILE \_ FLAG WRITE \_ \_ THROUGH) für seine Pipehandles mithilfe des *parameters dwFlagsAndAttributes* festlegen. Der Schreibmodus eines Pipehandle kann nicht mehr geändert werden, nachdem das Pipehandle erstellt wurde. Der Schreibmodus kann sich für Server- und Clienthandles von derselben Pipeinstanz unterscheiden.

Ein Pipeclient kann die [**SetNamedPipeHandleState-Funktion**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) verwenden, um die Anzahl der Bytes und den Time out-Zeitraum vor der Übertragung für eine Pipe zu steuern, für die der Schreibmodus deaktiviert ist. Für eine schreibgeschützte Pipe muss das Pipehandle mit den Zugriffsrechten GENERIC READ und FILE WRITE ATTRIBUTES geöffnet \_ \_ \_ werden.

 

 
