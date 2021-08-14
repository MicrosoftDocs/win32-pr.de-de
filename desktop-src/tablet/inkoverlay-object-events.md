---
description: 'In der folgenden Tabelle wird beschrieben, in welchen Threads die InkOverlay-Objektereignisse ausgelöst werden können. EventThreadsCursorButtonDownFires für den Ink-ThreadCursorButtonUpFires im Ink-ThreadCursorDownFires im Ink-ThreadCursorInRangeFires für den InkthreadCursorOutOfRangeFires im InkthreadDoubleClick (nur Automatisierung). Wird auf dem ThreadDoubleClick der Benutzeroberfläche (UI) der Anwendung ausgelöst (nur verwaltete Bibliothek). Wird auf dem Ui-Thread der Anwendung AusgelöstGestureFires für den FreihandthreadMouseDownFires im UI-Thread Der BenutzeroberflächenthreadMouseMoveFires der Anwendung im UI-ThreadMouseUpFires der Anwendung im UI-ThreadMouseWheelFires der Anwendung für die Anwendung s UI threadNewInAirPacketsFires on the ink threadNewPacketsFires on the ink threadPaintedFires on the application es UI threadPaintingFires on the application es UI threadSelectionChangedFires on the ink thread, oder in dem Thread, der die des InkOverlay-Objekts aktualisiert  Selection propertySelectionChangingFires on the ink threadSelectionMovedFires on the ink threadSelectionMovingFires on the ink threadSelectionResizedFires on the ink threadSelectionResizingFires on the ink threadStrokeFires on the ink threadSelectionResizingFires on the ink threadSelectionResizingFires on the ink thread ink threadStrokesDeletedFires on the ink threadStrokesDeletingFires on the ink threadSystemGestureFires on the ink threadTabletAddedFires on the ink threadTabletRemovedFires on the ink thread '
ms.assetid: 5d679e66-6ea1-491e-86a8-974c4ec61b96
title: InkOverlay-Objektereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531ee197a14edf3ce0aa8595bdbcdb3ea2937d9cf863dcc6e95690088ed8ee96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118218963"
---
# <a name="inkoverlay-object-events"></a>InkOverlay-Objektereignisse

In der folgenden Tabelle wird beschrieben, in welchen Threads die [**InkOverlay-Objektereignisse**](inkoverlay-class.md) ausgelöst werden können.



| Ereignis                                                                             | Threads                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkoverlay-cursorbuttondown.md)                           | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**CursorButtonUp**](inkoverlay-cursorbuttonup.md)                               | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**Cursordown**](inkoverlay-cursordown.md)                                       | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**Cursorinrange**](inkoverlay-cursorinrange.md)                                 | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**Cursoroutofrange**](inkoverlay-cursoroutofrange.md)                           | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**DoubleClick**](inkoverlay-doubleclick.md) (nur Automation).                  | Wird im Benutzeroberflächenthread der Anwendung ausgelöst.<br/>                                                                                                          |
| [**DoubleClick**](/previous-versions/ms567634(v=vs.100)) (nur verwaltete Bibliothek). | Wird im UI-Thread der Anwendung ausgelöst<br/>                                                                                                                           |
| [**Geste**](inkoverlay-gesture.md)                                             | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**Mousedown**](inkoverlay-mousedown.md)                                         | Wird im UI-Thread der Anwendung ausgelöst<br/>                                                                                                                           |
| [**Mousemove**](inkoverlay-mousemove.md)                                         | Wird im UI-Thread der Anwendung ausgelöst<br/>                                                                                                                           |
| [**Mouseup**](inkoverlay-mouseup.md)                                             | Wird im UI-Thread der Anwendung ausgelöst<br/>                                                                                                                           |
| [**Mousewheel**](inkoverlay-mousewheel.md)                                       | Wird im UI-Thread der Anwendung ausgelöst<br/>                                                                                                                           |
| [**Newinairpackets**](inkoverlay-newinairpackets.md)                             | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**Newpackets**](inkoverlay-newpackets.md)                                       | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**Gemalt**](inkoverlay-painted.md)                                             | Wird im UI-Thread der Anwendung ausgelöst<br/>                                                                                                                           |
| [**Malerei**](inkoverlay-painting.md)                                           | Wird im UI-Thread der Anwendung ausgelöst<br/>                                                                                                                           |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)                           | Wird für den Ink-Thread oder für den Thread ausgelöst, der die [**Selection-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) des [**InkOverlay-Objekts**](inkoverlay-class.md) aktualisiert.<br/> |
| [**Selectionchanging**](inkoverlay-selectionchanging.md)                         | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**Selectionmoved**](inkoverlay-selectionmoved.md)                               | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**Selectionmoving**](inkoverlay-selectionmoving.md)                             | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**Selectionresized**](inkoverlay-selectionresized.md)                           | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**Selectionresizing**](inkoverlay-selectionresizing.md)                         | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**Takt**](inkoverlay-stroke.md)                                               | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**Striche gelöscht**](inkoverlay-strokesdeleted.md)                               | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**StrokesDeleting**](inkoverlay-strokesdeleting.md)                             | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**Systemgesture**](inkoverlay-systemgesture.md)                                 | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**Tabletadded**](inkoverlay-tabletadded.md)                                     | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |
| [**Tabletremoved**](inkoverlay-tabletremoved.md)                                 | Wird für den Ink-Thread ausgelöst<br/>                                                                                                                                        |



 

 

