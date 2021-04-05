---
title: Sicherstellen, dass der Windows-Media Player den HtmlView-Inhalt öffnet
description: Sicherstellen, dass der Windows-Media Player den HtmlView-Inhalt öffnet
ms.assetid: 4ec4e027-4f9c-4a86-9f70-b4014971c070
keywords:
- Windows Media Metadatei-Wiedergabelisten, Windows Media Player öffnen von HtmlView-Inhalt
- Wiedergabelisten, Windows Media Player öffnen von HtmlView-Inhalt
- Metadatei-Wiedergabelisten, Windows Media Player öffnen von HtmlView-Inhalt
- Windows Media Metadatei-Wiedergabelisten, Öffnen von HtmlView-Inhalt
- Wiedergabelisten, Öffnen von HtmlView-Inhalt
- Metadatei-Wiedergabelisten, Öffnen von HtmlView-Inhalt
- Öffnen von HtmlView-Inhalt
- Windows Media Player, Öffnen von HtmlView-Inhalt
- Windows Media Player, HtmlView-Inhalt
- HtmlView, Öffnen von Inhalten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3d3220be44fcc33b3657fb115b0bb57d07d1b928
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710974"
---
# <a name="ensuring-that-windows-media-player-opens-the-htmlview-content"></a><span data-ttu-id="66b29-113">Sicherstellen, dass der Windows-Media Player den HtmlView-Inhalt öffnet</span><span class="sxs-lookup"><span data-stu-id="66b29-113">Ensuring that Windows Media Player Opens the HTMLView Content</span></span>

<span data-ttu-id="66b29-114">Derzeit sind Windows Media Player 9-Serie und Windows Media Player 10 die einzigen Player, die den *HtmlView* -Parameter in. ASX-Dateien unterstützen.</span><span class="sxs-lookup"><span data-stu-id="66b29-114">Currently, Windows Media Player 9 Series and Windows Media Player 10 are the only players that support the *HTMLView* parameter in .asx files.</span></span> <span data-ttu-id="66b29-115">Dies bedeutet, dass Sie Maßnahmen ergreifen sollten, um sicherzustellen, dass der HtmlView-Inhalt in diesen Versionen von Windows Media Player wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="66b29-115">This means you should take steps to ensure that your HTMLView content plays back in these versions of Windows Media Player.</span></span>

<span data-ttu-id="66b29-116">Sie müssen zuerst feststellen, ob die Windows Media Player 9-Serie oder Windows Media Player 10 auf dem Computer des Benutzers installiert ist.</span><span class="sxs-lookup"><span data-stu-id="66b29-116">You must first determine whether Windows Media Player 9 Series or Windows Media Player 10 is installed on the user's computer.</span></span> <span data-ttu-id="66b29-117">Das Windows Media Player SDK enthält ein umfassendes Beispiel, das veranschaulicht, wie verschiedene Versionen von Windows-Media Player in verschiedenen Webbrowsern erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="66b29-117">The Windows Media Player SDK includes a comprehensive sample that demonstrates how to detect different versions of Windows Media Player in different Web browsers.</span></span> <span data-ttu-id="66b29-118">Obwohl eine vollständige Analyse des Erkennungs Beispiels über den Rahmen dieses Abschnitts hinausgeht, gibt es einige grundlegende Schritte, die Sie durchführen können, um zu bestimmen, welche Version von Windows Media Player der Computer des Benutzers ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66b29-118">Although a complete analysis of the detection sample is beyond the scope of this section, there are some basic steps you can take to determine which version of Windows Media Player the user's computer is running.</span></span>

