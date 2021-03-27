---
description: Das umgebende Rechteck aller Monitore ist der virtuelle Bildschirm. Der Desktop deckt den virtuellen Bildschirm anstelle eines einzelnen Monitors ab. Die folgende Abbildung zeigt eine mögliche Anordnung von drei Monitoren.
ms.assetid: 3f84027d-f316-4454-92ad-2d36d10b2ec8
title: Der virtuelle Bildschirm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4550ab0f849b90523842e6cc4e093c238ff11cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995126"
---
# <a name="the-virtual-screen"></a>Der virtuelle Bildschirm

Das umgebende Rechteck aller Monitore ist der *virtuelle Bildschirm*. Der Desktop deckt den virtuellen Bildschirm anstelle eines einzelnen Monitors ab. Die folgende Abbildung zeigt eine mögliche Anordnung von drei Monitoren.

![Abbildung mit drei Feldern, die Monitore darstellen, die in einem Feld angeordnet sind, das den virtuellen Bildschirm darstellt](images/multimon-1.png)

Der *primäre Monitor* enthält den Ursprung (0,0). Dies dient der Kompatibilität mit vorhandenen Anwendungen, die einen Monitor mit einem Ursprung erwarten. Der primäre Monitor muss sich jedoch nicht in der oberen linken Ecke des virtuellen Bildschirms befinden. In Abbildung 1 befindet Sie sich in der Mitte. Wenn sich der primäre Monitor nicht in der oberen linken Ecke des virtuellen Bildschirms befindet, sind Teile des virtuellen Bildschirms mit negativen Koordinaten vorhanden. Da die Anordnung von Monitoren vom Benutzer festgelegt wird, sollten alle Anwendungen für die Arbeit mit negativen Koordinaten konzipiert werden. Weitere Informationen finden Sie unter [Überlegungen zu mehreren Monitoren für ältere Programme](multiple-monitor-considerations-for-older-programs.md).

Die Koordinaten des virtuellen Bildschirms werden aufgrund der 16-Bit-Werte, die in vielen vorhandenen Nachrichten enthalten sind, durch einen 16-Bit-Wert mit Vorzeichen dargestellt. Folglich lauten die Begrenzungen des virtuellen Bildschirms wie folgt:

``` syntax
SHORT_MIN    <= rcVirtualScreen.left   <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.right  <= SHORT_MAX
SHORT_MIN    <= rcVirtualScreen.top    <= SHORT_MAX - 1
SHORT_MIN +1 <= rcVirtualScreen.bottom <= SHORT_MAX
```

 

 



