---
description: DirectX-Video Beschleunigung 2,0
ms.assetid: acb73b20-89fa-4a48-be4a-846715a239b0
title: DirectX-Video Beschleunigung 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3ae813d3c81ebcf753dcaa273cc9f9149eaab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214313"
---
# <a name="directx-video-acceleration-20"></a>DirectX-Video Beschleunigung 2,0

Die DirectX-Video Beschleunigung (DXVA) ist eine API und ein entsprechendes DDI für die Verwendung der Hardwarebeschleunigung zum beschleunigen der Video-Codec-Verarbeitung. Software Codecs und Software-Video Prozessoren können mithilfe von DXVA bestimmte CPU-intensive Vorgänge an die GPU auslagern. Beispielsweise kann ein Software Decoder die umgekehrte diskrete Kosinus Transformation (IDCT) in die GPU auslagern.

In diesem Abschnitt werden die folgenden Themen behandelt:

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                             | BESCHREIBUNG                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu DXVA 2,0](about-dxva-2-0.md)<br/>                                                   | Übersicht über DXVA 2 und seine Beziehung zu DXVA 1.<br/>                                                                                                                                                        |
| [Direct3D Device Manager](direct3d-device-manager.md)<br/>                                 | Mit dem Microsoft Direct3D-Geräte-Manager können zwei oder mehr Objekte dasselbe Microsoft Direct3D 9-Gerät gemeinsam verwenden.<br/>                                                                                      |
| [Unterstützung von DXVA 2,0 in DirectShow](supporting-dxva-2-0-in-directshow.md)<br/>             | In diesem Thema wird beschrieben, wie DirectX Video Acceleration (DXVA) 2,0 in einem DirectShow-Decoderfilter unterstützt wird.<br/>                                                                                             |
| [Unterstützung von DXVA 2,0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md)<br/> | In diesem Thema wird beschrieben, wie die DirectX-Video Beschleunigung (DXVA) 2,0 in einer Media Foundation Transformation (MFT) mit Direct3D 9 unterstützt wird.<br/>                                                                      |
| [DXVA-Video Verarbeitung](dxva-video-processing.md)<br/>                                     | Die DXVA-Videoverarbeitung kapselt die Funktionen der Grafikhardware, die für die Verarbeitung von nicht komprimierten Videobildern verwendet werden. Die Video Verarbeitungsdienste umfassen Deinterlacing und Video Mischung.<br/> |
| [DXVA-HD](dxva-hd.md)<br/>                                                                 | Microsoft DirectX Video Acceleration High Definition (DXVA-HD) ist eine API für die hardwarebeschleunigte Video Verarbeitung. <br/>                                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-Programmier Handbuch](media-foundation-programming-guide.md)
</dt> <dt>

[DXVA 1-Spezifikation](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
