---
title: Drag & Drop
description: Drag & Drop bezieht sich auf Datenübertragungen, bei denen eine Maus oder ein anderes Zeigegerät verwendet wird, um sowohl die Datenquelle als auch das Ziel anzugeben.
ms.assetid: bba0ddf8-fcf9-4827-bf85-7ac597d33b4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc4b425637432024d097acb8afdc5e169467c6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337167"
---
# <a name="drag-and-drop"></a><span data-ttu-id="34fe5-103">Drag & Drop</span><span class="sxs-lookup"><span data-stu-id="34fe5-103">Drag and Drop</span></span>

<span data-ttu-id="34fe5-104">*Drag & Drop* bezieht sich auf Datenübertragungen, bei denen eine Maus oder ein anderes Zeigegerät verwendet wird, um sowohl die Datenquelle als auch das Ziel anzugeben.</span><span class="sxs-lookup"><span data-stu-id="34fe5-104">*Drag and drop* refers to data transfers in which a mouse or other pointing device is used to specify both the data source and its destination.</span></span> <span data-ttu-id="34fe5-105">Bei einem typischen Drag & Drop-Vorgang wählt ein Benutzer das zu übertragende Objekt aus, indem der Mauszeiger darauf bewegt und entweder die linke Schaltfläche oder eine andere für diesen Zweck festgelegte Schaltfläche gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="34fe5-105">In a typical drag and drop operation, a user selects the object to be transferred by moving the mouse pointer to it and holding down either the left button or some other button designated for this purpose.</span></span> <span data-ttu-id="34fe5-106">Wenn Sie die Schaltfläche weiterhin gedrückt halten, initiiert der Benutzer die Übertragung, indem er das Objekt auf das Ziel, das beliebige OLE-Container sein kann, zieht.</span><span class="sxs-lookup"><span data-stu-id="34fe5-106">While continuing to hold down the button, the user initiates the transfer by dragging the object to its destination, which can be any OLE container.</span></span> <span data-ttu-id="34fe5-107">Drag & Drop bietet genau die gleiche Funktionalität wie das Kopieren und Einfügen der OLE-Zwischenablage, fügt aber visuelles Feedback hinzu und entfällt die Notwendigkeit von Menüs.</span><span class="sxs-lookup"><span data-stu-id="34fe5-107">Drag and drop provides exactly the same functionality as the OLE clipboard copy and paste but adds visual feedback and eliminates the need for menus.</span></span> <span data-ttu-id="34fe5-108">Wenn eine Anwendung das Kopieren und Einfügen von Zwischenablage unterstützt, ist ein wenig zusätzlicher Aufwand erforderlich, um Drag & Drop zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="34fe5-108">In fact, if an application supports clipboard copy and paste, little extra is needed to support drag and drop.</span></span>

<span data-ttu-id="34fe5-109">Während eines OLE-Drag & Drop-Vorgangs werden die folgenden drei separaten Code Elemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="34fe5-109">During an OLE drag and drop operation, the following three separate pieces of code are used.</span></span>



| <span data-ttu-id="34fe5-110">Drag & Drop-Code Quelle</span><span class="sxs-lookup"><span data-stu-id="34fe5-110">Drag-and-drop code source</span></span>                               | <span data-ttu-id="34fe5-111">Implementierung und Verwendung</span><span class="sxs-lookup"><span data-stu-id="34fe5-111">Implementation and use</span></span>                                                                                                                                                                      |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34fe5-112">[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) -Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="34fe5-112">[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interface</span></span><br/> | <span data-ttu-id="34fe5-113">Wird von dem Objekt implementiert, das die gezogenen Daten enthält, die als Zieh *Quelle* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="34fe5-113">Implemented by the object containing the dragged data, referred to as the *drag source*.</span></span><br/>                                                                                         |
| <span data-ttu-id="34fe5-114">[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) -Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="34fe5-114">[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) interface</span></span><br/> | <span data-ttu-id="34fe5-115">Wird von dem Objekt implementiert, das den Löschvorgang akzeptieren soll, der als Ablage *Ziel* bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="34fe5-115">Implemented by the object that is intended to accept the drop, referred to as the *drop target*.</span></span><br/>                                                                                 |
| <span data-ttu-id="34fe5-116">[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) -Funktion</span><span class="sxs-lookup"><span data-stu-id="34fe5-116">[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) function</span></span><br/>    | <span data-ttu-id="34fe5-117">Wird von OLE implementiert und zum Initiieren eines Drag & Drop-Vorgangs verwendet.</span><span class="sxs-lookup"><span data-stu-id="34fe5-117">Implemented by OLE and used to initiate a drag and drop operation.</span></span> <span data-ttu-id="34fe5-118">Nachdem der Vorgang ausgeführt wurde, wird die Kommunikation zwischen der Zieh Quelle und dem Ablage Ziel erleichtert.</span><span class="sxs-lookup"><span data-stu-id="34fe5-118">After the operation is in progress, it facilitates communication between the drag source and the drop target.</span></span><br/> |



 

