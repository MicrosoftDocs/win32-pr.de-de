---
title: Methode hinzufügen
description: Methode hinzufügen
ms.assetid: dd258294-33d6-45f5-a6a1-a3a56b12a7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4527dec6014c93bb02b4f080e032266ea40159e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036850"
---
# <a name="add-method"></a><span data-ttu-id="d496e-103">Methode hinzufügen</span><span class="sxs-lookup"><span data-stu-id="d496e-103">Add Method</span></span>

<span data-ttu-id="d496e-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="d496e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="d496e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d496e-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="d496e-106">Fügt [der Befehls](the-commands-collection-object.md) Auflistung ein [Befehls](the-command-object.md) Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="d496e-106">Adds a [Command](the-command-object.md) object to the [Commands](the-commands-collection-object.md) collection.</span></span>

</dd> <dt>

<span data-ttu-id="d496e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="d496e-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="d496e-108">\*Agent ***. Zeichen ("*** Merkmal-ID \* \* *"). Befehle. Add* \*  *Name*, *Caption*, *Voice*, *aktiviert*, *Visible*</span><span class="sxs-lookup"><span data-stu-id="d496e-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Add*\* *Name*, *Caption*, *Voice*, *Enabled*, *Visible*</span></span>



| <span data-ttu-id="d496e-109">Teil</span><span class="sxs-lookup"><span data-stu-id="d496e-109">Part</span></span>      | <span data-ttu-id="d496e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d496e-110">Description</span></span>                                                                                                                                                                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d496e-111">*Name*</span><span class="sxs-lookup"><span data-stu-id="d496e-111">*Name*</span></span>    | <span data-ttu-id="d496e-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d496e-112">Required.</span></span> <span data-ttu-id="d496e-113">Ein Zeichen folgen Wert, der der ID entspricht, die Sie für den Befehl zuweisen.</span><span class="sxs-lookup"><span data-stu-id="d496e-113">A string value corresponding to the ID you assign for the command.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="d496e-114">*Caption*</span><span class="sxs-lookup"><span data-stu-id="d496e-114">*Caption*</span></span> | <span data-ttu-id="d496e-115">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d496e-115">Optional.</span></span> <span data-ttu-id="d496e-116">Ein Zeichen folgen Wert, der dem Namen entspricht, der im Popupmenü des Zeichens und im Befehlsfenster angezeigt wird, wenn die Client Anwendung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="d496e-116">A string value corresponding to the name that will appear in the character's pop-up menu and in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="d496e-117">Weitere Informationen finden Sie in der [Beschriftung](caption-property.md) -Eigenschaft des [Befehls](the-command-object.md) Objekts.</span><span class="sxs-lookup"><span data-stu-id="d496e-117">For more information, see the [Command](the-command-object.md) object's [Caption](caption-property.md) property.</span></span>                       |
| <span data-ttu-id="d496e-118">*Voice*</span><span class="sxs-lookup"><span data-stu-id="d496e-118">*Voice*</span></span>   | <span data-ttu-id="d496e-119">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d496e-119">Optional.</span></span> <span data-ttu-id="d496e-120">Ein Zeichen folgen Wert, der den Wörtern oder Ausdrücken entspricht, die von der Sprach-Engine zum erkennen dieses Befehls verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d496e-120">A string value corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> <span data-ttu-id="d496e-121">Weitere Informationen zum Formatieren von Alternativen für die Zeichenfolge finden Sie in der [Voice](voice-property.md) -Eigenschaft des [Befehls](the-command-object.md) Objekts.</span><span class="sxs-lookup"><span data-stu-id="d496e-121">For more information on formatting alternatives for the string, see the [Command](the-command-object.md) object's [Voice](voice-property.md) property.</span></span>                                |
| <span data-ttu-id="d496e-122">*Aktiviert*</span><span class="sxs-lookup"><span data-stu-id="d496e-122">*Enabled*</span></span> | <span data-ttu-id="d496e-123">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d496e-123">Optional.</span></span> <span data-ttu-id="d496e-124">Ein boolescher Wert, der angibt, ob der Befehl aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d496e-124">A Boolean value indicating whether the command is enabled.</span></span> <span data-ttu-id="d496e-125">Der Standardwert ist **True**.</span><span class="sxs-lookup"><span data-stu-id="d496e-125">The default value is **True**.</span></span> <span data-ttu-id="d496e-126">Weitere Informationen finden Sie unter der [aktivierten](enabled-property.md) Eigenschaft des [Befehls](the-command-object.md) Objekts.</span><span class="sxs-lookup"><span data-stu-id="d496e-126">For more information, see the [Command](the-command-object.md) object's [Enabled](enabled-property.md) property.</span></span>                                                                                              |
| <span data-ttu-id="d496e-127">*Visible*</span><span class="sxs-lookup"><span data-stu-id="d496e-127">*Visible*</span></span> | <span data-ttu-id="d496e-128">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d496e-128">Optional.</span></span> <span data-ttu-id="d496e-129">Ein boolescher Wert, der angibt, ob der Befehl im Popup Menü des Zeichens für das Zeichen sichtbar ist, wenn die Client Anwendung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="d496e-129">A Boolean value indicating whether the command is visible in the character's pop-up menu for the character when the client application is input-active.</span></span> <span data-ttu-id="d496e-130">Der Standardwert ist **True**.</span><span class="sxs-lookup"><span data-stu-id="d496e-130">The default value is **True**.</span></span> <span data-ttu-id="d496e-131">Weitere Informationen finden Sie in der [Visible](visible-property.md) -Eigenschaft des [Befehls](the-command-object.md) Objekts.</span><span class="sxs-lookup"><span data-stu-id="d496e-131">For more information, see the [Command](the-command-object.md) object's [Visible](visible-property.md) property.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d496e-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d496e-132">Remarks</span></span>

