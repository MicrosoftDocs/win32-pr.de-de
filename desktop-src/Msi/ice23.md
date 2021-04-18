---
description: ICE23 überprüft die Aktivier Reihenfolge der Steuerelemente für jedes Dialogfeld.
ms.assetid: d425f8c6-4615-439d-8194-3a0325eb3cc3
title: ICE23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c1823a70e50d7dd3c42c2e90d6a2d0f11f2fa5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368025"
---
# <a name="ice23"></a><span data-ttu-id="a7fce-103">ICE23</span><span class="sxs-lookup"><span data-stu-id="a7fce-103">ICE23</span></span>

<span data-ttu-id="a7fce-104">ICE23 überprüft die Aktivier Reihenfolge der Steuerelemente für jedes Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="a7fce-104">ICE23 validates the control tab order for each dialog box.</span></span>

<span data-ttu-id="a7fce-105">ICE23 überprüft Folgendes in der Dialog Feld [Tabelle](dialog-table.md) und der [Steuerelement Tabelle](control-table.md):</span><span class="sxs-lookup"><span data-stu-id="a7fce-105">ICE23 validates the following in the [Dialog table](dialog-table.md) and [Control table](control-table.md):</span></span>

-   <span data-ttu-id="a7fce-106">Jeder Datensatz in der Dialogfeld Tabelle gibt ein Steuerelement in der ersten Spalte des Steuer Elements an \_ , das im Dialogfeld vorhanden ist, das in der Dialogfeld Spalte angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a7fce-106">That every record in the Dialog table specifies a control in the Control\_First column that exists in the dialog box specified by the Dialog column.</span></span>
-   <span data-ttu-id="a7fce-107">Jeder Datensatz in der Steuerelement Tabelle gibt ein Steuerelement in der \_ nächsten Spalte des Steuer Elements an, das sich im gleichen Dialogfeld befindet wie das Steuerelement, das in der Steuerelement Spalte aufgelistet ist, oder \_ das nächste Steuerelement enthält den Nullwert</span><span class="sxs-lookup"><span data-stu-id="a7fce-107">That every record in the Control table specifies a control in the Control\_Next column that is on the same dialog as the control listed in the Control column, or Control\_Next contains the Null value.</span></span>
-   <span data-ttu-id="a7fce-108">Nach den nachfolgendes Steuerelementen des Steuer Elements in der Steuerelement \_ Tabelle wird eine einzelne, geschlossene Schleife erstellt, die zum ursprünglichen Steuerelement zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="a7fce-108">That following the Control\_Next entries from control to control in the Control table makes a single, closed, loop that comes back to the initial control.</span></span> <span data-ttu-id="a7fce-109">Nicht jedes Steuerelement muss sich in der Schleife befinden, aber die Schleife muss jedes Steuerelement durchlaufen, das über einen Eintrag in der nächsten Spalte des Steuer Elements verfügt \_ .</span><span class="sxs-lookup"><span data-stu-id="a7fce-109">Not every control needs to be in the loop, but the loop must pass through every control that has an entry in the Control\_Next column.</span></span>

## <a name="result"></a><span data-ttu-id="a7fce-110">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="a7fce-110">Result</span></span>

<span data-ttu-id="a7fce-111">ICE23 gibt eine Fehlermeldung aus, wenn die Aktivier Reihenfolge der Steuerelemente im Dialogfeld keine einzelne geschlossene Schleife bildet.</span><span class="sxs-lookup"><span data-stu-id="a7fce-111">ICE23 posts an error message if the tab order of controls does not form a single closed loop in the dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="a7fce-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a7fce-112">Example</span></span>

<span data-ttu-id="a7fce-113">ICE23 gibt die folgenden Fehlermeldungen für das gezeigte Beispiel an.</span><span class="sxs-lookup"><span data-stu-id="a7fce-113">ICE23 would post the following error messages for the example shown.</span></span>

