---
description: Die Microsoft Windows Journal Note Reader-Komponente ermöglicht programmgesteuerten Lesezugriff auf Dateien im Journal Format.
ms.assetid: 85dcda59-2972-48e3-a9f5-5cce0b60a1f1
title: Verwenden der Journal Reader-Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48fd098db4ce1c0c92a5ded76b0950e264aa2a73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958897"
---
# <a name="using-the-journal-reader-component"></a><span data-ttu-id="78cd0-103">Verwenden der Journal Reader-Komponente</span><span class="sxs-lookup"><span data-stu-id="78cd0-103">Using the Journal Reader Component</span></span>

<span data-ttu-id="78cd0-104">Die Microsoft Windows Journal Note Reader-Komponente ermöglicht programmgesteuerten Lesezugriff auf Dateien im Journal Format.</span><span class="sxs-lookup"><span data-stu-id="78cd0-104">The Microsoft Windows Journal Note Reader component provides programmatic read access to files in the Journal format.</span></span>

## <a name="component-overview"></a><span data-ttu-id="78cd0-105">Übersicht über Komponenten</span><span class="sxs-lookup"><span data-stu-id="78cd0-105">Component Overview</span></span>

<span data-ttu-id="78cd0-106">Journal Dateien haben die Dateierweiterung. jnt.</span><span class="sxs-lookup"><span data-stu-id="78cd0-106">Journal files have the .jnt file extension.</span></span> <span data-ttu-id="78cd0-107">Diese einfache Komponente übernimmt einen Stream, der eine JNT-Datei enthält, und gibt einen Stream zurück, der den Inhalt der Datei im XML-Format enthält.</span><span class="sxs-lookup"><span data-stu-id="78cd0-107">This simple component takes a stream containing a .jnt file and returns a stream containing the file's content in XML format.</span></span> <span data-ttu-id="78cd0-108">Der von der Komponente zurückgegebene XML-Code entspricht dem Journal Note Reader-Schema.</span><span class="sxs-lookup"><span data-stu-id="78cd0-108">The XML returned by the component conforms to the Journal Note Reader schema.</span></span> <span data-ttu-id="78cd0-109">Dieses Schema ist in der [Journal Reader-Schema Referenz](journal-reader-schema-reference.md)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="78cd0-109">This schema is documented in [Journal Reader Schema Reference](journal-reader-schema-reference.md).</span></span>

<span data-ttu-id="78cd0-110">Die-Komponente bietet keine Möglichkeit, JNT-Dateien zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="78cd0-110">The component does not provide the ability to write out .jnt files.</span></span>

<span data-ttu-id="78cd0-111">Die Komponente ist in nicht verwalteten und verwalteten Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="78cd0-111">The component is available in unmanaged and managed versions.</span></span> <span data-ttu-id="78cd0-112">Die nicht verwaltete Komponente ist in der journal.dll Dynamic Link Library (dll) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="78cd0-112">The unmanaged component is available in the journal.dll dynamic link library (DLL).</span></span> <span data-ttu-id="78cd0-113">Die verwaltete Version befindet sich entweder in der Microsoft.Ink.Journal.dll-Assembly (für die Weiterverteilung an Windows XP Tablet PC Edition oder Windows Vista) oder Microsoft.Ink.dll.</span><span class="sxs-lookup"><span data-stu-id="78cd0-113">The managed version is either in the Microsoft.Ink.Journal.dll assembly (for redistribution to Windows XP Tablet PC Edition or Windows Vista), or Microsoft.Ink.dll.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="78cd0-114">Ab Windows 10, Version 1607, ist journal.dll nicht im Windows-Betriebssystem enthalten.</span><span class="sxs-lookup"><span data-stu-id="78cd0-114">Beginning with Windows 10, version 1607, journal.dll is not included in the Windows operating system.</span></span> <span data-ttu-id="78cd0-115">Diese Bibliothek sollte als veraltet oder veraltet betrachtet werden und sollte nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78cd0-115">That library should be considered deprecated or obsolete and should not be used.</span></span>

 

### <a name="assembly-changes-of-note"></a><span data-ttu-id="78cd0-116">Assemblyänderungen von Hinweis</span><span class="sxs-lookup"><span data-stu-id="78cd0-116">Assembly Changes of Note</span></span>

