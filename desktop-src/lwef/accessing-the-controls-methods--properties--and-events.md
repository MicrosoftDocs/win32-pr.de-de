---
title: Zugreifen auf die Steuerelemente Methoden, Eigenschaften und Ereignisse
description: Zugreifen auf die Steuerelemente Methoden, Eigenschaften und Ereignisse
ms.assetid: 70a3b011-0290-4df4-9b66-23b27bcb14e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750ad6280b521cf50c2ecd1fb7f1fcec3e2c4164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388240"
---
# <a name="accessing-the-controls-methods-properties-and-events"></a><span data-ttu-id="538e4-103">Zugreifen auf die Steuerelemente Methoden, Eigenschaften und Ereignisse</span><span class="sxs-lookup"><span data-stu-id="538e4-103">Accessing the Controls Methods, Properties, and Events</span></span>

<span data-ttu-id="538e4-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="538e4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="538e4-105">Die Verwendung des Steuer Elements von Microsoft-Agent mit Visual Basic ähnelt der Verwendung des Steuer Elements mit VBScript, mit dem Unterschied, dass Ereignisse in Visual Basic den Datentyp der bestandenen Parameter einschließen müssen.</span><span class="sxs-lookup"><span data-stu-id="538e4-105">Using Microsoft Agent's control with Visual Basic is very similar to using the control with VBScript, except that events in Visual Basic must include the data type of passed parameters.</span></span> <span data-ttu-id="538e4-106">Beim Hinzufügen des Microsoft-Agent-Steuer Elements zu einem Formular werden die Ereignisse des Microsoft-Agents automatisch mit den entsprechenden Parametern eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="538e4-106">Adding the Microsoft Agent control to a form will automatically include Microsoft Agent's events with their appropriate parameters.</span></span> <span data-ttu-id="538e4-107">Außerdem wird automatisch eine Verbindung mit dem Agentserver hergestellt, wenn die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="538e4-107">It will also automatically create a connection to the Agent server when the application runs.</span></span>

