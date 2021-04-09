---
title: Attribut Bereichs Abruf
description: Ein mehr wertiges Attribut kann fast eine beliebige Anzahl von Werten aufweisen. In vielen Fällen kann es vorteilhaft oder sogar notwendig sein, den Wertebereich einzuschränken, der von einer Abfrage abgerufen wird.
ms.assetid: 3a0eb764-fca9-4ca6-9991-b85f293961af
ms.tgt_platform: multiple
keywords:
- Attribut Bereichs Abruf ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f8787eb0b2aba30d1926b4d9cbb7e566e0f59c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947359"
---
# <a name="attribute-range-retrieval"></a><span data-ttu-id="f3d27-105">Attribut Bereichs Abruf</span><span class="sxs-lookup"><span data-stu-id="f3d27-105">Attribute Range Retrieval</span></span>

<span data-ttu-id="f3d27-106">Ein mehr wertiges Attribut kann fast eine beliebige Anzahl von Werten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f3d27-106">A multi-valued attribute can have almost any number of values.</span></span> <span data-ttu-id="f3d27-107">In vielen Fällen kann es vorteilhaft oder sogar notwendig sein, den Wertebereich einzuschränken, der von einer Abfrage abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f3d27-107">In many cases, it may be advantageous, or even necessary, to limit the range of values that are retrieved by a query.</span></span>

<span data-ttu-id="f3d27-108">Der Bereichs Abruf umfasst das Anfordern einer begrenzten Anzahl von Attributwerten in einer einzelnen Abfrage.</span><span class="sxs-lookup"><span data-stu-id="f3d27-108">Range retrieval involves requesting a limited number of attribute values in a single query.</span></span> <span data-ttu-id="f3d27-109">Die Anzahl der angeforderten Werte muss kleiner oder gleich der maximalen Anzahl von Werten sein, die vom Server unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f3d27-109">The number of values requested must be less than, or equal to, the maximum number of values supported by the server.</span></span> <span data-ttu-id="f3d27-110">Um die Häufigkeit zu verringern, mit der die Abfrage den Server kontaktieren muss, sollte die Anzahl der angeforderten Werte so nah wie möglich an diesem Maximum liegen.</span><span class="sxs-lookup"><span data-stu-id="f3d27-110">To reduce the number of times the query must contact the server, the number of values requested should be as close to this maximum as possible.</span></span> <span data-ttu-id="f3d27-111">Damit eine Anwendung ordnungsgemäß mit allen Windows-Servern funktioniert, sollte eine maximale Anzahl von 1000 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3d27-111">To enable an application to work correctly with all Windows servers, a maximum number of 1000 should be used.</span></span>

<span data-ttu-id="f3d27-112">Die bereichsspezifier für eine Eigenschaften Abfrage muss folgende Form haben:</span><span class="sxs-lookup"><span data-stu-id="f3d27-112">The range specifiers for a property query require the following form:</span></span>


```C++
range=<low range>-<high range>
```



<span data-ttu-id="f3d27-113">dabei &lt; ist "Low Range &gt; " der null basierte Index des ersten Eigenschafts Werts, der abgerufen werden soll, und " &lt; High Range &gt; " ist der null basierte Index des letzten Eigenschafts Werts, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3d27-113">where "&lt;low range&gt;" is the zero-based index of the first property value to retrieve and "&lt;high range&gt;" is the zero-based index of the last property value to retrieve.</span></span> <span data-ttu-id="f3d27-114">NULL wird für " &lt; niedriger Bereich &gt; " verwendet, um den ersten Eintrag anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f3d27-114">Zero is used for "&lt;low range&gt;" to specify the first entry.</span></span> <span data-ttu-id="f3d27-115">Das Platzhalter Zeichen ( \* ) kann für " &lt; High Range" verwendet werden &gt; , um alle verbleibenden Einträge anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f3d27-115">The wildcard character (\*) can be used for "&lt;high range&gt;" to specify all remaining entries.</span></span>

<span data-ttu-id="f3d27-116">In der folgenden Tabelle sind Beispiele für Bereichs Bearbeiter aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3d27-116">The following table lists examples of range specifiers.</span></span>



