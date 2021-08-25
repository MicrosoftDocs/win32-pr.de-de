---
description: Beispielattribute
ms.assetid: 64aead5a-61c4-4e83-a556-af33e0aa82be
title: Beispielattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56593978a411b314e6e988c031ee36869c4ea44212fd7f154e3ba18478400b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776980"
---
# <a name="sample-attributes"></a>Beispielattribute

Die folgenden Attribute gelten für [Medienbeispiele.](media-samples.md) Um die Attribute aus einem Medienbeispiel abzurufen, verwenden Sie die [**INTERFACESAttributes-Schnittstelle.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)



| attribute                                                                                                      | Beschreibung                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md)                                                    | Gibt an, ob ein Medienbeispiel einen 3D-Videoframe enthält.                                                                                                                                                                                        |
| [MFSampleExtension \_ 3DVideo \_ SampleFormat](mfsampleextension-3dvideo-sampleformat.md)                         | Gibt an, wie ein 3D-Videoframe in einem Medienbeispiel gespeichert wird.                                                                                                                                                                                        |
| [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md)                    | Gibt die Felddominanz für einen Videorahmen mit Zeilensprung an.                                                                                                                                                                                       |
| [MFSampleExtension \_ CameraExtrinsics](mfsampleextension-cameraextrinsics.md)                                  | Die Kameraextrinsik für das Beispiel.                                                                                                                                                                                                              |
| [MFSampleExtension \_ CaptureMetadata](mfsampleextension-capturemetadata.md)                                    | Der [**STORESAttribute-Speicher**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) für alle Metadaten im Zusammenhang mit der Erfassungspipeline.                                                                                                                                             |
| [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md)                                | Gibt an, ob ein Videobeispiel ein Keyframe ist.                                                                                                                                                                                                   |
| [MFSampleExtension \_ Content \_ KeyID](mfsampleextension-content-keyid.md)                                       | Legt die Schlüssel-ID für das Beispiel fest.                                                                                                                                                                                                                    |
| [**MFSampleExtension \_ DerivedFromTopField**](mfsampleextension-derivedfromtopfield-attribute.md)              | Gibt an, ob ein deinterlaced Videoframe vom oberen oder unteren Feld abgeleitet wurde.                                                                                                                                                  |
| [MFSampleExtension \_ DeviceTimestamp](mfsampleextension-devicetimestamp.md)                                    | Der Zeitstempel des Gerätetreibers.                                                                                                                                                                                                             |
| [**\_MFSampleExtension-Diskontinuität**](mfsampleextension-discontinuity-attribute.md)                          | Gibt an, ob ein Medienbeispiel das erste Beispiel nach einer Lücke im Stream ist.                                                                                                                                                                    |
| [MFSampleExtension \_ Encryption \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md)               | Gibt die verschlüsselte Byteblockgröße für die stichprobenbasierte Musterverschlüsselung an.                                                                                                                                                                       |
| [MFSampleExtension \_ Encryption \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md)           | Gibt das Schutzschema für verschlüsselte Beispiele an.                                                                                                                                                                                             |
| [MFSampleExtension \_ Encryption \_ SampleID](mfsampleextension-encryption-sampleid.md)                           | Gibt die ID eines verschlüsselten Beispiels an.                                                                                                                                                                                                           |
| [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md)                 | Gibt die eindeutige (nicht verschlüsselte) Byteblockgröße für die beispielbasierte Musterverschlüsselung an.                                                                                                                                                           |
| [MFSampleExtension \_ Encryption \_ SubSampleMappingSplit](mfsampleextension-encryption-subsamplemappingsplit.md) | Legt die Unterbeispielzuordnung für das Beispiel fest, die die eindeutigen und verschlüsselten Bytes in den Beispieldaten angibt.                                                                                                                                            |
| [MFSampleExtension \_ FrameCorruption](mfsampleextension-framecorruption.md)                                    | Gibt an, ob ein Videoframe beschädigt ist.                                                                                                                                                                                                      |
| [MFSampleExtension \_ ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md)                          | Ruft ein Objekt vom Typ [**ABSTRACTIONCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) ab, das [**VON EINEM**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) DECODER weitergeleitete OBJEKTE enthält, die NALUs (Network Abstraction Layer Units) und SEI-Einheiten (Supplemental Enhancement Information) enthalten. |
| [MFSampleExtension \_ ForwardedDecodeUnitType](mfsampleextension-forwardeddecodeunittype.md)                    | Gibt den Typ (NALU oder SEI) einer Einheit an, die an ein [**FORWARDEDSample-Element**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in einer [MFSampleExtension \_ ForwardedDecodeUnits-Auflistung](mfsampleextension-forwardeddecodeunits.md) angefügt ist.                                                    |
| [**MFSampleExtension \_ Interlaced**](mfsampleextension-interlaced-attribute.md)                                | Gibt an, ob ein Videoframe übersprungen oder progressiv ist.                                                                                                                                                                                      |
| [MFSampleExtension \_ LongTermReferenceFrameInfo](mfsampleextension-longtermreferenceframeinfo.md)              | Gibt LTR-Frameinformationen (Long Term Reference) an und wird im Ausgabebeispiel zurückgegeben.                                                                                                                                                               |
| [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md)                      | Dieses Attribut gibt den mittleren absoluten Unterschied (Mean Absolute Difference, MAD) für alle Makroblöcke in der Y-Ebene zurück.                                                                                                                                                  |
| [**MFSampleExtension \_ PacketCrossOffsets**](mfsampleextension-packetcrossoffsets-attribute.md)                | Gibt die Nutzlastgrenzen für einen Frame an. Dies gilt für verschlüsselte Beispiele.                                                                                                                                                                   |
| [MFSampleExtension \_ PhotoThumbnail](mfsampleextension-photothumbnail.md)                                      | Enthält die Miniaturansicht eines [**PHOTOSAMPLE-**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).                                                                                                                                                                                  |
| [MFSampleExtension \_ PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md)                    | Enthält den [**FORMATSMediaType,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) der den Bildformattyp beschreibt, der im [MFSampleExtension \_ PhotoThumbnail-Attribut](mfsampleextension-photothumbnail.md) enthalten ist.                                                      |
| [MFSampleExtension \_ PinholeCameraIntrinsics](mfsampleextension-pinholecameraintrinsics.md)                    | Die systeminternen Pinholekameras für das Beispiel.                                                                                                                                                                                                      |
| [**MFSampleExtension \_ RepeatFirstField**](mfsampleextension-repeatfirstfield-attribute.md)                    | Gibt an, ob das erste Feld in einem geschachtelten Frame wiederholt werden soll.                                                                                                                                                                                |
| [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md)                                          | Gibt die Begrenzungen des bereichs von Interesse an, der den Bereich des Frames angibt, der eine andere Qualität erfordert.                                                                                                                            |
| [**MFSampleExtension \_ SingleField**](mfsampleextension-singlefield-attribute.md)                              | Gibt an, ob ein Videobeispiel ein einzelnes Oder zwei überlappende Felder enthält.                                                                                                                                                                 |
| [MFSampleExtension \_ TargetGlobalLuminance](mfsampleextension-targetgloballuminance.md)                        | Der Wert in Nits, der die zielorientierte globale Hintergrundbeleuchtung für den zugeordneten Videoframe angibt.                                                                                                                                           |
| [**MFSampleExtension-Token \_**](mfsampleextension-token-attribute.md)                                          | Enthält einen Zeiger auf das Token, das für die [**ENMEDIASTREAM::RequestSample-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) bereitgestellt wurde.                                                                                                             |
| [MFSampleExtension \_ VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)                      | Gibt die Begrenzungen des bereichs von Interesse an, der den Bereich des Frames angibt, der eine andere Qualität erfordert.                                                                                                                            |
| [MFSampleExtension \_ VideoEncodeQP](mfsampleextension-videoencodeqp.md)                                        | Gibt den Quantisierungsparameter (QP) an, der zum Codieren eines Videobeispiels verwendet wurde.                                                                                                                                                                  |



 

Nicht jedes Medienbeispiel enthält jedes hier aufgeführte Attribut. In einigen Fällen gilt ein Attribut nur für bestimmte Arten von Daten. Einige Attribute gelten beispielsweise nur für Videobeispiele und sollten nicht in Audiobeispielen angezeigt werden. In anderen Fällen verfügt das Attribut über einen Standardwert, der angewendet wird, wenn das Attribut nicht festgelegt ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**1000000000**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Media Foundation Attribute](media-foundation-attributes.md)
</dt> <dt>

[Medienbeispiele](media-samples.md)
</dt> </dl>

 

 



