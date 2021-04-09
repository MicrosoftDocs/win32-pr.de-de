---
description: Eine Webseite passt die Benutzeroberfläche (UI) mit dem Titel, dem Symbol und der Header Farbe an, indem Metadatentags verwendet werden, die auf der Webseite definiert sind.
ms.assetid: 6F1E0B2E-E013-4C5B-86A4-0AF8606D0C12
title: Anpassen der Benutzeroberflächenelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19314f8e4c5d4944a500a0eef3aa0f75cd231b12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867263"
---
# <a name="how-to-customize-the-ui-elements"></a>Anpassen der Benutzeroberflächenelemente

Eine Webseite passt die Benutzeroberfläche (UI) mit dem Titel, dem Symbol und der Header Farbe an, indem Metadatentags verwendet werden, die auf der Webseite definiert sind. Webentwickler können HTML <meta> -Tags verwenden, um die Persönlichkeit und Marke des Anbieters in der Benutzeroberfläche des Webauthentifizierungs Brokers anzuzeigen. Außerdem können Entwickler kompliziertere Benutzeraktionen weiterleiten, z. b. das registrieren und Wiederherstellen von Kenn Wörtern. Das Konzept ähnelt der Funktion angeheftete Sites von Windows Internet Explorer 9 und Windows 7.

Zusätzlich zur Anpassung der Benutzeroberfläche auf dem Webseiten Bereich sollte die Webseite auch die Stile der Windows 8-Steuerelemente nutzen, für die Fingereingabe aktiviert werden und Links aktivieren, die ggf. im Browser geöffnet werden.

Im folgenden finden Sie ein Beispiel für eine Webseite, die das Webauthentifizierungs Broker-Anpassungs Modell genutzt hat. ![Webauthentifizierungs Broker-Benutzeroberflächen Elemente](images/wab-figure7.png)

## <a name="instructions"></a>Anweisungen

### <a name="step-1-customize-the-icon"></a>Schritt 1: Anpassen des Symbols

Die Webseite kann ein Symbol mithilfe eines mswebdialog-Logo-Meta-Tags bereitstellen.

``` syntax
<meta name="mswebdialog-logo" content="https://www.contoso.com/logo.png"/>
```

Bei dem Inhalt handelt es sich um eine URL, die eine relative oder absolute Seite aufweisen kann. Das Schema der URL kann "http" oder "https" lauten. Das Format der Datei muss entweder PNG oder jpg lauten. Die Größe des Bilds sollte quadratisches 30x30 Pixel betragen. Wenn das Image die unterschiedliche Größe hat, wird es vom Betriebssystem zentral hoch-oder herunterskaliert, um dem quadratisches 30x30-Speicherplatz gerecht zu werden. Das Image sollte so entworfen werden, dass es bei einer Skalierung auf bis zu 140% und 180% für Bildschirme mit höherer Auflösung gut funktioniert. Wenn Sie verschiedene Skalierungsfaktoren testen möchten, verwenden Sie die in Visual Studio 11 geladene SDK-Beispiel-App für den [Web Authentication Broker](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker) , mit der unterschiedliche Auflösungen und Skalierungsfaktoren mithilfe der Geräte Fenster des Entwurfs Modus simuliert werden können.

### <a name="step-2-customize-the-title-text"></a>Schritt 2: Anpassen des Titel Texts

Die Webseite kann den Titel mithilfe des Meta-Tags mswebdialog-Title bereitstellen.

``` syntax
<meta name="mswebdialog-title" content="Contoso Social"/>
```

Der Titel sollte kurz sein und die Marke des Anbieters (z. b. "Configuration Manager") widerspiegeln.

### <a name="step-3-customize-the-header-color"></a>Schritt 3: Anpassen der Header Farbe

Die Webseite kann die Farbe bereitstellen, die Ihre Markenidentität darstellt, die für den Header des Dialog Felds verwendet werden soll, indem das Meta-Tag "mswebdialog-Header-Color" verwendet wird.

``` syntax
<meta name="mswebdialog-header-color" content="#1267DF"/>
```

Die Farbe kann ein beliebiger Wert sein, der hier angegeben wird. Allerdings ignoriert der Webauthentifizierungs Broker jeden beliebigen Alphakanal Wert. Mit dieser Farbe und Farben, die auf der Seite Allgemein verwendet werden, empfiehlt es sich, die gleichen Farben zu verwenden, die in der Windows 8-App des Anbieters verwendet werden, wenn diese APP vorhanden ist.

> [!Note]  
> Symbole und Farben werden pro Server auf dem Client zwischengespeichert, sobald Meta-Tags analysiert werden. Löschen Sie den Client Cache, bevor Sie die Benutzeroberfläche starten, damit die Änderungen wirksam werden. Ändern Sie hierzu die folgenden Registrierungs Einstellungen.

 

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

Wenn ein Symbol heruntergeladen wird, wird es für 24 Stunden nicht erneut abgerufen. Um mit Logo Bildern zu testen, legen Sie den oben angegebenen reg-Schlüssel auf einen niedrigeren Wert fest.

### <a name="step-4-customize-the-web-page"></a>Schritt 4: Anpassen der Webseite

Zusätzlich zur Anpassung der Benutzeroberfläche auf der Webseite sollten Entwickler auch Webseiten erstellen, die nahtlos und in die gesamte Windows 8-Umgebung integriert sind. Dies umfasst die Verwendung empfohlener Stile, die sicherstellen, dass Webseiten hervorragend mit Geräten mit aktiviertem Fingerabdruck funktionieren, und das Öffnen bestimmter Webseiten im Webbrowser.

