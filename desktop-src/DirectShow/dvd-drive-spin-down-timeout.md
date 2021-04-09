---
description: Timeout des DVD-Laufwerks
ms.assetid: 2295253d-0199-41b4-95a8-cda049ca93c7
title: Timeout des DVD-Laufwerks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda6853830ee7289e529d029c78fe4e56e4a0e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860411"
---
# <a name="dvd-drive-spin-down-timeout"></a>Timeout des DVD-Laufwerks

Auf Laptop Computern ist es möglicherweise wünschenswert, die Zeitspanne zu reduzieren, während der ein DVD-Laufwerk nach dem Anhalten der Wiedergabe nach dem Anhalten des Benutzers weiter gedreht wird. Standardmäßig sorgt der DVD-Navigator dafür, dass die CD für zwei Minuten spinnt ist. Dieser Wert kann in der Windows-Registrierung unter diesem Schlüssel geändert werden:


```C++
DWORD HKLM\SOFTWARE\Microsoft\DVDNavigator\DriveSpindown 
[Sec]
```



where


```
Sec
```



die Drehzeit in Sekunden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anhänge](appendixes.md)
</dt> </dl>

 

 



