---
description: In diesem Thema werden bewährte Methoden für das Entwerfen von Webseiten beschrieben, die Web Authentication Broker für die Anmeldung verwenden.
ms.assetid: 271EC68B-5E58-4C1C-B631-DED6A694E98F
title: Bewährte Methoden für das Entwerfen von Authentifizierungswebseiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6360e313b49a69c16aebf532911bcdf562f9a4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344368"
---
# <a name="best-practices-for-designing-authentication-web-pages"></a>Bewährte Methoden für das Entwerfen von Authentifizierungswebseiten

In diesem Thema werden bewährte Methoden für das Entwerfen von Webseiten beschrieben, die Web Authentication Broker für die Anmeldung verwenden.

-   [Verwendung von Metatags](#use-of-metatags)
-   [Verwendung von Windows 8 CSS-Formatvorlagen](#use-of-windows-8-css-styling)
-   [Verwendung von Farbe und Designs](#use-of-color-and-themes)
-   [Ausrichtung](#alignment)
-   [Entwerfen für Snap-in](#designing-for-snap)
-   [Entwerfen für eine schnelle und fließende Anmeldung](#designing-for-a-fast-and-fluid-login-experience)
-   [Sicherheitshinweise](#security-considerations)
-   [Zugehörige Themen](#related-topics)

## <a name="use-of-metatags"></a>Verwendung von Metatags

Mithilfe von Metatags kann der Anbieter "" in "" von "" von "" mit dem Titel "", dem Symbol und der Farbe des Headers angegeben werden. In der HTML-Beispieldatei (WebAuthLogin.html) wird dies mithilfe des folgenden Codes erreicht.


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



Dadurch wird es Windows ermöglicht, das vorhanden sein des Anbieters auf eine deutliche Weise im Header der Benutzeroberfläche zu integrieren, wie im folgenden Screenshot im roten Feld hervorgehoben. ![Anmeldeseite, die den Header "%" in der Benutzeroberfläche anzeigt](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a>Verwendung von Windows 8 CSS-Formatvorlagen

Das bereitgestellte "UI-Light. CSS-Stylesheet ist das Windows 8-Stylesheet, das von Windows Store-Apps verwendet wird. Es definiert das Windows Store-App-Format für typografiesteuer Elemente und Standard Steuerelemente wie Schaltflächen, Textfelder, Hyperlinks und Kontrollkästchen, um sicherzustellen, dass Sie benutzerfreundlich sind. Beim Entwerfen und Anpassen von webautorisierungs Seiten für Windows 8 empfiehlt es sich, dieses Stylesheet unverändert zu verwenden und es nach Bedarf zu aktualisieren, sofern Ihre Webseite weiterhin bewährte Methoden auf die gleiche Weise befolgt.

Wenn Sie z. b. über ein spezielles Stylesheet verfügen, für das die Hyperlinks auf der Webseite aussehen und angezeigt werden sollen, ist es gut, dass die von Ihnen bereitgestellte Formatierung auf die gleiche Weise wie standardmäßige Windows 8-Hyperlinks für Sie geeignet ist. Dies ist für die consumerbasis mit Windows 8 auf Ihren Berührungs Geräten von entscheidender Bedeutung.

## <a name="use-of-color-and-themes"></a>Verwendung von Farbe und Designs

Dieses Beispiel veranschaulicht eine durchdachte Verwendung von Farben auf verschiedene Weise.

-   Weißer Hintergrund für die Webseite. Wie Sie im vorherigen Screenshot erkennen können, wird die Webseite innerhalb einer weißen Oberfläche gehostet, die die Breite des Bildschirms umfasst. Um sicherzustellen, dass die Webseite in die-Oberfläche integriert wird, wird empfohlen, dass die Webseite einen weißen Hintergrund hat.
-   Farbliche Kennzeichnung von Steuerelementen basierend auf Ihrer Markenfarbe. Die CSS-Datei Theme-Colors. CSS bietet Formatierungs Verfahren zum Überschreiben der Standardfarben von Steuerelementen im lightweightstylesheet für die Benutzeroberfläche, um die Design der Steuerelemente mit der Farbe des Headers abzugleichen. Im folgenden Screenshot werden z. b. die Schaltflächen und Hyperlinks von Farben übernommen, die von der Header Farbe abgeleitet werden. ![Screenshot der Schaltflächen und des Texts mit der gleichen Farbe wie der Header](images/wab-figure11.png)
-   Header Farbe. Die Verwendung der Markenfarbe von "fium" in der Kopfzeile erstellt eine einheitliche Persönlichkeit für die Marke des Anbieters innerhalb der Systembenutzer Oberfläche.

## <a name="alignment"></a>Ausrichtung

Die Webseite selbst hat keine Auffüll Zeichen auf der linken oder rechten Seite, um die typografische Ausrichtung mit dem Titel in der Kopfzeile auf der linken Seite und das Symbol in der Kopfzeile auf der rechten Seite zuzulassen.

Sie werden auch bemerken, dass die Schaltflächen immer rechts unten auf der Webseite ausgerichtet sind (und rechtsbündig mit dem Symbol im Header). Dies ist eine bewährte Vorgehensweise, da Windows 8-Benutzer an ähnliche Dialog Abläufe mit Schaltflächen in der unteren rechten Ecke gewöhnt werden.

## <a name="designing-for-snap"></a>Entwerfen für Snap-in

In der folgenden Abbildung werden die Anmelde-und Berechtigungs Seiten im Snap-in-Zustand angezeigt.

![Ansicht "anzeigen" des Anmeldebildschirms ](images/wab-figure12.png) . ![Ansicht "Ansicht" der Seite "Berechtigungen" ](images/wab-figure13.png)

In der Beispieldatei UI-webauth. CSS können Sie die Verwendung von Medien Abfragen anzeigen, mit denen das Layout der Seite für den Snap-in auf der Grundlage der für die Webseite verfügbaren Breite optimiert wird. Der im folgenden Bereich eingeschlossene Code Ausschnitt implementiert CSS, das für den Andock Zustand zugeschnitten ist.


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



In Windows 8 ist die Breite des Andock Zustands 320 Pixel. Die webanwendungsseite belegt 260 Pixel in der obigen Benutzeroberfläche. Wir verwenden einen Wert der maximalen Breite mit ausreichendem Rand, sodass der Medien Abfrage Code des Anbieters nicht an die exakte Breite des Andock Zustands gebunden ist.

Wenn Sie Ihre APP für die Snap-Ansicht anpassen, ist es wichtig, dass der Benutzer keinen Kontext verliert, der in den anderen Ansichten der Webauthentifizierungs Darstellung (Full, Fill oder Charm) enthalten ist, aber es ist wertvoll, das Layout und die Hierarchie der Elemente auf der Seite neu zu strukturieren, damit die Informationen, die erforderlich sind, um den Kontext beizubehalten, sichtbar und interaktiv sind. Wir haben einige Beispiele dafür angegeben, wie das Beispiel die Webseite für den Andock Zustand tailtet.

-   Beispiel: für die Anmeldeseite im Snap-in-Zustand wurde die Width-Eigenschaft des Eingabetext Felds (wie in "UI-Light. CSS angegeben) überschrieben und als kleinerer numerischer Wert festgelegt, sodass das Textfeld nicht horizontal abgeschnitten wird.
-   Ein weiteres Beispiel: im Snap-in-Zustand wird der Schrift Grad der Header H1 und H2 auf 20 PT und 11 PT von 42 PT bzw. 20 PT reduziert. Dies erfolgt in Übereinstimmung mit der Windows 8-typrampe und optimiert den Text im geänderten Viewport als kompakter.
-   Beachten Sie als weiteres Beispiel, dass die Größe der Symbole auf der Seite Berechtigungen kleiner ist (im Vergleich zur vollständigen Ansichts Seite oben). Dies erfolgt wiederum, um den Kontext beizubehalten, während Sie Entwurfs Ressourcen austauschen, um die optimalen für den geänderten Viewport zu erzielen.

## <a name="designing-for-a-fast-and-fluid-login-experience"></a>Entwerfen für eine schnelle und fließende Anmeldung

Schon früh im Entwurf dieser Webseite haben wir einen Anteil daran gemacht, dass es sich bei dieser Seite am besten um eine schnelle und flüssige Anmeldung handelt. Daher ist die Benutzeroberfläche, die im Flow am wichtigsten ist, das Feld Benutzername und Kennwort auf der Anmeldeseite, um einen schnellen Anmelde Informations Eintrag zu erhalten. Wir haben festgestellt, dass es andere gängige Szenarien wie das Abrufen von Kenn Wörtern und das verweisen auf Datenschutzbestimmungen gibt Für alle Flows, die nicht mit der sicheren Webauthentifizierung verknüpft sind, wird empfohlen, den Benutzer zum Browser zu navigieren. Dies wird in der HTML-Beispieldatei (WebAuthLogin.html) wie folgt angezeigt: `<meta name="mswebdialog-newwindowurl" content="*" />` dadurch werden alle Webseiten geöffnet, die über die Seite Anmeldung oder Berechtigungen im Standardbrowser des Benutzers verknüpft sind, in der der Benutzer diese Flows ausführen und dann zur Anmeldung zur APP zurückkehren kann.

## <a name="security-considerations"></a>Überlegungen zur Sicherheit

Die folgenden Artikel bieten Anleitungen zum Schreiben von sicherem C++-Code.

-   [Bewährte Sicherheitsmethoden für C++](/cpp/security/security-best-practices-for-cpp)
-   [Muster & Praktiken Sicherheits Leit Fäden für Anwendungen](/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Überlegungen für die Webseitenentwicklung](considerations-for-the-web-page-development.md)
</dt> <dt>

[Häufig gestellte Fragen zum Webauthentifizierungs Broker](faq-for-web-authentication-broker.md)
</dt> <dt>

[Beispiel-App für das Web Authentication Broker SDK](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
