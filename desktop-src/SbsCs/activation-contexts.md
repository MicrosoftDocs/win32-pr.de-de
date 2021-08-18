---
description: Aktivierungskontexte sind Datenstrukturen im Arbeitsspeicher, die Informationen enthalten, mit denen das System eine Anwendung umleiten kann, um eine bestimmte DLL-Version, EINE COM-Objektinstanz oder eine benutzerdefinierte Fensterversion zu laden.
ms.assetid: 5416f8c0-d99b-4a5d-a689-a47bd0cf1a88
title: Aktivierungskontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21aaf2c4d2e4fc0f3ef691406e663dc5efac44a9d0b34880596d21cac8a5f621
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142543"
---
# <a name="activation-contexts"></a>Aktivierungskontexte

[*Aktivierungskontexte*](a-sbscs-gly.md) sind Datenstrukturen im Arbeitsspeicher, die Informationen enthalten, mit denen das System eine Anwendung umleiten kann, um eine bestimmte DLL-Version, EINE COM-Objektinstanz oder eine benutzerdefinierte Fensterversion zu laden. Ein Abschnitt des Aktivierungskontexts kann DLL-Umleitungsinformationen enthalten, die vom DLL-Ladeprogramm verwendet werden. Ein anderer Abschnitt kann COM-Serverinformationen enthalten. Die Aktivierungskontextfunktionen verwenden, erstellen, aktivieren und deaktivieren Aktivierungskontexte. Die Aktivierungsfunktionen können die Bindung einer Anwendung an Objekte mit Versionsnamen umleiten, die bestimmte DLL-Versionen, Fensterklassen, COM-Server, Typbibliotheken und Schnittstellen angeben. Weitere Informationen zu den Aktivierungskontextfunktionen und -strukturen finden Sie in der [Referenz zum Aktivierungskontext.](activation-context-reference.md)

Ab Windows XP ermöglichen Aktivierungskontextfunktionen Windows die Verwendung von Informationen in [Manifesten,](manifests.md) um Objekte mit Versionsnamen zu erstellen. Wenn eine Anwendung einen Prozess durch Aufrufen von [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)erstellt, überprüft Windows, ob ein [Anwendungsmanifest](application-manifests.md)vorhanden ist. Wenn ein Manifest vorhanden ist, verwendet Windows die Informationen im Manifest, um den Aktivierungskontext aufzufüllen. Da Manifeste die Abhängigkeit einer Anwendung von [parallelen Assemblyversionen](about-side-by-side-assemblies-.md) beschreiben, werden Objekte, die ohne Versionen im Manifest angegeben werden, mit Versionsnamen benannten Objekten zugeordnet. Beispielsweise kann das Manifest DLLs, Dateien, Fensterklassen, COM-Server, Typbibliotheken und Schnittstellen beschreiben.

Wenn ein globales Objekt innerhalb des Aktivierungskontexts erstellt wird, gibt das System dem Objekt automatisch einen versionsspezifischen Namen, indem es das Manifest abruft. Wenn die Anwendung ausgeführt wird und ein benanntes Objekt anfordert, ruft sie das Versionsobjekt ab. Dadurch können mehrere Versionen eines Codemoduls gleichzeitig auf dem System ausgeführt werden, ohne sich gegenseitig zu beeinträchtigen. Beispielsweise verwendet [Windows Shell](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)) ein Manifest, um eine Abhängigkeit von Version 6.0 von COMCTL32 zu beschreiben und Versionen von Fensterklassen zu erstellen.

Wenn eine Anwendung eine Ressource durch Aufrufen von [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)erstellt, gibt der Prozess einen Klassennamen für diese Funktion an. Der Aufruf von [**GetCurrentActCtx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx) ruft den aktuellen Aktivierungskontext ab und überprüft, ob eine Zuordnung für den angegebenen Klassennamen vorhanden ist. Wenn eine Zuordnung vorhanden ist, wird diese Version des aufrufenden Prozesses verwendet, um die Zuordnung aufzulösen und den versionsspezifischen Klassennamen bereitzustellen. Windows erstellt ein Fenster mit der Fensterprozedur, den Stilen und anderen Attributen, die diesem Klassennamen und dieser Version zugeordnet sind.

Der Aktivierungskontext wird in den meisten Fällen vom System verwaltet. Anwendungsentwickler und Assemblyanbieter müssen in der Regel keine Aufrufe des Stapels durchführen. Anwendungen können einen Aktivierungskontext verwalten, indem sie den Aktivierungskontext direkt aufrufen. Weitere Informationen finden Sie unter [Verwenden der Aktivierungskontext-API.](using-the-activation-context-api.md)

 

 
