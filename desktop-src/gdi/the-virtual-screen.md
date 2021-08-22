---
description: Das umrandende Rechteck aller Monitore ist der virtuelle Bildschirm. Der Desktop deckt den virtuellen Bildschirm statt eines einzelnen Monitors ab. Die folgende Abbildung zeigt eine mögliche Anordnung von drei Monitoren.
ms.assetid: 3f84027d-f316-4454-92ad-2d36d10b2ec8
title: Der virtuelle Bildschirm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5516ef0cb5d99124200ab7810e484ea79027cf832a0e8da74833bf709ce5cc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037518"
---
# <a name="the-virtual-screen"></a>Der virtuelle Bildschirm

Das umrandende Rechteck aller Monitore ist der *virtuelle Bildschirm*. Der Desktop deckt den virtuellen Bildschirm statt eines einzelnen Monitors ab. Die folgende Abbildung zeigt eine mögliche Anordnung von drei Monitoren.

![Abbildung mit drei Feldern, die Monitore darstellen, die in einem Feld angeordnet sind, das den virtuellen Bildschirm darstellt](images/multimon-1.png)

Der *primäre Monitor* enthält den Ursprung (0,0). Dies ist für die Kompatibilität mit vorhandenen Anwendungen, die einen Monitor mit einem Ursprung erwarten, zu gewährleisten. Der primäre Monitor muss sich jedoch nicht in der oberen linken Ecke des virtuellen Bildschirms finden. In Abbildung 1 befindet sie sich in der Nähe des Mittelpunkts. Wenn sich der primäre Monitor nicht links oben auf dem virtuellen Bildschirm befindet, haben Teile des virtuellen Bildschirms negative Koordinaten. Da die Anordnung von Monitoren vom Benutzer festgelegt wird, sollten alle Anwendungen so entworfen werden, dass sie mit negativen Koordinaten funktionieren. Weitere Informationen finden Sie unter [Überlegungen zu mehreren Monitoren für ältere Programme.](multiple-monitor-considerations-for-older-programs.md)

Die Koordinaten des virtuellen Bildschirms werden aufgrund der 16-Bit-Werte, die in vielen vorhandenen Nachrichten enthalten sind, durch einen signierten 16-Bit-Wert dargestellt. Daher sind die Begrenzungen des virtuellen Bildschirms:

``` syntax
SHORT_MIN    <= rcVirtualScreen.left   <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.right  <= SHORT_MAX
SHORT_MIN    <= rcVirtualScreen.top    <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.bottom <= SHORT_MAX
```

 

 



