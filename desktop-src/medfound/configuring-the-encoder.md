---
description: Codierungs Eigenschaften
ms.assetid: 6845c3fb-38a8-4b0d-aea2-e10f7e518653
title: Codierungs Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 093b72dc37501ca88882c6e3b530cda0eed1baa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127956"
---
# <a name="encoding-properties"></a>Codierungs Eigenschaften

Die Windows Media Audio-und Windows Media Video Encoder unterstützen eine Vielzahl von Codierungs Modi. Diese Modi werden im Allgemeinen durch Festlegen von Eigenschaften für den Encoder [Media Foundation Transform](media-foundation-transforms.md) (MFT) konfiguriert. Um die Datei Codierung durchzuführen, egal ob Sie Komponenten der wmcontainer-Ebene verwenden oder eine partielle Topologie aufbauen, müssen Sie den Encoder entsprechend konfigurieren, indem Sie die Eigenschaften abhängig vom Codierungs Modus und dem Medientyp des Streams festlegen. Der gleiche Satz von Eigenschaften muss sowohl für den Encoder als auch für das-Objekt (ASF File Sink oder ASF Multiplexer) festgelegt werden, das Sie zum Schreiben der ASF-Datei verwenden.

Die Encoder-Eigenschaften werden in wmcodecdsp. h definiert. Die spezifischen Eigenschaften, die verwendet werden, um den Encoder zu konfigurieren, werden mithilfe der Methoden der [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle festgelegt.

-   [Audiostreameigenschaften](#audio-stream-properties)
-   [Videostreameigenschaften](#video-stream-properties)
-   [Konfigurieren des Eigenschaften Speicher des Encoders](#configuring-the-encoders-property-store)

### <a name="audio-stream-properties"></a>Audiostreameigenschaften

In der folgenden Tabelle werden die Encoder-Konfigurationen für einen Audiostream angezeigt.



| Codierungstyp                                                                                        | Eigenschaftsname-Wert                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Konstante Bitrate-Codierung](constant-bit-rate-encoding.md)                                         | Mfpkey \_ vbrenabled- **false** (optional) standardmäßig ist mfpkey \_ vbrenabled auf **false** festgelegt.<br/>                                                                                             |
| [Qualitäts basierte Variable Bitrate Codierung](quality-based-variable-bit-rate--vbr--encoding.md)       | mfpkey \_ vbrenabled- **true**<br/> Mfpkey \_ passesused-1 (optional)<br/> Standardmäßig ist mfpkey \_ passesused auf 1 festgelegt.<br/> Mfpkey \_ gewünschte \_ vbrquality-von 0 bis 100<br/> |
| [Unbeschränkte Variablen Bitrate-Codierung](unconstrained-variable-bit-rate--vbr--encoding.md)       | mfpkey \_ vbrenabled- **true**<br/> Mfpkey \_ passesused-2<br/>                                                                                                                          |
| [Mit Spitzenwerten beschränkte Variable Bitrate-Codierung](peak-constrained-variable-bit-rate--vbr--encoding.md) | mfpkey \_ vbrenabled- **true**<br/> Mfpkey \_ passesused-2<br/> Mfpkey \_ Rmax-maximale Bitrate<br/> Mfpkey \_ bmax-maximales Puffer Fenster<br/>                               |



 

### <a name="video-stream-properties"></a>Videostreameigenschaften

In der folgenden Tabelle werden die Encoder-Konfigurationen für einen Videostream angezeigt.



| Codierungstyp                                                                                        | Eigenschaftenname                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Konstante Bitrate-Codierung](constant-bit-rate-encoding.md)                                         | Mfpkey \_ vbrenabled- **false** (optional)<br/> Standardmäßig ist "mfpkey \_ vbrenabled" auf " **false**" festgelegt.<br/> Mfpkey \_ -Videofenster-Puffer Fenster<br/>                                  |
| [Qualitäts basierte Variable Bitrate Codierung](quality-based-variable-bit-rate--vbr--encoding.md)       | mfpkey \_ vbrenabled- **true**<br/> Mfpkey \_ passesused-1 (optional)<br/> Standardmäßig ist mfpkey \_ passesused auf 1 festgelegt.<br/> Mfpkey \_ gewünschte \_ vbrquality-von 0 bis 100<br/> |
| [Unbeschränkte Variablen Bitrate-Codierung](unconstrained-variable-bit-rate--vbr--encoding.md)       | mfpkey \_ vbrenabled- **true**<br/> Mfpkey \_ passesused-2<br/>                                                                                                                          |
| [Mit Spitzenwerten beschränkte Variable Bitrate-Codierung](peak-constrained-variable-bit-rate--vbr--encoding.md) | mfpkey \_ vbrenabled- **true**<br/> Mfpkey \_ passesused-2<br/> Mfpkey \_ Rmax-maximale Bitrate<br/> Mfpkey \_ bmax-maximales Puffer Fenster<br/>                               |



 

### <a name="configuring-the-encoders-property-store"></a>Konfigurieren des Eigenschaften Speicher des Encoders

Sie müssen einen Encoder konfigurieren, indem Sie den Codierungstyp und die verschiedenen streamspezifischen Einstellungen vor der Codierungs Sitzung angeben. Außerdem müssen Sie die encodereigenschaften im Eigenschaften Speicher eines [ASF ContentInfo-Objekts](asf-contentinfo-object.md) festlegen, das das ASF-Header Objekt der Ausgabedatei darstellt.

Wenn Sie einen Encoder-MFT verwenden:

1.  Sie erhalten einen Verweis auf die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle der Encoder-MFT, wie in [Verwenden der imftransform-Schnittstelle eines Encoders](using-an-encoder-s-imftransform--interface.md)beschrieben.
2.  Abfragen der MFT des Encoders für die **IPropertyStore** -Schnittstelle.
3.  Festlegen der erforderlichen Eigenschaften durch Aufrufen von **IPropertyStore:: SetValue**.

Wenn Sie die integrierten Encoder-Aktivierungs Objekte verwenden und bereits eine konfigurierte ASF-Datei-Senke erstellt haben, können Sie den Eigenschafts Speicher der ASF-Medien Senke an [**mfkreatewmaencoderactivation**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) oder [**mfkreatewmvencoderactivation**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate)übergeben. Der Encoder wird automatisch basierend auf den von der Anwendung angegebenen Einstellungen konfiguriert. Weitere Informationen finden [Sie unter Verwenden der Aktivierungs Objekte eines Encoders](using-an-encoder-s-activation-objects.md).

Weitere Informationen zum Erstellen von Media Foundation Objekten mithilfe von Aktivierungs Objekten finden Sie unter [Activation Objects](activation-objects.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Instanziieren eines MFT-Encoders](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Media Encoder](windows-media-encoders.md)
</dt> </dl>

 

 
