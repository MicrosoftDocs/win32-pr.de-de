---
title: Informationen zu Sami-Dateien
description: Informationen zu Sami-Dateien
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
keywords:
- Windows Media Player, synchronisierter zugänglicher Medienaustausch (Sami)
- Windows Media Player-Objektmodell, synchronisierter zugänglicher Medienaustausch (Sami)
- Objektmodell, synchronisierter, zugänglicher Medienaustausch (Sami)
- Windows Media Player Mobile, synchronisierter verfügbarer Medienaustausch (Sami)
- Windows Media Player ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- Windows Media Player Mobile ActiveX-Steuerelement, synchronisierter barrierefreier Medienaustausch (Sami)
- ActiveX-Steuerelement, synchronisierter, zugänglicher Medienaustausch (Sami)
- Synchronisierter, barrierefreier Medienaustausch (Sami), Dateien
- Samisch (synchronisierter, zugänglicher Medienaustausch), Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d310ab3eb3016937f148ebb26e810dd9e6e6b6b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856267"
---
# <a name="about-sami-files"></a><span data-ttu-id="e32ed-112">Informationen zu Sami-Dateien</span><span class="sxs-lookup"><span data-stu-id="e32ed-112">About SAMI Files</span></span>

<span data-ttu-id="e32ed-113">Sami-Dateien sind Textdateien, die eine SMI-oder Sami-Dateinamenerweiterung haben.</span><span class="sxs-lookup"><span data-stu-id="e32ed-113">SAMI files are text files that have an .smi or .sami file name extension.</span></span> <span data-ttu-id="e32ed-114">Sie enthalten die Text Zeichenfolgen, die für synchronisierte Untertitel, Untertitel und Audiobeschreibungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e32ed-114">They contain the text strings used for synchronized closed captions, subtitles, and audio descriptions.</span></span> <span data-ttu-id="e32ed-115">Außerdem geben Sie die Zeit Steuerungsparameter an, die vom Windows Media Player-Steuerelement verwendet werden, um den Text der geschlossenen Überschrift mit Audioinhalten oder Videoinhalten</span><span class="sxs-lookup"><span data-stu-id="e32ed-115">They also specify the timing parameters used by the Windows Media Player control to synchronize closed caption text with audio or video content.</span></span> <span data-ttu-id="e32ed-116">Wenn eine digitale Mediendatei eine in der Sami-Datei festgelegte Zeit erreicht, ändert sich der Text entsprechend im Anzeigebereich der geschlossenen Beschriftung der Webseite.</span><span class="sxs-lookup"><span data-stu-id="e32ed-116">When a digital media file reaches a time designated in the SAMI file, the text changes accordingly in the closed caption display area of the webpage.</span></span>

<span data-ttu-id="e32ed-117">Anders als bei einem einfachen Text-Editor (z. b. Microsoft Notepad) ist keine spezielle Software erforderlich, um eine Sami-Datei zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e32ed-117">Other than a simple text editor (such as Microsoft Notepad), special software is not required to create a SAMI file.</span></span> <span data-ttu-id="e32ed-118">In Sami und HTML sind gemeinsame Elemente wie die <HEAD> Tags und gemeinsam <BODY> .</span><span class="sxs-lookup"><span data-stu-id="e32ed-118">SAMI and HTML share common elements, such as the <HEAD> and <BODY> tags.</span></span> <span data-ttu-id="e32ed-119">Wie in HTML müssen in Sami-Dateien verwendete Tags immer paarweise verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e32ed-119">As in HTML, tags used in SAMI files must always be used in pairs.</span></span> <span data-ttu-id="e32ed-120">Ein Body-Element beginnt z. b. mit einem <BODY> -Tag und muss immer mit einem-Tag enden </BODY> .</span><span class="sxs-lookup"><span data-stu-id="e32ed-120">For example, a BODY element begins with a <BODY> tag and must always end with a </BODY> tag.</span></span>