-   <span data-ttu-id="a7fce-114">Dialog1 hat nicht zuerst das Steuerelement \_ .</span><span class="sxs-lookup"><span data-stu-id="a7fce-114">Dialog1 has no Control\_First.</span></span>
-   <span data-ttu-id="a7fce-115">Control \_ First von Dialog Dialog2 bezieht sich auf das nicht vorhandene Steuerelement controlx.</span><span class="sxs-lookup"><span data-stu-id="a7fce-115">Control\_First of dialog Dialog2 refers to nonexistent control ControlX.</span></span>
-   <span data-ttu-id="a7fce-116">Dialog3 hat die Reihenfolge der aktivierbaren Registerkarten bei Steuerungs kontrolllb.</span><span class="sxs-lookup"><span data-stu-id="a7fce-116">Dialog3 has dead-end tab order at control ControlB.</span></span>
-   <span data-ttu-id="a7fce-117">Dialog4 hat eine falsch formatierte Aktivier Reihenfolge bei Steuerungs kontrolllc</span><span class="sxs-lookup"><span data-stu-id="a7fce-117">Dialog4 has malformed tab order at control ControlC</span></span>
-   <span data-ttu-id="a7fce-118">Dialog5 hat eine falsch formatierte Aktivier Reihenfolge bei Steuerungs kontrolllc.</span><span class="sxs-lookup"><span data-stu-id="a7fce-118">Dialog5 has malformed tab order at control ControlC.</span></span>
-   <span data-ttu-id="a7fce-119">Das Steuerelement \_ neben Control Dialog6. controlc ist mit einem unbekannten Steuerelement verknüpft.</span><span class="sxs-lookup"><span data-stu-id="a7fce-119">Control\_Next of control Dialog6.ControlC links to unknown control.</span></span>

<span data-ttu-id="a7fce-120">[Dialog Feld Tabelle](dialog-table.md) (teilweise)</span><span class="sxs-lookup"><span data-stu-id="a7fce-120">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="a7fce-121">Dialog</span><span class="sxs-lookup"><span data-stu-id="a7fce-121">Dialog</span></span>  | <span data-ttu-id="a7fce-122">\_Zuerst Steuern</span><span class="sxs-lookup"><span data-stu-id="a7fce-122">Control\_First</span></span> |
|---------|----------------|
| <span data-ttu-id="a7fce-123">Dialog1</span><span class="sxs-lookup"><span data-stu-id="a7fce-123">Dialog1</span></span> |                |
| <span data-ttu-id="a7fce-124">Dialog2</span><span class="sxs-lookup"><span data-stu-id="a7fce-124">Dialog2</span></span> | <span data-ttu-id="a7fce-125">Controlx</span><span class="sxs-lookup"><span data-stu-id="a7fce-125">ControlX</span></span>       |
| <span data-ttu-id="a7fce-126">Dialog3</span><span class="sxs-lookup"><span data-stu-id="a7fce-126">Dialog3</span></span> | <span data-ttu-id="a7fce-127">ControlA</span><span class="sxs-lookup"><span data-stu-id="a7fce-127">ControlA</span></span>       |
| <span data-ttu-id="a7fce-128">Dialog4</span><span class="sxs-lookup"><span data-stu-id="a7fce-128">Dialog4</span></span> | <span data-ttu-id="a7fce-129">ControlA</span><span class="sxs-lookup"><span data-stu-id="a7fce-129">ControlA</span></span>       |
| <span data-ttu-id="a7fce-130">Dialog5</span><span class="sxs-lookup"><span data-stu-id="a7fce-130">Dialog5</span></span> | <span data-ttu-id="a7fce-131">ControlA</span><span class="sxs-lookup"><span data-stu-id="a7fce-131">ControlA</span></span>       |



 

