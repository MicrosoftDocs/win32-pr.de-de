---
description: Übersicht über bewährte Methoden bei Verwendung des Stift Eingabe Panel-Objekts.
ms.assetid: 5b127743-0c88-4c4c-bcb6-5a91690cd2a1
title: Bewährte Methoden (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd492dfeda94ce9dce056b286ef1989f3389658c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218580"
---
# <a name="best-practices-tablet-pc"></a><span data-ttu-id="7b52b-103">Bewährte Methoden (Tablet PC)</span><span class="sxs-lookup"><span data-stu-id="7b52b-103">Best Practices (Tablet PC)</span></span>

<span data-ttu-id="7b52b-104">Es gibt einige Richtlinien, die Sie beachten sollten, wenn Sie das Objekt " [**pinputpanel**](peninputpanel-class.md) " verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b52b-104">There are a few guidelines to keep in mind when using the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>

-   [<span data-ttu-id="7b52b-105">InkEdit-Steuerelement bevorzugen</span><span class="sxs-lookup"><span data-stu-id="7b52b-105">Prefer InkEdit Control</span></span>](#prefer-inkedit-control)
-   [<span data-ttu-id="7b52b-106">Freihand Modus für InkEdit-Steuerelemente deaktivieren</span><span class="sxs-lookup"><span data-stu-id="7b52b-106">Disable Ink Mode on InkEdit Controls</span></span>](#disable-ink-mode-on-inkedit-controls)
-   [<span data-ttu-id="7b52b-107">Verwenden von fensterlosen Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="7b52b-107">Using Windowless Controls</span></span>](#using-windowless-controls)
-   [<span data-ttu-id="7b52b-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7b52b-108">Related topics</span></span>](#related-topics)

## <a name="prefer-inkedit-control"></a><span data-ttu-id="7b52b-109">InkEdit-Steuerelement bevorzugen</span><span class="sxs-lookup"><span data-stu-id="7b52b-109">Prefer InkEdit Control</span></span>

<span data-ttu-id="7b52b-110">[InkEdit](inkedit-control-reference.md) ist das bevorzugte Steuerelement, an das das Objekt " [**turinputpanel**](peninputpanel-class.md) " angefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b52b-110">[InkEdit](inkedit-control-reference.md) is the preferred control to which to attach the [**PenInputPanel**](peninputpanel-class.md) object.</span></span> <span data-ttu-id="7b52b-111">Das InkEdit-Steuerelement bietet Unterstützung für das [Text Services-Framework (TSF)](text-services-framework.md).</span><span class="sxs-lookup"><span data-stu-id="7b52b-111">The InkEdit control provides support for the [Text Services Framework (TSF)](text-services-framework.md).</span></span>

## <a name="disable-ink-mode-on-inkedit-controls"></a><span data-ttu-id="7b52b-112">Freihand Modus für InkEdit-Steuerelemente deaktivieren</span><span class="sxs-lookup"><span data-stu-id="7b52b-112">Disable Ink Mode on InkEdit Controls</span></span>

<span data-ttu-id="7b52b-113">Legen Sie beim Anfügen an ein [InkEdit](inkedit-control-reference.md) -Steuerelement die Eigenschaft [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) des InkEdit-Steuer Elements auf den Wert [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) fest.</span><span class="sxs-lookup"><span data-stu-id="7b52b-113">When attached to an [InkEdit](inkedit-control-reference.md) control, set the [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property of the InkEdit control to the [**InkMode**](/windows/desktop/api/inked/ne-inked-inkmode) value.</span></span> <span data-ttu-id="7b52b-114">Wenn die Eigenschaft **InkMode** nicht auf den Wert **InkMode** festgelegt ist, interpretiert das InkEdit-Steuerelement den ersten Tap als Strich, übergibt ihn an die Erkennung und fügt den Text in das InkEdit-Steuerelement ein.</span><span class="sxs-lookup"><span data-stu-id="7b52b-114">If the **InkMode** property is not set to the **InkMode** value, the InkEdit control interprets the first tap as a stroke, passes it to the recognizer, and inserts the text in the InkEdit control.</span></span> <span data-ttu-id="7b52b-115">Da Sie bereits [**über ein "**](peninputpanel-class.md) "-Objekt verfügen, das an eine frei Hand Eingabe gebunden ist, ist es nicht erforderlich, dass das InkEdit-Steuerelement auch für die frei Hand Eingabe aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7b52b-115">Since you already have a [**PenInputPanel**](peninputpanel-class.md) object attached to accept ink input, there is no need to have the InkEdit control also enabled for ink input.</span></span>

## <a name="using-windowless-controls"></a><span data-ttu-id="7b52b-116">Verwenden von fensterlosen Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="7b52b-116">Using Windowless Controls</span></span>

<span data-ttu-id="7b52b-117">Wenn ein " [**tzinputpanel**](peninputpanel-class.md) "-Objekt an ein übergeordnetes Fenster angefügt wird, das mehr als ein fensterloses Steuerelement enthält, weiß das Objekt " **tzinputpanel** " nicht, wie die Einfügemarke nachverfolgt werden soll, wenn sich der Fokus zwischen Fenstern untergeordneten Elementen</span><span class="sxs-lookup"><span data-stu-id="7b52b-117">When a [**PenInputPanel**](peninputpanel-class.md) object is attached to a parent window that contains more than one windowless control, the **PenInputPanel** object does not know how to track the caret as focus moves among windowless children.</span></span> <span data-ttu-id="7b52b-118">Handschrift Eingaben können an das falsche untergeordnete Element gesendet werden, wenn der Fokus von einem fensterlosen Steuerelement zu einem anderen verschoben wird, während die Eingabe aussteht.</span><span class="sxs-lookup"><span data-stu-id="7b52b-118">Handwriting input can be sent to the wrong child when focus moves from one windowless control to another while input is pending.</span></span>

<span data-ttu-id="7b52b-119">Um das Objekt " [**pinputpanel**](peninputpanel-class.md) " in einer fensterlosen Umgebung zu verwenden, kann folgendes Verfahren verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="7b52b-119">To use the [**PenInputPanel**](peninputpanel-class.md) object in a windowless environment, the following technique can be used:</span></span>

1.  <span data-ttu-id="7b52b-120">Instanziieren Sie ein [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) -Steuerelement, und positionieren Sie es über dem fensterlosen Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="7b52b-120">Instantiate a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) control and position it over the windowless control.</span></span>
2.  <span data-ttu-id="7b52b-121">Fügen Sie das Objekt " [**tzinputpanel**](peninputpanel-class.md) " an das neue Textfeld-Steuerelement an.</span><span class="sxs-lookup"><span data-stu-id="7b52b-121">Attach the [**PenInputPanel**](peninputpanel-class.md) object to the new text box control.</span></span>
3.  <span data-ttu-id="7b52b-122">Lassen Sie das Textfeld-Steuerelement den erkannten Text aus dem Objekt " [**tzinputpanel**](peninputpanel-class.md) " erfassen.</span><span class="sxs-lookup"><span data-stu-id="7b52b-122">Let the text box control collect the recognized text from the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>
4.  <span data-ttu-id="7b52b-123">Wenn sich der Fokus auf das Textfeld-Steuerelement ändert, wird die [**commitpdinginput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) -Methode des " [**tzinputpanel**](peninputpanel-class.md) "-Objekts aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7b52b-123">When focus changes away from the text box control, call the [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) method of the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>
5.  <span data-ttu-id="7b52b-124">Kopieren Sie den erkannten Text aus dem Textfeld-Steuerelement in das untergeordnete Fenster.</span><span class="sxs-lookup"><span data-stu-id="7b52b-124">Copy the recognized text from the text box control to the windowless child.</span></span>
6.  <span data-ttu-id="7b52b-125">Trennen Sie das Objekt " [**pinputpanel**](peninputpanel-class.md) ", indem Sie die Eigenschaft " [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) " (nur verwalteter Code) oder die Eigenschaft " [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) " auf NULL festlegen.</span><span class="sxs-lookup"><span data-stu-id="7b52b-125">Detach the [**PenInputPanel**](peninputpanel-class.md) object by setting its [AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (managed code only) property or [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow) property to null.</span></span>
7.  <span data-ttu-id="7b52b-126">Löschen Sie das Textfeld-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="7b52b-126">Destroy the text box control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b52b-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7b52b-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b52b-128">**Pinputpanel-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7b52b-128">**PenInputPanel Class**</span></span>](peninputpanel-class.md)
</dt> <dt>

<span data-ttu-id="7b52b-129">[Microsoft. Ink. pinputpanel](/previous-versions/ms583923(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="7b52b-129">[Microsoft.Ink.PenInputPanel](/previous-versions/ms583923(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="7b52b-130">Textdienstframework</span><span class="sxs-lookup"><span data-stu-id="7b52b-130">Text Services Framework</span></span>](../tsf/text-services-framework.md)
</dt> </dl>

 

 
