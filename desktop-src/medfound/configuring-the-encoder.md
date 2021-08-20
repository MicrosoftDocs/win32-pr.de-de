---
description: Codierungseigenschaften
ms.assetid: 6845c3fb-38a8-4b0d-aea2-e10f7e518653
title: Codierungseigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc7a1528e68153c742ece8c8d7fcb34bfb9b7bbc08f86567f51b54754bb6da3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743492"
---
# <a name="encoding-properties"></a>Codierungseigenschaften

Die Windows Media Audio und Windows Media Video-Encoder unterstützen eine Vielzahl von Codierungsmodi. Diese Modi werden in der Regel durch Festlegen von Eigenschaften auf dem Encoder Media Foundation [Transform (MFT)](media-foundation-transforms.md) konfiguriert. Zum Ausführen der Dateicodierung, unabhängig davon, ob Komponenten auf WMContainer-Ebene oder eine partielle Topologie erstellt werden, müssen Sie den Encoder entsprechend konfigurieren, indem Sie Eigenschaften abhängig vom Codierungsmodus und dem Medientyp des Streams festlegen. Derselbe Satz von Eigenschaften muss sowohl für den Encoder als auch für das Objekt (ASF-Dateisenke oder ASF-Multiplexer) festgelegt werden, die Sie zum Schreiben der ASF-Datei verwenden.

Die Encodereigenschaften werden in wmcodecdsp.h definiert. Die spezifischen Eigenschaften, die zum Konfigurieren des Encoders verwendet werden, werden mithilfe der Methoden der [**IPropertyStore-Schnittstelle**](/windows/win32/api/propsys/nn-propsys-ipropertystore) festgelegt.

-   [Audiostreameigenschaften](#audio-stream-properties)
-   [VideoStream-Eigenschaften](#video-stream-properties)
-   [Konfigurieren der Eigenschaft des Encoders Store](#configuring-the-encoders-property-store)

### <a name="audio-stream-properties"></a>Audiostreameigenschaften

Die folgende Tabelle zeigt die Encoderkonfigurationen für einen Audiostream.



| Codierungstyp                                                                                        | Eigenschaftenname – Wert                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codierung der konstanten Bitrate](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED – **FALSE** (optional)Standardmäßig ist MFPKEY \_ VBRENABLED auf **FALSE festgelegt.**<br/>                                                                                             |
| [Qualitätsbasierte Codierung mit variabler Bitrate](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED – **TRUE**<br/> MFPKEY \_ PASSESUSED – 1 (optional)<br/> Standardmäßig ist MFPKEY \_ PASSESUSED auf 1 festgelegt.<br/> MFPKEY \_ DESIRED \_ VBRQUALITY – Von 0 bis 100<br/> |
| [Codierung der unkonstraineden Variablenbitrate](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED – **TRUE**<br/> MFPKEY \_ PASSESUSED - 2<br/>                                                                                                                          |
| [Codierung der variablen Bitrate mit eingeschränkter Spitzenrate](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED – **TRUE**<br/> MFPKEY \_ PASSESUSED - 2<br/> MFPKEY \_ RMAX – Maximale Bitrate<br/> MFPKEY \_ BMAX – Maximales Pufferfenster<br/>                               |



 

### <a name="video-stream-properties"></a>VideoStream-Eigenschaften

Die folgende Tabelle zeigt die Encoderkonfigurationen für einen Videostream.



| Codierungstyp                                                                                        | Eigenschaftenname                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Codierung der konstanten Bitrate](constant-bit-rate-encoding.md)                                         | MFPKEY \_ VBRENABLED – **FALSE** (optional)<br/> Standardmäßig ist MFPKEY \_ VBRENABLED auf **FALSE festgelegt.**<br/> MFPKEY \_ VIDEOWINDOW – Pufferfenster<br/>                                  |
| [Qualitätsbasierte Codierung mit variabler Bitrate](quality-based-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED – **TRUE**<br/> MFPKEY \_ PASSESUSED – 1 (optional)<br/> Standardmäßig ist MFPKEY \_ PASSESUSED auf 1 festgelegt.<br/> MFPKEY \_ DESIRED \_ VBRQUALITY – Von 0 bis 100<br/> |
| [Codierung der unkonstraineden Variablenbitrate](unconstrained-variable-bit-rate--vbr--encoding.md)       | MFPKEY \_ VBRENABLED – **TRUE**<br/> MFPKEY \_ PASSESUSED - 2<br/>                                                                                                                          |
| [Codierung der variablen Bitrate mit eingeschränkter Spitzenrate](peak-constrained-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ VBRENABLED – **TRUE**<br/> MFPKEY \_ PASSESUSED - 2<br/> MFPKEY \_ RMAX – Maximale Bitrate<br/> MFPKEY \_ BMAX – Maximales Pufferfenster<br/>                               |



 

### <a name="configuring-the-encoders-property-store"></a>Konfigurieren der Eigenschaft des Encoders Store

Sie müssen einen Encoder konfigurieren, indem Sie vor der Codierungssitzung den Typ der Codierung und die verschiedenen streamspezifischen Einstellungen angeben. Sie müssen auch die Encodereigenschaften im Eigenschaftenspeicher eines [ASF ContentInfo-Objekts](asf-contentinfo-object.md) festlegen, das das ASF-Headerobjekt der Ausgabedatei darstellt.

Wenn Sie einen Encoder-MFT verwenden:

1.  Hiermit erhalten Sie einen Verweis auf die [**BENUTZEROBERFLÄCHEtransform-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) des Encoders MFT, wie unter Verwenden der [ENCODER-SCHNITTSTELLE FÜR DIETRANSFORM-Schnittstelle beschrieben.](using-an-encoder-s-imftransform--interface.md)
2.  Abfragen des Encoder-MFT für die **IPropertyStore-Schnittstelle.**
3.  Festlegen der erforderlichen Eigenschaften durch Aufrufen von **IPropertyStore::SetValue**.

Wenn Sie die integrierten Encoderaktivierungsobjekte verwenden und bereits eine konfigurierte ASF-Dateisenke erstellt haben, können Sie den Eigenschaftenspeicher der ASF-Mediensenke an [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) oder [**MFCreateWMVEncoderActivate übergeben.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) Der Encoder wird automatisch basierend auf den von der Anwendung angegebenen Einstellungen konfiguriert. Weitere Informationen finden Sie in der unter Verwenden von [Aktivierungsobjekten eines Encoders beschriebenen Prozedur.](using-an-encoder-s-activation-objects.md)

Weitere Informationen zum Erstellen von Media Foundation-Objekten mithilfe von Aktivierungsobjekten finden Sie unter [Activation Objects](activation-objects.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Instanziieren eines Encoder-MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Media Encoder](windows-media-encoders.md)
</dt> </dl>

 

 
