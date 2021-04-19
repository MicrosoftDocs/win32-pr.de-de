---
description: Enthält Informationen über den systemeigenen DDS-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Übersicht über das DDS-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c45222a66d5a250caaf46db465d2359e09b3e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348648"
---
# <a name="dds-format-overview"></a>Übersicht über das DDS-Format

Dieses Thema enthält Informationen über den systemeigenen DDS-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.

## <a name="codec-identity"></a>Codec-Identität

In der folgenden Tabelle werden Codec-Identifikationsinformationen bereitstellt.



|                        |                    |
|------------------------|--------------------|
| Formaler Name (n)         | DirectDraw-Oberfläche |
| Dateinamenerweiterung (en) | DDS                |
| MIME-Typ (MIME type)              | Image/vnd-ms. DDS   |



 

In der folgenden Tabelle werden die GUIDs aufgelistet, mit denen die systemeigenen DDS-Codec-Komponenten identifiziert werden.



| Komponente        | Anzeigename            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Container Format | GUID \_ containerformatdds | 9967cb95-2e85-4ac8-8ca283d7ccd425c9 |
| Decoder          | CLSID \_ wicddsdecoder     | 9053699f-A341-429d-9e90ee437cf80c73 |
| Encoder          | CLSID \_ wicddsencoder     | a61dde94-66ce-4ac1-881b71680588895e |



 

## <a name="pixel-format-support"></a>Unterstützung für Pixel Formate

Beachten Sie, dass das DDS-Format einen beliebigen gültigen [**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) Wert unterstützt. Der WIC-DDS-Codec unterstützt jedoch nur das Decodieren und Codieren von Dateien, die die folgenden Formate enthalten:

-   DXGI- \_ Format \_ BC1 \_ unorm
-   DXGI- \_ Format \_ BC2 \_ unorm
-   DXGI- \_ Format \_ BC3 \_ unorm

## <a name="encoding"></a>Codierung

Die WIC-Codierungs-APIs sind als Codec-unabhängig konzipiert, daher ist die Bildcodierung für WIC-fähige Codecs im Wesentlichen identisch. Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).

Das DDS-Dateiformat weist besondere Anforderungen auf, die aus der Unterstützung von Konzepten wie Mipmaps und Textur Arrays entstehen. Um die Kontrolle über die DDS-Bildcodierung vollständig zu steuern, sollten Sie die [**iwicddsencoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) -Schnittstelle verwenden, um DDS-spezifische Codierungs Parameter festzulegen.

## <a name="decoding"></a>Decodierung

Die WIC-Decodierung-APIs sind als Codec-unabhängig konzipiert, und die Decodierung von Bildern für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Decodierung von Bildern finden Sie in der Übersicht über die [Decodierung](-wic-creating-decoder.md). Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).

## <a name="block-compressed-data-access"></a>Komprimierten Datenzugriff blockieren

Zusätzlich zur Unterstützung der standardmäßigen WIC-Codec-Schnittstellen ermöglicht der DDS-Decoder den direkten Zugriff auf die systemeigenen Block komprimierten Daten mithilfe der DDS-spezifischen Schnittstellen [**iwicddsdecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) und [**iwicddsframedecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode). Um diese Schnittstellen zu verwenden, wird QueryInterface von [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) bzw. [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)aufgerufen.

 

 
