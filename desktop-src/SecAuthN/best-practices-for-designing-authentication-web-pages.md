---
description: In diesem Thema werden bewährte Methoden für das Entwerfen von Webseiten beschrieben, die Webauthentifizierungsbroker für die Anmeldung verwenden.
ms.assetid: 271EC68B-5E58-4C1C-B631-DED6A694E98F
title: Bewährte Methoden für das Entwerfen von Authentifizierungswebseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdd6ab5dc067c23cfb29d21d2ff4780cee0ef1c
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353673"
---
# <a name="best-practices-for-designing-authentication-web-pages"></a>Bewährte Methoden für das Entwerfen von Authentifizierungswebseiten

In diesem Thema werden bewährte Methoden für das Entwerfen von Webseiten beschrieben, die Webauthentifizierungsbroker für die Anmeldung verwenden.

-   [Verwendung von Metatags](#use-of-metatags)
-   [Verwenden der Windows 8 CSS-Formatierung](#use-of-windows-8-css-styling)
-   [Verwendung von Farbe und Designs](#use-of-color-and-themes)
-   [Ausrichtung](#alignment)
-   [Entwerfen für Snap](#designing-for-snap)
-   [Entwerfen für eine schnelle und schnelle Anmeldung](#designing-for-a-fast-and-fluid-login-experience)
-   [Sicherheitshinweise](#security-considerations)
-   [Verwandte Themen](#related-topics)

## <a name="use-of-metatags"></a>Verwendung von Metatags

Mithilfe von Metatags kann der Anbieter "Contoso Social" den Titel, das Symbol und die Farbe des Headers angeben. In der HTML-Beispieldatei (WebAuthLogin.html) erfolgt dies mithilfe des folgenden Codes.


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



Dies ermöglicht Windows, das Vorhandensein des Anbieters auf hervorgehobene Weise in den Header der Benutzeroberfläche zu integrieren, wie im folgenden Screenshot durch das rote Feld hervorgehoben. ![Anmeldeseite mit contoso-Header in der Benutzeroberfläche](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a>Verwenden der Windows 8 CSS-Formatierung

Das bereitgestellte Stylesheet ui-light.css ist das Windows 8 stylesheet, das von Windows Store wird. Sie definiert Windows Store App-Stil für Typografie und Standardsteuerelemente wie Schaltflächen, Textfelder, Links und Kontrollkästchen, um sicherzustellen, dass sie touch-nutzerfreundlich sind. Beim Entwerfen und Anpassen von Webautorisierungsseiten für Windows 8 empfehlen wir Ihnen, dieses Stylesheet so zu verwenden, wie es ist, und es nach Bedarf zu aktualisieren, solange Ihre Webseite weiterhin auf ihre eigene Weise den bewährten Methoden folgt.

Wenn Sie z. B. über ein spezielles Stylesheet verfügen, wie Hyperlinks auf Ihrer Webseite aussehen und aussehen sollen, ist es gut zu denken, um sicherzustellen, dass die von Ihnen zur Verfügung stellende Formatierung auf die gleiche Weise wie Standard-Windows 8-Links benutzerfreundlich ist. Dies ist wichtig für die Consumerbasis, die Windows 8 auf ihren Touchgeräten verwendet.

## <a name="use-of-color-and-themes"></a>Verwendung von Farbe und Designs

In diesem Beispiel wird eine durchdachte Verwendung von Farben auf unterschiedliche Weise veranschaulicht.

-   Weißer Hintergrund für die Webseite. Wie Sie im vorherigen Screenshot sehen können, wird die Webseite auf einer weißen Oberfläche gehostet, die die Breite des Bildschirms umfasst. Um sicherzustellen, dass die Webseite in die Oberfläche integriert ist, wird empfohlen, dass die Webseite einen weißen Hintergrund hat.
-   Farbgebung von Steuerelementen basierend auf Ihrer Markenfarbe. Die CSS-Datei theme-colors.css stellt Stile zur Verfügung, um die Standardfarben von Steuerelementen im Ui-Light-Stylesheet zu überschreiben, um das Design der Steuerelemente der Farbe des Headers zu entsprechen. Im folgenden Screenshot verwenden die Schaltflächen und Links beispielsweise Farben, die von der Kopfzeilenfarbe abgeleitet werden. ![Screenshot der Schaltflächen und des Texts mit der gleichen Farbe wie der Header](images/wab-figure11.png)
-   Headerfarbe. Die Verwendung der Markenfarbe von Contoso im Header erzeugt eine einheitliche Persönlichkeit für die Marke des Anbieters innerhalb der Systembenutzeroberfläche.

## <a name="alignment"></a>Ausrichtung

Die Webseite selbst verfügt über keine Auf padding auf der linken oder rechten Seite, um eine typografische Ausrichtung mit dem Titel in der Kopfzeile auf der linken Seite und dem Symbol in der Kopfzeile auf der rechten Seite zu ermöglichen.

Sie werden auch feststellen, dass Schaltflächen immer rechts unten auf der Webseite ausgerichtet sind (und rechts am Symbol in der Kopfzeile ausgerichtet sind). Dies ist eine bewährte Methode, Windows 8 Benutzer an ähnliche Dialogflüsse mit Schaltflächen in der unteren rechten Ecke gewohnt sind.

## <a name="designing-for-snap"></a>Entwerfen für Snap

In der folgenden Abbildung sehen Sie die Anmelde- und Berechtigungsseiten im Ausrichtungszustand.

![Ausrichtungsansicht des Anmeldebildschirms ](images/wab-figure12.png) . ![Andockansicht der Berechtigungsseite ](images/wab-figure13.png)

In der Beispieldatei ui-webauth.css können Sie die Verwendung von Medienabfragen sehen, die das Layout der Seite für den Ausrichtungszustand basierend auf der für die Webseite verfügbaren Breite optimieren. Der im folgenden Bereich eingeschlossene Codeausschnitt implementiert CSS, das auf den Ausrichtungszustand zugeschnitten ist.


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



In Windows 8 beträgt die Breite des Ausrichtungszustands 320 Pixel. Die Webauthentifizierungsseite belegt in der obigen Benutzeroberfläche 260 Pixel. Wir verwenden einen Wert mit maximaler Breite mit genügend Rand, sodass der Medienabfragecode des Anbieters nicht an die genaue Breite des Ausrichtungszustands gebunden ist.

Bei der Anpassung Ihrer App für die Ausrichtungsansicht ist es wichtig, dass der Benutzer keinen Kontext verliert, den er in den anderen Ansichten der Webauthentifizierungserfahrung (vollständige, Füll- oder Charmansichten) hat. Es ist jedoch wichtig, das Layout und die Hierarchie der Elemente auf der Seite neu zu strukturieren, damit die zum Beibehalten des Kontexts erforderlichen Informationen sichtbar und interaktiv sind. Wir haben einige Beispiele dafür genannt, wie das Beispiel die Webseite für den Ausrichtungszustand an passt.

-   Für die Anmeldeseite im Ausrichtungszustand wurde beispielsweise die Width-Eigenschaft des Eingabetextfelds (wie in ui-light.css angegeben) überschrieben und als kleinerer numerischer Wert festgelegt, sodass das Textfeld nicht horizontal abgeschnitten wird.
-   Als weiteres Beispiel wird der Schriftgrad der Header h1 und h2 im Ausrichtungszustand von 42 pt bzw. 20 pt auf 20 pt und 11 pt reduziert. Dies erfolgt in Übereinstimmung mit der Windows 8-Typverlauf und optimiert text so, dass er im geänderten Viewport kompakter ist.
-   Beachten Sie als weiteres Beispiel, dass die Größe der Symbole auf der Berechtigungsseite kleiner ist (im Vergleich zur seite mit der vollständigen Ansicht oben). Auch hier wird der Kontext beibehalten, während Entwurfsressourcen gegen diejenigen ausgetauscht werden, die für den geänderten Viewport optimaler sind.

## <a name="designing-for-a-fast-and-fluid-login-experience"></a>Entwerfen für eine schnelle und schnelle Anmeldung

Zu Beginn des Entwerfens dieser Webseite haben wir uns darauf besannen, dass es sich bei dieser Seite am besten um eine schnelle und strömungsschnelle Anmeldung handelt. Daher ist die Benutzeroberfläche, die im Flow am wichtigsten ist, das Feld "Benutzername und Kennwort" auf der Anmeldeseite für eine schnelle Eingabe von Anmeldeinformationen. Obwohl wir festgestellt haben, dass es andere gängige Szenarien wie das Abrufen von Kennwörtern und das Verweisen auf Datenschutzbestimmungen gibt, ist die umfassende Erfahrung im Web ein besserer Ort für diese Erfahrungen. Für alle Flows, die sich nicht auf die sichere Webauthentifizierungserfahrung bezieht, wird empfohlen, den Benutzer zum Browser zu navigieren. Dies wird in der HTML-Beispieldatei (WebAuthLogin.html) wie folgt gezeigt: Dadurch werden alle Webseiten geöffnet, mit denen über die Anmelde- oder Berechtigungsseite im Standardbrowser des Benutzers verknüpft ist, wo der Benutzer diese Flows abschließen und dann zur App zurückkehren kann, um sich `<meta name="mswebdialog-newwindowurl" content="*" />` anzumelden.

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Die folgenden Artikel enthalten Anleitungen zum Schreiben von sicherem C++-Code.

-   [Bewährte Sicherheitsmethoden für C++](/cpp/security/security-best-practices-for-cpp)
-   [Patterns & Practices Security Guidance for Applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überlegungen für die Webseitenentwicklung](considerations-for-the-web-page-development.md)
</dt> <dt>

[Häufig gestellte Fragen zum Webauthentifizierungsbroker](faq-for-web-authentication-broker.yml)
</dt> <dt>

[Beispiel-App für das Webauthentifizierungsbroker-SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
