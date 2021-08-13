---
description: WavSink-Beispiel
ms.assetid: 9e1af25f-d55c-45db-8c76-abf814e16700
title: WavSink-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1bd754e426d848e9d84aea337225ea51940d8727c63d1e1c78c93aeea43110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737135"
---
# <a name="wavsink-sample"></a>WavSink-Beispiel

Veranschaulicht das Implementieren einer benutzerdefinierten Mediensenke in Microsoft Media Foundation. Im Beispiel wird eine Archivsenke implementiert, die unkomprimierte PCM-Audiodaten in eine WAV-Datei schreibt.

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden Media Foundation veranschaulicht:

-   [**DEADClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**VEREERBUNGFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**VERERBUNGMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)
-   [**DELEGATEMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
-   [**DURCHSTREAMSTREAMSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)

## <a name="usage"></a>Verbrauch

Das WavSink-Beispiel enthält zwei Visual Studio Projekte:

-   WavSink.vcproj erstellt eine statische Bibliothek, die die Implementierung der Mediensenke enthält.
-   WriteWavFile.vcproj erstellt eine Konsolenanwendung, die die Mediensenke verwendet, um eine WAV-Datei zu erstellen. Diese Anwendung ist mit der Bibliothek verknüpft, die vom WavSink-Projekt erstellt wurde.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [github-Repository Windows klassischen Beispielen verfügbar.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> <dt>

[Mediensenken](media-sinks.md)
</dt> </dl>

 

 



