---
title: Installierbare Treiberfunktionen und-Meldungen
description: Installierbare Treiberfunktionen und-Meldungen
ms.assetid: f487705a-ae8e-4ea8-bfd5-9b0f6087ddbb
keywords:
- installierbare Treiber, Funktionen
- installierbare Treiber, Meldungen
- installierbare Treiber, opendriver-Funktion
- Opendriver-Funktion
- installierbare Treiber, benutzerdefinierte Meldungen
- Treiber Meldungen
- benutzerdefinierte Treiber Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66e6ebaac73bf8eb779119750cb390481152c3f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948701"
---
# <a name="installable-driver-functions-and-messages"></a>Installierbare Treiberfunktionen und-Meldungen

Sie können einen installierbaren Treiber aus einer Anwendung öffnen, indem Sie die [**opendriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) -Funktion verwenden. Diese Funktion erstellt eine Instanz des Treibers, lädt den Treiber in den Arbeitsspeicher, wenn keine andere Instanz vorhanden ist, und gibt das Handle der neuen Instanz zurück. Beim Öffnen eines installierbaren Treibers müssen Sie entweder den vollständigen Pfad des Treibers oder die Namen des Registrierungsschlüssels und des Werts angeben, die dem Treiber zugeordnet sind.

Sobald ein Treiber geöffnet ist, können Sie ihn zum Ausführen von Tasks leiten, indem Sie die [**senddrivermessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) -Funktion verwenden, um Treiber Nachrichten an den Treiber zu senden. Beispielsweise können Sie den Treiber weiterleiten, um das Konfigurations Dialogfeld anzuzeigen, indem Sie die [**drv- \_ configure**](drv-configure.md) -Nachricht senden. Vor dem Senden dieser Nachricht müssen Sie bestimmen, ob der Treiber über ein Konfigurations Dialogfeld verfügt, indem Sie die [**drv \_ queryconfigure**](drv-queryconfigure.md) -Nachricht senden und einen Rückgabewert ungleich NULL überprüfen. Viele Treiber stellen eine Reihe von benutzerdefinierten Nachrichten bereit, die Sie senden können, um die Vorgänge des Treibers zu steuern.

Wenn Sie besonderen Zugriff auf einen installierbaren Treiber benötigen, z. b. auf seine Ressourcen zugreifen, können Sie das Modul Handle des Treibers abrufen, indem Sie die [**getdrivermodulehandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) -Funktion verwenden.

Wenn Sie den installierbaren Treiber nicht mehr benötigen, können Sie ihn mit der [**closedriver**](/windows/win32/api/mmiscapi/nf-mmiscapi-closedriver) -Funktion schließen.

Mit den installierbaren Treiberfunktionen und-Nachrichten können Sie beliebige installierbare Treiber öffnen und verwalten. Die empfohlene Vorgehensweise zum Öffnen und Verwalten von Multimedia-Geräten ist jedoch zunächst die Verwendung von Standarddiensten (z. b. [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen), [**waveoutmessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)und [**waveoutclose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose) für Wellenform-Ausgabegeräte), sofern diese vorhanden sind. Wenn für einen Multimedia-Treiber keine Standarddienste vorhanden sind, öffnen und verwalten Sie den Treiber mithilfe der installierbaren Treiberfunktionen und-Meldungen.

> [!Note]  
> Die [**senddrivermessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) -Funktion und die [**getdrivermodulehandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle) -Funktion sind die bevorzugten Funktionen, die zum Senden von Nachrichten an einen Treiber und zum Abrufen eines Handles für eine Modul Instanz verwendet werden. Die ältere [**drvgetmodulehandle**](/windows/win32/api/mmiscapi/nf-mmiscapi-drvgetmodulehandle) -Funktion wurde jedoch eingeschlossen, um die Kompatibilität mit früheren Versionen des Windows-Betriebssystems aufrechtzuerhalten.

 

 

 