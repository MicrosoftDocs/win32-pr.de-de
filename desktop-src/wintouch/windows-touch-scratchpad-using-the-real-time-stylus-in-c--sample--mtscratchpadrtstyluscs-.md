---
title: Windows Touch Scratchpad mithilfe des Real-Time Tablettstiftbeispiels (C#)
description: Sehen Sie sich Windows Touch Scratchpad C#-Beispiel (MTScratchpadRTStylus) an, das zeigt, wie Sie mithilfe von Windows Touch-Nachrichten Ablaufverfolgungen der Berührungspunkte in ein Fenster zeichnen.
ms.assetid: 8e80672f-0780-4dec-a9b4-afec0f7782ad
keywords:
- Windows Touch,Codebeispiele
- Windows Touch,Beispielcode
- Windows Touch,Scratchpad-Beispiele
- Scratchpad-Beispiele
- Windows Touch-,Echtzeit-Stiftobjekt (RTS)
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: a76f7a66f8bc26b7e1cad8f1fa71d9703f0c0da1ad1452a078b374a0f1603238
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055845"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a>Windows Touch Scratchpad mithilfe des Real-Time Tablettstiftbeispiels (C#)

Das Windows Touch Scratchpad-Beispiel ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) zeigt, wie Sie mithilfe von Windows Touch-Nachrichten Ablaufverfolgungen der Berührungspunkte in ein Fenster zeichnen. Die Ablaufverfolgung des primären Fingers, der zuerst auf den Digitizer gezogen wurde, wird schwarz gezeichnet. Sekundäre Finger werden in sechs weiteren Farben gezeichnet: Rot, Grün, Blau, Zyan, Magenta und Gelb. Der folgende Screenshot zeigt, wie die Anwendung während der Ausführung aussehen könnte.

![Screenshot des Beispiels "Windows Touch Scratchpad" mithilfe des Echtzeit-Tablettstifts in C-Schärfe mit schwarzen und roten Unterschniffen auf dem Bildschirm](images/mtscratchpadrtstyluscs.png)

Für dieses Beispiel wird Real-Time RtS-Objekt (Stylus) erstellt und die Unterstützung für mehrere Kontaktpunkte aktiviert. Dem RTS wird ein DynamicRenderer-Plug-In hinzugefügt, um Inhalt zu rendern. Ein Plug-In, EventHandlerPlugIn, wird implementiert, um die Anzahl von Fingern zu verfolgen und die Farbe zu ändern, die der dynamische Renderer zeichnen soll. Bei beiden Plug-Ins im RTS-Plug-In-Stapel rendert die Windows Touch Scratchpad-Anwendung den primären Kontakt in Schwarz und die restlichen Kontakte in den verschiedenen Farben.

Der folgende Code zeigt, wie EventHandlerPlugIn die Anzahl der Kontakte erhöht und dekrementiert und die Farbe des dynamischen Renderers fest legt.

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

Der folgende Code zeigt, wie rts mit Unterstützung für mehrere Kontaktpunkt erstellt wird.

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

Nachdem sich die Farbe des DynamicRenderer-Objekts geändert und Striche gezeichnet wurden, werden die neuen Striche durch einen Aufruf von DynamicRenderer::Refresh angezeigt. Der folgende Code zeigt, wie dies in der OnPaintHandler-Methode ausgeführt wird.

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

[Scratchpad-Multi-Touch-Anwendung (RTS/C#),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS) [Multi-Touch Scratchpad-Anwendung (RTS/C++),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp) [Windows Touchbeispiele](windows-touch-samples.md)
