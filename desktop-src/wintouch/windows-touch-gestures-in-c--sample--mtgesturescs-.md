---
title: Windows Touchgesten in C-Beispiel (MTGesturesCS)
description: In diesem Abschnitt wird das Beispiel Windows Touchgesten in C\ beschrieben.
ms.assetid: 4b2d70bb-47e4-4448-97e2-6f6e29d1dfdf
keywords:
- Windows Touch,Codebeispiele
- Windows Touch,Beispielcode
- Windows Touch,Gesten
- Windows Touch,Gestenbeispiele
- Gestenbeispiele
- Gesten, Beispielcode
- Gesten,Codebeispiele
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: ac3a7c0772ad7329d14d9909b55f8a60ef6e7d7473a06fcba921297117a00b6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089904"
---
# <a name="windows-touch-gestures-in-c-sample-mtgesturescs"></a>Windows Beispiel für Touchgesten in C# (MTGesturesCS)

In diesem Abschnitt wird das Beispiel Windows Touchgesten in C# beschrieben.

Dieses beispiel Windows Touch-Gesten veranschaulicht, wie Gestenmeldungen verwendet werden, um ein feld zu übersetzen, zu drehen und zu skalieren, das vom Graphics Device Interface (GDI) gerendert wird, indem die WM_GESTURE [**wird.**](wm-gesture.md) Der folgende Screenshot zeigt, wie das Beispiel aussieht, wenn es ausgeführt wird.

![Screenshot, der die Touchbewegungen von Fenstern in c sharp-Beispiel zeigt, wenn es ausgeführt wird, mit einem schwarzen, weißen Rechteck, das auf dem Bildschirm zentriert ist](images/mtgesturescs.png)

Für dieses Beispiel werden Gestenmeldungen an eine Gesten-Engine übergeben, die dann Methoden für Zeichnungsobjekte aufruft, um ein Objekt zu übersetzen, zu drehen und zu skalieren, das über Methoden zum Behandeln dieser Befehle verfügt. Um dies in C# zu ermöglichen, wird eine spezielle Form, TouchableForm, erstellt, um Gestenmeldungen zu verarbeiten. Dieses Formular verwendet dann die Meldungen, um Änderungen an einem Zeichnungsobjekt (DrawingObject) vorzunehmen, um zu ändern, wie das Objekt in der Paint wird.

Um die Funktionsweise des Beispiels zu beispielen, sollten Sie die Schritte für die Verwendung des Schwenkbefehls zum Übersetzen des gerenderten Felds in Betracht ziehen. Ein Benutzer führt die Schwenkbewegung aus, die eine [**WM_GESTURE**](wm-gesture.md) mit dem Gestenbezeichner GID_PAN. TouchableForm verarbeitet diese Meldungen und aktualisiert die Position des Zeichnungsobjekts, und das Objekt rendert sich selbst übersetzt.

Der folgende Code zeigt, wie der Gestenhandler Parameter aus der [**WM_GESTURE-Nachricht**](wm-gesture.md) abruft und dann die Übersetzung des gerenderten Felds über einen Aufruf der Move-Methode des Zeichnungsobjekts ausführt.

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

Der folgende Code zeigt, wie die Move-Methode des Zeichnungsobjekts interne Positionsvariablen aktualisiert.

```CSharp
        public void Move(int deltaX,int deltaY)
        {
            _ptCenter.X += deltaX;
            _ptCenter.Y += deltaY;
        }
```

Der folgende Code zeigt, wie die Position in der Paint-Methode des Zeichnungsobjekts verwendet wird.

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

Schwenkgesten bewirken, dass das gezeichnete Feld übersetzt wird.

## <a name="related-topics"></a>Zugehörige Themen

[Multi-Touch-Gestenanwendung (C#),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS) [Multi-Touch-Gestenanwendung (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touchbeispiele](windows-touch-samples.md)
