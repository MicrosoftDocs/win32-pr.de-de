---
description: In der Tabelle ControlCondition kann ein Autor spezielle Aktionen angeben, die auf die Steuerelemente basierend auf dem Ergebnis einer Bedingungs Anweisung angewendet werden sollen. Wenn Sie diese Tabelle verwenden, könnte der Autor z. b. ein Steuerelement auf der Grundlage der VersionNT-Eigenschaft ausblenden.
ms.assetid: e36d20ec-cd7b-494f-b517-c07b40d2a338
title: ControlCondition-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 671dcdee6e2ed1067c51a04084693c276b8db2d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960157"
---
# <a name="controlcondition-table"></a><span data-ttu-id="8f3f2-104">ControlCondition-Tabelle</span><span class="sxs-lookup"><span data-stu-id="8f3f2-104">ControlCondition Table</span></span>

<span data-ttu-id="8f3f2-105">In der Tabelle ControlCondition kann ein Autor spezielle Aktionen angeben, die auf die Steuerelemente basierend auf dem Ergebnis einer Bedingungs Anweisung angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-105">The ControlCondition table enables an author to specify special actions to be applied to controls based on the result of a conditional statement.</span></span> <span data-ttu-id="8f3f2-106">Wenn Sie diese Tabelle verwenden, könnte der Autor z. b. ein Steuerelement auf der Grundlage der [**VersionNT**](versionnt.md) -Eigenschaft ausblenden.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-106">For example, using this table the author could choose to hide a control based on the [**VersionNT**](versionnt.md) property.</span></span>

<span data-ttu-id="8f3f2-107">Die Tabelle "ControlCondition" enthält die folgenden Spalten.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-107">The ControlCondition table has the following columns.</span></span>



