---
description: Instanziieren eines Encoder-MFT
ms.assetid: 50b71c00-b7cf-4c38-8114-bb36b358fda5
title: Instanziieren eines Encoder-MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40337bbef63cf243777978d1672a60de5ebfba8874b3cce0271ca06ccf4ab38b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974269"
---
# <a name="instantiating-an-encoder-mft"></a>Instanziieren eines Encoder-MFT

In Microsoft Media Foundation werden Encoder als [Media Foundation](media-foundation-transforms.md) (MFTs) implementiert. Bevor Sie einen Encoder erstellen, müssen Sie zuerst den Encoder finden, der für Ihre Anforderungen am besten geeignet ist.

-   Windows Codecs für Medienaudio

    Kategorie: **MFT \_ CATEGORY AUDIO \_ \_ ENCODER**

    Haupttyp: MFMediaType Audio \_

    SubType: MFAudioFormat \_ WMAudioV9, MFAudioFormat \_ WMAudioV8, MFAudioFormat \_ WMAudio \_ Lossless, MFAudioFormat \_ WMASPDIF

-   Windows Codecs für Medienvideos

    Kategorie: **MFT \_ CATEGORY VIDEO \_ \_ ENCODER**

    Haupttyp: \_ MFMediaType-Video

    Untertyp: MFVideoFormat \_ WVC1, MFVideoFormat \_ WMV3, MFVideoFormat \_ WMV2, MFVideoFormat \_ WMV1

Media Foundation bietet mehrere Funktionen, die Ihre Anwendung aufrufen kann, um die verschiedenen Encoder aufzählen zu können, die in Ihrem System verfügbar sind. Encoder werden als COM-Objekte registriert, und der Registrierungseintrag folgt dem Standardformat für COM-Klassen-Factorys. Die Registrierung verwaltet die CLSIDs für die Encoder, die nach dem Medienformat (Audio oder Video) kategorisiert sind. Die Klassenbezeichner der Windows Media Encoders werden in der Headerdatei wmcodecdsp.h als Konstanten definiert. In Media Foundation können die Encoder durch Aufrufe von [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) oder [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) registriert werden, indem die Kategorie, die unterstützten Eingabetypen und die unterstützten Ausgabetypen angegeben werden. Nach erfolgreicher Registrierung über diese Funktionen werden die MFTs von den Media Foundation berücksichtigt.

Zum Erstellen einer Instanz eines Encoder-MFT hat eine Anwendung die folgenden Optionen.

-   Erstellen Sie den Encoder MFT direkt, und empfangen Sie einen Zeiger auf die [**BENUTZEROBERFLÄCHETransform-Schnittstelle.**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) Weitere Informationen finden Sie unter [Erstellen eines Encoders mithilfe von CoCreateInstance](using-an-encoder-s-imftransform--interface.md).
-   Erstellen Sie eine Instanz des Aktivierungsobjekts für den Encoder MFT, und empfangen Sie einen Zeiger auf die [**SCHNITTSTELLE FÜR DIE AKTIVIERUNG.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) Weitere Informationen finden Sie unter [Verwenden von Aktivierungsobjekten eines Encoders.](using-an-encoder-s-activation-objects.md)

Wenn Ihre Anwendung [ASF-Komponenten](pipeline-layer-asf-components.md) der Pipelineebene verwendet, um eine Datei im ASF-Format zu codieren, müssen Sie den Encoder MFT als Transformationsknoten in die Pipeline einfügen. Beim Erstellen des Transformationsknotens in der Codierungstopologie können Sie entweder den Objekttyp als Zeiger auf die [**SCHNITTSTELLE BZW.**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) das [**OBJEKT FÜR DIE Codierung**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) festlegen. Media Foundation stellt Aktivierungsobjekte für Windows Media Encoders zur Bequemensung als Transformationsknoten in der Codierungstopologie. Wenn die Topologie aufgelöst wird, verwendet die Mediensitzung das Aktivierungsobjekt, um eine Instanz des Encoder-MFT zu erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Media Encoder](windows-media-encoders.md)
</dt> </dl>

 

 



