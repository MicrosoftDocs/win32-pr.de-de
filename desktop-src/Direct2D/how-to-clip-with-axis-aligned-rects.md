---
title: How to Clip with an Axis-Aligned Clip Rectangle
description: Zeigt, wie ein Bereich mit einem achsenbündigen Cliprechteck abgeschnitten wird.
ms.assetid: 4196653a-9177-4a41-9db9-4738a41313aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f666bac88d93cb8ea0f27bfb9c2d5b14975e0dc8bb67aba4f0e767178f6ebddc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569314"
---
# <a name="how-to-clip-with-an-axis-aligned-clip-rectangle"></a>How to Clip with an Axis-Aligned Clip Rectangle

In diesem Thema wird beschrieben, wie ein Bild mit einem achsenbündigen Cliprechteck abgeschnitten wird. Dieser Ansatz erzeugt nur rechteckige Clips, da die Inhaltsgrenze an der Achse des Rechtecks ausgerichtet ist. Dieser Ansatz ist effizienter als die Verwendung von Ebenen mit den Inhaltsgrenze. Weitere Informationen finden Sie unter[Übersicht über Ebenen.](direct2d-layers-overview.md)

**So clipen Sie mit einem an der Achse ausgerichteten Cliprechteck**

1.  Laden Sie das ursprüngliche Image aus einer Ressource. Informationen zum Laden einer Bitmap finden Sie unter Laden einer [Bitmap aus einer Ressource.](how-to-load-a-bitmap-from-a-resource.md)
2.  Rufen [**Sie ID2D1RenderTarget::P ushAxisAlignedClip auf,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) um ein Rechteck anzugeben. Die Renderingbefehle werden am Rechteck abgeschnitten.

3.  Paint das ursprüngliche Image.
4.  Rufen [**Sie ID2D1RenderTarget::P opAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) auf, um den letzten an der Achse ausgerichteten Clip aus dem Renderziel zu entfernen.

In der folgenden Abbildung beträgt die ursprüngliche Bitmap auf der linken Seite beispielsweise 200 \* 130 Pixel. Die Bitmap auf der rechten Seite ist die ursprüngliche Bitmap, die auf das am Achsen ausgerichtete Cliprechteck abgeschnitten ist. Die Dimensionen sind (20, 20) bis (100, 100).

![Abbildung einer Goldfish-Bitmap vor und nach dem Clipping der Bitmap](images/cliparegion-axisalignedclip.png)

Um das abgeschnittene Bild zu erstellen, erstellen Sie eine Rechteckstruktur als Ausschneidebereich. Rufen [**Sie PushAxisAlignedClip mit**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) dem Clippingbereich auf, und zeichnen Sie das ursprüngliche Bild. Rufen [**Sie PopAxisAlignedClip auf,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) um den Clip aus dem Renderziel zu entfernen. Dies wird im folgenden Code veranschaulicht.


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

 

 