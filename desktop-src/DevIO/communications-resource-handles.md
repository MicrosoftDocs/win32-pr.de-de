---
description: Ein Prozess verwendet die Funktion "Funktion", um ein Handle für eine Kommunikations Ressource zu öffnen.
ms.assetid: eaef6067-97a6-40c4-84ec-c0d86af6bb4a
title: Kommunikationsressourcenhandles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fc041f6125d93a1c52f3e17b77c96f35825c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393086"
---
# <a name="communications-resource-handles"></a>Kommunikationsressourcenhandles

Ein Prozess [**verwendet die Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "Funktion", um ein Handle für eine Kommunikations Ressource zu öffnen. Wenn Sie z. b. COM1 angeben, wird ein Handle für einen seriellen Anschluss geöffnet, und LPT1 öffnet ein Handle für einen parallelen Port. Wenn die angegebene Ressource zurzeit von einem anderen Prozess verwendet wird, schlägt " **deatefile** " fehl. Jeder Thread des Prozesses kann das von " **kreatefile** " zurückgegebene Handle verwenden, um die Ressource in einer der Funktionen zu identifizieren, die auf die Ressource zugreifen.

Wenn der Prozess " [**kreatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " aufruft, um eine Kommunikations Ressource zu öffnen, gibt er die folgenden Attribute an:

-   Der Typ des Lese-/Schreibzugriffs, der für die angegebene Ressource vorhanden ist.
-   Gibt an, ob das Handle von untergeordneten Prozessen geerbt werden kann.
-   Gibt an, ob das Handle in überlappenden (asynchronen) e/a-Vorgängen verwendet werden kann. (Eine Beschreibung der überlappenden Vorgänge finden Sie unter [Synchronisierung](/windows/desktop/Sync/synchronization).)

Wenn der Prozess zum Öffnen einer Kommunikations Ressource " [**kreatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " verwendet, müssen bestimmte Werte für die folgenden Parameter angegeben werden:

-   Der Parameter " *fidwsharemode* " muss NULL sein, um die Ressource für exklusiven Zugriff zu öffnen.
-   Der Parameter " *sdwcreate* " muss das Open \_ vorhandene-Flag angeben.
-   Der *htemplatefile* -Parameter muss **null** sein.

Wenn Sie mit " [**anatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " ein Handle direkt auf einem Gerät öffnen, muss eine Anwendung die Sonderzeichen " \\ \\ ." verwenden, \\ um das Gerät zu identifizieren. Um z. b. ein Handle zum Steuern eines zu öffnen, geben Sie an \\ \\ . \\ a: für den *lpszname* -Parameter von " **kreatefile**". Der aufrufenden Prozess kann das Handle in der [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) -Funktion verwenden, um Steuerungs Codes an das Gerät zu senden.

 

 
