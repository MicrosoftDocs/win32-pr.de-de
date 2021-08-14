---
title: So aufzählen Sie Codecformate
description: So aufzählen Sie Codecformate
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- Streams, Aufzählen von Codecformaten
- Codecs, Enumerationen
- Streams, Codecformate
- Codecs, Formate
- codecs,IWMCodecInfo-Schnittstelle
- IWMCodecInfo, Codecformate
- codecs,IWMCodecInfo3-Schnittstelle
- IWMCodecInfo3, Codecformate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5221b675c5aa3b5602bcfda96b22233f77d4ba92199f29f36885a4053700dfd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196516"
---
# <a name="to-enumerate-codec-formats"></a>So aufzählen Sie Codecformate

Ein Codecformat ist ein Datenstromkonfigurationsobjekt, das mit Daten aus einem Codec aufgefüllt wird. Jedes Codecformat enthält eine Medienkonfiguration, die vom Codec unterstützt wird. Die meisten Audiocodecs unterstützen eine begrenzte Anzahl von Formaten, von denen jedes vom Codec aufgezählt wird und auf die mithilfe der Methoden von [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)zugegriffen werden kann. Videocodecs bieten dagegen nur ein einziges Format. Dies liegt daran, dass Videostreams Variablen wie die Framegröße aufweisen, die flexibler als die Einstellungen eines Audiodatenstroms sind. Bei einem Videostream müssen Sie einige der Datenstromkonfigurationswerte eingeben. Audiostreamkonfigurationen sollten nur bearbeitet werden, um einen Namen, einen Verbindungsnamen und eine Streamnummer zuzuweisen. Weitere Informationen finden Sie unter [Configuration Common to All Streams](configuration-common-to-all-streams.md).

Die aufgelisteten Codecformate hängen von den aktuellen Codecenumerationseinstellungen ab, die mit [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting)festgelegt werden. Derzeit werden nur zwei Codeceigenschaften unterstützt: g \_ wszNumPasses, das die Anzahl der vom Codec auszuführenden Codierungsdurchläufe angibt, und g \_ wszVBREnabled, das angibt, ob der Codec die Codierung variabler Bitraten verwendet. Die maximale Anzahl von Codierungsdurchläufen, die von einem der Codecs unterstützt werden, beträgt zwei. Es gibt also vier unterschiedliche Konfigurationen, für die Sie Codecs abrufen können, wie in der folgenden Tabelle gezeigt.



|    &nbsp;    | CbR-Datenstrom (Constant Bit Rate) | 2-Pass-CBR-Datenstrom | Qualitätsbasierter Stream mit variabler Bitrate (VBR) | Bitratenbasierter VBR-Stream (eingeschränkt oder uneingeschränkt) |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| g \_ wszVBREnabled | FALSE                          | FALSE             | TRUE                                         | TRUE                                                     |
| g \_ wszNumPasses  | 1                              | 2                 | 1                                            | 2                                                        |



 

Um die für einen Codec unterstützten Formate aufzulisten, verwenden [**Sie IWMCodecInfo::GetCodecFormatCount,**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) um die Anzahl der unterstützten Codecs zu ermitteln. Rufen Sie dann [**IWMCodecInfo::GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) für jedes Format auf. Die Formatindizes reichen von 0 bis 1 kleiner als die Gesamtzahl der unterstützten Formate. Sie können eine Beschreibung des Formats abrufen, indem Sie [**IWMCodecInfo2::GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc)aufrufen. Wenn **Sie GetCodecFormatDesc** verwenden, müssen Sie **getCodecFormat** nicht verwenden, da das Streamkonfigurationsobjekt von beiden Methoden abgerufen wird. Videocodecformate enthalten keine Beschreibung. Jeder Videocodec hat nur ein Format, das für alle Streams dieses Typs verwendet wird.

Wenn Sie ein Codecformat abrufen, erhalten Sie die [**IWMStreamConfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) eines Streamkonfigurationsobjekts, das die Formateinstellungen enthält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Abrufen von Streamkonfigurationsinformationen von Codecs**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




