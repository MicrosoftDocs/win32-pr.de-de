---
description: Suchen nach Assemblydateien
ms.assetid: 6e6c1104-5cde-4c07-9ee2-d87062675dac
title: Suchen nach Assemblydateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b55614278d58913c8fb92371e302ffd71fd28b48b7828351d8ce6b37ae0eddc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884870"
---
# <a name="searching-for-assembly-files"></a>Suchen nach Assemblydateien

Aktivierungskontexte können dem Lader helfen, Assemblydateien zu finden. Wenn das Lader nach einer Datei sucht, die nach Namen geladen werden soll, sucht es zuerst nach Dateien mit dem angegebenen Namen, auf die von Assemblys verwiesen wird, die Mitglieder des derzeit aktiven Aktivierungskontexts sind. Bei einem Aufruf von [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) werden diese Dateien ebenfalls zuerst gesucht. Dateien mit dem angegebenen Namen und dem aktuellen Aktivierungskontext werden vor Dateien mit dem Namen im lokalen Verzeichnis oder in der PATH-Umgebungsvariablen gefunden und geladen. Dies bedeutet, dass Sie beim Erstellen von Manifesten alle Dateien auflisten müssen, die Sie mit **SearchPath,** [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)oder statischen Importen verwenden möchten.

Beachten Sie, dass diese Dateien nicht automatisch gefunden werden, wenn [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) oder andere Funktionen verwendet werden, die nicht nach Dateien suchen. Um diese Dateien mit **CreateFile zu** verwenden, verwenden Sie [**zuerst SearchPath,**](/windows/desktop/api/processenv/nf-processenv-searchpathw) um den Pfad zur isolierten Datei zu suchen, und verwenden Sie dann **CreateFile** für den zurückgegebenen Pfad.

Diese Methode der Dateisuche hilft, isolierte Anwendungen voneinander zu trennen, da sich mehrere Dateien mit demselben Namen dann nur durch ihre Zuordnung zu Assemblys unterschiedlicher Versionsnummern unterscheiden können. Das Betriebssystem kann die richtige Datei finden, die bei Dateivorgängen verwendet werden soll.

Wenn eine DLL auf diese Weise mit [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)geladen wird, wird der Einstiegspunkt dieser DLL (DllMain) aufgerufen, während der ursprüngliche Aktivierungskontext aktiv bleibt, es sei denn, die DLL selbst enthält ein Manifest an einer bestimmten Ressourcen-ID (ISOLATIONAWARE \_ MANIFEST RESOURCE ID oder \_ \_ 2).

 

 
