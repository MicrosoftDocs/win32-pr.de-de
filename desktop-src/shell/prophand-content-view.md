---
description: In diesem Thema wird eine neue Ansicht in Windows Explorer beschrieben, die als Inhaltsansicht bezeichnet wird, in der der relevanteste Inhalt für jedes Element angezeigt wird.
title: Inhaltsansicht nach Dateityp oder-Art
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E01A6726-14C4-4c00-81D4-AE1008088678
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 81982d2242a7ea466c10e7d0ee37d899eea3e687
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757362"
---
# <a name="content-view-by-file-type-or-kind"></a><span data-ttu-id="51abf-103">Inhaltsansicht nach Dateityp oder-Art</span><span class="sxs-lookup"><span data-stu-id="51abf-103">Content View By File Type or Kind</span></span>

<span data-ttu-id="51abf-104">In diesem Thema wird eine neue Ansicht in Windows Explorer beschrieben, die als Inhaltsansicht bezeichnet wird, in der der relevanteste Inhalt für jedes Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="51abf-104">This topic describes a new view in Windows Explorer, called the Content view, that displays the most relevant content for each item.</span></span> <span data-ttu-id="51abf-105">Mithilfe eines Satzes von Registrierungs Schlüsseln können Elemente eine Eigenschaften Liste und ein Layout definieren, die von der Shell für die Inhaltsansicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51abf-105">Using a set of registry keys, items can define a property list and a layout that the Shell uses for Content view.</span></span> <span data-ttu-id="51abf-106">Die Shell Ruft die Registrierungsschlüssel mithilfe des Zuordnungs [Arrays](fa-perceivedtypes.md)des Elements ab.</span><span class="sxs-lookup"><span data-stu-id="51abf-106">The Shell retrieves the registry keys by using the item's [association array](fa-perceivedtypes.md).</span></span>

## <a name="how-does-the-content-view-work"></a><span data-ttu-id="51abf-107">Wie funktioniert die Inhaltsansicht?</span><span class="sxs-lookup"><span data-stu-id="51abf-107">How Does the Content View Work?</span></span>

<span data-ttu-id="51abf-108">In Windows 7 und höher wird in der Inhaltsansicht eine Logik zur Größenänderung verwendet, die Eigenschaften löscht, wenn die Fenstergröße abnimmt, um sicherzustellen, dass die kritischsten Eigenschaften weiterhin Platz aufweisen, um eindeutig lesbar zu sein.</span><span class="sxs-lookup"><span data-stu-id="51abf-108">In Windows 7 and later, the Content view uses a resizing logic that drops properties when the window size decreases, to ensure that the most critical properties still have room to be clearly readable.</span></span> <span data-ttu-id="51abf-109">Der folgende Screenshot veranschaulicht die Inhaltsansicht von Suchergebnissen, die Musik, Bilder und Dokumente enthalten.</span><span class="sxs-lookup"><span data-stu-id="51abf-109">The following screen shot illustrates the Content view of search results containing music, pictures, and documents.</span></span>

![Inhaltsansicht von Suchergebnissen mit Musik, Bildern und Dokumenten](images/content-view/contentviewsearchresults.png)

<span data-ttu-id="51abf-111">Einige shelldatenquellen verwenden die Inhaltsansicht standardmäßig. Benutzer können jedoch die Inhaltsansicht auswählen, indem Sie im Windows-Explorer auf die Schaltfläche " **View Control** " klicken.</span><span class="sxs-lookup"><span data-stu-id="51abf-111">Some Shell data sources use Content view by default, but users can select the Content view by clicking the **View Control** button in Windows Explorer.</span></span> <span data-ttu-id="51abf-112">Eine shelldatenquelle erweitert den Shellnamespace und macht Elemente in einem Datenspeicher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="51abf-112">A Shell data source extends the Shell namespace and exposes items in a data store.</span></span> <span data-ttu-id="51abf-113">Die Elemente in einem Datenspeicher können vom Windows-Suchsystem mithilfe eines Protokoll Handlers indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="51abf-113">The items in a data store can be indexed by the Windows Search system using a protocol handler.</span></span>

## <a name="how-to-implement-the-content-view"></a><span data-ttu-id="51abf-114">Implementieren der Inhaltsansicht</span><span class="sxs-lookup"><span data-stu-id="51abf-114">How to Implement the Content View</span></span>

<span data-ttu-id="51abf-115">Wenn Sie einen neuen [Dateityp](fa-file-types.md) oder [Protokollhandler](../search/-search-3x-wds-extidx-prot-implementing.md)registrieren, können Sie die Inhaltsansicht nutzen, indem Sie einen der beiden unterschiedlichen Ansätze verwenden.</span><span class="sxs-lookup"><span data-stu-id="51abf-115">When registering a new [file type](fa-file-types.md) or [protocol handler](../search/-search-3x-wds-extidx-prot-implementing.md), you can take advantage of the Content view by using either of two different approaches.</span></span> <span data-ttu-id="51abf-116">Sie können einen vorhandenen Satz von Eigenschaften und layoutmustern verwenden, oder Sie können eine eigene Kombination erstellen.</span><span class="sxs-lookup"><span data-stu-id="51abf-116">You can use an existing set of properties and layout pattern, or you can create your own combination.</span></span>

