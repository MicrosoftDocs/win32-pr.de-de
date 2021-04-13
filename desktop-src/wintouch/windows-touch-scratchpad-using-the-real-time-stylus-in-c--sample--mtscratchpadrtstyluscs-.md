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
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a>Windows touchscratchpad mit dem Real-Time tablettstiftbeispiel (c#)

Das Windows touchscratchpad-Beispiel ([mtscratchpadrtstylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) zeigt, wie Sie Windows-touchnachrichten verwenden, um Ablauf Verfolgungen der touchpunkte zu einem Fenster zu zeichnen. Die Ablauf Verfolgung des primären Fingers, die zuerst auf dem Digitalisierer abgelegt wurde, wird schwarz gezeichnet. Sekundäre Finger werden in sechs anderen Farben gezeichnet: rot, grün, blau, Cyan, Magenta und gelb. Der folgende Screenshot zeigt, wie die Anwendung während der Ausführung aussehen könnte.

![Screenshot mit dem Windows touchscratchpad-Beispiel unter Verwendung des Echt Zeit Tablettstifts in c sharp mit schwarzen und roten Wellenlinien auf dem Bildschirm](images/mtscratchpadrtstyluscs.png)

In diesem Beispiel wird das Real-Time tablettstiftobjekt (RTS) erstellt, und die Unterstützung für mehrere Kontaktpunkte ist aktiviert. Dem RTS wird ein DynamicRenderer-Plug-in hinzugefügt, um Inhalt zu Renderern. Ein Plug-in, eventhandlerplugin, wird implementiert, um die Anzahl der Finger zu verfolgen und die Farbe zu ändern, die der dynamische Renderer zeichnet. Mit beiden Plug-ins im RTS-Plug-in-Stapel wird der primäre Kontakt von der Windows touchscratchpad-Anwendung in schwarz und den restlichen Kontakten in den verschiedenen Farben dargestellt.

Der folgende Code zeigt, wie das eventhandlerplugin-Ereignis eine Anzahl von Kontakten erhöht und dekrediert und die Farbe des dynamischen Renderers festlegt.

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

Der folgende Code zeigt, wie das RTS mit Unterstützung mehrerer Kontaktpunkte erstellt wird.

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

Nachdem sich die Farbe des DynamicRenderer-Objekts geändert hat und Striche gezeichnet wurden, bewirkt ein Aufrufe von DynamicRenderer:: Refresh, dass die neuen Striche angezeigt werden. Der folgende Code zeigt, wie dies in der onpainthandler-Methode erfolgt.

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

## <a name="related-topics"></a>Zugehörige Themen

[Multitouch Scratchpad-Anwendung (RTS/c#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [Multitouch Scratchpad-Anwendung (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows Touch-Beispiele](windows-touch-samples.md)
