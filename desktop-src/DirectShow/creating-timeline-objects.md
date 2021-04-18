---
description: Erstellen von Zeitachsen Objekten
ms.assetid: fb369b32-a54b-4d8a-8358-5f05aa48f853
title: Erstellen von Zeitachsen Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 929fffb6a953e198b6e7ed9b17250d45e84f7932
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344319"
---
# <a name="creating-timeline-objects"></a><span data-ttu-id="b7c6f-103">Erstellen von Zeitachsen Objekten</span><span class="sxs-lookup"><span data-stu-id="b7c6f-103">Creating Timeline Objects</span></span>

<span data-ttu-id="b7c6f-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="b7c6f-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="b7c6f-105">Der Beispielcode in diesem Artikel beginnt mit einer leeren Zeitachse, aber die gleichen Schritte gelten auch, wenn Sie ein vorhandenes Projekt laden und diesem Objekte hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="b7c6f-105">The sample code presented in this article starts with an empty timeline, but the same steps apply if you load an existing project and want to add objects to it.</span></span>

<span data-ttu-id="b7c6f-106">Um einen beliebigen Objekttyp in der Zeitachse zu erstellen, rufen Sie die [**iamtimeline::**](iamtimeline-createemptynode.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="b7c6f-106">To create any type of object in the timeline, call the [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) method.</span></span> <span data-ttu-id="b7c6f-107">Mit dem folgenden Code wird beispielsweise eine neue Gruppe erstellt:</span><span class="sxs-lookup"><span data-stu-id="b7c6f-107">For example, the following code creates a new group:</span></span>


```C++
IAMTimelineObj *pGroupObj = NULL;
pTL->CreateEmptyNode(&pGroupObj, TIMELINE_MAJOR_TYPE_GROUP);
```



<span data-ttu-id="b7c6f-108">Der zweite Parameter ist ein Member der [**Timeline- \_ \_ Haupttyp**](timeline-major-type.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="b7c6f-108">The second parameter is a member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumeration.</span></span> <span data-ttu-id="b7c6f-109">Gibt den Typ des zu erstellenden Zeitachsen Objekts an, z. b. eine Gruppe oder eine Spur.</span><span class="sxs-lookup"><span data-stu-id="b7c6f-109">It specifies the type of timeline object to create, such as a group or a track.</span></span>

<span data-ttu-id="b7c6f-110">Die Methode " **kreateemptynode** " erstellt das Objekt und gibt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="b7c6f-110">The **CreateEmptyNode** method creates the object and returns a pointer to the object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span> <span data-ttu-id="b7c6f-111">Außerdem erhöht Sie den Verweis Zähler für die **iamtimelineobj** -Schnittstelle, sodass Sie die Schnittstelle freigeben müssen, wenn Sie die Verwendung abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="b7c6f-111">It also increments the reference count on the **IAMTimelineObj** interface, so you must release the interface when you finish using it.</span></span> <span data-ttu-id="b7c6f-112">Nennen Sie die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion nicht.</span><span class="sxs-lookup"><span data-stu-id="b7c6f-112">Do not call the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span> <span data-ttu-id="b7c6f-113">Verwenden Sie stattdessen immer "antachse **", um** ein Zeitachsen Objekt zu erstellen, da das neue-Objekt für die Verwendung in einer Zeitachse initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b7c6f-113">Instead, always use **CreateEmptyNode** to create a timeline object, because it initializes the new object for use in a timeline.</span></span>

<span data-ttu-id="b7c6f-114">Die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle ist eine generische Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b7c6f-114">The [**IAMTimelineObj**](iamtimelineobj.md) interface is a generic interface.</span></span> <span data-ttu-id="b7c6f-115">Es stellt Methoden bereit, die allen Typen von Timeline-Objekten gemeinsam sind.</span><span class="sxs-lookup"><span data-stu-id="b7c6f-115">It provides methods that are common to all types of timeline object.</span></span> <span data-ttu-id="b7c6f-116">Jeder Objekttyp macht auch andere Schnittstellen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b7c6f-116">Each type of object exposes other interfaces as well.</span></span> <span data-ttu-id="b7c6f-117">Beispielsweise machen Gruppen unter anderem die [**iamtimelinegroup**](iamtimelinegroup.md) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b7c6f-117">For example, groups expose the [**IAMTimelineGroup**](iamtimelinegroup.md) interface, among others.</span></span> <span data-ttu-id="b7c6f-118">Sie können Zeiger auf die anderen Schnittstellen abrufen, indem Sie **QueryInterface** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b7c6f-118">You can obtain pointers to the other interfaces by calling **QueryInterface**.</span></span>

<span data-ttu-id="b7c6f-119">Nachdem Sie ein Objekt erstellt haben, ist es noch kein Teil der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="b7c6f-119">After you create an object, it is not yet a part of the timeline.</span></span> <span data-ttu-id="b7c6f-120">Die Methode zum Hinzufügen eines Objekts zur Zeitachse hängt vom Objekttyp ab.</span><span class="sxs-lookup"><span data-stu-id="b7c6f-120">The method to add an object to the timeline depends on the object type.</span></span> <span data-ttu-id="b7c6f-121">Im folgenden Abschnitt wird beschrieben, wie Sie Gruppen, Kompositionen und Spuren zur Zeitachse hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7c6f-121">The following section describes how to add groups, compositions, and tracks to the timeline.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7c6f-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b7c6f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7c6f-123">Erstellen einer Zeitachse</span><span class="sxs-lookup"><span data-stu-id="b7c6f-123">Constructing a Timeline</span></span>](constructing-a-timeline.md)
</dt> </dl>

 

 
