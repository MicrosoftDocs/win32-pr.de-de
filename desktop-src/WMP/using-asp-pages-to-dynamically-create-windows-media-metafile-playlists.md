---
title: Verwenden von ASP-Seiten zum dynamischen Erstellen von Windows Media Metafile-Wiedergabelisten
description: Verwenden von ASP-Seiten zum dynamischen Erstellen von Windows Media Metafile-Wiedergabelisten
ms.assetid: 9abf04a4-33b9-4502-aaf3-e40de06c7b41
keywords:
- Windows Media Metadatei-Wiedergabelisten, erstellen
- Metadatei-Wiedergabelisten, erstellen
- Wiedergabelisten, erstellen
- Windows Media Metadatei-Wiedergabelisten, dynamisches erstellen
- Metadatei-Wiedergabelisten, dynamisches erstellen
- Wiedergabelisten, dynamisches erstellen
- Windows Media Metadatei-Wiedergabelisten, ASP-Seiten
- Metadatei-Wiedergabelisten, ASP-Seiten
- Wiedergabelisten, ASP-Seiten
- Erstellen von Windows Media-Metadatei-Wiedergabelisten
- Dynamisches Erstellen von Windows Media-Metadatei-Wiedergabelisten
- ASP-Seiten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ea3cef88d86078aa95785163d7c2f4b0e57e975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515687"
---
# <a name="using-asp-pages-to-dynamically-create-windows-media-metafile-playlists"></a><span data-ttu-id="93db3-115">Verwenden von ASP-Seiten zum dynamischen Erstellen von Windows Media Metafile-Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="93db3-115">Using ASP Pages to Dynamically Create Windows Media Metafile Playlists</span></span>

<span data-ttu-id="93db3-116">Sie können Active Server Seiten (ASP oder ASP-Dateien) verwenden, um auf der Grundlage der von den Benutzern bereitgestellten Informationen dynamisch Wiedergabelisten zu generieren.</span><span class="sxs-lookup"><span data-stu-id="93db3-116">You can use Active Server Pages (ASP, or .asp files) to dynamically generate playlists based on information provided by users.</span></span> <span data-ttu-id="93db3-117">Eine ASP-Seite ist eine dynamische Webseite, die in Verbindung mit Microsoft Internetinformationsdienste (IIS) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="93db3-117">An ASP page is a dynamic webpage used in conjunction with Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="93db3-118">ASP ist eine Umgebung, in der Sie HTML, Skripts und wiederverwendbare ActiveX-Serverkomponenten kombinieren können, um dynamische und leistungsstarke webbasierte Geschäftslösungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="93db3-118">ASP is an environment in which you can combine HTML, scripts, and reusable ActiveX server components to create dynamic and powerful Web-based business solutions.</span></span> <span data-ttu-id="93db3-119">ASP Pages ermöglichen die serverseitige Skripterstellung für IIS mit nativer Unterstützung für Microsoft Visual Basic Scripting Edition (VBScript) und Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="93db3-119">ASP pages enable server-side scripting for IIS with native support for both Microsoft Visual Basic Scripting Edition (VBScript) and Microsoft JScript.</span></span> <span data-ttu-id="93db3-120">In dieser Erläuterung wird davon ausgegangen, dass Sie mit ASP vertraut sind und Variablen definieren.</span><span class="sxs-lookup"><span data-stu-id="93db3-120">This discussion assumes that you are familiar with ASP and defining variables.</span></span>

<span data-ttu-id="93db3-121">Alle Header Informationen müssen in der ersten Zeile der ASP-Seiten Zeichenfolge enthalten sein, die an Windows Media Player zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="93db3-121">All header information must be contained on the first line of the ASP page string returned to Windows Media Player.</span></span>

<span data-ttu-id="93db3-122">Wenn Sie ASP-Seiten zum Generieren Media Player von Wiedergabelisten verwenden, müssen Sie Werte für die **ContentType** -Eigenschaft des **Antwort** Objekts angeben und auf der ASP-Seite auf der ASP-Seite die Eigenschaften **ablaufen** .</span><span class="sxs-lookup"><span data-stu-id="93db3-122">When you use ASP pages to generate playlists, you must specify values for the **Response** object's **ContentType** and **expires** properties in the ASP page because of latency issues with Windows Media Player.</span></span> <span data-ttu-id="93db3-123">Der **Response. ContentType** -Wert muss eine gültige Dateinamenerweiterung für Windows Media-Metadateien sein.</span><span class="sxs-lookup"><span data-stu-id="93db3-123">The **Response.ContentType** value must be a valid file name extension for Windows Media metafiles.</span></span> <span data-ttu-id="93db3-124">Zulässige Werte sind WMA, Wax, WMV, WVX, ASF und ASX.</span><span class="sxs-lookup"><span data-stu-id="93db3-124">Acceptable values include wma, wax, wmv, wvx, asf, and asx.</span></span>

<span data-ttu-id="93db3-125">Die **Response. abgelaufen** -Eigenschaft gibt die Zeitdauer in Sekunden an, die der Windows-Media Player die Wiedergabelisten Datei zwischenspeichert.</span><span class="sxs-lookup"><span data-stu-id="93db3-125">The **Response.expires** property specifies the length of time, in seconds, that Windows Media Player caches the playlist file.</span></span> <span data-ttu-id="93db3-126">Wenn Sie einen Wert von NULL angeben, wird in Windows Media Player jedes Mal, wenn der Benutzer die Seite aktualisiert, eine neue Wiedergabeliste vom Server angefordert.</span><span class="sxs-lookup"><span data-stu-id="93db3-126">Specifying a value of zero results in Windows Media Player requesting a new playlist from the server each time the user refreshes the page.</span></span>

<span data-ttu-id="93db3-127">Ausführliche Informationen zur Verwendung des **Antwort** Objekts auf Active Server Seiten finden Sie im Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="93db3-127">See the Platform SDK for details about using the **Response** object in Active Server Pages.</span></span>

<span data-ttu-id="93db3-128">Der folgende Code ist ein Beispiel für eine ASP-Seite, die verwendet wird, um eine Windows Media Metadatei-Wiedergabeliste zu generieren.</span><span class="sxs-lookup"><span data-stu-id="93db3-128">The following code is an example of an ASP page used to generate a Windows Media metafile playlist.</span></span>


```XML
<%Response.ContentType = "video/x-ms-wma"%><%Response.expires=0 %>
<ASX VERSION="3.0">
    <TITLE>Your title here</TITLE>
    <ENTRY>
        <REF HREF ="mms://adventure-works.com/pubpt/filename.wma" />
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a><span data-ttu-id="93db3-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="93db3-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93db3-130">**Erstellen von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="93db3-130">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> </dl>

 

 




