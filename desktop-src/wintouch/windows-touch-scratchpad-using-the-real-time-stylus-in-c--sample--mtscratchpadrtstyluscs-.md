---
title: Windows Touch Scratchpad mithilfe des Real-Time-Stiftbeispiels (C#)
description: Sehen Sie sich Windows Touch Scratchpad C#-Beispiel (MTScratchpadRTStylus) an, das zeigt, wie sie Windows Touch-Nachrichten verwenden, um Ablaufverfolgungen der Berührungspunkte in ein Fenster zu zeichnen.
ms.assetid: 8e80672f-0780-4dec-a9b4-afec0f7782ad
keywords:
- Windows Touch,Codebeispiele
- Windows Touch,Beispielcode
- Windows Touch,Scratchpad-Beispiele
- Scratchpad-Beispiele
- Windows Touch RTS-Objekt (Real-Time Stylus)
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 3c30d3543024a48394ddd7b9b2b06a05b61f5025
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406313"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a><span data-ttu-id="8cf59-108">Windows Touch Scratchpad mithilfe des Real-Time-Stiftbeispiels (C#)</span><span class="sxs-lookup"><span data-stu-id="8cf59-108">Windows Touch Scratchpad using the Real-Time Stylus Sample (C#)</span></span>

<span data-ttu-id="8cf59-109">Das Windows Touch Scratchpad-Beispiel ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) zeigt, wie Sie Windows Touch-Nachrichten verwenden, um Ablaufverfolgungen der Berührungspunkte in ein Fenster zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="8cf59-109">The Windows Touch Scratchpad sample ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="8cf59-110">Die Ablaufverfolgung des primären Fingers, der zuerst auf den Digitizer gezogen wurde, wird schwarz gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8cf59-110">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="8cf59-111">Sekundäre Finger werden in sechs weiteren Farben gezeichnet: Rot, Grün, Blau, Zyan, Magenta und Gelb.</span><span class="sxs-lookup"><span data-stu-id="8cf59-111">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta and yellow.</span></span> <span data-ttu-id="8cf59-112">Der folgende Screenshot zeigt, wie die Anwendung während der Ausführung aussehen könnte.</span><span class="sxs-lookup"><span data-stu-id="8cf59-112">The following screen shot shows how the application could look while running.</span></span>

![Screenshot des Beispiels "Windows Touch Scratchpad" mit dem Echtzeit-Tablettstift in C-Schärfe mit schwarzen und roten Drehungen auf dem Bildschirm](images/mtscratchpadrtstyluscs.png)

<span data-ttu-id="8cf59-114">Für dieses Beispiel wird Real-Time RtS-Objekt (Stylus) erstellt und die Unterstützung für mehrere Kontaktpunkte aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8cf59-114">For this sample, the Real-Time Stylus (RTS) object is created and support for multiple contact points is enabled.</span></span> <span data-ttu-id="8cf59-115">Ein DynamicRenderer-Plug-In wird rts hinzugefügt, um Inhalt zu rendern.</span><span class="sxs-lookup"><span data-stu-id="8cf59-115">A DynamicRenderer plug-in is added to the RTS to render content.</span></span> <span data-ttu-id="8cf59-116">Ein Plug-In, EventHandlerPlugIn, wird implementiert, um die Anzahl von Fingern zu verfolgen und die Farbe zu ändern, die der dynamische Renderer zeichnen soll.</span><span class="sxs-lookup"><span data-stu-id="8cf59-116">A plug-in, EventHandlerPlugIn, is implemented to track down the number of fingers and to change the color that the dynamic renderer is drawing.</span></span> <span data-ttu-id="8cf59-117">Bei beiden Plug-Ins im RTS-Plug-In-Stapel rendert die Windows Touch Scratchpad-Anwendung den primären Kontakt schwarz und die restlichen Kontakte in den verschiedenen Farben.</span><span class="sxs-lookup"><span data-stu-id="8cf59-117">With both plug-ins in the RTS plug-in stack, the Windows Touch Scratchpad application will render the primary contact in black and the rest of the contacts in the various colors.</span></span>

<span data-ttu-id="8cf59-118">Der folgende Code zeigt, wie EventHandlerPlugIn die Anzahl der Kontakte erhöht und dekrementiert und die Farbe des dynamischen Renderers fest legt.</span><span class="sxs-lookup"><span data-stu-id="8cf59-118">The following code shows how the EventHandlerPlugIn increments and decrements a count of the number of contacts and sets the color of the dynamic renderer.</span></span>

```CSharp
        public void StylusDown(RealTimeStylus sender, StylusDownData data)
        {
            // Set new stroke color to the DrawingAttributes of the DynamicRenderer
            // If there are no fingers down, this is a primary contact
            dynamicRenderer.DrawingAttributes.Color = touchColor.GetColor(cntContacts == 0);

            ++cntContacts;  // Increment finger-down counter
        }

        public void StylusUp(RealTimeStylus sender, StylusUpData data)
        {
            --cntContacts;  // Decrement finger-down counter
        }
```

<span data-ttu-id="8cf59-119">Der folgende Code zeigt, wie rts mit Unterstützung für mehrere Kontaktpunkt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="8cf59-119">The following code shows how the RTS is created with multiple contact point support.</span></span>

```CSharp
        private void OnLoadHandler(Object sender, EventArgs e)
        {
            // Create RealTimeStylus object and enable it for multi-touch
            realTimeStylus = new RealTimeStylus(this);
            realTimeStylus.MultiTouchEnabled = true;

            // Create DynamicRenderer and event handler, and add them to the RTS object as synchronous plugins
            dynamicRenderer = new DynamicRenderer(this);
            eventHandler = new EventHandlerPlugIn(this.CreateGraphics(), dynamicRenderer);
            realTimeStylus.SyncPluginCollection.Add(eventHandler);
            realTimeStylus.SyncPluginCollection.Add(dynamicRenderer);

            // Enable RTS and DynamicRenderer object, and enable auto-redraw of the DynamicRenderer
            realTimeStylus.Enabled = true;
            dynamicRenderer.Enabled = true;
            dynamicRenderer.EnableDataCache = true;
        }
```

<span data-ttu-id="8cf59-120">Nachdem sich die Farbe des DynamicRenderer-Objekts geändert und Striche gezeichnet wurden, werden die neuen Striche durch einen Aufruf von DynamicRenderer::Refresh angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8cf59-120">After the DynamicRenderer object's color has changed and strokes have been drawn, a call to DynamicRenderer::Refresh will cause the new strokes to appear.</span></span> <span data-ttu-id="8cf59-121">Der folgende Code zeigt, wie dies in der OnPaintHandler-Methode ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8cf59-121">The following code shows how this is performed in the OnPaintHandler method.</span></span>

```CSharp
        private void OnPaintHandler(object sender, PaintEventArgs e)
        {
            // Erase the background
            Brush brush = new SolidBrush(SystemColors.Window);
            e.Graphics.FillRectangle(brush, ClientRectangle);

            // Ask DynamicRenderer to redraw itself
            dynamicRenderer.Refresh();
        }
```

## <a name="related-topics"></a><span data-ttu-id="8cf59-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8cf59-122">Related topics</span></span>

<span data-ttu-id="8cf59-123">[Scratchpad-Multi-Touch-Anwendung (RTS/C#),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS) [Multi-Touch Scratchpad-Anwendung (RTS/C++),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp) [Windows Touch Beispiele](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="8cf59-123">[Multi-touch Scratchpad Application (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [Multi-touch Scratchpad Application (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
