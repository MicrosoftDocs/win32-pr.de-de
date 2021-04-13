---
title: Verbundene Eigenschaft
description: Verbundene Eigenschaft
ms.assetid: 61b7f550-d8d6-4719-a0d4-0bf3a8cf096c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bba78358c7c42f0754da017aa0c188d41acd189
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310584"
---
# <a name="connected-property"></a><span data-ttu-id="e69bf-103">Verbundene Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e69bf-103">Connected Property</span></span>

<span data-ttu-id="e69bf-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e69bf-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e69bf-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e69bf-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e69bf-106">Gibt zurück oder legt fest, ob das aktuelle Steuerelement mit dem Microsoft-Agent-Server verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="e69bf-106">Returns or sets whether the current control is connected to the Microsoft Agent server.</span></span>

</dd> <dt>

<span data-ttu-id="e69bf-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="e69bf-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e69bf-108">*Agent. \* \* \* verbunden* \*  \[  =  *boolescher* Wert\]</span><span class="sxs-lookup"><span data-stu-id="e69bf-108">*agent.\*\*\*Connected*\* \[ = *boolean*\]</span></span>



| <span data-ttu-id="e69bf-109">Teil</span><span class="sxs-lookup"><span data-stu-id="e69bf-109">Part</span></span>      | <span data-ttu-id="e69bf-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e69bf-110">Description</span></span>                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e69bf-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="e69bf-111">*boolean*</span></span> | <span data-ttu-id="e69bf-112">Ein boolescher Ausdruck, der angibt, ob das Steuerelement verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="e69bf-112">A Boolean expression specifying whether the control is connected.</span></span> <span data-ttu-id="e69bf-113">**True** Das Steuerelement ist verbunden.</span><span class="sxs-lookup"><span data-stu-id="e69bf-113">**True** The control is connected.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e69bf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e69bf-114">Remarks</span></span>

<span data-ttu-id="e69bf-115">In vielen Fällen wird durch das Angeben des Steuer Elements automatisch eine Verbindung mit dem Microsoft-Agent-Server hergestellt.</span><span class="sxs-lookup"><span data-stu-id="e69bf-115">In many situations, specifying the control automatically creates a connection with the Microsoft Agent server.</span></span> <span data-ttu-id="e69bf-116">Wenn Sie z. b. die CLSID des Microsoft-Agent-Steuer Elements im- <OBJECT> Tag einer Webseite angeben, wird automatisch eine Server Verbindung geöffnet, und das Beenden der Seite schließt die Verbindung.</span><span class="sxs-lookup"><span data-stu-id="e69bf-116">For example, specifying the Microsoft Agent control's CLSID in the <OBJECT> tag in a webpage automatically opens a server connection and exiting the page closes the connection.</span></span> <span data-ttu-id="e69bf-117">Ebenso wird bei Visual Basic oder anderen Sprachen, mit denen Sie ein Steuerelement auf einem Formular ablegen können, durch das Ausführen des Programms automatisch eine Verbindung geöffnet, und die Verbindung wird beendet.</span><span class="sxs-lookup"><span data-stu-id="e69bf-117">Similarly, for Visual Basic or other languages that enable you to drop a control on a form, running the program automatically opens a connection and exiting the program closes the connection.</span></span> <span data-ttu-id="e69bf-118">Wenn der Server zurzeit nicht ausgeführt wird, wird er automatisch gestartet.</span><span class="sxs-lookup"><span data-stu-id="e69bf-118">If the server isn't currently running, it automatically starts.</span></span>

<span data-ttu-id="e69bf-119">Wenn Sie jedoch ein agentsteuerelement zur Laufzeit erstellen möchten, müssen Sie möglicherweise auch explizit eine neue Verbindung mit dem Server mithilfe der **verbundenen** Eigenschaft öffnen.</span><span class="sxs-lookup"><span data-stu-id="e69bf-119">However, if you want to create an Agent control at run time, you may also need to explicitly open a new connection to the server using the **Connected** property.</span></span> <span data-ttu-id="e69bf-120">Beispielsweise können Sie in Visual Basic zur Laufzeit ein ActiveX-Objekt mit der Set-Anweisung mit dem **New** -Schlüsselwort (oder der Funktion "comateobject") erstellen.</span><span class="sxs-lookup"><span data-stu-id="e69bf-120">For example, in Visual Basic you can create an ActiveX object at run time using the Set statement with the **New** keyword (or CreateObject function).</span></span> <span data-ttu-id="e69bf-121">Obwohl das-Objekt erstellt wird, wird die Verbindung mit dem Server möglicherweise nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="e69bf-121">While this creates the object, it may not create the connection to the server.</span></span> <span data-ttu-id="e69bf-122">Sie können die **verbundene** Eigenschaft vor jedem beliebigen Code verwenden, der die Programmierschnittstelle des Microsoft-Agents aufruft, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="e69bf-122">You can use the **Connected** property before any code that calls into Microsoft Agent's programming interface, as shown in the following example:</span></span>


```
   ' Declare a global variable for the control
   Dim MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load a character
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Display the character
   MyAgent.Characters("Genie").Show
```