<span data-ttu-id="e32ed-121">Eine grundlegende Sami-Datei erfordert drei grundlegende Tags: <SAMI> , <HEAD> und <BODY> .</span><span class="sxs-lookup"><span data-stu-id="e32ed-121">A basic SAMI file requires three fundamental tags: <SAMI>, <HEAD>, and <BODY>.</span></span>

<span data-ttu-id="e32ed-122">Das- <SAMI> Tag identifiziert das Dokument als Sami-Dokument, sodass andere Anwendungen sein Dateiformat erkennen können.</span><span class="sxs-lookup"><span data-stu-id="e32ed-122">The <SAMI> tag identifies the document as a SAMI document so other applications can recognize its file format.</span></span>

<span data-ttu-id="e32ed-123">Zwischen den Tags <HEAD> und </HEAD> definieren Sie grundlegende Richtlinien und andere Formatinformationen für das Sami-Dokument, z. b. den Dokumenttitel, allgemeine Informationen und Stileigenschaften für Untertitel.</span><span class="sxs-lookup"><span data-stu-id="e32ed-123">Between the <HEAD> and </HEAD> tags, you define basic guidelines and other format information for the SAMI document, such as the document title, general information, and style properties for closed captions.</span></span> <span data-ttu-id="e32ed-124">Wie bei HTML wird der innerhalb des Head-Elements deklarierte Inhalt nicht als Ausgabe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e32ed-124">Like HTML, content declared within the HEAD element does not display as output.</span></span>

<span data-ttu-id="e32ed-125">Elemente und Attribute, die zwischen den Tags <BODY> und </BODY> definiert sind, zeigen Inhalt an, der vom Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e32ed-125">Elements and attributes defined between the <BODY> and </BODY> tags display content seen by the user.</span></span> <span data-ttu-id="e32ed-126">In Sami enthält das Body-Element die Parameter für die Synchronisierung und die Text Zeichenfolgen, die für Untertitel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e32ed-126">In SAMI, the BODY element contains the parameters for synchronization and the text strings used for closed captions.</span></span>

<span data-ttu-id="e32ed-127">Das Style-Element, das im Head-Element definiert ist, bietet zusätzliche Funktionen in Sami.</span><span class="sxs-lookup"><span data-stu-id="e32ed-127">Defined within the HEAD element, the STYLE element provides for added functionality in SAMI.</span></span> <span data-ttu-id="e32ed-128">Zwischen den Tags und können Sie mehrere Cascading Stylesheet (CSS) <STYLE> - </STYLE> Selektoren für Stil und Layout definieren.</span><span class="sxs-lookup"><span data-stu-id="e32ed-128">Between the <STYLE> and </STYLE> tags, you can define several Cascading Style Sheet (CSS) selectors for style and layout.</span></span> <span data-ttu-id="e32ed-129">Stileigenschaften wie Schriftarten, Größen und Ausrichtungen können angepasst werden, um eine umfangreiche Benutzerfreundlichkeit bereitzustellen und gleichzeitig Barrierefreiheit zu fördern.</span><span class="sxs-lookup"><span data-stu-id="e32ed-129">Style properties such as fonts, sizes, and alignments can be customized to provide a rich user experience while also promoting accessibility.</span></span> <span data-ttu-id="e32ed-130">Wenn Sie z. b. eine große Textschrift Klasse definieren, kann die Lesbarkeit für Benutzer verbessert werden, die Probleme beim Lesen von geringem Text haben.</span><span class="sxs-lookup"><span data-stu-id="e32ed-130">For example, defining a large text font style class can improve the readability for users who have difficulty reading small text.</span></span> <span data-ttu-id="e32ed-131">Darüber hinaus können Sie durch die Definition verschiedener Sprachklassen den digitalen Medieninhalt besser verstehen.</span><span class="sxs-lookup"><span data-stu-id="e32ed-131">In addition, by defining several different language classes, you can help international users better understand the digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e32ed-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e32ed-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e32ed-133">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="e32ed-133">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




