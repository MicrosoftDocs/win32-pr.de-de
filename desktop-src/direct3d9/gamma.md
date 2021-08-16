---
description: Texturinhalte werden häufig im sRGB-Format gespeichert.
ms.assetid: d076140d-3e91-412a-b099-9baa52f8d7d8
title: Gamma (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ede077347d67c1657b86ad09b778625e22fd19a39c8333d7f11fec51be53b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523023"
---
# <a name="gamma-direct3d-9"></a>Gamma (Direct3D 9)

Texturinhalte werden häufig im sRGB-Format gespeichert. In der Regel wurde bei Pixelpipelines davon ausgegangen, dass die Farben linear sind, sodass Blendingvorgänge im linearen Raum durchgeführt wurden. Da jedoch der SRGB-Inhalt korrigiert wird, führt das Mischen von Vorgängen im linearen Raum zu falschen Ergebnissen. Grafikkarten können dieses Problem jetzt beheben, indem sie die Gammakorrektur rückgängig machen, wenn sie SRGB-Inhalte lesen, und Pixeldaten beim Schreiben von Pixeln wieder in das sRGB-Format konvertieren. In diesem Fall werden alle Vorgänge innerhalb der Pixelpipeline im linearen Raum ausgeführt.

## <a name="gamma-correction"></a>Gamma-Korrektur

Direct3D 9 kann:

-   Geben Sie an, ob eine Textur gamma 2.2 korrigiert wurde oder nicht (sRGB oder nicht). Der Treiber konvertiert entweder in ein lineares Gamma für Blendingvorgänge zur SetTexture-Zeit, oder der Sampler konvertiert ihn zur Suchzeit in lineare Daten.
-   Geben Sie an, ob die Pixelpipeline beim Schreiben in das Renderziel eine Gammakorrektur in den SRGB-Bereich durchführen soll.

Alle anderen Farben (klare Farbe, Materialfarbe, Scheitelpunktfarbe usw.) werden im linearen Raum angenommen. Anwendungen können die in den Framepuffer geschriebenen Farben mithilfe von Pixelshaderanweisungen per Gamma korrigieren. Die Linearisierung sollte nur auf die RGB-Kanäle und nicht auf den Alphakanal angewendet werden.

Nicht alle Oberflächenformate können linearisiert werden. Nur die Formate, die [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit D3DUSAGE QUERY SRGBREAD übergeben, \_ können \_ linearisiert werden. Der Samplerzustand D3DSAMP \_ SRGBTEXTURE wird für den Rest ignoriert. Es wird erwartet, dass nur unsignierte Texturformate diese Konvertierung unterstützen. Nicht signierte Texturformate enthalten nur R-, G-, B- und L-Komponenten. Wenn der Alphakanal vorhanden ist, wird er ignoriert. Wenn gemischte Formate die SRGB-Linearisierung unterstützen, sind nur die nicht signierten Kanäle betroffen. Im Idealfall sollte die Hardware die Linearisierung vor dem Filtern durchführen, aber in Direct3D 9 kann Hardware die Linearisierung nach dem Filtern durchführen.

Nicht alle Oberflächenformate können im SRGB-Bereich geschrieben werden. Nur die Formate, die [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) mit dem Verwendungsflag D3DUSAGE \_ QUERY \_ SRGBWRITE übergeben, können linearisiert werden. Der Renderzustand D3DRS \_ SRGBWRITEENABLE wird für den Rest ignoriert. Es wird erwartet, dass acht RGB-Formate ohne Vorzeichen pro Kanal diese Fähigkeit verfügbar machen.

Im Idealfall sollte die Hardware die Framepuffermischungsvorgänge im linearen Raum ausführen, aber Hardware darf sie nach dem Pixelshader, aber vor dem Framepufferblender ausführen. Dies bedeutet, dass die Framepuffermischungsvorgänge, die im SRGB-Bereich stattfinden, zu falschen Ergebnissen führen. D3DRS \_ SRGBWRITEENABLE wird beim Löschen des Renderziels berücksichtigt. Für Hardware, die [Mehrere Renderziele (Direct3D 9)](multiple-render-targets.md) oder Texturen mit [mehreren Elementen (Direct3D 9)](multiple-element-textures.md)unterstützt, wird nur das erste Renderziel oder -element geschrieben.

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



### <a name="windowed-swap-chains"></a>Vertauschungsketten mit Fenstern

Es ist für Anwendungen nützlich, die Hintergrundpuffer ihrer Swapketten im linearen Raum zu halten, um korrekte Mischungsvorgänge zu ermöglichen. Da sich der Desktop in der Regel nicht im linearen Raum befindet, ist eine Gammakorrektur erforderlich, bevor der Inhalt des Hintergrundpuffers angezeigt werden kann. Die Anwendung kann diese Korrektur selbst bewirken, indem sie einen zusätzlichen Puffer zuweise und eine eigene korrigierende Kopie aus dem linearen Puffer in den Hintergrundpuffer ausführt. Dies erfordert eine zusätzliche Kopie, die vermieden werden kann, wenn der Treiber im Rahmen der Präsentations-Blit eine Gammakorrektur durchführt.

In Direct3D 9 ist ein neues Flag, [D3DPRESENT \_ LINEAR \_ CONTENT,](d3dpresent.md)für [**Present**](/windows/desktop/api) verfügbar, mit dem die Darstellung implizit aus dem linearen Raum in sRGB/gamma 2.2 konvertiert werden kann. Anwendungen sollten dieses Flag angeben, wenn das Backbufferformat 16-Bit-Gleitkomma ist, um den fensterbasierten Modus abzugleichen, der dem Gammaverhalten des Vollbildmodus entspricht, sofern D3DCAPS3 \_ LINEAR \_ TO \_ SRGB PRESENTATION für \_ Gerätefunktionen zurückgegeben wird, die über [**GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps)abgerufen werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Framepuffer](frame-buffer.md)
</dt> </dl>

 

 
