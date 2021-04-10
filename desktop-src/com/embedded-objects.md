---
title: Eingebettete Objekte (com)
description: Eingebettete Objekte
ms.assetid: 1f863fd4-fead-4dd3-b855-8820e015b52a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8da9938b17130209fec024f94ee99061ad690693
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102691"
---
# <a name="embedded-objects-com"></a><span data-ttu-id="82344-103">Eingebettete Objekte (com)</span><span class="sxs-lookup"><span data-stu-id="82344-103">Embedded Objects (COM)</span></span>

<span data-ttu-id="82344-104">Ein eingebettetes Objekt wird physisch im Verbund Dokument gespeichert, zusammen mit allen Informationen, die für die Verwaltung des Objekts benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="82344-104">An embedded object is physically stored in the compound document, along with all the information needed to manage the object.</span></span> <span data-ttu-id="82344-105">Das heißt, dass das eingebettete Objekt tatsächlich Teil des Verbund Dokuments ist, in dem es sich befindet.</span><span class="sxs-lookup"><span data-stu-id="82344-105">In other words, the embedded object is actually a part of the compound document in which it resides.</span></span> <span data-ttu-id="82344-106">Diese Anordnung hat einige Nachteile.</span><span class="sxs-lookup"><span data-stu-id="82344-106">This arrangement has a couple of disadvantages.</span></span> <span data-ttu-id="82344-107">Zuerst ist ein zusammengesetztes Dokument mit eingebetteten Objekten größer als eins, das die gleichen Objekte wie Verknüpfungen enthält.</span><span class="sxs-lookup"><span data-stu-id="82344-107">First, a compound document containing embedded objects will be larger than one containing the same objects as links.</span></span> <span data-ttu-id="82344-108">Zweitens werden Änderungen, die an der Quelle eines eingebetteten Objekts vorgenommen werden, nicht automatisch in der eingebetteten Kopie repliziert, und Änderungen in der eingebetteten Kopie werden nicht in der Quelle übernommen, wie Sie es bei einem Link gibt.</span><span class="sxs-lookup"><span data-stu-id="82344-108">Second, changes made to the source of an embedded object will not be automatically replicated in the embedded copy, and changes in the embedded copy will not be reflected in the source, as they are with a link.</span></span>

<span data-ttu-id="82344-109">Für bestimmte Zwecke bietet Einbettungen aber mehrere Vorteile gegenüber Links.</span><span class="sxs-lookup"><span data-stu-id="82344-109">Still, for certain purposes, embedding offers several advantages over links.</span></span> <span data-ttu-id="82344-110">Zunächst können die Benutzer zusammengesetzte Dokumente mit eingebetteten Objekten auf andere Computer oder an andere Speicherorte auf demselben Computer übertragen, ohne einen Link zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="82344-110">First, users can transfer compound documents with embedded objects to other computers, or other locations on the same computer, without breaking a link.</span></span> <span data-ttu-id="82344-111">Zweitens können Benutzer eingebettete Objekte bearbeiten, ohne den Inhalt des Originals zu ändern.</span><span class="sxs-lookup"><span data-stu-id="82344-111">Second, users can edit embedded objects without changing the content of the original.</span></span> <span data-ttu-id="82344-112">Manchmal ist diese Trennung genau das, was erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="82344-112">Sometimes, this separation is precisely what is required.</span></span> <span data-ttu-id="82344-113">Drittens können eingebettete Objekte direkt aktiviert werden. Dies bedeutet, dass der Benutzer das Objekt bearbeiten oder anderweitig bearbeiten kann, ohne in einem separaten Fenster von dem Container des Objekts arbeiten zu müssen.</span><span class="sxs-lookup"><span data-stu-id="82344-113">Third, embedded objects can be activated in place, meaning that the user can edit or otherwise manipulate the object without having to work in a separate window from that of the object's container.</span></span> <span data-ttu-id="82344-114">Wenn das Objekt aktiviert ist, wird stattdessen die Benutzeroberfläche der Containeranwendung geändert, um die Tools verfügbar zu machen, die zum Verwalten oder Ändern des Objekts erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="82344-114">Instead, when the object is activated, the container application's user interface changes to expose those tools that are necessary to manage or modify the object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82344-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="82344-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82344-116">Erstellen von verknüpften und eingebetteten Objekten aus vorhandenen Daten</span><span class="sxs-lookup"><span data-stu-id="82344-116">Creating Linked and Embedded Objects from Existing Data</span></span>](creating-linked-and-embedded-objects-from-existing-data.md)
</dt> </dl>

 

 




