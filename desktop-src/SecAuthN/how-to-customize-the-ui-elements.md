---
description: Eine Webseite passt die Benutzeroberfläche mit Titel, Symbol und Headerfarbe mithilfe von Metadatentags an, die auf der Webseite definiert sind.
ms.assetid: 6F1E0B2E-E013-4C5B-86A4-0AF8606D0C12
title: Anpassen der Benutzeroberflächenelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a99e8e7da789653226db40763116472eb065df0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884561"
---
# <a name="how-to-customize-the-ui-elements"></a>Anpassen der Benutzeroberflächenelemente

Eine Webseite passt die Benutzeroberfläche mit Titel, Symbol und Headerfarbe mithilfe von Metadatentags an, die auf der Webseite definiert sind. Webentwickler können HTML-Metatags verwenden, um die Persönlichkeit und Marke des Anbieters auf der &lt; &gt; Webauthentifizierungsbroker-Benutzeroberfläche anzuzeigen. Darüber hinaus können Entwickler komplexere Benutzeraktionen ausführen, z. B. das Anmelden und Wiederherstellen von Kennwörtern. Das Konzept ähnelt dem Feature Angeheftete Sites des Windows Internet Explorer 9 und Windows 7.

Zusätzlich zum Anpassen der Benutzeroberfläche um den Webseitenbereich sollte die Webseite auch die Stile der Windows 8-Steuerelemente nutzen, für touch aktiviert sein und das Öffnen von Links im Browser nach Möglichkeit ermöglichen.

Im Folgenden finden Sie ein Beispiel für eine Webseite, die das Anpassungsmodell des Webauthentifizierungsbrokers genutzt hat. ![Benutzeroberflächenelemente des Webauthentifizierungsbrokers](images/wab-figure7.png)

## <a name="instructions"></a>Anweisungen

### <a name="step-1-customize-the-icon"></a>Schritt 1: Anpassen des Symbols

Die Webseite kann ein Symbol bereitstellen, indem ein meta-Tag mswebdialog-logo verwendet wird.

``` syntax
<meta name="mswebdialog-logo" content="https://www.contoso.com/logo.png"/>
```

Der Inhalt ist eine URL, die eine relative oder absolute Seite sein kann. Das Schema der URL kann HTTP oder HTTPS sein. Das Format der Datei sollte entweder PNG oder JPG sein. Die Größe des Bilds sollte 30 x 30 Pixel betragen. Wenn das Image eine andere Größe auf hat, wird es vom Betriebssystem herunter- oder hochskaliert, damit es dem 30x30-Speicherplatz passt. Das Bild sollte so entworfen werden, dass es gut gerendert wird, wenn es auf 140 % und 180 % hochskaliert wird, um Bildschirme mit höherer Auflösung zu berücksichtigen. Um verschiedene Skalierungsfaktoren zu testen, verwenden Sie die in Visual Studio 11 geladene [Webauthentifizierungsbroker-SDK-Beispiel-App,](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) die das Simulieren verschiedener Auflösungen und Skalierungsfaktoren mithilfe der Gerätefenster des Entwurfsmodus ermöglicht.

### <a name="step-2-customize-the-title-text"></a>Schritt 2: Anpassen des Titeltexts

Die Webseite kann den Titel mithilfe des Metatags mswebdialog-title bereitstellen.

``` syntax
<meta name="mswebdialog-title" content="Contoso Social"/>
```

Der Titel sollte kurz sein und die Marke des Anbieters (z. B. Contoso) widerspiegeln.

### <a name="step-3-customize-the-header-color"></a>Schritt 3: Anpassen der Kopfzeilenfarbe

Die Webseite kann mithilfe des Metatags mswebdialog-header-color die Farbe bereitstellen, die ihre Markenidentität darstellt, die für den Header des Dialogfelds verwendet werden soll.

``` syntax
<meta name="mswebdialog-header-color" content="#1267DF"/>
```

Die Farbe kann ein beliebiger wert sein, der hier angegeben wird. Der Webauthentifizierungsbroker ignoriert jedoch alle Alphakanalwerte. Da diese Farbe speziell und mit farben auf der Seite im Allgemeinen verwendet wird, wird empfohlen, die gleichen Farben zu verwenden, die in der App des Anbieters Windows 8 verwendet werden, wenn eine solche App vorhanden ist.

> [!Note]  
> Symbole und Farben werden pro Server auf dem Client zwischengespeichert, sobald META-Tags analysiert wurden. Löschen Sie den Clientcache, bevor Sie die Benutzeroberfläche starten, damit die Änderungen wirksam werden. Ändern Sie dazu die folgenden Registrierungseinstellungen.

 

``` syntax
// Registry location under HKLM used for setting various AuthHost parameters.
#define AUTH_HOST_LOCAL_MACHINE_REGPATH \
    L"SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\Image File Execution Options\\authhost.exe"
// MaxAge to use for downloading logo images
#define AUTH_HOST_LOGO_IMAGE_MAX_AGE_SECONDS_REG_VALUE_NAME \
    L"LogoImageMaxAgeSeconds"
// 24 hours
#define AUTH_HOST_LOGO_IMAGE_MAX_AGE_SECONDS_DEFAULT        \
    (24 * 60 * 60)
```

Nachdem ein Symbol heruntergeladen wurde, wird es 24 Stunden lang nicht mehr angezeigt. Um mit Logobildern zu testen, legen Sie den obigen Reg-Schlüssel mit einem niedrigeren Wert fest.

### <a name="step-4-customize-the-web-page"></a>Schritt 4: Anpassen der Webseite

