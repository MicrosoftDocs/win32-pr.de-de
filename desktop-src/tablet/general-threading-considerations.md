---
description: Übersicht über die allgemeinen Überlegungen zum Threading.
ms.assetid: cf35724f-5f80-4b3e-992a-a9d5ea99aae9
title: Allgemeine Überlegungen zum Threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f825ec7a1397dae7d60aa14b31603ee76a2f59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526585"
---
# <a name="general-threading-considerations"></a>Allgemeine Überlegungen zum Threading

Im folgenden finden Sie allgemeine Threading Aspekte bei der Entwicklung von Tablet PCs.

-   [Anwendungs-und nicht-Anwendungsthreads](#application-and-non-application-threads)
-   [Leistungsaspekte](#performance-considerations)
    -   [Ereignishandler](#event-handlers)
    -   [AutoRedraw (Eigenschaft)](#autoredraw-property)
    -   [DynamicRendering (Eigenschaft)](#dynamicrendering-property)
-   [Überlegungen zum ereignisthreading](#event-threading-considerations)
    -   [InkCollector-und InkOverlay-Objekt Ereignisse](#inkcollector-and-inkoverlay-objects-events)
    -   [Auflistungs Objekt-und Strokes-Sammlungs Ereignisse](#ink-object-and-strokes-collection-events)
    -   [Erkennungs Ereignisse](#recognition-events)
    -   [Ereignisse im Stift Eingabe Panel](#pen-input-panel-events)
-   [Zugehörige Themen](#related-topics)

## <a name="application-and-non-application-threads"></a>Anwendungs-und nicht-Anwendungsthreads

Alle frei Hand Ereignisse werden in einem separaten frei Hand Thread mit hoher Priorität generiert. Dadurch können frei Hand Eingaben reibungslos fließen, auch wenn eine Anwendung langsam ausgeführt wird. Ereignishandler können das Rendern von frei Hand Eingaben jedoch verlangsamen oder blockieren.

Alle Erkennungs Ereignisse, die durch Aufrufe der Hintergrund Erkennungsmethode generiert werden, werden in einem separaten Hintergrund Erkennungs Thread mit normaler Priorität behandelt.

Alle Mausereignisse werden auf dem Hauptbenutzer Oberflächen Thread der Anwendung generiert.

## <a name="performance-considerations"></a>Überlegungen zur Leistung

### <a name="event-handlers"></a>Ereignishandler

Die Tablet PC Platform-API (Application Programming Interface) verfügt über ein interaktives Modell für Ereignisse anstelle eines Benachrichtigungs Modells. Halten Sie Code in Ereignis Handlern kurz, um die Zeit zu verkürzen, in der das frei Hand Rendering blockiert wird. Die Sammlung von frei Hand Eingaben durch den Tablet PC wird nicht blockiert, Ihre Anwendung erhält jedoch keine frei Hand Eingaben, während Ihre Anwendung blockiert wird.

### <a name="autoredraw-property"></a>AutoRedraw (Eigenschaft)

Wenn Ihre Anwendung ein benutzerdefiniertes Rendering durchführt oder wenn Ihre Anwendung für Zeichnungs Probleme sensibel ist, können Sie das Neuzeichnen selbst verarbeiten und die [**AutoRedraw**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_autoredraw) -Eigenschaft für das [**InkCollector**](inkcollector-class.md) -Objekt, das [**InkOverlay**](inkoverlay-class.md) -Objekt oder das [InkPicture](inkpicture-control.md) -Steuerelement auf **false** festlegen. Verwenden Sie die Ereignisse in der folgenden Tabelle, um das Neuzeichnen zu verarbeiten.



| Objekt oder Steuerelement                                            | Ereignis                                                                                                                                                                                                                     |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InkCollector**](inkcollector-class.md) Objekt<br/> | Das Steuerelement des zugrunde liegenden Steuer Elements [. ungültige](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) und [Control. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) -Ereignisse.<br/>                                 |
| [**InkOverlay**](inkoverlay-class.md) Objekt<br/>     | Das Steuerelement des zugrunde liegenden Steuer Elements [. ungültige](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) und [Control. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) -Ereignisse.<br/>                                 |
| [InkPicture](inkpicture-control.md) Steuerelement<br/>      | Geerbtes Steuerelement des [InkPicture](inkpicture-control.md) -Steuer Elements [. ungültig](/dotnet/api/system.windows.forms.control.invalidated?view=netcore-3.1) erklärt und [Control. Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) -Ereignisse.<br/> |



 

### <a name="dynamicrendering-property"></a>DynamicRendering (Eigenschaft)

Wenn Ihre Anwendung ein benutzerdefiniertes Rendering durchführt oder wenn Sie die Informationen, aber nicht die frei Hand Eingabe benötigen, können Sie das Einlagern von frei Hand Eingaben selbst durchsetzen und die Echtzeitdarstellung von frei Hand Eingaben ausschalten, indem Sie die [**DynamicRendering**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_dynamicrendering) -Eigenschaft für das [**InkCollector**](inkcollector-class.md) -Objekt, das [**InkOverlay**](inkoverlay-class.md) -Objekt oder das [InkPicture](inkpicture-control.md) -Steuerelement auf **false** festlegen

## <a name="event-threading-considerations"></a>Überlegungen zum ereignisthreading

Die API-Ereignisse der Tablet PC-Plattform werden in verschiedenen Threads ausgelöst.

### <a name="inkcollector-and-inkoverlay-objects-events"></a>InkCollector-und InkOverlay-Objekt Ereignisse

Die meisten [**InkCollector**](inkcollector-class.md) -und [**InkOverlay**](inkoverlay-class.md) -Objekt Ereignisse werden im frei Hand Thread ausgelöst. Nur die Mausereignisse für diese Objekte werden im UI-Thread ausgelöst. Beispielsweise wird für das **InkCollector** -Objekt das [**MouseDown**](inkcollector-mousedown.md) -Ereignis im UI-Thread ausgelöst, und das [**Cursor**](inkcollector-cursordown.md) -Ereignis wird im frei Hand Thread ausgelöst.

### <a name="ink-object-and-strokes-collection-events"></a>Auflistungs Objekt-und Strokes-Sammlungs Ereignisse

Das frei [**Hand Objekt und die**](inkdisp-class.md) [**Striche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistungs Ereignisse können aus dem frei Hand Thread oder dem UI-Thread stammen. Wenn die Anwendung das frei Hand **Objekt oder die Auflistung** der **Striche** bearbeitet, wird das Ereignis im UI-Thread generiert. Wenn das [**InkCollector**](inkcollector-class.md) -Objekt oder das [**InkOverlay**](inkoverlay-class.md) -Objekt das **Ink** -Objekt oder die **Striche** -Auflistung aktualisiert, wird das Ereignis im frei Hand Thread generiert.

Die Steuerelemente [InkPicture](inkpicture-control-reference.md) und [InkEdit](inkedit-control-reference.md) arbeiten in einem Single Thread-Apartment (STA). Wenn das InkPicture-oder InkEdit-Steuerelement das [**Ink**](inkdisp-class.md) -Objekt oder die [**Striche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung aktualisiert, wird das-Ereignis im UI-Thread ausgelöst.

### <a name="recognition-events"></a>Erkennungs Ereignisse

Erkennungs Ereignisse werden im UI-Thread oder im Hintergrund Erkennungs Thread ausgelöst.

-   Die [**Erkennungs**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) Methode des [InkEdit](inkedit-control-reference.md) -Steuer Elements löst das Erkennungs Ereignis (nur verwaltete Bibliothek) oder das [Erkennungs](/previous-versions/ms836436(v=msdn.10)) [**Ergebnis**](inkedit-recognitionresult.md) (nur Automation) im UI-Thread aus.
-   Die Methoden [**Background**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) Recognition und [**backgrounderkennzewithalternativen**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) des Erkennungs [**Kontext**](inkrecognizercontext-class.md) Objekts rufen die Ereignisse [**Recognition**](inkrecognizercontext-recognition.md) und [**erkentionwithalternativen**](inkrecognizercontext-recognitionwithalternates.md) im Hintergrund Erkennungs Thread auf.

### <a name="pen-input-panel-events"></a>Ereignisse im Stift Eingabe Panel

In dem Thread, in dem das Objekt " **pinputpanel** " erstellt wird, werden " [**pinputpanel**](peninputpanel-class.md) "-Ereignisse ausgelöst.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft. Ink. InkCollector. DynamicRendering](/previous-versions/ms836502(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkOverlay. DynamicRendering](/previous-versions/ms833104(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkPicture. DynamicRendering](/previous-versions/ms582188(v=vs.100))
</dt> <dt>

[Microsoft. Ink. InkCollector. AutoRedraw](/previous-versions/ms836495(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkOverlay. AutoRedraw](/previous-versions/ms833082(v=msdn.10))
</dt> <dt>

[Microsoft. Ink. InkPicture. AutoRedraw](/previous-versions/ms582180(v=vs.100))
</dt> </dl>

 

