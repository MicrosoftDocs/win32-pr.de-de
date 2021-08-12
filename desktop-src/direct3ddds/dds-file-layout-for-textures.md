---
title: DDS-Texturbeispiel
description: Verwenden Sie für eine unkomprimierte Textur die DDSD \_ PITCH- und DDPF \_ RGB-Flags. Verwenden Sie für eine komprimierte Textur die Flags DDSD \_ LINEARSIZE und DDPF \_ FOURCC.
ms.assetid: 5bf54e8d-1dc5-4782-96c1-132d258fb560
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47fe1d7da71727c2c84bb3745772a10520367ac1cf6e9c4033932548d86c1302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289797"
---
# <a name="dds-texture-example"></a>DDS-Texturbeispiel

Verwenden Sie für eine unkomprimierte Textur die DDSD \_ PITCH- und DDPF \_ RGB-Flags. Verwenden Sie für eine komprimierte Textur die Flags DDSD \_ LINEARSIZE und DDPF \_ FOURCC. Verwenden Sie für eine mipmapped-Textur die Flags DDSD \_ MIPMAPCOUNT, DDSCAPS \_ MIPMAP und DDSCAPS \_ COMPLEX sowie den Member mipmap count. Wenn Mipmaps generiert werden, werden in der Regel alle Ebenen bis 1 x 1 geschrieben.

Bei einer komprimierten Textur beträgt die Größe jedes Bilds auf Mipmapebene in der Regel ein Viertel der Größe des vorherigen Bilds mit mindestens 8 (DXT1) oder 16 (DXT2-5) Bytes (für quadratische Texturen). Verwenden Sie die folgende Formel, um die Größe jeder Ebene für eine nicht quadratische Textur zu berechnen:


```
max(1, ( (width + 3) / 4 ) ) x max(1, ( (height + 3) / 4 ) ) x 8(DXT1) or 16(DXT2-5)
```



In dieser Tabelle wird die Menge des Speicherplatzes aufgeführt, der von jeder Ebene für eine Textur von 256 X 256 R8G8B8 ohne Komprimierung verwendet wird.



| DDS-Komponenten          | \# Bytes |
|-------------------------|----------|
| header                  | 128      |
| 256-by-256-Hauptbild   | 196608   |
| 128 by-128 mipmap-Bild | 49152    |
| 64-by-64-mipmap-Bild   | 12288    |
| 32-by-32-mipmap-Bild   | 3072     |
| 16-by-16-mipmap-Bild   | 768      |
| 8-by-8-Mipmap-Bild     | 192      |
| 4-by-4-Mipmap-Bild     | 48       |
| 2-by-2-Mipmap-Bild     | 12       |
| 1-by-1-Mipmap-Bild     | 3        |



 

In dieser Tabelle wird die Menge des Speicherplatzes aufgeführt, der von jeder Ebene für dieselbe Textur mithilfe der Komprimierung (DXT1) genutzt wird.



| DDS-Komponenten         | \# Bytes |
|------------------------|----------|
| header                 | 128      |
| 256 by-64-Hauptbild   | 8192     |
| 128 by-32 mipmap-Bild | 2048     |
| 64-by-16 mipmap-Bild  | 512      |
| 32-by-8-Mipmap-Bild   | 128      |
| 16-by-4-Mipmap-Bild   | 32       |
| 8-by-2-Mipmap-Bild    | 16       |
| 4-by-1-Mipmap-Bild    | 8        |
| 2-by-1-Mipmap-Bild    | 8        |
| 1-by-1-Mipmap-Bild    | 8        |



 

In dieser Tabelle wird die Menge des Speicherplatzes aufgeführt, der von jeder Ebene für dieselbe Textur mithilfe eines DXGI-Komprimierungsformats (in diesem Fall BC3 UNORM) benötigt wird \_ und daher den erweiterten Header erfordert:



| DDS-Komponenten                                                | \# Bytes |
|---------------------------------------------------------------|----------|
| header (FourCC auf "DX10" festgelegt)                                 | 128      |
| erweiterter Header (DXGI-Format auf DXGI \_ FORMAT \_ BC3 \_ UNORM festgelegt) | 20       |
| 256 by-64-Hauptbild                                          | 16384    |
| 128 by-32 mipmap-Bild                                        | 4096     |
| 64-by-16 mipmap-Bild                                         | 1024     |
| 32-by-8-Mipmap-Bild                                          | 256      |
| 16-by-4-Mipmap-Bild                                          | 64       |
| 8-by-2-Mipmap-Bild                                           | 32       |
| 4-by-1-Mipmap-Bild                                           | 16       |
| 2-by-1-Mipmap-Bild                                           | 16       |
| 1-by-1-Mipmap-Bild                                           | 16       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch für DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




