---
description: Instanziieren eines MFT-Encoders
ms.assetid: 50b71c00-b7cf-4c38-8114-bb36b358fda5
title: Instanziieren eines MFT-Encoders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5344c19a3a00c659efbbfd88d42176b876528380
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217032"
---
# <a name="instantiating-an-encoder-mft"></a>Instanziieren eines MFT-Encoders

In Microsoft Media Foundation werden Encoder als [Media Foundation Transformationen](media-foundation-transforms.md) (MFTs) implementiert. Bevor Sie einen Encoder erstellen, müssen Sie zuerst den Encoder ermitteln, der für Ihre Anforderungen am besten geeignet ist.

-   Windows Media-Audiocodecs

    Kategorie: **\_ \_ \_ Audioencoder der MFT-Kategorie**

    Haupttyp: MF MediaType \_ -Audiodatei

    SubType: MF Audioformat \_ WMAudioV9, MF Audioformat \_ WMAudioV8, MF Audioformat \_ wmaudio \_ Lossless, MF Audioformat \_ wmaspdif

-   Windows Media-Video Codecs

    Kategorie: **\_ \_ Video \_ Encoder der MFT-Kategorie**

    Haupttyp: MF MediaType- \_ Video

    Untertyp: MF-Format \_ WVC1, MF-Format \_ WMV3, MF-Format \_ WMV2, MF-Format \_ WMV1

Media Foundation bietet verschiedene Funktionen, die von der Anwendung aufgerufen werden können, um die verschiedenen Encoder aufzulisten, die im System verfügbar sind. Encoder werden als COM-Objekte registriert, und der Registrierungs Eintrag folgt dem Standardformat für com-Klassenfactorys. Die Registrierung verwaltet die CLSIDs für die Encoder, die nach dem Medienformat (Audiodatei oder Video) kategorisiert sind. Die Klassen Bezeichner der Windows Media Encoder werden als Konstanten in der Header Datei "wmcodecdsp. h" definiert. In Media Foundation können die Encoder durch Aufrufe von [**mftregisterlocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) oder [**mftregisterlocalbyclsid**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) registriert werden, indem der catertyp, die unterstützten Eingabetypen und die unterstützten Ausgabetypen angegeben werden. Bei erfolgreicher Registrierung durch diese Funktionen werden die MFTs von den Media Foundation Enumerationsfunktionen berücksichtigt.

Zum Erstellen einer Instanz eines MFT-Encoders hat eine Anwendung die folgenden Optionen.

-   Erstellen Sie den Encoder-MFT direkt, und erhalten Sie einen Zeiger auf die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle. Weitere Informationen finden Sie unter [Erstellen eines Encoders mithilfe von cokreateinstance](using-an-encoder-s-imftransform--interface.md).
-   Erstellen Sie eine Instanz des Aktivierungs Objekts für den Encoder-MFT, und erhalten Sie einen Zeiger auf die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle. Weitere Informationen finden Sie unter [Verwenden der Aktivierungs Objekte eines Encoders](using-an-encoder-s-activation-objects.md).

Wenn Ihre Anwendung in der [Pipeline Schicht-ASF-Komponenten](pipeline-layer-asf-components.md) verwendet, um eine Datei in das ASF-Format zu codieren, müssen Sie den Encoder-MFT als Transformations Knoten in die Pipeline einfügen. Wenn Sie den Transformations Knoten in der Codierungs Topologie erstellen, können Sie entweder den Objekttyp als Zeiger auf die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle oder das [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Objekt festlegen. Media Foundation stellt Aktivierungs Objekte für Windows Media Encoder bereit, sodass Sie bequem als Transformations Knoten in der Codierungs Topologie festgelegt werden können. Wenn die Topologie aufgelöst wird, verwendet die Medien Sitzung das Aktivierungs Objekt, um eine Instanz des MFT-Encoders zu erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows Media Encoder](windows-media-encoders.md)
</dt> </dl>

 

 



