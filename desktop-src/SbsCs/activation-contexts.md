---
description: Aktivierungs Kontexte sind Datenstrukturen im Arbeitsspeicher mit Informationen, die das System zum Umleiten einer Anwendung verwenden kann, um eine bestimmte dll-Version, com-Objektinstanz oder eine benutzerdefinierte Fensterversion zu laden.
ms.assetid: 5416f8c0-d99b-4a5d-a689-a47bd0cf1a88
title: Aktivierungs Kontexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f1f20d747f63ba71eee73fc17c0d5543003e5f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345329"
---
# <a name="activation-contexts"></a>Aktivierungs Kontexte

[*Aktivierungs Kontexte*](a-sbscs-gly.md) sind Datenstrukturen im Arbeitsspeicher mit Informationen, die das System zum Umleiten einer Anwendung verwenden kann, um eine bestimmte dll-Version, com-Objektinstanz oder eine benutzerdefinierte Fensterversion zu laden. Ein Abschnitt des Aktivierungs Kontexts kann dll-Umleitungs Informationen enthalten, die vom dll-Lade Modul verwendet werden. ein anderer Abschnitt enthält möglicherweise com-Server Informationen. Die Aktivierungs Kontextfunktionen verwenden, erstellen, aktivieren und deaktivieren Aktivierungs Kontexte. Die Aktivierungs Funktionen können die Bindung einer Anwendung an Versions benannte Objekte umleiten, die bestimmte dll-Versionen, Fenster Klassen, com-Server, Typbibliotheken und Schnittstellen angeben. Weitere Informationen zu den Aktivierungs Kontextfunktionen und-Strukturen finden Sie in der [Aktivierungs Kontext Referenz](activation-context-reference.md).

Ab Windows XP ermöglichen Aktivierungs Kontextfunktionen Windows die Verwendung von Informationen in [Manifesten](manifests.md) , um Versions benannte Objekte zu erstellen. Wenn eine Anwendung einen Prozess durch Aufrufen von [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)erstellt, prüft Windows, ob ein [Anwendungs Manifest](application-manifests.md)vorhanden ist. Wenn ein Manifest vorhanden ist, verwendet Windows die Informationen im Manifest, um den Aktivierungs Kontext aufzufüllen. Da Manifeste die Abhängigkeit einer [Anwendung von parallelen](about-side-by-side-assemblies-.md) Assemblyversionen beschreiben, werden Objekte, die ohne Versionen im Manifest angegeben sind, benannten Objekten zugeordnet. Im Manifest können z. b. DLLs, Dateien, Fenster Klassen, com-Server, Typbibliotheken und Schnittstellen beschrieben werden.

Wenn ein globales Objekt im Aktivierungs Kontext erstellt wird, erhält das System automatisch einen Versions spezifischen Namen, indem er das Manifest konsultiert. Wenn die Anwendung ausgeführt wird und ein benanntes Objekt anfordert, ruft Sie das Versions benannte Objekt ab. Dadurch können mehrere Versionen eines Codemodul gleichzeitig auf dem System ausgeführt werden, ohne sich gegenseitig zu stören. Beispielsweise verwendet [Windows Shell](/previous-versions/windows/desktop/legacy/bb776778(v=vs.85)) ein Manifest, um eine Abhängigkeit von Version 6,0 von ComCtl32 und zum Erstellen von Versionen von Fenster Klassen zu beschreiben.

Wenn eine Anwendung eine Ressource durch Aufrufen von [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)erstellt, gibt der Prozess einen Klassennamen für diese Funktion an. Der [**getcurrentactctx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx) -Befehl ruft den aktuellen Aktivierungs Kontext ab und überprüft, ob eine Zuordnung für den angegebenen Klassennamen vorhanden ist. Wenn eine Zuordnung vorhanden ist, wird diese Version des aufrufenden Prozesses verwendet, um die Zuordnung aufzulösen und den Versions spezifischen Klassennamen bereitzustellen. Windows erstellt ein Fenster mit den Fenster Prozeduren, Stilen und anderen Attributen, die mit diesem Klassennamen und dieser Version verknüpft sind.

Der Aktivierungs Kontext wird in den meisten Fällen vom System verwaltet. Anwendungsentwickler und Assemblyanbieter müssen häufig keine Aufrufe an den Stapel durchführen. Anwendungen können einen Aktivierungs Kontext verwalten, indem Sie den Aktivierungs Kontext direkt aufrufen. Weitere Informationen finden Sie unter [Verwenden der Aktivierungs Kontext-API](using-the-activation-context-api.md).

 

 
