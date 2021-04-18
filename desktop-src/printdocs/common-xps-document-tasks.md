---
description: Auf dieser Seite werden einige der Programmieraufgaben aufgelistet, die häufig mit der XPS-Dokument-API ausgeführt werden.
ms.assetid: ced2098f-5462-40d7-a728-4e53f7f41003
title: Allgemeine XPS-Dokument Programmierungsaufgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92c40ee0c901b9d906d4d59c69bab4cfc22d8208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347352"
---
# <a name="common-xps-document-programming-tasks"></a><span data-ttu-id="70e62-103">Allgemeine XPS-Dokument Programmierungsaufgaben</span><span class="sxs-lookup"><span data-stu-id="70e62-103">Common XPS Document Programming Tasks</span></span>

<span data-ttu-id="70e62-104">Auf dieser Seite werden einige der Programmieraufgaben aufgelistet, die häufig mit der XPS-Dokument-API ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="70e62-104">This page lists some of the programming tasks that are commonly performed with the XPS Document API.</span></span>

## <a name="common-xps-document-tasks"></a><span data-ttu-id="70e62-105">Allgemeine XPS-Dokument Aufgaben</span><span class="sxs-lookup"><span data-stu-id="70e62-105">Common XPS Document Tasks</span></span>

<span data-ttu-id="70e62-106">Die folgenden Codebeispiele veranschaulichen einige der Programmieraufgaben, die häufig ausgeführt werden, wenn die XPS-Dokument-API zum Arbeiten mit einem XPS-OM verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="70e62-106">The following code examples illustrate some of the programming tasks that are commonly performed when the XPS Document API is used for working with an XPS OM.</span></span>

<dl>

[<span data-ttu-id="70e62-107">Initialisieren eines XPS-OMS</span><span class="sxs-lookup"><span data-stu-id="70e62-107">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)  
[<span data-ttu-id="70e62-108">Erstellen eines leeren XPS-OMS</span><span class="sxs-lookup"><span data-stu-id="70e62-108">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)  
[<span data-ttu-id="70e62-109">Lesen eines XPS-Dokuments in ein XPS-OM</span><span class="sxs-lookup"><span data-stu-id="70e62-109">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)  
[<span data-ttu-id="70e62-110">Navigieren im XPS-OM</span><span class="sxs-lookup"><span data-stu-id="70e62-110">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)  
[<span data-ttu-id="70e62-111">Schreiben von Text in ein XPS-OM</span><span class="sxs-lookup"><span data-stu-id="70e62-111">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)  
[<span data-ttu-id="70e62-112">Zeichnen von Grafiken in einem XPS-OM</span><span class="sxs-lookup"><span data-stu-id="70e62-112">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)  
[<span data-ttu-id="70e62-113">Platzieren von Bildern in einem XPS-OM</span><span class="sxs-lookup"><span data-stu-id="70e62-113">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)  
[<span data-ttu-id="70e62-114">Schreiben eines XPS-om in ein XPS-Dokument</span><span class="sxs-lookup"><span data-stu-id="70e62-114">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)  
[<span data-ttu-id="70e62-115">Drucken eines XPS-OM</span><span class="sxs-lookup"><span data-stu-id="70e62-115">Print an XPS OM</span></span>](print-an-xps-om.md)  
[<span data-ttu-id="70e62-116">Arbeiten mit XPS OM-Sammlungs Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="70e62-116">Working with XPS OM Collection Interfaces</span></span>](working-with-xps-object-model-collection-interfaces.md)  
</dl>

## <a name="disclaimer"></a><span data-ttu-id="70e62-117">Haftungsausschluss</span><span class="sxs-lookup"><span data-stu-id="70e62-117">Disclaimer</span></span>

<span data-ttu-id="70e62-118">Code Beispiele sind nicht als komplett und funktionierende Programme gedacht.</span><span class="sxs-lookup"><span data-stu-id="70e62-118">Code examples are not intended to be complete and working programs.</span></span> <span data-ttu-id="70e62-119">In den Codebeispielen, die auf dieser Seite referenziert werden, wird z. b. keine Parameter Überprüfung, Fehlerüberprüfung oder Fehlerbehandlung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="70e62-119">The code examples that are referenced on this page, for example, do not perform parameter checking, error checking, or error handling.</span></span> <span data-ttu-id="70e62-120">Verwenden Sie diese Beispiele als Ausgangspunkt, und fügen Sie dann den Code hinzu, der erforderlich ist, um eine robuste Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="70e62-120">Use these examples as a starting point, and then add the code necessary to create a robust application.</span></span> <span data-ttu-id="70e62-121">Weitere Informationen zu den **HRESULT** -Rückgabe Werten und Fehlerbehandlungsstrategien finden Sie unter [Fehlerbehandlung in com](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="70e62-121">For more information about **HRESULT** return values and error handling strategies, see [Error Handling in COM](../com/error-handling-in-com.md).</span></span>

<span data-ttu-id="70e62-122">Bevor XPS OM-Schnittstellen verwendet werden können, muss com im Thread initialisiert werden, wie im folgenden Beispielcode gezeigt.</span><span class="sxs-lookup"><span data-stu-id="70e62-122">Before XPS OM interfaces can be used, COM must be initialized in the thread, as shown in the following example code.</span></span>


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



<span data-ttu-id="70e62-123">Aus Gründen der Übersichtlichkeit verwenden diese Codebeispiele ein sehr einfaches XPS-OM, das möglicherweise nicht komplex genug für Ihre Anwendung ist.</span><span class="sxs-lookup"><span data-stu-id="70e62-123">For clarity, these code examples use a very simple XPS OM, one that might not be complex enough for your application.</span></span> <span data-ttu-id="70e62-124">In den Codebeispielen, die Inhalte zu einer Seite hinzufügen, werden die visuellen Elemente einer Seite in einem Fall direkt der Liste der visuellen Objekte der Seite hinzugefügt. in der Praxis möchten Sie jedoch möglicherweise visuelle Objekte in Canvas-Objekte gruppieren, sodass mehrere Objekte als Gruppe behandelt werden könnten.</span><span class="sxs-lookup"><span data-stu-id="70e62-124">As a case in point, in the code examples that add content to a page, the visual elements of a page are added directly to the page's list of visual objects; in practice, however, you might want to group visual objects into canvas objects, so that multiple objects could be acted upon as a group.</span></span> <span data-ttu-id="70e62-125">Um die Unterstützung desselben Inhalts für mehr als eine Seitengröße zu aktivieren, können Sie daher den visuellen Inhalt einer Seite in einem einzelnen Canvas-Objekt gruppieren und dann eine Transformation auf den Zeichenbereich anwenden, um ihn auf die aktuelle Seitengröße zu skalieren.</span><span class="sxs-lookup"><span data-stu-id="70e62-125">Thus, to enable support of the same content for more than one page size, you could group the visual content of a page into a single canvas object, and then apply a transform to the canvas to scale it to the current page size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70e62-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="70e62-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70e62-127">Fehlerbehandlung in com</span><span class="sxs-lookup"><span data-stu-id="70e62-127">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> <dt>

[<span data-ttu-id="70e62-128">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="70e62-128">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
