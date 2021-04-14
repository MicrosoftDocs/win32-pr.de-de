---
description: Ein Fehler Dialogfeld ist ein modales Dialogfeld Feld, in dem eine Fehlermeldung angezeigt wird. In jeder Installation kann mehr als ein Fehler Dialogfeld vorhanden sein.
ms.assetid: 11d4fe8b-ec5f-4576-95e5-c86344f0195c
title: Fehler Dialogfeld
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a153f5e6ee38235f830937d794a9ca9b81314583
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527251"
---
# <a name="error-dialog"></a><span data-ttu-id="d7988-104">Fehler Dialogfeld</span><span class="sxs-lookup"><span data-stu-id="d7988-104">Error Dialog</span></span>

<span data-ttu-id="d7988-105">Ein Fehler Dialogfeld ist ein modales Dialogfeld Feld, in dem eine Fehlermeldung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d7988-105">An Error dialog box is a modal dialog box box that displays an error message.</span></span> <span data-ttu-id="d7988-106">In jeder Installation kann mehr als ein Fehler Dialogfeld vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="d7988-106">More than one Error dialog box can exist in each installation.</span></span>

<span data-ttu-id="d7988-107">Eine ErrorDialog-Eigenschaft muss festgelegt werden, die angibt, welches Dialogfeld verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7988-107">An ErrorDialog property needs to be set that specifies which dialog box is to be used.</span></span> <span data-ttu-id="d7988-108">Wenn diese Eigenschaft nicht festgelegt ist oder nicht auf ein gültiges Fehler Dialogfeld zeigt, werden die Fehlermeldungen nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7988-108">If this property is not set or does not point to a valid Error dialog box, then the error messages will not be displayed.</span></span> <span data-ttu-id="d7988-109">In diesem Fall wird der Fehler nur mit einer Warnung über das fehlende Dialogfeld protokolliert.</span><span class="sxs-lookup"><span data-stu-id="d7988-109">In this case, the error is only logged with a warning about the missing dialog box.</span></span>

<span data-ttu-id="d7988-110">Für ein Fehler Dialogfeld muss das [Fehler Dialogfeld des Dialog](error-dialog-style-bit.md) Felds festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="d7988-110">An Error dialog box must have the [Error Dialog style bit](error-dialog-style-bit.md) set.</span></span> <span data-ttu-id="d7988-111">Das Dialogfeld muss über ein [Text Steuer](text-control.md) Element namens ErrorText verfügen.</span><span class="sxs-lookup"><span data-stu-id="d7988-111">The dialog box must have a [Text control](text-control.md) named ErrorText.</span></span> <span data-ttu-id="d7988-112">Der Datensatz für das Fehler Dialogfeld in der [Dialogfeld Tabelle](dialog-table.md) muss das ErrorText-Steuerelement in das erste Feld des Steuer Elements eingegeben haben \_ .</span><span class="sxs-lookup"><span data-stu-id="d7988-112">The record for the Error dialog box in the [Dialog table](dialog-table.md) must have the ErrorText control entered into the Control\_First field.</span></span>

