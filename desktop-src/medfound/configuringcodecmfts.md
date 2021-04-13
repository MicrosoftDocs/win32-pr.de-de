---
description: Konfigurieren von Codec-MFTs
ms.assetid: 0de0cb2e-67bc-4db5-879a-95879f16b98d
title: Konfigurieren von Codec-MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0065f05d10eae367b13ef6f7caf3fe2ab322163a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484099"
---
# <a name="configuring-codec-mfts"></a>Konfigurieren von Codec-MFTs

In diesem Thema wird der Prozess der Konfiguration der Codec-MFTs beschrieben. Jeder Codec verfügt über bestimmte Prozeduren, aber die gemeinsamen Informationen werden hier beschrieben.

## <a name="configuring-mft-inputs-and-outputs"></a>Konfigurieren von MFT-Eingaben und-Ausgaben

Jede MFT unterstützt bestimmte Eingabe-und Ausgabetypen. Sie können unterstützte Eingabetypen abrufen, indem Sie " [**imftransform:: getinputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)" wiederholt aufrufen und dabei den Typindex bei jedem Aufruf inkrementieren. Wenn Sie einen geeigneten Typ finden, legen Sie den Eingabetyp durch Aufrufen von [**imftransform:: setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)fest. Anschließend können Sie den Vorgang für den Ausgabetyp mit den Aufrufen [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) und [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)wiederholen. Sie müssen die verfügbaren Ausgabetypen erst Abfragen oder festlegen, nachdem Sie den Eingabetyp festgelegt haben.

## <a name="configuring-the-codec-mfts-for-encoding"></a>Konfigurieren der Codec-MFTs für die Codierung

Alle Windows Media Audio-und Video Codecs unterstützen eine Vielzahl von Codierungs Features. Diese Features werden in der Regel durch Festlegen der Eigenschaften für die MFT mithilfe der Methoden der **IPropertyStore** -Schnittstelle konfiguriert. Einige Eigenschaften werden mithilfe spezieller Codec-Schnittstellen konfiguriert. Diese Schnittstellen werden für jeden Codec im Abschnitt [Codec-Objekte](codecobjects.md)aufgelistet.

Die allgemeine Reihenfolge der Vorgänge zum Konfigurieren einer Codierungs-MFT lautet wie folgt:

1.  Konfigurieren Sie die Codec-Features wie gewünscht mithilfe der Methoden von **IPropertyStore**.
2.  Verwenden Sie die Codec-MFT-Schnittstellen, um zusätzliche Features zu konfigurieren, falls erforderlich.
3.  Konfigurieren Sie die Eingabe-und Ausgabetypen. Die Reihenfolge, in der die Typen konfiguriert werden sollten, variiert für einzelne Codecs. Weitere Informationen finden Sie unter [Arbeiten mit Audiodaten](workingwithaudio.md) und [Arbeiten mit Videos](workingwithvideo.md).

## <a name="configuring-the-codec-mfts-for-decoding"></a>Konfigurieren der Codec-MFTs für das Decodieren

Decodierung ist einfacher als die Codierung, da weniger Decoder-Features unterstützt werden.

Die allgemeine Reihenfolge der Vorgänge zum Konfigurieren einer MFT-Decodierung lautet wie folgt:

1.  Konfigurieren Sie die decoderfeatures wie gewünscht mithilfe der Methoden von **IPropertyStore**.
2.  Legen Sie den Eingabetyp auf den für die encoderausgabe verwendeten Typ fest.
3.  Konfigurieren Sie den Ausgabetyp. Die unterstützten Ausgabetypen unterscheiden sich für unterschiedliche Eingaben.

> [!Note]  
> Es ist wichtig, den gleichen Medientyp für die decodereingabe zu verwenden, die für die encoderausgabe verwendet wurde. Dies liegt daran, dass die Windows Media Audio-und Video Codecs Medienformate mit zusätzlichen Daten verwenden. Ohne die erweiterten Formatierungsdaten können Sie den komprimierten Inhalt nicht decodieren.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



