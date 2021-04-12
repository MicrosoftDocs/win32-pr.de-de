---
title: Druck- und Befehlslisten
description: Das Druck Steuerelement Direct2D \ 32; ist eine neue Komponente im Direct2D-Modul in Windows 8.
ms.assetid: C51ACCDE-B205-4F79-A2FD-D112BAAD1616
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6beb16a24c972016686e2dffe915a947128a63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390440"
---
# <a name="printing-and-command-lists"></a><span data-ttu-id="ca6e8-103">Druck- und Befehlslisten</span><span class="sxs-lookup"><span data-stu-id="ca6e8-103">Printing and command lists</span></span>

<span data-ttu-id="ca6e8-104">Das [Direct2D](./direct2d-portal.md) - [**Druck Steuer**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) Element ist eine neue Komponente im Direct2D-Modul in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ca6e8-104">The [Direct2D](./direct2d-portal.md) [**print control**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) is a new component in the Direct2D module in Windows 8.</span></span> <span data-ttu-id="ca6e8-105">Mit dieser Komponente können Direct2D-Apps ihre Direct2D-Zeichnungs Aufrufe (hinsichtlich Zustandsänderungen und renderprimitiver) wieder verwenden, um Druckergebnisse zu übermitteln, die mit der Anzeige auf dem Bildschirm vergleichbar sind.</span><span class="sxs-lookup"><span data-stu-id="ca6e8-105">This component lets Direct2D apps reuse their Direct2D drawing calls (in terms of state changes and rending primitives) to deliver printing results that are similar to what you see on the screen.</span></span>

<span data-ttu-id="ca6e8-106">Die [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) -Schnittstelle stellt einen virtuellen Druckauftrag dar: Sie können ein [Direct2D](./direct2d-portal.md) -Druck Steuerelement erstellen, um einen neuen Druckauftrag zu initiieren, Direct2D-Inhalte für jede Seite zu übergeben, die Sie drucken möchten, und dann das Druck Steuerelement schließen, um einen Druckauftrag abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ca6e8-106">The [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) interface represents a virtual print job: you can create a [Direct2D](./direct2d-portal.md) print control to initiate a new print job, pass in Direct2D contents for each page you want to print, then close the print control to complete a print job.</span></span>

> [!Note]  
> <span data-ttu-id="ca6e8-107">Ein Druck Steuerelement wird einem und genau einem Druckauftrag zugeordnet und kann nicht wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca6e8-107">A print control maps to one and exactly one print job, and you can't reuse it.</span></span>

<span data-ttu-id="ca6e8-108">Mit dem Druck Steuerelement [Direct2D](./direct2d-portal.md) wird der übergebene Direct2D-Inhalt für das Druck Subsystem konvertiert und optimiert, das mit den echten Druckern funktioniert, um das tatsächliche PrintOut-Element bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ca6e8-108">The [Direct2D](./direct2d-portal.md) print control converts and optimizes the passed in Direct2D contents for the print sub-system, which works with the real printers to deliver the actual printout.</span></span> <span data-ttu-id="ca6e8-109">Alle druckspezifischen Details werden in Direct2D-apps ausgeblendet, was bedeutet, dass Direct2D-apps drucken können, ohne zu wissen, auf welche Geräte Sie sich beziehen, oder wie die Zeichnungen in den Druckvorgang übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="ca6e8-109">All print-specific details are hidden from Direct2D apps, which means Direct2D apps can print without knowing what devices they are drawing to, or how the drawings are translated to printing.</span></span>

<span data-ttu-id="ca6e8-110">Zum Drucken mit [Direct2D](./direct2d-portal.md)müssen Sie eine Direct2D-Befehlsliste für jede Seite vorbereiten, die Sie drucken möchten. übergeben Sie dann die Befehlsliste an das Direct2D-Druck Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="ca6e8-110">To print with [Direct2D](./direct2d-portal.md), you need to prepare one Direct2D command list for each page you want to print, then pass that command list to the Direct2D print control.</span></span> <span data-ttu-id="ca6e8-111">Um diese Direct2D-Befehlsliste vorzubereiten, erstellen Sie einfach eine Befehlsliste als Zeichnungs Ziel des aktuellen Geräte Kontexts und legen Sie dann auf diesen Gerätekontext fest, genau so, als ob Sie auf ein bitmapziel für die Anzeige zeichnen.</span><span class="sxs-lookup"><span data-stu-id="ca6e8-111">To prepare that Direct2D command list, you simply create and set a command list as the drawing target of the current device context, and then draw to that device context, exactly as if you are drawing to a bitmap target for display.</span></span> <span data-ttu-id="ca6e8-112">Weitere Informationen zu Geräten und Zielen finden Sie unter [Geräte und Geräte Kontexte](devices-and-device-contexts.md) .</span><span class="sxs-lookup"><span data-stu-id="ca6e8-112">See [Devices and Device Contexts](devices-and-device-contexts.md) for more info on devices and targets.</span></span>

