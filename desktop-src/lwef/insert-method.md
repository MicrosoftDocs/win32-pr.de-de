---
title: Insert-Methode
description: Insert-Methode
ms.assetid: d58cfe50-ace7-4b0f-8539-c2e13a180c96
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74eb6d76c1be9b83b7742255ee5a771ed93c64d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338058"
---
# <a name="insert-method"></a><span data-ttu-id="a8deb-103">Insert-Methode</span><span class="sxs-lookup"><span data-stu-id="a8deb-103">Insert Method</span></span>

<span data-ttu-id="a8deb-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="a8deb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="a8deb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a8deb-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="a8deb-106">Fügt ein **Befehls** Objekt in die **Commands** -Auflistung ein.</span><span class="sxs-lookup"><span data-stu-id="a8deb-106">Inserts a **Command** object in the **Commands** collection.</span></span>

</dd> <dt>

<span data-ttu-id="a8deb-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="a8deb-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="a8deb-108">\*Agent ***. Zeichen ("*** Merkmal-ID \* \* *"). Commands. Insert* \*  *Name*, *ref Name*, *before*\_</span><span class="sxs-lookup"><span data-stu-id="a8deb-108">*agent ***.Characters ("*** CharacterID\*\*\*").Commands.Insert*\* *Name*, *RefName*, *Before*\_</span></span>

<span data-ttu-id="a8deb-109">*Beschriftung*, *Stimme, aktiviert, sichtbar*</span><span class="sxs-lookup"><span data-stu-id="a8deb-109">*Caption*, *Voice, Enabled, Visible*</span></span>



