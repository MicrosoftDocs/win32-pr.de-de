---
description: Zum Konvertieren von Mediendateien in das ASF-Format können Sie Windows Media Encoder verwenden. Erfahren Sie mehr über die Verwendung der Aktivierungsobjekte eines Encoders.
ms.assetid: 18c26619-6047-4f7f-bb65-ca418f02e5b1
title: Verwenden von Encoderaktivierungsobjekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24915020c1b888be6a1aeaca1e21af95d11cfc181a5c00a91c8359c3f780fa0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972739"
---
# <a name="using-an-encoders-activation-objects"></a>Verwenden der Aktivierungsobjekte eines Encoders

Zum Konvertieren von Mediendateien in das ASF-Format können Sie Windows Media Encoder verwenden. Um diese Encoder verwenden zu können, müssen sie beim System registriert werden.

Informationen zur Encoderregistrierung finden Sie unter [Instanziieren eines Encoder MFT.](instantiating-the-encoder-mft.md)

-   [Verwenden der Aktivierungsobjekte eines Encoders](#using-an-encoders-activation-objects)
-   [Encoderenumeration in Windows 7 und höher](#encoder-enumeration-in-windows-7-and-later)
-   [Zugehörige Themen](#related-topics)

## <a name="using-an-encoders-activation-objects"></a>Verwenden der Aktivierungsobjekte eines Encoders

Als Alternative zur Verwendung der [**-Schnittstelle DES ENCODERs (beschrieben**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) unter Creating an Encoder by Using CoCreateInstance ) (Erstellen eines [Encoders mithilfe von CoCreateInstance)](using-an-encoder-s-imftransform--interface.md)können Sie eine Instanz des Aktivierungsobjekts für den Encoder erstellen. Aktivierungsobjekte erleichtern die Encodererstellung und Media Foundation stellt die folgenden beiden Funktionen für diesen Ansatz zur Verfügung:

-   [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) zum Instanziieren des Windows Media-Audioencoder.
-   [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) zum Instanziieren des Windows Media Video Encoder.

Beide Funktionen erfordern, dass Sie den Zielmedientyp erstellen und die Codierungseigenschaften festlegen, bevor Sie diese Funktionen aufrufen. Wenn Ihre Anwendung [ASF-Komponenten](pipeline-layer-asf-components.md) auf Pipelineebene verwendet, um eine Datei im ASF-Format zu codieren, und die ASF-Mediensenken bereits erstellt und konfiguriert haben, können Sie diese Informationen von der ASF-Mediensenke erhalten. [](asf-media-sinks.md)

[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) und [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) legen den Ausgabetyp des Encoders auf den von der Anwendung angegebenen Medientyp fest.

**Hinweis:**  Wenn Sie [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) und [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) verwenden, können Sie den Encoder aktivieren, indem Sie [**DENTactivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) aufrufen. Sie können jedoch weder die Eingabe- und Ausgabemedientypen des Encoders noch die Codierungseigenschaften ändern.

Weitere Informationen zum Erstellen von Media Foundation-Objekten mithilfe von Aktivierungsobjekten finden Sie unter [Activation Objects](activation-objects.md).

**So erhalten Sie den Zielmedientyp aus der ASF-Mediensenke**

1.  Rufen Sie einen Zeiger auf den [**IMFASFContentInfo-Zeiger**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) der ASF-Mediensenke ab, indem Sie FÜR DIE ASF-Mediensenke DURCH Aufrufen **vonGEFMediaSink::QueryInterface** **iiD \_ IMFASFContentInfo** als Schnittstellenbezeichner übergeben.
2.  Hier erhalten Sie das ASF-Profilobjekt, das dem ContentInfo-Objekt zugeordnet ist.
3.  Enumerieren Sie die Streams im Profil, um den Medientyp des Streams zu erhalten.

**So erhalten Sie die Codierungseigenschaften aus der ASF-Mediensenke**

1.  Wenn Sie die Codierungseigenschaften [in](configuring-the-encoder.md) der Mediensenke konfiguriert haben (wie unter Festlegen von Eigenschaften [in](setting-properties-in-the-file-sink.md)der Dateisenke beschrieben), können Sie einen Verweis auf den Eigenschaftenspeicher der Senke erstellen, indem Sie **DIE MEDIENMEDIASink::QueryInterface** in der ASF-Mediensenke aufrufen und **IID \_ IPropertyStore** als Schnittstellenbezeichner übergeben.
2.  Wenn Sie über einen Zeiger auf das ContentInfo-Objekt der Senke verfügen, können Sie [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) aufrufen, um einen Verweis auf den Eigenschaftenspeicher der Mediensenke zu erhalten.

    Stellen Sie sicher, dass alle Codierungseigenschaften, die für die ASF-Mediensenke festgelegt sind, im Eigenschaftenspeicher widergespiegelt werden, der an [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) und [**MFCreateWMVEncoderActivate übergeben wird.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) Der Encoder wird automatisch basierend auf den von der Anwendung angegebenen Einstellungen konfiguriert.

Beim Erstellen des Transformationsknotens in der Codierungstopologie können Sie den Objekttyp als [**EINEN INAKTIVAktivierungszeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) festlegen, der in diesen beiden Aufrufen empfangen wurde. Wenn die Topologie aufgelöst wird, verwendet die Mediensitzung das Aktivierungsobjekt, um eine Instanz des Encoder-MFT zu erstellen.

## <a name="encoder-enumeration-in-windows-7-and-later"></a>Encoderenumeration in Windows 7 und höher

Für Anwendungen, die auf Windows 7 ausgeführt werden, können Sie zusätzlich zu [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) die Encoder-MFTs aufzählen, indem Sie [**MFTEnumEx aufrufen.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) Diese Funktion gibt einen Zeiger auf das Aktivierungsobjekt des Encoder-MFT zurück. Die Struktur der Funktion ähnelt der oben beschriebenen **MFTEnum-** mit der Ausnahme, dass **MFTEnumEx** für die Encoder-MFTs, die den Suchkriterien entsprechen, ein Array von VERWERT-Zeigern zurückgibt. [](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Instanziieren eines Encoder-MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Media Encoder](windows-media-encoders.md)
</dt> <dt>

[Aktivierungsobjekte](activation-objects.md)
</dt> </dl>

 

 



