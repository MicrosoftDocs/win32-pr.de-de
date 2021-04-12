---
title: Strukturierter Speicher
description: Die strukturierte Speicherung bietet Datei-und Daten Persistenz in com, indem eine einzelne Datei als strukturierte Auflistung von Objekten behandelt wird, die als Speicher und Streams bezeichnet werden.
ms.assetid: 57a5f34d-c3db-47c5-9836-6e2163732d30
keywords:
- Strukturierter Speicherplatz-STG
- Strukturierter Speicherplatz Halter-STG, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606fef01d67cd78997f21dcd9008785d30985315
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315705"
---
# <a name="structured-storage"></a><span data-ttu-id="63cd3-105">Strukturierter Speicher</span><span class="sxs-lookup"><span data-stu-id="63cd3-105">Structured Storage</span></span>

## <a name="purpose"></a><span data-ttu-id="63cd3-106">Zweck</span><span class="sxs-lookup"><span data-stu-id="63cd3-106">Purpose</span></span>

<span data-ttu-id="63cd3-107">Die strukturierte Speicherung bietet Datei-und Daten Persistenz in com, indem eine einzelne Datei als strukturierte Auflistung von Objekten behandelt wird, die als Speicher und Streams bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="63cd3-107">Structured Storage provides file and data persistence in COM by handling a single file as a structured collection of objects known as storages and streams.</span></span>

<span data-ttu-id="63cd3-108">Der Zweck der strukturierten Speicherung besteht darin, die Leistungseinbußen und den Aufwand für das Speichern von separaten Objekten in einer einzelnen Datei zu verringern.</span><span class="sxs-lookup"><span data-stu-id="63cd3-108">The purpose of Structured Storage is to reduce the performance penalties and overhead associated with storing separate objects in a single file.</span></span> <span data-ttu-id="63cd3-109">Die strukturierte Speicherung bietet eine Lösung, indem definiert wird, wie eine einzelne Datei Entität als strukturierte Auflistung von zwei Typen von Objekten verarbeitet und durch eine Standard Implementierung mit dem Namen "Verbund Dateien" gestreamt wird.</span><span class="sxs-lookup"><span data-stu-id="63cd3-109">Structured Storage provides a solution by defining how to handle a single file entity as a structured collection of two types of objects storages and streams through a standard implementation called Compound Files.</span></span> <span data-ttu-id="63cd3-110">Dies ermöglicht es dem Benutzer, mit einer Verbund Datei zu interagieren und diese zu verwalten, als ob es sich um eine einzelne Datei und nicht um eine geschachtelte Hierarchy von separaten Objekten handelt.</span><span class="sxs-lookup"><span data-stu-id="63cd3-110">This enables the user to interact with, and manage, a compound file as if it were a single file rather than a nested hierarchy of separate objects.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="63cd3-111">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="63cd3-111">Where applicable</span></span>

<span data-ttu-id="63cd3-112">Strukturierter Speicher kann auf Microsoft com-basierten Betriebssystemen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="63cd3-112">Structured Storage can be used on Microsoft COM-based operating systems.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="63cd3-113">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="63cd3-113">Developer audience</span></span>

<span data-ttu-id="63cd3-114">Die strukturierte Speicher Dokumentation ist für erfahrene C-und C++-Programmierer und com-basierte Systementwickler gedacht.</span><span class="sxs-lookup"><span data-stu-id="63cd3-114">The Structured Storage documentation is intended for experienced C and C++ programmers and COM-based system developers.</span></span>

<span data-ttu-id="63cd3-115">Die strukturierte Speicherung unterstützt hauptsächlich C-und C++-Programmiersprachen, aber alle COM-basierten Technologien unterstützen auch jede Programmiersprache, die Schnittstellen Zeiger verwendet.</span><span class="sxs-lookup"><span data-stu-id="63cd3-115">Structured Storage primarily supports C and C++ programming languages, however any COM-based technology will also support any programming language that utilizes interface pointers.</span></span>

<span data-ttu-id="63cd3-116">Ein solides Verständnis der com-Technologien ist eine Voraussetzung für die Entwicklungs Verwendung von strukturiertem Speicher.</span><span class="sxs-lookup"><span data-stu-id="63cd3-116">A solid understanding of COM technologies is prerequisite to the developmental use of Structured Storage.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="63cd3-117">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="63cd3-117">Run-time requirements</span></span>

<span data-ttu-id="63cd3-118">Weitere Informationen zu den Betriebssystemen, die für die Verwendung eines bestimmten API-Elements erforderlich sind, finden Sie im Abschnitt "Anforderungen" in der Dokumentation für das-Element.</span><span class="sxs-lookup"><span data-stu-id="63cd3-118">For more information about which operating systems are required to use a particular API element, see the Requirements section of the documentation for the element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="63cd3-119">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="63cd3-119">In this section</span></span>



| <span data-ttu-id="63cd3-120">Thema</span><span class="sxs-lookup"><span data-stu-id="63cd3-120">Topic</span></span>                                                               | <span data-ttu-id="63cd3-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="63cd3-121">Description</span></span>                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63cd3-122">Übersicht</span><span class="sxs-lookup"><span data-stu-id="63cd3-122">Overview</span></span>](about-structured-storage.md)<br/>                 | <span data-ttu-id="63cd3-123">Allgemeine Informationen über die strukturierte Speicherung.</span><span class="sxs-lookup"><span data-stu-id="63cd3-123">General information about Structured Storage.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="63cd3-124">Verwenden von strukturierter Speicherung</span><span class="sxs-lookup"><span data-stu-id="63cd3-124">Using Structured Storage</span></span>](using-structured-storage.md)<br/> | <span data-ttu-id="63cd3-125">Verwenden von Informationen für die strukturierte Speicherung.</span><span class="sxs-lookup"><span data-stu-id="63cd3-125">Using information for Structured Storage.</span></span><br/>                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="63cd3-126">Verweis</span><span class="sxs-lookup"><span data-stu-id="63cd3-126">Reference</span></span>](structured-storage-reference.md)<br/>            | <span data-ttu-id="63cd3-127">Dokumentation zu strukturierten Speicher spezifischen Schnittstellen, Funktionen, Strukturen und Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="63cd3-127">Documentation of Structured Storage specific interfaces, functions, structures, and enumerations.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="63cd3-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63cd3-128">Samples</span></span>](samples.md)<br/>                                   | <span data-ttu-id="63cd3-129">In C++ geschriebene Code Beispiele.</span><span class="sxs-lookup"><span data-stu-id="63cd3-129">Code examples written in C++.</span></span> <span data-ttu-id="63cd3-130">Weitere Informationen finden Sie unter [Namen in IStorage](names-in-istorage.md), [Eigenschaften Satz Header](property-set-header.md), [Abschnitt](section.md), [Speichern von Eigenschafts Sätzen](storing-property-sets.md)und [Verwenden von strukturiertem Speicher](using-structured-storage.md).</span><span class="sxs-lookup"><span data-stu-id="63cd3-130">For more information, see [Names in IStorage](names-in-istorage.md), [Property Set Header](property-set-header.md), [Section](section.md), [Storing Property Sets](storing-property-sets.md), and [Using Structured Storage](using-structured-storage.md).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="63cd3-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="63cd3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63cd3-132">Das Component Object Model</span><span class="sxs-lookup"><span data-stu-id="63cd3-132">The Component Object Model</span></span>](../com/the-component-object-model.md)
</dt> </dl>

 