<span data-ttu-id="34fe5-119">Die [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) -Schnittstelle und die [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) -Schnittstelle können entweder in einem Container oder in einer Objekt Anwendung implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="34fe5-119">The [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) and [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) interfaces can be implemented in either a container or in an object application.</span></span> <span data-ttu-id="34fe5-120">Die Rolle von "Drag Source" oder "Drop Target" ist nicht auf einen Typ von OLE-Anwendungen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="34fe5-120">The role of drag source or drop target is not limited to any one type of OLE application.</span></span>

<span data-ttu-id="34fe5-121">Die OLE-Funktion [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implementiert eine Schleife, mit der die Maus-und Tastatur Bewegung nachverfolgt wird, bis der Zieh Vorgang abgebrochen oder eine Ablage auftritt.</span><span class="sxs-lookup"><span data-stu-id="34fe5-121">The OLE function [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) implements a loop that tracks mouse and keyboard movement until such time as the drag is canceled or a drop occurs.</span></span> <span data-ttu-id="34fe5-122">**DoDragDrop** ist die Schlüsselfunktion im Drag & Drop-Prozess und ermöglicht so die Kommunikation zwischen der Zieh Quelle und dem Ablage Ziel.</span><span class="sxs-lookup"><span data-stu-id="34fe5-122">**DoDragDrop** is the key function in the drag and drop process, facilitating communication between the drag source and drop target.</span></span>

<span data-ttu-id="34fe5-123">Während eines Drag & Drop-Vorgangs können dem Benutzer drei Feedback Typen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="34fe5-123">During a drag and drop operation, three types of feedback can be displayed to the user.</span></span>



| <span data-ttu-id="34fe5-124">Art des Feedbacks</span><span class="sxs-lookup"><span data-stu-id="34fe5-124">Type of feedback</span></span>            | <span data-ttu-id="34fe5-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34fe5-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34fe5-126">Quellen Feedback</span><span class="sxs-lookup"><span data-stu-id="34fe5-126">Source feedback</span></span><br/>  | <span data-ttu-id="34fe5-127">Das Feedback der Quelle wird von der Zieh Quelle bereitgestellt und zeigt an, dass die Daten gezogen und während des Zieh Vorgangs nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="34fe5-127">Provided by the drag source, the source feedback indicates the data is being dragged and does not change during the course of the drag.</span></span> <span data-ttu-id="34fe5-128">Normalerweise werden die Daten hervorgehoben, um zu signalisieren, dass Sie ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="34fe5-128">Typically, the data is highlighted to signal it has been selected.</span></span><br/>                                                                                                                                            |
| <span data-ttu-id="34fe5-129">Zeiger Feedback</span><span class="sxs-lookup"><span data-stu-id="34fe5-129">Pointer feedback</span></span><br/> | <span data-ttu-id="34fe5-130">Der von der Zieh Quelle bereitgestellte Zeiger gibt an, was geschieht, wenn die Maus zu einem beliebigen Zeitpunkt freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="34fe5-130">Provided by the drag source, the pointer feedback indicates what happens if the mouse is released at any given moment.</span></span> <span data-ttu-id="34fe5-131">Zeiger Feedback werden fortlaufend geändert, wenn der Benutzer die Maus bewegt und/oder eine Modifizierertaste drückt.</span><span class="sxs-lookup"><span data-stu-id="34fe5-131">Pointer feedback changes continually as the user moves the mouse and/or presses a modifier key.</span></span> <span data-ttu-id="34fe5-132">Wenn der Zeiger z. b. in ein Fenster verschoben wird, das keinen Löschvorgang akzeptieren kann, wird der Zeiger in das Symbol "nicht zulässig" geändert.</span><span class="sxs-lookup"><span data-stu-id="34fe5-132">For example, if the pointer is moved into a window that cannot accept a drop, the pointer changes to the "not allowed" symbol.</span></span><br/> |
| <span data-ttu-id="34fe5-133">Ziel Feedback</span><span class="sxs-lookup"><span data-stu-id="34fe5-133">Target feedback</span></span><br/>  | <span data-ttu-id="34fe5-134">Das vom Ablage Ziel bereitgestellte Ziel Feedback gibt an, wo der Ablage Vorgang erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="34fe5-134">Provided by the drop target, target feedback indicates where the drop is to occur.</span></span><br/>                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="34fe5-135">Weitere Informationen finden Sie unter über [tragen von Quell Zuständigkeiten](drag-source-responsibilities.md).</span><span class="sxs-lookup"><span data-stu-id="34fe5-135">For more information, see [Drag Source Responsibilities](drag-source-responsibilities.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="34fe5-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="34fe5-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34fe5-137">Datenübertragung</span><span class="sxs-lookup"><span data-stu-id="34fe5-137">Data Transfer</span></span>](data-transfer.md)
</dt> </dl>

 

 





