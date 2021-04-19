---
description: Übersicht über das Anzeigen des Eingabe Bereichs.
ms.assetid: 6301dde1-e46b-42a0-ae0b-ccd984e9199b
title: Anzeigen des Eingabe Bereichs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1fa8404cadd7c40b0185d60b574ac7d8ec77ced
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362774"
---
# <a name="displaying-the-input-panel"></a><span data-ttu-id="213e4-103">Anzeigen des Eingabe Bereichs</span><span class="sxs-lookup"><span data-stu-id="213e4-103">Displaying the Input Panel</span></span>

<span data-ttu-id="213e4-104">\[" [**Pinputpanel**](peninputpanel-class.md) " wurde durch " [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) " ersetzt ("[Microsoft. Ink. TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) " für verwalteten Code).</span><span class="sxs-lookup"><span data-stu-id="213e4-104">\[[**PenInputPanel**](peninputpanel-class.md) has been replaced by [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ([Microsoft.Ink.TextInput](/previous-versions/dotnet/netframework-3.5/ms581554(v=vs.90)) for managed code).</span></span> <span data-ttu-id="213e4-105">Weitere Informationen finden Sie im Abschnitt [Programmieren des Text Eingabe](programming-the-text-input-panel.md)Bereichs.\]</span><span class="sxs-lookup"><span data-stu-id="213e4-105">Please refer to the [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="213e4-106">Die Reihenfolge der verschiedenen Fokus Ereignisse für ein Steuerelement lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="213e4-106">The order of the various focus events for a control is as follows:</span></span>

-   [<span data-ttu-id="213e4-107">Control. Enter</span><span class="sxs-lookup"><span data-stu-id="213e4-107">Control.Enter</span></span>](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1)
-   [<span data-ttu-id="213e4-108">Control. GotFocus</span><span class="sxs-lookup"><span data-stu-id="213e4-108">Control.GotFocus</span></span>](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1)
-   [<span data-ttu-id="213e4-109">Control. Leave</span><span class="sxs-lookup"><span data-stu-id="213e4-109">Control.Leave</span></span>](/dotnet/api/system.windows.forms.control.leave?view=netcore-3.1)
-   [<span data-ttu-id="213e4-110">Control. validieren</span><span class="sxs-lookup"><span data-stu-id="213e4-110">Control.Validating</span></span>](/dotnet/api/system.windows.forms.control.validating?view=netcore-3.1)
-   [<span data-ttu-id="213e4-111">Control. validiert</span><span class="sxs-lookup"><span data-stu-id="213e4-111">Control.Validated</span></span>](/dotnet/api/system.windows.forms.control.validated?view=netcore-3.1)
-   [<span data-ttu-id="213e4-112">Control. LostFocus</span><span class="sxs-lookup"><span data-stu-id="213e4-112">Control.LostFocus</span></span>](/dotnet/api/system.windows.forms.control.lostfocus?view=netcore-3.1)

<span data-ttu-id="213e4-113">Es gibt keine Garantie, dass das Steuerelement den Fokus tatsächlich um den Zeitpunkt hat, zu dem die [Control. Visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) -Eigenschaft geschrieben wird, wenn Sie im [Control. Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) -Ereignishandler festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="213e4-113">There is no guarantee that the control actually has focus by the time the [Control.Visible](/dotnet/api/system.windows.forms.control.visible?view=netcore-3.1) property is written when it is set in the [Control.Enter](/dotnet/api/system.windows.forms.control.enter?view=netcore-3.1) event handler.</span></span> <span data-ttu-id="213e4-114">Das Steuerelement. Enter-Ereignis ist der beste Ort, um [das Objekt "](/previous-versions/ms583923(v=vs.100)) " "" "" "" "" "" "" " [".](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) [](/previous-versions/ms571984(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="213e4-114">The Control.Enter event is the best place to attach the [PenInputPanel](/previous-versions/ms583923(v=vs.100)) object to a control, but the [Control.GotFocus](/dotnet/api/system.windows.forms.control.gotfocus?view=netcore-3.1) event is the best place to change the [PenInputPanel.Visible](/previous-versions/ms571984(v=vs.100)) property.</span></span>

 

 
