---
title: Attributliste
description: Attributliste
ms.assetid: 81fc356e-ee7a-4630-841f-6c1543e022d3
keywords:
- Windows Medienformat-SDK, Attribute
- Advanced Systems Format (ASF), Attribute
- ASF (Advanced Systems Format), Attribute
- Attribute,Liste von
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ad976956a57ff1a1ac65cc969fe55e79110557296f9ab0dcb46c69cc811af7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117656201"
---
# <a name="attribute-list"></a>Attributliste

Die in diesem SDK enthaltenen vordefinierten Attribute werden in der folgenden Tabelle alphabetisch dargestellt. Jedes Attribut verfügt über einen Namen, einen globalen Bezeichner und einen Datentyp, wie vom entsprechenden Member der [**WMT \_ ATTR \_ DATATYPE-Enumeration**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) definiert. Einige Attribute verwenden keinen einfachen Datentyp oder werden entsprechend einer -Struktur formatiert. Einträge für diese Attribute listen einen Strukturnamen in der Datentypspalte mit dem Datentyp auf, der zum Festlegen des Werts in Klammern verwendet wird.

> [!Note]  
> Eine [Tabelle aller DRM-bezogenen](drm-attribute-list.md) Attribute finden Sie unter DRM-Attributliste.

 

Wenn Sie mit diesen Attributen programmieren, sollten Sie den globalen Bezeichner verwenden, anstatt den Namen als Zeichenfolgenliteral zu verwenden. Bei Verwendung des globalen Bezeichners führen typografische Fehler zur Kompilierzeit zu einem Fehler.



