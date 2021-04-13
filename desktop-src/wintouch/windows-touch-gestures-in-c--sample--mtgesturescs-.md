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
# <a name="windows-touch-gestures-in-c-sample-mtgesturescs"></a><span data-ttu-id="1038a-110">Windows-Touchgesten in c#-Beispiel (mtgesturescs)</span><span class="sxs-lookup"><span data-stu-id="1038a-110">Windows Touch Gestures in C# Sample (MTGesturesCS)</span></span>

<span data-ttu-id="1038a-111">In diesem Abschnitt wird das Beispiel für Windows-Touchgesten in c# beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1038a-111">This section describes the Windows Touch Gestures sample in C#.</span></span>

<span data-ttu-id="1038a-112">In diesem Beispiel für die Windows-touchbewegung wird veranschaulicht, wie Gesten Nachrichten verwendet werden, um ein durch die Graphics Device Interface (GDI) gerendertes Feld zu übersetzen, zu drehen und zu skalieren, indem die [**WM_GESTURE**](wm-gesture.md)</span><span class="sxs-lookup"><span data-stu-id="1038a-112">This Windows Touch Gestures sample demonstrates how to use gesture messages to translate, rotate, and scale a box rendered by the Graphics Device Interface (GDI) by handling the [**WM_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="1038a-113">Der folgende Screenshot zeigt, wie das Beispiel aussieht, wenn es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1038a-113">The following screen shot shows how the sample looks when it is running.</span></span>

![Screenshot mit den Windows-Touchgesten in c sharp Sample, wenn diese ausgeführt wird, wobei ein auf dem Bildschirm zentrierter, Schwarzes, Schwarzes, weißes Rechteck angezeigt wird](images/mtgesturescs.png)

<span data-ttu-id="1038a-115">In diesem Beispiel werden Gesten Meldungen an eine Gesten-Engine weitergegeben, die dann Methoden für Zeichnungsobjekte aufruft, um ein Objekt zu übersetzen, zu drehen und zu skalieren, das über Methoden zum Verarbeiten dieser Befehle verfügt.</span><span class="sxs-lookup"><span data-stu-id="1038a-115">For this sample, gesture messages are passed to a gesture engine which then calls methods on drawing objects to translate, rotate, and scale an object that has methods for handling these commands.</span></span> <span data-ttu-id="1038a-116">Um dies in c# zu ermöglichen, wird eine spezielle Form, touchableform, erstellt, um Gesten Nachrichten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1038a-116">To make this possible in C#, a special form, TouchableForm, is created to handle gesture messages.</span></span> <span data-ttu-id="1038a-117">Dieses Formular verwendet dann die Nachrichten, um Änderungen an einem Zeichnungsobjekt (DrawingObject) vorzunehmen, um zu ändern, wie das Objekt in der Paint-Methode gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="1038a-117">This form then uses the messages to make changes on a drawing object, DrawingObject, to change how the object renders in the Paint method.</span></span>

<span data-ttu-id="1038a-118">Um die Funktionsweise des Beispiels zu veranschaulichen, sollten Sie die Schritte zum Übersetzen der gerenderten Box mithilfe des Befehls "Pan" übersetzen.</span><span class="sxs-lookup"><span data-stu-id="1038a-118">To help show how the sample works, consider the steps for using the pan command to translate the rendered box.</span></span> <span data-ttu-id="1038a-119">Ein Benutzer führt die schwenken-Geste aus, die eine [**WM_GESTURE**](wm-gesture.md) Meldung mit dem Gesten Bezeichner GID_PAN generiert.</span><span class="sxs-lookup"><span data-stu-id="1038a-119">A user performs the pan gesture which generates a [**WM_GESTURE**](wm-gesture.md) message with the gesture identifier GID_PAN.</span></span> <span data-ttu-id="1038a-120">Touchableform verarbeitet diese Nachrichten und aktualisiert die Position des Zeichnungs Objekts, und das Objekt wird dann selbst übersetzt.</span><span class="sxs-lookup"><span data-stu-id="1038a-120">The TouchableForm handles this messages and updates the position of the drawing object, and the object will then render itself translated.</span></span>

<span data-ttu-id="1038a-121">Der folgende Code zeigt, wie der Gesten Handler Parameter aus der [**WM_GESTURE**](wm-gesture.md) Nachricht abruft und dann die Übersetzung in der gerenderten Box durch einen Rückruf der Move-Methode des Zeichnungs Objekts ausführt.</span><span class="sxs-lookup"><span data-stu-id="1038a-121">The following code shows how the gesture handler retrieves parameters from the [**WM_GESTURE**](wm-gesture.md) message and then performs translation on the rendered box through a call to the drawing object's move method.</span></span>

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

<span data-ttu-id="1038a-122">Der folgende Code zeigt, wie die Move-Methode des Zeichnungs Objekts interne Positions Variablen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="1038a-122">The following code shows how the drawing object's move method updates internal position variables.</span></span>

```CSharp
        public void Move(int deltaX,int deltaY)
        {
            _ptCenter.X += deltaX;
            _ptCenter.Y += deltaY;
        }
```

<span data-ttu-id="1038a-123">Der folgende Code zeigt, wie die Position in der Paint-Methode des Zeichnungs Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1038a-123">The following code shows how the position is used in the drawing object's paint method.</span></span>

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

<span data-ttu-id="1038a-124">Schwenkbewegungen bewirken, dass das Feld gezeichnet gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="1038a-124">Pan gestures will cause the drawn box to be rendered translated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1038a-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1038a-125">Related topics</span></span>

<span data-ttu-id="1038a-126">[Multitouch-Gesten Anwendung (c#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [Multitouch-Gesten Anwendung (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touch-Beispiele](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="1038a-126">[Multi-touch Gestures Application (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [Multi-touch Gestures Application (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