| <span data-ttu-id="a8deb-110">Teil</span><span class="sxs-lookup"><span data-stu-id="a8deb-110">Part</span></span>      | <span data-ttu-id="a8deb-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a8deb-111">Description</span></span>                                                                                                                                                                                                                                                                                          |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8deb-112">*Name*</span><span class="sxs-lookup"><span data-stu-id="a8deb-112">*Name*</span></span>    | <span data-ttu-id="a8deb-113">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a8deb-113">Required.</span></span> <span data-ttu-id="a8deb-114">Ein Zeichen folgen Wert, der der ID entspricht, die Sie dem [**Befehl**](/windows/desktop/lwef/the-command-object)zuweisen.</span><span class="sxs-lookup"><span data-stu-id="a8deb-114">A string value corresponding to the ID you assign to the [**Command**](/windows/desktop/lwef/the-command-object).</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="a8deb-115">*RefName*</span><span class="sxs-lookup"><span data-stu-id="a8deb-115">*RefName*</span></span> | <span data-ttu-id="a8deb-116">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a8deb-116">Required.</span></span> <span data-ttu-id="a8deb-117">Ein Zeichen folgen Wert, der dem Namen (ID) des Befehls direkt oberhalb oder unterhalb des Befehls entspricht, an dem der neue Befehl eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8deb-117">A string value corresponding to the name (ID) of the command just above or below where you want to insert the new command.</span></span>                                                                                                                                                                 |
| <span data-ttu-id="a8deb-118">*Vorher*</span><span class="sxs-lookup"><span data-stu-id="a8deb-118">*Before*</span></span>  | <span data-ttu-id="a8deb-119">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8deb-119">Optional.</span></span> <span data-ttu-id="a8deb-120">Ein boolescher Wert, der angibt, ob der neue Befehl vor dem Befehl eingefügt werden soll, der von *refname* angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a8deb-120">A Boolean value indicating whether to insert the new command before the command specified by *RefName*.</span></span> <span data-ttu-id="a8deb-121">**True** (Standard).</span><span class="sxs-lookup"><span data-stu-id="a8deb-121">**True** (Default).</span></span> <span data-ttu-id="a8deb-122">Der neue Befehl wird vor dem Befehl eingefügt, auf den verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a8deb-122">The new command will be inserted before the referenced command.</span></span><br/> <span data-ttu-id="a8deb-123">**False** Der neue Befehl wird nach dem Befehl eingefügt, auf den verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a8deb-123">**False** The new command will be inserted after the referenced command.</span></span><br/> |
| <span data-ttu-id="a8deb-124">*Caption*</span><span class="sxs-lookup"><span data-stu-id="a8deb-124">*Caption*</span></span> | <span data-ttu-id="a8deb-125">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8deb-125">Optional.</span></span> <span data-ttu-id="a8deb-126">Ein Zeichen folgen Wert, der dem Namen entspricht, der im Popupmenü des Zeichens und im Befehlsfenster angezeigt wird, wenn die Client Anwendung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="a8deb-126">A string value corresponding to the name that will appear in the character's pop-up menu and in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="a8deb-127">Weitere Informationen finden Sie in der [**Beschriftung**](caption-property.md)-Eigenschaft des [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts.</span><span class="sxs-lookup"><span data-stu-id="a8deb-127">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's [**Caption**](caption-property.md)property.</span></span>    |
| <span data-ttu-id="a8deb-128">*Voice*</span><span class="sxs-lookup"><span data-stu-id="a8deb-128">*Voice*</span></span>   | <span data-ttu-id="a8deb-129">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8deb-129">Optional.</span></span> <span data-ttu-id="a8deb-130">Ein Zeichen folgen Wert, der den Wörtern oder Ausdrücken entspricht, die von der Sprach-Engine zum erkennen dieses Befehls verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a8deb-130">A string value corresponding to the words or phrase to be used by the speech engine for recognizing this command.</span></span> <span data-ttu-id="a8deb-131">Weitere Informationen zum Formatieren von Alternativen für die Zeichenfolge finden Sie in der **Voice** -Eigenschaft des [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts.</span><span class="sxs-lookup"><span data-stu-id="a8deb-131">For more information on formatting alternatives for the string, see the [**Command**](/windows/desktop/lwef/the-command-object) object's **Voice** property.</span></span>                                  |
| <span data-ttu-id="a8deb-132">*Aktiviert*</span><span class="sxs-lookup"><span data-stu-id="a8deb-132">*Enabled*</span></span> | <span data-ttu-id="a8deb-133">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8deb-133">Optional.</span></span> <span data-ttu-id="a8deb-134">Ein boolescher Wert, der angibt, ob der Befehl aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a8deb-134">A Boolean value indicating whether the command is enabled.</span></span> <span data-ttu-id="a8deb-135">Der Standardwert ist **True**.</span><span class="sxs-lookup"><span data-stu-id="a8deb-135">The default value is **True**.</span></span> <span data-ttu-id="a8deb-136">Weitere Informationen finden Sie unter der **aktivierten** Eigenschaft des [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts.</span><span class="sxs-lookup"><span data-stu-id="a8deb-136">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's **Enabled** property.</span></span>                                                                                                  |
| <span data-ttu-id="a8deb-137">*Visible*</span><span class="sxs-lookup"><span data-stu-id="a8deb-137">*Visible*</span></span> | <span data-ttu-id="a8deb-138">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8deb-138">Optional.</span></span> <span data-ttu-id="a8deb-139">Ein boolescher Wert, der angibt, ob der Befehl im Befehlsfenster sichtbar ist, wenn die Client Anwendung aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="a8deb-139">A Boolean value indicating whether the command is visible in the Commands Window when the client application is input-active.</span></span> <span data-ttu-id="a8deb-140">Der Standardwert ist **True**.</span><span class="sxs-lookup"><span data-stu-id="a8deb-140">The default value is **True**.</span></span> <span data-ttu-id="a8deb-141">Weitere Informationen finden Sie in der [**Visible**](visible-property.md) -Eigenschaft des [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts.</span><span class="sxs-lookup"><span data-stu-id="a8deb-141">For more information, see the [**Command**](/windows/desktop/lwef/the-command-object) object's [**Visible**](visible-property.md) property.</span></span>       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a8deb-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8deb-142">Remarks</span></span>

<span data-ttu-id="a8deb-143">Der Wert der Eigenschaft " [**Name**](name-property.md) " eines [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts muss [**innerhalb der Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="a8deb-143">The value of a [**Command**](/windows/desktop/lwef/the-command-object) object's [**Name**](name-property.md) property must be unique within its [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="a8deb-144">Sie müssen einen **Befehl** entfernen, bevor Sie einen neuen **Befehl** mit der gleichen **namens** Eigenschafts Einstellung erstellen können.</span><span class="sxs-lookup"><span data-stu-id="a8deb-144">You must remove a **Command** before you can create a new **Command** with the same **Name** property setting.</span></span> <span data-ttu-id="a8deb-145">Wenn Sie versuchen, einen **Befehl** mit einer bereits vorhandenen **Name** -Eigenschaft zu erstellen, wird ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="a8deb-145">Attempting to create a **Command** with a **Name** property that already exists raises an error.</span></span>

<span data-ttu-id="a8deb-146">Diese Methode gibt auch ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="a8deb-146">This method also returns a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span> <span data-ttu-id="a8deb-147">Dies ermöglicht es Ihnen, ein Objekt zu deklarieren und ihm einen **Befehl** zuzuweisen, wenn Sie die **Insert** -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a8deb-147">This enables you to declare an object and assign a **Command** to it when you call the **Insert** method.</span></span>


```
   Dim Cmd2 as IAgentCtlCommandEx
   Set Cmd2 = Genie.Commands.Insert ("my second command", "my first command",_ True, "Test", "Test", True, True)
   Cmd2.VoiceCaption = "this is a test"
```



## <a name="see-also"></a><span data-ttu-id="a8deb-148">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a8deb-148">See Also</span></span>

<span data-ttu-id="a8deb-149">[**Add-Methode**](add-method.md), [**Remove**](remove-method.md)-Methode, [**RemoveAll-Methode**](removeall-method.md)</span><span class="sxs-lookup"><span data-stu-id="a8deb-149">[**Add method**](add-method.md), [**Remove method**](remove-method.md), [**RemoveAll method**](removeall-method.md)</span></span>


 

