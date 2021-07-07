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
# <a name="best-practices-for-designing-authentication-web-pages"></a><span data-ttu-id="4c15b-103">Bewährte Methoden für das Entwerfen von Authentifizierungswebseiten</span><span class="sxs-lookup"><span data-stu-id="4c15b-103">Best Practices for designing authentication web pages</span></span>

<span data-ttu-id="4c15b-104">In diesem Thema werden bewährte Methoden für das Entwerfen von Webseiten beschrieben, die Webauthentifizierungsbroker für die Anmeldung verwenden.</span><span class="sxs-lookup"><span data-stu-id="4c15b-104">This topic describes best practices for designing web pages that use Web Authentication Broker for logging on.</span></span>

-   [<span data-ttu-id="4c15b-105">Verwendung von Metatags</span><span class="sxs-lookup"><span data-stu-id="4c15b-105">Use of metatags</span></span>](#use-of-metatags)
-   [<span data-ttu-id="4c15b-106">Verwenden der Windows 8 CSS-Formatierung</span><span class="sxs-lookup"><span data-stu-id="4c15b-106">Use of Windows 8 CSS styling</span></span>](#use-of-windows-8-css-styling)
-   [<span data-ttu-id="4c15b-107">Verwendung von Farbe und Designs</span><span class="sxs-lookup"><span data-stu-id="4c15b-107">Use of color and themes</span></span>](#use-of-color-and-themes)
-   [<span data-ttu-id="4c15b-108">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="4c15b-108">Alignment</span></span>](#alignment)
-   [<span data-ttu-id="4c15b-109">Entwerfen für Snap</span><span class="sxs-lookup"><span data-stu-id="4c15b-109">Designing for snap</span></span>](#designing-for-snap)
-   [<span data-ttu-id="4c15b-110">Entwerfen für eine schnelle und schnelle Anmeldung</span><span class="sxs-lookup"><span data-stu-id="4c15b-110">Designing for a fast and fluid login experience</span></span>](#designing-for-a-fast-and-fluid-login-experience)
-   [<span data-ttu-id="4c15b-111">Sicherheitshinweise</span><span class="sxs-lookup"><span data-stu-id="4c15b-111">Security Considerations</span></span>](#security-considerations)
-   [<span data-ttu-id="4c15b-112">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="4c15b-112">Related topics</span></span>](#related-topics)

## <a name="use-of-metatags"></a><span data-ttu-id="4c15b-113">Verwendung von Metatags</span><span class="sxs-lookup"><span data-stu-id="4c15b-113">Use of metatags</span></span>

<span data-ttu-id="4c15b-114">Mithilfe von Metatags kann der Anbieter "Contoso Social" den Titel, das Symbol und die Farbe des Headers angeben.</span><span class="sxs-lookup"><span data-stu-id="4c15b-114">Using metatags, the provider "Contoso Social" can specify the title, the icon and the color of the header.</span></span> <span data-ttu-id="4c15b-115">In der HTML-Beispieldatei (WebAuthLogin.html) erfolgt dies mithilfe des folgenden Codes.</span><span class="sxs-lookup"><span data-stu-id="4c15b-115">In the sample HTML file (WebAuthLogin.html), this is done by using the following code.</span></span>


```HTML
<meta name="mswebdialog-title" content="Contoso Social" />
<meta name="mswebdialog-header-color" content="#326464" /> <!-- Your brand color -->
<meta name="mswebdialog-logo" content="contoso_social_glyph.png" />
```



<span data-ttu-id="4c15b-116">Dies ermöglicht Windows, das Vorhandensein des Anbieters auf hervorgehobene Weise in den Header der Benutzeroberfläche zu integrieren, wie im folgenden Screenshot durch das rote Feld hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="4c15b-116">This allows Windows to integrate the presence of the provider in a prominent way in the header of the UI as highlighted by the red box in the following screenshot.</span></span> ![Anmeldeseite mit contoso-Header in der Benutzeroberfläche](images/wab-figure17.png)

## <a name="use-of-windows-8-css-styling"></a><span data-ttu-id="4c15b-118">Verwenden der Windows 8 CSS-Formatierung</span><span class="sxs-lookup"><span data-stu-id="4c15b-118">Use of Windows 8 CSS styling</span></span>

<span data-ttu-id="4c15b-119">Das bereitgestellte Stylesheet ui-light.css ist das Windows 8 stylesheet, das von Windows Store wird.</span><span class="sxs-lookup"><span data-stu-id="4c15b-119">The provided ui-light.css stylesheet is the Windows 8 stylesheet used by Windows Store apps.</span></span> <span data-ttu-id="4c15b-120">Sie definiert Windows Store App-Stil für Typografie und Standardsteuerelemente wie Schaltflächen, Textfelder, Links und Kontrollkästchen, um sicherzustellen, dass sie touch-nutzerfreundlich sind.</span><span class="sxs-lookup"><span data-stu-id="4c15b-120">It defines Windows Store app styling for typography and standard controls, like buttons, text boxes, hyperlinks, and check boxes to make sure they are touch friendly.</span></span> <span data-ttu-id="4c15b-121">Beim Entwerfen und Anpassen von Webautorisierungsseiten für Windows 8 empfehlen wir Ihnen, dieses Stylesheet so zu verwenden, wie es ist, und es nach Bedarf zu aktualisieren, solange Ihre Webseite weiterhin auf ihre eigene Weise den bewährten Methoden folgt.</span><span class="sxs-lookup"><span data-stu-id="4c15b-121">When designing and tailoring web authorization pages for Windows 8, we encourage you to use this stylesheet as is and update it as needed as long as your web page still follows best-practices in its own way.</span></span>

<span data-ttu-id="4c15b-122">Wenn Sie z. B. über ein spezielles Stylesheet verfügen, wie Hyperlinks auf Ihrer Webseite aussehen und aussehen sollen, ist es gut zu denken, um sicherzustellen, dass die von Ihnen zur Verfügung stellende Formatierung auf die gleiche Weise wie Standard-Windows 8-Links benutzerfreundlich ist.</span><span class="sxs-lookup"><span data-stu-id="4c15b-122">For example, if you have a special stylesheet for what hyperlinks should look and feel like on your web page, it's good to be thoughtful to make sure that the styling you provide is touch friendly in the same way as standard Windows 8 hyperlinks.</span></span> <span data-ttu-id="4c15b-123">Dies ist wichtig für die Consumerbasis, die Windows 8 auf ihren Touchgeräten verwendet.</span><span class="sxs-lookup"><span data-stu-id="4c15b-123">This is essential for the consumer base using Windows 8 on their touch devices.</span></span>

## <a name="use-of-color-and-themes"></a><span data-ttu-id="4c15b-124">Verwendung von Farbe und Designs</span><span class="sxs-lookup"><span data-stu-id="4c15b-124">Use of color and themes</span></span>

<span data-ttu-id="4c15b-125">In diesem Beispiel wird eine durchdachte Verwendung von Farben auf unterschiedliche Weise veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="4c15b-125">This sample demonstrates a thoughtful use of color in a few different ways.</span></span>

-   <span data-ttu-id="4c15b-126">Weißer Hintergrund für die Webseite.</span><span class="sxs-lookup"><span data-stu-id="4c15b-126">White background for the web page.</span></span> <span data-ttu-id="4c15b-127">Wie Sie im vorherigen Screenshot sehen können, wird die Webseite auf einer weißen Oberfläche gehostet, die die Breite des Bildschirms umfasst.</span><span class="sxs-lookup"><span data-stu-id="4c15b-127">As you can tell from the previous screenshot, the web page is hosted within a white surface that spans the width of the screen.</span></span> <span data-ttu-id="4c15b-128">Um sicherzustellen, dass die Webseite in die Oberfläche integriert ist, wird empfohlen, dass die Webseite einen weißen Hintergrund hat.</span><span class="sxs-lookup"><span data-stu-id="4c15b-128">To make sure that the web page integrates with the surface, it is advised that the web page should have a white background.</span></span>
-   <span data-ttu-id="4c15b-129">Farbgebung von Steuerelementen basierend auf Ihrer Markenfarbe.</span><span class="sxs-lookup"><span data-stu-id="4c15b-129">Colorizing controls based on your brand color.</span></span> <span data-ttu-id="4c15b-130">Die CSS-Datei theme-colors.css stellt Stile zur Verfügung, um die Standardfarben von Steuerelementen im Ui-Light-Stylesheet zu überschreiben, um das Design der Steuerelemente der Farbe des Headers zu entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4c15b-130">The CSS file theme-colors.css provides styling to override the standard colors of controls in the ui-light stylesheet to match the theming of the controls to the color of the header.</span></span> <span data-ttu-id="4c15b-131">Im folgenden Screenshot verwenden die Schaltflächen und Links beispielsweise Farben, die von der Kopfzeilenfarbe abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="4c15b-131">For example, in the following screenshot, the buttons and hyperlinks take on colors derived from the header color.</span></span> ![Screenshot der Schaltflächen und des Texts mit der gleichen Farbe wie der Header](images/wab-figure11.png)
-   <span data-ttu-id="4c15b-133">Headerfarbe.</span><span class="sxs-lookup"><span data-stu-id="4c15b-133">Header color.</span></span> <span data-ttu-id="4c15b-134">Die Verwendung der Markenfarbe von Contoso im Header erzeugt eine einheitliche Persönlichkeit für die Marke des Anbieters innerhalb der Systembenutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="4c15b-134">The use of Contoso's brand color in the header creates a unified personality for the provider's brand within the system UI.</span></span>

## <a name="alignment"></a><span data-ttu-id="4c15b-135">Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="4c15b-135">Alignment</span></span>

<span data-ttu-id="4c15b-136">Die Webseite selbst verfügt über keine Auf padding auf der linken oder rechten Seite, um eine typografische Ausrichtung mit dem Titel in der Kopfzeile auf der linken Seite und dem Symbol in der Kopfzeile auf der rechten Seite zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="4c15b-136">The web page itself has no padding on the left or the right to allow for typographic alignment with the title in the header on the left and the icon in the header on the right.</span></span>

<span data-ttu-id="4c15b-137">Sie werden auch feststellen, dass Schaltflächen immer rechts unten auf der Webseite ausgerichtet sind (und rechts am Symbol in der Kopfzeile ausgerichtet sind).</span><span class="sxs-lookup"><span data-stu-id="4c15b-137">You will also notice that buttons are always bottom-right aligned in the web page (and right aligned with the icon in the header).</span></span> <span data-ttu-id="4c15b-138">Dies ist eine bewährte Methode, Windows 8 Benutzer an ähnliche Dialogflüsse mit Schaltflächen in der unteren rechten Ecke gewohnt sind.</span><span class="sxs-lookup"><span data-stu-id="4c15b-138">This is best-practice as Windows 8 users will be accustomed to similar dialog flows having buttons in the bottom-right.</span></span>

## <a name="designing-for-snap"></a><span data-ttu-id="4c15b-139">Entwerfen für Snap</span><span class="sxs-lookup"><span data-stu-id="4c15b-139">Designing for snap</span></span>

<span data-ttu-id="4c15b-140">In der folgenden Abbildung sehen Sie die Anmelde- und Berechtigungsseiten im Ausrichtungszustand.</span><span class="sxs-lookup"><span data-stu-id="4c15b-140">In the following image, you can see the login and permissions pages in snap state.</span></span>

![<span data-ttu-id="4c15b-141">Ausrichtungsansicht des Anmeldebildschirms</span><span class="sxs-lookup"><span data-stu-id="4c15b-141">snap view of the login screen</span></span> ](images/wab-figure12.png) <span data-ttu-id="4c15b-142">.</span><span class="sxs-lookup"><span data-stu-id="4c15b-142">.</span></span> ![<span data-ttu-id="4c15b-143">Andockansicht der Berechtigungsseite</span><span class="sxs-lookup"><span data-stu-id="4c15b-143">snap view of the permissions page</span></span> ](images/wab-figure13.png)

<span data-ttu-id="4c15b-144">In der Beispieldatei ui-webauth.css können Sie die Verwendung von Medienabfragen sehen, die das Layout der Seite für den Ausrichtungszustand basierend auf der für die Webseite verfügbaren Breite optimieren.</span><span class="sxs-lookup"><span data-stu-id="4c15b-144">In the sample file ui-webauth.css, you can see the use of media queries that optimize the layout of the page for snap state based on width available for the web page.</span></span> <span data-ttu-id="4c15b-145">Der im folgenden Bereich eingeschlossene Codeausschnitt implementiert CSS, das auf den Ausrichtungszustand zugeschnitten ist.</span><span class="sxs-lookup"><span data-stu-id="4c15b-145">The code snippet enclosed in the following scope implements CSS tailored for snap state.</span></span>


```HTML
@media screen and (max-width: 500px) 
{
…
}
```



<span data-ttu-id="4c15b-146">In Windows 8 beträgt die Breite des Ausrichtungszustands 320 Pixel.</span><span class="sxs-lookup"><span data-stu-id="4c15b-146">In Windows 8, the width of the snap state is 320 pixels.</span></span> <span data-ttu-id="4c15b-147">Die Webauthentifizierungsseite belegt in der obigen Benutzeroberfläche 260 Pixel.</span><span class="sxs-lookup"><span data-stu-id="4c15b-147">The web-auth page occupies 260 pixels in the UI above.</span></span> <span data-ttu-id="4c15b-148">Wir verwenden einen Wert mit maximaler Breite mit genügend Rand, sodass der Medienabfragecode des Anbieters nicht an die genaue Breite des Ausrichtungszustands gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="4c15b-148">We're using a max-width value with enough margin, so the media query code of the provider is not bound to the exact width of the snap state.</span></span>

<span data-ttu-id="4c15b-149">Bei der Anpassung Ihrer App für die Ausrichtungsansicht ist es wichtig, dass der Benutzer keinen Kontext verliert, den er in den anderen Ansichten der Webauthentifizierungserfahrung (vollständige, Füll- oder Charmansichten) hat. Es ist jedoch wichtig, das Layout und die Hierarchie der Elemente auf der Seite neu zu strukturieren, damit die zum Beibehalten des Kontexts erforderlichen Informationen sichtbar und interaktiv sind.</span><span class="sxs-lookup"><span data-stu-id="4c15b-149">In tailoring your app for the snap view, it's important that user does not lose any context that they have in the other views of web auth experience (full, fill or charm views), but it's valuable to re-structure the layout and hierarchy of the elements in the page so that the information needed to retain context is visible and interactive.</span></span> <span data-ttu-id="4c15b-150">Wir haben einige Beispiele dafür genannt, wie das Beispiel die Webseite für den Ausrichtungszustand an passt.</span><span class="sxs-lookup"><span data-stu-id="4c15b-150">We've called out some examples of how the sample tailors the web page for the snap state.</span></span>

-   <span data-ttu-id="4c15b-151">Für die Anmeldeseite im Ausrichtungszustand wurde beispielsweise die Width-Eigenschaft des Eingabetextfelds (wie in ui-light.css angegeben) überschrieben und als kleinerer numerischer Wert festgelegt, sodass das Textfeld nicht horizontal abgeschnitten wird.</span><span class="sxs-lookup"><span data-stu-id="4c15b-151">As an example, for the login page in snap state, the width property of the input text field (as specified in ui-light.css) has been overridden and been set as smaller numerical value, so that the text field is not horizontally clipped.</span></span>
-   <span data-ttu-id="4c15b-152">Als weiteres Beispiel wird der Schriftgrad der Header h1 und h2 im Ausrichtungszustand von 42 pt bzw. 20 pt auf 20 pt und 11 pt reduziert.</span><span class="sxs-lookup"><span data-stu-id="4c15b-152">As another example, in snap state, the font size of the h1 and h2 headers is reduced to 20 pt and 11 pt from 42 pt and 20 pt respectively.</span></span> <span data-ttu-id="4c15b-153">Dies erfolgt in Übereinstimmung mit der Windows 8-Typverlauf und optimiert text so, dass er im geänderten Viewport kompakter ist.</span><span class="sxs-lookup"><span data-stu-id="4c15b-153">This is done in accordance with the Windows 8 type ramp, and optimizes text to be more compact in the changed viewport.</span></span>
-   <span data-ttu-id="4c15b-154">Beachten Sie als weiteres Beispiel, dass die Größe der Symbole auf der Berechtigungsseite kleiner ist (im Vergleich zur seite mit der vollständigen Ansicht oben).</span><span class="sxs-lookup"><span data-stu-id="4c15b-154">As another example, notice the sizes of the icons in the permissions page are smaller (compare to the full view page above).</span></span> <span data-ttu-id="4c15b-155">Auch hier wird der Kontext beibehalten, während Entwurfsressourcen gegen diejenigen ausgetauscht werden, die für den geänderten Viewport optimaler sind.</span><span class="sxs-lookup"><span data-stu-id="4c15b-155">Again, this is done to retain context, while swapping design assets for those more optimal for the changed viewport.</span></span>

## <a name="designing-for-a-fast-and-fluid-login-experience"></a><span data-ttu-id="4c15b-156">Entwerfen für eine schnelle und schnelle Anmeldung</span><span class="sxs-lookup"><span data-stu-id="4c15b-156">Designing for a fast and fluid login experience</span></span>

<span data-ttu-id="4c15b-157">Zu Beginn des Entwerfens dieser Webseite haben wir uns darauf besannen, dass es sich bei dieser Seite am besten um eine schnelle und strömungsschnelle Anmeldung handelt.</span><span class="sxs-lookup"><span data-stu-id="4c15b-157">Early in the designing of this web page, we made a stake in the ground that one thing that this page is best at is a fast and fluid login experience.</span></span> <span data-ttu-id="4c15b-158">Daher ist die Benutzeroberfläche, die im Flow am wichtigsten ist, das Feld "Benutzername und Kennwort" auf der Anmeldeseite für eine schnelle Eingabe von Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="4c15b-158">Thus, the UI that is most prominent in the flow is the username and password field in the login page for a quick credential entry experience.</span></span> <span data-ttu-id="4c15b-159">Obwohl wir festgestellt haben, dass es andere gängige Szenarien wie das Abrufen von Kennwörtern und das Verweisen auf Datenschutzbestimmungen gibt, ist die umfassende Erfahrung im Web ein besserer Ort für diese Erfahrungen.</span><span class="sxs-lookup"><span data-stu-id="4c15b-159">While we identified that there are other common scenarios such as password retrieval, and referencing privacy statements, the rich experience of the web is a better place for those experiences.</span></span> <span data-ttu-id="4c15b-160">Für alle Flows, die sich nicht auf die sichere Webauthentifizierungserfahrung bezieht, wird empfohlen, den Benutzer zum Browser zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="4c15b-160">For all flows not related to secure web auth experience, we recommend navigating the user to the browser.</span></span> <span data-ttu-id="4c15b-161">Dies wird in der HTML-Beispieldatei (WebAuthLogin.html) wie folgt gezeigt: Dadurch werden alle Webseiten geöffnet, mit denen über die Anmelde- oder Berechtigungsseite im Standardbrowser des Benutzers verknüpft ist, wo der Benutzer diese Flows abschließen und dann zur App zurückkehren kann, um sich `<meta name="mswebdialog-newwindowurl" content="*" />` anzumelden.</span><span class="sxs-lookup"><span data-stu-id="4c15b-161">This is shown in the sample HTML file (WebAuthLogin.html) as follows: `<meta name="mswebdialog-newwindowurl" content="*" />` This opens all web pages linked to from the login or permissions page in the user's default browser where the user can complete these flows and then return to the app to log in.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="4c15b-162">Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="4c15b-162">Security Considerations</span></span>

<span data-ttu-id="4c15b-163">Die folgenden Artikel enthalten Anleitungen zum Schreiben von sicherem C++-Code.</span><span class="sxs-lookup"><span data-stu-id="4c15b-163">The following articles provide guidance for writing secure C++ code.</span></span>

-   [<span data-ttu-id="4c15b-164">Bewährte Sicherheitsmethoden für C++</span><span class="sxs-lookup"><span data-stu-id="4c15b-164">Security Best Practices for C++</span></span>](/cpp/security/security-best-practices-for-cpp)
-   <span data-ttu-id="4c15b-165">[Patterns & Practices Security Guidance for Applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span><span class="sxs-lookup"><span data-stu-id="4c15b-165">[Patterns & Practices Security Guidance for Applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c15b-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4c15b-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c15b-167">Überlegungen für die Webseitenentwicklung</span><span class="sxs-lookup"><span data-stu-id="4c15b-167">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="4c15b-168">Häufig gestellte Fragen zum Webauthentifizierungsbroker</span><span class="sxs-lookup"><span data-stu-id="4c15b-168">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.yml)
</dt> <dt>

[<span data-ttu-id="4c15b-169">Beispiel-App für das Webauthentifizierungsbroker-SDK</span><span class="sxs-lookup"><span data-stu-id="4c15b-169">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="4c15b-170">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="4c15b-170">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
