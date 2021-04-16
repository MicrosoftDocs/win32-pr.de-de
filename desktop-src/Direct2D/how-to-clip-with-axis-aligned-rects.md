---
title: Vorgehensweise beim Abschneiden mit einem Axis-Aligned Clip-Rechteck
description: Zeigt, wie Sie einen Bereich mit einem Achsen ausgerichteten Clip Rechteck ausschneiden.
ms.assetid: 4196653a-9177-4a41-9db9-4738a41313aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9fea904f9df396918d2cdfdb5205f6dd0197d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104564076"
---
# <a name="how-to-clip-with-an-axis-aligned-clip-rectangle"></a>Vorgehensweise beim Abschneiden mit einem Axis-Aligned Clip-Rechteck

In diesem Thema wird beschrieben, wie Sie ein Bild mithilfe eines Achsen ausgerichteten Clip Rechtecks Ausschneiden. Bei diesem Ansatz werden nur rechteckige Clips erzeugt, da die Inhalts Begrenzungen an der Achse des Rechtecks ausgerichtet werden. Diese Vorgehensweise ist effizienter als die Verwendung von Ebenen mit den Inhalts Begrenzungen. Weitere Informationen finden Sie unter[Übersicht über Ebenen](direct2d-layers-overview.md).

**So schneiden Sie mithilfe eines Achsen ausgerichteten Clip Rechtecks ab**

1.  Laden Sie das ursprüngliche Bild aus einer Ressource. Weitere Informationen zum Laden einer Bitmap finden Sie unter Gewusst [wie: Laden einer Bitmap aus einer Ressource](how-to-load-a-bitmap-from-a-resource.md).
2.  [**ID2D1RenderTarget::P ushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) zum Angeben eines Rechtecks. Die renderingbefehle werden auf das Rechteck zugeschnitten.

3.  Zeichnen Sie das ursprüngliche Bild.
4.  [**ID2D1RenderTarget::P opaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) aufgerufen, um den letzten an der Achse ausgerichteten Clip aus dem Renderziel zu entfernen.

In der folgenden Abbildung ist beispielsweise die ursprüngliche Bitmap auf der linken Seite 200 \* 130 Pixel. Die Bitmap auf der rechten Seite ist die ursprüngliche Bitmap, die auf das Achsen ausgerichtete Clip Rechteck zugeschnitten ist. Die Abmessungen sind (20, 20) bis (100, 100).

![Abbildung einer Goldfisch-Bitmap vor und nach dem abgeschnitten der Bitmap](images/cliparegion-axisalignedclip.png)

Um das abgeschnittene Bild zu erstellen, erstellen Sie eine Rechteck Struktur als Clippingbereich. Nennen Sie [**pushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) mit dem Clippingbereich, und zeichnen Sie das ursprüngliche Bild. Nennen Sie [**popaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) , um den Clip aus dem Renderziel zu entfernen. Dies wird im folgenden Code veranschaulicht.


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 