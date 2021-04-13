---
title: Windows touchscratchpad mit dem Real-Time tablettstiftbeispiel (c#)
description: Das Windows touchscratchpad-Beispiel (mtscratchpadrtstylus) zeigt, wie Sie Windows-touchnachrichten verwenden, um Ablauf Verfolgungen der touchpunkte zu einem Fenster zu zeichnen.
ms.assetid: 8e80672f-0780-4dec-a9b4-afec0f7782ad
keywords:
- Windows-Fingereingabe, Codebeispiele
- Windows-Fingereingabe, Beispielcode
- Windows Toucheingabe, Scratchpad-Beispiele
- Scratchpad-Beispiele
- Windows-Fingereingabe, RTS-Objekt (Echt Zeit Stift)
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 4cf9ab2e451dcdcaaee808083ca42c420778f231
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314255"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a><span data-ttu-id="2585b-108">Windows touchscratchpad mit dem Real-Time tablettstiftbeispiel (c#)</span><span class="sxs-lookup"><span data-stu-id="2585b-108">Windows Touch Scratchpad using the Real-Time Stylus Sample (C#)</span></span>

<span data-ttu-id="2585b-109">Das Windows touchscratchpad-Beispiel ([mtscratchpadrtstylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) zeigt, wie Sie Windows-touchnachrichten verwenden, um Ablauf Verfolgungen der touchpunkte zu einem Fenster zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="2585b-109">The Windows Touch Scratchpad sample ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="2585b-110">Die Ablauf Verfolgung des primären Fingers, die zuerst auf dem Digitalisierer abgelegt wurde, wird schwarz gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2585b-110">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="2585b-111">Sekundäre Finger werden in sechs anderen Farben gezeichnet: rot, grün, blau, Cyan, Magenta und gelb.</span><span class="sxs-lookup"><span data-stu-id="2585b-111">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta and yellow.</span></span> <span data-ttu-id="2585b-112">Der folgende Screenshot zeigt, wie die Anwendung während der Ausführung aussehen könnte.</span><span class="sxs-lookup"><span data-stu-id="2585b-112">The following screen shot shows how the application could look while running.</span></span>

![Screenshot mit dem Windows touchscratchpad-Beispiel unter Verwendung des Echt Zeit Tablettstifts in c sharp mit schwarzen und roten Wellenlinien auf dem Bildschirm](images/mtscratchpadrtstyluscs.png)

<span data-ttu-id="2585b-114">In diesem Beispiel wird das Real-Time tablettstiftobjekt (RTS) erstellt, und die Unterstützung für mehrere Kontaktpunkte ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2585b-114">For this sample, the Real-Time Stylus (RTS) object is created and support for multiple contact points is enabled.</span></span> <span data-ttu-id="2585b-115">Dem RTS wird ein DynamicRenderer-Plug-in hinzugefügt, um Inhalt zu Renderern.</span><span class="sxs-lookup"><span data-stu-id="2585b-115">A DynamicRenderer plug-in is added to the RTS to render content.</span></span> <span data-ttu-id="2585b-116">Ein Plug-in, eventhandlerplugin, wird implementiert, um die Anzahl der Finger zu verfolgen und die Farbe zu ändern, die der dynamische Renderer zeichnet.</span><span class="sxs-lookup"><span data-stu-id="2585b-116">A plug-in, EventHandlerPlugIn, is implemented to track down the number of fingers and to change the color that the dynamic renderer is drawing.</span></span> <span data-ttu-id="2585b-117">Mit beiden Plug-ins im RTS-Plug-in-Stapel wird der primäre Kontakt von der Windows touchscratchpad-Anwendung in schwarz und den restlichen Kontakten in den verschiedenen Farben dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2585b-117">With both plug-ins in the RTS plug-in stack, the Windows Touch Scratchpad application will render the primary contact in black and the rest of the contacts in the various colors.</span></span>

<span data-ttu-id="2585b-118">Der folgende Code zeigt, wie das eventhandlerplugin-Ereignis eine Anzahl von Kontakten erhöht und dekrediert und die Farbe des dynamischen Renderers festlegt.</span><span class="sxs-lookup"><span data-stu-id="2585b-118">The following code shows how the EventHandlerPlugIn increments and decrements a count of the number of contacts and sets the color of the dynamic renderer.</span></span>

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

<span data-ttu-id="2585b-119">Der folgende Code zeigt, wie das RTS mit Unterstützung mehrerer Kontaktpunkte erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2585b-119">The following code shows how the RTS is created with multiple contact point support.</span></span>

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

<span data-ttu-id="2585b-120">Nachdem sich die Farbe des DynamicRenderer-Objekts geändert hat und Striche gezeichnet wurden, bewirkt ein Aufrufe von DynamicRenderer:: Refresh, dass die neuen Striche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="2585b-120">After the DynamicRenderer object's color has changed and strokes have been drawn, a call to DynamicRenderer::Refresh will cause the new strokes to appear.</span></span> <span data-ttu-id="2585b-121">Der folgende Code zeigt, wie dies in der onpainthandler-Methode erfolgt.</span><span class="sxs-lookup"><span data-stu-id="2585b-121">The following code shows how this is performed in the OnPaintHandler method.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="2585b-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2585b-122">Related topics</span></span>

<span data-ttu-id="2585b-123">[Multitouch Scratchpad-Anwendung (RTS/c#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [Multitouch Scratchpad-Anwendung (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows Touch-Beispiele](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="2585b-123">[Multi-touch Scratchpad Application (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [Multi-touch Scratchpad Application (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
