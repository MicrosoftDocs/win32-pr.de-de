---
description: Bei der Authentifizierung wird bestätigt, wer Sie sind.
ms.assetid: 5B058197-67B3-40DD-80D8-7BD8EE084CC9
title: Authentifizierung für Webseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46a063cdd63631f84aa21980f89a143b3d1e9b42af020799d0f9f1bb7502b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141437"
---
# <a name="authentication-for-web-pages"></a>Authentifizierung für Webseiten

Bei der Authentifizierung wird bestätigt, wer Sie sind.

**Ziel:** Damit der Webauthentifizierungsbroker als Teil Ihrer App angezeigt wird.

## <a name="prerequisites"></a>Voraussetzungen

Keine

**Zeit bis zum Abschluss:** 15 Minuten.

## <a name="instructions"></a>Anweisungen

### <a name="1-getting-started"></a>1. Erste Schritte

Starten Sie die Setupdatei, um eine Contoso-Website in Internetinformationsdienste 8 auf dem lokalen Computer zu installieren, um die HTML- und CSS-Beispieldateien zu hosten.

1.  Html- und CSS-Beispieldateien werden im Verzeichnis der Programmdateien unter Microsoft \\ Contoso installiert.
2.  Darüber hinaus wird eine "Fabrikam Social"-Windows Store-App auf dem Desktop entpackt.

### <a name="2-getting-familiar"></a>2. Kennenlernen

Um ein Gefühl dafür zu erhalten, wie die Beispielseiten im Webauthentifizierungsbroker aussehen, öffnen Sie die Projektmappendatei Fabrikam Social Visual Studio 11 im Ordner "Fabrikam Social" auf dem Desktop.

1.  Führen Sie die Anwendung aus, und klicken Sie auf "Launch", um die Beispielseiten im Webauthentifizierungsbroker aufzuführen.
2.  Die Größe der App kann auf eine Seite geändert oder aktiviert werden, indem einige Daten für die Anwendung freigegeben werden.

### <a name="3-authentication"></a>3. Authentifizierung

Wenn die Webauthentifizierungs-API von der zugrunde liegenden App aufgerufen wird, um eine Verbindung mit dem Anbieter "Contoso Social" herzustellen, wird die Anmeldeseite angezeigt. Diese Seite ist so konzipiert, dass sie für eine schnelle und fließende Anmeldung am besten geeignet ist. Sie bietet auch Einstiegspunkte für einige andere gängige Benutzeraktionen, z. B. das Abrufen von Kennwortdetails, die Registrierung für ein Konto und das Lesen von Anweisungen zu Datenschutz und Geschäftsbedingungen, die im Browser abgeschlossen werden. ![Contoso-Anmeldeseite](images/wab-figure8.png)

## <a name="summary-and-next-steps"></a>Zusammenfassung und nächste Schritte

[Zusammenfassungstutorial für die Authentifizierung von Webseiten](tutorial-for-authenticating-web-pages.md)

Nächste [Autorisierung für Webseiten](authorization-for-web-pages.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überlegungen für die Webseitenentwicklung](considerations-for-the-web-page-development.md)
</dt> <dt>

[Webauthentifizierungsbroker-SDK-Beispiel-App](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
