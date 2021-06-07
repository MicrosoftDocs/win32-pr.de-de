---
description: Stellt Informationen zum nativen DDS-Codec bereit, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Übersicht über das DDS-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f860a5759218575acb53be5f2142e71aa34e9554
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444951"
---
# <a name="dds-format-overview"></a>Übersicht über das DDS-Format

Dieses Thema enthält Informationen zum nativen DDS-Codec, der über die Windows-Bilderstellungskomponente (WIC) verfügbar ist.

## <a name="codec-identity"></a>Codec-Identität

Die folgende Tabelle enthält Informationen zur Codecidentifikation.



| Komponente              | BESCHREIBUNG        |
|------------------------|--------------------|
| Formale Namen         | DirectDraw Surface |
| Dateinamenerweiterungen | Dds                |
| MIME-Typ (MIME type)              | image/vnd-ms.dds   |



 

In der folgenden Tabelle sind die GUIDs aufgeführt, die zum Identifizieren der nativen DDS-Codeckomponenten verwendet werden.



| Komponente        | Anzeigename            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Containerformat | GUID \_ ContainerFormatDds | 9967cb95-2e85-4ac8-8ca283d7ccd425c9 |
| Decoder          | CLSID \_ WICDdsDecoder     | 9053699f-a341-429d-9e90ee437cf80c73 |
| Encoder          | CLSID \_ WICDdsEncoder     | a61dde94-66ce-4ac1-881b71680588895e |



 

## <a name="pixel-format-support"></a>Pixelformatunterstützung

Beachten Sie, dass das DDS-Format jeden gültigen [**DXGI \_ FORMAT-Wert**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) unterstützt. Der WIC-DDS-Codec unterstützt jedoch nur das Decodieren und Codieren von Dateien mit den folgenden Formaten:

-   \_DXGI-FORMAT \_ BC1 \_ UNORM
-   DXGI \_ FORMAT \_ BC2 \_ UNORM
-   \_DXGI-FORMAT \_ BC3 \_ UNORM

## <a name="encoding"></a>Codierung

Die WIC-Codierungs-APIs sind codecunabhängig. Daher ist die Bildcodierung für WIC-fähige Codecs im Wesentlichen identisch. Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der Übersicht über die [Codierung.](-wic-creating-encoder.md)

Das DDS-Dateiformat weist besondere Anforderungen auf, die sich aus der Unterstützung von Konzepten wie Mipmaps und Texturarrays ergeben. Um die Kontrolle über die DDS-Bildcodierung vollständig zu steuern, sollten Sie die [**IWICDdsEncoder-Schnittstelle**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) verwenden, um DDS-spezifische Codierungsparameter festzulegen.

## <a name="decoding"></a>Decodierung

Die WIC-Decodierungs-APIs sind so konzipiert, dass sie codecunabhängig sind, und die Bilddecodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bilddecodierung finden Sie in der Übersicht über die [Decodierung.](-wic-creating-decoder.md) Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmapquellen.](-wic-bitmapsources.md)

## <a name="block-compressed-data-access"></a>Blockieren des Zugriffs auf komprimierte Daten

Zusätzlich zur Unterstützung der standardmäßigen WIC-Codecschnittstellen ermöglicht der DDS-Decoder mithilfe der DDS-spezifischen Schnittstellen [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) und [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode)direkten Zugriff auf die nativen komprimierten Blockdaten. Um diese Schnittstellen zu verwenden, rufen Sie QueryInterface von [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) bzw. [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)auf.

 

 
