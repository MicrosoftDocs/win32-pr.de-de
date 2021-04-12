---
title: Personalisieren der Medien Bereitstellung
description: Personalisieren der Medien Bereitstellung
ms.assetid: ffd62602-8bfc-4ca7-91fd-c610faa330cd
keywords:
- Windows Media Metadatei-Wiedergabelisten, Personalisieren der Medien Bereitstellung
- Wiedergabelisten, Personalisieren der Medien Übermittlung
- Metadatei-Wiedergabelisten, Personalisieren der Medien Übermittlung
- Windows Media Metadatei-Wiedergabelisten, Personalisierung von Medien Übermittlung
- Wiedergabelisten, Personalisierung von Medien Übermittlung
- Metadatei-Wiedergabelisten, Personalisierung von Medien Übermittlung
- Personalisierung der Medien Übermittlung
- Personalisieren der Medien Bereitstellung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ddb01364e2ea36214b94d01517f1d3d3b802ba63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206347"
---
# <a name="personalizing-media-delivery"></a><span data-ttu-id="9ae35-111">Personalisieren der Medien Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="9ae35-111">Personalizing Media Delivery</span></span>

<span data-ttu-id="9ae35-112">Anders als bei der unidirektionalen Kommunikation, bei der identische Inhalte an eine große Zielgruppe übermittelt werden, bietet Windows Media-Technologien Ihnen die Tools, mit denen Demographics zum Individualisieren von Sendungen</span><span class="sxs-lookup"><span data-stu-id="9ae35-112">Unlike one-way communication that broadcasts identical content to a mass audience, Windows Media Technologies provides you with the tools to use demographics to individualize broadcasts.</span></span> <span data-ttu-id="9ae35-113">Mit dem Internet ist die bidirektionale Kommunikation mit einer großen Skalierung sofort verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9ae35-113">With the Internet, two-way communication on a large scale is readily available.</span></span> <span data-ttu-id="9ae35-114">Dieser dynamische Informationsaustausch ermöglicht Inhaltsanbietern, Ihre Zielgruppe zu kennen und mit angepassten Präsentationen zu antworten.</span><span class="sxs-lookup"><span data-stu-id="9ae35-114">This dynamic interchange of information enables content providers to know their audience and respond with customized presentations.</span></span>

<span data-ttu-id="9ae35-115">Im folgenden Beispiel wird mithilfe eines fiktiven Unternehmens veranschaulicht, wie die Übermittlung von Streaminginhalten personalisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="9ae35-115">The following example, using a fictional company, illustrates how delivery of streaming content can be personalized.</span></span> <span data-ttu-id="9ae35-116">In dieser Erläuterung wird davon ausgegangen, dass Sie mit Active Server Seiten (ASP-oder ASP-Dateien) vertraut sind und Variablen definieren.</span><span class="sxs-lookup"><span data-stu-id="9ae35-116">This discussion assumes that you are familiar with Active Server Pages (ASP, or .asp files) and defining variables.</span></span>

<span data-ttu-id="9ae35-117">News Network ist eine fiktive Broadcast-News-Organisation, die den Betrieb erweitert hat, um eine Website einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="9ae35-117">News Network is a fictional broadcast news organization that has expanded its operations to include a website.</span></span> <span data-ttu-id="9ae35-118">Das Haupt Feature der Site ist ein Abschnitt, in dem Benutzer ihre eigenen personalisierten neuskoren erstellen können.</span><span class="sxs-lookup"><span data-stu-id="9ae35-118">The main feature of the site is a section where users can create their own personalized newscasts.</span></span> <span data-ttu-id="9ae35-119">Anstatt eine herkömmliche newscast anzuzeigen, die auf eine große Zielgruppe ausgerichtet ist, zeigt ein Benutzer ein umfassendes Nachrichtenprogramm an, das nur Themen mit persönlichem Interesse enthält.</span><span class="sxs-lookup"><span data-stu-id="9ae35-119">Instead of viewing a traditional newscast that is aimed at a mass audience, a user views a complete news program that contains only topics of personal interest.</span></span> <span data-ttu-id="9ae35-120">In der folgenden Sequenz wird eine typische Benutzer Darstellung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9ae35-120">The following sequence describes a typical user experience.</span></span>

