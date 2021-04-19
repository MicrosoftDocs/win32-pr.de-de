---
description: Textur Inhalte werden häufig im sRGB-Format gespeichert.
ms.assetid: d076140d-3e91-412a-b099-9baa52f8d7d8
title: Gamma (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cea4b3ba224452e1c3be8f96b7136f4e4f649c8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342716"
---
# <a name="gamma-direct3d-9"></a>Gamma (Direct3D 9)

Textur Inhalte werden häufig im sRGB-Format gespeichert. In der Vergangenheit haben Pixel Pipelines angenommen, dass die Farben linear sind, sodass Mischungs Vorgänge im linearen Raum durchgeführt wurden. Da der sRGB-Inhalt jedoch Gamma korrigiert ist, führen Mischungs Vorgänge im linearen Bereich zu falschen Ergebnissen. Mit Video Karten kann dieses Problem nun behoben werden, indem die Gammakorrektur rückgängig gemacht wird, wenn Sie sRGB-Inhalte lesen, und Pixeldaten beim Schreiben von Pixeln in das sRGB-Format zurück konvertiert werden. In diesem Fall werden alle Vorgänge innerhalb der Pixel Pipeline im linearen Bereich ausgeführt.

## <a name="gamma-correction"></a>Gamma-Korrektur

Direct3D 9 kann:

-   Geben Sie an, ob eine Textur von Gamma 2,2 korrigiert wurde (sRGB oder nicht). Der Treiber wird entweder in ein lineares Gamma für Mischungs Vorgänge bei SetTexture Time konvertiert, oder der Sampler konvertiert es zur Such Zeit in lineare Daten.
-   Geben Sie an, ob die Pixel Pipeline beim Schreiben in das Renderziel beim Schreiben in den sRGB-Raum ein Gamma korrigieren soll.

Es wird davon ausgegangen, dass sich alle anderen Farben (klar Farbe, Material Farbe, Scheitelpunkt Farbe usw.) im linearen Bereich befinden. Anwendungen können die in den Frame Puffer geschriebenen Farben mithilfe von pixelshaderanweisungen in Gamma korrigieren. Die Linearisierung sollte nur auf die RGB-Kanäle und nicht auf den Alphakanal angewendet werden.

Nicht alle Oberflächen Formate können linearisiert werden. Nur die Formate, die [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit D3DUSAGE \_ Query \_ srgbread bestehen, können linearisiert sein. Der samplerstatus D3DSAMP \_ srgbtexture wird für den Rest ignoriert. Diese Konvertierung wird nur von nicht signierten Textur Formaten unterstützt. Nicht signierte Textur Formate enthalten nur R-, G-, B-und L-Komponenten. Wenn der Alphakanal vorhanden ist, wird er ignoriert. Wenn gemischte Formate sRGB-Linearisierung unterstützen, sind nur die nicht signierten Kanäle betroffen. Im Idealfall sollte die-Hardware die Linearisierung vor dem Filtern ausführen, aber in Direct3D 9 ist es der Hardware gestattet, die Linearisierung nach dem Filtern auszuführen.

Nicht alle Oberflächen Formate können in sRGB-Speicherplatz geschrieben werden. Nur die Formate, die das [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit dem Usage-Flag D3DUSAGE \_ Query \_ srgbwrite bestehen, können linearisiert sein. Der "Rendering State D3DRS \_ srgbwrite teenable" wird für den Rest ignoriert. Es wird erwartet, dass 8 Bits pro Channel RGB-nicht signierte Formate diese Fähigkeit verfügbar machen.

Im Idealfall sollte die Hardware die Frame Puffer Mischungs Vorgänge im linearen Raum ausführen, aber die Hardware kann Sie nach dem Pixelshader, aber vor dem Frame Puffer Blender ausführen. Dies bedeutet, dass der Frame Puffer, der Vorgänge in sRGB-Speicherplatz durchführt, zu falschen Ergebnissen führt. D3DRS \_ srgbschreiteenable wird berücksichtigt, wenn das Renderziel eindeutig ist. Bei Hardware, die [mehrere Renderziele (Direct3D 9)](multiple-render-targets.md) oder [mehrere-Element-Texturen (Direct3D 9)](multiple-element-textures.md)unterstützt, wird nur das erste Renderziel oder-Element geschrieben.

### <a name="api-changes"></a>API-Änderungen


```
// New sampler state (DWORD)
// If this is nonzero, the texture is linearized on lookup.
D3DSAMP_SRGBTEXTURE       // Default FALSE

// New render state (DWORD)
D3DRS_SRGBWRITEENABLE     // Default FALSE

// New usage flags
D3DUSAGE_QUERY_SRGBWRITE
D3DUSAGE_QUERY_SRGBREAD
```



### <a name="windowed-swap-chains"></a>Fensteraustausch Ketten

Es ist hilfreich, wenn Anwendungen die Puffer der Austausch Ketten im linearen Raum aufbewahren, um korrekte Mischungs Vorgänge zu ermöglichen. Da sich der Desktop in der Regel nicht im linearen Raum befindet, ist eine Gammakorrektur erforderlich, bevor der Inhalt des Hintergrund Puffers dargestellt werden kann. Die Anwendung kann diese Korrektur selbst beeinflussen, indem Sie einen zusätzlichen Puffer zuordnet und eine eigene korrigierende Kopie aus dem linearen Puffer in den Hintergrund Puffer ausführt. Dies erfordert eine zusätzliche Kopie, die vermieden werden kann, wenn der Treiber eine Gammakorrektur als Teil der Präsentations-Blit ausführt.

In Direct3D 9 ist ein neues Flag [D3DPRESENT \_ linearer \_ Inhalt](d3dpresent.md)verfügbar, das es der Präsentation [**ermöglicht, eine**](/windows/desktop/api) implizite Konvertierung von linearem Raum in sRGB/Gamma 2,2 durchzusetzen. Anwendungen sollten dieses Flag angeben, wenn es sich bei dem backpufferformat um einen 16-Bit-Gleit Komma Wert handelt, um den für das Vollbild-Gamma Verhalten vorhandenen Fenster-Modus abzugleichen \_ \_ \_ \_ [](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Frame Puffer](frame-buffer.md)
</dt> </dl>

 

 