<span data-ttu-id="78cd0-117">Es ist wichtig, dass Sie einige Änderungen an der Assembly kennen, die die Journal Notiz Reader-Komponente enthält, die zwischen der Version, die in Verbindung mit Version 1,7 des Tablet Developers Kit veröffentlicht wurde, und der Version, die im Windows Vista-Betriebssystem enthalten ist, aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="78cd0-117">It is important to be aware of some changes to the assembly containing the Journal Note Reader component that occurred between the version released in conjunction with version 1.7 of the Tablet Developers Kit and the version that ships in the Windows Vista operating system.</span></span>

<span data-ttu-id="78cd0-118">Die 1,7-Version der Reader-Komponente, die entweder an Windows XP oder Windows Vista weitergegeben werden kann, ist in einer Assembly mit dem Namen "Microsoft.Ink.Journal.dll" enthalten.</span><span class="sxs-lookup"><span data-stu-id="78cd0-118">The 1.7 version of the reader component, which can be redistributed to either Windows XP or Windows Vista, is contained in an assembly called Microsoft.Ink.Journal.dll.</span></span> <span data-ttu-id="78cd0-119">Die Reader-Komponente ist in Windows Vista enthalten, wurde jedoch in die Core Microsoft.Ink.dll-Assembly integriert.</span><span class="sxs-lookup"><span data-stu-id="78cd0-119">The reader component ships in Windows Vista, but has been integrated into the core Microsoft.Ink.dll assembly.</span></span> <span data-ttu-id="78cd0-120">Dies bedeutet, dass Anwendungen, die die 1,7-Assembly verwenden, diese Assembly mit Ihrem Setup neu verteilen müssen.</span><span class="sxs-lookup"><span data-stu-id="78cd0-120">This means that applications that make use of the 1.7 assembly need to redistribute that assembly with their setup.</span></span>

## <a name="using-the-component"></a><span data-ttu-id="78cd0-121">Verwenden der Komponente</span><span class="sxs-lookup"><span data-stu-id="78cd0-121">Using the Component</span></span>

<span data-ttu-id="78cd0-122">Die Reader-Komponente für Journal Hinweise ist hilfreich zum Extrahieren der frei Hand Daten und anderer Informationen über die Datei aus einer Journal Datei.</span><span class="sxs-lookup"><span data-stu-id="78cd0-122">The Journal Note Reader component is useful for extracting the ink data and other information about the file from a Journal file.</span></span>

### <a name="com"></a><span data-ttu-id="78cd0-123">COM</span><span class="sxs-lookup"><span data-stu-id="78cd0-123">COM</span></span>

<span data-ttu-id="78cd0-124">Die COM-Komponente "Journal Notiz Reader" befindet sich in der Datei Journal.dll, die beim Herunterladen und Ausführen der Installationsdatei für Journal Notiz Reader installiert und registriert wird.</span><span class="sxs-lookup"><span data-stu-id="78cd0-124">The Journal Note Reader COM component is in the file Journal.dll, which is installed and registered when you download and run the Journal Note Reader installation file.</span></span>

<span data-ttu-id="78cd0-125">Die [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle wird von der COM-Komponente nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="78cd0-125">The COM component does not support the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span>

### <a name="managed"></a><span data-ttu-id="78cd0-126">Verwaltet</span><span class="sxs-lookup"><span data-stu-id="78cd0-126">Managed</span></span>

<span data-ttu-id="78cd0-127">Die verwaltete Komponente "Journal Notiz Reader" befindet sich in der Microsoft.Ink.JournalReader.dll-Assembly.</span><span class="sxs-lookup"><span data-stu-id="78cd0-127">The Journal Note Reader managed component is in the Microsoft.Ink.JournalReader.dll assembly.</span></span> <span data-ttu-id="78cd0-128">Diese Assembly wird im globalen Assemblycache installiert und registriert, wenn Sie die Installationsdatei des Journal Notiz Readers ausführen.</span><span class="sxs-lookup"><span data-stu-id="78cd0-128">This assembly is installed and registered in the global assembly cache when you run the Journal Note Reader installation file.</span></span>

<span data-ttu-id="78cd0-129">Fügen Sie einen Verweis auf die Assembly hinzu, um Sie in Ihrem verwalteten Projekt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="78cd0-129">Add a reference to the assembly to use it in your managed project.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78cd0-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="78cd0-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78cd0-131">**Ijournalreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="78cd0-131">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> <dt>

[<span data-ttu-id="78cd0-132">Schema Referenz für Journal Reader</span><span class="sxs-lookup"><span data-stu-id="78cd0-132">Journal Reader Schema Reference</span></span>](journal-reader-schema-reference.md)
</dt> </dl>

 

 
