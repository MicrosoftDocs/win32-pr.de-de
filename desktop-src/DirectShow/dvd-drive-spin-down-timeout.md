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
# <a name="dvd-drive-spin-down-timeout"></a><span data-ttu-id="23256-103">Timeout des DVD-Laufwerks</span><span class="sxs-lookup"><span data-stu-id="23256-103">DVD Drive Spin Down Timeout</span></span>

<span data-ttu-id="23256-104">Auf Laptop Computern ist es möglicherweise wünschenswert, die Zeitspanne zu reduzieren, während der ein DVD-Laufwerk nach dem Anhalten der Wiedergabe nach dem Anhalten des Benutzers weiter gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="23256-104">On laptop computers, to conserve battery life it may be desirable to reduce the length of time that a DVD drive will continue to spin after the user has paused playback.</span></span> <span data-ttu-id="23256-105">Standardmäßig sorgt der DVD-Navigator dafür, dass die CD für zwei Minuten spinnt ist.</span><span class="sxs-lookup"><span data-stu-id="23256-105">By default, the DVD Navigator keeps the disc spinning for two minutes.</span></span> <span data-ttu-id="23256-106">Dieser Wert kann in der Windows-Registrierung unter diesem Schlüssel geändert werden:</span><span class="sxs-lookup"><span data-stu-id="23256-106">This value can be modified in the Windows Registry under this key:</span></span>


```C++
DWORD HKLM\SOFTWARE\Microsoft\DVDNavigator\DriveSpindown 
[Sec]
```



<span data-ttu-id="23256-107">where</span><span class="sxs-lookup"><span data-stu-id="23256-107">where</span></span>


```
Sec
```



<span data-ttu-id="23256-108">die Drehzeit in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="23256-108">is the spin down time in seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23256-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="23256-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23256-110">Anhänge</span><span class="sxs-lookup"><span data-stu-id="23256-110">Appendixes</span></span>](appendixes.md)
</dt> </dl>

 

 



