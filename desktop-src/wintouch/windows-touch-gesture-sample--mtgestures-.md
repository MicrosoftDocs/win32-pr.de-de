---
title: Windows Touchgestenbeispiel (MTGestures)
description: In diesem Abschnitt wird das Beispiel für Windows Touchgeste beschrieben.
ms.assetid: 04166c9c-5de7-409e-9d5e-dd210a3a3f11
keywords:
- Windows Toucheingabe, Codebeispiele
- Windows Toucheingabe, Beispielcode
- Windows Toucheingabe, Gesten
- Windows Toucheingabe, Gestenbeispiele
- Gestenbeispiele
- Gesten, Beispielcode
- Gesten, Codebeispiele
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 656b269eae779cd999680e165ba071d983d18526c2e9b873c5a916d61ccdb9f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110584"
---
# <a name="windows-touch-gesture-sample-mtgestures"></a>Windows Touchgestenbeispiel (MTGestures)

In diesem Abschnitt wird das Beispiel für Windows Touchgeste beschrieben.

Im Windows Beispiel für Touchgesten wird veranschaulicht, wie Gestennachrichten verwendet werden, um ein vom Graphics Device Interface (GDI) gerenderte Feld zu übersetzen, zu drehen und zu skalieren, indem die [**WM_GESTURE**](wm-gesture.md) Nachricht verarbeitet wird. Der folgende Screenshot zeigt, wie das Beispiel aussieht, wenn es ausgeführt wird.

![Screenshot des Beispiels für die Windows-Touchgeste während der Ausführung mit einem gedrehten, schwarz umrandeten weißen Rechteck auf dem Bildschirm](images/mtgestures.png)

In diesem Beispiel werden Gestenmeldungen an eine Gesten-Engine übergeben, die dann Methoden zum Zeichnen von Objekten aufruft, um ein Objekt zu übersetzen, zu drehen und zu skalieren, das Methoden für die Verarbeitung dieser Befehle enthält. Um zu zeigen, wie das Beispiel funktioniert, sollten Sie die Schritte zum Verwenden des Befehls zum Tippen mit zwei Fingern zum Aktivieren oder Deaktivieren diagonaler Linien im gerenderten Feld in Betracht ziehen. Ein Benutzer führt die Tippbewegung mit zwei Fingern aus, die eine Nachricht generiert, die vom Programm verarbeitet wird. Wenn die Nachricht verarbeitet wird, schaltet sie einen booleschen Wert zum Rendern von Diagonalen für das Zeichnungsobjekt um, und das Objekt rendert dann die diagonalen Linien.

Der folgende Code zeigt, wie Gestenmeldungen von der WndProc-Methode an die Gesten-Engine übergeben werden.

```C++
    case WM_GESTURE:
        // The gesture-processing code is implemented in the CGestureEngine
        // class.
        return g_cGestureEngine.WndProc(hWnd,wParam,lParam);
        break;
```

Der folgende Code zeigt, wie die Gesten-Engine den Befehl zum Tippen mit zwei Fingern behandelt.

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

Der folgende Code zeigt, wie das Zeichnungsobjekt seine Diagonalen umschaltet.

```C++
void ToggleDrawDiagonals(void){_bDrawDiagonals = !_bDrawDiagonals;}
```

Der folgende Code zeigt, wie das Objekt diagonale Linien in seiner Draw-Methode rendert.

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

[Multitouch Gestures Application (C#),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS) [Multitouch Gestures Application (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp) [, Windows Touch Samples](windows-touch-samples.md)
