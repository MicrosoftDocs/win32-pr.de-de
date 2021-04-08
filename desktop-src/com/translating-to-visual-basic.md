---
title: Übersetzen in Visual Basic
description: Übersetzen in Visual Basic
ms.assetid: 48672d0c-b0d7-4820-91d4-d985030396f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c45e7beedaaa3983b1be1503b5ce443a3adf4d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856400"
---
# <a name="translating-to-visual-basic"></a><span data-ttu-id="0c2eb-103">Übersetzen in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="0c2eb-103">Translating to Visual Basic</span></span>

<span data-ttu-id="0c2eb-104">Sie können Ihrem Visual Basic Projekt ein COM-Objekt als Verweis oder Komponente hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-104">You can add a COM object to your Visual Basic project either as a reference or a component.</span></span> <span data-ttu-id="0c2eb-105">Nachdem das Objekt dem Projekt hinzugefügt wurde, kann die Anwendung auf die Klassen und Schnittstellen zugreifen.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-105">Once the object is added to your project, your application can access its classes and interfaces.</span></span> <span data-ttu-id="0c2eb-106">Sie können dann die Visual Basic Objektkatalog verwenden, um die Typbibliotheks Informationen des Objekts in Visual Basic Syntax anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-106">You can then use the Visual Basic Object Browser to view the object's type library information in Visual Basic syntax.</span></span>

<span data-ttu-id="0c2eb-107">Normalerweise werden Steuerelemente zu einem Projekt hinzugefügt, da eine Komponente und nicht-Steuerelemente als Verweise hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-107">Typically, controls are added to a project as a components and noncontrols are added as references.</span></span> <span data-ttu-id="0c2eb-108">Wenn ein COM-Objekt als Komponente hinzugefügt wird, wird es in der Visual Basic Toolbox angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-108">When a COM object is added as a component, it appears in the Visual Basic toolbox.</span></span> <span data-ttu-id="0c2eb-109">Neue Instanzen dieses Objekts werden erstellt, indem das Objekt Symbol aus der Toolbox auf ein Visual Basic Formular oder einen anderen Containertyp gezogen wird.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-109">New instances of that object are created by dragging the object icon from the toolbox onto a Visual Basic form or other type of container.</span></span> <span data-ttu-id="0c2eb-110">Neue Instanzen von COM-Objekten, die als Verweise hinzugefügt werden, werden mithilfe des Schlüssel Worts **New** erstellt.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-110">New instances of COM objects added as references are created using the **new** keyword.</span></span>

<span data-ttu-id="0c2eb-111">Der Unterschied zwischen der Verwendung einer Klasse als Verweis im Vergleich zu einer Komponente ist sehr gering, aber wichtig.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-111">The distinction between using a class as a reference versus a component is subtle but important.</span></span> <span data-ttu-id="0c2eb-112">Wenn Sie ein Objekt als Verweis hinzufügen, können Sie nur die Typbibliothek verwenden, die das Steuerelement bereitstellt, oder die Typbibliothek "RAW".</span><span class="sxs-lookup"><span data-stu-id="0c2eb-112">When you add an object as a reference, you can use only the type library that the control provides, or the "raw" type library.</span></span>

<span data-ttu-id="0c2eb-113">Wenn Sie ein-Steuerelement als Komponente hinzufügen Visual Basic werden die Extendereigenschaften und-Methoden der Form, in der das Steuerelement mit der Typbibliothek des Steuer Elements eingebettet ist, zusammengeführt und somit eine umschließende erweiterte Version der Typbibliothek bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-113">If you add a control as a component, Visual Basic merges the extender properties and methods of the form in which the control is embedded with the control's type library, thus providing a wrapped, extended version of the type library.</span></span> <span data-ttu-id="0c2eb-114">Mit dieser Version der Typbibliothek können Sie Extender-Eigenschaften wie z. b. Top und Left verwenden, als wären Sie Teil des-Steuer Elements, anstatt den Container des Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-114">With this version of the type library, you can use extender properties such as Top and Left as if they were part of the control, instead of the control's container.</span></span>

<span data-ttu-id="0c2eb-115">Visual Basic unterstützt derzeit nicht mehrere Typbibliotheken, die in eine einzelne DLL-Datei integriert sind.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-115">Visual Basic does not currently support multiple type libraries built into a single .dll file.</span></span> <span data-ttu-id="0c2eb-116">Wenn Sie eine DLL-Datei ausführen, die mehrere Typbibliotheken umfasst, sollten Sie eigenständige Kopien der Typbibliotheken von der Quelle erhalten, von der das Objekt bereitgestellt wurde, um das Objekt mit Visual Basic zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0c2eb-116">If you run into a DLL that incorporates multiple type libraries, you should get stand-alone copies of the type libraries from the source that supplied the object in order to use the object with Visual Basic.</span></span>

<span data-ttu-id="0c2eb-117">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="0c2eb-117">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="0c2eb-118">Übersetzen in Visual Basic von C++</span><span class="sxs-lookup"><span data-stu-id="0c2eb-118">Translating to Visual Basic from C++</span></span>](translating-to-visual-basic-from-c--.md)
-   [<span data-ttu-id="0c2eb-119">Übersetzen in Visual Basic aus Java</span><span class="sxs-lookup"><span data-stu-id="0c2eb-119">Translating to Visual Basic from Java</span></span>](translating-to-visual-basic-from-java.md)
-   [<span data-ttu-id="0c2eb-120">Hinzufügen einer Komponente zu einem Visual Basic Projekt</span><span class="sxs-lookup"><span data-stu-id="0c2eb-120">Adding a Component to a Visual Basic Project</span></span>](adding-a-component-to-a-visual-basic-project.md)
-   [<span data-ttu-id="0c2eb-121">Hinzufügen eines Verweises auf ein Visual Basic Projekt</span><span class="sxs-lookup"><span data-stu-id="0c2eb-121">Adding a Reference to a Visual Basic Project</span></span>](adding-a-reference-to-a-visual-basic-project.md)
-   [<span data-ttu-id="0c2eb-122">Visual Basic Objektkatalog</span><span class="sxs-lookup"><span data-stu-id="0c2eb-122">Visual Basic Object Browser</span></span>](visual-basic-object-browser.md)

## <a name="related-topics"></a><span data-ttu-id="0c2eb-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0c2eb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c2eb-124">Übersetzen in C++</span><span class="sxs-lookup"><span data-stu-id="0c2eb-124">Translating to C++</span></span>](translating-to-c--.md)
</dt> <dt>

[<span data-ttu-id="0c2eb-125">Übersetzen in Java</span><span class="sxs-lookup"><span data-stu-id="0c2eb-125">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




