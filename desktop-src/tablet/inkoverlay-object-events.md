---
description: 'In der folgenden Tabelle wird beschrieben, in welchen Threads die InkOverlay-Objekt Ereignisse ausgelöst werden können. Eventthreadscursorbuttondowntriggers auf dem Ink threadcurrsorbuttonupfires auf dem Ink threadcurrsordowntriggers auf dem Ink threadcurrsorinrangetriggers auf dem Ink threadcurrsoroutfrangetriggers auf dem Ink threaddoubleclick (nur Automation). Wird in der Benutzeroberfläche der Anwendung (UI) threaddoubleclick (nur verwaltete Bibliothek) ausgelöst. Wird in der Benutzeroberfläche threadgesturetriggers der Anwendung auf dem Ink threadmousedowntriggers auf der UI threadmousemuveauslöst der Anwendung auf der UI threadmouseuptriggers der Anwendung auf der Benutzeroberfläche threadmousewheeltriggers der Anwendung ausgelöst. die UI threadnetwinairpacketauslöst auf dem Ink threadnewpackettriggers auf dem Ink threadbacintedauslöst auf der UI threadpaintingtriggers der Anwendung auf der Benutzeroberfläche threadselectionchangedtriggers der Anwendung auf dem frei Hand Thread. oder in dem Thread, der die Auswahl propertyselectionchangingtriggers des InkOverlay-Objekts auf der frei Hand threadselectionmuvedtriggers auf der frei Hand threadselectionreport Settings auf dem Ink threadselectionresizedauslöst auf dem Ink threadselectionresizingauslöst on The Ink threadstroketriggers on the Ink threadstrokesdeletedtriggers on the Ink threadstrokesdeletingtriggers on the Ink threadsystemgesturetriggers on the Ink threadtabletaddedfires on the Ink threadtabletremuvedtriggers on the Ink Thread. '
ms.assetid: 5d679e66-6ea1-491e-86a8-974c4ec61b96
title: InkOverlay-Objekt Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6122709f043fa94f4c1b3d04fcd1c51bb3cd8982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366118"
---
# <a name="inkoverlay-object-events"></a>InkOverlay-Objekt Ereignisse

In der folgenden Tabelle wird beschrieben, in welchen Threads die [**InkOverlay**](inkoverlay-class.md) -Objekt Ereignisse ausgelöst werden können.



| Ereignis                                                                             | Threads                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Currsorbuttondown**](inkoverlay-cursorbuttondown.md)                           | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**Currsorbuttonup**](inkoverlay-cursorbuttonup.md)                               | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**Cursor**](inkoverlay-cursordown.md)                                       | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**Cursor Bereich**](inkoverlay-cursorinrange.md)                                 | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**Cursor-Ausgabe**](inkoverlay-cursoroutofrange.md)                           | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**DoubleClick**](inkoverlay-doubleclick.md) (nur Automatisierung).                  | Wird auf dem Benutzeroberflächen Thread der Anwendung ausgelöst.<br/>                                                                                                          |
| [**DoubleClick**](/previous-versions/ms567634(v=vs.100)) (nur verwaltete Bibliothek). | Wird im UI-Thread der Anwendung ausgelöst.<br/>                                                                                                                           |
| [**Geste**](inkoverlay-gesture.md)                                             | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**MouseDown**](inkoverlay-mousedown.md)                                         | Wird im UI-Thread der Anwendung ausgelöst.<br/>                                                                                                                           |
| [**MouseMove**](inkoverlay-mousemove.md)                                         | Wird im UI-Thread der Anwendung ausgelöst.<br/>                                                                                                                           |
| [**MouseUp**](inkoverlay-mouseup.md)                                             | Wird im UI-Thread der Anwendung ausgelöst.<br/>                                                                                                                           |
| [**Mausrad**](inkoverlay-mousewheel.md)                                       | Wird im UI-Thread der Anwendung ausgelöst.<br/>                                                                                                                           |
| [**"Netwinairpakete"**](inkoverlay-newinairpackets.md)                             | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**Neupakete**](inkoverlay-newpackets.md)                                       | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**Be**](inkoverlay-painted.md)                                             | Wird im UI-Thread der Anwendung ausgelöst.<br/>                                                                                                                           |
| [**Be**](inkoverlay-painting.md)                                           | Wird im UI-Thread der Anwendung ausgelöst.<br/>                                                                                                                           |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)                           | Wird im frei Hand Thread oder im Thread ausgelöst, der die [**Auswahl**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) Eigenschaft des [**InkOverlay**](inkoverlay-class.md) -Objekts aktualisiert.<br/> |
| [**Ereignis**](inkoverlay-selectionchanging.md)                         | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**Selectionverschoben**](inkoverlay-selectionmoved.md)                               | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**SelectionMoving**](inkoverlay-selectionmoving.md)                             | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**SelectionResized**](inkoverlay-selectionresized.md)                           | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**Selectionresisierend**](inkoverlay-selectionresizing.md)                         | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**Stellung**](inkoverlay-stroke.md)                                               | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**StrokesDeleted**](inkoverlay-strokesdeleted.md)                               | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**Strokeslöschung**](inkoverlay-strokesdeleting.md)                             | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**System Bewegung**](inkoverlay-systemgesture.md)                                 | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**TabletAdded**](inkoverlay-tabletadded.md)                                     | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |
| [**Tabletreverschohe**](inkoverlay-tabletremoved.md)                                 | Wird im frei Hand Thread ausgelöst<br/>                                                                                                                                        |



 

 

