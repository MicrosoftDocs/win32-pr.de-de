---
title: Das Command-Objekt
description: Das Command-Objekt
ms.assetid: a757846a-c2d0-4239-9533-babf5dc8399f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9e9ce22b3a1c0c2286232b5e2204e158501332
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340263"
---
# <a name="the-command-object"></a><span data-ttu-id="b0bad-103">Das Command-Objekt</span><span class="sxs-lookup"><span data-stu-id="b0bad-103">The Command Object</span></span>

<span data-ttu-id="b0bad-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="b0bad-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="b0bad-105">Ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt ist ein Element in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="b0bad-105">A [**Command**](/windows/desktop/lwef/the-command-object) object is an item in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="b0bad-106">Der Server stellt dem Benutzer Zugriff auf die **Befehls** Objekte zur Verfügung, wenn die Client Anwendung aktiv wird.</span><span class="sxs-lookup"><span data-stu-id="b0bad-106">The server provides the user access to your **Command** objects when your client application becomes input-active.</span></span>

-   [<span data-ttu-id="b0bad-107">Befehls Objekteigenschaften</span><span class="sxs-lookup"><span data-stu-id="b0bad-107">Command Object Properties</span></span>](command-object-properties.md)

<span data-ttu-id="b0bad-108">Wenn Sie auf die-Eigenschaft eines [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts zugreifen möchten, verweisen Sie in der zugehörigen Auflistung mit der Eigenschaft " [**Name**](name-property.md) " darauf.</span><span class="sxs-lookup"><span data-stu-id="b0bad-108">To access the property of a [**Command**](/windows/desktop/lwef/the-command-object) object, you reference it in its collection using its [**Name**](name-property.md) property.</span></span> <span data-ttu-id="b0bad-109">In VBScript und Visual Basic können Sie die **Name** -Eigenschaft direkt verwenden:</span><span class="sxs-lookup"><span data-stu-id="b0bad-109">In VBScript and Visual Basic you can use the **Name** property directly:</span></span>


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



<span data-ttu-id="b0bad-110">Verwenden Sie für Programmiersprachen, die keine Auflistungen unterstützen, die [**Befehls**](command-method.md) Methode:</span><span class="sxs-lookup"><span data-stu-id="b0bad-110">For programming languages that don't support collections, use the [**Command**](command-method.md) method:</span></span>


```
   <i>agent</i>.Characters("<i>CharacterID</i>").Commands.Command("<i>Name</i>").<i>property</i> [= <i>value</i>]
```



<span data-ttu-id="b0bad-111">Sie können auch auf ein Befehls Objekt verweisen, indem Sie einen Verweis darauf erstellen.</span><span class="sxs-lookup"><span data-stu-id="b0bad-111">You can also reference a Command object by creating a reference to it.</span></span> <span data-ttu-id="b0bad-112">Deklarieren Sie in Visual Basic eine Objekt Variable, und verwenden Sie die Set-Anweisung, um den Verweis zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="b0bad-112">In Visual Basic, declare an object variable and use the Set statement to create the reference:</span></span>


```
   Dim Cmd1 as Object
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="b0bad-113">In Visual Basic 5,0 können Sie das Objekt auch als Typ [**iagentctlcommandex**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) deklarieren und den Verweis erstellen.</span><span class="sxs-lookup"><span data-stu-id="b0bad-113">In Visual Basic 5.0, you can also declare the object as type [**IAgentCtlCommandEx**](https://www.bing.com/search?q=**IAgentCtlCommandEx**) and create the reference.</span></span> <span data-ttu-id="b0bad-114">Diese Konvention ermöglicht eine frühe Bindung, was zu einer besseren Leistung führt:</span><span class="sxs-lookup"><span data-stu-id="b0bad-114">This convention enables early binding, which results in better performance:</span></span>


```
   Dim Cmd1 as IAgentCtlCommandEx
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="b0bad-115">In VBScript können Sie einen Verweis als einen bestimmten Typ deklarieren, aber Sie können die Variable trotzdem deklarieren und Sie auf den [**Befehl**](/windows/desktop/lwef/the-command-object) in der Sammlung festlegen:</span><span class="sxs-lookup"><span data-stu-id="b0bad-115">In VBScript, you can declare a reference as a particular type, but you can still declare the variable and set it to the [**Command**](/windows/desktop/lwef/the-command-object) in the collection:</span></span>


```
   Dim Cmd1
   ...
   Set Cmd1 = Agent.Characters("MyCharacterID").Commands("SampleCommand")
   ...
   Cmd1.Enabled = True
```



<span data-ttu-id="b0bad-116">Ein Befehl kann entweder im Popup-Menü des Zeichens und im Fenster "Befehle" oder in beiden angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b0bad-116">A command may appear in either the character's pop-up menu and the Commands Window, or in both.</span></span> <span data-ttu-id="b0bad-117">Um im Popup Menü angezeigt zu werden, muss Sie über eine Beschriftung verfügen, und die [**Visible**](visible-property.md) -Eigenschaft muss auf **true** festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="b0bad-117">To appear in the pop-up menu it must have a caption and have the [**Visible**](visible-property.md) property set to **True**.</span></span> <span data-ttu-id="b0bad-118">Außerdem muss die **sichtbare** Eigenschaft des Commands-Auflistungs Objekts auch auf **true** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b0bad-118">In addition, its Commands collection object **Visible** property must also be set to **True**.</span></span> <span data-ttu-id="b0bad-119">Um im Fenster Befehle angezeigt zu werden, muss für einen [**Befehl**](/windows/desktop/lwef/the-command-object) die [**Beschriftung**](caption-property.md) und die [**sprach**](voice-property.md) Eigenschaften festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="b0bad-119">To appear in the Commands Window, a [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Caption**](caption-property.md) and [**Voice**](voice-property.md) properties set.</span></span> <span data-ttu-id="b0bad-120">Beachten Sie, dass sich die Popup Menüeinträge eines Zeichens nicht ändern, während das Menü angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b0bad-120">Note that a character's pop-up menu entries do not change while the menu displays.</span></span> <span data-ttu-id="b0bad-121">Wenn Sie Befehle hinzufügen oder entfernen oder deren Eigenschaften ändern, während das Popup Menü des Zeichens angezeigt wird, werden diese Änderungen im Menü angezeigt, sobald der Benutzer das nächste Mal anzeigt.</span><span class="sxs-lookup"><span data-stu-id="b0bad-121">If you add or remove commands or change their properties while the character's pop-up menu is displayed, the menu displays those changes whenever the user next displays it.</span></span> <span data-ttu-id="b0bad-122">Das Fenster "Befehle" reflektiert jedoch dynamisch alle Änderungen, die Sie vornehmen.</span><span class="sxs-lookup"><span data-stu-id="b0bad-122">However, the Commands Window dynamically reflects any changes you make.</span></span>

<span data-ttu-id="b0bad-123">In der folgenden Tabelle wird zusammengefasst, wie sich die Eigenschaften eines [**Befehls**](/windows/desktop/lwef/the-command-object) auf seine Darstellung auswirken:</span><span class="sxs-lookup"><span data-stu-id="b0bad-123">The following table summarizes how the properties of a [**Command**](/windows/desktop/lwef/the-command-object) affect its presentation:</span></span>



<span data-ttu-id="b0bad-124">Caption-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b0bad-124">Caption Property</span></span>

<span data-ttu-id="b0bad-125">Voice-Caption-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b0bad-125">Voice-Caption Property</span></span>

<span data-ttu-id="b0bad-126">Voice-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b0bad-126">Voice Property</span></span>

<span data-ttu-id="b0bad-127">Visible-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b0bad-127">Visible Property</span></span>

<span data-ttu-id="b0bad-128">Enabled-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b0bad-128">Enabled Property</span></span>

<span data-ttu-id="b0bad-129">Wird im Popupmenü des Zeichens angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b0bad-129">Appears in Character's Pop-up Menu</span></span>

<span data-ttu-id="b0bad-130">Wird im Fenster "Befehle" angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-130">Appears in Commands Window</span></span>

<span data-ttu-id="b0bad-131">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-131">Yes</span></span>

<span data-ttu-id="b0bad-132">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-132">Yes</span></span>

<span data-ttu-id="b0bad-133">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-133">Yes</span></span>

<span data-ttu-id="b0bad-134">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-134">True</span></span>

<span data-ttu-id="b0bad-135">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-135">True</span></span>

<span data-ttu-id="b0bad-136">Normal, mit [ **Beschriftung**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0bad-136">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="b0bad-137">Ja, mit [ **voicecaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0bad-137">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="b0bad-138">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-138">Yes</span></span>

<span data-ttu-id="b0bad-139">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-139">Yes</span></span>

<span data-ttu-id="b0bad-140">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-140">Yes</span></span>

<span data-ttu-id="b0bad-141">Richtig</span><span class="sxs-lookup"><span data-stu-id="b0bad-141">True</span></span>

<span data-ttu-id="b0bad-142">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-142">False</span></span>

<span data-ttu-id="b0bad-143">Deaktiviert mit [ **Beschriftung**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0bad-143">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="b0bad-144">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-144">No</span></span>

<span data-ttu-id="b0bad-145">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-145">Yes</span></span>

<span data-ttu-id="b0bad-146">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-146">Yes</span></span>

<span data-ttu-id="b0bad-147">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-147">Yes</span></span>

<span data-ttu-id="b0bad-148">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-148">False</span></span>

<span data-ttu-id="b0bad-149">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-149">True</span></span>

<span data-ttu-id="b0bad-150">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-150">Does not appear</span></span>

<span data-ttu-id="b0bad-151">Ja, mit [ **voicecaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0bad-151">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="b0bad-152">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-152">Yes</span></span>

<span data-ttu-id="b0bad-153">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-153">Yes</span></span>

<span data-ttu-id="b0bad-154">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-154">Yes</span></span>

<span data-ttu-id="b0bad-155">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-155">False</span></span>

<span data-ttu-id="b0bad-156">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-156">False</span></span>

<span data-ttu-id="b0bad-157">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-157">Does not appear</span></span>

<span data-ttu-id="b0bad-158">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-158">No</span></span>

<span data-ttu-id="b0bad-159">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-159">Yes</span></span>

<span data-ttu-id="b0bad-160">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-160">Yes</span></span>

<span data-ttu-id="b0bad-161">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-161">No</span></span> 

<span data-ttu-id="b0bad-162">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-162">True</span></span>

<span data-ttu-id="b0bad-163">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-163">True</span></span>

<span data-ttu-id="b0bad-164">Normal, mit [ **Beschriftung**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0bad-164">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="b0bad-165">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-165">No</span></span>

<span data-ttu-id="b0bad-166">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-166">Yes</span></span>

<span data-ttu-id="b0bad-167">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-167">Yes</span></span>

<span data-ttu-id="b0bad-168">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-168">No</span></span> 

<span data-ttu-id="b0bad-169">Richtig</span><span class="sxs-lookup"><span data-stu-id="b0bad-169">True</span></span>

<span data-ttu-id="b0bad-170">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-170">False</span></span>

<span data-ttu-id="b0bad-171">Deaktiviert mit [ **Beschriftung**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0bad-171">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="b0bad-172">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-172">No</span></span>

<span data-ttu-id="b0bad-173">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-173">Yes</span></span>

<span data-ttu-id="b0bad-174">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-174">Yes</span></span>

<span data-ttu-id="b0bad-175">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-175">No</span></span> 

<span data-ttu-id="b0bad-176">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-176">False</span></span>

<span data-ttu-id="b0bad-177">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-177">True</span></span>

<span data-ttu-id="b0bad-178">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-178">Does not appear</span></span>

<span data-ttu-id="b0bad-179">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-179">No</span></span>

<span data-ttu-id="b0bad-180">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-180">Yes</span></span>

<span data-ttu-id="b0bad-181">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-181">Yes</span></span>

<span data-ttu-id="b0bad-182">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-182">No</span></span> 

<span data-ttu-id="b0bad-183">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-183">False</span></span>

<span data-ttu-id="b0bad-184">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-184">False</span></span>

<span data-ttu-id="b0bad-185">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-185">Does not appear</span></span>

<span data-ttu-id="b0bad-186">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-186">No</span></span>

<span data-ttu-id="b0bad-187">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-187">No</span></span> 

<span data-ttu-id="b0bad-188">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-188">Yes</span></span>

<span data-ttu-id="b0bad-189">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-189">Yes</span></span>

<span data-ttu-id="b0bad-190">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-190">True</span></span>

<span data-ttu-id="b0bad-191">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-191">True</span></span>

<span data-ttu-id="b0bad-192">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-192">Does not appear</span></span>

<span data-ttu-id="b0bad-193">Ja, mit [ **voicecaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0bad-193">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="b0bad-194">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-194">No</span></span> 

<span data-ttu-id="b0bad-195">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-195">Yes</span></span>

<span data-ttu-id="b0bad-196">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-196">Yes</span></span>

<span data-ttu-id="b0bad-197">Richtig</span><span class="sxs-lookup"><span data-stu-id="b0bad-197">True</span></span>

<span data-ttu-id="b0bad-198">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-198">False</span></span>

<span data-ttu-id="b0bad-199">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-199">Does not appear</span></span>

<span data-ttu-id="b0bad-200">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-200">No</span></span>

<span data-ttu-id="b0bad-201">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-201">No</span></span> 

<span data-ttu-id="b0bad-202">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-202">Yes</span></span>

<span data-ttu-id="b0bad-203">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-203">Yes</span></span>

<span data-ttu-id="b0bad-204">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-204">False</span></span>

<span data-ttu-id="b0bad-205">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-205">True</span></span>

<span data-ttu-id="b0bad-206">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-206">Does not appear</span></span>

<span data-ttu-id="b0bad-207">Ja, mit [ **voicecaption**](voicecaption-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0bad-207">Yes, using [**VoiceCaption**](voicecaption-property.md)</span></span>

<span data-ttu-id="b0bad-208">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-208">No</span></span> 

<span data-ttu-id="b0bad-209">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-209">Yes</span></span>

<span data-ttu-id="b0bad-210">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-210">Yes</span></span>

<span data-ttu-id="b0bad-211">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-211">False</span></span>

<span data-ttu-id="b0bad-212">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-212">False</span></span>

<span data-ttu-id="b0bad-213">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-213">Does not appear</span></span>

<span data-ttu-id="b0bad-214">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-214">No</span></span>

<span data-ttu-id="b0bad-215">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-215">No</span></span> 

<span data-ttu-id="b0bad-216">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-216">Yes</span></span>

<span data-ttu-id="b0bad-217">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-217">No</span></span> 

<span data-ttu-id="b0bad-218">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-218">True</span></span>

<span data-ttu-id="b0bad-219">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-219">True</span></span>

<span data-ttu-id="b0bad-220">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-220">Does not appear</span></span>

<span data-ttu-id="b0bad-221">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-221">No</span></span>

<span data-ttu-id="b0bad-222">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-222">No</span></span> 

<span data-ttu-id="b0bad-223">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-223">Yes</span></span>

<span data-ttu-id="b0bad-224">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-224">No</span></span> 

<span data-ttu-id="b0bad-225">Richtig</span><span class="sxs-lookup"><span data-stu-id="b0bad-225">True</span></span>

<span data-ttu-id="b0bad-226">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-226">False</span></span>

<span data-ttu-id="b0bad-227">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-227">Does not appear</span></span>

<span data-ttu-id="b0bad-228">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-228">No</span></span>

<span data-ttu-id="b0bad-229">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-229">No</span></span> 

<span data-ttu-id="b0bad-230">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-230">Yes</span></span>

<span data-ttu-id="b0bad-231">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-231">No</span></span> 

<span data-ttu-id="b0bad-232">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-232">False</span></span>

<span data-ttu-id="b0bad-233">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-233">True</span></span>

<span data-ttu-id="b0bad-234">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-234">Does not appear</span></span>

<span data-ttu-id="b0bad-235">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-235">No</span></span>

<span data-ttu-id="b0bad-236">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-236">No</span></span> 

<span data-ttu-id="b0bad-237">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-237">Yes</span></span>

<span data-ttu-id="b0bad-238">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-238">No</span></span> 

<span data-ttu-id="b0bad-239">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-239">False</span></span>

<span data-ttu-id="b0bad-240">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-240">False</span></span>

<span data-ttu-id="b0bad-241">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-241">Does not appear</span></span>

<span data-ttu-id="b0bad-242">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-242">No</span></span>

<span data-ttu-id="b0bad-243">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-243">Yes</span></span>

<span data-ttu-id="b0bad-244">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-244">No</span></span> 

<span data-ttu-id="b0bad-245">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-245">Yes</span></span>

<span data-ttu-id="b0bad-246">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-246">True</span></span>

<span data-ttu-id="b0bad-247">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-247">True</span></span>

<span data-ttu-id="b0bad-248">Normal, mit [ **Beschriftung**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0bad-248">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="b0bad-249">Ja, mit [ **Beschriftung**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0bad-249">Yes, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="b0bad-250">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-250">Yes</span></span>

<span data-ttu-id="b0bad-251">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-251">No</span></span> 

<span data-ttu-id="b0bad-252">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-252">Yes</span></span>

<span data-ttu-id="b0bad-253">Richtig</span><span class="sxs-lookup"><span data-stu-id="b0bad-253">True</span></span>

<span data-ttu-id="b0bad-254">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-254">False</span></span>

<span data-ttu-id="b0bad-255">Deaktiviert mit [ **Beschriftung**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0bad-255">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="b0bad-256">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-256">No</span></span>

<span data-ttu-id="b0bad-257">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-257">Yes</span></span>

<span data-ttu-id="b0bad-258">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-258">No</span></span> 

<span data-ttu-id="b0bad-259">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-259">Yes</span></span>

<span data-ttu-id="b0bad-260">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-260">False</span></span>

<span data-ttu-id="b0bad-261">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-261">True</span></span>

<span data-ttu-id="b0bad-262">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-262">Does not appear</span></span>

<span data-ttu-id="b0bad-263">Ja, mit [ **Beschriftung**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0bad-263">Yes, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="b0bad-264">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-264">Yes</span></span>

<span data-ttu-id="b0bad-265">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-265">No</span></span> 

<span data-ttu-id="b0bad-266">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-266">Yes</span></span>

<span data-ttu-id="b0bad-267">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-267">False</span></span>

<span data-ttu-id="b0bad-268">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-268">False</span></span>

<span data-ttu-id="b0bad-269">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-269">Does not appear</span></span>

<span data-ttu-id="b0bad-270">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-270">No</span></span>

<span data-ttu-id="b0bad-271">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-271">Yes</span></span>

<span data-ttu-id="b0bad-272">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-272">No</span></span> 

<span data-ttu-id="b0bad-273">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-273">No</span></span> 

<span data-ttu-id="b0bad-274">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-274">True</span></span>

<span data-ttu-id="b0bad-275">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-275">True</span></span>

<span data-ttu-id="b0bad-276">Normal, mit [ **Beschriftung**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0bad-276">Normal, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="b0bad-277">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-277">No</span></span>

<span data-ttu-id="b0bad-278">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-278">Yes</span></span>

<span data-ttu-id="b0bad-279">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-279">No</span></span> 

<span data-ttu-id="b0bad-280">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-280">No</span></span> 

<span data-ttu-id="b0bad-281">Richtig</span><span class="sxs-lookup"><span data-stu-id="b0bad-281">True</span></span>

<span data-ttu-id="b0bad-282">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-282">False</span></span>

<span data-ttu-id="b0bad-283">Deaktiviert mit [ **Beschriftung**](caption-property.md)</span><span class="sxs-lookup"><span data-stu-id="b0bad-283">Disabled, using [**Caption**](caption-property.md)</span></span>

<span data-ttu-id="b0bad-284">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-284">No</span></span>

<span data-ttu-id="b0bad-285">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-285">Yes</span></span>

<span data-ttu-id="b0bad-286">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-286">No</span></span> 

<span data-ttu-id="b0bad-287">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-287">No</span></span> 

<span data-ttu-id="b0bad-288">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-288">False</span></span>

<span data-ttu-id="b0bad-289">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-289">True</span></span>

<span data-ttu-id="b0bad-290">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-290">Does not appear</span></span>

<span data-ttu-id="b0bad-291">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-291">No</span></span>

<span data-ttu-id="b0bad-292">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-292">Yes</span></span>

<span data-ttu-id="b0bad-293">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-293">No</span></span> 

<span data-ttu-id="b0bad-294">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-294">No</span></span> 

<span data-ttu-id="b0bad-295">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-295">False</span></span>

<span data-ttu-id="b0bad-296">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-296">False</span></span>

<span data-ttu-id="b0bad-297">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-297">Does not appear</span></span>

<span data-ttu-id="b0bad-298">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-298">No</span></span>

<span data-ttu-id="b0bad-299">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-299">No</span></span> 

<span data-ttu-id="b0bad-300">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-300">No</span></span> 

<span data-ttu-id="b0bad-301">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-301">Yes</span></span>

<span data-ttu-id="b0bad-302">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-302">True</span></span>

<span data-ttu-id="b0bad-303">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-303">True</span></span>

<span data-ttu-id="b0bad-304">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-304">Does not appear</span></span>

<span data-ttu-id="b0bad-305">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-305">No</span></span> 

<span data-ttu-id="b0bad-306">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-306">No</span></span> 

<span data-ttu-id="b0bad-307">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-307">No</span></span> 

<span data-ttu-id="b0bad-308">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-308">Yes</span></span>

<span data-ttu-id="b0bad-309">Richtig</span><span class="sxs-lookup"><span data-stu-id="b0bad-309">True</span></span>

<span data-ttu-id="b0bad-310">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-310">False</span></span>

<span data-ttu-id="b0bad-311">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-311">Does not appear</span></span>

<span data-ttu-id="b0bad-312">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-312">No</span></span>

<span data-ttu-id="b0bad-313">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-313">No</span></span> 

<span data-ttu-id="b0bad-314">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-314">No</span></span> 

<span data-ttu-id="b0bad-315">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-315">Yes</span></span>

<span data-ttu-id="b0bad-316">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-316">False</span></span>

<span data-ttu-id="b0bad-317">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-317">True</span></span>

<span data-ttu-id="b0bad-318">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-318">Does not appear</span></span>

<span data-ttu-id="b0bad-319">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-319">No</span></span> 

<span data-ttu-id="b0bad-320">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-320">No</span></span> 

<span data-ttu-id="b0bad-321">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-321">No</span></span> 

<span data-ttu-id="b0bad-322">Ja</span><span class="sxs-lookup"><span data-stu-id="b0bad-322">Yes</span></span>

<span data-ttu-id="b0bad-323">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-323">False</span></span>

<span data-ttu-id="b0bad-324">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-324">False</span></span>

<span data-ttu-id="b0bad-325">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-325">Does not appear</span></span>

<span data-ttu-id="b0bad-326">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-326">No</span></span>

<span data-ttu-id="b0bad-327">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-327">No</span></span> 

<span data-ttu-id="b0bad-328">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-328">No</span></span> 

<span data-ttu-id="b0bad-329">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-329">No</span></span> 

<span data-ttu-id="b0bad-330">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-330">True</span></span>

<span data-ttu-id="b0bad-331">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-331">True</span></span>

<span data-ttu-id="b0bad-332">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-332">Does not appear</span></span>

<span data-ttu-id="b0bad-333">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-333">No</span></span>

<span data-ttu-id="b0bad-334">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-334">No</span></span> 

<span data-ttu-id="b0bad-335">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-335">No</span></span> 

<span data-ttu-id="b0bad-336">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-336">No</span></span> 

<span data-ttu-id="b0bad-337">Richtig</span><span class="sxs-lookup"><span data-stu-id="b0bad-337">True</span></span>

<span data-ttu-id="b0bad-338">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-338">False</span></span>

<span data-ttu-id="b0bad-339">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-339">Does not appear</span></span>

<span data-ttu-id="b0bad-340">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-340">No</span></span>

<span data-ttu-id="b0bad-341">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-341">No</span></span> 

<span data-ttu-id="b0bad-342">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-342">No</span></span> 

<span data-ttu-id="b0bad-343">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-343">No</span></span> 

<span data-ttu-id="b0bad-344">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-344">False</span></span>

<span data-ttu-id="b0bad-345">True</span><span class="sxs-lookup"><span data-stu-id="b0bad-345">True</span></span>

<span data-ttu-id="b0bad-346">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-346">Does not appear</span></span>

<span data-ttu-id="b0bad-347">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-347">No</span></span>

<span data-ttu-id="b0bad-348">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-348">No</span></span> 

<span data-ttu-id="b0bad-349">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-349">No</span></span> 

<span data-ttu-id="b0bad-350">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-350">No</span></span> 

<span data-ttu-id="b0bad-351">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-351">False</span></span>

<span data-ttu-id="b0bad-352">False</span><span class="sxs-lookup"><span data-stu-id="b0bad-352">False</span></span>

<span data-ttu-id="b0bad-353">Wird nicht angezeigt</span><span class="sxs-lookup"><span data-stu-id="b0bad-353">Does not appear</span></span>

<span data-ttu-id="b0bad-354">Nein</span><span class="sxs-lookup"><span data-stu-id="b0bad-354">No</span></span>

 <span data-ttu-id="b0bad-355">, Wenn die Eigenschafts Einstellung NULL ist.</span><span class="sxs-lookup"><span data-stu-id="b0bad-355">If the property setting is null.</span></span> <span data-ttu-id="b0bad-356">In manchen Programmiersprachen kann eine leere Zeichenfolge nicht wie eine NULL-Zeichenfolge interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="b0bad-356">In some programming languages, an empty string may not be interpreted the same as a null string.</span></span>  <span data-ttu-id="b0bad-357">Der Befehl ist weiterhin sprach zugänglich.</span><span class="sxs-lookup"><span data-stu-id="b0bad-357">The command is still voice-accessible.</span></span><br/>



 

<span data-ttu-id="b0bad-358">Wenn der Server Eingaben für einen ihrer Befehle empfängt, sendet er ein [**Befehls**](/windows/desktop/lwef/the-command-object) Ereignis und übergibt den Namen des **Befehls** als Attribut des [**UserInput**](/windows/desktop/lwef/iagentuserinput) -Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="b0bad-358">When the server receives input for one of your commands, it sends a [**Command**](/windows/desktop/lwef/the-command-object) event, and passes back the name of the **Command** as an attribute of the [**UserInput**](/windows/desktop/lwef/iagentuserinput) object.</span></span> <span data-ttu-id="b0bad-359">Anschließend können Sie bedingte Anweisungen verwenden, um den **Befehl** abzugleichen und zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="b0bad-359">You can then use conditional statements to match and process the **Command**.</span></span>

 

