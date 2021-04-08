---
description: Die Autorisierung legt fest, auf welche Ressourcen Sie Zugriff haben.
ms.assetid: DD6836EE-DF73-4A07-9DF1-0F5A959DDE8F
title: Autorisierung für Webseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c26e9bc8333d74d18989c5c581cc54054a29ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863535"
---
# <a name="authorization-for-web-pages"></a>Autorisierung für Webseiten

Die Autorisierung legt fest, auf welche Ressourcen Sie Zugriff haben.

**Ziel:** , Um Benutzern den Zugriff auf Ihre APP zu ermöglichen.

## <a name="prerequisites"></a>Voraussetzungen

Keine

**Zeit bis zum Abschluss:** 2 Minuten.

## <a name="instructions"></a>Anweisungen

### <a name="1-authorization"></a>1. Autorisierung

Wenn der Benutzer seine Anmelde Informationen eingibt und auf die Anmelde Schaltfläche klickt, wird die Seite Berechtigungen angezeigt. Diese Seite ermöglicht es Benutzern, differenzierte Berechtigungen zu steuern, um der APP den Zugriff auf die Daten von "appto" zu gewähren. ![Seite "Berechtigungen" für "Seite"](images/wab-figure9.png)

### <a name="2-how-to-use-the-sample"></a>2. Verwenden des Beispiels

Sie müssen sich über die folgenden HTML-und CSS-Dateien informieren.

1.  Die folgenden HTML-Dateien entsprechen den beiden Seiten im webautorisierungs Fluss.
    -   WebAuthLogin.html – Beispiel-HTML für die Anmeldeseite
    -   WebAuthPermissions.html – Beispiel-HTML für die Seite "Berechtigungen"
2.  Die CSS-Dateien enthalten Windows 8-Stile zum Erstellen einer Windows Store-App-Webseite.
    -   "UI-Light. CSS – dies wurde aus dem Basis Stylesheet für Windows 8-Steuerelemente abgeleitet.
    -   UI-webauth. CSS – diese Methode bietet inkrementelles formatieren zum Optimieren des Layouts für Webauthentifizierungs Seiten.
    -   Theme-Colors. CSS – bietet das inkrementelle formatieren zum Überschreiben der Standard Akzentfarben von Steuerelementen mit der Markenfarbe des Anbieters.

## <a name="summary-and-next-steps"></a>Zusammenfassung und nächste Schritte

Zusammenfassungs- [Tutorial zum Authentifizieren von Webseiten](tutorial-for-authenticating-web-pages.md)

Nächste [bewährte Methoden für das Entwerfen von Authentifizierungs Webseiten](best-practices-for-designing-authentication-web-pages.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überlegungen für die Webseitenentwicklung](considerations-for-the-web-page-development.md)
</dt> <dt>

[Beispiel-App für das Web Authentication Broker SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