-   Format

    Es wird dringend empfohlen, den hier empfohlenen Stil zu verwenden, um eine konsistentere Benutzeroberfläche für Webauthentifizierungs Broker-Webseiten und andere Benutzeroberflächen Komponenten von Windows 8 zu erstellen. Die Webseite sollte einen weißen Hintergrund und keine Rahmen verwenden. Die Schaltflächen, wie z. b. Login oder Cancel, sollten in der rechten unteren Ecke positioniert werden und die gleiche Farbe wie der-Header verwenden. Da Web Authentication Broker nun eine Schaltfläche "zurück" bereitstellt, empfiehlt es sich, eine Schaltfläche Abbrechen von der Webseite vollständig zu entfernen.

-   Aktivieren der Fingereingabe

    Die Webseite sollte mit einer berührungsbasierten Benutzerinteraktion entworfen werden. Weitere Informationen zum Entwerfen von Touchscreen in Windows 8 finden Sie im Thema zum Design der Fingereingabe [Interaktion](https://msdn.microsoft.com/library/Hh465415(v=Win.10).aspx) .

-   Anpassen des Ziels der Hyperlinks

    Web Authentication Broker eignet sich hervorragend für die Bereitstellung von Webseiten, die eine einzelne Benutzeraktion erfordern, z. b. Anmelde-oder OAuth-Autorisierungs Für kompliziertere Benutzer Abläufe, wie z. b. das Erstellen von Konten, das Wiederherstellen nach einem verlorenen oder vergessenen Kennwort, das darstellen von Datenschutzbestimmungen usw., bei denen der Benutzer eine gewisse Zeit zum Verständnis und zum Abschließen des Flows investieren soll, wird empfohlen, dass diese Seiten im bevorzugten Browser des Benutzers gestartet werden, um die vollständige Navigation zu unterstützen. Der Webauthentifizierungs Broker lässt standardmäßig nicht zu, dass neue Browserfenster von einer Webseite geöffnet werden (Weitere Informationen finden Sie im Abschnitt "keine neuen Fenster"). Mithilfe des Meta-Tags `mswebdialog-newwindowurl` kann die Webseite jedoch deklarieren, welche URLs im Browser geöffnet werden sollen.

    `mswebdialog-newwindowurl`Ermöglicht es der Webseite, eine URL oder einen Teil der URL anzugeben, die der Webauthentifizierungs Broker verwendet, um eine Entsprechung für zu finden (linke Zeichen folgen Entsprechung), wenn Sie aufgefordert wird, eine URL in einem neuen Fenster zu öffnen, indem Sie entweder das target-Attribut oder die Window. Open ()-Methode verwenden. Wenn eine Entsprechung vorliegt, wird die URL im Standardbrowser des Benutzers geöffnet. Wenn keine Entsprechung gefunden wird, navigiert der Webauthentifizierungs Broker zur URL selbst (Standardverhalten). Beispiel: `<meta name="mswebdialog-newwindowurl" content="https://www.contoso.com/privacy"/>`

    Im Fall dieses Meta-Tags öffnet der Webauthentifizierungs Broker den https://www.contoso.com/privacy/policy.html im Browser, wird jedoch direkt zu navigieren https://www.contoso.com/termsofuse.html . Beachten Sie, dass Verknüpfungen, die nicht versuchen, in einem neuen Fenster zu öffnen (z. b. Verknüpfungen, die keine Ziel Attribute oder Window. Open ()-Methode verwenden), von diesem Meta-Tag nicht betroffen sind. Bei dem Inhalt handelt es sich um eine URL, die eine relative oder absolute Seite aufweisen kann. Das Schema der URL kann "http" oder "https" lauten. Sie sollten `mswebdialog-newwindowurl` Meta-Tags definieren, um Links zu behandeln, die nicht Teil des Kern benutzerflows sind, z. b. Datenschutzbestimmungen, Registrierungsformulare usw. Wenn Sie die Anmeldung mit einem Authentifizierungs Anbieter eines Drittanbieters (z. b. OpenID-Anbieter) unterstützen, stellen Sie sicher, dass diese Interaktionen innerhalb des Webauthentifizierungs Brokers beibehalten werden. Um zu ermöglichen, dass alle Links auf der Seite im Browser als sicher geöffnet werden, verwenden Sie die Stern Syntax, wie z. b., `  <meta name="mswebdialog-newwindowurl" content="*"/>` dass " \* " nur exklusiv verwendet werden kann und nicht mit einer anderen URL kombiniert werden kann, z https://www.contoso.com/\ . b. ist "*" keine gültige Syntax.

### <a name="step-5-rules-applied-to-all-meta-tags"></a>Schritt 5: Regeln, die auf alle Meta-Tags angewendet werden

Wenn der Webauthentifizierungs Broker Meta-Tags verarbeitet, gelten die folgenden Regeln:

-   Die Auswirkung des Meta-Tags wird auf allen Seiten unter derselben Domäne der zweiten Ebene (z. b. contoso.com) beibehalten, es sei denn, es ist ein anderes Meta-Tag mit dem gleichen Namen, aber unterschiedlichem Inhalt aufgetreten.
-   Wenn auf derselben Seite mehrere Meta-Tags desselben Namens gefunden werden, wählt der Webauthentifizierungs Broker nur einen aus und ignoriert den Rest. Welches spezifische Meta-Tag ausgewählt wird, ist nicht definiert.
    > [!Note]  
    > Diese Regel gilt nicht für das `mswebdialog-newwindowurl` Meta-Tag, das mehrere Instanzen auf derselben Seite zulässt.

     

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überlegungen für die Webseitenentwicklung](considerations-for-the-web-page-development.md)
</dt> <dt>

[Beispiel-App für das Web Authentication Broker SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
