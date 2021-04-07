---
title: Beispiel für eine Windows-touchbewegung (mtgesten)
description: In diesem Abschnitt wird das Beispiel für die Windows-touchbewegung beschrieben.
ms.assetid: 04166c9c-5de7-409e-9d5e-dd210a3a3f11
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
ms.openlocfilehash: 0e01d97e844af37caeb5c33f3cb780601da4629d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723445"
---
# <a name="windows-touch-gesture-sample-mtgestures"></a><span data-ttu-id="6b56c-110">Beispiel für eine Windows-touchbewegung (mtgesten)</span><span class="sxs-lookup"><span data-stu-id="6b56c-110">Windows Touch Gesture Sample (MTGestures)</span></span>

<span data-ttu-id="6b56c-111">In diesem Abschnitt wird das Beispiel für die Windows-touchbewegung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6b56c-111">This section describes the Windows Touch Gesture sample.</span></span>

<span data-ttu-id="6b56c-112">Das Beispiel für die Windows-touchbewegung veranschaulicht, wie Gesten Nachrichten verwendet werden, um ein durch die Graphics Device Interface (GDI) gerendertes Feld zu übersetzen, zu drehen und zu skalieren, indem die [**WM_GESTURE**](wm-gesture.md) Meldung verarbeitet</span><span class="sxs-lookup"><span data-stu-id="6b56c-112">The Windows Touch Gesture sample demonstrates how to use gesture messages to translate, rotate, and scale a box rendered by the Graphics Device Interface (GDI) by handling the [**WM_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="6b56c-113">Der folgende Screenshot zeigt, wie das Beispiel aussieht, wenn es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b56c-113">The following screen shot shows how the sample looks when it is running.</span></span>

![Screenshot, der das Beispiel für die Windows-touchbewegung anzeigt, wenn es ausgeführt wird, mit einem rotierten, schwarz dargestellten weißen Rechteck auf dem Bildschirm](images/mtgestures.png)

<span data-ttu-id="6b56c-115">In diesem Beispiel werden Gesten Meldungen an eine Gesten-Engine weitergegeben, die dann Methoden für Zeichnungsobjekte aufruft, um ein Objekt zu übersetzen, zu drehen und zu skalieren, das über Methoden zum Verarbeiten dieser Befehle verfügt.</span><span class="sxs-lookup"><span data-stu-id="6b56c-115">For this sample, gesture messages are passed to a gesture engine, which then calls methods on drawing objects to translate, rotate, and scale an object that has methods for handling these commands.</span></span> <span data-ttu-id="6b56c-116">Um die Funktionsweise des Beispiels zu veranschaulichen, sollten Sie die Schritte zum Aktivieren oder Deaktivieren von diagonalen Linien im gerenderten Feld mithilfe des Two-Finger Tap-Befehls ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b56c-116">To help show how the sample works, consider the steps for using the two-finger tap command to enable or disable diagonal lines in the rendered box.</span></span> <span data-ttu-id="6b56c-117">Ein Benutzer führt die Two-fingertap-Geste aus, die eine Meldung generiert, die vom Programm verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="6b56c-117">A user performs the two-finger tap gesture, which generates a message that is handled by the program.</span></span> <span data-ttu-id="6b56c-118">Wenn die Nachricht behandelt wird, wird ein boolescher Wert zum Rendern von diagonalen auf dem Zeichnungsobjekt gewechselt, und das-Objekt rendert dann die diagonalen Linien.</span><span class="sxs-lookup"><span data-stu-id="6b56c-118">When the message is handled, it will toggle a Boolean for rendering diagonals on the drawing object, and the object will then render the diagonal lines.</span></span>

<span data-ttu-id="6b56c-119">Der folgende Code zeigt, wie Gesten Meldungen aus der WndProc-Methode an die Gesten-Engine übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="6b56c-119">The following code shows how gesture messages are passed to the gesture engine from the WndProc method.</span></span>

```C++
    case WM_GESTURE:
        // The gesture-processing code is implemented in the CGestureEngine
        // class.
        return g_cGestureEngine.WndProc(hWnd,wParam,lParam);
        break;
```

<span data-ttu-id="6b56c-120">Der folgende Code zeigt, wie die Gesten-Engine den Two-Finger Tap-Befehl behandelt.</span><span class="sxs-lookup"><span data-stu-id="6b56c-120">The following code shows how the gesture engine handles the two-finger tap command.</span></span>

```C++
// Two-finger tap command
void CMyGestureEngine::ProcessTwoFingerTap(void)
{
    if(_pcRect)
    {
        _pcRect->ToggleDrawDiagonals();
    }
}
```

<span data-ttu-id="6b56c-121">Der folgende Code zeigt, wie das Zeichnungsobjekt seine diagonals schaltet.</span><span class="sxs-lookup"><span data-stu-id="6b56c-121">The following code shows how the drawing object toggles its diagonals.</span></span>

```C++
void ToggleDrawDiagonals(void){_bDrawDiagonals = !_bDrawDiagonals;}
```

<span data-ttu-id="6b56c-122">Der folgende Code zeigt, wie das-Objekt in der Draw-Methode diagonal Linien rendert.</span><span class="sxs-lookup"><span data-stu-id="6b56c-122">The following code shows how the object renders diagonal lines in its draw method.</span></span>

```C++
    if(_bDrawDiagonals)
    {
        // draw diagonals
        MoveToEx(hdc,ptRect[0].x,ptRect[0].y,NULL);
        LineTo(hdc,ptRect[2].x,ptRect[2].y);
        MoveToEx(hdc,ptRect[1].x,ptRect[1].y,NULL);
        LineTo(hdc,ptRect[3].x,ptRect[3].y);
    }
```

## <a name="related-topics"></a><span data-ttu-id="6b56c-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b56c-123">Related topics</span></span>

<span data-ttu-id="6b56c-124">[Multitouch-Gesten Anwendung (c#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [Multitouch-Gesten Anwendung (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touch-Beispiele](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="6b56c-124">[Multi-touch Gestures Application (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [Multi-touch Gestures Application (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