<span data-ttu-id="d496e-133">Der Wert der Eigenschaft " [Name](name-property.md) " eines [Befehls](the-command-object.md) Objekts muss [innerhalb der Befehls](the-commands-collection-object.md) Auflistung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="d496e-133">The value of a [Command](the-command-object.md) object's [Name](name-property.md) property must be unique within its [Commands](the-commands-collection-object.md) collection.</span></span> <span data-ttu-id="d496e-134">Sie müssen einen Befehl entfernen, bevor Sie einen neuen Befehl mit der gleichen Namens Eigenschafts Einstellung erstellen können.</span><span class="sxs-lookup"><span data-stu-id="d496e-134">You must remove a Command before you can create a new Command with the same Name property setting.</span></span> <span data-ttu-id="d496e-135">Wenn Sie versuchen, einen Befehl mit einer bereits vorhandenen Name-Eigenschaft zu erstellen, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d496e-135">Attempting to create a Command with a Name property that already exists raises an error.</span></span>

<span data-ttu-id="d496e-136">Diese Methode gibt auch ein [Command](the-command-object.md) -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="d496e-136">This method also returns a [Command](the-command-object.md) object.</span></span> <span data-ttu-id="d496e-137">Dies ermöglicht es Ihnen, ein Objekt zu deklarieren und ihm einen Befehl zuzuweisen, wenn Sie die AddMethod-Methode aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="d496e-137">This enables you to declare an object and assign a Command to it when you call the Addmethod.</span></span>


```
   Dim Cmd1 as IAgentCtlCommandEx
   Set Cmd1 = Genie.Commands.Add ("my first command", "Test", "Test", True, True)
   Cmd1.VoiceCaption = "this is a test"
```



## <a name="related-topics"></a><span data-ttu-id="d496e-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d496e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d496e-139">**Insert-Methode**</span><span class="sxs-lookup"><span data-stu-id="d496e-139">**Insert method**</span></span>](insert-method.md)
</dt> <dt>

[<span data-ttu-id="d496e-140">**RemoveAll-Methode**</span><span class="sxs-lookup"><span data-stu-id="d496e-140">**RemoveAll method**</span></span>](removeall-method.md)
</dt> <dt>

[<span data-ttu-id="d496e-141">**Remove-Methode**</span><span class="sxs-lookup"><span data-stu-id="d496e-141">**Remove method**</span></span>](remove-method.md)
</dt> </dl>

 

 