<span data-ttu-id="d7988-113">Das Dialogfeld muss sieben [Pushbuttons](pushbutton-control.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="d7988-113">The dialog box must contain seven [PushButtons](pushbutton-control.md).</span></span> <span data-ttu-id="d7988-114">Alle diese Schaltflächen geben das [EndDialog](enddialog-controlevent.md) -ControlEvent in der [ControlEvent-Tabelle](controlevent-table.md)an.</span><span class="sxs-lookup"><span data-stu-id="d7988-114">All of these buttons specify the [EndDialog](enddialog-controlevent.md) ControlEvent in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="d7988-115">Jede Schaltfläche gibt eines der folgenden Attribute an: **errorabort**, **errorcancel**, **errorignore**, **errorno**, **errorok**, **errorretry**, **erroryes**.</span><span class="sxs-lookup"><span data-stu-id="d7988-115">Each button specifies one of the following attributes: **ErrorAbort**, **ErrorCancel**, **ErrorIgnore**, **ErrorNo**, **ErrorOk**, **ErrorRetry**, **ErrorYes**.</span></span>

> [!Note]  
> <span data-ttu-id="d7988-116">Der Fokus dieser Steuerelemente sollte nicht durch die Verwendung der nächsten Spalte des Steuer Elements \_ in der [Steuerelement Tabelle](control-table.md)verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="d7988-116">The focus of these controls should not be linked through the use of the Control\_Next column in the [Control table](control-table.md).</span></span>

 

<span data-ttu-id="d7988-117">Diese Schaltflächen sollten in etwa der gleichen Position im Dialogfeld platziert werden, da bei der Erstellung nur eine Teilmenge dieser sieben Schaltflächen erstellt wird, abhängig von der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d7988-117">These buttons should be placed in approximately the same position in the dialog box because when it is created, only a subset of these seven buttons is created, depending on the message.</span></span> <span data-ttu-id="d7988-118">Die X-Koordinate der Schaltflächen wird so geändert, dass die angezeigten Schaltflächen gleichmäßig verteilt sind.</span><span class="sxs-lookup"><span data-stu-id="d7988-118">The X coordinate of the buttons is modified so the buttons that are displayed are evenly spaced.</span></span> <span data-ttu-id="d7988-119">Die Y-Koordinate, die Höhe und die Breite der Schaltflächen sind unverändert.</span><span class="sxs-lookup"><span data-stu-id="d7988-119">The Y coordinate, height, and width of the buttons are unchanged.</span></span> <span data-ttu-id="d7988-120">Da die Schaltflächen horizontal angeordnet werden, kann kein anderes Steuerelement im selben horizontalen Bereich des Dialog Felds platziert werden.</span><span class="sxs-lookup"><span data-stu-id="d7988-120">Because the buttons are arranged horizontally, no other control can be placed in the same horizontal region of the dialog box.</span></span>

<span data-ttu-id="d7988-121">Wenn ein Fehler Dialogfeld angezeigt wird, werden die Felder Steuerelement \_ Standard und Steuerelement \_ Abbruch in der [Dialogfeld Tabelle](dialog-table.md) ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d7988-121">For an Error dialog box, the Control\_Default and Control\_Cancel fields in the [Dialog table](dialog-table.md) are ignored.</span></span> <span data-ttu-id="d7988-122">Das Steuerelement \_ First-Feld für ein Fehler Dialogfeld muss das ErrorText-Steuerelement angeben.</span><span class="sxs-lookup"><span data-stu-id="d7988-122">The Control\_First field for an Error dialog box must specify the ErrorText control.</span></span>

<span data-ttu-id="d7988-123">Wenn in diesem Dialogfeld ein [Symbol Steuer](icon-control.md) Element mit dem Namen erroricon enthalten ist, werden die folgenden standardmäßigen Windows-Symbole angezeigt:</span><span class="sxs-lookup"><span data-stu-id="d7988-123">If an [Icon control](icon-control.md) named ErrorIcon is included on this dialog, the following standard Windows icons are displayed:</span></span>

-   <span data-ttu-id="d7988-124">IDI- \_ Fehler als Antwort auf imtfatalexit-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="d7988-124">IDI\_ERROR in response to imtFatalExit messages.</span></span>
-   <span data-ttu-id="d7988-125">IDI \_ -Warnung als Reaktion auf imterror-und imtwarning-Meldungen.</span><span class="sxs-lookup"><span data-stu-id="d7988-125">IDI\_WARNING in response to imtError and imtWarning messages.</span></span>
-   <span data-ttu-id="d7988-126">IDI- \_ Informationen als Reaktion auf imtoutofdiskspace-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="d7988-126">IDI\_INFORMATION in response to imtOutOfDiskSpace messages.</span></span>

<span data-ttu-id="d7988-127">Das erroricon-Steuerelement sollte mit dem [FixedSize-Steuer](fixedsize-control-attribute.md) Element festgelegt werden, um eine nicht ordnungsgemäße Anpassung der standardmäßigen Windows-Symbole zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="d7988-127">The ErrorIcon control should be created with the [FixedSize control attribute](fixedsize-control-attribute.md) set to avoid improper sizing of the standard Windows icons.</span></span>

 

 



