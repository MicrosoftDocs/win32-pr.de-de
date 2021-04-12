---
title: Hinzufügen eines Verweises auf ein Visual Basic Projekt
description: Hinzufügen eines Verweises auf ein Visual Basic Projekt
ms.assetid: 635b1fe9-e592-42d7-a0ee-34fea205f412
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b29b99610464287f34e9c78e44319c16b4d47c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309732"
---
# <a name="adding-a-reference-to-a-visual-basic-project"></a><span data-ttu-id="f2059-103">Hinzufügen eines Verweises auf ein Visual Basic Projekt</span><span class="sxs-lookup"><span data-stu-id="f2059-103">Adding a Reference to a Visual Basic Project</span></span>

<span data-ttu-id="f2059-104">Im folgenden Verfahren wird beschrieben, wie einem Visual Basic Projekt ein Verweis auf ein COM-Objekt hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f2059-104">The following procedure describes how to add a reference to a COM object to a Visual Basic project.</span></span> <span data-ttu-id="f2059-105">Die Anwendung kann dann die Klassen dieses Objekts verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2059-105">Your application can then use the classes of that object.</span></span>

<span data-ttu-id="f2059-106">Wenn Sie ein Objekt als Verweis hinzufügen, können Sie nur die Typbibliothek verwenden, die vom Steuerelement bereitgestellt wird, oder die Typbibliothek "RAW".</span><span class="sxs-lookup"><span data-stu-id="f2059-106">When you add an object as a reference, you can only use the type library provided by the control, or the "raw" type library.</span></span> <span data-ttu-id="f2059-107">Im Gegensatz dazu macht das Hinzufügen eines-Steuer Elements als Komponente auch die Visual Basic Extender-Eigenschaften und-Methoden verfügbar, als wären Sie Teil des-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="f2059-107">In contrast, adding a control as a component also exposes the Visual Basic extender properties and methods as if they were part of the control.</span></span>

<span data-ttu-id="f2059-108">**So erstellen Sie einen Visual Basic Verweis auf eine Komponente**</span><span class="sxs-lookup"><span data-stu-id="f2059-108">**To make a Visual Basic reference to a component**</span></span>

1.  <span data-ttu-id="f2059-109">Klicken Sie im Menü **Projekt** auf **Verweise**.</span><span class="sxs-lookup"><span data-stu-id="f2059-109">On the **Project** menu, click **References**.</span></span>
2.  <span data-ttu-id="f2059-110">Aktivieren Sie das Kontrollkästchen neben der Komponente, die Sie hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="f2059-110">Click to select the check box next to the component you want to add.</span></span> <span data-ttu-id="f2059-111">Wenn die Komponente nicht aufgelistet ist, suchen Sie die dll-oder OCX-Datei mithilfe von **Durchsuchen**.</span><span class="sxs-lookup"><span data-stu-id="f2059-111">If the component is not listed, locate the .dll or .ocx file using **Browse**.</span></span>
3.  <span data-ttu-id="f2059-112">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="f2059-112">Click **OK**.</span></span>

<span data-ttu-id="f2059-113">Die Komponente ist nun Teil des Projekts.</span><span class="sxs-lookup"><span data-stu-id="f2059-113">The component is now part of the project.</span></span> <span data-ttu-id="f2059-114">Die Anwendung kann mit dem **New** -Schlüsselwort Klassen Instanzen erstellen.</span><span class="sxs-lookup"><span data-stu-id="f2059-114">Your application can create class instances using the **New** keyword.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2059-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2059-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2059-116">Hinzufügen einer Komponente zu einem Visual Basic Projekt</span><span class="sxs-lookup"><span data-stu-id="f2059-116">Adding a Component to a Visual Basic Project</span></span>](adding-a-component-to-a-visual-basic-project.md)
</dt> <dt>

[<span data-ttu-id="f2059-117">Übersetzen in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f2059-117">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 




