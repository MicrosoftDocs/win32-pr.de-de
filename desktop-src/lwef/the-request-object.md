---
title: Das Anforderungs Objekt.
description: Das Anforderungs Objekt.
ms.assetid: d8b37164-6855-48c0-bcf8-a86c0f8b3a59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a50d554a5799af9a434b456113d7c826d2a0aa2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337219"
---
# <a name="the-request-object"></a><span data-ttu-id="fdc74-103">Das Anforderungs Objekt.</span><span class="sxs-lookup"><span data-stu-id="fdc74-103">The Request Object</span></span>

<span data-ttu-id="fdc74-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="fdc74-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="fdc74-105">Der Server verarbeitet einige Methoden asynchron.</span><span class="sxs-lookup"><span data-stu-id="fdc74-105">The server processes some methods asynchronously.</span></span> <span data-ttu-id="fdc74-106">Dadurch kann der Anwendungscode fortgesetzt werden, während die Methode abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="fdc74-106">This enables your application code to continue while the method is completing.</span></span> <span data-ttu-id="fdc74-107">Wenn eine Client Anwendung eine dieser Methoden aufruft, erstellt und gibt das-Steuerelement ein [**Request**](/windows/desktop/lwef/the-request-object) -Objekt für die Anforderung zurück.</span><span class="sxs-lookup"><span data-stu-id="fdc74-107">When a client application calls one of these methods, the control creates and returns a [**Request**](/windows/desktop/lwef/the-request-object) object for the request.</span></span> <span data-ttu-id="fdc74-108">Sie können das **Request** -Objekt verwenden, um den Status der Methode zu verfolgen, indem Sie der-Methode eine Objekt Variable zuweisen.</span><span class="sxs-lookup"><span data-stu-id="fdc74-108">You can use the **Request** object to track the status of the method by assigning an object variable to the method.</span></span> <span data-ttu-id="fdc74-109">Deklarieren Sie in Visual Basic zuerst eine Objekt Variable:</span><span class="sxs-lookup"><span data-stu-id="fdc74-109">In Visual Basic, first declare an object variable:</span></span>


```
   Dim MyRequest as Object
```



<span data-ttu-id="fdc74-110">In VBScript schließen Sie den Variablentyp nicht in die Deklaration ein:</span><span class="sxs-lookup"><span data-stu-id="fdc74-110">In VBScript, you don't include the variable type in your declaration:</span></span>


```
   Dim MyRequest
```



<span data-ttu-id="fdc74-111">Und verwenden die Set-Anweisung von Visual Basic, um die Variable dem Methoden aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="fdc74-111">And use Visual Basic's Set statement to assign the variable to the method call:</span></span>


```
   Set MyRequest = <i>agent</i>.Characters("<i>CharacterID</i>").<i>method</i> (<i>parameter</i>[s])
```