| Attributname                                                                       | Globaler Bezeichner                             | Datentyp                                            |
|--------------------------------------------------------------------------------------|-----------------------------------------------|------------------------------------------------------|
| [**ASFLeakyBucketPairs**](asfleakybucketpairs.md)                                   | g \_ wszASFLeakyBucketPairs                     | **\_WMT-TYP \_ BINARY**                                |
| [**AspectRatioX**](aspectratiox.md)                                                 | g \_ wszWMAspectRatioX                          | **WMT \_ TYPE \_ DWORD**                                 |
| [**AspectRatioy**](aspectratioy.md)                                                 | g \_ wszWMAspectRatioY                          | **WMT \_ TYPE \_ DWORD**                                 |
| [**Autor**](author.md)                                                             | g \_ wszWMAuthor                                | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**AverageLevel**](averagelevel.md)                                                 | g \_ wszAverageLevel                            | **WMT \_ TYPE \_ DWORD**                                 |
| [**BannerImageData**](bannerimagedata.md)                                           | g \_ wszWMBannerImageData                       | **\_WMT-TYP \_ BINARY**                                |
| [**BannerImageType**](bannerimagetype.md)                                           | g \_ wszWMBannerImageType                       | **WMT \_ TYPE \_ DWORD**                                 |
| [**BannerImageURL**](bannerimageurl.md)                                             | g \_ wszWMBannerImageURL                        | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**Bitrate**](bit-rate.md)                                                          | g \_ wszWMBitrate                               | **WMT \_ TYPE \_ DWORD**                                 |
| [**Übertragen**](broadcast.md)                                                       | g \_ wszWMBroadcast                             | **\_WMT-TYP \_ BOOL**                                  |
| [**BufferAverage**](bufferaverage.md)                                               | g \_ wszBufferAverage                           | **WMT \_ TYPE \_ DWORD**                                 |
| [**Kann \_ rückwärts überspringen \_**](can-skip-backward.md)                                     | g \_ wszWMSkipBackward                          | **\_WMT-TYP \_ BOOL**                                  |
| [**Kann \_ Vorwärts überspringen \_**](can-skip-forward.md)                                       | g \_ wszWMSkipForward                           | **\_WMT-TYP \_ BOOL**                                  |
| [**Copyright**](copyright.md)                                                       | g \_ wszWMCopyright                             | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**CopyrightURL**](copyrighturl.md)                                                 | g \_ wszWMCopyrightURL                          | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**CurrentBitrate**](currentbitrate.md)                                             | g \_ wszWMCurrentBitrate                        | **WMT \_ TYPE \_ DWORD**                                 |
| [**Beschreibung**](description.md)                                                   | g \_ wszWMDescription                           | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**DRM \_ ContentID**](drm-contentid.md)                                              | g \_ wszWMDRM \_ ContentID                        | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**DRM \_ DRMHeader \_ ContentDistributor**](drm-drmheader-contentdistributor.md)       | g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor    | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**DRM \_ DRMHeader \_ ContentID**](drm-drmheader-contentid.md)                         | g \_ wszWMDRM \_ DRMHeader \_ ContentID             | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**DRM \_ DRMHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md) | g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**DRM \_ DRMHeader \_ KeyID**](drm-drmheader-keyid.md)                                 | g \_ wszWMDRM \_ DRMHeader \_ KeyID                 | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**DRM \_ DRMHeader \_ LicenseAcqURL**](drm-drmheader-licenseacqurl.md)                 | g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL         | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**DRM \_ DRMHeader \_ SubscriptionContentID**](drm-drmheader-subscriptioncontentid.md) | g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**DRM \_ DRMHeader**](drm-drmheader.md)                                              | g \_ wszWMDRM \_ DRMHeader                        | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**DRM \_ IndividualizedVersion**](drm-individualizedversion.md)                      | g \_ wszWMDRM \_ IndividualizedVersion            | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**\_DRM-Schlüssel-ID**](drm-keyid.md)                                                      | g \_ wszWMDRM \_ KeyID                            | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**DRM \_ LASignatureCert**](drm-lasignaturecert.md)                                  | g \_ wszWMDRM \_ LASignatureCert                  | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**DRM \_ LASignatureLicSrvCert**](drm-lasignaturelicsrvcert.md)                      | g \_ wszWMDRM \_ LASignatureLicSrvCert            | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**DRM \_ LASignaturePrivKey**](drm-lasignatureprivkey.md)                            | g \_ wszWMDRM \_ LASignaturePrivKey               | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**DRM \_ LASignatureRootCert**](drm-lasignaturerootcert.md)                          | g \_ wszWMDRM \_ LASignatureRootCert              | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**\_DRM-LizenzAcqURL**](drm-licenseacqurl.md)                                      | g \_ wszWMDRM \_ LicenseAcqURL                    | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**\_DRM-Lizenz-ID**](drm-licenseid.md)                                              | g \_ wszWMDRM \_ LicenseID                        | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**\_DRM-Quell-ID**](drm-sourceid.md)                                                | g \_ wszWMDRM \_ SourceID                         | **\_WMT-TYP \_ DWORD**                                 |
| [**DRM \_ V1LicenseAcqURL**](drm-v1licenseacqurl.md)                                  | g \_ wszWMDRM \_ V1LicenseAcqURL                  | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**Dauer**](duration.md)                                                         | g \_ wszWMDuration                              | **\_WMT-TYP \_ QWORD**                                 |
| [**FileSize**](filesize.md)                                                         | g \_ wszWMFileSize                              | **\_WMT-TYP \_ QWORD**                                 |
| [**HasArbitraryDataStream**](hasarbitrarydatastream.md)                             | g \_ wszWMHasArbitraryDataStream                | **\_WMT-TYP \_ BOOL**                                  |
| [**HasAttachedImages**](hasattachedimages.md)                                       | g \_ wszWMHasAttachedImages                     | **\_WMT-TYP \_ BOOL**                                  |
| [**HasAudio**](hasaudio.md)                                                         | g \_ wszWMHasAudio                              | **\_WMT-TYP \_ BOOL**                                  |
| [**HasFileTransferStream**](hasfiletransferstream.md)                               | g \_ wszWMHasFileTransferStream                 | **\_WMT-TYP \_ BOOL**                                  |
| [**HasImage**](hasimage.md)                                                         | g \_ wszWMHasImage                              | **\_WMT-TYP \_ BOOL**                                  |
| [**HasScript**](hasscript.md)                                                       | g \_ wszWMHasScript                             | **\_WMT-TYP \_ BOOL**                                  |
| [**HasVideo**](hasvideo.md)                                                         | g \_ wszWMHasVideo                              | **\_WMT-TYP \_ BOOL**                                  |
| [**Ist \_ geschützt**](is-protected.md)                                                | g \_ wszWMProtected                             | **\_WMT-TYP \_ BOOL**                                  |
| [**Ist \_ vertrauenswürdig**](is-trusted.md)                                                    | g \_ wszWMTrusted                               | **\_WMT-TYP \_ BOOL**                                  |
| [**Isan**](isan.md)                                                                 | g \_ wszUNEN                                    | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**IsVBR**](isvbr.md)                                                               | g \_ wszWMIsVBR                                 | **\_WMT-TYP \_ BOOL**                                  |
| [**\_NSC-Adresse**](nsc-address.md)                                                  | g \_ wszWMNSCAddress                            | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**\_NSC-Beschreibung**](nsc-description.md)                                          | g \_ wszWMNSCDescription                        | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**\_NSC-E-Mail**](nsc-email.md)                                                      | g \_ wszWMNSCEmail                              | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**\_NSC-Name**](nsc-name.md)                                                        | g \_ wszWMNSCName                               | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**\_NSC-Telefon**](nsc-phone.md)                                                      | g \_ wszWMNSCPhone                              | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**NumberOfFrames**](numberofframes.md)                                             | g \_ wszWMNumberOfFrames                        | **\_WMT-TYP \_ QWORD**                                 |
| [**OptimalBitrate**](optimalbitrate.md)                                             | g \_ wszWMOptimalBitrate                        | **\_WMT-TYP \_ DWORD**                                 |
| [**PeakValue**](peakvalue.md)                                                       | g \_ wszPeakValue                               | **\_WMT-TYP \_ DWORD**                                 |
| [**Rating**](rating.md)                                                             | g \_ wszWMRating                                | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**Seekable**](seekable.md)                                                         | g \_ wszWMSeekable                              | **\_WMT-TYP \_ BOOL**                                  |
| [**\_Signaturname**](signature-name.md)                                            | g \_ wszWMSignature \_ Name                       | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**Stridable**](stridable.md)                                                       | g \_ wszWMStridable                             | **\_WMT-TYP \_ BOOL**                                  |
| [**Titel**](title.md)                                                               | g \_ wszWMTitle                                 | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**VBRPeak**](vbrpeak.md)                                                           | g \_ wszVBRPeak                                 | **\_WMT-TYP \_ DWORD**                                 |
| [**WM/AlbumArtist**](wm-albumartist.md)                                             | g \_ wszWMMeldungArtist                           | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/AlbumCoverURL**](wm-albumcoverurl.md)                                         | g \_ wszWMCoverURL                         | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/AlbumTitle**](wm-albumtitle.md)                                               | g \_ wszWMIedtitle                            | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/ASFPacketCount**](wm-asfpacketcount.md)                                       | g \_ wszWMASFPacketCount                        | **\_WMT-TYP \_ QWORD**                                 |
| [**WM/ASFSecurityObjectsSize**](wm-asfsecurityobjectssize.md)                       | g \_ wszWMASFSecurityObjectsSize                | **\_WMT-TYP \_ QWORD**                                 |
| [**WM/AudioFileURL**](wm-audiofileurl.md)                                           | g \_ wszWMAudioFileURL                          | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/AudioSourceURL**](wm-audiosourceurl.md)                                       | g \_ wszWMAudioSourceURL                        | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/AuthorURL**](wm-authorurl.md)                                                 | g \_ wszWMAuthorURL                             | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/BeatsPerMinute**](wm-beatsperminute.md)                                       | g \_ wszWMBeatsPerMinute                        | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/Kategorie**](wm-category.md)                                                   | g \_ wszWMCategory                              | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/Codec**](wm-codec.md)                                                         | g \_ wszWMCodec                                 | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/Composer**](wm-composer.md)                                                   | g \_ wszWMComposer                              | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/Enumer**](wm-conductor.md)                                                 | g \_ wszWMConductor                             | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/ContainerFormat**](wm-containerformat.md)                                     | g \_ wszWMContainerFormat                       | **WMT \_ \_SPEICHERFORMAT** (**\_ WMT-TYP \_ BINARY**)     |
| [**WM/ContentDistributor**](wm-contentdistributor.md)                               | g \_ wszWMContentDistributor                    | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/ContentGroupDescription**](wm-contentgroupdescription.md)                     | g \_ wszWMContentGroupDescription               | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/Director**](wm-director.md)                                                   | g \_ wszWMDirector                              | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/DRM**](wm-drm.md)                                                             | g \_ wszWMDRM                                   | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/DVDID**](wm-dvdid.md)                                                         | g \_ wszWMDVDID                                 | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/EncodedBy**](wm-encodedby.md)                                                 | g \_ wszWMEncodedBy                             | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/EncodingSettings**](wm-encodingsettings.md)                                   | g \_ wszWMEncodingSettings                      | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/EncodingTime**](wm-encodingtime.md)                                           | g \_ wszWMEncodingTime                          | **FILETIME** (**\_ WMT-TYP \_ QWORD**)                  |
| [**WM/Genre**](wm-genre.md)                                                         | g \_ wszWMGenre                                 | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/GenreID**](wm-genreid.md)                                                     | g \_ wszWMGenreID                               | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/InitialKey**](wm-initialkey.md)                                               | g \_ wszWMInitialKey                            | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/ISRC**](wm-isrc.md)                                                           | g \_ wszWMISRC                                  | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/Sprache**](wm-language.md)                                                   | g \_ wszWMLanguage                              | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/Wms**](wm-lyrics.md)                                                       | g \_ wszWMLyrics                                | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/Synchronisierte Wm/Wm-Synchronisierung \_**](wm-lyrics-synchronised.md)                            | g \_ wszWMLyrics \_ Synchronisiert                  | **WM \_ SYNCHRONISIERTE \_ MENTS** (**\_ WMT-TYP \_ BINARY**) |
| [**WM/MCDI**](wm-mcdi.md)                                                           | g \_ wszWMMCDI                                  | **\_WMT-TYP \_ BINARY**                                |
| [**WM/MediaClassPrimaryID**](wm-mediaprimaryid.md)                                  | g \_ wszWMMediaClassPrimaryID                   | **\_ \_ WMT-TYP-GUID**                                  |
| [**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)                              | g \_ wszWMMediaClassSecondaryID                 | **\_ \_ WMT-TYP-GUID**                                  |
| [**WM/MediaCredits**](wm-mediacredits.md)                                           | g \_ wszWMMediaCredits                          | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/MediaIsDelay**](wm-mediaisdelay.md)                                           | g \_ wszWMMediaIsDelay                          | **\_WMT-TYP \_ BOOL**                                  |
| [**WM/MediaIsFinale**](wm-mediaisfinale.md)                                         | g \_ wszWMMediaIsFinale                         | **\_WMT-TYP \_ BOOL**                                  |
| [**WM/MediaIsLive**](wm-mediaislive.md)                                             | g \_ wszWMMediaIsLive                           | **\_WMT-TYP \_ BOOL**                                  |
| [**WM/MediaIsPremiere**](wm-mediaispremiere.md)                                     | g \_ wszWMMediaIsPremiere                       | **\_WMT-TYP \_ BOOL**                                  |
| [**WM/MediaIsRepeat**](wm-mediaisrepeat.md)                                         | g \_ wszWMMediaIsRepeat                         | **\_WMT-TYP \_ BOOL**                                  |
| [**WM/MediaIsSAP**](wm-mediaissap.md)                                               | g \_ wszWMMediaIsSAP                            | **\_WMT-TYP \_ BOOL**                                  |
| [**WM/MediaIsStereo**](wm-mediaisstereo.md)                                         | g \_ wszWMMediaIsStereo                         | **\_WMT-TYP \_ BOOL**                                  |
| [**WM/MediaIsSubtitled**](wm-mediaissubtitled.md)                                   | g \_ wszWMMediaIsSubtitled                      | **\_WMT-TYP \_ BOOL**                                  |
| [**WM/MediaIsTape**](wm-mediaistape.md)                                             | g \_ wszWMMediaIsTape                           | **\_WMT-TYP \_ BOOL**                                  |
| [**WM/MediaNetworkAffiliation**](wm-medianetworkaffiliation.md)                     | g \_ wszWMMediaNetworkAffiliation               | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/MediaOriginalBroadcastDateTime**](wm-mediaoriginalbroadcastdatetime.md)       | g \_ wszWMMediaOriginalBroadcastDateTime        | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/MediaOriginalChannel**](wm-mediaoriginalchannel.md)                           | g \_ wszWMMediaOriginalChannel                  | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/MediaStationCallSign**](wm-mediastationcallsign.md)                           | g \_ wszWMMediaStationCallSign                  | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/MediaStationName**](wm-mediastationname.md)                                   | g \_ wszWMMediaStationName                      | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/ModifiedBy**](wm-modifiedby.md)                                               | g \_ wszWMModifiedBy                            | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/Stimmung**](wm-mood.md)                                                           | g \_ wszWMMood                                  | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/OriginalIedTitle**](wm-originalalbumtitle.md)                               | g \_ wszWMOriginalIedTitle                    | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/OriginalArtist**](wm-originalartist.md)                                       | g \_ wszWMOriginalArtist                        | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/OriginalFilename**](wm-originalfilename.md)                                   | g \_ wszWMOriginalFilename                      | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/OriginalLyricist**](wm-originallyricist.md)                                   | g \_ wszWMOriginalLyricist                      | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/OriginalReleaseTime**](wm-originalreleasetime.md)                             | g \_ wszWMOriginalReleaseTime                   | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/OriginalReleaseYear**](wm-originalreleaseyear.md)                             | g \_ wszWMOriginalReleaseYear                   | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/ParentalRating**](wm-parentalrating.md)                                       | g \_ wszWMParentalRating                        | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/ParentalRatingReason**](wm-parentalratingreason.md)                           | g \_ wszWMParentalRatingReason                  | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/PartOfSet**](wm-partofset.md)                                                 | g \_ wszWMPartOfSet                             | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/PeakBitrate**](wm-peakbitrate.md)                                             | g \_ wszWMPeakBitrate                           | **\_WMT-TYP \_ DWORD**                                 |
| [**WM/Zeitraum**](wm-period.md)                                                       | g \_ wszWMPeriod                                | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/Bild**](/windows/desktop/wmformat/wmpicture)                                      | g \_ wszWMPicture                               | **WM \_ PICTURE** (**WMT \_ TYPE \_ BINARY**)              |
| [**WM/PlaylistDelay**](wm-playlistdelay.md)                                         | g \_ wszWMPlaylistDelay                         | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/Producer**](wm-producer.md)                                                   | g \_ wszWMProducer                              | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/PromotionURL**](wm-promotionurl.md)                                           | g \_ wszWMPromotionURL                          | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/ProtectionType**](wm-protectiontype.md)                                       | g \_ wszWMProtectionType                        | **\_ \_ WMT-TYPZEICHENFOLGE**                                |
| [**WM/Anbieter**](wm-provider.md)                                                   | g \_ wszWMProvider                              | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/ProviderCopyright**](wm-providercopyright.md)                                 | g \_ wszWMProviderCopyright                     | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/ProviderRating**](wm-providerrating.md)                                       | g \_ wszWMProviderRating                        | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/ProviderStyle**](wm-providerstyle.md)                                         | g \_ wszWMProviderStyle                         | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/Publisher**](wm-publisher.md)                                                 | g \_ wszWMPublisher                             | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/RadioStationName**](wm-radiostationname.md)                                   | g \_ wszWM WorkstationName                      | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/RadioStationOwner**](wm-radiostationowner.md)                                 | g \_ wszWM WorkstationOwner                     | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/SharedUserRating**](wm-shareduserrating.md)                                   | g \_ wszWMSharedUserRating                      | **WMT \_ TYPE \_ DWORD**                                 |
| [**WM/StreamTypeInfo**](wm-streamtypeinfo.md)                                       | g \_ wszWMStreamTypeInfo                        | **WM \_ STREAM \_ TYPE \_ INFO** (**WMT TYPE \_ \_ BINARY**)   |
| [**WM/SubscriptionContentID**](wm-subscriptioncontentid.md)                         | g \_ wszWMSubscriptionContentID                 | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/Untertitel**](wm-subtitle.md)                                                   | g \_ wszWMSubTitle                              | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/SubTitleDescription**](wm-subtitledescription.md)                             | g \_ wszWMSubTitleDescription                   | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/Text**](wm-text.md)                                                           | g \_ wszWMText                                  | **WM \_ \_BENUTZERTEXT** (**\_ WMT-TYP \_ BINARY**)           |
| [**WM/ToolName**](wm-toolname.md)                                                   | g \_ wszWMToolName                              | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/ToolVersion**](wm-toolversion.md)                                             | g \_ wszWMToolVersion                           | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/Track**](wm-track.md)                                                         | g \_ wszWMTrack                                 | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/TrackNumber**](wm-tracknumber.md)                                             | g \_ wszWMTrackNumber                           | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/UniqueFileIdentifier**](wm-uniquefileidentifier.md)                           | g \_ wszWMUniqueFileIdentifier                  | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/UserWebURL**](wm-userweburl.md)                                               | g \_ wszWMUserWebURL                            | **WM \_ \_ \_ BENUTZER-WEB-URL** (**BINÄRER \_ WMT-TYP \_**)       |
| [**WM/VideoClosedCaptioning**](wm-videoclosedcaptioning.md)                         | g \_ wszWMVideoClosedCaptioning                 | **\_WMT-TYP \_ BOOL**                                  |
| [**WM/VideoFrameRate**](wm-videoframerate.md)                                       | g \_ wszWMVideoFrameRate                        | **WMT \_ TYPE \_ DWORD**                                 |
| [**WM/VideoHeight**](wm-videoheight.md)                                             | g \_ wszWMVideoHeight                           | **WMT \_ TYPE \_ DWORD**                                 |
| [**WM/VideoWidth**](wm-videowidth.md)                                               | g \_ wszWMVideoWidth                            | **WMT \_ TYPE \_ DWORD**                                 |
| [**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)                       | g \_ wszWMWMADRCAverageReference                | **WMT \_ TYPE \_ DWORD**                                 |
| [**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)                             | g \_ wszWMWMADRCAverageTarget                   | **WMT \_ TYPE \_ DWORD**                                 |
| [**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)                             | g \_ wszWMWMADRCPeakReference                   | **WMT \_ TYPE \_ DWORD**                                 |
| [**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)                                   | g \_ wszWMWMADRCPeakTarget                      | **WMT \_ TYPE \_ DWORD**                                 |
| [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md)                             | g \_ wszWMWMCollectionGroupID                   | **\_ \_ WMT-TYP-GUID**                                  |
| [**WM/WMCollectionID**](wm-wmcollectionid.md)                                       | g \_ wszWMWMCollectionID                        | **\_ \_ WMT-TYP-GUID**                                  |
| [**WM/WMContentID**](wm-wmcontentid.md)                                             | g \_ wszWMWMContentID                           | **\_ \_ WMT-TYP-GUID**                                  |
| [**WM/WMShadowFileSourceDRMType**](wm-wmshadowfilesourcedrmtype.md)                 | g \_ wszWMWMShadowFileSourceDRMType             | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/WMShadowFileSourceFileType**](wm-wmshadowfilesourcefiletype.md)               | g \_ wszWMWMShadowFileSourceFileType            | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/Writer**](wm-writer.md)                                                       | g \_ wszWMWriter                                | **\_WMT-TYPZEICHENFOLGE \_**                                |
| [**WM/Jahr**](wm-year.md)                                                           | g \_ wszWMYear                                  | **\_WMT-TYPZEICHENFOLGE \_**                                |



 

## <a name="remarks"></a>Hinweise

Die folgenden Konstanten werden mit den Attributen definiert. Jedes Attribut gibt die Anzahl eines bestimmten Attributtyps an. Sie müssen diese Werte nicht für etwas in Ihren Anwendungen verwenden.



| Konstante                 | Wert |
|--------------------------|-------|
| g \_ dwWMSpecialAttributes | 20    |
| g \_ dwWMContentAttributes | 5     |
| g \_ dwWMNSCAttributes     | 5     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Attribute**](attributes.md)
</dt> </dl>

 

 