---
description: Arbeiten mit Direct3D-Renderzielen
ms.assetid: 271b919c-421b-4484-8e60-afbf3cbdca44
title: Arbeiten mit Direct3D-Renderzielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f7bacf36402b071d60989e225cdcd9533500494a0593bcf9753ddc06bb93ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650340"
---
# <a name="working-with-direct3d-render-targets"></a>Arbeiten mit Direct3D-Renderzielen

Mehrere Medienuntertypen für Direct3D-Renderziele sind für die Verwendung mit VMR-7 und VMR-9 definiert. Wenn ein Upstreamfilter eine Verbindung mit einem dieser Untertypen vorschlägt, zeigt er dem VMR an, dass das Rendering auf einem Direct3D-Renderziel ausgeführt werden soll. Für VMR-7 ist dies ein DirectX 7 Direct3D-Renderziel, und für VMR-9 ist dies ein DirectX 9 Direct3D-Renderziel. Wenn sich die VMR im Mischungsmodus befindet, ist die Oberfläche auch eine Direct3D-Texturoberfläche. Wenn sich die VMR nicht im Gemischtmodus befindet, ist die Oberfläche eine reguläre Direct3D-Oberfläche. Die ARGB-Pixelformate werden nur unterstützt, wenn sich die VMR im Gemischtmodus befindet. Die Renderzieluntertypen sind:



| VMR-7                                | VMR-9                                |
|--------------------------------------|--------------------------------------|
| MEDIASUBTYPE \_ RGB32 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ RGB32 \_ D3D \_ DX9 \_ RT    |
| MEDIASUBTYPE \_ RGB16 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ RGB16 \_ D3D \_ DX9 \_ RT    |
| MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX7 \_ RT   | MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX9 \_ RT   |
| MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ DX9 \_ RT |
| MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX9 \_ RT |



 

Diese Typen werden in der Headerdatei uuids.h definiert. Die MEDIASUBTYPE RGB32-Medientypen sind ein \_ RGBx888-Format, und MEDIASUBTYPE RGB16-Medientypen sind \_ ein RGB565-Format. Weitere Informationen zu diesen Pixelformaten finden Sie in der DirectX-Grafikdokumentation.

**Anfordern einer entsperrten Oberfläche**

Das Sperren und Entsperren von DirectDraw-Oberflächen ist rechenintensive Vorgänge. Bei Verwendung der Direct3D-Renderzielmedien-Untertypen muss der Upstreamfilter die Oberflächen entsperren, damit er mit der Grafikhardware darauf zugreifen kann. Um einen unnötigen Sperr-/Entsperrvorgang zu vermeiden, unterstützt der VMR ein neues Flag für die [**IMemAllocator::GetBuffer-Methode**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) AM \_ GBF NODDSURFACELOCK, das den VMR anweisen soll, die DirectDraw-Oberfläche nicht zu sperren, bevor ein Beispiel an den Upstreamfilter übergeben \_ wird. Wenn dieses Flag verwendet wird, können Aufrufe von [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) nicht ausgeführt werden, da kein gesperrter Zeiger vorkommt. Um Zugriff auf die DirectDraw-Oberfläche zu erhalten, muss der Filter **QueryInterface** für das zurückgegebene [**IMediaSample-Objekt**](/windows/desktop/api/Strmif/nn-strmif-imediasample) aufrufen und die [**IVMRSurface-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) anfordern. Natürlich muss der Upstreamfilter sicherstellen, dass die Oberfläche nicht gesperrt ist, wenn das Beispiel wieder in die Freie Liste aufgenommen wird.

 

 



