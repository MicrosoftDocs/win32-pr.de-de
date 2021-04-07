---
title: So zählen Sie Codec-Formate auf
description: So zählen Sie Codec-Formate auf
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- Streams, Auflisten von Codec-Formaten
- Codecs, Enumerationen
- Streams, Codec-Formate
- Codecs, Formate
- Codecs, iwmcodecinfo-Schnittstelle
- Iwmcodecinfo, Codec-Formate
- Codecs, IWMCodecInfo3-Schnittstelle
- IWMCodecInfo3, Codec-Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ea062723ec1480a82b45fd025fb7a8c37020d5
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104038676"
---
# <a name="to-enumerate-codec-formats"></a>So zählen Sie Codec-Formate auf

Ein Codec-Format ist ein Datenstrom-Konfigurationsobjekt, das mit Daten aus einem Codec aufgefüllt ist. Jedes Codec-Format enthält eine Medien Konfiguration, die vom Codec unterstützt wird. Die meisten Audiocodecs unterstützen eine endliche Anzahl von Formaten, von denen jede durch den Codec aufgezählt wird und auf die mit den Methoden von [**iwmcodecinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)zugegriffen werden kann. Mit Video Codecs hingegen wird nur ein einzelnes Format bereitgestellt. Dies liegt daran, dass Videostreams Variablen wie die Frame Größe aufweisen, die flexibler als die Einstellungen eines Audiodatenstroms sind. Mit einem Videostream müssen Sie einige der streamkonfigurationswerte ausfüllen. audiostreamkonfigurationen sollten nur bearbeitet werden, um einen Namen, einen Verbindungs Namen und eine streamnummer zuzuweisen. Weitere Informationen finden Sie unter [Allgemeine Konfiguration für alle Streams](configuration-common-to-all-streams.md).

Die aufgezählten Codec-Formate hängen von den aktuellen Codec-enumerationseinstellungen ab, die mithilfe von [**IWMCodecInfo3:: setcodecenumerationsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting)festgelegt werden. Zurzeit werden nur zwei Codec-Eigenschaften unterstützt: g \_ wsznumpass, das die Anzahl der Codierungs Überläufen angibt, die der Codec durchführt, und g \_ wszvbrenabled, die angibt, ob der Codec Variablen Bitrate Codierung verwendet. Die maximale Anzahl von Codierungs Durchläufen, die von einem der Codecs unterstützt werden, ist 2. es gibt also vier verschiedene Konfigurationen, für die Sie Codecs abrufen können, wie in der folgenden Tabelle dargestellt.



|                  | Konstanter Bitrate (CBR)-Stream | 2-Pass-CBR-Stream | Quality-based Variable Bitrate (VBR)-Stream | Bitraten basierter VBR-Datenstrom (eingeschränkt oder nicht eingeschränkt) |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| g \_ wszvbrenabled | false                          | false             | TRUE                                         | TRUE                                                     |
| g \_ wsznumpass  | 1                              | 2                 | 1                                            | 2                                                        |



 

Um die für einen Codec unterstützten Formate aufzulisten, verwenden Sie [**iwmcodecinfo:: getcodecformatcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) , um die Anzahl der unterstützten Codecs zu ermitteln. Nennen Sie anschließend [**iwmcodecinfo:: getcodecformat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) für jedes Format. Die Format Indizes reichen von Null bis zu einem Wert, der kleiner als die Gesamtzahl unterstützter Formate ist. Sie können eine Beschreibung des Formats durch Aufrufen von [**IWMCodecInfo2:: getcodecformatdesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc)abrufen. Wenn Sie **getcodecformatdesc** verwenden, ist es nicht erforderlich, **getcodecformat** zu verwenden, da das Datenstrom-Konfigurationsobjekt von beiden Methoden abgerufen wird. Videocodec-Formate enthalten keine Beschreibung. Jeder Videocodec verfügt nur über ein Format, das für alle Streams dieses Typs verwendet wird.

Wenn Sie ein Codec-Format abrufen, erhalten Sie die [**iwmstreamconfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) -Schnittstelle eines Stream-Konfigurations Objekts, das die Format Einstellungen enthält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu streamkonfigurations Informationen von Codecs**](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