| <span data-ttu-id="f3d27-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f3d27-117">Example</span></span>      | <span data-ttu-id="f3d27-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3d27-118">Description</span></span>                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d27-119">Bereich = 0-\*</span><span class="sxs-lookup"><span data-stu-id="f3d27-119">range=0-\*</span></span>   | <span data-ttu-id="f3d27-120">Ruft alle Eigenschaftswerte ab.</span><span class="sxs-lookup"><span data-stu-id="f3d27-120">Retrieve all property values.</span></span> <span data-ttu-id="f3d27-121">Dies unterliegt den vom Server vorgegebenen Grenzwerten.</span><span class="sxs-lookup"><span data-stu-id="f3d27-121">This is subject to limits imposed by the server.</span></span>                |
| <span data-ttu-id="f3d27-122">Bereich = 0-500</span><span class="sxs-lookup"><span data-stu-id="f3d27-122">range=0-500</span></span>  | <span data-ttu-id="f3d27-123">Abrufen von 1. bis 501st-Werten.</span><span class="sxs-lookup"><span data-stu-id="f3d27-123">Retrieve from 1st to 501st values inclusively.</span></span>                                                |
| <span data-ttu-id="f3d27-124">Bereich = 2-3</span><span class="sxs-lookup"><span data-stu-id="f3d27-124">range=2-3</span></span>    | <span data-ttu-id="f3d27-125">Abrufen von 3-und 4-Werten.</span><span class="sxs-lookup"><span data-stu-id="f3d27-125">Retrieve 3rd and 4th values.</span></span>                                                                  |
| <span data-ttu-id="f3d27-126">Bereich = 501-\*</span><span class="sxs-lookup"><span data-stu-id="f3d27-126">range=501-\*</span></span> | <span data-ttu-id="f3d27-127">Rufen Sie das 502nd und alle verbleibenden Werte ab.</span><span class="sxs-lookup"><span data-stu-id="f3d27-127">Retrieve the 502nd and all remaining values.</span></span> <span data-ttu-id="f3d27-128">Dies unterliegt den vom Server vorgegebenen Grenzwerten.</span><span class="sxs-lookup"><span data-stu-id="f3d27-128">This is subject to limits imposed by the server.</span></span> |



 

<span data-ttu-id="f3d27-129">Es gibt verschiedene Möglichkeiten zum Abrufen eines Bereichs von Eigenschafts Werten.</span><span class="sxs-lookup"><span data-stu-id="f3d27-129">There are several different ways to retrieve a range of property values.</span></span> <span data-ttu-id="f3d27-130">Die [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) -Methode kann entweder in einer Automatisierungs Sprache oder in C++ verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3d27-130">The [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) method can be used in either an automation language or C++.</span></span> <span data-ttu-id="f3d27-131">Die **IADs. GetInfoEx** -Methode ist die bevorzugte Methode zur Durchführung des Bereichs Abrufs.</span><span class="sxs-lookup"><span data-stu-id="f3d27-131">The **IADs.GetInfoEx** method is the preferred method of performing range retrieval.</span></span> <span data-ttu-id="f3d27-132">Weitere Informationen zur Verwendung von **IADs. GetInfoEx** für den Bereichs Abruf finden Sie unter [using IADs:: GetInfoEx for Range Abruf](using-iads--getinfoex-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="f3d27-132">For more information about using **IADs.GetInfoEx** for range retrieval, see [Using IADs::GetInfoEx for Range Retrieval](using-iads--getinfoex-for-range-retrieval.md).</span></span>

<span data-ttu-id="f3d27-133">Wenn eine Automatisierungs Sprache verwendet wird, können die ActiveX-Verzeichnisobjekte (ADO) zum Abrufen eines Bereichs von Eigenschafts Werten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3d27-133">If an automation language is used, the ActiveX Directory Objects (ADO) can be used to retrieve a range of property values.</span></span> <span data-ttu-id="f3d27-134">Weitere Informationen zur Verwendung von ADO für den Bereichs Abruf finden Sie unter [Verwenden von ADO für den Bereichs Abruf](using-ado-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="f3d27-134">For more information about using ADO for range retrieval, see [Using ADO for Range Retrieval](using-ado-for-range-retrieval.md).</span></span>

<span data-ttu-id="f3d27-135">Wenn C++ verwendet wird, können die Schnittstellen [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) und [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) zum Abrufen eines Bereichs von Eigenschafts Werten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3d27-135">If C++ is used, the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) and [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interfaces can be used to retrieve a range of property values.</span></span> <span data-ttu-id="f3d27-136">Weitere Informationen zur Verwendung von **IDirectorySearch** und **IDirectoryObject** für den Bereichs Abruf finden [Sie unter Verwenden von IDirectorySearch und IDirectoryObject für den Bereichs Abruf](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).</span><span class="sxs-lookup"><span data-stu-id="f3d27-136">For more information about using **IDirectorySearch** and **IDirectoryObject** for range retrieval, see [Using IDirectorySearch and IDirectoryObject for Range Retrieval](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).</span></span>

 

 




