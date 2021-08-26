---
description: In diesem Thema werden bewährte Methoden zum Entwerfen von Webseiten beschrieben, die Webauthentifizierungsbroker für die Anmeldung verwenden.
ms.assetid: 271EC68B-5E58-4C1C-B631-DED6A694E98F
title: Bewährte Methoden für das Entwerfen von Authentifizierungswebseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80fbf38c0e020cad342331d67278818b56ce331ff39434aefd726dea52bae1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883616"
---
# <a name="best-practices-for-designing-authentication-web-pages"></a>Bewährte Methoden für das Entwerfen von Authentifizierungswebseiten

In diesem Thema werden bewährte Methoden zum Entwerfen von Webseiten beschrieben, die Webauthentifizierungsbroker für die Anmeldung verwenden.

-   [Verwenden von Metatags](#use-of-metatags)
-   [Verwenden Windows 8 CSS-Stils](#use-of-windows-8-css-styling)
-   [Verwendung von Farbe und Designs](#use-of-color-and-themes)
-   [Ausrichtung](#alignment)
-   [Entwerfen für Snap](#designing-for-snap)
-   [Entwerfen für eine schnelle und fließende Anmeldung](#designing-for-a-fast-and-fluid-login-experience)
-   [Sicherheitshinweise](#security-considerations)
-   [Zugehörige Themen](#related-topics)

## <a name="use-of-metatags"></a>Verwenden von Metatags

Mithilfe von Metatags kann der Anbieter "Contoso Social" den Titel, das Symbol und die Farbe des Headers angeben. In der HTML-Beispieldatei (WebAuthLogin.html) erfolgt dies mit dem folgenden Code.


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



Dadurch können Windows das Vorhandensein des Anbieters auf hervorgehobene Weise in den Header der Benutzeroberfläche integrieren, wie im folgenden Screenshot im roten Feld hervorgehoben. ![Anmeldeseite mit contoso-Header in der Benutzeroberfläche](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a>Verwendung Windows 8 CSS-Stils

Das bereitgestellte Stylesheet ui-light.css ist das Windows 8 Stylesheet, das von Windows Store-Apps verwendet wird. Es definiert Windows Store App-Stil für Typografie und Standardsteuerelemente wie Schaltflächen, Textfelder, Links und Kontrollkästchen, um sicherzustellen, dass sie touchfreundlicher sind. Beim Entwerfen und Anpassen von Webautorisierungsseiten für Windows 8 empfehlen wir Ihnen, dieses Stylesheet unverändert zu verwenden und nach Bedarf zu aktualisieren, solange Ihre Webseite weiterhin den bewährten Methoden auf eigene Weise folgt.

Wenn Sie z. B. über ein spezielles Stylesheet verfügen, wie Hyperlinks auf Ihrer Webseite aussehen und wie sie aussehen sollen, sollten Sie mit Bedacht sicherstellen, dass die von Ihnen angegebenen Stile auf die gleiche Weise wie standard-Windows 8 Hyperlinks touchfreundlicher sind. Dies ist für die Kundenbasis wichtig, indem Windows 8 auf ihren Touchgeräten verwendet wird.

## <a name="use-of-color-and-themes"></a>Verwendung von Farbe und Designs

Dieses Beispiel veranschaulicht eine durchdachte Verwendung von Farben auf verschiedene Weise.

-   Weißer Hintergrund für die Webseite. Wie Sie im vorherigen Screenshot sehen können, wird die Webseite auf einer weißen Oberfläche gehostet, die sich über die Breite des Bildschirms erstreckt. Um sicherzustellen, dass die Webseite in die Oberfläche integriert ist, wird empfohlen, dass die Webseite einen weißen Hintergrund hat.
-   Farbgebung von Steuerelementen basierend auf Ihrer Markenfarbe. Die CSS-Datei theme-colors.css stellt Stile bereit, um die Standardfarben von Steuerelementen im Ui-Light-Stylesheet zu überschreiben, um die Designs der Steuerelemente mit der Farbe des Headers abzugleichen. Im folgenden Screenshot nehmen die Schaltflächen und Hyperlinks z. B. Farben an, die von der Headerfarbe abgeleitet werden. ![Screenshot der Schaltflächen und des Texts mit der gleichen Farbe wie die Kopfzeile](images/wab-figure11.png)
-   Headerfarbe. Die Verwendung der Markenfarbe von Contoso im Header erstellt eine einheitliche Persönlichkeit für die Marke des Anbieters innerhalb der Systemoberfläche.

## <a name="alignment"></a>Ausrichtung

Die Webseite selbst verfügt über keine Auffüllung links oder rechts, um eine typografische Ausrichtung mit dem Titel im Header links und dem Symbol im Header auf der rechten Seite zu ermöglichen.

Sie werden auch feststellen, dass Schaltflächen immer unten rechts auf der Webseite ausgerichtet sind (und rechts am Symbol in der Kopfzeile ausgerichtet sind). Dies ist eine bewährte Methode, da Windows 8 Benutzer an ähnliche Dialogflows mit Schaltflächen in der unteren rechten Seite gewohnt sind.

## <a name="designing-for-snap"></a>Entwerfen für Snap

In der folgenden Abbildung sehen Sie die Anmelde- und Berechtigungsseiten im Snap-Zustand.

![Ausrichtungsansicht des Anmeldebildschirms ](images/wab-figure12.png) . ![Snap-Ansicht der Seite "Berechtigungen" ](images/wab-figure13.png)

In der Beispieldatei ui-webauth.css sehen Sie die Verwendung von Medienabfragen, die das Layout der Seite für den Ausrichtungszustand basierend auf der für die Webseite verfügbaren Breite optimieren. Der im folgenden Bereich eingeschlossene Codeausschnitt implementiert CSS, das auf den Snap-Zustand zugeschnitten ist.


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



In Windows 8 beträgt die Breite des Ausrichtungszustands 320 Pixel. Die Webauthentifizierungsseite belegt oben auf der Benutzeroberfläche 260 Pixel. Wir verwenden einen Wert für die maximale Breite mit genügend Rand, sodass der Medienabfragecode des Anbieters nicht an die genaue Breite des Ausrichtungszustands gebunden ist.

Beim Anpassen Ihrer App für die Ausrichtungsansicht ist es wichtig, dass der Benutzer keinen Kontext verliert, den er in den anderen Ansichten der Webauthentifizierungserfahrung hat (vollständige, füllende oder interaktive Ansichten), aber es ist wichtig, das Layout und die Hierarchie der Elemente auf der Seite neu zu strukturieren, sodass die zum Beibehalten des Kontexts erforderlichen Informationen sichtbar und interaktiv sind. Wir haben einige Beispiele dafür genannt, wie das Beispiel die Webseite an den Ausrichtungszustand angepasst.

-   Beispielsweise wurde für die Anmeldeseite im Snap-Zustand die Width-Eigenschaft des Eingabetextfelds (wie in ui-light.css angegeben) überschrieben und als kleinerer numerischer Wert festgelegt, sodass das Textfeld nicht horizontal abgeschnitten wird.
-   Als weiteres Beispiel im Ausrichtungszustand wird der Schriftgrad der h1- und h2-Header von 42 pt bzw. 20 pt auf 20 pt und 11 pt reduziert. Dies erfolgt in Übereinstimmung mit der Windows 8 Typverlauf und optimiert text so, dass er kompakter im geänderten Viewport ist.
-   Beachten Sie als weiteres Beispiel, dass die Größen der Symbole auf der Berechtigungsseite kleiner sind (im Vergleich zur seite mit der vollständigen Ansicht oben). Auch hier wird der Kontext beibehalten, während Entwurfsressourcen für diejenigen ausgetauscht werden, die für den geänderten Viewport optimaler sind.

## <a name="designing-for-a-fast-and-fluid-login-experience"></a>Entwerfen für eine schnelle und fließende Anmeldung

Zu Beginn des Entwurfs dieser Webseite haben wir uns darauf spezialisiert, dass diese Seite am besten für eine schnelle und fließende Anmeldung geeignet ist. Daher ist die Benutzeroberfläche, die im Flow besonders hervorgehoben ist, das Feld Benutzername und Kennwort auf der Anmeldeseite für eine schnelle Anmeldeinformationseingabe. Wir haben zwar festgestellt, dass es andere gängige Szenarien gibt, z. B. das Abrufen von Kennwörtern und das Verweisen auf Datenschutzbestimmungen, aber die umfassende Erfahrung im Web ist ein besserer Ort für diese Erfahrungen. Für alle Flows, die sich nicht auf die sichere Webauthentifizierung beziehen, wird empfohlen, den Benutzer zum Browser zu navigieren. Dies wird in der HTML-Beispieldatei (WebAuthLogin.html) wie folgt gezeigt: Dadurch werden alle Webseiten geöffnet, mit denen `<meta name="mswebdialog-newwindowurl" content="*" />` über die Anmelde- oder Berechtigungsseite im Standardbrowser des Benutzers verknüpft ist, wo der Benutzer diese Flows abschließen und dann zur App zurückkehren kann, um sich anzumelden.

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Die folgenden Artikel enthalten Anleitungen zum Schreiben von sicherem C++-Code.

-   [Bewährte Sicherheitsmethoden für C++](/cpp/security/security-best-practices-for-cpp)
-   [Muster & Sicherheitsleitfadens für Anwendungen](/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überlegungen für die Webseitenentwicklung](considerations-for-the-web-page-development.md)
</dt> <dt>

[Häufig gestellte Fragen zum Webauthentifizierungsbroker](faq-for-web-authentication-broker.yml)
</dt> <dt>

[Webauthentifizierungsbroker-SDK-Beispiel-App](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
