---
description: Der Pipeserver gibt die Pipe-Zugriffs-, Überlappungs-und Schreibvorgänge im dwopenmode-Parameter der Funktion "up-amedpipe" an. Die Pipeclients können diese geöffneten Modi für Ihre Pipehandles mithilfe der Funktion "-Funktion" (Funktion) angeben.
ms.assetid: 88824566-93c7-4941-a4fc-3a7ae9a332a4
title: Named Pipe-Öffnungs Modi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f51d41ea98a47a269634b06ccdad869bd649fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960674"
---
# <a name="named-pipe-open-modes"></a>Named Pipe-Öffnungs Modi

Der Pipeserver gibt die Pipe-Zugriffs-, Überlappungs-und Schreibvorgänge im *dwopenmode* -Parameter der Funktion "up- [**amedpipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) " an. Die Pipeclients können diese geöffneten Modi für Ihre Pipehandles [**mithilfe der Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "-Funktion" (Funktion) angeben.

## <a name="access-mode"></a>Zugriffsmodus

Das Festlegen des pipezugriffsmodus entspricht dem Angeben des Lese-oder Schreibzugriffs, der den Handles des Pipeservers zugeordnet ist. In der folgenden Tabelle wird das äquivalente allgemeine Zugriffsrecht für jeden Zugriffsmodus angezeigt, den Sie mit " [**kreatenamedpipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)" angeben können.



| Zugriffsmodus            | Äquivalente generische Zugriffsrechte |
|------------------------|---------------------------------|
| senkrechter Pipe- \_ Zugriff \_  | generischer \_ Lesevorgang                   |
| ausgehende Pipe- \_ Zugriff \_ | generischer \_ Schreibvorgang                  |
| \_pipezugriffsduplex \_   | generischer \_ Lese \| generischer \_ Schreibvorgang |



 

Wenn der Pipeserver eine Pipe mit einem eingehenden Pipe \_ -Zugriff erstellt \_ , ist die Pipe für den Pipeserver schreibgeschützt und für den Pipeclient schreibgeschützt. Wenn der Pipeserver eine Pipe mit \_ ausgehendem Pipe-Zugriff erstellt \_ , ist die Pipe schreibgeschützt für den Pipeserver und schreibgeschützt für den Pipeclient. Eine Pipe, die mit Pipe \_ -Zugriffs Duplex erstellt wurde, \_ wird sowohl für den Pipeserver als auch für den Pipeclient gelesen/geschrieben.

Mithilfe von Pipe- [**Clients, die**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) mithilfe von "" eine Verbindung mit einem Named Pipe herstellen, muss im Parameter " *dwDesiredAccess* " ein Zugriffsrecht angegeben werden, der mit dem vom Pipeserver angegebenen Zugriffsmodus kompatibel ist. Beispielsweise muss ein Client generischen \_ Lesezugriff angeben, um ein Handle für eine Pipe zu öffnen, die der Pipeserver mit \_ ausgehendem Pipe-Zugriff erstellt hat \_ . Die Zugriffs Modi müssen für alle Instanzen einer Pipe identisch sein.

Zum Lesen von pipeattributen, wie z. b. dem Lesemodus oder dem Blockierungs Modus, muss das Pipehandle über die Datei \_ Lese Attribute-Zugriffsberechtigung verfügen \_ . um pipeattribute schreiben zu können, muss das Pipehandle über das \_ \_ Zugriffsrecht Datei Schreib Attribute verfügen. Diese Zugriffsrechte können mit dem generischen Zugriffsrecht kombiniert werden, das für die Pipe geeignet ist: generisches \_ Lesen mit Datei \_ Schreib \_ Attributen für eine schreibgeschützte Pipe oder generisches \_ Schreiben mit Datei \_ Lese \_ Attributen für eine schreibgeschützte Pipe. Das Einschränken von Zugriffsrechten auf diese Weise bietet eine bessere Sicherheit für die Pipe.

## <a name="overlapped-mode"></a>Überlappende Modus

Im überlappenden Modus können Funktionen, die lange Lese-, Schreib-und Verbindungs Vorgänge ausführen, sofort zurückgeben. Dadurch kann der Thread andere Vorgänge ausführen, während ein zeitaufwändiger Vorgang im Hintergrund ausgeführt wird. Um den überlappenden Modus anzugeben, verwenden Sie das überlappende \_ Flag Dateiflag \_ . Weitere Informationen finden Sie unter [synchrone und überlappende Eingabe und Ausgabe](synchronous-and-overlapped-input-and-output.md).

Die [**Funktion "**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) Funktion" ermöglicht dem Pipe-Client das Festlegen des überlappenden Modus (Dateiflag \_ überlappen \_ ) für die zugehörigen Pipehandles mithilfe des Parameters " *dwflagsandattributs* ".

## <a name="write-through-mode"></a>Write-Through Modus

Geben Sie den Lese-/Schreibmodus mit einem \_ Dateiflag an \_ \_ . Dieser Modus wirkt sich nur auf Schreibvorgänge zwischen Pipeclients und pipeservern auf verschiedenen Computern aus. Im Write-Through-Modus geben die Funktionen, die in eine Named Pipe schreiben, erst dann zurück, wenn die Daten über das Netzwerk und in den Puffer der Pipe auf dem Remote Computer übertragen werden. Der Lese-/Schreibmodus ist nützlich für Anwendungen, die für jeden Schreibvorgang eine Synchronisierung erfordern.

Wenn der Lese-/Schreibmodus nicht aktiviert ist, erweitert das System die Effizienz von Netzwerk Vorgängen, indem Daten gepuffert werden, bis eine Mindestanzahl von Bytes kumuliert wurde oder bis ein maximaler Zeitraum abgelaufen ist. Durch die Pufferung kann das System mehrere Schreibvorgänge in einer einzelnen Netzwerkübertragung kombinieren. Dies bedeutet, dass ein Schreibvorgang erfolgreich abgeschlossen werden kann, nachdem das System die Daten in den ausgehenden Puffer eingefügt hat, jedoch bevor das System Sie über das Netzwerk überträgt.

Die [**Funktion "**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) Funktion" ermöglicht dem Pipe-Client das Festlegen des Lese-/Schreibmodus (Dateiflag- \_ \_ Schreibvorgang \_ ) für die Pipe-Handles mithilfe des Parameters " *dwflagsandattributs* ". Der Lese-/Schreibmodus eines Pipehandles kann nicht geändert werden, nachdem das Pipehandle erstellt wurde. Der Lese-/Schreibmodus kann für Server-und Client Handles in derselben Pipe-Instanz unterschiedlich sein.

Ein Pipe-Client kann die [**setnamedpipelenker State**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) -Funktion verwenden, um die Anzahl von Bytes und den Timeout Zeitraum vor der Übertragung für eine Pipe zu steuern, in der der Schreibmodus deaktiviert ist. Bei einer schreibgeschützten Pipe muss das Pipehandle mit den allgemeinen \_ Zugriffsrechten für Lese-und Datei \_ Schreib \_ Attribute geöffnet werden.

 

 
