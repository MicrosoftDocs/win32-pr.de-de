---
description: Dieses Thema enthält Informationen über den nativen GIF-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Übersicht über GIF-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f592b50300edf79c71ff4050a2c0d5aeba8b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216964"
---
# <a name="gif-format-overview"></a>Übersicht über GIF-Format

Dieses Thema enthält Informationen über den nativen GIF-Codec, der über die Windows Imaging Component (WIC) verfügbar ist.

## <a name="codec-identity"></a>Codec-Identität

In der folgenden Tabelle werden Codec-Identifikationsinformationen bereitstellt.



|                        |                                       |
|------------------------|---------------------------------------|
| Formaler Name (n)         | Graphics Interchange Format 89A (GIF) |
| Dateinamenerweiterung (en) | GIF                                   |
| MIME-Typ (MIME type)              | image/gif                             |
| Spezifikations Unterstützung  | GIF-Spezifikation 89A/89m             |



 

In der folgenden Tabelle werden die GUIDs aufgelistet, mit denen die systemeigenen GIF-Codec-Komponenten identifiziert werden.



| Komponente        | Anzeigename            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Container Format | GUID \_ containerformatgif | 1F 8a5601-7d4d-4cbd-9c821bc8d4eeb9a5 |
| Decoder          | CLSID- \_ wicgifdecoder     | 381dda3c-9ce9-4834-a23e1f98f8fc52be |
| Encoder          | CLSID \_ wicgifencoder     | 114 f 5598-0b22-40A0-86a1c83ea495adbd |



 

## <a name="encoding"></a>Codierung

Die WIC-Codierungs-API ist als Codec-unabhängig konzipiert, und die Bildcodierung für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Bildcodierung mithilfe der WIC-API finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Codierungsoptionen

WIC-fähige Codecs unterscheiden sich auf der Codierungs Options Ebene. Codierungsoptionen entsprechen den Funktionen eines Bild Encoders, und jeder Native Codec unterstützt eine Reihe dieser Codierungsoptionen. Codierungsoptionen können grundlegende WIC-unterstützte Optionen sein, die für alle WIC-fähigen Codes verfügbar sind (aber nicht unbedingt unterstützt werden), oder für Codec-spezifische Optionen, die vom Abbild Format Zum Verwalten dieser Codierungsoptionen während des Codierungs Prozesses verwendet WIC die [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Schnittstelle. Weitere Informationen zur Verwendung der **IPropertyBag2** -Schnittstelle für WIC-Codierung finden Sie in der [Übersicht über die Codierung](-wic-creating-encoder.md).

Der GIF-Encoder unterstützt keine grundlegenden WIC-Optionen und bietet keine benutzerdefinierten Codierungsoptionen. Wenn eine Encoder-Option in der [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) -Optionsliste enthalten ist, wird Sie ignoriert.

## <a name="decoding"></a>Decodierung

Die WIC-Decodierung-API ist als Codec-unabhängig konzipiert, und die Decodierung von Bildern für WIC-fähige Codecs ist im Wesentlichen identisch. Weitere Informationen zur Decodierung von Bildern finden Sie in der Übersicht über die [Decodierung](-wic-creating-decoder.md). Weitere Informationen zur Verwendung von decodierten Bilddaten finden Sie in der [Übersicht über Bitmap-Quellen](-wic-bitmapsources.md).

 

 
