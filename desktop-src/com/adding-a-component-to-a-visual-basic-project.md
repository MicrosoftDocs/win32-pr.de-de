---
title: Hinzufügen einer Komponente zu einem Visual Basic Projekt
description: Hinzufügen einer Komponente zu einem Visual Basic Projekt
ms.assetid: 7e78853a-b134-46d7-a230-3ee8d80d05c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd64b8367b33590b972adc2439af3a2479ee920e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309735"
---
# <a name="adding-a-component-to-a-visual-basic-project"></a><span data-ttu-id="891b0-103">Hinzufügen einer Komponente zu einem Visual Basic Projekt</span><span class="sxs-lookup"><span data-stu-id="891b0-103">Adding a Component to a Visual Basic Project</span></span>

<span data-ttu-id="891b0-104">Im folgenden Verfahren wird beschrieben, wie ein COM-Objekt als Komponente zu einem Visual Basic-Projekt hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="891b0-104">The following procedure describes how to add a COM object as a component to a Visual Basic project.</span></span> <span data-ttu-id="891b0-105">Die Anwendung kann dann die Klassen dieses Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="891b0-105">Your application can then use the classes of that object.</span></span>

<span data-ttu-id="891b0-106">Wenn Sie ein-Steuerelement als Komponente hinzufügen, werden die Eigenschaften und Methoden des Visual Basic Extender so verfügbar gemacht, als wären Sie Teil des Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="891b0-106">Adding a control as a component exposes the Visual Basic extender properties and methods as if they were part of the control.</span></span> <span data-ttu-id="891b0-107">Wenn Sie dagegen ein Objekt als Verweis hinzufügen, können Sie nur die Typbibliothek verwenden, die vom Steuerelement bereitgestellt wird, oder die Typbibliothek "RAW".</span><span class="sxs-lookup"><span data-stu-id="891b0-107">In contrast, when you add an object as a reference you can only use the type library provided by the control, or the "raw" type library.</span></span>

<span data-ttu-id="891b0-108">**So fügen Sie ein Steuerelement in ein Visual Basic Projekt ein**</span><span class="sxs-lookup"><span data-stu-id="891b0-108">**To insert a control into a Visual Basic project**</span></span>

1.  <span data-ttu-id="891b0-109">Klicken Sie im Menü **Projekt** auf **Komponenten**.</span><span class="sxs-lookup"><span data-stu-id="891b0-109">On the **Project** menu, click **Components**.</span></span>
2.  <span data-ttu-id="891b0-110">Aktivieren Sie das Kontrollkästchen neben der Komponente, die Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="891b0-110">Click to select the check box next to the component you want to add.</span></span> <span data-ttu-id="891b0-111">Wenn die Komponente nicht aufgelistet ist, suchen Sie die dll-oder OCX-Datei mithilfe von **Durchsuchen**.</span><span class="sxs-lookup"><span data-stu-id="891b0-111">If the component is not listed, locate the .dll or .ocx file using **Browse**.</span></span>
3.  <span data-ttu-id="891b0-112">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="891b0-112">Click **OK**.</span></span>

<span data-ttu-id="891b0-113">Die Komponente ist nun Teil des Projekts und wird in der Objekt Symbolleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="891b0-113">The component is now part of the project and appears in the object toolbar.</span></span> <span data-ttu-id="891b0-114">Die Anwendung kann Instanzen des Steuer Elements erstellen, indem Sie das Steuerelement von der Symbolleiste ziehen und in einem Formular oder Dialogfeld ablegen.</span><span class="sxs-lookup"><span data-stu-id="891b0-114">Your application can create instances of the control by dragging the control from the toolbar and dropping it onto a form or dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="891b0-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="891b0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="891b0-116">Hinzufügen eines Verweises auf ein Visual Basic Projekt</span><span class="sxs-lookup"><span data-stu-id="891b0-116">Adding a Reference to a Visual Basic Project</span></span>](adding-a-reference-to-a-visual-basic-project.md)
</dt> <dt>

[<span data-ttu-id="891b0-117">Übersetzen in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="891b0-117">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 




