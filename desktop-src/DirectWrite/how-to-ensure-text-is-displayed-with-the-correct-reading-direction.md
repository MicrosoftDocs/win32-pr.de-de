---
title: Stellen Sie sicher, dass Text mit der richtigen Leserichtung angezeigt wird.
description: Einige Sprachen, z. b. Arabisch und Hebräisch, erfordern eine Leserichtung von rechts nach links.
ms.assetid: fa9a3dd6-575a-4877-a488-22845c6726c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d97eee49a830986718c04b4adab7443e488093
ms.sourcegitcommit: 43b2f5209d67eae96b17c03bac2a2afab1f4d30a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730169"
---
# <a name="ensure-text-is-displayed-with-the-correct-reading-direction"></a>Stellen Sie sicher, dass Text mit der richtigen Leserichtung angezeigt wird.

Einige Sprachen, z. b. Arabisch und Hebräisch, erfordern eine Leserichtung von rechts nach links. Bei einem Objekt im [DirectWrite](direct-write-portal.md) -Textformat ist die Standard Leserichtung von links nach rechts. DirectWrite leitet die Leserichtung nicht automatisch aus dem Gebiets Schema ab, sodass Sie dies selbst tun müssen.

Holen Sie zuerst die erweiterten stilflags für das Fenster, in dem der Text gerendert wird, indem Sie das in WINDOWSX. h definierte getwindowstyleex-Makro verwenden.


```C++
// Get the window extended style flagsfor the current window.
DWORD dwStyle = GetWindowExStyle(hwnd_);
```



Das-Makro gibt einen DWORD-Wert zurück, der aus mehreren Flags zusammen mit bitweisen or-Vorgängen besteht. Sie müssen bestimmen, ob die spezifischen Flags, die die Leserichtung beeinflussen, vorhanden sind.

Es gibt zwei verschiedene Flags, die sich auf die Leserichtung beziehen: WS \_ Ex \_ layoutrtl und WS \_ Ex \_ RtlReading.

Verwenden Sie den bitweisen AND-Operator (&) mit der dwstyle-Variablen und dem WS \_ Ex \_ layoutrtl-Makro, um einen booleschen Wert zu speichern, der angibt, ob das Layout gespiegelt wird.


```C++
// Is the WS_EX_LAYOUTRTL flag present?
BOOL bWSLayout = dwStyle & WS_EX_LAYOUTRTL;
```



Führen Sie die gleichen Schritte für das WS \_ Ex \_ RtlReading-Flag aus.


```C++
// Is the WS_EX_RLTREADING flag present?
BOOL bWSReading = dwStyle & WS_EX_RTLREADING;
```



Legen Sie die Leserichtung mithilfe der Methode [**idschreitetextformat:: setreadingdirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) fest. Der Standardwert ist von links nach rechts, sodass Sie nur die Leserichtung festlegen müssen, wenn Sie von rechts nach links ist.

> [!Note]  
> WS \_ Ex \_ layoutrtl spiegelt das gesamte Layout wider und impliziert die Leserichtung von rechts nach links. Legen Sie daher die Leserichtung nur dann fest, wenn eines dieser Flags vorhanden ist. Wenn beide vorhanden sind, brechen Sie einander ab, und die Leserichtung für das Textformat sollte von links nach rechts erfolgen.

 


```C++
// If either the WS_EX_LAYOUTRTL flag or the WS_EX_RLTREADING flag is present,
// but NOT BOTH, set the reading direction to right to left.
if ((bWSLayout && !bWSReading)
||  (!bWSLayout && bWSReading))
{
    pTextFormat_->SetReadingDirection(DWRITE_READING_DIRECTION_RIGHT_TO_LEFT);
}
```



 

 