<span data-ttu-id="ca6e8-113">Das Diagramm zeigt die Interaktion zwischen der APP, dem Gerätekontext, dem bitmapziel, dem Ziel der Befehlsliste und dem Druck Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="ca6e8-113">The diagram here illustrates the interaction between the app, device context, bitmap target, command list target, and the print control.</span></span>

> [!Note]  
> <span data-ttu-id="ca6e8-114">Die Druck Sub-System und Drucker Komponenten von Windows sind grau, da Sie in [Direct2D](./direct2d-portal.md) -apps vollständig ausgeblendet sind.</span><span class="sxs-lookup"><span data-stu-id="ca6e8-114">The Windows Print Sub-System and Printer components are in gray because they are completely hidden from [Direct2D](./direct2d-portal.md) apps.</span></span>

![ein Diagramm, das zeigt, wie die CommandList und der Druckvorgang mit einer APP und Direct2D interagieren.](images/d2dprintcontroldiagram.png)

## <a name="example"></a><span data-ttu-id="ca6e8-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ca6e8-116">Example</span></span>

<span data-ttu-id="ca6e8-117">Der gesamte Druck Direct2D Inhalt umfasst die folgenden Schritte.</span><span class="sxs-lookup"><span data-stu-id="ca6e8-117">The complete process of printing Direct2D content includes the following steps.</span></span>

1.  <span data-ttu-id="ca6e8-118">Erstellen Sie ein Druck Steuerelement zum Initiieren eines Druckauftrags.</span><span class="sxs-lookup"><span data-stu-id="ca6e8-118">Create a print control to initiate a print job.</span></span>
2.  <span data-ttu-id="ca6e8-119">Fügen Sie dem Druck Steuerelement eine Seite hinzu, indem Sie eine Befehlsliste übergeben.</span><span class="sxs-lookup"><span data-stu-id="ca6e8-119">Add a page to the print control by passing in a command list.</span></span>
3.  <span data-ttu-id="ca6e8-120">Wiederholen Sie Schritt 2 für jede Seite im restlichen Dokument.</span><span class="sxs-lookup"><span data-stu-id="ca6e8-120">Repeat step 2 for each page in the rest of the document</span></span>
4.  <span data-ttu-id="ca6e8-121">Schließen Sie das Druck Steuerelement, um den Druckauftrag abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ca6e8-121">Close the print control to complete the print job.</span></span>

<span data-ttu-id="ca6e8-122">Hier sehen Sie ein Codebeispiel, in dem der Prozess veranschaulicht wird.</span><span class="sxs-lookup"><span data-stu-id="ca6e8-122">Here is a code example showing the process.</span></span>

```cpp
ID2D1CommandList* commandList;
// Skip command list creation and drawing for simplicity.

// Set print control properties.
D2D1_PRINT_CONTROL_PROPERTIES printControlProperties;
printControlProperties.rasterDPI = 150.0f; // Use the default rasterization DPI for all unsupported Direct2D commands 
                                                                                                                                                                            //  or options.
printControlProperties.fontSubset = D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT; // Using the default font subset strategy.
printControlProperties.colorSpace = D2D1_COLOR_SPACE_SRGB; // Color space for vector graphics in Direct2D print control.

// Create a Direct2D Print Control to initiate a print job.
ID2D1PrintControl* d2dPrintControl;
d2dDevice->CreatePrintControl(
    wicFactory,
    documentTarget,
    printControlProperties,
    &d2dPrintControl
    );

// Add Direct2D drawing commands encapsulated in a command list.
// You can add in more pages by calling this API multiple times.
d2dPrintControl->AddPage(commandList);

// Close the print control to complete a print job.
d2dPrintControl->Close();
```

## <a name="related-topics"></a><span data-ttu-id="ca6e8-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ca6e8-123">Related topics</span></span>

[<span data-ttu-id="ca6e8-124">**ID2D1CommandList**</span><span class="sxs-lookup"><span data-stu-id="ca6e8-124">**ID2D1CommandList**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)

[<span data-ttu-id="ca6e8-125">**ID2D1PrintControl**</span><span class="sxs-lookup"><span data-stu-id="ca6e8-125">**ID2D1PrintControl**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)

[<span data-ttu-id="ca6e8-126">Verbessern der Leistung von Direct2D-Anwendungen und Drucken</span><span class="sxs-lookup"><span data-stu-id="ca6e8-126">Improving the Performance of Direct2D Applications and Printing</span></span>](improving-direct2d-performance.md)