<span data-ttu-id="66b29-119">In der einfachsten Form ist das Erkennen von Windows Media Player das Einbetten des Player-Steuer Elements auf der Webseite, das mit Ihrem HtmlView-Inhalt verknüpft ist, und die anschließende Überprüfung des vom *Player* abgerufenen Werts. **VERSIONINFO** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="66b29-119">In its simplest form, detecting Windows Media Player involves embedding the Player control in the webpage that links to your HTMLView content and then inspecting the value retrieved by the *Player*.**versionInfo** property.</span></span> <span data-ttu-id="66b29-120">Nachdem Sie sich vergewissert haben, dass der Benutzer Windows Media Player 9-oder Windows Media Player 10 installiert hat, können Sie die [Player. openplayer](player-openplayer.md) -Methode verwenden, um den Inhalt im Vollmodus-Player zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="66b29-120">Once you have verified that the user has Windows Media Player 9 Series or Windows Media Player 10 installed, you can use the [Player.openPlayer](player-openplayer.md) method to open the content in the full-mode Player.</span></span> <span data-ttu-id="66b29-121">Die **openplayer** -Methode stellt sicher, dass Ihre Inhalte anfänglich in der Funktion " **jetzt** wiedergeben" des vollmodusplayers angezeigt werden, nicht in einer Skin, im Mini Player Modus oder in einem anderen Player, der sich selbst als Standardprogramm für Dateien mit der Dateinamenerweiterung ". asx" registriert hat, aber HtmlView nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="66b29-121">The **openPlayer** method ensures that your content is initially displayed in the **Now Playing** feature of the full-mode Player, rather than in a skin, in mini Player mode, or in another player that has registered itself as the default program for files with an .asx file name extension, but doesn't support HTMLView.</span></span> <span data-ttu-id="66b29-122">Sobald der Inhalt angezeigt wird, verfügt der Benutzer jedoch über die komplette Kontrolle über Windows Media Player, was bedeutet, dass er eine andere Funktion als **jetzt spielen**, in den Skin-Modus wechseln oder sogar den Player beenden kann.</span><span class="sxs-lookup"><span data-stu-id="66b29-122">Once the content is displayed, however, the user has complete control of Windows Media Player, meaning that he or she can choose to display a feature other than **Now Playing**, switch to skin mode, or even quit the Player.</span></span>

<span data-ttu-id="66b29-123">Im folgenden Beispielcode wird eine Webseite für Internet Explorer erstellt.</span><span class="sxs-lookup"><span data-stu-id="66b29-123">The following example code creates a webpage for Internet Explorer.</span></span> <span data-ttu-id="66b29-124">Auf dieser Seite wird eine. ASX-Datei geöffnet, die eine HtmlView-Webseite angibt, die im vollmodusplayer angezeigt wird, wenn Windows Media Player 9 oder höher installiert ist.</span><span class="sxs-lookup"><span data-stu-id="66b29-124">This page opens an .asx file, which specifies an HTMLView webpage that appears in the full-mode Player when Windows Media Player 9 Series or later is installed.</span></span>


