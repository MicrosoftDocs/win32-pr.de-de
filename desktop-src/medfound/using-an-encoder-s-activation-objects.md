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

Informationen zur Encoderregistrierung finden Sie unter [Instanziieren eines Encoder-MFT.](instantiating-the-encoder-mft.md)

-   [Verwenden der Aktivierungsobjekte eines Encoders](#using-an-encoders-activation-objects)
-   [Encoderenumeration in Windows 7 und höher](#encoder-enumeration-in-windows-7-and-later)
-   [Zugehörige Themen](#related-topics)

## <a name="using-an-encoders-activation-objects"></a>Verwenden der Aktivierungsobjekte eines Encoders

Als Alternative zur Verwendung der [**ENCODER-SCHNITTSTELLE VONTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) (beschrieben unter [Erstellen eines Encoders mit CoCreateInstance)](using-an-encoder-s-imftransform--interface.md)können Sie eine Instanz des Aktivierungsobjekts für den Encoder erstellen. Aktivierungsobjekte erleichtern die Encodererstellung, und Media Foundation stellt die folgenden beiden Funktionen für diesen Ansatz bereit:

-   [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) zum Instanziieren des Windows Media-Audioencoders.
-   [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) zum Instanziieren des Windows Media-Videoencoders.

Beide Funktionen erfordern, dass Sie den Zielmedientyp erstellen und die Codierungseigenschaften festlegen, bevor Sie diese Funktionen aufrufen. Wenn Ihre Anwendung [ASF-Komponenten](pipeline-layer-asf-components.md) auf Pipelineebene zum Codieren einer Datei im ASF-Format verwendet und die [ASF-Mediensenken](asf-media-sinks.md)bereits erstellt und konfiguriert hat, können Sie diesen Satz von Informationen aus der ASF-Mediensenke abrufen.

[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) und [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) legen den Ausgabetyp des Encoders auf den von der Anwendung angegebenen Medientyp fest.

**Hinweis**  Wenn Sie [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) und [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) verwenden, können Sie den Encoder aktivieren, indem Sie [**DIE AKTIONACTIVATE::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) aufrufen. Sie können jedoch weder die Eingabe- und Ausgabemedientypen des Encoders noch die Codierungseigenschaften ändern.

Weitere Informationen zum Erstellen von Media Foundation Objekten mithilfe von Aktivierungsobjekten finden Sie unter [Activation Objects](activation-objects.md).

**So erhalten Sie den Zielmedientyp aus der ASF-Mediensenke**

1.  Rufen Sie einen Zeiger auf den [**IMFASFContentInfo-Zeiger**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) der ASF-Mediensenke ab, indem Sie ÜBER EINEN AUFRUF **VONMEDIASink::QueryInterface** in der ASF-Mediensenke **iid \_ IMFASFContentInfo** als Schnittstellenbezeichner übergeben.
2.  Abrufen des ASF-Profilobjekts, das dem ContentInfo-Objekt zugeordnet ist.
3.  Aufzählen der Datenströme im Profil, um den Medientyp des Streams abzurufen.

**So erhalten Sie die Codierungseigenschaften aus der ASF-Mediensenke**

1.  Wenn Sie die [Codierungseigenschaften](configuring-the-encoder.md) in der Mediensenke konfiguriert haben (wie unter [Festlegen von Eigenschaften in der Dateisenke](setting-properties-in-the-file-sink.md)beschrieben), können Sie einen Verweis auf den Eigenschaftenspeicher der Senke erstellen, indem Sie **AUFMEDIASink::QueryInterface** für die ASF-Mediensenke aufrufen und **IID \_ IPropertyStore** als Schnittstellenbezeichner übergeben.
2.  Wenn Sie einen Zeiger auf das ContentInfo-Objekt der Senke haben, können Sie [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) aufrufen, um einen Verweis auf den Eigenschaftenspeicher der Mediensenke abzurufen.

    Stellen Sie sicher, dass alle Codierungseigenschaften, die für die ASF-Mediensenke festgelegt sind, im Eigenschaftenspeicher widergespiegelt werden, der an [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) und [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate)übergeben wird. Der Encoder wird automatisch basierend auf den von der Anwendung angegebenen Einstellungen konfiguriert.

Beim Erstellen des Transformationsknotens in der Codierungstopologie können Sie den Objekttyp als [**einen INDATEActivate-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) festlegen, der in diesen beiden Aufrufen empfangen wird. Wenn die Topologie aufgelöst wird, verwendet die Mediensitzung das Aktivierungsobjekt, um eine Instanz des Encoder-MFT zu erstellen.

## <a name="encoder-enumeration-in-windows-7-and-later"></a>Encoderenumeration in Windows 7 und höher

Für Anwendungen, die auf Windows 7 ausgeführt werden, können Sie zusätzlich zu [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) die Encoder-MFTs aufzählen, indem Sie [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)aufrufen. Diese Funktion gibt einen Zeiger auf das Aktivierungsobjekt des Encoder-MFT zurück. Die Struktur der Funktion ähnelt der oben **beschriebenen MFTEnum-Struktur,** mit der Ausnahme, dass **MFTEnumEx** ein Array von [**POINTERActivate-Zeigern**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) für die Encoder-MFTs zurückgibt, die den Suchkriterien entsprechen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Instanziieren eines Encoder-MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Medienencoder](windows-media-encoders.md)
</dt> <dt>

[Aktivierungsobjekte](activation-objects.md)
</dt> </dl>

 

 