| <span data-ttu-id="8f3f2-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="8f3f2-108">Column</span></span>    | <span data-ttu-id="8f3f2-109">Typ</span><span class="sxs-lookup"><span data-stu-id="8f3f2-109">Type</span></span>                         | <span data-ttu-id="8f3f2-110">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="8f3f2-110">Key</span></span> | <span data-ttu-id="8f3f2-111">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="8f3f2-111">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="8f3f2-112">Dialog\_</span><span class="sxs-lookup"><span data-stu-id="8f3f2-112">Dialog\_</span></span>  | [<span data-ttu-id="8f3f2-113">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="8f3f2-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="8f3f2-114">J</span><span class="sxs-lookup"><span data-stu-id="8f3f2-114">Y</span></span>   | <span data-ttu-id="8f3f2-115">N</span><span class="sxs-lookup"><span data-stu-id="8f3f2-115">N</span></span>        |
| <span data-ttu-id="8f3f2-116">Steuerelement\_</span><span class="sxs-lookup"><span data-stu-id="8f3f2-116">Control\_</span></span> | [<span data-ttu-id="8f3f2-117">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="8f3f2-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="8f3f2-118">J</span><span class="sxs-lookup"><span data-stu-id="8f3f2-118">Y</span></span>   | <span data-ttu-id="8f3f2-119">N</span><span class="sxs-lookup"><span data-stu-id="8f3f2-119">N</span></span>        |
| <span data-ttu-id="8f3f2-120">Aktion</span><span class="sxs-lookup"><span data-stu-id="8f3f2-120">Action</span></span>    | [<span data-ttu-id="8f3f2-121">Text</span><span class="sxs-lookup"><span data-stu-id="8f3f2-121">Text</span></span>](text.md)             | <span data-ttu-id="8f3f2-122">J</span><span class="sxs-lookup"><span data-stu-id="8f3f2-122">Y</span></span>   | <span data-ttu-id="8f3f2-123">N</span><span class="sxs-lookup"><span data-stu-id="8f3f2-123">N</span></span>        |
| <span data-ttu-id="8f3f2-124">Bedingung</span><span class="sxs-lookup"><span data-stu-id="8f3f2-124">Condition</span></span> | [<span data-ttu-id="8f3f2-125">Condition</span><span class="sxs-lookup"><span data-stu-id="8f3f2-125">Condition</span></span>](condition.md)   | <span data-ttu-id="8f3f2-126">J</span><span class="sxs-lookup"><span data-stu-id="8f3f2-126">Y</span></span>   | <span data-ttu-id="8f3f2-127">N</span><span class="sxs-lookup"><span data-stu-id="8f3f2-127">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="8f3f2-128">Spalten</span><span class="sxs-lookup"><span data-stu-id="8f3f2-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="8f3f2-129"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span><span class="sxs-lookup"><span data-stu-id="8f3f2-129"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="8f3f2-130">Ein externer Schlüssel für die erste Spalte der [Dialog Feld Tabelle](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="8f3f2-130">An external key to the first column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="8f3f2-131">Durch kombinieren dieses Felds mit dem Steuerelement Feld wird ein eindeutiges \_ Steuerelement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-131">Combining this field with the Control\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="8f3f2-132"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Steuerelement\_</span><span class="sxs-lookup"><span data-stu-id="8f3f2-132"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="8f3f2-133">Ein externer Schlüssel für die zweite Spalte der [Steuerelement Tabelle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="8f3f2-133">An external key to the second column of the [Control table](control-table.md).</span></span> <span data-ttu-id="8f3f2-134">Durch kombinieren dieses Felds wird das Dialog \_ Feld mit einem eindeutigen Steuerelement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-134">Combining this field the Dialog\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="8f3f2-135"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel</span><span class="sxs-lookup"><span data-stu-id="8f3f2-135"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="8f3f2-136">Die Aktion, die für das-Steuerelement ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-136">The action that is to be taken on the control.</span></span> <span data-ttu-id="8f3f2-137">Die möglichen Aktionen sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-137">The possible actions are shown in the following table.</span></span>



| <span data-ttu-id="8f3f2-138">Wert</span><span class="sxs-lookup"><span data-stu-id="8f3f2-138">Value</span></span>   | <span data-ttu-id="8f3f2-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8f3f2-139">Meaning</span></span>                     |
|---------|-----------------------------|
| <span data-ttu-id="8f3f2-140">Standard</span><span class="sxs-lookup"><span data-stu-id="8f3f2-140">Default</span></span> | <span data-ttu-id="8f3f2-141">Legen Sie das Steuerelement als Standard fest.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-141">Set control as the default.</span></span> |
| <span data-ttu-id="8f3f2-142">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="8f3f2-142">Disable</span></span> | <span data-ttu-id="8f3f2-143">Deaktivieren Sie das-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-143">Disable the control.</span></span>        |
| <span data-ttu-id="8f3f2-144">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="8f3f2-144">Enable</span></span>  | <span data-ttu-id="8f3f2-145">Aktivieren Sie das-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-145">Enable the control.</span></span>         |
| <span data-ttu-id="8f3f2-146">Ausblenden</span><span class="sxs-lookup"><span data-stu-id="8f3f2-146">Hide</span></span>    | <span data-ttu-id="8f3f2-147">Blenden Sie das Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-147">Hide the control.</span></span>           |
| <span data-ttu-id="8f3f2-148">Anzeigen</span><span class="sxs-lookup"><span data-stu-id="8f3f2-148">Show</span></span>    | <span data-ttu-id="8f3f2-149">Zeigen Sie das Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-149">Display the control.</span></span>        |



 

</dd> <dt>

<span data-ttu-id="8f3f2-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage</span><span class="sxs-lookup"><span data-stu-id="8f3f2-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="8f3f2-151">Eine Bedingungs Anweisung, die angibt, unter welchen Bedingungen die Aktion ausgelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-151">A conditional statement that specifies under which conditions the action should be triggered.</span></span> <span data-ttu-id="8f3f2-152">Diese Spalte darf nicht leer bleiben.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-152">This column may not be left blank.</span></span> <span data-ttu-id="8f3f2-153">Wenn diese Anweisung nicht als true ausgewertet wird, wird die Aktion nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-153">If this statement does not evaluate to TRUE, the action does not take place.</span></span> <span data-ttu-id="8f3f2-154">Wenn der Wert auf 1 festgelegt ist, wird die Aktion immer angewendet.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-154">If it is set to 1, the action is always applied.</span></span> <span data-ttu-id="8f3f2-155">Weitere Informationen zur Syntax von Bedingungs Anweisungen finden Sie unter [Syntax für bedingte](conditional-statement-syntax.md)Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-155">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f3f2-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8f3f2-156">Remarks</span></span>

<span data-ttu-id="8f3f2-157">Wenn Sie ein [PUSHBUTTON-Steuer](pushbutton-control.md) Element oder ein CheckBox- [Steuer](checkbox-control.md) Element auf der Grundlage einer Bedingungs Anweisung im Bedingungs Feld der ControlCondition-Tabelle ausblenden und deaktivieren möchten, sollten Sie für jedes Steuerelement vier Datensätze verwenden, um das Steuerelement zu deaktivieren und das Steuerelement auszublenden.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-157">If you want to hide and disable a [PushButton control](pushbutton-control.md) or [CheckBox control](checkbox-control.md) based on a conditional statement in the Condition field of the ControlCondition table, you should use four records for each control to disable as well as hide the control.</span></span> <span data-ttu-id="8f3f2-158">Auf PUSHBUTTON-oder CheckBox-Steuerelemente, die nur ausgeblendet wurden, kann weiterhin über Tastenkombinationen zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-158">PushButton or CheckBox controls that have only been hidden can still be accessed by shortcut keys.</span></span>

<span data-ttu-id="8f3f2-159">Die folgenden Datensätze Blenden z. b. die ControlA in dialoga aus und deaktivieren Sie, wenn das Produkt installiert wird.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-159">For example, the following records hide and disable ControlA on DialogA when the product is installed.</span></span> <span data-ttu-id="8f3f2-160">Das-Steuerelement ist sichtbar und wird aktiviert, wenn das Produkt nicht installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8f3f2-160">The control will be visible and enabled when the product is not installed.</span></span>



| <span data-ttu-id="8f3f2-161">Dialog</span><span class="sxs-lookup"><span data-stu-id="8f3f2-161">Dialog</span></span>  | <span data-ttu-id="8f3f2-162">Control</span><span class="sxs-lookup"><span data-stu-id="8f3f2-162">Control</span></span>  | <span data-ttu-id="8f3f2-163">Aktion</span><span class="sxs-lookup"><span data-stu-id="8f3f2-163">Action</span></span>  | <span data-ttu-id="8f3f2-164">Bedingung</span><span class="sxs-lookup"><span data-stu-id="8f3f2-164">Condition</span></span>                      |
|---------|----------|---------|--------------------------------|
| <span data-ttu-id="8f3f2-165">Dialoga</span><span class="sxs-lookup"><span data-stu-id="8f3f2-165">DialogA</span></span> | <span data-ttu-id="8f3f2-166">ControlA</span><span class="sxs-lookup"><span data-stu-id="8f3f2-166">ControlA</span></span> | <span data-ttu-id="8f3f2-167">Ausblenden</span><span class="sxs-lookup"><span data-stu-id="8f3f2-167">Hide</span></span>    | [<span data-ttu-id="8f3f2-168">**Installiert**</span><span class="sxs-lookup"><span data-stu-id="8f3f2-168">**Installed**</span></span>](installed.md) |
| <span data-ttu-id="8f3f2-169">Dialoga</span><span class="sxs-lookup"><span data-stu-id="8f3f2-169">DialogA</span></span> | <span data-ttu-id="8f3f2-170">ControlA</span><span class="sxs-lookup"><span data-stu-id="8f3f2-170">ControlA</span></span> | <span data-ttu-id="8f3f2-171">Deaktivieren</span><span class="sxs-lookup"><span data-stu-id="8f3f2-171">Disable</span></span> | <span data-ttu-id="8f3f2-172">Installiert</span><span class="sxs-lookup"><span data-stu-id="8f3f2-172">Installed</span></span>                      |
| <span data-ttu-id="8f3f2-173">Dialoga</span><span class="sxs-lookup"><span data-stu-id="8f3f2-173">DialogA</span></span> | <span data-ttu-id="8f3f2-174">ControlA</span><span class="sxs-lookup"><span data-stu-id="8f3f2-174">ControlA</span></span> | <span data-ttu-id="8f3f2-175">Anzeigen</span><span class="sxs-lookup"><span data-stu-id="8f3f2-175">Show</span></span>    | <span data-ttu-id="8f3f2-176">Nicht installiert</span><span class="sxs-lookup"><span data-stu-id="8f3f2-176">NOT Installed</span></span>                  |
| <span data-ttu-id="8f3f2-177">Dialoga</span><span class="sxs-lookup"><span data-stu-id="8f3f2-177">DialogA</span></span> | <span data-ttu-id="8f3f2-178">ControlA</span><span class="sxs-lookup"><span data-stu-id="8f3f2-178">ControlA</span></span> | <span data-ttu-id="8f3f2-179">Aktivieren</span><span class="sxs-lookup"><span data-stu-id="8f3f2-179">Enable</span></span>  | <span data-ttu-id="8f3f2-180">Nicht installiert</span><span class="sxs-lookup"><span data-stu-id="8f3f2-180">NOT Installed</span></span>                  |



 

## <a name="validation"></a><span data-ttu-id="8f3f2-181">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="8f3f2-181">Validation</span></span>

<dl>

[<span data-ttu-id="8f3f2-182">ICE03</span><span class="sxs-lookup"><span data-stu-id="8f3f2-182">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="8f3f2-183">ICE06</span><span class="sxs-lookup"><span data-stu-id="8f3f2-183">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="8f3f2-184">ICE17</span><span class="sxs-lookup"><span data-stu-id="8f3f2-184">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="8f3f2-185">ICE32</span><span class="sxs-lookup"><span data-stu-id="8f3f2-185">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="8f3f2-186">ICE46</span><span class="sxs-lookup"><span data-stu-id="8f3f2-186">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="8f3f2-187">ICE79</span><span class="sxs-lookup"><span data-stu-id="8f3f2-187">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="8f3f2-188">ICE86</span><span class="sxs-lookup"><span data-stu-id="8f3f2-188">ICE86</span></span>](ice86.md)  
</dl>

 

 