<span data-ttu-id="a7fce-132">[Control-Tabelle](control-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="a7fce-132">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="a7fce-133">Dialog</span><span class="sxs-lookup"><span data-stu-id="a7fce-133">Dialog</span></span>  | <span data-ttu-id="a7fce-134">Control</span><span class="sxs-lookup"><span data-stu-id="a7fce-134">Control</span></span>  | <span data-ttu-id="a7fce-135">Nächstes Steuerelement \_</span><span class="sxs-lookup"><span data-stu-id="a7fce-135">Control\_Next</span></span> |
|---------|----------|---------------|
| <span data-ttu-id="a7fce-136">Dialog1</span><span class="sxs-lookup"><span data-stu-id="a7fce-136">Dialog1</span></span> | <span data-ttu-id="a7fce-137">ControlA</span><span class="sxs-lookup"><span data-stu-id="a7fce-137">ControlA</span></span> |               |
| <span data-ttu-id="a7fce-138">Dialog1</span><span class="sxs-lookup"><span data-stu-id="a7fce-138">Dialog1</span></span> | <span data-ttu-id="a7fce-139">Controlb</span><span class="sxs-lookup"><span data-stu-id="a7fce-139">ControlB</span></span> | <span data-ttu-id="a7fce-140">ControlA</span><span class="sxs-lookup"><span data-stu-id="a7fce-140">ControlA</span></span>      |
| <span data-ttu-id="a7fce-141">Dialog2</span><span class="sxs-lookup"><span data-stu-id="a7fce-141">Dialog2</span></span> | <span data-ttu-id="a7fce-142">ControlA</span><span class="sxs-lookup"><span data-stu-id="a7fce-142">ControlA</span></span> | <span data-ttu-id="a7fce-143">Controlb</span><span class="sxs-lookup"><span data-stu-id="a7fce-143">ControlB</span></span>      |
| <span data-ttu-id="a7fce-144">Dialog2</span><span class="sxs-lookup"><span data-stu-id="a7fce-144">Dialog2</span></span> | <span data-ttu-id="a7fce-145">Controlb</span><span class="sxs-lookup"><span data-stu-id="a7fce-145">ControlB</span></span> | <span data-ttu-id="a7fce-146">ControlA</span><span class="sxs-lookup"><span data-stu-id="a7fce-146">ControlA</span></span>      |
| <span data-ttu-id="a7fce-147">Dialog3</span><span class="sxs-lookup"><span data-stu-id="a7fce-147">Dialog3</span></span> | <span data-ttu-id="a7fce-148">ControlA</span><span class="sxs-lookup"><span data-stu-id="a7fce-148">ControlA</span></span> | <span data-ttu-id="a7fce-149">Controlb</span><span class="sxs-lookup"><span data-stu-id="a7fce-149">ControlB</span></span>      |
| <span data-ttu-id="a7fce-150">Dialog3</span><span class="sxs-lookup"><span data-stu-id="a7fce-150">Dialog3</span></span> | <span data-ttu-id="a7fce-151">Controlb</span><span class="sxs-lookup"><span data-stu-id="a7fce-151">ControlB</span></span> |               |
| <span data-ttu-id="a7fce-152">Dialog4</span><span class="sxs-lookup"><span data-stu-id="a7fce-152">Dialog4</span></span> | <span data-ttu-id="a7fce-153">ControlA</span><span class="sxs-lookup"><span data-stu-id="a7fce-153">ControlA</span></span> | <span data-ttu-id="a7fce-154">Controlb</span><span class="sxs-lookup"><span data-stu-id="a7fce-154">ControlB</span></span>      |
| <span data-ttu-id="a7fce-155">Dialog4</span><span class="sxs-lookup"><span data-stu-id="a7fce-155">Dialog4</span></span> | <span data-ttu-id="a7fce-156">Controlb</span><span class="sxs-lookup"><span data-stu-id="a7fce-156">ControlB</span></span> | <span data-ttu-id="a7fce-157">Controlc</span><span class="sxs-lookup"><span data-stu-id="a7fce-157">ControlC</span></span>      |
| <span data-ttu-id="a7fce-158">Dialog4</span><span class="sxs-lookup"><span data-stu-id="a7fce-158">Dialog4</span></span> | <span data-ttu-id="a7fce-159">Controlc</span><span class="sxs-lookup"><span data-stu-id="a7fce-159">ControlC</span></span> | <span data-ttu-id="a7fce-160">Controlb</span><span class="sxs-lookup"><span data-stu-id="a7fce-160">ControlB</span></span>      |
| <span data-ttu-id="a7fce-161">Dialog5</span><span class="sxs-lookup"><span data-stu-id="a7fce-161">Dialog5</span></span> | <span data-ttu-id="a7fce-162">ControlA</span><span class="sxs-lookup"><span data-stu-id="a7fce-162">ControlA</span></span> | <span data-ttu-id="a7fce-163">Controlb</span><span class="sxs-lookup"><span data-stu-id="a7fce-163">ControlB</span></span>      |
| <span data-ttu-id="a7fce-164">Dialog5</span><span class="sxs-lookup"><span data-stu-id="a7fce-164">Dialog5</span></span> | <span data-ttu-id="a7fce-165">Controlb</span><span class="sxs-lookup"><span data-stu-id="a7fce-165">ControlB</span></span> | <span data-ttu-id="a7fce-166">Controlc</span><span class="sxs-lookup"><span data-stu-id="a7fce-166">ControlC</span></span>      |
| <span data-ttu-id="a7fce-167">Dialog5</span><span class="sxs-lookup"><span data-stu-id="a7fce-167">Dialog5</span></span> | <span data-ttu-id="a7fce-168">Controlc</span><span class="sxs-lookup"><span data-stu-id="a7fce-168">ControlC</span></span> | <span data-ttu-id="a7fce-169">ControlA</span><span class="sxs-lookup"><span data-stu-id="a7fce-169">ControlA</span></span>      |
| <span data-ttu-id="a7fce-170">Dialog5</span><span class="sxs-lookup"><span data-stu-id="a7fce-170">Dialog5</span></span> | <span data-ttu-id="a7fce-171">ControlD</span><span class="sxs-lookup"><span data-stu-id="a7fce-171">ControlD</span></span> | <span data-ttu-id="a7fce-172">ControlA</span><span class="sxs-lookup"><span data-stu-id="a7fce-172">ControlA</span></span>      |
| <span data-ttu-id="a7fce-173">Dialog6</span><span class="sxs-lookup"><span data-stu-id="a7fce-173">Dialog6</span></span> | <span data-ttu-id="a7fce-174">ControlA</span><span class="sxs-lookup"><span data-stu-id="a7fce-174">ControlA</span></span> | <span data-ttu-id="a7fce-175">Controlb</span><span class="sxs-lookup"><span data-stu-id="a7fce-175">ControlB</span></span>      |
| <span data-ttu-id="a7fce-176">Dialog6</span><span class="sxs-lookup"><span data-stu-id="a7fce-176">Dialog6</span></span> | <span data-ttu-id="a7fce-177">Controlb</span><span class="sxs-lookup"><span data-stu-id="a7fce-177">ControlB</span></span> | <span data-ttu-id="a7fce-178">Controlc</span><span class="sxs-lookup"><span data-stu-id="a7fce-178">ControlC</span></span>      |
| <span data-ttu-id="a7fce-179">Dialog6</span><span class="sxs-lookup"><span data-stu-id="a7fce-179">Dialog6</span></span> | <span data-ttu-id="a7fce-180">Controlc</span><span class="sxs-lookup"><span data-stu-id="a7fce-180">ControlC</span></span> | <span data-ttu-id="a7fce-181">Controlx</span><span class="sxs-lookup"><span data-stu-id="a7fce-181">ControlX</span></span>      |
| <span data-ttu-id="a7fce-182">Dialog6</span><span class="sxs-lookup"><span data-stu-id="a7fce-182">Dialog6</span></span> | <span data-ttu-id="a7fce-183">ControlD</span><span class="sxs-lookup"><span data-stu-id="a7fce-183">ControlD</span></span> | <span data-ttu-id="a7fce-184">ControlA</span><span class="sxs-lookup"><span data-stu-id="a7fce-184">ControlA</span></span>      |



 

<span data-ttu-id="a7fce-185">Beachten Sie die folgenden Tabellen, um diese Fehler zu beheben, und nehmen Sie die angezeigten Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="a7fce-185">To fix these errors note the following in the above tables and make the indicated changes.</span></span>

<span data-ttu-id="a7fce-186">Nicht jede Zeile in der Dialog Tabelle verfügt über ein Steuerelement, das in der ersten Spalte des Steuer Elements angegeben ist \_ .</span><span class="sxs-lookup"><span data-stu-id="a7fce-186">Not every row in the Dialog table has a control specified in the Control\_First column.</span></span> <span data-ttu-id="a7fce-187">Ändern Sie die Control \_ First-Spalte des Dialog1-Datensatzes in der Dialog Feld Tabelle in ein Steuerelement, das in Dialog1 vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a7fce-187">Change the Control\_First column of the Dialog1 record in the Dialog table to a control that exists in Dialog1.</span></span>

<span data-ttu-id="a7fce-188">Nicht jede Zeile in der Dialogfeld Tabelle verfügt über ein Steuerelement, das in der ersten Spalte des Steuer Elements angegeben ist \_ , die im Dialog Feld vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a7fce-188">Not every row in the Dialog table has a control specified in the Control\_First column that exists on the dialog box.</span></span> <span data-ttu-id="a7fce-189">Ändern Sie die Control \_ First-Spalte des Dialog2 in ein Steuerelement, das in Dialog2 vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a7fce-189">Change the Control\_First column of the Dialog2 to a control that exists in Dialog2.</span></span>

<span data-ttu-id="a7fce-190">Nach dem Steuern der \_ nächsten Einträge in der Steuerelement Tabelle von Steuerelement zu Steuerelement wird in jedem Fall keine geschlossene Schleife durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="a7fce-190">Following the Control\_Next entries in the Control table from control to control does not make a closed loop in every case.</span></span> <span data-ttu-id="a7fce-191">Ändern Sie das Steuerelement \_ Next column for controlb in Dialog3 to ControlA.</span><span class="sxs-lookup"><span data-stu-id="a7fce-191">Change the Control\_Next column for ControlB in Dialog3 to ControlA.</span></span>

<span data-ttu-id="a7fce-192">Nach dem Steuern der Steuerelemente \_ in der Steuerelement Tabelle von Steuerelement zu Steuerelement wird in jedem Fall nicht mehr auf das ursprüngliche Steuerelement zurückgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7fce-192">Following the Control\_Next entries in the Control table from control to control does not lead back to the initial control in every case.</span></span> <span data-ttu-id="a7fce-193">Ändern Sie das Steuerelement \_ Next column for controlc in Dialog4, um auf ControlA zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="a7fce-193">Change the Control\_Next column for ControlC in Dialog4 to refer to ControlA.</span></span>

<span data-ttu-id="a7fce-194">Wenn Sie das Steuerelement \_ Nächste Einträge in der Steuerelement Tabelle von Steuerelement zu Steuerung befolgen, werden nicht alle Steuerelemente im Dialogfeld durch einen Eintrag in der nächsten Spalte des-Steuer Elements weitergeleitet \_ .</span><span class="sxs-lookup"><span data-stu-id="a7fce-194">Following the Control\_Next entries in the Control table from control to control does not pass through every control in the dialog box having an entry in the Control\_Next column.</span></span> <span data-ttu-id="a7fce-195">Ändern Sie das Steuerelement \_ Next column for controlc in Dialog5 to ControlD.</span><span class="sxs-lookup"><span data-stu-id="a7fce-195">Change the Control\_Next column for ControlC in Dialog5 to ControlD.</span></span>

<span data-ttu-id="a7fce-196">Das \_ nächste Steuerelement verweist nicht auf ein gültiges Steuerelement, das sich im gleichen Dialogfeld wie das Steuerelement befindet, das in der Steuerelement Spalte aufgelistet ist.</span><span class="sxs-lookup"><span data-stu-id="a7fce-196">Control\_Next does not refer to a valid control that is in the same dialog as the control listed in the Control column.</span></span> <span data-ttu-id="a7fce-197">Ändern Sie das Steuerelement \_ Next column for controlc in Dialog6, um auf ControlD zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="a7fce-197">Change the Control\_Next column for ControlC in Dialog6 to refer to ControlD.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7fce-198">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a7fce-198">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7fce-199">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="a7fce-199">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



