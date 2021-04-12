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
# <a name="best-practices-for-designing-authentication-web-pages"></a><span data-ttu-id="f0f86-103">Bewährte Methoden für das Entwerfen von Authentifizierungswebseiten</span><span class="sxs-lookup"><span data-stu-id="f0f86-103">Best Practices for designing authentication web pages</span></span>

<span data-ttu-id="f0f86-104">In diesem Thema werden bewährte Methoden für das Entwerfen von Webseiten beschrieben, die Web Authentication Broker für die Anmeldung verwenden.</span><span class="sxs-lookup"><span data-stu-id="f0f86-104">This topic describes best practices for designing web pages that use Web Authentication Broker for logging on.</span></span>

-   [<span data-ttu-id="f0f86-105">Verwendung von Metatags</span><span class="sxs-lookup"><span data-stu-id="f0f86-105">Use of metatags</span></span>](#use-of-metatags)
-   [<span data-ttu-id="f0f86-106">Verwendung von Windows 8 CSS-Formatvorlagen</span><span class="sxs-lookup"><span data-stu-id="f0f86-106">Use of Windows 8 CSS styling</span></span>](#use-of-windows-8-css-styling)
-   [<span data-ttu-id="f0f86-107">Verwendung von Farbe und Designs</span><span class="sxs-lookup"><span data-stu-id="f0f86-107">Use of color and themes</span></span>](#use-of-color-and-themes)
-   [<span data-ttu-id="f0f86-108">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="f0f86-108">Alignment</span></span>](#alignment)
-   [<span data-ttu-id="f0f86-109">Entwerfen für Snap-in</span><span class="sxs-lookup"><span data-stu-id="f0f86-109">Designing for snap</span></span>](#designing-for-snap)
-   [<span data-ttu-id="f0f86-110">Entwerfen für eine schnelle und fließende Anmeldung</span><span class="sxs-lookup"><span data-stu-id="f0f86-110">Designing for a fast and fluid login experience</span></span>](#designing-for-a-fast-and-fluid-login-experience)
-   [<span data-ttu-id="f0f86-111">Sicherheitshinweise</span><span class="sxs-lookup"><span data-stu-id="f0f86-111">Security Considerations</span></span>](#security-considerations)
-   [<span data-ttu-id="f0f86-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0f86-112">Related topics</span></span>](#related-topics)

## <a name="use-of-metatags"></a><span data-ttu-id="f0f86-113">Verwendung von Metatags</span><span class="sxs-lookup"><span data-stu-id="f0f86-113">Use of metatags</span></span>

<span data-ttu-id="f0f86-114">Mithilfe von Metatags kann der Anbieter "" in "" von "" von "" mit dem Titel "", dem Symbol und der Farbe des Headers angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f0f86-114">Using metatags, the provider "Contoso Social" can specify the title, the icon and the color of the header.</span></span> <span data-ttu-id="f0f86-115">In der HTML-Beispieldatei (WebAuthLogin.html) wird dies mithilfe des folgenden Codes erreicht.</span><span class="sxs-lookup"><span data-stu-id="f0f86-115">In the sample HTML file (WebAuthLogin.html), this is done by using the following code.</span></span>


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



<span data-ttu-id="f0f86-116">Dadurch wird es Windows ermöglicht, das vorhanden sein des Anbieters auf eine deutliche Weise im Header der Benutzeroberfläche zu integrieren, wie im folgenden Screenshot im roten Feld hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="f0f86-116">This allows Windows to integrate the presence of the provider in a prominent way in the header of the UI as highlighted by the red box in the following screenshot.</span></span> ![Anmeldeseite, die den Header "%" in der Benutzeroberfläche anzeigt](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a><span data-ttu-id="f0f86-118">Verwendung von Windows 8 CSS-Formatvorlagen</span><span class="sxs-lookup"><span data-stu-id="f0f86-118">Use of Windows 8 CSS styling</span></span>

<span data-ttu-id="f0f86-119">Das bereitgestellte "UI-Light. CSS-Stylesheet ist das Windows 8-Stylesheet, das von Windows Store-Apps verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f0f86-119">The provided ui-light.css stylesheet is the Windows 8 stylesheet used by Windows Store apps.</span></span> <span data-ttu-id="f0f86-120">Es definiert das Windows Store-App-Format für typografiesteuer Elemente und Standard Steuerelemente wie Schaltflächen, Textfelder, Hyperlinks und Kontrollkästchen, um sicherzustellen, dass Sie benutzerfreundlich sind.</span><span class="sxs-lookup"><span data-stu-id="f0f86-120">It defines Windows Store app styling for typography and standard controls, like buttons, text boxes, hyperlinks, and check boxes to make sure they are touch friendly.</span></span> <span data-ttu-id="f0f86-121">Beim Entwerfen und Anpassen von webautorisierungs Seiten für Windows 8 empfiehlt es sich, dieses Stylesheet unverändert zu verwenden und es nach Bedarf zu aktualisieren, sofern Ihre Webseite weiterhin bewährte Methoden auf die gleiche Weise befolgt.</span><span class="sxs-lookup"><span data-stu-id="f0f86-121">When designing and tailoring web authorization pages for Windows 8, we encourage you to use this stylesheet as is and update it as needed as long as your web page still follows best-practices in its own way.</span></span>

<span data-ttu-id="f0f86-122">Wenn Sie z. b. über ein spezielles Stylesheet verfügen, für das die Hyperlinks auf der Webseite aussehen und angezeigt werden sollen, ist es gut, dass die von Ihnen bereitgestellte Formatierung auf die gleiche Weise wie standardmäßige Windows 8-Hyperlinks für Sie geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="f0f86-122">For example, if you have a special stylesheet for what hyperlinks should look and feel like on your web page, it's good to be thoughtful to make sure that the styling you provide is touch friendly in the same way as standard Windows 8 hyperlinks.</span></span> <span data-ttu-id="f0f86-123">Dies ist für die consumerbasis mit Windows 8 auf Ihren Berührungs Geräten von entscheidender Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="f0f86-123">This is essential for the consumer base using Windows 8 on their touch devices.</span></span>

## <a name="use-of-color-and-themes"></a><span data-ttu-id="f0f86-124">Verwendung von Farbe und Designs</span><span class="sxs-lookup"><span data-stu-id="f0f86-124">Use of color and themes</span></span>

<span data-ttu-id="f0f86-125">Dieses Beispiel veranschaulicht eine durchdachte Verwendung von Farben auf verschiedene Weise.</span><span class="sxs-lookup"><span data-stu-id="f0f86-125">This sample demonstrates a thoughtful use of color in a few different ways.</span></span>

-   <span data-ttu-id="f0f86-126">Weißer Hintergrund für die Webseite.</span><span class="sxs-lookup"><span data-stu-id="f0f86-126">White background for the web page.</span></span> <span data-ttu-id="f0f86-127">Wie Sie im vorherigen Screenshot erkennen können, wird die Webseite innerhalb einer weißen Oberfläche gehostet, die die Breite des Bildschirms umfasst.</span><span class="sxs-lookup"><span data-stu-id="f0f86-127">As you can tell from the previous screenshot, the web page is hosted within a white surface that spans the width of the screen.</span></span> <span data-ttu-id="f0f86-128">Um sicherzustellen, dass die Webseite in die-Oberfläche integriert wird, wird empfohlen, dass die Webseite einen weißen Hintergrund hat.</span><span class="sxs-lookup"><span data-stu-id="f0f86-128">To make sure that the web page integrates with the surface, it is advised that the web page should have a white background.</span></span>
-   <span data-ttu-id="f0f86-129">Farbliche Kennzeichnung von Steuerelementen basierend auf Ihrer Markenfarbe.</span><span class="sxs-lookup"><span data-stu-id="f0f86-129">Colorizing controls based on your brand color.</span></span> <span data-ttu-id="f0f86-130">Die CSS-Datei Theme-Colors. CSS bietet Formatierungs Verfahren zum Überschreiben der Standardfarben von Steuerelementen im lightweightstylesheet für die Benutzeroberfläche, um die Design der Steuerelemente mit der Farbe des Headers abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="f0f86-130">The CSS file theme-colors.css provides styling to override the standard colors of controls in the ui-light stylesheet to match the theming of the controls to the color of the header.</span></span> <span data-ttu-id="f0f86-131">Im folgenden Screenshot werden z. b. die Schaltflächen und Hyperlinks von Farben übernommen, die von der Header Farbe abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="f0f86-131">For example, in the following screenshot, the buttons and hyperlinks take on colors derived from the header color.</span></span> ![Screenshot der Schaltflächen und des Texts mit der gleichen Farbe wie der Header](images/wab-figure11.png)
-   <span data-ttu-id="f0f86-133">Header Farbe.</span><span class="sxs-lookup"><span data-stu-id="f0f86-133">Header color.</span></span> <span data-ttu-id="f0f86-134">Die Verwendung der Markenfarbe von "fium" in der Kopfzeile erstellt eine einheitliche Persönlichkeit für die Marke des Anbieters innerhalb der Systembenutzer Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="f0f86-134">The use of Contoso's brand color in the header creates a unified personality for the provider's brand within the system UI.</span></span>

## <a name="alignment"></a><span data-ttu-id="f0f86-135">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="f0f86-135">Alignment</span></span>

<span data-ttu-id="f0f86-136">Die Webseite selbst hat keine Auffüll Zeichen auf der linken oder rechten Seite, um die typografische Ausrichtung mit dem Titel in der Kopfzeile auf der linken Seite und das Symbol in der Kopfzeile auf der rechten Seite zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="f0f86-136">The web page itself has no padding on the left or the right to allow for typographic alignment with the title in the header on the left and the icon in the header on the right.</span></span>

<span data-ttu-id="f0f86-137">Sie werden auch bemerken, dass die Schaltflächen immer rechts unten auf der Webseite ausgerichtet sind (und rechtsbündig mit dem Symbol im Header).</span><span class="sxs-lookup"><span data-stu-id="f0f86-137">You will also notice that buttons are always bottom-right aligned in the web page (and right aligned with the icon in the header).</span></span> <span data-ttu-id="f0f86-138">Dies ist eine bewährte Vorgehensweise, da Windows 8-Benutzer an ähnliche Dialog Abläufe mit Schaltflächen in der unteren rechten Ecke gewöhnt werden.</span><span class="sxs-lookup"><span data-stu-id="f0f86-138">This is best-practice as Windows 8 users will be accustomed to similar dialog flows having buttons in the bottom-right.</span></span>

## <a name="designing-for-snap"></a><span data-ttu-id="f0f86-139">Entwerfen für Snap-in</span><span class="sxs-lookup"><span data-stu-id="f0f86-139">Designing for snap</span></span>

<span data-ttu-id="f0f86-140">In der folgenden Abbildung werden die Anmelde-und Berechtigungs Seiten im Snap-in-Zustand angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f0f86-140">In the following image, you can see the login and permissions pages in snap state.</span></span>

![<span data-ttu-id="f0f86-141">Ansicht "anzeigen" des Anmeldebildschirms</span><span class="sxs-lookup"><span data-stu-id="f0f86-141">snap view of the login screen</span></span> ](images/wab-figure12.png) <span data-ttu-id="f0f86-142">.</span><span class="sxs-lookup"><span data-stu-id="f0f86-142">.</span></span> ![<span data-ttu-id="f0f86-143">Ansicht "Ansicht" der Seite "Berechtigungen"</span><span class="sxs-lookup"><span data-stu-id="f0f86-143">snap view of the permissions page</span></span> ](images/wab-figure13.png)

<span data-ttu-id="f0f86-144">In der Beispieldatei UI-webauth. CSS können Sie die Verwendung von Medien Abfragen anzeigen, mit denen das Layout der Seite für den Snap-in auf der Grundlage der für die Webseite verfügbaren Breite optimiert wird.</span><span class="sxs-lookup"><span data-stu-id="f0f86-144">In the sample file ui-webauth.css, you can see the use of media queries that optimize the layout of the page for snap state based on width available for the web page.</span></span> <span data-ttu-id="f0f86-145">Der im folgenden Bereich eingeschlossene Code Ausschnitt implementiert CSS, das für den Andock Zustand zugeschnitten ist.</span><span class="sxs-lookup"><span data-stu-id="f0f86-145">The code snippet enclosed in the following scope implements CSS tailored for snap state.</span></span>


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



<span data-ttu-id="f0f86-146">In Windows 8 ist die Breite des Andock Zustands 320 Pixel.</span><span class="sxs-lookup"><span data-stu-id="f0f86-146">In Windows 8, the width of the snap state is 320 pixels.</span></span> <span data-ttu-id="f0f86-147">Die webanwendungsseite belegt 260 Pixel in der obigen Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="f0f86-147">The web-auth page occupies 260 pixels in the UI above.</span></span> <span data-ttu-id="f0f86-148">Wir verwenden einen Wert der maximalen Breite mit ausreichendem Rand, sodass der Medien Abfrage Code des Anbieters nicht an die exakte Breite des Andock Zustands gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="f0f86-148">We're using a max-width value with enough margin, so the media query code of the provider is not bound to the exact width of the snap state.</span></span>

<span data-ttu-id="f0f86-149">Wenn Sie Ihre APP für die Snap-Ansicht anpassen, ist es wichtig, dass der Benutzer keinen Kontext verliert, der in den anderen Ansichten der Webauthentifizierungs Darstellung (Full, Fill oder Charm) enthalten ist, aber es ist wertvoll, das Layout und die Hierarchie der Elemente auf der Seite neu zu strukturieren, damit die Informationen, die erforderlich sind, um den Kontext beizubehalten, sichtbar und interaktiv sind.</span><span class="sxs-lookup"><span data-stu-id="f0f86-149">In tailoring your app for the snap view, it's important that user does not lose any context that they have in the other views of web auth experience (full, fill or charm views), but it's valuable to re-structure the layout and hierarchy of the elements in the page so that the information needed to retain context is visible and interactive.</span></span> <span data-ttu-id="f0f86-150">Wir haben einige Beispiele dafür angegeben, wie das Beispiel die Webseite für den Andock Zustand tailtet.</span><span class="sxs-lookup"><span data-stu-id="f0f86-150">We've called out some examples of how the sample tailors the web page for the snap state.</span></span>

-   <span data-ttu-id="f0f86-151">Beispiel: für die Anmeldeseite im Snap-in-Zustand wurde die Width-Eigenschaft des Eingabetext Felds (wie in "UI-Light. CSS angegeben) überschrieben und als kleinerer numerischer Wert festgelegt, sodass das Textfeld nicht horizontal abgeschnitten wird.</span><span class="sxs-lookup"><span data-stu-id="f0f86-151">As an example, for the login page in snap state, the width property of the input text field (as specified in ui-light.css) has been overridden and been set as smaller numerical value, so that the text field is not horizontally clipped.</span></span>
-   <span data-ttu-id="f0f86-152">Ein weiteres Beispiel: im Snap-in-Zustand wird der Schrift Grad der Header H1 und H2 auf 20 PT und 11 PT von 42 PT bzw. 20 PT reduziert.</span><span class="sxs-lookup"><span data-stu-id="f0f86-152">As another example, in snap state, the font size of the h1 and h2 headers is reduced to 20 pt and 11 pt from 42 pt and 20 pt respectively.</span></span> <span data-ttu-id="f0f86-153">Dies erfolgt in Übereinstimmung mit der Windows 8-typrampe und optimiert den Text im geänderten Viewport als kompakter.</span><span class="sxs-lookup"><span data-stu-id="f0f86-153">This is done in accordance with the Windows 8 type ramp, and optimizes text to be more compact in the changed viewport.</span></span>
-   <span data-ttu-id="f0f86-154">Beachten Sie als weiteres Beispiel, dass die Größe der Symbole auf der Seite Berechtigungen kleiner ist (im Vergleich zur vollständigen Ansichts Seite oben).</span><span class="sxs-lookup"><span data-stu-id="f0f86-154">As another example, notice the sizes of the icons in the permissions page are smaller (compare to the full view page above).</span></span> <span data-ttu-id="f0f86-155">Dies erfolgt wiederum, um den Kontext beizubehalten, während Sie Entwurfs Ressourcen austauschen, um die optimalen für den geänderten Viewport zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="f0f86-155">Again, this is done to retain context, while swapping design assets for those more optimal for the changed viewport.</span></span>

## <a name="designing-for-a-fast-and-fluid-login-experience"></a><span data-ttu-id="f0f86-156">Entwerfen für eine schnelle und fließende Anmeldung</span><span class="sxs-lookup"><span data-stu-id="f0f86-156">Designing for a fast and fluid login experience</span></span>

<span data-ttu-id="f0f86-157">Schon früh im Entwurf dieser Webseite haben wir einen Anteil daran gemacht, dass es sich bei dieser Seite am besten um eine schnelle und flüssige Anmeldung handelt.</span><span class="sxs-lookup"><span data-stu-id="f0f86-157">Early in the designing of this web page, we made a stake in the ground that one thing that this page is best at is a fast and fluid login experience.</span></span> <span data-ttu-id="f0f86-158">Daher ist die Benutzeroberfläche, die im Flow am wichtigsten ist, das Feld Benutzername und Kennwort auf der Anmeldeseite, um einen schnellen Anmelde Informations Eintrag zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f0f86-158">Thus, the UI that is most prominent in the flow is the username and password field in the login page for a quick credential entry experience.</span></span> <span data-ttu-id="f0f86-159">Wir haben festgestellt, dass es andere gängige Szenarien wie das Abrufen von Kenn Wörtern und das verweisen auf Datenschutzbestimmungen gibt</span><span class="sxs-lookup"><span data-stu-id="f0f86-159">While we identified that there are other common scenarios such as password retrieval, and referencing privacy statements, the rich experience of the web is a better place for those experiences.</span></span> <span data-ttu-id="f0f86-160">Für alle Flows, die nicht mit der sicheren Webauthentifizierung verknüpft sind, wird empfohlen, den Benutzer zum Browser zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="f0f86-160">For all flows not related to secure web auth experience, we recommend navigating the user to the browser.</span></span> <span data-ttu-id="f0f86-161">Dies wird in der HTML-Beispieldatei (WebAuthLogin.html) wie folgt angezeigt: `<meta name="mswebdialog-newwindowurl" content="*" />` dadurch werden alle Webseiten geöffnet, die über die Seite Anmeldung oder Berechtigungen im Standardbrowser des Benutzers verknüpft sind, in der der Benutzer diese Flows ausführen und dann zur Anmeldung zur APP zurückkehren kann.</span><span class="sxs-lookup"><span data-stu-id="f0f86-161">This is shown in the sample HTML file (WebAuthLogin.html) as follows: `<meta name="mswebdialog-newwindowurl" content="*" />` This opens all web pages linked to from the login or permissions page in the user's default browser where the user can complete these flows and then return to the app to log in.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="f0f86-162">Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="f0f86-162">Security Considerations</span></span>

<span data-ttu-id="f0f86-163">Die folgenden Artikel bieten Anleitungen zum Schreiben von sicherem C++-Code.</span><span class="sxs-lookup"><span data-stu-id="f0f86-163">The following articles provide guidance for writing secure C++ code.</span></span>

-   [<span data-ttu-id="f0f86-164">Bewährte Sicherheitsmethoden für C++</span><span class="sxs-lookup"><span data-stu-id="f0f86-164">Security Best Practices for C++</span></span>](/cpp/security/security-best-practices-for-cpp)
-   <span data-ttu-id="f0f86-165">[Muster & Praktiken Sicherheits Leit Fäden für Anwendungen](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="f0f86-165">[Patterns & Practices Security Guidance for Applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0f86-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f0f86-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0f86-167">Überlegungen für die Webseitenentwicklung</span><span class="sxs-lookup"><span data-stu-id="f0f86-167">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="f0f86-168">Häufig gestellte Fragen zum Webauthentifizierungs Broker</span><span class="sxs-lookup"><span data-stu-id="f0f86-168">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)
</dt> <dt>

[<span data-ttu-id="f0f86-169">Beispiel-App für das Web Authentication Broker SDK</span><span class="sxs-lookup"><span data-stu-id="f0f86-169">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="f0f86-170">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="f0f86-170">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
