---
description: Obwohl die Begriffe Breite und Tonhöhe häufig informell verwendet werden, haben Sie eine sehr wichtige und deutlich unterschiedliche Bedeutungen. Daher sollten Sie die Bedeutungen der einzelnen Elemente verstehen und die Werte interpretieren, die von Direct3D verwendet werden, um Sie zu beschreiben.
ms.assetid: 2f99881b-f95d-470f-b14d-8300ad930e2a
title: Breite und Tonhöhe (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50d0c8fc49b3bce984e56f7b1a727ed40fee67b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104562739"
---
# <a name="width-vs-pitch-direct3d-9"></a>Breite und Tonhöhe (Direct3D 9)

Obwohl die Begriffe Breite und Tonhöhe häufig informell verwendet werden, haben Sie eine sehr wichtige und deutlich unterschiedliche Bedeutungen. Daher sollten Sie die Bedeutungen der einzelnen Elemente verstehen und die Werte interpretieren, die von Direct3D verwendet werden, um Sie zu beschreiben.

Direct3D verwendet die [**D3DSURFACE \_ DESC**](d3dsurface-desc.md) -Struktur zum Übertragen von Informationen, die eine Oberfläche beschreiben. Diese Struktur wird unter anderem so definiert, dass Sie Informationen über die Dimensionen einer Oberfläche und die Darstellung der Dimensionen im Arbeitsspeicher enthält. Die-Struktur verwendet die Height-und Width-Member, um die logischen Dimensionen der-Oberfläche zu beschreiben. Beide Elemente werden in Pixel gemessen. Daher sind die Höhen-und Breitenwerte für eine 640 x 480-Oberfläche identisch, unabhängig davon, ob es sich um eine 8-Bit-Oberfläche oder eine 24-Bit-RGB-Fläche handelt.

Wenn Sie eine Oberfläche mithilfe der [**IDirect3DSurface9:: lockrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) -Methode sperren, füllt die Methode eine [**D3DLOCKED \_ Rect**](d3dlocked-rect.md) -Struktur aus, die die Oberfläche der Oberfläche und einen Zeiger auf die gesperrten Bits enthält. Der Wert im "Pitch"-Member beschreibt die speicherfläche der Oberfläche, auch als "stride" bezeichnet. "Pitch" ist der Abstand zwischen zwei Speicheradressen (in Bytes), die den Anfang einer bitmaplinie darstellen, und dem Anfang der nächsten Bitmap-Linie. Da die-Tonhöhe in Bytes und nicht in Pixel gemessen wird, hat eine 640 x480x8-Oberfläche einen sehr anderen Wert als eine Oberfläche mit denselben Dimensionen, aber einem anderen Pixel Format. Außerdem spiegelt der Wert für die Festsetzung manchmal Bytes wider, die Direct3D als Cache reserviert hat, sodass es nicht sicher geht, dass die Tonhöhe nur die Breite multipliziert mit der Anzahl der Bytes pro Pixel ist. Visualisieren Sie stattdessen den Unterschied zwischen Breite und Tonhöhe, wie in der folgenden Abbildung dargestellt.

![Diagramm der Tonhöhe und Breite für denselben Vorder-und Hintergrund Puffer sowie den Cache](images/pitch.png)

In diesem Diagramm sind der Vorder-und Hintergrund Puffer 640 x480x8, und der Cache ist 384x480x8.

Wenn Sie direkt auf die Oberflächen zugreifen, achten Sie darauf, dass der für die Dimensionen der Oberfläche zugeordnete Arbeitsspeicher beibehalten wird und dass der für den Cache reservierte Arbeitsspeicher verbleibt Wenn Sie darüber hinaus nur einen Teil einer Oberfläche sperren, müssen Sie in dem Rechteck bleiben, das Sie beim Sperren der Oberfläche angeben. Wenn diese Richtlinien nicht befolgt werden, treten unvorhersehbare Ergebnisse auf. Wenn Sie direkt in den Surface-Speicher rendern, verwenden Sie immer die von der [**IDirect3DSurface9:: lockrect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) -Methode zurückgegebene Tonhöhe. Gehen Sie nicht davon aus, dass eine auf dem Anzeigemodus basierende Tonhöhe allein ist. Wenn Ihre Anwendung auf einigen Anzeige Adaptern funktioniert, aber auf anderen angezeigt wird, ist dies möglicherweise die Ursache des Problems.

Weitere Informationen finden Sie unter Direktes [zugreifen auf den Surface-Speicher (Direct3D 9)](accessing-surface-memory-directly.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> </dl>

 

 
