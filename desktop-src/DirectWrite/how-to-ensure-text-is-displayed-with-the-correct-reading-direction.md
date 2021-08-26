---
title: Stellen Sie sicher, dass Text mit der richtigen Leserichtung angezeigt wird.
description: Einige Sprachen, z. B. Arabisch und Hebräisch, erfordern eine Leserichtung von rechts nach links.
ms.assetid: fa9a3dd6-575a-4877-a488-22845c6726c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3774e4d237863a218cadf5206e4dc4921bceaeaa06c00ab81057f80dd8ee6549
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982170"
---
# <a name="ensure-text-is-displayed-with-the-correct-reading-direction"></a>Stellen Sie sicher, dass Text mit der richtigen Leserichtung angezeigt wird.

Einige Sprachen, z. B. Arabisch und Hebräisch, erfordern eine Leserichtung von rechts nach links. Für [](direct-write-portal.md) ein DirectWrite-Textformatobjekt ist die Standardleserichtung von links nach rechts. DirectWrite die Leserichtung nicht automatisch aus dem -Locale abgeleitet, daher müssen Sie dies selbst tun.

Zunächst können Sie die erweiterten Stilflags für das Fenster, in dem der Text gerendert wird, mithilfe des in windowsx.h definierten Makros GetWindowStyleEx erhalten.


```C++
// Get the window extended style flagsfor the current window.
DWORD dwStyle = GetWindowExStyle(hwnd_);
```



Das Makro gibt einen DWORD-Wert zurück, der aus mehreren Flags in Kombination mit bitweisem OR-Vorgängen besteht. Sie müssen ermitteln, ob die spezifischen Flags, die die Leserichtung beeinflussen, dort sind.

Es gibt zwei verschiedene Flags, die mit der Leserichtung verknüpft sind: WS \_ EX \_ LAYOUTRTL und WS \_ EX \_ RTLREADING.

Verwenden Sie den bitweise AND-Operator (&) mit der dwStyle-Variablen und dem WS EX LAYOUTRTL-Makro, um einen BOOL-Wert zu speichern, der angibt, ob das Layout \_ \_ gespiegelt ist.


```C++
// Is the WS_EX_LAYOUTRTL flag present?
BOOL bWSLayout = dwStyle & WS_EX_LAYOUTRTL;
```



Gehen Sie für das WS \_ EX \_ RTLREADING-Flag genauso vor.


```C++
// Is the WS_EX_RLTREADING flag present?
BOOL bWSReading = dwStyle & WS_EX_RTLREADING;
```



Legen Sie die Leserichtung mithilfe der [**IDWriteTextFormat::SetReadingDirection-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) fest. Der Standardwert ist von links nach rechts, sodass Sie die Leserichtung nur festlegen müssen, wenn sie von rechts nach links ist.

> [!Note]  
> WS EX LAYOUTRTL spiegelt das gesamte Layout und impliziert die Leserichtung von rechts nach links. Legen Sie daher die Leserichtung nur fest, wenn eines dieser \_ \_ Flags vorhanden ist. Wenn beide vorhanden sind, brechen sie einander ab, und die Leserichtung für das Textformat sollte von links nach rechts sein.

 


```C++
// If either the WS_EX_LAYOUTRTL flag or the WS_EX_RLTREADING flag is present,
// but NOT BOTH, set the reading direction to right to left.
if ((bWSLayout && !bWSReading)
||  (!bWSLayout && bWSReading))
{
    pTextFormat_->SetReadingDirection(DWRITE_READING_DIRECTION_RIGHT_TO_LEFT);
}
```



 

 
