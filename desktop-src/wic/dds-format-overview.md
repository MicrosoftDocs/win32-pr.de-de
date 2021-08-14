---
description: Stellt Informationen zum nativen DDS-Codec bereit, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Übersicht über das DDS-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a9fd00f17d17b7bb227a04e56bbc9369de86eb03f9c953a73267400d4a6df9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204477"
---
# <a name="dds-format-overview"></a>Übersicht über das DDS-Format

Dieses Thema enthält Informationen zum nativen DDS-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.

## <a name="codec-identity"></a>Codec-Identität

Die folgende Tabelle enthält Codec-Identifikationsinformationen.



| Komponente              | BESCHREIBUNG        |
|------------------------|--------------------|
| Formale Namen         | DirectDraw Surface |
| Dateinamenerweiterung(en) | Dds                |
| MIME-Typ (MIME type)              | image/vnd-ms.dds   |



 

In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen DDS-Codeckomponenten verwendet werden.



| Komponente        | Anzeigename            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Containerformat | GUID \_ ContainerFormatDds | 9967cb95-2e85-4ac8-8ca283d7ccd425c9 |
| Decoder          | CLSID \_ WICDdsDecoder     | 9053699f-a341-429d-9e90ee437cf80c73 |
| Encoder          | CLSID \_ WICDdsEncoder     | a61dde94-66ce-4ac1-881b71680588895e |



 

## <a name="pixel-format-support"></a>Pixelformatunterstützung

Beachten Sie, dass das DDS-Format jeden gültigen [**DXGI \_ FORMAT-Wert**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) unterstützt. Der WIC DDS-Codec unterstützt jedoch nur Decodierungs- und Codierungsdateien mit den folgenden Formaten:

-   DXGI \_ FORMAT \_ BC1 \_ UNORM
-   DXGI \_ FORMAT \_ BC2 \_ UNORM
-   \_DXGI-FORMAT \_ BC3 \_ UNORM

## <a name="encoding"></a>Codierung

Die WIC-Codierungs-APIs sind codecunabhängig. Daher ist die Bildcodierung für WIC-fähige Codecs im Wesentlichen identisch. Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie unter Übersicht über [die Codierung.](-wic-creating-encoder.md)

Das DDS-Dateiformat hat besondere Anforderungen, die sich aus seiner Unterstützung für Konzepte wie Mipmaps und Texturarrays ergeben. Um die DDS-Bildcodierung vollständig zu steuern, sollten Sie die [**IWICDdsEncoder-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) verwenden, um DDS-spezifische Codierungsparameter festlegen.

## <a name="decoding"></a>Decodierung

Die WIC-Decodierungs-APIs sind codecunabhängig, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bilddecodierung finden Sie in der [Übersicht über die Decodierung.](-wic-creating-decoder.md) Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)

## <a name="block-compressed-data-access"></a>Blockieren des Zugriffs auf komprimierte Daten

Zusätzlich zur Unterstützung der standardmäßigen WIC-Codecschnittstellen bietet der DDS-Decoder direkten Zugriff auf die systemeigenen, blockkomprimierten Daten mithilfe der DDS-spezifischen Schnittstellen [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) und [**IWICDdsFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode) Um diese Schnittstellen zu verwenden, rufen Sie QueryInterface von [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) bzw. [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)auf.

 

 