1.  <span data-ttu-id="9ae35-121">Ein neuer Benutzer wechselt zur Website und klickt auf **Create Your Personal newscast**.</span><span class="sxs-lookup"><span data-stu-id="9ae35-121">A new user goes to the site, and clicks **Create Your Personal Newscast**.</span></span>
2.  <span data-ttu-id="9ae35-122">Ein bevorzugte Formular wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="9ae35-122">A preference form opens.</span></span> <span data-ttu-id="9ae35-123">In diesem Formular beantwortet der Benutzer Fragen zu persönlichen Vorlieben, wie z. b. bevorzugte News Storys, am wenigsten bevorzugte News Stories, Hobbys und eine übliche Methode zum empfangen täglicher Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="9ae35-123">On this form, the user answers questions regarding personal preferences, such as favorite news stories, least favorite news stories, hobbies, and usual method of receiving daily news.</span></span>
3.  <span data-ttu-id="9ae35-124">Der Benutzer sendet diese Informationen, und einige Sekunden später wird eine komplette, 15-minütige, persönliche newscast mit Programm Inhalt,-Übergängen und-Werbeeinblendungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ae35-124">The user sends this information, and a few seconds later views a complete, 15-minute, personal newscast containing program content, transitions, and commercials.</span></span> <span data-ttu-id="9ae35-125">Die Auswahl der einzelnen Medienelemente (einschließlich der Werbespots) basiert auf dem Benutzerprofil und wird automatisch mit den Komponenten der Windows Media-Technologien und den Tools für das Offline-Internet erreicht.</span><span class="sxs-lookup"><span data-stu-id="9ae35-125">Selection of each media element, including commercials, is based on the user profile, and is accomplished automatically with Windows Media Technologies components and off-the-shelf Internet tools.</span></span>

<span data-ttu-id="9ae35-126">In der folgenden Liste wird beschrieben, wie die verschiedenen Tools interagieren, um eine personalisierte newscast zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9ae35-126">The following list describes how the various tools interact to create a personalized newscast.</span></span>

1.  <span data-ttu-id="9ae35-127">Das bevorzugte Formular, das der Benutzer ausfüllt, ist eine Active Server Seite (ASP) ("Choices. asp").</span><span class="sxs-lookup"><span data-stu-id="9ae35-127">The preference form that the user fills out is an Active Server Page (ASP) (Choices.asp).</span></span> <span data-ttu-id="9ae35-128">Daten, die aus dem bevorzugten Formular abgerufen werden, werden von zwei Serverkomponenten analysiert.</span><span class="sxs-lookup"><span data-stu-id="9ae35-128">Data obtained from the preference form is analyzed by two server components.</span></span> <span data-ttu-id="9ae35-129">Eine Komponente verwendet die Informationen, um eine Microsoft SQL Server Datenbank von News Storys abzufragen.</span><span class="sxs-lookup"><span data-stu-id="9ae35-129">One component uses the information to query a Microsoft SQL Server database of news stories.</span></span> <span data-ttu-id="9ae35-130">Bei der anderen Komponente handelt es sich um einen Ad-Server, der einen komplexen Regelsatz verwendet, der auf vertraglichen Anforderungen und demografiken basiert, um die Werbeeinblendungen zu diesem Zeitpunkt zu planen.</span><span class="sxs-lookup"><span data-stu-id="9ae35-130">The other component is an ad server that uses a complex set of rules based on contractual requirements and demographics to schedule ads appropriate to the user at that time.</span></span>
2.  <span data-ttu-id="9ae35-131">Die beiden Datenbanken geben verschiedene Teile einer Wiedergabeliste zurück.</span><span class="sxs-lookup"><span data-stu-id="9ae35-131">The two databases return different portions of a playlist.</span></span> <span data-ttu-id="9ae35-132">Die News Story-Datenbank gibt eine Reihe entsprechender Story-Einträge zurück, und der Ad-Server gibt eine Reihe geeigneter kommerzieller Einträge zurück.</span><span class="sxs-lookup"><span data-stu-id="9ae35-132">The news story database returns a set of appropriate story Entries, and the ad server returns a set of appropriate commercial Entries.</span></span>
3.  <span data-ttu-id="9ae35-133">Eine zweite ASP-Seite (playshow. ASP) empfängt die Einträge aus der News Story-Datenbank und dem Ad-Server und kombiniert diese mit den standardmäßigen Show Open-, Close-und Transition-Einträgen.</span><span class="sxs-lookup"><span data-stu-id="9ae35-133">A second ASP page (PlayShow.asp) receives the Entries from the news story database and ad server, and combines those with standard show open, close, and transition Entries.</span></span> <span data-ttu-id="9ae35-134">Alle Einträge werden dann entsprechend der von playshow. ASP bereitgestellten Vorlage angeordnet, und die ASP-Seite gibt eine Wiedergabeliste an den Benutzer zurück.</span><span class="sxs-lookup"><span data-stu-id="9ae35-134">All Entries are then laid out according to the template provided by PlayShow.asp, and the ASP page returns a playlist to the user.</span></span>
4.  <span data-ttu-id="9ae35-135">Das eingebettete Windows Media Player-Steuerelement auf dem Computer des Benutzers spielt die Wiedergabeliste von Anfang bis Ende, und der Benutzer zeigt eine personalisierte newscast an.</span><span class="sxs-lookup"><span data-stu-id="9ae35-135">The embedded Windows Media Player control on the user's computer plays the playlist from beginning to end, and the user views a personalized newscast.</span></span>

