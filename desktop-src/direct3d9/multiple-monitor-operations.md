---
description: 'Wenn ein Gerät erfolgreich zurückgesetzt wird (IDirect3DDevice9:: Reset) oder (IDirect3D9:: builatedevice) in voll Bild Vorgängen erstellt wurde, wird das Direct3D-Objekt, das das Gerät erstellt hat, als Besitzer aller Adapter auf diesem System markiert.'
ms.assetid: df3b6ed7-830b-4635-9295-fff05cc35891
title: Multiple-Monitor Vorgänge (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04427db6c91ff85706040589a89f6fdcfb3761e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345995"
---
# <a name="multiple-monitor-operations-direct3d-9"></a>Multiple-Monitor Vorgänge (Direct3D 9)

Wenn ein Gerät erfolgreich zurückgesetzt wird ([**IDirect3DDevice9:: Reset**](/windows/desktop/api)) oder ([**IDirect3D9:: builatedevice**](/windows/desktop/api)) in voll Bild Vorgängen erstellt wurde, wird das Direct3D-Objekt, das das Gerät erstellt hat, als Besitzer aller Adapter auf diesem System markiert. Dieser Status wird als exklusiver Modus bezeichnet, und das Direct3D-Objekt besitzt den exklusiven Modus. Der exklusive Modus bedeutet, dass Geräte, die von einem anderen Direct3D-Objekt erstellt wurden, keine voll Bild Vorgänge annehmen und keinen Videospeicher zuordnen können. Wenn ein Direct3D-Objekt den exklusiven Modus annimmt, werden darüber hinaus alle anderen Geräte als der Vollbildmodus in den Zustand "verloren" versetzt. Weitere Informationen finden Sie unter [verlorene Geräte (Direct3D 9)](lost-devices.md).

Zusammen mit dem exklusiven Modus wird das Direct3D-Objekt über das Fokus Fenster informiert, das vom Gerät verwendet wird. Der exklusive Modus wird freigegeben, wenn das endgültige voll Bild Gerät, das diesem Direct3D-Objekt gehört, entweder auf den Fenstermodus zurückgesetzt oder zerstört wird.

Geräte können in zwei Kategorien unterteilt werden, wenn ein Direct3D-Objekt im exklusiven Modus ist. Die erste Kategorie von Geräten hat die folgenden Eigenschaften:

-   Sie werden vom gleichen Direct3D-Objekt erstellt, das das voll Bild geschützte Gerät erstellt hat.
-   Sie haben dasselbe Fokus Fenster wie das Gerät, das voll Bildschirm ist.
-   Sie stellen einen anderen Adapter von allen voll Bild Geräten dar.

Geräte in dieser Kategorie haben keine Einschränkungen hinsichtlich ihrer Fähigkeit, zurückgesetzt oder erstellt zu werden, und Sie werden nicht in den Zustand "verloren" versetzt. Geräte in dieser Kategorie können sogar in den Vollbildmodus versetzt werden.

Geräte, die nicht in die erste Kategorie fallen: Geräte, die von einem anderen Direct3D-Objekt erstellt, mit einem anderen Fokus Fenster erstellt und für einen Adapter mit einem bereits voll Bild-Gerät erstellt wurden, können nicht zurückgesetzt werden und bleiben verloren, bis der exklusive Modus verloren geht. Demzufolge kann eine Anwendung mit mehreren Monitoren mehrere Geräte im Vollbildmodus platzieren, aber nur, wenn alle diese Geräte für verschiedene Adapter vorhanden sind, die vom gleichen Direct3D-Objekt erstellt wurden und dasselbe Fokus Fenster gemeinsam verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Präsentieren einer Szene](presenting-a-scene.md)
</dt> </dl>

 

 



