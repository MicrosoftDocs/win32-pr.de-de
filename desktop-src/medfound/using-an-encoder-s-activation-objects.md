---
description: Zum Umstellen von Mediendateien in das ASF-Format können Sie Windows Media Encoder verwenden. Um diese Encoder verwenden zu können, müssen Sie beim System registriert werden.
ms.assetid: 18c26619-6047-4f7f-bb65-ca418f02e5b1
title: Verwenden von Encoders-Aktivierungs Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd44a1b97ad0f133b7215ff4474835ddfba66bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863935"
---
# <a name="using-an-encoders-activation-objects"></a>Verwenden der Aktivierungs Objekte eines Encoders

Zum Umstellen von Mediendateien in das ASF-Format können Sie Windows Media Encoder verwenden. Um diese Encoder verwenden zu können, müssen Sie beim System registriert werden.

Weitere Informationen zur encoderregistrierung finden Sie unter [Instanziieren eines Encoders MFT](instantiating-the-encoder-mft.md).

-   [Verwenden der Aktivierungs Objekte eines Encoders](#using-an-encoders-activation-objects)
-   [Encoderenumeration in Windows 7 und höher](#encoder-enumeration-in-windows-7-and-later)
-   [Zugehörige Themen](#related-topics)

## <a name="using-an-encoders-activation-objects"></a>Verwenden der Aktivierungs Objekte eines Encoders

Als Alternative zur Verwendung der [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle eines Encoders (beschrieben unter [Erstellen eines Encoders mithilfe von cokreateinstance](using-an-encoder-s-imftransform--interface.md)) können Sie eine Instanz des Aktivierungs Objekts für den Encoder erstellen. Aktivierungs Objekte erleichtern die encodererstellung, und Media Foundation stellt die folgenden beiden Funktionen für diesen Ansatz bereit:

-   [**MF | atewmaencoderaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) zum Instanziieren des Windows Media-Audioencoders.
-   [**MF | atewmvencoderaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) zum Instanziieren des Windows Media-Video Encoders.

Beide Funktionen erfordern, dass Sie den Ziel Medientyp erstellen und die Codierungs Eigenschaften festlegen, bevor Sie diese Funktionen aufrufen. Wenn Ihre Anwendung die [ASF-Komponenten der Pipeline Schicht](pipeline-layer-asf-components.md) verwendet, um eine Datei in das ASF-Format zu codieren, und die [ASF-Medien senken](asf-media-sinks.md)bereits erstellt und konfiguriert haben, können Sie diesen Satz von Informationen aus der ASF-Medien Senke erhalten.

[**Mfkreatewmaencoderaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) und [**mfkreatewmvencoderaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) legen Sie den Ausgabetyp des Encoders auf den Medientyp fest, der von der Anwendung angegeben wird.

**Hinweis**  Wenn Sie [**mfcreatewmaencoderaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) und [**mfcreatewmvencoderaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) verwenden, können Sie den Encoder durch Aufrufen von [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) aktivieren, aber Sie können die Eingabe-und Ausgabemedien Typen des Encoders nicht ändern, und Sie können die Codierungs Eigenschaften nicht ändern.

Weitere Informationen zum Erstellen von Media Foundation Objekten mithilfe von Aktivierungs Objekten finden Sie unter [Activation Objects](activation-objects.md).

**So erhalten Sie den Ziel Medientyp aus der ASF-Medien Senke**

1.  Rufen Sie einen Zeiger auf den [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Zeiger der ASF-Medien Senke ab, indem Sie **imfmediasink:: QueryInterface** in der ASF-Medien Senke aufrufen und **IID \_ imfasfcontentinfo** als Schnittstellen Bezeichner übergeben.
2.  Holen Sie sich das dem ContentInfo-Objekt zugeordnete ASF-Profil Objekt.
3.  Listet die Streams im Profil auf, um den Medientyp des Streams zu erhalten.

**So erhalten Sie die Codierungs Eigenschaften aus der ASF-Medien Senke**

1.  Wenn Sie die [Codierungs Eigenschaften](configuring-the-encoder.md) in der Medien Senke konfiguriert haben (siehe [Festlegen von Eigenschaften in der Datei Senke](setting-properties-in-the-file-sink.md)), können Sie einen Verweis auf den Eigenschaften Speicher der Senke aufrufen, indem Sie **imfmediasink:: QueryInterface** in der ASF-Medien Senke aufrufen und **IID \_ IPropertyStore** als Schnittstellen Bezeichner übergeben.
2.  Wenn Sie einen Zeiger auf das ContentInfo-Objekt der Senke haben, können Sie [**imfasfcontentinfo:: getencodingconfigurationpropertystore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) aufrufen, um einen Verweis auf den Eigenschaften Speicher der Medien Senke zu erhalten.

    Stellen Sie sicher, dass alle Codierungs Eigenschaften, die auf der ASF-Medien Senke festgelegt sind, im Eigenschaften Speicher widergespiegelt werden, der an [**mfkreatewmaencoderaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) und [**mfkreatewmvencoderaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate)übergeben wird. Der Encoder wird automatisch basierend auf den von der Anwendung angegebenen Einstellungen konfiguriert.

Beim Erstellen des Transformations Knotens in der Codierungs Topologie können Sie den Objekttyp als [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger festlegen, der in diesen beiden Aufrufen empfangen wird. Wenn die Topologie aufgelöst wird, verwendet die Medien Sitzung das Aktivierungs Objekt, um eine Instanz des MFT-Encoders zu erstellen.

## <a name="encoder-enumeration-in-windows-7-and-later"></a>Encoderenumeration in Windows 7 und höher

Für Anwendungen, die unter Windows 7 ausgeführt werden, können Sie zusätzlich zu [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) die Encoder-MFTs durch Aufrufen von [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)auflisten. Diese Funktion gibt einen Zeiger auf das Aktivierungs Objekt des Encoder-MFT zurück. Die Struktur der Funktion ähnelt der oben beschriebenen **mftenum** , außer dass **mftenumex** ein Array von [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeigern für die Encoder-MFTs zurückgibt, die den Suchkriterien entsprechen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Instanziieren eines MFT-Encoders](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Media Encoder](windows-media-encoders.md)
</dt> <dt>

[Aktivierungs Objekte](activation-objects.md)
</dt> </dl>

 

 



