---
title: Quellen Zuständigkeiten ziehen
description: Quellen Zuständigkeiten ziehen
ms.assetid: bafef0c1-f78e-424a-9ed0-07764a60b22d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce91a795815148f442c19530a552cf7c843332
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106339914"
---
# <a name="drag-source-responsibilities"></a><span data-ttu-id="f9213-103">Quellen Zuständigkeiten ziehen</span><span class="sxs-lookup"><span data-stu-id="f9213-103">Drag Source Responsibilities</span></span>

<span data-ttu-id="f9213-104">Die Zieh Quelle ist für die folgenden Aufgaben zuständig:</span><span class="sxs-lookup"><span data-stu-id="f9213-104">The drag source is responsible for the following tasks:</span></span>

-   <span data-ttu-id="f9213-105">Bereitstellen eines Datenübertragungs Objekts für das Ablage Ziel, das die [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -Schnittstelle und die [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="f9213-105">Providing a data-transfer object for the drop target that exposes the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) and [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interfaces.</span></span>
-   <span data-ttu-id="f9213-106">Zeiger-und Quell Feedback werden erzeugt.</span><span class="sxs-lookup"><span data-stu-id="f9213-106">Generating pointer and source feedback.</span></span>
-   <span data-ttu-id="f9213-107">Es wird ermittelt, wann der Zieh Vorgang abgebrochen wurde oder ein Ablage Vorgang aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="f9213-107">Determining when the drag operation has been canceled or a drop operation has occurred.</span></span>
-   <span data-ttu-id="f9213-108">Ausführen von Aktionen für die ursprünglichen Daten, die durch den Drop-Vorgang verursacht wurden, wie z. b. das Löschen der Daten oder das Erstellen einer Verknüpfung.</span><span class="sxs-lookup"><span data-stu-id="f9213-108">Performing any action on the original data caused by the drop operation, such as deleting the data or creating a link to it.</span></span>

<span data-ttu-id="f9213-109">Die Hauptaufgabe ist das Erstellen eines Datenübertragungs Objekts, das die [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) -Schnittstelle und die [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="f9213-109">The main task is creating a data-transfer object that exposes the [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) and [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) interfaces.</span></span> <span data-ttu-id="f9213-110">Die Zieh Quelle enthält möglicherweise eine Kopie der ausgewählten Daten.</span><span class="sxs-lookup"><span data-stu-id="f9213-110">The drag source might or might not include a copy of the selected data.</span></span> <span data-ttu-id="f9213-111">Dies ist nicht zwingend erforderlich, aber dadurch wird der Schutz vor unbeabsichtigten Änderungen gewährleistet, und der Code der Zwischenablage kann mit dem Drag & Drop-Code identisch sein.</span><span class="sxs-lookup"><span data-stu-id="f9213-111">Including it is not mandatory, but doing so helps protect against inadvertent changes and allows the Clipboard operations code to be identical to the drag and drop code.</span></span>

<span data-ttu-id="f9213-112">Während eines Zieh Vorgangs ist die Zieh Quelle für das Festlegen des Mauszeigers und ggf. für das Bereitstellen zusätzlicher Quell Feedback für den Benutzer verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="f9213-112">While a drag operation is in progress, the drag source is responsible for setting the mouse pointer and, if appropriate, for providing additional source feedback to the user.</span></span> <span data-ttu-id="f9213-113">Die Zieh Quelle kann kein Feedback bereitstellen, das die Mausposition nachverfolgt, außer durch das tatsächliche Festlegen des echten Zeigers (siehe [**SetCursor**](/windows/win32/api/winuser/nf-winuser-setcursor) -Funktion).</span><span class="sxs-lookup"><span data-stu-id="f9213-113">The drag source cannot provide any feedback that tracks the mouse position other than by actually setting the real pointer (see the [**SetCursor**](/windows/win32/api/winuser/nf-winuser-setcursor) function).</span></span> <span data-ttu-id="f9213-114">Diese Regel muss erzwungen werden, um Konflikte mit dem vom Drop-Ziel bereitgestellten Feedback zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="f9213-114">This rule must be enforced to avoid conflicts with the feedback provided by the drop target.</span></span> <span data-ttu-id="f9213-115">(Eine Zieh Quelle kann auch ein Ablage Ziel sein.</span><span class="sxs-lookup"><span data-stu-id="f9213-115">(A drag source can also be a drop target.</span></span> <span data-ttu-id="f9213-116">Wenn Sie sich selbst ablegen, kann die Quelle/das Ziel natürlich das Ziel Feedback bereitstellen, um die Mausposition zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="f9213-116">When dropping on itself, the source/target can, of course, provide target feedback to track the mouse position.</span></span> <span data-ttu-id="f9213-117">In diesem Fall ist es jedoch das Ablage Ziel, das die Maus nachverfolgt, nicht die Quelle.) Basierend auf dem Feedback, das das Ablage Ziel bietet, legt die Quelle einen entsprechenden Zeiger fest.</span><span class="sxs-lookup"><span data-stu-id="f9213-117">In this case, however, it is the drop target tracking the mouse, not the source.) Based on the feedback offered by the drop target, the source sets an appropriate pointer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9213-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9213-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9213-119">Drag &amp; Drop</span><span class="sxs-lookup"><span data-stu-id="f9213-119">Drag and Drop</span></span>](drag-and-drop.md)
</dt> </dl>

 

 