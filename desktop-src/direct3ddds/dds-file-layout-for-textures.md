---
title: Beispiel für DDS-Textur
description: Verwenden Sie für eine nicht komprimierte Textur die ddsd \_ -und ddpf- \_ RGB-Flags. verwenden Sie für eine komprimierte Textur die ddsd \_ -Informationen linearsize und ddpf \_ FourCC.
ms.assetid: 5bf54e8d-1dc5-4782-96c1-132d258fb560
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbaa6f86dddc7e60d7f41fc34d7c9fe994d50e4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342278"
---
# <a name="dds-texture-example"></a>Beispiel für DDS-Textur

Verwenden Sie für eine nicht komprimierte Textur die ddsd \_ -und ddpf- \_ RGB-Flags. verwenden Sie für eine komprimierte Textur die ddsd \_ -Informationen linearsize und ddpf \_ FourCC. Verwenden Sie für eine mipzugeordnete Textur die \_ komplexen Flags ddsd mipmapcount, DDSCAPS \_ MIPMAP und DDSCAPS sowie \_ das Element MIPMAP count. Wenn Mipmaps generiert werden, werden alle Ebenen, die bis zu 1 bis 1 liegen, in der Regel geschrieben.

Bei einer komprimierten Textur ist die Größe jedes Bilds auf MipMap-Ebene in der Regel eine vierte der Größe des vorherigen Bilds, mit mindestens 8 (DXT1) oder 16 (DXT2-5) Bytes (für quadratische Texturen). Verwenden Sie die folgende Formel, um die Größe der einzelnen Ebenen für eine nicht quadratische Textur zu berechnen:


```
max(1, ( (width + 3) / 4 ) ) x max(1, ( (height + 3) / 4 ) ) x 8(DXT1) or 16(DXT2-5)
```



In dieser Tabelle wird der von jeder Schicht benötigte Speicherplatz für eine 256-by-256 R8G8B8-Textur ohne Komprimierung aufgelistet.



| DDS-Komponenten          | \# Satz |
|-------------------------|----------|
| header                  | 128      |
| 256-bis 256-Haupt Abbild   | 196608   |
| 128-nach-128-MipMap-Bild | 49152    |
| 64-nach-64-MipMap-Bild   | 12288    |
| 32-nach-32-MipMap-Bild   | 3072     |
| 16-by-16-MipMap-Bild   | 768      |
| 8-bis-8-MipMap-Bild     | 192      |
| 4 x 4-MipMap-Bild     | 48       |
| Bild von 2 x 2 MipMap     | 12       |
| 1:1-MipMap-Bild     | 3        |



 

In dieser Tabelle wird der von jeder Ebene benötigte Speicherplatz für die gleiche Textur mithilfe von Komprimierung (DXT1) aufgelistet.



| DDS-Komponenten         | \# Satz |
|------------------------|----------|
| header                 | 128      |
| 256-bis 64-Haupt Abbild   | 8192     |
| 128-nach-32-MipMap-Bild | 2048     |
| 64-x-16-MipMap-Bild  | 512      |
| 32-x-8-MipMap-Bild   | 128      |
| 16-x-4-MipMap-Bild   | 32       |
| 8-x-2-MipMap-Bild    | 16       |
| 4-x-1-MipMap-Bild    | 8        |
| 2:1 MipMap-Bild    | 8        |
| 1:1-MipMap-Bild    | 8        |



 

In dieser Tabelle wird der von jeder Ebene benötigte Speicherplatz für die gleiche Textur mit einem DXGI-Komprimierungs Format (in diesem Fall BC3 \_ unorm) aufgelistet, das daher den erweiterten Header erfordert:



| DDS-Komponenten                                                | \# Satz |
|---------------------------------------------------------------|----------|
| Header (FourCC ist auf "DX10" festgelegt)                                 | 128      |
| Extended-Header (DXGI-Format ist auf DXGI-Format festgelegt \_ \_ BC3 \_ unorm) | 20       |
| 256-bis 64-Haupt Abbild                                          | 16384    |
| 128-nach-32-MipMap-Bild                                        | 4096     |
| 64-x-16-MipMap-Bild                                         | 1024     |
| 32-x-8-MipMap-Bild                                          | 256      |
| 16-x-4-MipMap-Bild                                          | 64       |
| 8-x-2-MipMap-Bild                                           | 32       |
| 4-x-1-MipMap-Bild                                           | 16       |
| 2:1 MipMap-Bild                                           | 16       |
| 1:1-MipMap-Bild                                           | 16       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmier Handbuch für DDS](dx-graphics-dds-pguide.md)
</dt> </dl>

 

 




