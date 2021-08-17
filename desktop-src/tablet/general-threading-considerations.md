---
description: Übersicht über allgemeine Überlegungen zum Threading.
ms.assetid: cf35724f-5f80-4b3e-992a-a9d5ea99aae9
title: Allgemeine Überlegungen zum Threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f4c6f2aa76775d3d88e8ea60c3899a2d8ac47e5ef07fddbbdfaca96196dee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092574"
---
# <a name="general-threading-considerations"></a>Allgemeine Überlegungen zum Threading

Im Folgenden finden Sie allgemeine Überlegungen zum Threading bei der Entwicklung für Tablet PC.

-   [Anwendungsthreads und Nichtanwendungsthreads](#application-and-non-application-threads)
-   [Leistungsaspekte](#performance-considerations)
    -   [Ereignishandler](#event-handlers)
    -   [AutoRedraw-Eigenschaft](#autoredraw-property)
    -   [DynamicRendering-Eigenschaft](#dynamicrendering-property)
-   [Überlegungen zum Ereignisthreading](#event-threading-considerations)
    -   [InkCollector- und InkOverlay Objects-Ereignisse](#inkcollector-and-inkoverlay-objects-events)
    -   [Ink Object and Strokes Collection Events](#ink-object-and-strokes-collection-events)
    -   [Erkennungsereignisse](#recognition-events)
    -   [Stifteingabebereichsereignisse](#pen-input-panel-events)
-   [Zugehörige Themen](#related-topics)

## <a name="application-and-non-application-threads"></a>Anwendungsthreads und Nichtanwendungsthreads

Alle Ink-Ereignisse werden in einem separaten Ink-Thread mit hoher Priorität generiert. Dies ermöglicht einen reibungslosen Fluss der Ink-Funktion, auch wenn eine Anwendung langsam ausgeführt wird. Ereignishandler können jedoch das Rendern von Ink verlangsamen oder blockieren.

Alle Erkennungsereignisse, die von Methodenaufrufen der Hintergrunderkennung generiert werden, werden in einem separaten Hintergrunderkennungsthread mit normaler Priorität behandelt.

Alle Mausereignisse werden im Hauptthread der Benutzeroberfläche der Anwendung generiert.

## <a name="performance-considerations"></a>Überlegungen zur Leistung

### <a name="event-handlers"></a>Ereignishandler

Die Anwendungsprogrammierschnittstelle (Application Programming Interface, API) der Tablet PC-Plattform verfügt über ein interaktives Modell für Ereignisse und nicht über ein Benachrichtigungsmodell. Halten Sie Code in Ereignishandlern kurz, um die Zeit zu reduzieren, die das Rendern von Ink-Daten blockiert. Die Sammlung von Ink durch den Tablet-PC wird nicht blockiert, aber Ihre Anwendung erhält die Ink nicht, während Ihre Anwendung blockiert ist.

### <a name="autoredraw-property"></a>AutoRedraw-Eigenschaft

Wenn Ihre Anwendung benutzerdefiniertes Rendering vorsteuert oder wenn Ihre Anwendung auf Probleme beim Malen reagieren kann, können Sie die Neuzeichnung selbst durchführen und die [**AutoRedraw-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw) für das [**InkCollector-Objekt,**](inkcollector-class.md) das [**InkOverlay-Objekt**](inkoverlay-class.md) oder das [InkPicture-Steuerelement](inkpicture-control.md) auf **FALSE** festlegen. Verwenden Sie die Ereignisse in der folgenden Tabelle, um die Neupaintierung zu behandeln.



| Objekt oder Steuerelement                                            | Ereignis                                                                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InkCollector**](inkcollector-class.md) Objekt<br/> | Die Ereignisse [Control.Invalidated](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) und [Control.Paint des zugrunde liegenden Steuerelements.](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1)<br/>                                 |
| [**InkOverlay**](inkoverlay-class.md) Objekt<br/>     | Die Ereignisse [Control.Invalidated](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) und [Control.Paint des zugrunde liegenden Steuerelements.](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1)<br/>                                 |
| [InkPicture](inkpicture-control.md) Steuerung<br/>      | [Die geerbten](inkpicture-control.md) [Control.Invalidated-](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) und [Control.Paint-Ereignisse](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) des InkPicture-Steuerelements.<br/> |



 

### <a name="dynamicrendering-property"></a>DynamicRendering-Eigenschaft

Wenn Ihre Anwendung benutzerdefiniertes Rendering vorsteuert oder wenn Sie die Informationen, aber nicht die Ink-Eigenschaft, verwenden möchten, können Sie die  InkOverlay-Darstellung selbst verarbeiten und das Echtzeitrendering von InkPicture deaktivieren, indem Sie die [**DynamicRendering-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_dynamicrendering) für das [**InkCollector-Objekt,**](inkcollector-class.md) das [**InkOverlay-Objekt**](inkoverlay-class.md) oder das [InkPicture-Steuerelement](inkpicture-control.md) auf FALSE festlegen.

## <a name="event-threading-considerations"></a>Überlegungen zum Ereignisthreading

Api-Ereignisse der Tablet PC-Plattform werden in verschiedenen Threads ausgelöst.

### <a name="inkcollector-and-inkoverlay-objects-events"></a>InkCollector- und InkOverlay Objects-Ereignisse

Die [**meisten InkCollector-**](inkcollector-class.md) und [**InkOverlay-Objektereignisse**](inkoverlay-class.md) werden im Ink-Thread ausgelöst. Nur die Mausereignisse für diese Objekte werden im UI-Thread ausgelöst. Für das **InkCollector-Objekt** wird beispielsweise das [**MouseDown-Ereignis**](inkcollector-mousedown.md) im UI-Thread ausgelöst, und das [**CursorDown-Ereignis**](inkcollector-cursordown.md) wird im Ink-Thread ausgelöst.

### <a name="ink-object-and-strokes-collection-events"></a>Ink Object and Strokes Collection Events

Die [**Ink-Objekt-**](inkdisp-class.md) [**und Strokes-Auflistungsereignisse**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) können aus dem Ink-Thread oder dem UI-Thread stammen. Wenn Ihre Anwendung das **Ink-Objekt** oder die **Strokes-Auflistung** bearbeitet, wird das Ereignis im UI-Thread generiert. Wenn der [**InkCollector**](inkcollector-class.md) oder das [**InkOverlay-Objekt**](inkoverlay-class.md) das **Ink-Objekt** oder die **Strokes-Auflistung** aktualisiert, wird das Ereignis im Ink-Thread generiert.

Die [Steuerelemente InkPicture](inkpicture-control-reference.md) und [InkEdit](inkedit-control-reference.md) arbeiten in einem Singlethread-Apartment (STA). Wenn das InkPicture- oder InkEdit-Steuerelement das [**Ink-Objekt**](inkdisp-class.md) oder die [**Strokes-Auflistung**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) aktualisiert, wird das -Ereignis im UI-Thread ausgelöst.

### <a name="recognition-events"></a>Erkennungsereignisse

Erkennungsereignisse werden im UI-Thread oder im Hintergrunderkennungsthread ausgelöst.

-   Die [**Recognize-Methode**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) des [InkEdit-Steuerelements](inkedit-control-reference.md) löst das [Ereignis Recognition](/previous-versions/ms836436(v=msdn.10)) (nur verwaltete Bibliothek) oder [**RecognitionResult**](inkedit-recognitionresult.md) (nur Automation) im UI-Thread aus.
-   Die Methoden [**BackgroundRecognize und BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) des [**RecognizerContext-Objekts**](inkrecognizercontext-class.md) heben die [**Ereignisse Recognition**](inkrecognizercontext-recognition.md) und [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) im Hintergrunderkennungsthread auf. [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)

### <a name="pen-input-panel-events"></a>Stifteingabebereichsereignisse

[**PenInputPanel-Ereignisse**](peninputpanel-class.md) werden in dem Thread ausgelöst, in dem das **PenInputPanel-Objekt** erstellt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft.Ink.InkCollector.DynamicRendering](/previous-versions/ms836502(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkOverlay.DynamicRendering](/previous-versions/ms833104(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkPicture.DynamicRendering](/previous-versions/ms582188(v=vs.100))
</dt> <dt>

[Microsoft.Ink.InkCollector.AutoRedraw](/previous-versions/ms836495(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkOverlay.AutoRedraw](/previous-versions/ms833082(v=msdn.10))
</dt> <dt>

[Microsoft.Ink.InkPicture.AutoRedraw](/previous-versions/ms582180(v=vs.100))
</dt> </dl>

 

