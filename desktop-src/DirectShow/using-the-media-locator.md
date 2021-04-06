---
description: Verwenden des medienlocators
ms.assetid: 07840a37-7065-41e8-aee5-855c9f89fb77
title: Verwenden des medienlocators
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce934b06d92c0bec66d9260a485516d3acaf5a9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961099"
---
# <a name="using-the-media-locator"></a><span data-ttu-id="914aa-103">Verwenden des medienlocators</span><span class="sxs-lookup"><span data-stu-id="914aa-103">Using the Media Locator</span></span>

<span data-ttu-id="914aa-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="914aa-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="914aa-105">Der medienlocator ist ein Hilfsobjekt, das Dateinamen überprüft und nach fehlenden Dateien in lokalen Verzeichnissen oder Netzwerkverzeichnissen sucht.</span><span class="sxs-lookup"><span data-stu-id="914aa-105">The media locator is a helper object that verifies file names and searches for missing files on local or network directories.</span></span> <span data-ttu-id="914aa-106">Der Medien Detektor speichert einen Cache von Verzeichnis Pfaden, in denen er Dateien in früheren Such Vorgängen erfolgreich gefunden hat.</span><span class="sxs-lookup"><span data-stu-id="914aa-106">The media detector keeps a cache of directory paths where it has successfully found files in past searches.</span></span> <span data-ttu-id="914aa-107">Um eine Datei zu suchen, durchsucht Sie die Verzeichnisse im Cache.</span><span class="sxs-lookup"><span data-stu-id="914aa-107">To locate a file, it searches the directories in its cache.</span></span> <span data-ttu-id="914aa-108">Wenn ein Fehler auftritt, kann der Medien Detektor ein Dialogfeld "Datei öffnen" anzeigen, in dem der Benutzer eine Datei manuell finden kann.</span><span class="sxs-lookup"><span data-stu-id="914aa-108">Failing that, the media detector can display an Open File dialog for the user to locate a file manually.</span></span> <span data-ttu-id="914aa-109">Wenn der Benutzer die Datei eingibt, fügt der medienlocator das neue Verzeichnis dem Cache hinzu.</span><span class="sxs-lookup"><span data-stu-id="914aa-109">Assuming the user locates the file, the media locator adds the new directory to its cache.</span></span> <span data-ttu-id="914aa-110">Der medienlocator macht die [**imedialocator**](imedialocator.md) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="914aa-110">The media locator exposes the [**IMediaLocator**](imedialocator.md) interface.</span></span>

<span data-ttu-id="914aa-111">In der Regel erstellt Ihre Anwendung nicht direkt eine Instanz des medienlocators.</span><span class="sxs-lookup"><span data-stu-id="914aa-111">Typically, your application does not directly create an instance of the media locator.</span></span> <span data-ttu-id="914aa-112">Stattdessen stellen die Zeitachse und die Renderingengine die folgenden Methoden zum Validieren von Dateinamen mithilfe des Medien Detektors bereit.</span><span class="sxs-lookup"><span data-stu-id="914aa-112">Instead, the timeline and the render engine provide the following methods for validating file names using the media detector.</span></span>

-   <span data-ttu-id="914aa-113">Um Dateinamen in der Zeitachse zu validieren, nennen Sie [**iamtimeline:: validatesourcenames**](iamtimeline-validatesourcenames.md).</span><span class="sxs-lookup"><span data-stu-id="914aa-113">To validate file names in the timeline, call [**IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md).</span></span> <span data-ttu-id="914aa-114">Optional aktualisiert diese Methode auch die Quell Objekte mit den richtigen Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="914aa-114">Optionally, this method also updates the source objects with the correct file names.</span></span>
-   <span data-ttu-id="914aa-115">Zum Überprüfen von Dateinamen, wenn das Projekt gerendert wird, nennen Sie " [**irienderengine:: setsourcenamevalidation**](irenderengine-setsourcenamevalidation.md)".</span><span class="sxs-lookup"><span data-stu-id="914aa-115">To validate file names when the project is rendered, call [**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md).</span></span>

<span data-ttu-id="914aa-116">Beide Methoden verwenden Flags, die das Verhalten des medienlocators steuern.</span><span class="sxs-lookup"><span data-stu-id="914aa-116">Both methods take flags that control the behavior of the media locator.</span></span> <span data-ttu-id="914aa-117">Beispielsweise können Sie die Suche auf lokale Verzeichnisse beschränken.</span><span class="sxs-lookup"><span data-stu-id="914aa-117">For example, you can restrict the search to local directories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="914aa-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="914aa-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="914aa-119">Arbeiten mit Quellen</span><span class="sxs-lookup"><span data-stu-id="914aa-119">Working with Sources</span></span>](working-with-sources.md)
</dt> </dl>

 

 



