---
description: Arbeiten mit Direct3D-Renderingzielen
ms.assetid: 271b919c-421b-4484-8e60-afbf3cbdca44
title: Arbeiten mit Direct3D-Renderingzielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8aca19082c5db9521cfc1c7341fd74c98270cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372911"
---
# <a name="working-with-direct3d-render-targets"></a>Arbeiten mit Direct3D-Renderingzielen

Mehrere Medien Untertypen für Direct3D-Renderziele sind für die Verwendung mit VMR-7 und VMR-9 definiert. Wenn ein upstreamfilter eine Verbindung mit einem dieser Untertypen vorschlägt, weist er dem VMR an, dass das Rendering für ein Direct3D-Renderziel ausgeführt werden soll. Bei VMR-7 handelt es sich hierbei um ein DirectX 7 Direct3D Renderziel, und für VMR-9 ist dies ein DirectX 9 Direct3D-Renderziel. Wenn sich der VMR im Mischungs Modus befindet, ist die Oberfläche auch eine Direct3D-Textur Oberfläche. Wenn VMR sich nicht im Mischungs Modus befindet, ist die Oberfläche eine reguläre Direct3D-Oberfläche. Die ARGB-Pixel Formate werden nur unterstützt, wenn sich der VMR im Mischungs Modus befindet. Die Untertypen des Renderziels sind:



| VMR-7                                | VMR-9                                |
|--------------------------------------|--------------------------------------|
| Mediasubtype \_ RGB32 \_ D3D \_ DX7 \_ RT    | Mediasubtype \_ RGB32 \_ D3D \_ DX9 \_ RT    |
| Mediasubtype \_ RGB16 \_ D3D \_ DX7 \_ RT    | Mediasubtype \_ RGB16 \_ D3D \_ DX9 \_ RT    |
| Mediasubtype \_ ARGB32 \_ D3D \_ DX7 \_ RT   | Mediasubtype \_ ARGB32 \_ D3D \_ DX9 \_ RT   |
| Mediasubtype \_ ARGB4444 \_ D3D \_ DX7 \_ RT | Mediasubtype \_ ARGB4444 \_ D3D \_ DX9 \_ RT |
| Mediasubtype \_ ARGB1555 \_ D3D \_ DX7 \_ RT | Mediasubtype \_ ARGB1555 \_ D3D \_ DX9 \_ RT |



 

Diese Typen sind in der Header Datei "UUIDs. h" definiert. Die mediasubtype \_ RGB32-Medientypen sind ein RGBx888-Format, und mediasubtype \_ RGB16-Medientypen sind ein RGB565-Format. Weitere Informationen zu diesen Pixel Formaten finden Sie in der Dokumentation zu DirectX-Grafiken.

**Anfordern einer entsperrter Oberfläche**

Das Sperren und Entsperren von DirectDraw-Oberflächen ist rechenintensive Vorgänge. Bei Verwendung der Direct3D Renderziel Medien-Untertypen benötigt der upstreamfilter, dass die Oberflächen entsperrt werden, damit Sie mit der Grafikhardware betrieben werden können. Um einen unnötigen Sperr Vorgang zu vermeiden, unterstützt VMR ein neues Flag für die [**imemzuzucator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) -Methode, am \_ GBF \_ noddsurfacelock, das den VMR anweist, die DirectDraw-Oberfläche nicht zu sperren, bevor eine Stichprobe an den upstreamfilter übergeben wird. Wenn dieses Flag verwendet wird, schlagen Aufrufe von [**imediasample:: getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) fehl, da kein gesperrter Zeiger vorhanden ist. Um Zugriff auf die DirectDraw-Oberfläche zu erhalten, muss der Filter **QueryInterface** für das zurückgegebene [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Objekt aufrufen und die [**ivmrsurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) -Schnittstelle anfordern. Natürlich muss der Upstream-Filter sicherstellen, dass die Oberfläche nicht gesperrt ist, wenn Sie das Beispiel wieder in der freien Liste wieder gibt.

 

 



