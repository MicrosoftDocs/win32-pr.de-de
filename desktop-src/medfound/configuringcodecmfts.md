---
description: Konfigurieren von Codec-MFTs
ms.assetid: 0de0cb2e-67bc-4db5-879a-95879f16b98d
title: Konfigurieren von Codec-MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb4a9ae53c0aee61e30fb5d61b2ad78fd4fe8e624df394f462dd01618272476
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743332"
---
# <a name="configuring-codec-mfts"></a>Konfigurieren von Codec-MFTs

In diesem Thema wird der Prozess der Konfiguration der Codec-MFTs beschrieben. Jeder Codec verfügt über bestimmte Verfahren, aber die informationen, die allen gemeinsam sind, werden hier beschrieben.

## <a name="configuring-mft-inputs-and-outputs"></a>Konfigurieren von MFT-Eingaben und -Ausgaben

Jeder MFT unterstützt bestimmte Eingabe- und Ausgabetypen. Sie können unterstützte Eingabetypen abrufen, indem Sie [**WIEDERHOLT DENTRANSFORM::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)aufrufen und den Typindex mit jedem Aufruf erhöhen. Wenn Sie einen geeigneten Typ finden, legen Sie den Eingabetyp fest, indem Sie [**DENTRANSFORM::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)aufrufen. Anschließend können Sie den Prozess für den Ausgabetyp wiederholen, indem Sie die Aufrufe [**VONTRANSFORM::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) und [**VONTRANSTRANSFORM::SetOutputType verwenden.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) Sie müssen die verfügbaren Ausgabetypen erst nach dem Festlegen des Eingabetyps abfragen oder festlegen.

## <a name="configuring-the-codec-mfts-for-encoding"></a>Konfigurieren der Codec-MFTs für die Codierung

Alle Windows Medienaudio- und Videocodecs unterstützen eine Vielzahl von Codierungsfunktionen. Diese Features werden im Allgemeinen konfiguriert, indem Eigenschaften für den MFT mithilfe der Methoden der **IPropertyStore-Schnittstelle** festgelegt werden. Einige Eigenschaften werden mit speziellen Codecschnittstellen konfiguriert. Diese Schnittstellen sind für jeden Codec im Abschnitt [CodecObjekte](codecobjects.md)aufgeführt.

Die allgemeine Reihenfolge der Vorgänge zum Konfigurieren eines Codierungs-MFT lautet wie folgt:

1.  Konfigurieren Sie Codecfunktionen wie gewünscht mithilfe der Methoden von **IPropertyStore.**
2.  Verwenden Sie die Codec-MFT-Schnittstellen, um bei Bedarf zusätzliche Features zu konfigurieren.
3.  Konfigurieren Sie die Eingabe- und Ausgabetypen. Die Reihenfolge, in der die Typen konfiguriert werden sollen, variiert je nach Codec. Weitere Informationen finden Sie unter [Working with Audio (Arbeiten mit Audio)](workingwithaudio.md) und [Working with Video (Arbeiten mit Video).](workingwithvideo.md)

## <a name="configuring-the-codec-mfts-for-decoding"></a>Konfigurieren der Codec-MFTs für die Decodierung

Die Decodierung ist einfacher als die Codierung, da weniger Decoderfeatures unterstützt werden.

Die allgemeine Reihenfolge der Vorgänge zum Konfigurieren eines decodierenden MFT lautet wie folgt:

1.  Konfigurieren Sie Decoderfeatures wie gewünscht mithilfe der Methoden von **IPropertyStore.**
2.  Legen Sie den Eingabetyp auf den Typ fest, der für die Encoderausgabe verwendet wird.
3.  Konfigurieren Sie den Ausgabetyp. Die unterstützten Ausgabetypen unterscheiden sich für verschiedene Eingaben.

> [!Note]  
> Es ist wichtig, für die Decodereingabe denselben Medientyp wie für die Encoderausgabe zu verwenden. Dies liegt daran, dass die Windows Medienaudio- und Videocodecs Medienformate mit zusätzlichen Daten verwenden. Ohne die erweiterten Formatdaten können Sie den komprimierten Inhalt nicht decodieren.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



