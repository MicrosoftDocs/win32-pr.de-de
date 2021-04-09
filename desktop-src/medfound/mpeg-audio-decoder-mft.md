---
description: Der Microsoft MPEG-Audiodecoder ist eine synchrone Media Foundation Transformation (MFT), die das Decodieren von MPEG-audioelementaren streamformaten mithilfe der Media Foundation (MF)-Pipeline ermöglicht.
ms.assetid: 29A0491D-CA0D-4909-96F0-5640D5EE77F9
title: MPEG-Audiodecoder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98106ce4610c7c89a5e6212c225fd8eca3e4526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959235"
---
# <a name="mpeg-audio-decoder"></a>MPEG-Audiodecoder

Der Microsoft MPEG-Audiodecoder ist eine synchrone [Media Foundation Transformation](media-foundation-transforms.md) (MFT), die das Decodieren von MPEG-audioelementaren streamformaten mithilfe der Media Foundation (MF)-Pipeline ermöglicht.

Der Decoder unterstützt die folgenden MPEG-Datenstrom Formate.

-   MPEG-1-Audioebenen I und II (ISO/IEC 11172-3). 2. MPEG-2 rückwärtskompatibel, Ebenen I und II (ISO

-   MPEG-2 rückwärtskompatibel, Ebenen I und II (ISO/IEC 13818-3), Mono und Stereo

## <a name="class-identifier"></a>Klassen Bezeichner

Der Klassen Bezeichner (CLSID) des MPEG-Audiodecoders ist **CLSID \_ msmpeer gauddecmft**, der in der Header Datei wmcodecdsp. h definiert ist.

## <a name="input-media-types"></a>Eingabemedien Typen

Der MPEG-Audiodecoder unterstützt die folgenden Attribute für den Eingabe Medientyp.



| Attribut                                                                               | Wert                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Haupt-Typ des MF- \_ MT \_ \_**](mf-mt-major-type-attribute.md)                               | **MF MediaType \_ -Audiodatei**                                                                                                                                                                                                                                                |
| [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)                                      | **MF Audioformat \_ MPEG**                                                                                                                                                                                                                                               |
| [**MF \_ \_ -MT- \_ audionum- \_ Kanäle**](mf-mt-audio-num-channels-attribute.md)              | Optionale Normalerweise 1 für Mono oder 2 für Stereo, kann jedoch bis zu sechs Kanäle sein.<br/>                                                                                                                                                                                |
| [**MF \_ \_ -MT \_ - \_ audiokanalmaske**](mf-mt-audio-channel-mask-attribute.md)              | Optionale Normalerweise 0x4 für Mono oder 0x3 für Stereo, kann aber auch eine der Kanalmasken sein, die bis zu 6 Kanälen zugeordnet sind (3/2/1, 3/2, 3/1, 2/2, 2/1). Wenn die Kanalmaske vorhanden ist, muss Sie mit der angegebenen Eingabe Anzahl von Kanälen konsistent sein.<br/> |
| [**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde**](mf-mt-audio-samples-per-second-attribute.md) | Optionale Eines der folgenden: 16000, 22050, 24000, 32000, 44100, 48000. Wenn angegeben, muss die Eingabe Stichproben Rate eine der gültigen MPEG-Stichproben Raten sein.<br/>                                                                                             |



 

## <a name="output-media-types"></a>Ausgabemedien Typen

Der MPEG-Audiodecoder unterstützt bis zu vier Ausgabemedien-Untertypen in der folgenden Reihenfolge.

<dl> 1. Stereo, Gleit Komma.  
2. Stereo-und 16-Bit-PCM.  
3. Mono, Gleit Komma Zahl (nur, wenn die Eingabe Mono oder Dual-Mono ist).  
4. Mono, 16-Bit-PCM (nur, wenn die Eingabe Mono oder Dual-Mono ist).  
</dl>

Der Decoder unterstützt immer die Stereoausgabe und wird als erster Ausgabe Medientyp aufgelistet.

Der Decoder unterstützt die folgenden Attribute des Ausgabemedien Typs.



| Attribut                                                                           | Wert                                                                      |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [Haupt-Typ des MF- \_ MT \_ \_](mf-mt-major-type-attribute.md)                               | **MF MediaType \_ -Audiodatei**                                                     |
| [MF- \_ MT- \_ Untertyp](mf-mt-subtype-attribute.md)                                      | **MF Audioformat \_ PCM** oder **MF Audioformat \_ float**                  |
| [MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel](mf-mt-audio-bits-per-sample-attribute.md)       | 16 oder 32                                                                   |
| [MF \_ \_ -MT- \_ audionum- \_ Kanäle](mf-mt-audio-num-channels-attribute.md)              | 1 oder 2                                                                     |
| [MF \_ \_ -MT \_ - \_ audiokanalmaske](mf-mt-audio-channel-mask-attribute.md)              | 0x4 für Mono oder 0x3 für Stereo                                             |
| [MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde](mf-mt-audio-samples-per-second-attribute.md) | Eines der folgenden: 16000, 22050, 24000, 32000, 44100, 48000.<br/> |



 

## <a name="transform-attributes"></a>Transformations Attribute

Der MPEG-Audiodecoder implementiert die [**IMF Transform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) -Methode. Anwendungen können diese Methode verwenden, um die folgenden Attribute zu erhalten oder festzulegen.



| Attribut                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Codecapi \_ avdecaudiodualmono**](../directshow/avdecaudiodualmono-property.md)                   | Gibt an, ob die decodierte 2-Kanal-Audiodatei Dual Mono ist. Schreibgeschützt. Wird von der MFT festgelegt. Weitere Informationen finden Sie unter [**eavdecaudiodualmono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).                                                                                                                               |
| [**Codecapi \_ avdecaudiodualmonorepromode**](../directshow/avdecaudiodualmonorepromode-property.md) | Gibt an, wie der Decoder Dual Mono-Audiodaten wiederherstellt. Der Standardwert ist **eavdecaudiodualmonorepromode \_ left \_ Mono**.<br/> Lesen/Schreiben Anwendungen können diese Eigenschaft festlegen, um das Standardverhalten zu ändern. Weitere Informationen finden Sie unter [**eavdecaudiodualmono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).<br/> |
| [**Codecapi \_ avenccommonmeanbitrate**](../directshow/avenccommonmeanbitrate-property.md)           | Gibt die komprimierte streambitrate an. Schreibgeschützt. Wird von der MFT festgelegt.                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-Objekte](codecobjects.md)
</dt> </dl>

 

 
