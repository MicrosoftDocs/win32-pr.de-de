---
title: Aktivieren der Protokollierung
description: Aktivieren der Protokollierung
ms.assetid: 50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad
keywords:
- Windows Medien Geräte-Manager,Protokollierung
- Geräte-Manager,Protokollierung
- Desktopanwendungen, Protokollierung
- Dienstanbieter,Protokollierung
- Programmierhandbuch,Protokollierung
- logging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff937b2a3abd16f7319c3abb73a3a2159350049fff8c89d343cc5545f8a21ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585118"
---
# <a name="enabling-logging"></a>Aktivieren der Protokollierung

Windows Media Geräte-Manager stellt ein Protokollierungsobjekt bereit, das Informationen zur Laufzeit in einer Textdatei speichern kann. Entwickler von Anwendungen und Dienstanbietern können dieses Objekt verwenden, um Nachrichten in einer Protokolldatei zu speichern, während ihre Anwendung oder ihr Dienstanbieter ausgeführt wird. Dieses Objekt ist besonders nützlich bei der Verarbeitung von DURCH DRM geschützten Dateien, da Windows Media Geräte-Manager es Ihnen nicht ermöglicht, einen Debugger an einen Prozess anzufügen, der DRM-geschützte Dateien verarbeitet.

Die Protokollierung ist ein COM-Objekt mit der Klassen-ID CLSID \_ WMDMLogger, das eine Schnittstelle, [**IWMDMLogger,**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger)verfügbar macht. Komponenten benötigen kein Zertifikat, um das Protokollierungsobjekt zu verwenden.

Standardmäßig verwaltet Windows Media Geräte-Manager eine Protokolldatei, unabhängig davon, ob eine Anwendung **IWMDMLogger** verwendet. Diese Protokolldatei ist eine einfache Textdatei, und jeder Eintrag enthält einen Eintrag, dem ein Zeitstempel im Format YYYYMMDDHHMMSS vorangestellt ist, wobei 24-Stunden-Ortszeit verwendet wird. Windows Media Geräte-Manager protokolliert alle API-Aufrufe sowie alle Einträge, die Sie durch Aufrufen von **IWMDMLogger-Nachrichten** hinzufügen. Alle Protokolldateieinträge werden an die Datei angefügt, bis [**Zurücksetzen**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) aufgerufen wird oder die Datei ihre maximale Größe überschreitet. Die Datei wird nach jedem Protokollierungsvorgang automatisch geschlossen. Dieselbe Protokolldatei wird für Anwendungs- und Systemeinträge verwendet.

In den folgenden Schritten wird die Verwendung des Protokollierungsobjekts veranschaulicht:

1.  Schließen Sie wmdmlog.h in Ihr Projekt ein.
2.  Erstellen Sie ein Protokollierungsobjekt, indem **Sie CoCreateInstance**(CLSID \_ WMDMLogger) aufrufen und die **IWMDMLogger-Schnittstelle** anfordern. Weisen Sie den Schnittstellenzeiger einer globalen Variablen zu.
3.  Überprüfen Sie, ob die Protokollierung aktiviert ist, indem [**Sie IWMDMLogger::IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled)aufrufen. Wenn nicht, aktivieren Sie es, indem [**Sie IWMDMLogger::Enable aufrufen.**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable)
4.  Geben Sie einen benutzerdefinierten Protokolldateinamen und eine benutzerdefinierte Protokolldateigröße an. Dazu rufen [**Sie IWMDMLogger::SetLogFileName**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) und [**IWMDMLogger::SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams)auf.
5.  Rufen Sie an den Punkten im Code, an denen Sie einen Eintrag im Protokoll vornehmen möchten, entweder [**IWMDMLogger::LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) auf, um Zeichenfolgen mit Variablen zu protokollieren (diese Methode ähnelt **wsprintf** in der Weise, wie sie es Ihnen ermöglicht, eine Zeichenfolge mit einem Variablenwert zu formatieren), oder rufen Sie [**IWMDMLogger::LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) auf, um konstante Zeichenfolgen zu protokollieren.

Beispielcode finden Sie auf den Referenzseiten für die Methoden von [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Aufgaben für Anwendungen und Dienstanbieter**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




