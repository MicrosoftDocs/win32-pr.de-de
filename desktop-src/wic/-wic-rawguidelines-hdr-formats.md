---
description: Hohe dynamische Bereichs Pixel Formate
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: Hohe dynamische Bereichs Pixel Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8405a01fa5397dd5681077ac1ac9acc28e7d1003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867323"
---
# <a name="high-dynamic-range-pixel-formats"></a>Hohe dynamische Bereichs Pixel Formate

Codecs sollten Windows Imaging Component (WIC) Pixel Formate verwenden, die den gesamten dynamischen Bereich der zugrunde liegenden Sensordaten beibehalten. GUID \_ WICPixelFormat48bppRGB ist ein typisches festgelegtes 16-Bit-pro-Channel-Format, das verwendet werden kann. Andere Formate mit höherer Genauigkeit können ebenfalls verwendet werden. Um die vollständige Unterstützung für das Windows Presentation Foundation Graphics Processing Unit (GPU)-beschleunigte Renderingpipeline zu aktivieren, ermutigt Microsoft dringend die Unterstützung für ein 32-Bit-Gleit Komma-Pixel Format.

High Color Pixel Formats: bei Windows 7 wurden zwei neue WIC-Pixel Formate hinzugefügt, um die neuen Hochleistungs-Anzeige Formate zu unterstützen. Dies sind die folgenden: GUID \_ WICPixelFormat32bppRGBA1010102 und GUID \_ WICPixelFormat32bppRGBA1010102XR.

Das "16 Bit pro Channel (BPC) float High Color Format" wird vom vorhandenen GUID \_ WICPixelFormat64bppRGBAHalf Pixel-Format unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über die Windows Imaging-Komponente](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[WIC-Richtlinien für Kamera Rohbild Formate](-wic-rawguidelines.md)
</dt> <dt>

[Schreiben eines WIC-Enabled Codecs](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



