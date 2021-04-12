---
title: Erstellen von Metafile-Wiedergabelisten
description: Erstellen von Metafile-Wiedergabelisten
ms.assetid: 0afe3aaa-bcd1-4060-8772-add50f3b6bac
keywords:
- Windows Media Metadatei-Wiedergabelisten, erstellen
- Wiedergabelisten, erstellen
- Metadatei-Wiedergabelisten, erstellen
- Erstellen von Windows Media-Metadatei-Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d4acff6452640c3f0b66219b765a931033b9f3a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207111"
---
# <a name="creating-metafile-playlists"></a><span data-ttu-id="c0ab3-107">Erstellen von Metafile-Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="c0ab3-107">Creating Metafile Playlists</span></span>

<span data-ttu-id="c0ab3-108">Sie können eine Wiedergabeliste mit einem beliebigen Text-Editor erstellen, z. b. Microsoft Notepad.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-108">You can create a playlist using any text editor, such as Microsoft Notepad.</span></span> <span data-ttu-id="c0ab3-109">Öffnen Sie den Text-Editor.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-109">Open your text editor.</span></span> <span data-ttu-id="c0ab3-110">Geben Sie die Skript Einträge ein, die Sie implementieren möchten.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-110">Type the script entries you want to implement.</span></span> <span data-ttu-id="c0ab3-111">Nachdem Sie die Eingabe in Notepad abgeschlossen haben, speichern Sie die Datei mit einem entsprechenden Dateinamen und einer Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-111">After you have finished typing into Notepad, save the file with an appropriate file name and file name extension.</span></span> <span data-ttu-id="c0ab3-112">Weitere Informationen zu Erweiterungen finden Sie unter [Richtlinien für metadateierweiterungen](metafile-extension-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="c0ab3-112">For more information about extensions, see [Metafile Extension Guidelines](metafile-extension-guidelines.md).</span></span> <span data-ttu-id="c0ab3-113">In der Regel ist der Dateiname der Name der Windows Media-Datei oder des Streams, gefolgt von der Erweiterung. Wax,. wvx oder. ASX.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-113">Typically the file name is the name of the Windows Media file or stream followed by an extension of .wax, .wvx, or .asx.</span></span> <span data-ttu-id="c0ab3-114">Wenn Ihr Medieninhalt z. b. eine Windows Media-Audiodatei mit der Erweiterung. WMA ist, verwenden Sie die Erweiterung. Wax, wenn Sie die Wiedergabeliste benennen.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-114">For example, if your media content is a Windows Media audio file that has a .wma extension, use the .wax extension when naming the playlist.</span></span> <span data-ttu-id="c0ab3-115">Wiedergabelisten dürfen keine Formatierungscodes eines Textprozessors enthalten, wie z. b. Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-115">Playlists must not include any formatting codes from a word processor, such as Microsoft Word.</span></span> <span data-ttu-id="c0ab3-116">Speichern Sie die Datei als nur-Text-oder ASCII-Datei, um sicherzustellen, dass keine Formatierungscodes in der Wiedergabeliste enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-116">To be sure no formatting codes are included in the playlist, save the file as a plain text or ASCII file.</span></span>

> [!Note]  
> <span data-ttu-id="c0ab3-117">Bei Elementen und Attributen wird Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="c0ab3-117">Elements and attributes are not case sensitive.</span></span> <span data-ttu-id="c0ab3-118">Der Text, der in der Wiedergabeliste zum Definieren eines Elements oder Attributs verwendet wird, kann entweder groß-oder Kleinbuchstaben oder eine Kombination aus beidem sein.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-118">The text used in the playlist to define an element or attribute can be either uppercase or lowercase, or a mixture of both.</span></span>

 

<span data-ttu-id="c0ab3-119">Wenn ein Element über keine untergeordneten Elemente verfügt (solche, die sich in einem anderen Element ändern oder befinden), kann ein einzelner Schrägstrich (/) am Ende des öffnenden Tags direkt vor dem ">" anstelle eines Endtags verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-119">If an element does not have any child elements (those that modify or are contained within another element), a single slash character (/) can be used at the end of the opening tag, just before the '>', in place of a closing tag.</span></span> <span data-ttu-id="c0ab3-120">Untergeordnete Elemente eines Elements müssen zwischen dem öffnenden und dem schließenden Tag für dieses Element angezeigt werden. Andernfalls sind Sie keine untergeordneten Elemente für dieses Element und werden ignoriert, oder es wird ein Fehler in der Syntax der Wiedergabeliste verursacht.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-120">Child elements of an element must appear between the opening and closing tag for that element; otherwise they are not child elements for that element, and are ignored or cause an error in the syntax of the playlist.</span></span>

<span data-ttu-id="c0ab3-121">Die ersten vier Zeichen einer Wiedergabeliste müssen " &lt; ASX" lauten.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-121">The first four characters of a playlist must be "&lt;ASX".</span></span> <span data-ttu-id="c0ab3-122">Das Element " **ASX** " wird in allen Wiedergabelisten verwendet, unabhängig davon, ob die Erweiterung. Wax,. wvx oder. ASX ist.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-122">The **ASX** element is used in all playlists whether their extension is .wax, .wvx, or .asx.</span></span> <span data-ttu-id="c0ab3-123">Es darf nur ein **ASX** -Element pro Wiedergabeliste vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-123">There must be only one **ASX** element per playlist.</span></span> <span data-ttu-id="c0ab3-124">Dieses Element identifiziert die Datei als Windows Media-Metadatei-Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-124">This element identifies the file as a Windows Media metafile playlist.</span></span> <span data-ttu-id="c0ab3-125">Der Typ der Wiedergabeliste wird nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-125">It does not specify the type of playlist.</span></span>

<span data-ttu-id="c0ab3-126">Das Element " **ASX** " hat drei mögliche Attribute:</span><span class="sxs-lookup"><span data-stu-id="c0ab3-126">The **ASX** element has three possible attributes:</span></span>

<span data-ttu-id="c0ab3-127">**VERSION**</span><span class="sxs-lookup"><span data-stu-id="c0ab3-127">**VERSION**</span></span>

<span data-ttu-id="c0ab3-128">Das **Versions** Attribut ist erforderlich und muss unmittelbar hinter dem Element " **ASX** " folgen, z. b. "<-Version =" 3,0 " &gt; ".</span><span class="sxs-lookup"><span data-stu-id="c0ab3-128">The **VERSION** attribute is required and must follow immediately after the **ASX** element, for example "<ASX version = "3.0"&gt;".</span></span> <span data-ttu-id="c0ab3-129">Die aktuelle Versionsnummer ist 3,0.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-129">The current version number is 3.0.</span></span> <span data-ttu-id="c0ab3-130">Windows Media Player unterstützt alle vorherigen Versionen.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-130">Windows Media Player supports all previous versions.</span></span> <span data-ttu-id="c0ab3-131">Zulässige Werte für das **Versions** Attribut sind 3,0 und 3 (ohne Dezimaltrennzeichen).</span><span class="sxs-lookup"><span data-stu-id="c0ab3-131">Acceptable values for the **VERSION** attribute include both 3.0 and 3 (with no decimal point).</span></span>

<span data-ttu-id="c0ab3-132">**PREVIEWMODE**</span><span class="sxs-lookup"><span data-stu-id="c0ab3-132">**PREVIEWMODE**</span></span>

<span data-ttu-id="c0ab3-133">Das **PreviewMode** -Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-133">The **PREVIEWMODE** attribute is optional.</span></span> <span data-ttu-id="c0ab3-134">Es bietet einen weiteren Mechanismus zum angeben, wie lange ein Clip dargestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-134">It provides another mechanism for specifying how long to render a clip.</span></span> <span data-ttu-id="c0ab3-135">Wenn der Wert des **PreviewMode** -Attributs auf "yes" festgelegt ist, renderMedia Player jedes Clip für die Dauer, die durch das Element " **previewduration**" angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-135">If the value of the **PREVIEWMODE** attribute is YES, Windows Media Player will render each clip for the duration specified by the element **PREVIEWDURATION**.</span></span> <span data-ttu-id="c0ab3-136">Für jeden Clip kann eine **previewduration** angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-136">Each clip can have a **PREVIEWDURATION** specified.</span></span>

<span data-ttu-id="c0ab3-137">**Bannerbar**</span><span class="sxs-lookup"><span data-stu-id="c0ab3-137">**BANNERBAR**</span></span>

<span data-ttu-id="c0ab3-138">Das optionale **bannerbar** -Attribut definiert, ob das Windows Media Player-Steuerelement Platz für eine Banner Grafik reserviert.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-138">The optional **BANNERBAR** attribute defines whether the Windows Media Player control reserves space for a banner graphic.</span></span> <span data-ttu-id="c0ab3-139">(Verwenden Sie das **Banner** -Element, um die anzuzeigende Grafik anzugeben.) Wenn der Wert von " **bannerbar** " festgelegt ist, reserviert Windows Media Player Bannerbereich für die Anzeige und für jeden Clip, ob die Metadatei-Wiedergabeliste ein Banner für die Anzeige oder den Clip angibt.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-139">(Use the **BANNER** element to specify the graphic to display.) If the value of **BANNERBAR** is FIXED, Windows Media Player reserves banner space for the show and for every clip, whether the metafile playlist specifies a banner for the show or clip.</span></span> <span data-ttu-id="c0ab3-140">Dadurch wird die Größe des Fensters "Windows Media Player" unverändert gehalten (es sei denn, die Videogröße wird geändert), unabhängig davon, ob eine Banner Grafik vorhanden ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-140">This will keep the size of the Windows Media Player window the same (except when the video size changes) regardless of the absence or presence of a banner graphic.</span></span> <span data-ttu-id="c0ab3-141">Wenn dem anzeigen oder Clip kein Banner zugeordnet ist, ist der reservierte Speicherplatz schwarz.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-141">If the show or clip does not have a banner associated with it, the space reserved for one is black.</span></span> <span data-ttu-id="c0ab3-142">Wenn der Wert des **bannerbar** -Attributs "Auto" ist, reserviert Windows Media Player Platz für das Banner nur dann, wenn die Anzeige oder der Clip eine enthält.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-142">If the value of the **BANNERBAR** attribute is AUTO, Windows Media Player reserves space for the banner only when the show or clip includes one.</span></span>


```XML
<ASX version="3.0" BANNERBAR="AUTO" >

```



<span data-ttu-id="c0ab3-143">Weitere Informationen zu den drei Attributen des **-Elements für das-** Element finden Sie im Referenz Eintrag für das-Element von [ASX](asx-element.md).</span><span class="sxs-lookup"><span data-stu-id="c0ab3-143">For more information about the three attributes of the **ASX** element, see the reference entry for the [ASX Element](asx-element.md).</span></span>

<span data-ttu-id="c0ab3-144">Ein **ASX** -Element enthält untergeordnete **Eintrags** Elemente, die Informationen zu den Mediendateien definieren, auf die zugegriffen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-144">An **ASX** element contains **ENTRY** child elements that define information about the media files to be accessed.</span></span> <span data-ttu-id="c0ab3-145">Jedes **Entry** -Element muss ein **ref** -Element enthalten, das den Pfad zu der Mediendatei angibt, die gestreamt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-145">Each **ENTRY** element must contain a **REF** element that specifies the path to the media file to be streamed.</span></span> <span data-ttu-id="c0ab3-146">Es muss mindestens ein **Entry** -oder **ENTRYREF** -Element in einem **ASX** -Element vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-146">There must be at least one **ENTRY** or **ENTRYREF** element within an **ASX** element.</span></span>

<span data-ttu-id="c0ab3-147">Andere Elemente, die im Gültigkeitsbereich des **ASX** -Elements definiert sind, z. b. **Title** und **Author**, werden den von Windows Media Player angezeigten Metadaten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-147">Other elements defined within the scope of the **ASX** element, such as **TITLE** and **AUTHOR**, are associated with the metadata displayed by Windows Media Player.</span></span>

<span data-ttu-id="c0ab3-148">Die einfachsten Wiedergabelisten werden erstellt, indem einer Metadatei mehrere **Entry** -Elemente mit einem einzelnen **ref** -Element hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-148">The simplest playlists are created by adding multiple **ENTRY** elements with a single **REF** element to a metafile.</span></span> <span data-ttu-id="c0ab3-149">Jedes **Entry** -Element in einer Metadatei-Wiedergabeliste wird in der Reihenfolge gerendert, in der es in der Datei angezeigt wird, als ob der Benutzer den einzelnen Clip manuell</span><span class="sxs-lookup"><span data-stu-id="c0ab3-149">Each **ENTRY** element in a metafile playlist is rendered in the order it appears in the file as though the user had manually opened each clip.</span></span>

<span data-ttu-id="c0ab3-150">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="c0ab3-150">Example Code</span></span>


```XML
<ASX version = "3.0">
<!--A simple playlist with entries to be played in sequence.-->
    <Title>The Show Title</Title>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title1.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title2.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title3.wma" />
    </Entry>
</ASX>

```



<span data-ttu-id="c0ab3-151">Stellen Sie sicher, dass die Wiedergabeliste funktioniert, indem Sie in Windows-Explorer darauf doppelklicken.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-151">Be sure that the playlist is working by double-clicking it in Windows Explorer.</span></span> <span data-ttu-id="c0ab3-152">Windows Media Player sollte geöffnet werden und mit dem Streamen der Medieninhalte beginnen.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-152">Windows Media Player should open and start streaming the media content.</span></span> <span data-ttu-id="c0ab3-153">Nachdem Sie sich vergewissert haben, dass die Wiedergabeliste funktioniert, speichern Sie sie zusammen mit ihren Webseiten auf Ihrem Webserver, und verknüpfen Sie Sie über ein **href** -Element, oder Betten Sie Sie mithilfe des Windows-Media Player **Object** -Elements in eine Webseite ein.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-153">After you have confirmed that the playlist works, save it to your web server along with your webpages, and link to it by means of an **HREF** element, or embed it in a webpage using the Windows Media Player **OBJECT** element.</span></span>

<span data-ttu-id="c0ab3-154">Die folgenden Abschnitte enthalten weitere Informationen:</span><span class="sxs-lookup"><span data-stu-id="c0ab3-154">The following sections contain more information:</span></span>

-   [<span data-ttu-id="c0ab3-155">Schachteln von Metadateien</span><span class="sxs-lookup"><span data-stu-id="c0ab3-155">Nesting Metafiles</span></span>](nesting-metafiles.md)
-   [<span data-ttu-id="c0ab3-156">Verwenden von ASP-Seiten zum dynamischen Erstellen von Windows Media Metafile-Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="c0ab3-156">Using ASP Pages to Dynamically Create Windows Media Metafile Playlists</span></span>](using-asp-pages-to-dynamically-create-windows-media-metafile-playlists.md)

## <a name="related-topics"></a><span data-ttu-id="c0ab3-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c0ab3-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0ab3-158">**Banner-Element**</span><span class="sxs-lookup"><span data-stu-id="c0ab3-158">**BANNER Element**</span></span>](banner-element.md)
</dt> <dt>

[<span data-ttu-id="c0ab3-159">**Beispiel Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="c0ab3-159">**Example Playlists**</span></span>](example-playlists.md)
</dt> <dt>

[<span data-ttu-id="c0ab3-160">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="c0ab3-160">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="c0ab3-161">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="c0ab3-161">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