<span data-ttu-id="538e4-108">Möglicherweise können Sie auch die Objectes-Erstellungs Syntax Ihrer Programmiersprache verwenden, um zur Laufzeit eine Instanz des Steuer Elements zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="538e4-108">You may also be able to use your programming language's object's creation syntax to create an instance of the control at runtime.</span></span> <span data-ttu-id="538e4-109">Wenn Sie z. b. in Visual Basic (5,0 oder höher) das Microsoft-Agent 2,0-Steuerelement in die Verweise Ihres Projekts einschließen, können Sie [**mit-Ereignissen**](https://www.bing.com/search?q=**With+Events**)verwenden. [**Neue**](https://www.bing.com/search?q=**New**) Deklaration.</span><span class="sxs-lookup"><span data-stu-id="538e4-109">For example, in Visual Basic (5.0 or later), if you include the Microsoft Agent 2.0 Control in your project's references, you can use a [**With Events**](https://www.bing.com/search?q=**With+Events**)..[**New**](https://www.bing.com/search?q=**New**) declaration.</span></span> <span data-ttu-id="538e4-110">Wenn Sie den Verweis nicht einschließen, löst VB einen Fehler aus, der anzeigt, dass der Microsoft-Agent nicht gestartet werden konnte (Fehlercode 80042502).</span><span class="sxs-lookup"><span data-stu-id="538e4-110">If you do not include the reference, VB raises an error indicating that Microsoft Agent was unable to start (error code 80042502).</span></span>

``` syntax
   ' Declare a global variable for the control
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```

<span data-ttu-id="538e4-111">Für Versionen von VB vor 5,0 können Sie das VB [**New**](https://www.bing.com/search?q=**New**) -Schlüsselwort ohne [**wider Vents**](https://www.bing.com/search?q=**WithEvents**) -Deklaration oder die VB-Funktion von "detarateobject" verwenden, aber diese Konventionen machen die Ereignisse des Agent-Steuer Elements nicht verfügbar. [](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="538e4-111">For versions of VB prior to 5.0, you can use the VB [**New**](https://www.bing.com/search?q=**New**) keyword without [**WithEvents**](https://www.bing.com/search?q=**WithEvents**) declaration or the VB [**CreateObject**](https://msdn.microsoft.com/library/Bb545141(v=VS.85).aspx) function, but these conventions will not expose the Agent control's events.</span></span> <span data-ttu-id="538e4-112">Sie müssen auch die [**verbundene**](https://www.bing.com/search?q=**Connected**) -Eigenschaft verwenden, bevor Sie auf Agent-Methoden oder-Eigenschaften verweisen können.</span><span class="sxs-lookup"><span data-stu-id="538e4-112">You also need to use the [**Connected**](https://www.bing.com/search?q=**Connected**) property before you reference any Agent methods or properties.</span></span> <span data-ttu-id="538e4-113">Wenn dies nicht erfolgt, gibt VB einen Fehler aus, der anzeigt, dass der Microsoft-Agent nicht gestartet werden konnte (Fehlercode 80042502).</span><span class="sxs-lookup"><span data-stu-id="538e4-113">If this is not done, VB will raise an error indicating that Microsoft Agent was unable to start (error code 80042502).</span></span>

<span data-ttu-id="538e4-114">Ähnlich wie bei anderen Programmiersprachen müssen Sie möglicherweise die [**verbundene**](https://www.bing.com/search?q=**Connected**) -Eigenschaft verwenden, um eine Verbindung mit dem com-Server (Agent Component Object Model) herzustellen, bevor der Code eine der Methoden oder Eigenschaften des Agent-Steuer Elements abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="538e4-114">Similarly for other programming languages, you may have to use the [**Connected**](https://www.bing.com/search?q=**Connected**) property to establish a connection to the Agent Component Object Model (COM) server before your code can call any of the Agent control's methods or properties.</span></span> <span data-ttu-id="538e4-115">Außerdem können die Methoden und Eigenschaften des Agents für einige Programmiersprachen nicht direkt verfügbar gemacht werden, es sei denn, Sie deklarieren das agentsteuerelement mithilfe des Typs.</span><span class="sxs-lookup"><span data-stu-id="538e4-115">In addition, for some programming languages, Agent's methods and properties may not be directly exposed unless you declare the Agent control using its type.</span></span> <span data-ttu-id="538e4-116">Beispielsweise müssen Sie in Microsoft Access 97 das Objekt als Typ-Agent deklarieren, damit die Methoden und Eigenschaften im Dropdown Feld Member automatisch auflisten angezeigt werden, wenn Sie eingeben.</span><span class="sxs-lookup"><span data-stu-id="538e4-116">For example, in Microsoft Access 97, you will need to declare the object as type Agent to see the methods and properties display in the Auto List Members drop-down box when you type.</span></span>

<span data-ttu-id="538e4-117">Die meisten Programmiersprachen, die ActiveX-Steuerelemente unterstützen, folgen Konventionen wie Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="538e4-117">Most programming languages that support ActiveX controls follow conventions similar to Visual Basic.</span></span> <span data-ttu-id="538e4-118">Für Programmiersprachen, die keine Objekt Auflistungen unterstützen, können Sie mit der [**Zeichen**](https://www.bing.com/search?q=**Character**) Methode und der [**Befehls**](https://www.bing.com/search?q=**Command**) Methode auf Methoden und Eigenschaften von Elementen in der Auflistung zugreifen.</span><span class="sxs-lookup"><span data-stu-id="538e4-118">For programming languages that do not support object collections, you can use the [**Character**](https://www.bing.com/search?q=**Character**) method and [**Command**](https://www.bing.com/search?q=**Command**) method to access methods and properties of items in the collection.</span></span>

<span data-ttu-id="538e4-119">Programmiersprachen wie Visual Basic, die Zugriff auf die vom agentsteuerelement verfügbar gemachten Objekttypen ermöglichen, ermöglichen es Ihnen, diese in den Objekt Deklarationen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="538e4-119">Programming languages like Visual Basic, that provide access to the object types exposed by the Agent control, enable you to use these in your object declarations.</span></span> <span data-ttu-id="538e4-120">Anstatt ein Objekt als generischen Typ zu deklarieren, verwenden Sie z. b. Folgendes:</span><span class="sxs-lookup"><span data-stu-id="538e4-120">For example, instead of declaring an object as a generic type:</span></span>

``` syntax
   Dim Genie as Object
```

<span data-ttu-id="538e4-121">Sie können ein Objekt als bestimmten Typ deklarieren:</span><span class="sxs-lookup"><span data-stu-id="538e4-121">You can declare an object as a specific type:</span></span>

``` syntax
   Dim Genie as IAgentCtlCharacterEx
```

<span data-ttu-id="538e4-122">Dies kann die Gesamtleistung der Anwendung verbessern.</span><span class="sxs-lookup"><span data-stu-id="538e4-122">This may improve the overall performance of your application.</span></span>

<span data-ttu-id="538e4-123">Bei einigen Objekttypen finden Sie möglicherweise zwei Typen, die mit Ausnahme des Suffix "ex" identisch sind.</span><span class="sxs-lookup"><span data-stu-id="538e4-123">For some object types, you may find two types that are the same except for the "Ex" suffix.</span></span> <span data-ttu-id="538e4-124">Wenn beide vorhanden sind, verwenden Sie den Typ "ex", da dies die vollständige Funktionalität des-Agents bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="538e4-124">Where both exist, use the "Ex" type because this provides the full functionality of Agent.</span></span> <span data-ttu-id="538e4-125">Die nicht-"ex"-Entsprechungen sind nur aus Gründen der Abwärtskompatibilität enthalten.</span><span class="sxs-lookup"><span data-stu-id="538e4-125">The non-"Ex" counterparts are included only for backward compatibility.</span></span>

 

 




