---
title: Zeichen Objektmethoden
description: Zeichen Objektmethoden
ms.assetid: 0f926b7b-c1cf-4bd6-ba8c-1b2877eb1d24
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19bb0dbb256c99660cbce1613c9fdd27d85a92dc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948606"
---
# <a name="character-object-methods"></a><span data-ttu-id="33eee-103">Zeichen Objektmethoden</span><span class="sxs-lookup"><span data-stu-id="33eee-103">Character Object Methods</span></span>

<span data-ttu-id="33eee-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="33eee-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="33eee-105">Der Server macht auch Methoden für jedes Zeichen in einer [**Zeichen**](/windows/desktop/lwef/the-characters-object) Auflistung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="33eee-105">The server also exposes methods for each character in a [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span> <span data-ttu-id="33eee-106">Folgende Methoden werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="33eee-106">The following methods are supported:</span></span>

-   [<span data-ttu-id="33eee-107">**Aktivieren**</span><span class="sxs-lookup"><span data-stu-id="33eee-107">**Activate**</span></span>](activate-method.md)
-   [<span data-ttu-id="33eee-108">**Gestureat**</span><span class="sxs-lookup"><span data-stu-id="33eee-108">**GestureAt**</span></span>](gestureat-method.md)
-   [<span data-ttu-id="33eee-109">**Erhalten**</span><span class="sxs-lookup"><span data-stu-id="33eee-109">**Get**</span></span>](get-method.md)
-   [<span data-ttu-id="33eee-110">**Ausblenden**</span><span class="sxs-lookup"><span data-stu-id="33eee-110">**Hide**</span></span>](hide-method.md)
-   [<span data-ttu-id="33eee-111">**Interrupt**</span><span class="sxs-lookup"><span data-stu-id="33eee-111">**Interrupt**</span></span>](interrupt-method.md)
-   [<span data-ttu-id="33eee-112">**Lauschen**</span><span class="sxs-lookup"><span data-stu-id="33eee-112">**Listen**</span></span>](listen-method.md)
-   [<span data-ttu-id="33eee-113">**MoveTo**</span><span class="sxs-lookup"><span data-stu-id="33eee-113">**MoveTo**</span></span>](moveto-method.md)
-   [<span data-ttu-id="33eee-114">**Abspielen**</span><span class="sxs-lookup"><span data-stu-id="33eee-114">**Play**</span></span>](play-method.md)
-   [<span data-ttu-id="33eee-115">**Auftritt**</span><span class="sxs-lookup"><span data-stu-id="33eee-115">**Show**</span></span>](show-method.md)
-   [<span data-ttu-id="33eee-116">**ShowPopupMenu**</span><span class="sxs-lookup"><span data-stu-id="33eee-116">**ShowPopupMenu**</span></span>](showpopupmenu-method.md)
-   [<span data-ttu-id="33eee-117">**Speak**</span><span class="sxs-lookup"><span data-stu-id="33eee-117">**Speak**</span></span>](speak-method.md)
-   [<span data-ttu-id="33eee-118">**Stop**</span><span class="sxs-lookup"><span data-stu-id="33eee-118">**Stop**</span></span>](stop-method.md)
-   [<span data-ttu-id="33eee-119">**StopAll**</span><span class="sxs-lookup"><span data-stu-id="33eee-119">**StopAll**</span></span>](stopall-method.md)
-   [<span data-ttu-id="33eee-120">**Meiner**</span><span class="sxs-lookup"><span data-stu-id="33eee-120">**Think**</span></span>](think-method.md)
-   [<span data-ttu-id="33eee-121">**Wait**</span><span class="sxs-lookup"><span data-stu-id="33eee-121">**Wait**</span></span>](wait-method.md)

<span data-ttu-id="33eee-122">Um eine Methode zu verwenden, verweisen Sie auf das Zeichen in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="33eee-122">To use a method, reference the character in the collection.</span></span> <span data-ttu-id="33eee-123">In VBScript und Visual Basic müssen Sie dazu die ID für ein Zeichen angeben:</span><span class="sxs-lookup"><span data-stu-id="33eee-123">In VBScript and Visual Basic, you do this by specifying the ID for a character:</span></span>


```
   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Display the character
   Agent1.Characters("Genie").Show
   Agent1.Characters("Genie").Play "Greet"
   Agent1.Characters("Genie").Speak "Hello. "

   End Sub
```



<span data-ttu-id="33eee-124">Um die Syntax des Codes zu vereinfachen, können Sie eine Objekt Variable definieren und Sie so festlegen, dass Sie auf ein Zeichen Objekt in der [**Zeichen**](/windows/desktop/lwef/the-characters-object) Auflistung verweist. Anschließend können Sie die Variable verwenden, um auf Methoden oder Eigenschaften des Zeichens zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="33eee-124">To simplify the syntax of your code, you can define an object variable and set it to reference a character object in the [**Characters**](/windows/desktop/lwef/the-characters-object) collection; then you can use your variable to reference methods or properties of the character.</span></span> <span data-ttu-id="33eee-125">Im folgenden Beispiel wird veranschaulicht, wie Sie dies mit der Visual Basic Set-Anweisung erreichen können:</span><span class="sxs-lookup"><span data-stu-id="33eee-125">The following example demonstrates how you can do this using the Visual Basic Set statement:</span></span>


```
   'Define a global object variable
   Dim Genie as Object

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", " Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   'Get the Restpose animation
   Genie.Get "animation", "RestPose"

   'Make the character say Hello
   Genie.Speak "Hello."

   End Sub
```



<span data-ttu-id="33eee-126">In Visual Basic 5,0 können Sie auch den Verweis erstellen, indem Sie die Variable als [**Zeichen**](/windows/desktop/lwef/the-characters-object)Objekt deklarieren:</span><span class="sxs-lookup"><span data-stu-id="33eee-126">In Visual Basic 5.0, you can also create your reference by declaring your variable as a [**Character**](/windows/desktop/lwef/the-characters-object)object:</span></span>


```
   Dim Genie as IAgentCtlCharacterEx

   Sub FormLoad

   'Load the genie character into the Characters collection
   Agent1.Characters.Load "Genie", "Genie.acs"

   'Create a reference to the character
   Set Genie = Agent1.Characters("Genie")

   'Display the character
   Genie.Show

   End Sub
```



<span data-ttu-id="33eee-127">Durch das Deklarieren Ihres Objekts vom Typ iagentctlcharakteriex wird eine frühe Bindung für das Objekt ermöglicht, was zu einer besseren Leistung führt.</span><span class="sxs-lookup"><span data-stu-id="33eee-127">Declaring your object of type IAgentCtlCharacterEx enables early binding on the object, which results in better performance.</span></span>

<span data-ttu-id="33eee-128">In VBScript können Sie keinen Verweis als bestimmten Typ deklarieren.</span><span class="sxs-lookup"><span data-stu-id="33eee-128">In VBScript, you cannot declare a reference as a particular type.</span></span> <span data-ttu-id="33eee-129">Sie können jedoch einfach den Variablen Verweis deklarieren:</span><span class="sxs-lookup"><span data-stu-id="33eee-129">However, you can simply declare the variable reference:</span></span>


```
<SCRIPT LANGUAGE = "VBSCRIPT">
<!—--

   Dim Genie
   
   Sub window_OnLoad
   
   'Load the character
   AgentCtl.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   'Create an object reference to the character in the collection
   set Genie= AgentCtl.Characters ("Genie")

   'Get the Showing state animation
   Genie.Get "state", "Showing"

   'Display the character
   Genie.Show

   End Sub

-->
   </SCRIPT>
```



<span data-ttu-id="33eee-130">Einige Programmiersprachen unterstützen keine Auflistungen.</span><span class="sxs-lookup"><span data-stu-id="33eee-130">Some programming languages do not support collections.</span></span> <span data-ttu-id="33eee-131">Allerdings können Sie mit der [**Zeichen**](character-method.md) Methode auf die Methoden eines [**Zeichen**](/windows/desktop/lwef/the-characters-object) Objekts zugreifen:</span><span class="sxs-lookup"><span data-stu-id="33eee-131">However, you can access a [**Character**](/windows/desktop/lwef/the-characters-object) object's methods with the [**Character**](character-method.md) method:</span></span>


```
   agent.Characters.Character("CharacterID").method
```



<span data-ttu-id="33eee-132">Darüber hinaus können Sie auch einen Verweis auf das [**Zeichen**](/windows/desktop/lwef/the-characters-object) Objekt erstellen, damit der Skriptcode leichter befolgt werden kann:</span><span class="sxs-lookup"><span data-stu-id="33eee-132">In addition, you can also create a reference to the [**Character**](/windows/desktop/lwef/the-characters-object) object to make your script code easier to follow:</span></span>


```
<SCRIPT LANGUAGE="JScript" FOR="window" EVENT="onLoad()">
<!--
   
   //Load the character's data
   AgentCtl.Characters.Load ("Genie", _
      "https://agent.microsoft.com/characters/v2/genie/genie.acf");   

   //Create a reference to this object
   Genie = AgentCtl.Characters.Character("Genie");
   
   //Get the Showing state animation
   Genie.Get("state", "Showing");

   //Display the character
   Genie.Show();

-->
</SCRIPT>
```



 

 