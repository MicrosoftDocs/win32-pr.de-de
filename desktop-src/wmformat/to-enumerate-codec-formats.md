---
title: So aufzählen Sie Codecformate
description: So aufzählen Sie Codecformate
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- Streams,Aufzählen von Codecformaten
- Codecs,Enumerationen
- Streams, Codecformate
- Codecs,Formate
- codecs,IWMCodecInfo-Schnittstelle
- IWMCodecInfo,Codec-Formate
- codecs,IWMCodecInfo3-Schnittstelle
- IWMCodecInfo3, Codecformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a00c9afdbeba5a187be4b992a19d4c9bdb138e1
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444781"
---
# <a name="to-enumerate-codec-formats"></a>So aufzählen Sie Codecformate

Ein Codecformat ist ein Streamkonfigurationsobjekt, das mit Daten aus einem Codec aufgefüllt wird. Jedes Codecformat enthält eine vom Codec unterstützte Medienkonfiguration. Die meisten Audiocodecs unterstützen eine begrenzte Anzahl von Formaten, von denen jedes vom Codec aufzählt wird und auf die mithilfe der [**Methoden von IWMCodecInfo zugegriffen werden kann.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo) Videocodecs bieten dagegen nur ein einzelnes Format. Dies liegt daran, dass Videostreams Variablen wie die Framegröße haben, die flexibler als die Einstellungen eines Audiostreams sind. Mit einem Videostream müssen Sie einige der Streamkonfigurationswerte ausfüllen. Audiostreamkonfigurationen sollten nur bearbeitet werden, um einen Namen, einen Verbindungsnamen und eine Streamnummer zu zuweisen. Weitere Informationen finden Sie unter [Allgemeine Konfiguration für alle Streams.](configuration-common-to-all-streams.md)

Die aufgelisteten Codecformate hängen von den aktuellen Codecenumerationseinstellungen ab, die [**mitHILFE von IWMCodecInfo3::SetCodecEnumerationSetting festgelegt werden.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting) Derzeit werden nur zwei Codeceigenschaften unterstützt: g wszNumPasses, das die Anzahl der vom Codec durchzuführenden Codierungsüberläufe angibt, und \_ g wszVBREnabled, das angibt, ob der Codec die Codierung mit variabler Bitrate \_ verwendet. Die maximale Anzahl von Codierungsüberläufen, die von einem der Codecs unterstützt werden, beträgt zwei. Daher gibt es vier unterschiedliche Konfigurationen, für die Sie Codecs abrufen können, wie in der folgenden Tabelle gezeigt.



|    &nbsp;    | CBR-Stream (Constant Bit Rate) | 2-Pass-CBR-Stream | Qualitätsbasierter Stream mit variabler Bitrate (VBR) | Bitratenbasierter VBR-Stream (eingeschränkt oder nicht eingeschränkt) |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| g \_ wszVBREnabled | FALSE                          | FALSE             | TRUE                                         | TRUE                                                     |
| g \_ wszNumPasses  | 1                              | 2                 | 1                                            | 2                                                        |



 

Um die für einen Codec unterstützten Formate zu aufzählen, verwenden Sie [**IWMCodecInfo::GetCodecFormatCount,**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) um die Anzahl der unterstützten Codecs zu finden. Rufen Sie [**dann IWMCodecInfo::GetCodecFormat für**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) jedes Format auf. Die Formatindizes reichen von 0 (null) bis zu einem Wert kleiner als die Gesamtzahl der unterstützten Formate. Sie können eine Beschreibung des Formats abrufen, indem Sie [**IWMCodecInfo2::GetCodecFormatDesc aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc) Bei Verwendung **von GetCodecFormatDesc** müssen Sie **GetCodecFormat** nicht verwenden, da das Streamkonfigurationsobjekt von beiden Methoden abgerufen wird. Videocodecformate enthalten keine Beschreibung. Jeder Videocodec hat nur ein Format, das für alle Streams dieses Typs verwendet wird.

Wenn Sie ein Codecformat abrufen, erhalten Sie die [**IWMStreamConfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) eines Streamkonfigurationsobjekts, das die Formateinstellungen enthält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Abrufen von Streamkonfigurationsinformationen aus Codecs**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




