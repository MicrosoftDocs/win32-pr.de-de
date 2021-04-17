---
description: Beispiel Attribute
ms.assetid: 64aead5a-61c4-4e83-a556-af33e0aa82be
title: Beispiel Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1329946c36b1b7454deb76a25247985d9dcfdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527842"
---
# <a name="sample-attributes"></a>Beispiel Attribute

Die folgenden Attribute gelten für [Medien Beispiele](media-samples.md). Um die Attribute aus einem Medien Beispiel zu erhalten, verwenden Sie die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle.



| Attribut                                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF Sample Extension \_ 3dvideo](mfsampleextension-3dvideo.md)                                                    | Gibt an, ob ein Medien Beispiel einen 3D-Videoframe enthält.                                                                                                                                                                                        |
| [MF Sample Extension \_ 3dvideo \_ Sample Format](mfsampleextension-3dvideo-sampleformat.md)                         | Gibt an, wie ein 3D-Videoframe in einem Medien Beispiel gespeichert wird.                                                                                                                                                                                        |
| [**MF Sample Extension \_ bottomfieldfirst**](mfsampleextension-bottomfieldfirst-attribute.md)                    | Gibt die Feld Dominanz für einen verschachtelten Videorahmen an.                                                                                                                                                                                       |
| [MF Sample Extension \_ cameraextrinsics](mfsampleextension-cameraextrinsics.md)                                  | Die Kamera ist extra insics für das Beispiel.                                                                                                                                                                                                              |
| [MF Sample Extension \_ capturemetadata](mfsampleextension-capturemetadata.md)                                    | Der [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Speicher für alle Metadaten, die mit der Aufzeichnungs Pipeline verknüpft sind.                                                                                                                                             |
| [**MF Sample Extension- \_ Cleanpoint**](mfsampleextension-cleanpoint-attribute.md)                                | Gibt an, ob ein Video Beispiel ein Keyframe ist.                                                                                                                                                                                                   |
| [MF SampleExtension- \_ Inhalts \_ Schlüssel-ID](mfsampleextension-content-keyid.md)                                       | Legt die Schlüssel-ID für das Beispiel fest.                                                                                                                                                                                                                    |
| [**MF Sample Extension \_ derivedfromtopfield**](mfsampleextension-derivedfromtopfield-attribute.md)              | Gibt an, ob ein Deinterlacing-Videoframe aus dem oberen Feld oder dem unteren Feld abgeleitet wurde.                                                                                                                                                  |
| [MF Sample Extension \_ devicetimestamp](mfsampleextension-devicetimestamp.md)                                    | Der Zeitstempel des Gerätetreibers.                                                                                                                                                                                                             |
| [**Diskontinuität von MF SampleExtension \_**](mfsampleextension-discontinuity-attribute.md)                          | Gibt an, ob ein Medien Beispiel nach einer Lücke im Stream das erste Beispiel ist.                                                                                                                                                                    |
| [MF SampleExtension \_ Encryption \_ cryptbyteblock](mfsampleextension-encryption-cryptbyteblock.md)               | Gibt die verschlüsselte Byte Blockgröße für die Beispiel basierte Muster Verschlüsselung an.                                                                                                                                                                       |
| [Verschlüsselungsschutz Schema für MF SampleExtension \_ \_](mfsampleextension-encryption-protectionscheme.md)           | Gibt das Schutzschema für verschlüsselte Beispiele an.                                                                                                                                                                                             |
| [MF SampleExtension \_ Encryption \_ SampleID](mfsampleextension-encryption-sampleid.md)                           | Gibt die ID einer verschlüsselten Stichprobe an.                                                                                                                                                                                                           |
| [MF SampleExtension- \_ Verschlüsselung \_ skipbyteblock](mfsampleextension-encryption-skipbyteblock.md)                 | Gibt die eindeutige (nicht verschlüsselte) Byte Blockgröße für die Beispiel basierte Muster Verschlüsselung an.                                                                                                                                                           |
| [MF SampleExtension \_ Encryption \_ subsamplemappingsplit](mfsampleextension-encryption-subsamplemappingsplit.md) | Legt die unter Stichproben Zuordnung für das Beispiel fest, das die unverschlüsselten und verschlüsselten Bytes in den Beispiel Daten angibt.                                                                                                                                            |
| [MF SampleExtension- \_ frameworkbeschädigung](mfsampleextension-framecorruption.md)                                    | Gibt an, ob ein Videoframe beschädigt ist.                                                                                                                                                                                                      |
| [MF Sample Extension \_ forwardeddecodeunits](mfsampleextension-forwardeddecodeunits.md)                          | Ruft ein Objekt vom Typ [**imbercollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) ab, das [**imbersample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Objekte enthält, die von einem Decoder weitergeleitete Einheiten für die Netzwerk Abstraktionsschicht (nalus) und zusätzliche Erweiterungs Informationen (was) enthalten. |
| [MF Sample Extension \_ forwardeddecodeunittype](mfsampleextension-forwardeddecodeunittype.md)                    | Gibt den Typ (Nalu oder ist) einer Einheit an, die an ein [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in einer [mfsampleextension \_ forwardeddecodeunits](mfsampleextension-forwardeddecodeunits.md) -Auflistung angehängt ist.                                                    |
| [**MF Sample Extension mit Zeilen Sprung \_**](mfsampleextension-interlaced-attribute.md)                                | Gibt an, ob ein Videorahmen Zeilen Sprung oder progressiv ist.                                                                                                                                                                                      |
| [Mfsampleextension \_ longtermreferenceframeinfo](mfsampleextension-longtermreferenceframeinfo.md)              | Gibt Informationen zum Long-Term Reference (LTR)-Frame an und wird im Ausgabe Beispiel zurückgegeben.                                                                                                                                                               |
| [MF Sample Extension " \_ meanabsolutedifference"](mfsampleextension-meanabsolutedifference.md)                      | Dieses Attribut gibt den Mean absolute Difference (Mad) über alle Makroblöcke in der Y-Ebene zurück.                                                                                                                                                  |
| [**MF Sample Extension \_ packetcrossoffsets**](mfsampleextension-packetcrossoffsets-attribute.md)                | Gibt die Nutz Last Begrenzungen für einen Frame an. Dies gilt für verschlüsselte Beispiele.                                                                                                                                                                   |
| [MF SampleExtension- \_ Fotoansicht](mfsampleextension-photothumbnail.md)                                      | Enthält die Foto Miniaturansicht eines [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).                                                                                                                                                                                  |
| [MF Sample Extension \_ photothumbnailmediatype](mfsampleextension-photothumbnailmediatype.md)                    | Enthält den [**imemediatype**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , der den Bild Formattyp beschreibt, der im " [MF SampleExtension \_ photominiatur](mfsampleextension-photothumbnail.md) "-Attribut enthalten ist.                                                      |
| [MF Sample Extension \_ pinholecameraintrinsics](mfsampleextension-pinholecameraintrinsics.md)                    | Die intrinsie-Kamera-Funktionen für das Beispiel.                                                                                                                                                                                                      |
| [**MF Sample Extension \_ repeatfirstfield**](mfsampleextension-repeatfirstfield-attribute.md)                    | Gibt an, ob das erste Feld in einem Zeilen Sprung Rahmen wiederholt werden soll.                                                                                                                                                                                |
| [MF Sample Extension- \_ roirechteck](mfsampleextension-roirectangle.md)                                          | Gibt die Grenzen des relevanten Bereichs an, der den Bereich des Frames angibt, der unterschiedliche Qualität erfordert.                                                                                                                            |
| [**MF Sample Extension- \_ Singlefield**](mfsampleextension-singlefield-attribute.md)                              | Gibt an, ob ein Video Beispiel ein einzelnes Feld oder zwei verschachtelte Felder enthält.                                                                                                                                                                 |
| [MF Sample Extension \_ targetgloballeninance](mfsampleextension-targetgloballuminance.md)                        | Der Wert in Nits, der die Ziel-globale Hintergrundbeleuchtung für den zugeordneten Videoframe angibt.                                                                                                                                           |
| [**MF Sample Extension- \_ Token**](mfsampleextension-token-attribute.md)                                          | Enthält einen Zeiger auf das Token, das für die [**imfmediastream:: requestsample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) -Methode bereitgestellt wurde.                                                                                                             |
| [MF Sample Extension \_ videoencodepicturetype](mfsampleextension-videoencodepicturetype.md)                      | Gibt die Grenzen des relevanten Bereichs an, der den Bereich des Frames angibt, der unterschiedliche Qualität erfordert.                                                                                                                            |
| [MF Sample Extension \_ videoencodeqp](mfsampleextension-videoencodeqp.md)                                        | Gibt den Quantisierungsparameter (QP) an, der zum Codieren eines Video Beispiels verwendet wurde.                                                                                                                                                                  |



 

Nicht jedes Medien Beispiel enthält jedes hier aufgeführte Attribut. In einigen Fällen gilt ein Attribut nur für bestimmte Arten von Daten. Einige Attribute gelten z. b. nur für Videobeispiele und sollten nicht in Audiobeispielen angezeigt werden. In anderen Fällen hat das-Attribut einen Standardwert, der angewendet wird, wenn das Attribut nicht festgelegt ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Medien Beispiele](media-samples.md)
</dt> </dl>

 

 



