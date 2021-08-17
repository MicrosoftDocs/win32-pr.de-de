---
description: Die Autorisierung legt fest, auf welche Ressourcen Sie Zugriff haben.
ms.assetid: DD6836EE-DF73-4A07-9DF1-0F5A959DDE8F
title: Autorisierung für Webseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4f64cbbf3dd9ac38a13719cd8835a198f1fbb3b522e8ac368ffaf4e759fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141327"
---
# <a name="authorization-for-web-pages"></a>Autorisierung für Webseiten

Die Autorisierung legt fest, auf welche Ressourcen Sie Zugriff haben.

**Ziel:** So ermöglichen Sie Benutzern den Zugriff auf Ihre App.

## <a name="prerequisites"></a>Voraussetzungen

Keine

**Zeit bis zum Abschluss:** 2 Minuten.

## <a name="instructions"></a>Anweisungen

### <a name="1-authorization"></a>1. Autorisierung

Wenn der Benutzer seine Anmeldeinformationen ein gibt und auf die Schaltfläche Anmelden klickt, wird die Berechtigungsseite angezeigt. Auf dieser Seite können Benutzer am besten präzise Berechtigungen steuern, um der App Zugriff auf die Daten von Contoso zu gewähren. ![Contoso-Berechtigungsseite](images/wab-figure9.png)

### <a name="2-how-to-use-the-sample"></a>2. Verwenden des Beispiels

Sie müssen die folgenden HTML- und CSS-Dateien kennen.

1.  Die folgenden HTML-Dateien entsprechen den beiden Seiten im Webautorisierungsfluss.
    -   WebAuthLogin.html – Beispiel-HTML für die Anmeldeseite
    -   WebAuthPermissions.html – Beispiel-HTML für die Berechtigungsseite
2.  Die CSS-Dateien enthalten Windows 8 Formatvorlagen zum Erstellen einer Windows Store-App-Webseite.
    -   ui-light.css: Dies wurde aus dem Basis-Stylesheet für Windows 8 abgeleitet.
    -   ui-webauth.css: Bietet inkrementelle Formatierungen zum Optimieren des Layouts für Webauthentifizierungsseiten.
    -   theme-colors.css: Stellt die inkrementelle Formatierung zur Außerkraftsetzung von Standardakzentfarben von Steuerelementen mit der Markenfarbe des Anbieters zurVerfeinern.

## <a name="summary-and-next-steps"></a>Zusammenfassung und nächste Schritte

[Zusammenfassungstutorial für die Authentifizierung von Webseiten](tutorial-for-authenticating-web-pages.md)

Nächste [bewährte Methoden für das Entwerfen von Authentifizierungswebseiten](best-practices-for-designing-authentication-web-pages.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überlegungen für die Webseitenentwicklung](considerations-for-the-web-page-development.md)
</dt> <dt>

[Beispiel-App für das Webauthentifizierungsbroker-SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
