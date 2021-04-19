---
description: Wenn dieses Bit festgelegt ist, ist das Dialogfeld ein Fehler Dialogfeld.
ms.assetid: a8a95f6a-6465-433b-98a4-95281cddedd3
title: Fehler Dialogfeld-Stilbit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ff3e4868cf1941f80be4f7b2d70068ec949a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353138"
---
# <a name="error-dialog-style-bit"></a><span data-ttu-id="32f74-103">Fehler Dialogfeld-Stilbit</span><span class="sxs-lookup"><span data-stu-id="32f74-103">Error Dialog Style Bit</span></span>

<span data-ttu-id="32f74-104">Wenn dieses Bit festgelegt ist, ist das Dialogfeld ein Fehler Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="32f74-104">If this bit is set, the dialog box is an error dialog.</span></span>

<span data-ttu-id="32f74-105">Es können mehrere Dialogfelder mit diesem Stil vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="32f74-105">There can be more than one dialog with this style.</span></span> <span data-ttu-id="32f74-106">Die **ErrorDialog** -Eigenschaft bestimmt, welches Dialogfeld als Fehler Dialogfeld verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="32f74-106">The **ErrorDialog** property determines which dialog is used as an error dialog.</span></span> <span data-ttu-id="32f74-107">Bei dem ausgewählten Dialogfeld kann es sich nur um einen Benutzer handeln, für den dieses Stilbit festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="32f74-107">The selected dialog can be only one of those that have this style bit set.</span></span> <span data-ttu-id="32f74-108">Das Fehler Dialogfeld muss über ein statisches Text Steuerelement namens ErrorText verfügen.</span><span class="sxs-lookup"><span data-stu-id="32f74-108">The error dialog must have a static text control named ErrorText.</span></span> <span data-ttu-id="32f74-109">Dieses Steuerelement empfängt den Text der Fehlermeldung.</span><span class="sxs-lookup"><span data-stu-id="32f74-109">This control receives the text of the error message.</span></span> <span data-ttu-id="32f74-110">Das Dialogfeld sollte auch über die sieben pushschaltflächen verfügen, die den möglichen Rückgabe Werten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="32f74-110">The dialog should also have the seven push buttons corresponding to the possible return values.</span></span> <span data-ttu-id="32f74-111">Die Fehlermeldung bestimmt, welche dieser Schaltflächen tatsächlich angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="32f74-111">The error message determines which of these buttons are actually displayed.</span></span> <span data-ttu-id="32f74-112">Die angezeigten Schaltflächen werden neu angeordnet, sodass Sie im Dialogfeld gleichmäßig verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="32f74-112">The displayed buttons are rearranged so they are evenly distributed on the dialog.</span></span> <span data-ttu-id="32f74-113">Diese Neuanordnung ändert die X-Koordinate der Schaltflächen, jedoch nicht die anderen drei Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="32f74-113">This rearrangement changes the X coordinate of the buttons, but not the other three coordinates.</span></span> <span data-ttu-id="32f74-114">Daher ist es ratsam, dass kein anderes Steuerelement im selben horizontalen Bereich des Dialog Felds wie die Schaltflächen erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="32f74-114">Therefore it is advisable that no other control should be authored in the same horizontal region of the dialog as the buttons.</span></span> <span data-ttu-id="32f74-115">Wenn in der Fehlermeldung keine Schaltfläche angegeben ist, wird die Schaltfläche **OK** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="32f74-115">If the error message specifies no button, the **OK** button is displayed.</span></span> <span data-ttu-id="32f74-116">Die **Standard** Schaltfläche, die ersten aktiven Steuerelemente und Schaltflächen Werte **Abbrechen** werden bei einem Fehler Dialogfeld ignoriert.</span><span class="sxs-lookup"><span data-stu-id="32f74-116">The **Default** button, First active control and **Cancel** button values are ignored for an error dialog.</span></span> <span data-ttu-id="32f74-117">Die in der Fehlermeldung definierte **Standard** Schaltfläche wird allen drei Werten zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="32f74-117">The **Default** button defined in the error message will be assigned to all three values.</span></span> <span data-ttu-id="32f74-118">Der Effekt, dass diese Schaltflächen gedrückt werden, muss in der [ControlEvent-Tabelle](controlevent-table.md) genau wie für alle anderen Schaltflächen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="32f74-118">The effect of pushing these buttons have to be defined in the [ControlEvent table](controlevent-table.md) just like for all other buttons.</span></span> <span data-ttu-id="32f74-119">Der Titel des Dialog Felds wird auf eine Weise erstellt, die anderen Dialogfeldern ähnelt.</span><span class="sxs-lookup"><span data-stu-id="32f74-119">The title of the dialog is authored in a way similar to other dialogs.</span></span> <span data-ttu-id="32f74-120">Sie kann von der Fehlermeldung überschrieben werden, wenn Sie einen Header Text nach der Schaltflächen Liste angibt.</span><span class="sxs-lookup"><span data-stu-id="32f74-120">It can get overwritten by the error message if it specifies a header text after the button list.</span></span>

## <a name="value"></a><span data-ttu-id="32f74-121">Wert</span><span class="sxs-lookup"><span data-stu-id="32f74-121">Value</span></span>



| <span data-ttu-id="32f74-122">Decimal</span><span class="sxs-lookup"><span data-stu-id="32f74-122">Decimal</span></span> | <span data-ttu-id="32f74-123">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="32f74-123">Hexadecimal</span></span> | <span data-ttu-id="32f74-124">Konstante</span><span class="sxs-lookup"><span data-stu-id="32f74-124">Constant</span></span>                       |
|---------|-------------|--------------------------------|
| <span data-ttu-id="32f74-125">65536</span><span class="sxs-lookup"><span data-stu-id="32f74-125">65536</span></span>   | <span data-ttu-id="32f74-126">0x00010000</span><span class="sxs-lookup"><span data-stu-id="32f74-126">0x00010000</span></span>  | <span data-ttu-id="32f74-127">**msidbdialogattributeserror**</span><span class="sxs-lookup"><span data-stu-id="32f74-127">**msidbDialogAttributesError**</span></span> |



 

 

 



