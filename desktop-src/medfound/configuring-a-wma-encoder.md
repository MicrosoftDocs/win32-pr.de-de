---
description: Festlegen eines Ausgabe Typs für einen WMA-Encoder
ms.assetid: 0a1a22bb-460f-4ac2-be76-4249997441de
title: Festlegen eines Ausgabe Typs für einen WMA-Encoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6b078dc2426b062a90f706c5d113960f54ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127961"
---
# <a name="setting-an-output-type-for-a-wma-encoder"></a>Festlegen eines Ausgabe Typs für einen WMA-Encoder

Um einen gültigen Ausgabetyp für einen Windows Media Audio-Encoder (WMA) zu erstellen, müssen Sie über die folgenden Informationen verfügen:

-   Der audiountertyp, der das codierte WMA-Format repmmert. Siehe [audiountertyp-GUIDs](audio-subtype-guids.md).
-   Die Konfigurations Eigenschaften, die für den Encoder festgelegt werden sollen.

    Die Konfigurations Eigenschaften sind in der Dokumentation zu Windows Media Audio und Video Codec und DSP-APIs dokumentiert. Weitere Informationen finden Sie unter "audiostreameigenschaften" in den [Codierungs Eigenschaften](configuring-the-encoder.md).

### <a name="windows-vista-or-later"></a>Windows Vista oder höher

Um einen gültigen Ausgabetyp für den Encoder zu erhalten, führen Sie die folgenden Schritte aus.

1.  Verwenden Sie die Funktion [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) oder [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) zum Erstellen einer Instanz des Encoders.
2.  Fragen Sie den Encoder nach der **IPropertyStore** -Schnittstelle ab.
3.  Verwenden Sie die **IPropertyStore** -Schnittstelle, um den Encoder zu konfigurieren.
4.  Rufen Sie die unterstützten Ausgabetypen ab, indem Sie [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) in einer Schleife aufrufen, bis der Encoder die Datei " **MF \_ E \_ No \_ more \_** " zurückgibt und Sie den Ziel Medientyp auswählen. I
5.  Aufrufen von [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) , um den Medientyp für die Komprimierung für den Encoder festzulegen.

### <a name="windows-7"></a>Windows 7

Um einen gültigen Ausgabetyp für den Encoder in Windows 7 zu erhalten, stellt Media Foundation die [**mftranscodegetaudiooutputavailabletypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) -Funktion bereit. Für eine Anwendung muss der audiountertyp erforderlich sein, der die codierte WMA-und Codierungs Eigenschaften ableitet. Die Eigenschaften sind erforderlich, da der Encoder die unterstützten Ausgabetypen abhängig vom festgelegten Modus ändert.

> [!Note]  
> [**Mftranscodegetaudiooutputavailabletypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)wird nur für die [Konstante Bitrate-Codierung](constant-bit-rate-encoding.md)unterstützt.

 

Wenn der-Vorgang erfolgreich ist, empfängt die Anwendung eine Liste der IUnknown-Zeiger der unterstützten Ausgabemedien Typen in einem [**imfcollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) -Objekt. Um den Typ des Ausgabe Mediums festzulegen, suchen Sie nach dem Typ, der mit dem Zieltyp übereinstimmt, und geben Sie [**imftransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) ein, um den Typ der Komprimierungs Medien für den Encoder

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Instanziieren eines MFT-Encoders](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Media Encoder](windows-media-encoders.md)
</dt> </dl>

 

 