<span data-ttu-id="e69bf-123">Wenn Sie ein Steuerelement mit dieser Technik erstellen, werden die Ereignisse des Agent-Steuer Elements nicht verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="e69bf-123">Creating a control using this technique does not expose the Agent control's events.</span></span> <span data-ttu-id="e69bf-124">In Visual Basic 5,0 (und höher) können Sie auf die Ereignisse des-Steuer Elements zugreifen, indem Sie das-Steuerelement in die Verweise Ihres Projekts einschließen und das **widervents** -Schlüsselwort in der Variablen Deklaration verwenden:</span><span class="sxs-lookup"><span data-stu-id="e69bf-124">In Visual Basic 5.0 (and later), you can access the control's events by including the control in your project's references, and use the **WithEvents** keyword in your variable declaration:</span></span>


```
   Dim WithEvents MyAgent as Agent

   ' Create an instance of the control using New
   Set MyAgent = New Agent
```



<span data-ttu-id="e69bf-125">Durch die Verwendung von **wiwitvents** zum Erstellen einer Instanz des Agent-Steuer Elements zur Laufzeit wird die Verbindung mit dem Microsoft-Agent-Server automatisch geöffnet.</span><span class="sxs-lookup"><span data-stu-id="e69bf-125">Using **WithEvents** to create an instance of the Agent control at run time automatically opens the connection with the Microsoft Agent server.</span></span> <span data-ttu-id="e69bf-126">Daher müssen Sie keine **verbundene** Anweisung einschließen.</span><span class="sxs-lookup"><span data-stu-id="e69bf-126">Therefore, you don't need to include a **Connected** statement.</span></span>

<span data-ttu-id="e69bf-127">Sie können die Verbindung mit dem Server schließen, indem Sie alle von Ihnen erstellten Verweise auf-Agent-Objekte, z. b. iagentctlcharakteriex und iagentctlcommandex, freigeben.</span><span class="sxs-lookup"><span data-stu-id="e69bf-127">You can close your connection to the server by releasing all references you created to Agent objects, such as IAgentCtlCharacterEx and IAgentCtlCommandEx.</span></span> <span data-ttu-id="e69bf-128">Sie müssen auch den Verweis auf das agentsteuerelement selbst freigeben.</span><span class="sxs-lookup"><span data-stu-id="e69bf-128">You must also release your reference to the Agent control itself.</span></span> <span data-ttu-id="e69bf-129">In Visual Basic können Sie einen Verweis auf ein Objekt freigeben, indem Sie die Variable auf " **Nothing**" festlegen.</span><span class="sxs-lookup"><span data-stu-id="e69bf-129">In Visual Basic, you can release a reference to an object by setting its variable to **Nothing**.</span></span> <span data-ttu-id="e69bf-130">Wenn Sie Zeichen geladen haben, entladen Sie diese, bevor Sie das Zeichen Objekt freigeben.</span><span class="sxs-lookup"><span data-stu-id="e69bf-130">If you have loaded characters, unload them before releasing the character object.</span></span>


```
   Dim WithEvents MyAgent as Agent
   Dim Genie as IAgentCtlCharacterEx
   
   Sub Form_Load

   ' Create an instance of the control using New
   Set MyAgent = New Agent

   ' Open a connection to the server
   MyAgent.Connected = True

   ' Load the character into the Characters collection
   MyAgent.Characters.Load "Genie", " Genie.acs"

   ' Create a reference to the character
   Set Genie = MyAgent.Characters("Genie")

   End Sub

   Sub CloseConnection

   ' Unload the character
   MyAgent.Characters.Unload "Genie"

   ' Release the reference to the character object
   Set Genie = Nothing

   ' Release the reference to the Agent control
   Set MyAgent = Nothing
   End Sub
```



> [!Note]  
> <span data-ttu-id="e69bf-131">Sie können die Verbindung mit dem Server nicht schließen, indem Sie Verweise freigeben, bei denen die Komponente hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="e69bf-131">You cannot close your connection to the server by releasing references where the component has been added.</span></span> <span data-ttu-id="e69bf-132">Beispielsweise können Sie die Verbindung mit dem Server auf Webseiten nicht schließen, auf dem Sie das- <OBJECT> Tag verwenden, um das Steuerelement zu deklarieren, oder in einer Visual Basic Anwendung, in der Sie das Steuerelement in einem Formular ablegen.</span><span class="sxs-lookup"><span data-stu-id="e69bf-132">For example, you cannot close your connection to the server on webpages where you use the <OBJECT> tag to declare the control or in a Visual Basic application where you drop the control on a form.</span></span> <span data-ttu-id="e69bf-133">Wenn alle agentverweise freigegeben werden, wird die Arbeitsgruppe des Agents reduziert. die Verbindung bleibt so lange erhalten, bis Sie zur nächsten Seite navigieren oder die Anwendung beenden.</span><span class="sxs-lookup"><span data-stu-id="e69bf-133">While releasing all Agent references will reduce Agent's working set, the connection remains until you navigate to the next page or exit the application.</span></span>

 

 

 