```XML
<HTML>
<BODY>

<!-- This code embeds the Player object in invisible mode. -->
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6" height = 0 width = 0> 
        <PARAM Name = "AutoStart"  Value = "True">
        <PARAM Name = "uiMode" Value = "invisible">
</OBJECT>

<!-- Create a button to open the content. -->
<INPUT Type = "Button"  ID = "btnPlay"  Value = "Play ASX"  onClick = "PlayASX();"/>

<SCRIPT Language = "JScript">

// This function tests the Player version. If it is Windows Media 
// Player 9 Series or later, the script opens the .asx file in the full-mode 
// Player. Otherwise, the script makes the embedded control visible to 
// the user and opens the .asx file in the webpage. 

function PlayASX()
{
    if(parseInt(Player.versionInfo) >= 9)
        {
            // Open the full-mode Player to show HTMLView.
            Player.openPlayer("https://www.proseware.com/MyHTMLView.asx");
        }
        else
        {
            // Open the .asx file in the embedded Player.
            Player.uiMode = "full";
            Player.height = 200;
            Player.width = 200;
            Player.URL = "https://www.proseware.com/MyHTMLView.asx";
        }
}
</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="66b29-125">Der Code im vorherigen Beispiel bettet das Windows Media Player-Steuerelement ein, bei dem die **uiMode** -Eigenschaft auf "unsichtbar" festgelegt ist und die Attribute height und Width auf NULL festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="66b29-125">The code in the preceding example embeds the Windows Media Player control with the **uiMode** property set to "invisible" and the Player height and width attributes set to zero.</span></span> <span data-ttu-id="66b29-126">Der Grund hierfür ist, dass die Benutzeroberfläche des Player-Steuer Elements von der Webseite anfänglich nicht angezeigt werden muss – Sie benötigt lediglich Zugriff auf das Player-Objektmodell.</span><span class="sxs-lookup"><span data-stu-id="66b29-126">This is because the webpage does not require the Player control user interface to be displayed initially—it only requires access to the Player object model.</span></span> <span data-ttu-id="66b29-127">Die Seite zeigt auch eine Eingabe Schaltfläche an, mit der der Benutzer die. ASX-Datei wiedergeben kann.</span><span class="sxs-lookup"><span data-stu-id="66b29-127">The page also displays an input button that enables the user to play the .asx file.</span></span>

<span data-ttu-id="66b29-128">Wenn der Benutzer auf die Schaltfläche "wiedergeben" klickt, wird die Microsoft JScript-Funktion playasx ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="66b29-128">When the user clicks the Play ASX button, the Microsoft JScript function PlayASX runs.</span></span> <span data-ttu-id="66b29-129">Diese Funktion ruft zuerst den Wert für die Eigenschaft "Player **VERSIONINFO** " ab und verwendet dabei die Methode "JScript **Paramet** ", um den numerischen Wert der abgerufenen Zeichenfolge zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="66b29-129">This function first retrieves the value for the Player **versionInfo** property, using the JScript **parseInt** method to inspect the numerical value of the string retrieved.</span></span> <span data-ttu-id="66b29-130">Wenn der numerische Wert größer oder gleich 9 ist (d. h., dass der Benutzer Windows Media Player 9-Reihe installiert hat), ruft der Skriptcode die **openplayer** -Methode auf und übergibt dabei die URL der. ASX-Datei, die den HtmlView-Parameter enthält.</span><span class="sxs-lookup"><span data-stu-id="66b29-130">If the numerical value is greater than or equal to 9 (meaning that the user has Windows Media Player 9 Series installed), the script code calls the **openPlayer** method, passing the URL of the .asx file that contains the HTMLView parameter.</span></span> <span data-ttu-id="66b29-131">Diese Methode öffnet die. ASX-Datei mithilfe von Windows Media Player im vollständigen Modus, gibt den digitalen Medieninhalt in der. ASX-Wiedergabeliste wieder und zeigt den webbasierten HtmlView-Inhalt im Feature " **jetzt** wiedergeben" an.</span><span class="sxs-lookup"><span data-stu-id="66b29-131">This method opens the .asx file using Windows Media Player in full mode, plays the digital media content in the .asx playlist, and displays the HTMLView Web-based content in the **Now Playing** feature.</span></span>

<span data-ttu-id="66b29-132">Wenn der numerische Wert der Versions Zeichenfolge nicht größer oder gleich 9 ist (d. h., dass der Benutzer nicht über eine Windows Media Player 9-Serie oder höher auf seinem Computer installiert ist), der Skriptcode ändert den **uiMode** -Wert des Player-Steuer Elements in "Full", legt eine neue Breite und Höhe für das Steuerelement fest und öffnet dann die. ASX-Datei im eingebetteten Player, indem ein Wert für die **URL** -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="66b29-132">If the numerical value of the version string is not greater than or equal to 9 (meaning that the user does not have Windows Media Player 9 Series or later installed on his or her computer), the script code changes the **uiMode** of the Player control to "full", sets a new width and height for the control, and then opens the .asx file in the embedded Player by specifying a value for the **URL** property.</span></span> <span data-ttu-id="66b29-133">In diesem Fall wird der Inhalt digitaler Medien auf der Webseite abgespielt, aber alle in der. ASX-Datei angegebenen HtmlView-Werte werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="66b29-133">When this happens, the digital media content plays in the webpage, but any HTMLView values specified in the .asx file are ignored.</span></span>

<span data-ttu-id="66b29-134">Die Art und Weise, wie Inhalte wiedergegeben werden, wenn der Benutzer keine Windows Media Player 9-Serie oder Windows Media Player 10 installiert hat.</span><span class="sxs-lookup"><span data-stu-id="66b29-134">How content is played back when the user does not have Windows Media Player 9 Series or Windows Media Player 10 installed is up to you.</span></span> <span data-ttu-id="66b29-135">Im vorangehenden Beispiel wird gezeigt, wie angegeben wird, dass der Inhalt auf der Webseite statt im vollmodusplayer abgespielt wird, wobei jeder HtmlView-Inhalt im Prozess ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="66b29-135">The preceding example shows how to specify that the content play in the webpage instead of the full-mode Player, ignoring any HTMLView content in the process.</span></span> <span data-ttu-id="66b29-136">Es gibt noch andere Ansätze, die Sie ergreifen können.</span><span class="sxs-lookup"><span data-stu-id="66b29-136">There are other approaches you might take.</span></span> <span data-ttu-id="66b29-137">Beispielsweise können Sie den Benutzer auffordern, eine neuere Version von Windows Media Player zu installieren, sodass diese Version des Players für die Wiedergabe digitaler Medieninhalte erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="66b29-137">For example, you could prompt the user to install a newer version of Windows Media Player, making that version of the Player a requirement for playing back your digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66b29-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="66b29-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66b29-139">**Anzeigen von Webseiten in Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="66b29-139">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="66b29-140">**Player. uiMode**</span><span class="sxs-lookup"><span data-stu-id="66b29-140">**Player.uiMode**</span></span>](player-uimode.md)
</dt> <dt>

[<span data-ttu-id="66b29-141">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="66b29-141">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 