<span data-ttu-id="fdc74-112">Dadurch wird ein Verweis auf das [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="fdc74-112">This adds a reference to the [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="fdc74-113">Das **Anforderungs** Objekt wird zerstört, wenn keine weiteren Verweise darauf vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="fdc74-113">The **Request** object will be destroyed when there are no more references to it.</span></span> <span data-ttu-id="fdc74-114">Wo Sie das **Anforderungs** Objekt deklarieren und wie Sie es verwenden, legt seine Lebensdauer fest.</span><span class="sxs-lookup"><span data-stu-id="fdc74-114">Where you declare the **Request** object and how you use it determines its lifetime.</span></span> <span data-ttu-id="fdc74-115">Wenn das Objekt in einer Unterroutine oder Funktion als lokal deklariert ist, wird es zerstört, wenn es den Gültigkeitsbereich verlässt. Das heißt, wenn die Unterroutine oder Funktion beendet wird.</span><span class="sxs-lookup"><span data-stu-id="fdc74-115">If the object is declared local to a subroutine or function, it will be destroyed when it goes out of scope; that is, when the subroutine or function ends.</span></span> <span data-ttu-id="fdc74-116">Wenn das Objekt global deklariert ist, wird es erst zerstört, wenn das Programm beendet wird oder ein neuer Wert (oder ein als "leer" festgelegter Wert) dem Objekt zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="fdc74-116">If the object is declared globally, it will not be destroyed until either the program terminates or a new value (or a value set to "empty") is assigned to the object.</span></span>

<span data-ttu-id="fdc74-117">Das [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt bietet verschiedene Eigenschaften, die Sie Abfragen können.</span><span class="sxs-lookup"><span data-stu-id="fdc74-117">The [**Request**](/windows/desktop/lwef/the-request-object) object provides several properties you can query.</span></span> <span data-ttu-id="fdc74-118">Die [**Status**](status-property.md) -Eigenschaft gibt beispielsweise den aktuellen Status der Anforderung zurück.</span><span class="sxs-lookup"><span data-stu-id="fdc74-118">For example, the [**Status**](status-property.md) property returns the current status of the request.</span></span> <span data-ttu-id="fdc74-119">Sie können diese Eigenschaft verwenden, um den Status Ihrer Anforderung zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="fdc74-119">You can use this property to check the status of your request:</span></span>


```
   Dim MyRequest
   
   Set MyRequest = Agent1.Characters.Load ("Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf")

   If (MyRequest.Status = 2) then
      'do something

   Else If (MyRequest.Status = 0) then
      'do something right away

   End If
```



<span data-ttu-id="fdc74-120">Die [**Status**](status-property.md) -Eigenschaft gibt den Status eines [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekts als Long Integer-Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fdc74-120">The [**Status**](status-property.md) property returns the status of a [**Request**](/windows/desktop/lwef/the-request-object) object as a Long integer value.</span></span>



| <span data-ttu-id="fdc74-121">Status</span><span class="sxs-lookup"><span data-stu-id="fdc74-121">Status</span></span> | <span data-ttu-id="fdc74-122">Definition</span><span class="sxs-lookup"><span data-stu-id="fdc74-122">Definition</span></span>                                        |
|--------|---------------------------------------------------|
| <span data-ttu-id="fdc74-123">0</span><span class="sxs-lookup"><span data-stu-id="fdc74-123">0</span></span>      | <span data-ttu-id="fdc74-124">Die Anforderung wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="fdc74-124">Request successfully completed.</span></span>                   |
| <span data-ttu-id="fdc74-125">1</span><span class="sxs-lookup"><span data-stu-id="fdc74-125">1</span></span>      | <span data-ttu-id="fdc74-126">Fehler bei der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="fdc74-126">Request failed.</span></span>                                   |
| <span data-ttu-id="fdc74-127">2</span><span class="sxs-lookup"><span data-stu-id="fdc74-127">2</span></span>      | <span data-ttu-id="fdc74-128">Ausstehende Anforderung (in der Warteschlange, aber nicht abgeschlossen).</span><span class="sxs-lookup"><span data-stu-id="fdc74-128">Request pending (in the queue, but not complete).</span></span> |
| <span data-ttu-id="fdc74-129">3</span><span class="sxs-lookup"><span data-stu-id="fdc74-129">3</span></span>      | <span data-ttu-id="fdc74-130">Die Anforderung wurde unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="fdc74-130">Request interrupted.</span></span>                              |
| <span data-ttu-id="fdc74-131">4</span><span class="sxs-lookup"><span data-stu-id="fdc74-131">4</span></span>      | <span data-ttu-id="fdc74-132">Die Anforderung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fdc74-132">Request in progress.</span></span>                              |



 

<span data-ttu-id="fdc74-133">Das [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt enthält außerdem einen Long Integer-Wert in der [**Number**](https://www.bing.com/search?q=**Number**) -Eigenschaft, der den Fehler oder die Ursache des [**Status**](status-property.md) Codes zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fdc74-133">The [**Request**](/windows/desktop/lwef/the-request-object) object also includes a Long integer value in the [**Number**](https://www.bing.com/search?q=**Number**) property that returns the error or cause of the [**Status**](status-property.md) code.</span></span> <span data-ttu-id="fdc74-134">Wenn kein Wert ist, ist dieser Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fdc74-134">If none, this value is zero (0).</span></span> <span data-ttu-id="fdc74-135">Die [**Description**](description-property.md) -Eigenschaft enthält einen Zeichen folgen Wert, der der Fehlernummer entspricht.</span><span class="sxs-lookup"><span data-stu-id="fdc74-135">The [**Description**](description-property.md) property contains a string value that corresponds to the error number.</span></span> <span data-ttu-id="fdc74-136">Wenn die Zeichenfolge nicht vorhanden ist, enthält die **Beschreibung** "Anwendungs-oder Objekt definierter Fehler".</span><span class="sxs-lookup"><span data-stu-id="fdc74-136">If the string doesn't exist, **Description** contains "Application-defined or object-defined error".</span></span>

<span data-ttu-id="fdc74-137">Informationen zu den Werten und der von der [**Number**](https://www.bing.com/search?q=**Number**) -Eigenschaft zurückgegebenen Bedeutung finden Sie unter [Error Codes](microsoft-agent-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="fdc74-137">For the values and meaning returned by the [**Number**](https://www.bing.com/search?q=**Number**) property, see [Error Codes](microsoft-agent-error-codes.md).</span></span>

<span data-ttu-id="fdc74-138">Der Server platziert Animations Anforderungen in der Warteschlange des angegebenen Zeichens.</span><span class="sxs-lookup"><span data-stu-id="fdc74-138">The server places animation requests in the specified character's queue.</span></span> <span data-ttu-id="fdc74-139">Dadurch kann der Server die Animation in einem separaten Thread wiedergeben, und der Code der Anwendung kann fortgesetzt werden, während Animationen wiedergegeben werden.</span><span class="sxs-lookup"><span data-stu-id="fdc74-139">This enables the server to play the animation on a separate thread, and your application's code can continue while animations play.</span></span> <span data-ttu-id="fdc74-140">Wenn Sie einen [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt Verweis erstellen, benachrichtigt der Server Sie automatisch, wenn eine Animations Anforderung durch das [**requeststart**](https://www.bing.com/search?q=**RequestStart**) -Ereignis und das [**requestcomplete**](https://www.bing.com/search?q=**RequestComplete**) -Ereignis gestartet oder abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="fdc74-140">If you create a [**Request**](/windows/desktop/lwef/the-request-object) object reference, the server automatically notifies you when an animation request has started or completed through the [**RequestStart**](https://www.bing.com/search?q=**RequestStart**) and [**RequestComplete**](https://www.bing.com/search?q=**RequestComplete**) events.</span></span> <span data-ttu-id="fdc74-141">Da Methoden, die **Anforderungs** Objekte zurückgeben, asynchron sind und während des Gültigkeits Bereichs der aufrufenden Funktion möglicherweise nicht vervollständigt werden, deklarieren Sie den Verweis auf das **Anforderungs** Objekt Global.</span><span class="sxs-lookup"><span data-stu-id="fdc74-141">Because methods that return **Request** objects are asynchronous and may not complete during the scope of the calling function, declare your reference to the **Request** object globally.</span></span>

<span data-ttu-id="fdc74-142">Die folgenden Methoden können verwendet werden, um ein [**Anforderungs**](/windows/desktop/lwef/the-request-object) Objekt zurückzugeben: [**gestureat**](gestureat-method.md), [**Get**](get-method.md), [**Hide**](hide-method.md), [**Interrupt**](interrupt-method.md), [**Load**](load-method.md), [**muveto**](moveto-method.md), [**Play**](play-method.md), [**Show**](show-method.md), [**Speak**](speak-method.md)und [**Wait**](https://www.bing.com/search?q=**Wait**).</span><span class="sxs-lookup"><span data-stu-id="fdc74-142">The following methods can be used to return a [**Request**](/windows/desktop/lwef/the-request-object) object: [**GestureAt**](gestureat-method.md), [**Get**](get-method.md), [**Hide**](hide-method.md), [**Interrupt**](interrupt-method.md), [**Load**](load-method.md), [**MoveTo**](moveto-method.md), [**Play**](play-method.md), [**Show**](show-method.md), [**Speak**](speak-method.md), and [**Wait**](https://www.bing.com/search?q=**Wait**).</span></span>

 

 