<span data-ttu-id="51abf-117">Sie können einen Registrierungs Eintrag verwenden, um den Dateityp oder das Element einem [vordefinierten Typ](../properties/building-property-handlers-user-friendly-kind-names.md)zuzuordnen, bei dem es sich um eine Eigenschaft handelt, die Sie als Inhaltskategorie betrachten können.</span><span class="sxs-lookup"><span data-stu-id="51abf-117">You can use a registry entry to associate your file type or item with a predefined [Kind](../properties/building-property-handlers-user-friendly-kind-names.md), which is a property that you can think of as a content category.</span></span> <span data-ttu-id="51abf-118">Indem Sie den Dateityp oder das Element mit bestimmten dieser Art verknüpfen, erben Sie die Layoutmuster und Eigenschaften Listen der Inhaltsansicht dieser Art automatisch.</span><span class="sxs-lookup"><span data-stu-id="51abf-118">By associating your file type or item with certain of these Kinds, you automatically inherit that Kind's Content view layout patterns and property lists.</span></span> <span data-ttu-id="51abf-119">Windows definiert Layoutmuster und Eigenschaften Listen für die Inhaltsansicht für die folgenden Arten: Dokumente, e-Mail, Ordner, Musik, Bild und generisch.</span><span class="sxs-lookup"><span data-stu-id="51abf-119">Windows defines Content view layout patterns and property lists for the following Kinds: documents, email, folder, music, picture, and generic.</span></span> <span data-ttu-id="51abf-120">Diese Art von Zuordnung wird empfohlen.</span><span class="sxs-lookup"><span data-stu-id="51abf-120">This type of association is encouraged.</span></span> <span data-ttu-id="51abf-121">Damit können Sie die konsistente Benutzer Leistung bereitstellen, die ein Benutzer für ähnliche Elemente erwartet.</span><span class="sxs-lookup"><span data-stu-id="51abf-121">It lets you provide the consistent experience that a user expects for similar items.</span></span>

<span data-ttu-id="51abf-122">Weitere Informationen finden Sie unter [Dateitypen](fa-file-types.md) und [Kind-Namen](../properties/building-property-handlers-user-friendly-kind-names.md) und [Registrieren eines eindeutigen Inhalts Ansichts Satzes von Eigenschaften und layoutmustern für den Dateityp oder das Element](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).</span><span class="sxs-lookup"><span data-stu-id="51abf-122">For more information, see [File Types](fa-file-types.md) and [Kind Names](../properties/building-property-handlers-user-friendly-kind-names.md) and [How To Register a Unique Content View Set of Properties and Layout Pattern for the File Type or Item](register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51abf-123">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="51abf-123">Additional Resources</span></span>

-   <span data-ttu-id="51abf-124">Informationen zur Eigenschafts Referenz Dokumentation finden Sie unter [System. Kind](../properties/props-system-kind.md)und [System. kindtext](../properties/props-system-kindtext.md).</span><span class="sxs-lookup"><span data-stu-id="51abf-124">For property reference documentation, see [System.Kind](../properties/props-system-kind.md), and [System.KindText](../properties/props-system-kindtext.md).</span></span>
-   <span data-ttu-id="51abf-125">Eine Referenz Dokumentation zur proplist finden Sie unter [System. proplist. contentviewmodeforbrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)und [System. proplist. contentviewmodeforsearch](../properties/props-system-proplist-contentviewmodeforsearch.md).</span><span class="sxs-lookup"><span data-stu-id="51abf-125">For PropList reference documentation, see [System.PropList.ContentViewModeForBrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md), and [System.PropList.ContentViewModeForSearch](../properties/props-system-proplist-contentviewmodeforsearch.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="51abf-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="51abf-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51abf-127">Anwendungs Registrierung</span><span class="sxs-lookup"><span data-stu-id="51abf-127">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="51abf-128">Dateitypen</span><span class="sxs-lookup"><span data-stu-id="51abf-128">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="51abf-129">Funktionsweise von Dateizuordnungen</span><span class="sxs-lookup"><span data-stu-id="51abf-129">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="51abf-130">Dateityp Überprüfung</span><span class="sxs-lookup"><span data-stu-id="51abf-130">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="51abf-131">Dateityp Handler</span><span class="sxs-lookup"><span data-stu-id="51abf-131">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="51abf-132">Programmgesteuerte Bezeichner</span><span class="sxs-lookup"><span data-stu-id="51abf-132">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="51abf-133">Wahrgenommene Typen</span><span class="sxs-lookup"><span data-stu-id="51abf-133">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="51abf-134">Zuordnungs Arrays</span><span class="sxs-lookup"><span data-stu-id="51abf-134">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
