---
description: Wenn ein Gerät erfolgreich zurückgesetzt (IDirect3DDevice9::Reset) oder bei Vollbildvorgängen (IDirect3D9::CreateDevice) erstellt wird, wird das Direct3D-Objekt, das das Gerät erstellt hat, als DerEntität aller Adapter auf diesem System gekennzeichnet.
ms.assetid: df3b6ed7-830b-4635-9295-fff05cc35891
title: Multiple-Monitor Operations (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4f175c136cd432223eeaaf32cf44bfbb08e724b54b8afe1dbb9717c2d79a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728210"
---
# <a name="multiple-monitor-operations-direct3d-9"></a>Multiple-Monitor Operations (Direct3D 9)

Wenn ein Gerät erfolgreich zurückgesetzt ([**IDirect3DDevice9::Reset**](/windows/desktop/api)) oder erstellt ([**IDirect3D9::CreateDevice**](/windows/desktop/api)) in Vollbildvorgängen erstellt wurde, wird das Direct3D-Objekt, das das Gerät erstellt hat, als besitzend aller Adapter auf diesem System markiert. Dieser Zustand wird als exklusiver Modus bezeichnet, und das Direct3D-Objekt besitzt den exklusiven Modus. Der exklusive Modus bedeutet, dass Geräte, die von einem anderen Direct3D-Objekt erstellt wurden, weder Vollbildvorgänge voraussind noch Videospeicher zuordnen können. Wenn ein Direct3D-Objekt den exklusiven Modus an nimmt, werden darüber hinaus alle Geräte, die nicht im Vollbildmodus ausgeführt wurden, in den Zustand "Verloren" gesetzt. Weitere Informationen finden Sie unter [Verlorene Geräte (Direct3D 9).](lost-devices.md)

Zusammen mit dem exklusiven Modus wird das Direct3D-Objekt über das Fokusfenster informiert, das das Gerät verwendet. Der exklusive Modus wird freigegeben, wenn das endgültige Vollbildgerät, das sich im Besitz dieses Direct3D-Objekts befindet, entweder auf den Fenstermodus zurückgesetzt oder zerstört wird.

Geräte können in zwei Kategorien unterteilt werden, wenn ein Direct3D-Objekt den exklusiven Modus besitzt. Die erste Kategorie von Geräten hat die folgenden Merkmale.

-   Sie werden von demselben Direct3D-Objekt erstellt, mit dem das Gerät im Vollbildmodus erstellt wurde.
-   Sie verfügen über das gleiche Fokusfenster wie das Vollbildgerät.
-   Sie stellen einen anderen Adapter als ein beliebiges Vollbildgerät dar.

Für Geräte in dieser Kategorie gelten keine Einschränkungen hinsichtlich der Möglichkeit, zurückgesetzt oder erstellt zu werden, und sie befinden sich nicht im Zustand "Verloren". Geräte in dieser Kategorie können sogar in den Vollbildmodus wechseln.

Geräte, die nicht in die erste Kategorie fallen – Geräte, die von einem anderen Direct3D-Objekt erstellt, mit einem anderen Fokusfenster erstellt und für einen Adapter mit einem Bereits-Vollbildgerät erstellt wurden – können erst zurückgesetzt werden, wenn der exklusive Modus verloren geht. Daher kann eine Anwendung mit mehreren Monitoren mehrere Geräte im Vollbildmodus platzieren, aber nur, wenn alle diese Geräte für unterschiedliche Adapter sind, vom gleichen Direct3D-Objekt erstellt wurden und das gleiche Fokusfenster verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präsentieren einer Szene](presenting-a-scene.md)
</dt> </dl>

 

 



