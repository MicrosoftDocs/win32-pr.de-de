---
description: Ein Prozess verwendet die CreateFile-Funktion, um ein Handle für eine Kommunikationsressource zu öffnen.
ms.assetid: eaef6067-97a6-40c4-84ec-c0d86af6bb4a
title: Kommunikationsressourcenhandles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 585d7ab257c36bc288a494c2e55d9f192749e9742b0eb88ead6d0b0ffad919cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768760"
---
# <a name="communications-resource-handles"></a>Kommunikationsressourcenhandles

Ein Prozess verwendet die [**CreateFile-Funktion,**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) um ein Handle für eine Kommunikationsressource zu öffnen. Wenn Sie beispielsweise COM1 angeben, wird ein Handle für einen seriellen Anschluss geöffnet, und LPT1 öffnet ein Handle für einen parallelen Port. Wenn die angegebene Ressource derzeit von einem anderen Prozess verwendet wird, schlägt **CreateFile** fehl. Jeder Thread des Prozesses kann das von **CreateFile** zurückgegebene Handle verwenden, um die Ressource in einer der Funktionen zu identifizieren, die auf die Ressource zugreifen.

Wenn der Prozess [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) aufruft, um eine Kommunikationsressource zu öffnen, gibt er die folgenden Attribute an:

-   Welche Art von Lese-/Schreibzugriff für die angegebene Ressource vorhanden ist.
-   Gibt an, ob das Handle von untergeordneten Prozessen geerbt werden kann.
-   Gibt an, ob das Handle in überlappenden (asynchronen) E/A-Vorgängen verwendet werden kann. (Eine Beschreibung überlappender Vorgänge finden Sie unter [Synchronisierung](/windows/desktop/Sync/synchronization).)

Wenn der Prozess [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) verwendet, um eine Kommunikationsressource zu öffnen, müssen bestimmte Werte für die folgenden Parameter angegeben werden:

-   Der *fdwShareMode-Parameter* muss 0 (null) sein, um die Ressource für den exklusiven Zugriff zu öffnen.
-   Der *fdwCreate-Parameter* muss das OPEN \_ EXISTING-Flag angeben.
-   Der *hTemplateFile-Parameter* muss **NULL** sein.

Wenn [**Sie CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) verwenden, um ein Handle direkt für ein Gerät zu öffnen, muss eine Anwendung die Sonderzeichen " \\ \\ . " \\ verwenden, um das Gerät zu identifizieren. Um beispielsweise ein Handle für Laufwerk A zu öffnen, geben Sie \\ \\ an. \\ a: für den *lpszName-Parameter* von **CreateFile**. Der aufrufende Prozess kann das Handle in der [**DeviceIoControl-Funktion**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) verwenden, um Steuerungscodes an das Gerät zu senden.

 

 
