---
title: Windows-Touchgesten in C-Beispiel (mtgesturescs)
description: In diesem Abschnitt wird das Beispiel für Windows-Touchgesten in C \ beschrieben.
ms.assetid: 4b2d70bb-47e4-4448-97e2-6f6e29d1dfdf
keywords:
- Windows-Fingereingabe, Codebeispiele
- Windows-Fingereingabe, Beispielcode
- Windows-Toucheingabe, Gesten
- Windows-Toucheingabe, Gesten Beispiele
- Gesten Beispiele
- Gesten, Beispielcode
- Gesten, Codebeispiele
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: e6ffc0e8caf63807d4df80a1b96229f2fa7b5ff9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389860"
---
# <a name="windows-touch-gestures-in-c-sample-mtgesturescs"></a>Windows-Touchgesten in c#-Beispiel (mtgesturescs)

In diesem Abschnitt wird das Beispiel für Windows-Touchgesten in c# beschrieben.

In diesem Beispiel für die Windows-touchbewegung wird veranschaulicht, wie Gesten Nachrichten verwendet werden, um ein durch die Graphics Device Interface (GDI) gerendertes Feld zu übersetzen, zu drehen und zu skalieren, indem die [**WM_GESTURE**](wm-gesture.md) Der folgende Screenshot zeigt, wie das Beispiel aussieht, wenn es ausgeführt wird.

![Screenshot mit den Windows-Touchgesten in c sharp Sample, wenn diese ausgeführt wird, wobei ein auf dem Bildschirm zentrierter, Schwarzes, Schwarzes, weißes Rechteck angezeigt wird](images/mtgesturescs.png)

In diesem Beispiel werden Gesten Meldungen an eine Gesten-Engine weitergegeben, die dann Methoden für Zeichnungsobjekte aufruft, um ein Objekt zu übersetzen, zu drehen und zu skalieren, das über Methoden zum Verarbeiten dieser Befehle verfügt. Um dies in c# zu ermöglichen, wird eine spezielle Form, touchableform, erstellt, um Gesten Nachrichten zu verarbeiten. Dieses Formular verwendet dann die Nachrichten, um Änderungen an einem Zeichnungsobjekt (DrawingObject) vorzunehmen, um zu ändern, wie das Objekt in der Paint-Methode gerendert wird.

Um die Funktionsweise des Beispiels zu veranschaulichen, sollten Sie die Schritte zum Übersetzen der gerenderten Box mithilfe des Befehls "Pan" übersetzen. Ein Benutzer führt die schwenken-Geste aus, die eine [**WM_GESTURE**](wm-gesture.md) Meldung mit dem Gesten Bezeichner GID_PAN generiert. Touchableform verarbeitet diese Nachrichten und aktualisiert die Position des Zeichnungs Objekts, und das Objekt wird dann selbst übersetzt.

Der folgende Code zeigt, wie der Gesten Handler Parameter aus der [**WM_GESTURE**](wm-gesture.md) Nachricht abruft und dann die Übersetzung in der gerenderten Box durch einen Rückruf der Move-Methode des Zeichnungs Objekts ausführt.

```CSharp
            switch (gi.dwID)
            {
                case GID_BEGIN:
                case GID_END:
                    break;
               (...)
                case GID_PAN:
                    switch (gi.dwFlags)
                    {
                        case GF_BEGIN:
                            _ptFirst.X = gi.ptsLocation.x;
                            _ptFirst.Y = gi.ptsLocation.y;
                            _ptFirst = PointToClient(_ptFirst);
                            break;

                        default:
                            // We read the second point of this gesture. It is a
                            // middle point between fingers in this new position
                            _ptSecond.X = gi.ptsLocation.x;
                            _ptSecond.Y = gi.ptsLocation.y;
                            _ptSecond = PointToClient(_ptSecond);

                            // We apply move operation of the object
                            _dwo.Move(_ptSecond.X - _ptFirst.X, _ptSecond.Y - _ptFirst.Y);

                            Invalidate();

                            // We have to copy second point into first one to
                            // prepare for the next step of this gesture.
                            _ptFirst = _ptSecond;
                            break;
                    }
                    break;
```

Der folgende Code zeigt, wie die Move-Methode des Zeichnungs Objekts interne Positions Variablen aktualisiert.

```CSharp
        public void Move(int deltaX,int deltaY)
        {
            _ptCenter.X += deltaX;
            _ptCenter.Y += deltaY;
        }
```

Der folgende Code zeigt, wie die Position in der Paint-Methode des Zeichnungs Objekts verwendet wird.

```CSharp
public void Paint(Graphics graphics)
        {
(...)
            for (int j = 0; j < 5; j++)
            {
                int idx = arrPts[j].X;
                int idy = arrPts[j].Y;

                // rotation
                arrPts[j].X = (int)(idx * dCos + idy * dSin);
                arrPts[j].Y = (int)(idy * dCos - idx * dSin);

                // translation
                arrPts[j].X += _ptCenter.X;
                arrPts[j].Y += _ptCenter.Y;
            }
(...)
        }
```

Schwenkbewegungen bewirken, dass das Feld gezeichnet gerendert wird.

## <a name="related-topics"></a>Zugehörige Themen

[Multitouch-Gesten Anwendung (c#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [Multitouch-Gesten Anwendung (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touch-Beispiele](windows-touch-samples.md)
