---
description: Festlegen eines Ausgabetyps für einen WMA-Encoder
ms.assetid: 0a1a22bb-460f-4ac2-be76-4249997441de
title: Festlegen eines Ausgabetyps für einen WMA-Encoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48f2731a081138bda30ab3e81f01d353e0348f4d3586fd4c02878b62a7f04393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880571"
---
# <a name="setting-an-output-type-for-a-wma-encoder"></a>Festlegen eines Ausgabetyps für einen WMA-Encoder

Um einen gültigen Ausgabetyp für einen WMA-Encoder (Windows Media Audio) zu erstellen, benötigen Sie die folgenden Informationen:

-   Der Audiountertyp, der das codierte WMA-Format erneut aufweist. Weitere Informationen finden Sie unter [Audio-Untertyp-GUIDs.](audio-subtype-guids.md)
-   Die Konfigurationseigenschaften, die für den Encoder festgelegt werden sollen.

    Die Konfigurationseigenschaften sind in der Dokumentation Windows Medienaudio- und Videocodec und DSP-APIs dokumentiert. Weitere Informationen finden Sie unter "Audiostreameigenschaften" unter [Codierungseigenschaften.](configuring-the-encoder.md)

### <a name="windows-vista-or-later"></a>Windows Vista oder höher

Führen Sie die folgenden Schritte aus, um einen gültigen Ausgabetyp für den Encoder abzurufen.

1.  Verwenden Sie die [**MFTEnum-**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) oder [**MFTEnumEx-Funktion,**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) um eine Instanz des Encoders zu erstellen.
2.  Fragen Sie den Encoder nach der **IPropertyStore-Schnittstelle** ab.
3.  Verwenden Sie die **IPropertyStore-Schnittstelle,** um den Encoder zu konfigurieren.
4.  Rufen Sie die unterstützten Ausgabetypen ab, indem [**Sie ÜBERTRANSFORM::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) in einer Schleife aufrufen, bis der Encoder **MF E NO MORE \_ \_ \_ \_ TYPES** zurückgibt und Sie den Zielmedientyp auswählen. I
5.  Rufen Sie [**ÜBERTRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) auf, um den Komprimierungsmedientyp für den Encoder festzulegen.

### <a name="windows-7"></a>Windows 7

Um einen gültigen Ausgabetyp für den Encoder in Windows 7 abzurufen, stellt Media Foundation die [**MFTranscodeGetAudioOutputAvailableTypes-Funktion**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) bereit. Eine Anwendung muss den Audiountertyp übergeben, der die codierten WMA- und Codierungseigenschaften erneut aufweist. Die Eigenschaften sind erforderlich, da der Encoder die unterstützten Ausgabetypen abhängig vom Modussatz ändert.

> [!Note]  
> [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)wird nur für [Constant Bit Rate Encoding](constant-bit-rate-encoding.md)unterstützt.

 

Wenn der Aufruf erfolgreich ist, empfängt die Anwendung eine Liste von IUnknown-Zeigern der unterstützten Ausgabemedientypen in einem [**POINTERCollection-Objekt.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) Um den Ausgabemedientyp festzulegen, suchen Sie nach dem Typ, der ihrem Zieltyp entspricht, und rufen [**Sie DANN ÜBERTRANSFORM::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) auf, um den Komprimierungsmedientyp auf dem Encoder festzulegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Instanziieren eines Encoder-MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Medienencoder](windows-media-encoders.md)
</dt> </dl>

 

 



