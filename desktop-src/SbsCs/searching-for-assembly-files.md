---
description: Assemblydateien werden gesucht
ms.assetid: 6e6c1104-5cde-4c07-9ee2-d87062675dac
title: Assemblydateien werden gesucht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7be73b162ea41fd9eeb0a042a1fc2e202b8115
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217791"
---
# <a name="searching-for-assembly-files"></a>Assemblydateien werden gesucht

Aktivierungs Kontexte können dem Lade Programme helfen, Assemblydateien zu suchen. Wenn das Lade Modul nach einer Datei sucht, die anhand des Namens geladen werden soll, sucht es zuerst nach Dateien mit dem angegebenen Namen, auf die von Assemblys verwiesen wird, die Mitglieder des aktuell aktiven Aktivierungs Kontexts sind. Bei einem [**Suchpfad**](/windows/desktop/api/processenv/nf-processenv-searchpathw) -aufrufort werden diese Dateien auch zuerst gesucht. Dateien mit dem angegebenen Namen und dem aktuellen Aktivierungs Kontext werden gefunden und vor Dateien mit dem Namen im lokalen Verzeichnis oder in der PATH-Umgebungsvariablen geladen. Dies bedeutet, dass Sie beim Erstellen von Manifesten alle Dateien auflisten müssen, die Sie mit **SearchPath**, [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)oder statischen Importen verwenden möchten.

Beachten Sie, dass diese Dateien nicht automatisch gefunden werden, wenn Sie " [**deatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " oder andere Funktionen verwenden, die nicht nach Dateien suchen. Wenn Sie diese Dateien mit "up **File**" verwenden möchten, verwenden Sie zuerst " [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) ", um den Pfad zur isolierten Datei zu suchen, und verwenden Sie dann " **deatefile** " im zurückgegebenen Pfad.

Diese Methode der Dateisuche hilft dabei, isolierte Anwendungen voneinander getrennt zu halten, da sich mehrere Dateien mit demselben Namen nur durch ihre Zuordnung zu Assemblys mit unterschiedlichen Versionsnummern unterscheiden können. Das Betriebssystem kann die richtige Datei finden, die bei Datei Vorgängen verwendet werden soll.

Wenn eine DLL auf diese Weise mithilfe von [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)geladen wird, wird der Einstiegspunkt (DllMain) der dll aufgerufen, während der ursprüngliche Aktivierungs Kontext aktiv bleibt, es sei denn, die DLL selbst enthält ein Manifest an einer bestimmten Ressourcen-ID (isolationaware \_ Manifest-Ressourcen- \_ \_ ID oder 2).

 

 