<span data-ttu-id="9ae35-136">Das folgende Beispiel ist ein Teil einer Wiedergabelisten Datei, die ein Benutzer möglicherweise empfängt.</span><span class="sxs-lookup"><span data-stu-id="9ae35-136">The following example is a portion of a playlist file that a user might receive.</span></span> <span data-ttu-id="9ae35-137">Ad-Banner, moreingefo-Links und Abstracts wurden hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9ae35-137">Ad banners, MOREINFO links, and ABSTRACTS have been added to it.</span></span>


```XML
<ASX Version="3">
<TITLE>MyPersonalized NewsCast</TITLE>
<ENTRY ClientSkip="no">
    <!<entity type="mdash"/>- Commercial Element 1 -->
    <REF HREF="mms://proseware.com/Commercial.wma" />
    <BANNER HREF="https://www.proseware.com/images/MoreInfo.gif" >
        <MOREINFO HREF="https://www.proseware.com" target="_blank" />
    <ABSTRACT>Courtesy of Windows Media Technologies
    </ABSTRACT>
    </BANNER>
</ENTRY>
<ENTRY>
    <!<entity type="mdash"/>- Program Element 1 -->
    <TITLE>A Celebrity's Life</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/TheFile.wma" />
    <ABSTRACT>
     :: A celebrity looks back on her career after 40 years in public life.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004-- All Rights
         Reserved
    </COPYRIGHT>
</ENTRY>

<ENTRY>
    <!<entity type="mdash"/>Program Element 2 -->
    <TITLE>City council votes to build new bicycle path</TITLE>
    <COPYRIGHT>Copyright 2004</COPYRIGHT>
    <REF HREF="mms://proseware.com/SomePath/MyFile.wma" />
    <ABSTRACT>
        :: Some residents opposed changing the landscape in the public parks to accommodate bicycles.
    </ABSTRACT>
    <COPYRIGHT>Copyright 2004 -- All Rights Reserved
    </COPYRIGHT>
</ENTRY>
</ASX>

```



-   <span data-ttu-id="9ae35-138">Die in den Beispielen verwendeten Firmen, Organisationen, Produkte, Personen und Ereignisse sind frei erfunden, soweit nichts anderes angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="9ae35-138">The example companies, organizations, products, people and events depicted herein are fictitious.</span></span> <span data-ttu-id="9ae35-139">Jede Ähnlichkeit mit bestehenden Firmen, Organisationen, Produkten, Personen oder Ereignissen ist rein zufällig.</span><span class="sxs-lookup"><span data-stu-id="9ae35-139">No association with any real company, organization, product, person or event is intended or should be inferred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ae35-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9ae35-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ae35-141">**Erstellen von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="9ae35-141">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="9ae35-142">**Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="9ae35-142">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="9ae35-143">**Verwenden von Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="9ae35-143">**Using Metafile Playlists**</span></span>](using-metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="9ae35-144">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="9ae35-144">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="9ae35-145">**Leitfaden für Windows Media-Metadateien**</span><span class="sxs-lookup"><span data-stu-id="9ae35-145">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> </dl>

 

 




