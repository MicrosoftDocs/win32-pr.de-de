---
description: Obwohl die Begriffe Breite und Tonhöhe häufig informell verwendet werden, haben sie sehr wichtige und deutlich unterschiedliche Bedeutungen. Daher sollten Sie die Bedeutungen der einzelnen Werte verstehen und die Werte interpretieren, die Direct3D verwendet, um sie zu beschreiben.
ms.assetid: 2f99881b-f95d-470f-b14d-8300ad930e2a
title: Breite und Tonhöhe (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1c697ec4c9278a78a5539818b30038d99fc9d59d96af7f22ee87c33949abf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095514"
---
# <a name="width-vs-pitch-direct3d-9"></a>Breite und Tonhöhe (Direct3D 9)

Obwohl die Begriffe Breite und Tonhöhe häufig informell verwendet werden, haben sie sehr wichtige und deutlich unterschiedliche Bedeutungen. Daher sollten Sie die Bedeutungen der einzelnen Werte verstehen und die Werte interpretieren, die Direct3D verwendet, um sie zu beschreiben.

Direct3D verwendet die [**D3DSURFACE \_ DESC-Struktur,**](d3dsurface-desc.md) um Informationen zu enthalten, die eine Oberfläche beschreiben. Diese Struktur ist unter anderem so definiert, dass sie Informationen über die Dimensionen einer Oberfläche sowie darüber enthält, wie diese Dimensionen im Arbeitsspeicher dargestellt werden. Die -Struktur verwendet die Height- und Width-Elemente, um die logischen Dimensionen der Oberfläche zu beschreiben. Beide Elemente werden in Pixel gemessen. Daher sind die Werte für Höhe und Breite für eine 640 x 480-Oberfläche gleich, unabhängig davon, ob es sich um eine 8-Bit-Oberfläche oder eine 24-Bit-RGB-Oberfläche handelt.

Wenn Sie eine Oberfläche mit der [**IDirect3DSurface9::LockRect-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) sperren, füllt die Methode eine [**D3DLOCKED \_ RECT-Struktur**](d3dlocked-rect.md) aus, die die Tonhöhe der Oberfläche und einen Zeiger auf die gesperrten Bits enthält. Der Wert im Pitch-Member beschreibt die Speicherhöhe der Oberfläche, die auch als Stride bezeichnet wird. Tonhöhe ist der Abstand zwischen zwei Speicheradressen in Bytes, die den Anfang einer Bitmaplinie und den Anfang der nächsten Bitmaplinie darstellen. Da die Tonhöhe nicht in Pixel, sondern in Bytes gemessen wird, hat eine 640 x 480 x 8-Oberfläche einen sehr anderen Tonhöhenwert als eine Oberfläche mit den gleichen Dimensionen, aber einem anderen Pixelformat. Darüber hinaus spiegelt der Tonhöhenwert manchmal Bytes wider, die Direct3D als Cache reserviert hat. Daher kann nicht davon ausgegangen werden, dass die Tonhöhe nur die Breite multipliziert mit der Anzahl der Bytes pro Pixel ist. Visualisieren Sie stattdessen den Unterschied zwischen Breite und Tonhöhe, wie im folgenden Diagramm dargestellt.

![Diagramm der Tonhöhe und Breite für den gleichen Frontpuffer, Denkpuffer und Cache](images/pitch.png)

In diesem Diagramm sind front buffer und back buffer jeweils 640x480x8, und der Cache ist 384x480x8.

Achten Sie beim direkten Zugriff auf Oberflächen darauf, innerhalb des Arbeitsspeichers zu bleiben, der für die Dimensionen der Oberfläche zugeordnet ist, und lassen Sie den für den Cache reservierten Arbeitsspeicher aus. Wenn Sie nur einen Teil einer Oberfläche sperren, müssen Sie außerdem innerhalb des Rechtecks bleiben, das Sie beim Sperren der Oberfläche angeben. Wenn diese Richtlinien nicht befolgt werden, kann dies zu unvorhersehbaren Ergebnissen führen. Verwenden Sie beim direkten Rendern in den Oberflächenspeicher immer die Von der [**IDirect3DSurface9::LockRect-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-lockrect) zurückgegebene Tonhöhe. Gehen Sie nicht von einer Tonhöhe aus, die ausschließlich auf dem Anzeigemodus basiert. Wenn Ihre Anwendung auf einigen Anzeigeadaptern funktioniert, aber auf anderen bildschirmend aussieht, kann dies die Ursache des Problems sein.

Weitere Informationen finden Sie unter [Direktes Zugreifen auf Surface Memory (Direct3D 9).](accessing-surface-memory-directly.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Oberflächen](direct3d-surfaces.md)
</dt> </dl>

 

 
