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
# <a name="windows-touch-gesture-sample-mtgestures"></a>Beispiel für eine Windows-touchbewegung (mtgesten)

In diesem Abschnitt wird das Beispiel für die Windows-touchbewegung beschrieben.

Das Beispiel für die Windows-touchbewegung veranschaulicht, wie Gesten Nachrichten verwendet werden, um ein durch die Graphics Device Interface (GDI) gerendertes Feld zu übersetzen, zu drehen und zu skalieren, indem die [**WM_GESTURE**](wm-gesture.md) Meldung verarbeitet Der folgende Screenshot zeigt, wie das Beispiel aussieht, wenn es ausgeführt wird.

![Screenshot, der das Beispiel für die Windows-touchbewegung anzeigt, wenn es ausgeführt wird, mit einem rotierten, schwarz dargestellten weißen Rechteck auf dem Bildschirm](images/mtgestures.png)

In diesem Beispiel werden Gesten Meldungen an eine Gesten-Engine weitergegeben, die dann Methoden für Zeichnungsobjekte aufruft, um ein Objekt zu übersetzen, zu drehen und zu skalieren, das über Methoden zum Verarbeiten dieser Befehle verfügt. Um die Funktionsweise des Beispiels zu veranschaulichen, sollten Sie die Schritte zum Aktivieren oder Deaktivieren von diagonalen Linien im gerenderten Feld mithilfe des Two-Finger Tap-Befehls ausführen. Ein Benutzer führt die Two-fingertap-Geste aus, die eine Meldung generiert, die vom Programm verarbeitet wird. Wenn die Nachricht behandelt wird, wird ein boolescher Wert zum Rendern von diagonalen auf dem Zeichnungsobjekt gewechselt, und das-Objekt rendert dann die diagonalen Linien.

Der folgende Code zeigt, wie Gesten Meldungen aus der WndProc-Methode an die Gesten-Engine übermittelt werden.

```C++
    case WM_GESTURE:
        // The gesture-processing code is implemented in the CGestureEngine
        // class.
        return g_cGestureEngine.WndProc(hWnd,wParam,lParam);
        break;
```

Der folgende Code zeigt, wie die Gesten-Engine den Two-Finger Tap-Befehl behandelt.

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

Der folgende Code zeigt, wie das Zeichnungsobjekt seine diagonals schaltet.

```C++
void ToggleDrawDiagonals(void){_bDrawDiagonals = !_bDrawDiagonals;}
```

Der folgende Code zeigt, wie das-Objekt in der Draw-Methode diagonal Linien rendert.

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

## <a name="related-topics"></a>Zugehörige Themen

[Multitouch-Gesten Anwendung (c#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [Multitouch-Gesten Anwendung (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touch-Beispiele](windows-touch-samples.md)
