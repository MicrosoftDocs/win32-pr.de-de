---
description: Die folgenden Konstanten, die in Gdipluspixelformats.h definiert sind, geben verschiedene Pixelformate an, die in Bitmaps verwendet werden.
ms.assetid: 362204c5-5dd7-461a-b90b-15826c025689
title: Bildpixelformatkonstanten (Gdipluspixelformats.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38465f02f2dc79b8bbbfc5b04596327b823c4b97132e1cb80685950634b7fe01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117696438"
---
# <a name="image-pixel-format-constants"></a>Bildpixelformatkonstanten

Die folgenden Konstanten, die in Gdipluspixelformats.h definiert sind, geben verschiedene Pixelformate an, die in Bitmaps verwendet werden.



| Konstante                                                                                                                                                                                                                                     | Beschreibung                                                                                                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PixelFormat1bppIndexed"></span><span id="pixelformat1bppindexed"></span><span id="PIXELFORMAT1BPPINDEXED"></span><dl> <dt>**PixelFormat1bppIndexed**</dt> </dl>             | Gibt an, dass das Format 1 Bit pro Pixel indiziert ist.<br/>                                                                                                                                                         |
| <span id="PixelFormat4bppIndexed"></span><span id="pixelformat4bppindexed"></span><span id="PIXELFORMAT4BPPINDEXED"></span><dl> <dt>**PixelFormat4bppIndexed**</dt> </dl>             | Gibt an, dass das Format 4 Bits pro Pixel ist und indizierte Farben verwendet werden.<br/>                                                                                                                                                        |
| <span id="PixelFormat8bppIndexed"></span><span id="pixelformat8bppindexed"></span><span id="PIXELFORMAT8BPPINDEXED"></span><dl> <dt>**PixelFormat8bppIndexed**</dt> </dl>             | Gibt an, dass das indizierte Format 8 Bits pro Pixel ist.<br/>                                                                                                                                                        |
| <span id="PixelFormat16bppARGB1555"></span><span id="pixelformat16bppargb1555"></span><span id="PIXELFORMAT16BPPARGB1555"></span><dl> <dt>**PixelFormat16bppARGB1555**</dt> </dl>     | Gibt an, dass das Format 16 Bits pro Pixel beträgt. 1 Bit wird für die Alphakomponente verwendet, und 5 Bits werden jeweils für die roten, grünen und blauen Komponenten verwendet.<br/>                                                       |
| <span id="PixelFormat16bppGrayScale"></span><span id="pixelformat16bppgrayscale"></span><span id="PIXELFORMAT16BPPGRAYSCALE"></span><dl> <dt>**PixelFormat16bppGrayScale**</dt> </dl> | Gibt an, dass das Format 16 Bits pro Pixel und Graustufen beträgt.<br/>                                                                                                                                                     |
| <span id="PixelFormat16bppRGB555"></span><span id="pixelformat16bpprgb555"></span><span id="PIXELFORMAT16BPPRGB555"></span><dl> <dt>**PixelFormat16bppRGB555**</dt> </dl>             | Gibt an, dass das Format 16 Bits pro Pixel ist, wobei für den Rot-, Grün- und Blauanteil jeweils 5 Bits verwendet werden. Das verbleibende Bit wird nicht verwendet.<br/>                                                                   |
| <span id="PixelFormat16bppRGB565"></span><span id="pixelformat16bpprgb565"></span><span id="PIXELFORMAT16BPPRGB565"></span><dl> <dt>**PixelFormat16bppRGB565**</dt> </dl>             | Gibt an, dass das Format 16 Bits pro Pixel ist, wobei für den Rot- und Blauanteil jeweils 5 Bits und für den Grünanteil 6 Bits verwendet werden.<br/>                                    |
| <span id="PixelFormat24bppRGB"></span><span id="pixelformat24bpprgb"></span><span id="PIXELFORMAT24BPPRGB"></span><dl> <dt>**PixelFormat24bppRGB**</dt> </dl>                         | Gibt an, dass das Format 24 Bit pro Pixel ist, wobei jeweils 8 Bits für die rote, grüne und die blaue Komponente verwendet werden.<br/>                                                                                                  |
| <span id="PixelFormat32bppARGB"></span><span id="pixelformat32bppargb"></span><span id="PIXELFORMAT32BPPARGB"></span><dl> <dt>**PixelFormat32bppARGB**</dt> </dl>                     | Gibt an, dass das Format 32 Bits pro Pixel ist, wobei für den Alpha-, Rot-, Grün- und Blauanteil jeweils 8 Bits verwendet werden.<br/>                                                                                           |
| <span id="PixelFormat32bppPARGB"></span><span id="pixelformat32bpppargb"></span><span id="PIXELFORMAT32BPPPARGB"></span><dl> <dt>**PixelFormat32bppPARGB**</dt> </dl>                 | Gibt an, dass das Format 32 Bits pro Pixel ist, wobei für den Alpha-, Rot-, Grün- und Blauanteil jeweils 8 Bits verwendet werden. Die Rot-, Grün- und Blaukomponente wird entsprechend der Alphakomponente im Voraus multipliziert.<br/>   |
| <span id="PixelFormat32bppRGB"></span><span id="pixelformat32bpprgb"></span><span id="PIXELFORMAT32BPPRGB"></span><dl> <dt>**PixelFormat32bppRGB**</dt> </dl>                         | Gibt an, dass das Format 32 Bit pro Pixel ist, wobei jeweils 8 Bit für die rote, grüne und die blaue Komponente verwendet werden. Die verbleibendenden 8 Bits werden nicht verwendet.<br/>                                                               |
| <span id="PixelFormat48bppRGB"></span><span id="pixelformat48bpprgb"></span><span id="PIXELFORMAT48BPPRGB"></span><dl> <dt>**PixelFormat48bppRGB**</dt> </dl>                         | Gibt an, dass das Format 48 Bit pro Pixel ist, wobei jeweils 16 Bit für die rote, grüne und die blaue Komponente verwendet werden.<br/>                                                                                                 |
| <span id="PixelFormat64bppARGB"></span><span id="pixelformat64bppargb"></span><span id="PIXELFORMAT64BPPARGB"></span><dl> <dt>**PixelFormat64bppARGB**</dt> </dl>                     | Gibt an, dass das Format 64 Bit pro Pixel ist, wobei jeweils 16 Bit für die Alphakomponente sowie die rote, grüne und die blaue Komponente verwendet werden.<br/>                                                                                          |
| <span id="PixelFormat64bppPARGB"></span><span id="pixelformat64bpppargb"></span><span id="PIXELFORMAT64BPPPARGB"></span><dl> <dt>**PixelFormat64bppPARGB**</dt> </dl>                 | Gibt an, dass das Format 64 Bit pro Pixel ist, wobei jeweils 16 Bit für die Alphakomponente sowie die rote, grüne und die blaue Komponente verwendet werden. Die Rot-, Grün- und Blaukomponente wird entsprechend der Alphakomponente im Voraus multipliziert. <br/> |



## <a name="remarks"></a>Hinweise

**PixelFormat48bppRGB,** **PixelFormat64bppARGB** und **PixelFormat64bppPARGB** verwenden 16 Bits pro Farbkomponente (Kanal). Windows GDI+ Version 1.0 kann 16-Bit-Bilder pro Kanal lesen, aber solche Bilder werden zum Verarbeiten, Anzeigen und Speichern in ein 8-Bit-Format pro Kanal konvertiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Gdipluspixelformats.h</dt> </dl> |



 

 