Zusätzlich zum Anpassen der Benutzeroberfläche um die Webseite sollten Entwickler auch Webseiten erstellen, die nahtlos und in die allgemeine Benutzeroberfläche Windows 8 sind. Dies umfasst die Verwendung empfohlener Stile, das Sicherstellen, dass Webseiten mit Touch-fähigen Geräten gut funktionieren, und das Öffnen bestimmter Webseiten im Webbrowser.

-   Format

    Es wird dringend empfohlen, die hier empfohlene Formatierung zu verwenden, um eine konsistentere Benutzeroberfläche für Webauthentifizierungsbroker-Webseiten und andere Benutzeroberflächenkomponenten von Windows 8. Die Webseite sollte einen weißen Hintergrund und keine Rahmen verwenden. Die Schaltflächen wie Login oder Cancel sollten in der rechten unteren Ecke positioniert sein und die gleiche Farbe wie der Header verwenden. Da der Webauthentifizierungsbroker eine Schaltfläche "Zurück" bietet, sollten Sie erwägen, die Schaltfläche Abbrechen von der Webseite vollständig zu entfernen.

-   Aktivieren von Touch

    Die Webseite sollte mit einer touchbasierten Benutzerinteraktion entworfen werden. Weitere Informationen zum Entwerfen für touch in Windows 8 finden Sie im Thema [Entwurf der Touchinteraktion.](https://msdn.microsoft.com/library/Hh465415(v=Win.10).aspx)

-   Anpassen des Ziels der Links

    Der Webauthentifizierungsbroker ist ideal für die Bereitstellung von Webseiten, die eine einzelne Benutzeraktion erfordern, z. B. Anmelde- oder OAuth-Autorisierungsseiten. Bei komplexen Benutzerabläufen wie kontobasiertem Erstellen, Wiederherstellen nach einem verlorenen oder vergessenen Kennwort, Anzeigen von Datenschutzbestimmungen und so weiter, bei denen der Benutzer einige Zeit in das Verstehen und Abschließen des Flows investieren soll, wird empfohlen, diese Seiten im bevorzugten Browser des Benutzers zu öffnen, um die vollständige Navigation zu unterstützen und das Browsen zu erreichen. Der Webauthentifizierungsbroker lässt standardmäßig nicht zu, dass neue Browserfenster über eine Webseite geöffnet werden (weitere Informationen finden Sie im Abschnitt Standardmäßig keine neuen Fenster). Mithilfe des Metatags kann `mswebdialog-newwindowurl` die Webseite jedoch deklarieren, welche URLs im Browser geöffnet werden sollen.

    Ermöglicht es der Webseite, eine URL oder einen Teil der URL anzugeben, die der Webauthentifizierungsbroker verwendet, um bei jedem Öffnen einer URL in einem neuen Fenster mithilfe des Zielattributs oder der window.open()-Methode eine Übereinstimmung (Linke Zeichenfolgen-Übereinstimmung) zu `mswebdialog-newwindowurl` erhalten. Bei einer Übereinstimmung wird die URL im Standardbrowser des Benutzers geöffnet. Wenn keine Übereinstimmung besteht, navigiert der Webauthentifizierungsbroker zur URL selbst (Standardverhalten). Beispiel: `<meta name="mswebdialog-newwindowurl" content="https://www.contoso.com/privacy"/>`

    Im Fall dieses Metatags öffnet der Webauthentifizierungsbroker die im Browser, navigiert https://www.contoso.com/privacy/policy.html aber direkt zu https://www.contoso.com/termsofuse.html . Beachten Sie, dass Links, die nicht versuchen, in einem neuen Fenster zu öffnen (z. B. Links, die nicht das Zielattribut oder die window.open()-Methode verwenden) von diesem Metatag nicht betroffen sind. Der Inhalt ist eine URL, die eine relative oder absolute Seite sein kann. Das Schema der URL kann HTTP oder HTTPS sein. Sie sollten Metatags definieren, um alle Links zu behandeln, die nicht Teil des Grundlegenden Benutzerflusses sind, z. B. `mswebdialog-newwindowurl` Datenschutzbestimmungen, Anmeldeformulare und so weiter. Wenn Sie die Anmeldung mit einem Authentifizierungsanbieter eines Drittanbieters (z. B. OpenID-Anbieter) unterstützen, stellen Sie sicher, dass diese Interaktionen innerhalb des Webauthentifizierungsbrokers bleiben. Damit alle Links auf Ihrer Seite sicher im Browser geöffnet werden können, verwenden Sie die Sternsyntax, z. B. beachten Sie, dass " " nur exklusiv verwendet und nicht mit einer anderen URL kombiniert werden kann, z. B. " *" ist keine gültige `  <meta name="mswebdialog-newwindowurl" content="*"/>` \* https://www.contoso.com/\ Syntax.

### <a name="step-5-rules-applied-to-all-meta-tags"></a>Schritt 5: Auf alle Metatags angewendete Regeln

Wenn Der Webauthentifizierungsbroker Metatags verarbeitet, gelten die folgenden Regeln:

-   Die Auswirkungen des Metatags bleiben auf allen Seiten unter derselben Domäne der zweiten Ebene (z. B. contoso.com) erhalten, es sei denn, es wird ein anderes Metatag mit demselben Namen, aber unterschiedlichen Inhalten gefunden.
-   Wenn mehrere Metatags mit demselben Namen auf derselben Seite gefunden werden, wählt der Webauthentifizierungsbroker nur eines davon aus und ignoriert den Rest. Welches meta-Tag ausgewählt wird, ist nicht definiert.
    > [!Note]  
    > Diese Regel gilt nicht für das `mswebdialog-newwindowurl` Metatag, das mehrere Instanzen auf derselben Seite zulässt.

     

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überlegungen für die Webseitenentwicklung](considerations-for-the-web-page-development.md)
</dt> <dt>

[Beispiel-App für das Webauthentifizierungsbroker-SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
