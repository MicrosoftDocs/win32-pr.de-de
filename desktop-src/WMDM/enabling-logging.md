---
title: Aktivieren der Protokollierung
description: Aktivieren der Protokollierung
ms.assetid: 50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad
keywords:
- Windows Media-Device Manager, Protokollierung
- Device Manager, Protokollierung
- Desktop Anwendungen, Protokollierung
- Dienstanbieter, Protokollierung
- Programmier Handbuch, Protokollierung
- logging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e95be13e93a5a58bb728d5600c6fdea9801ec2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341649"
---
# <a name="enabling-logging"></a>Aktivieren der Protokollierung

Windows Media Device Manager stellt ein Protokollierungs Objekt bereit, mit dem Informationen zur Laufzeit in einer Textdatei gespeichert werden können. Entwickler von Anwendungen und Dienstanbietern können dieses Objekt zum Speichern von Nachrichten in einer Protokolldatei verwenden, während Ihre Anwendung oder Ihr Dienstanbieter ausgeführt wird. Dieses Objekt ist besonders nützlich bei der Handhabung von DRM-geschützten Dateien, da Windows Media Device Manager es Ihnen nicht gestattet, einen Debugger an einen Prozess anzufügen, der von DRM geschützte Dateien verarbeitet.

Der Logger ist ein COM-Objekt mit der Klassen-ID CLSID \_ wmdmlogger, das eine Schnittstelle, [**iwmdmlogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger), verfügbar macht. Komponenten benötigen kein Zertifikat für die Verwendung des Protokollierungs Objekts.

Standardmäßig verwaltet Windows Media Device Manager eine Protokolldatei, unabhängig davon, ob eine Anwendung **iwmdmlogger** verwendet. Diese Protokolldatei ist eine einfache Textdatei, und jeder Eintrag enthält einen Eintrag, dem ein Zeitstempel im Format yyyymmddhhmmss mit einer Ortszeit von 24 Stunden vorangestellt ist. Windows Media Device Manager protokolliert alle API-Aufrufe zusammen mit allen Einträgen, die Sie durch Aufrufen von **iwmdmlogger** -Nachrichten hinzufügen. Alle Protokolldatei Einträge werden an die Datei angehängt, bis die [**zurück**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) Setzung aufgerufen wird, oder die Datei überschreitet die maximale Größe. Die Datei wird nach jedem Protokollierungs Vorgang automatisch geschlossen. Die gleiche Protokolldatei wird für Anwendungs Einträge und Systemeinträge verwendet.

Die folgenden Schritte zeigen, wie das Protokollierungs Objekt verwendet wird:

1.  Fügen Sie "wmdmlog. h" in Ihr Projekt ein.
2.  Erstellen Sie ein Protokollierungs Objekt, indem Sie **CoCreateInstance**(CLSID \_ wmdmlogger) aufrufen und die **iwmdmlogger** -Schnittstelle anfordern. Weisen Sie den Schnittstellen Zeiger einer globalen Variablen zu.
3.  Überprüfen Sie, ob die Protokollierung durch Aufrufen von [**iwmdmlogger:: isaktiviaktiviert**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled)ist. Wenn dies nicht der Fall ist, aktivieren Sie es durch Aufrufen von [**iwmdmlogger:: enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).
4.  Geben Sie den Namen und die Größe der benutzerdefinierten Protokolldatei an. Dies erfolgt durch den Aufruf von [**iwmdmlogger:: setlogfilename**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) und [**iwmdmlogger:: setsizeparameter.**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams)
5.  Wenn Sie in Ihrem Code an der Stelle, an der Sie einen Eintrag im Protokoll erstellen möchten, einen Eintrag in das Protokoll einfügen möchten, können Sie entweder [**iwmdmlogger:: logdword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) zum Protokollieren von Zeichen folgen mit Variablen verwenden (diese Methode ähnelt **wsprintf** in der Weise, wie Sie eine Zeichenfolge mit einem variablen Wert formatieren kann), oder Sie können [**iwmdm**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring)

Beispielcode finden Sie auf den Referenzseiten für die Methoden von [**iwmdmlogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Aufgaben für Anwendungen und Dienstanbieter**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




