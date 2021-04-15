---
title: Attributliste
description: Attributliste
ms.assetid: 81fc356e-ee7a-4630-841f-6c1543e022d3
keywords:
- Windows Media-Format-SDK, Attribute
- Advanced Systems Format (ASF), Attribute
- ASF (Advanced Systems Format), Attribute
- Attribute, Liste von
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793c0a860f6f9e40257bb6aec610dc7680b34538
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516799"
---
# <a name="attribute-list"></a>Attributliste

Die in diesem SDK enthaltenen vordefinierten Attribute werden in der folgenden Tabelle alphabetisch dargestellt. Jedes Attribut verfügt über einen Namen, einen globalen Bezeichner und einen Datentyp, der vom entsprechenden Member der [**WMT \_ attr \_ DataType**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) -Enumeration definiert wird. Einige Attribute verwenden keinen einfachen Datentyp oder werden entsprechend einer Struktur formatiert. Einträge für diese Attribute listet einen Struktur Namen in der Spalte Datentyp mit dem Datentyp auf, mit dem der Wert in Klammern festgelegt wird.

> [!Note]  
> Eine Tabelle aller DRM-bezogenen Attribute finden Sie in der [Liste der DRM-Attribute](drm-attribute-list.md) .

 

Wenn Sie mit diesen Attributen programmieren, sollten Sie den globalen Bezeichner verwenden, anstatt den Namen als Zeichenfolgenliteralzeichen zu verwenden. Durch die Verwendung des globalen Bezeichners führt jede typografische Fehler zur Kompilierzeit zu einem Fehler.



| Attributname                                                                       | Globaler Bezeichner                             | Datentyp                                            |
|--------------------------------------------------------------------------------------|-----------------------------------------------|------------------------------------------------------|
| [**Asfleakybucketpair**](asfleakybucketpairs.md)                                   | g \_ wszasfleakybucketpairs                     | **WMT \_ - \_ typbinär Datei**                                |
| [**Aspectratiox**](aspectratiox.md)                                                 | g \_ wszwmaspectratiox                          | **WMT- \_ Typ \_ DWORD**                                 |
| [**Aspectratioy**](aspectratioy.md)                                                 | g \_ wszwmaspectratioy                          | **WMT- \_ Typ \_ DWORD**                                 |
| [**Autor**](author.md)                                                             | g \_ wszwmauthor                                | **WMT \_ - \_ Typzeichenfolge**                                |
| [**Averagelevel**](averagelevel.md)                                                 | g \_ wszaveragelevel                            | **WMT- \_ Typ \_ DWORD**                                 |
| [**Bannerimagedata**](bannerimagedata.md)                                           | g \_ wszwmbannerimagedata                       | **WMT \_ - \_ typbinär Datei**                                |
| [**Bannerimagetype**](bannerimagetype.md)                                           | g \_ wszwmbannerimagetype                       | **WMT- \_ Typ \_ DWORD**                                 |
| [**Bannerimageurl**](bannerimageurl.md)                                             | g \_ wszwmbannerimageurl                        | **WMT \_ - \_ Typzeichenfolge**                                |
| [**Bitrate**](bit-rate.md)                                                          | g \_ wszwmbitrate                               | **WMT- \_ Typ \_ DWORD**                                 |
| [**Übertragen**](broadcast.md)                                                       | g \_ wszwmbroadcast                             | **WMT- \_ Typ \_ bool**                                  |
| [**Bufferaverage**](bufferaverage.md)                                               | g \_ wszbufferaverage                           | **WMT- \_ Typ \_ DWORD**                                 |
| [**Kann \_ \_ rückwärts springen**](can-skip-backward.md)                                     | g \_ wszwmskiprückwärts                          | **WMT- \_ Typ \_ bool**                                  |
| [**Kann \_ \_ Vorwärts springen**](can-skip-forward.md)                                       | g \_ wszwmskipforward                           | **WMT- \_ Typ \_ bool**                                  |
| [**Copyright**](copyright.md)                                                       | g \_ wszwmcopyright                             | **WMT \_ - \_ Typzeichenfolge**                                |
| [**Copyrighturl**](copyrighturl.md)                                                 | g \_ wszwmcopyrighturl                          | **WMT \_ - \_ Typzeichenfolge**                                |
| [**Currentbitrate**](currentbitrate.md)                                             | g \_ wszwmcurrentbitrate                        | **WMT- \_ Typ \_ DWORD**                                 |
| [**Beschreibung**](description.md)                                                   | g \_ wszwmdescription                           | **WMT \_ - \_ Typzeichenfolge**                                |
| [**DRM- \_ contentid**](drm-contentid.md)                                              | g \_ wszwmdrm- \_ contentid                        | **WMT \_ - \_ Typzeichenfolge**                                |
| [**DRM- \_ drmHeader- \_ contentdistributor**](drm-drmheader-contentdistributor.md)       | g \_ wszwmdrm \_ drmHeader- \_ contentdistributor    | **WMT \_ - \_ Typzeichenfolge**                                |
| [**DRM- \_ drmHeader- \_ contentid**](drm-drmheader-contentid.md)                         | g \_ wszwmdrm \_ drmHeader \_ contentid             | **WMT \_ - \_ Typzeichenfolge**                                |
| [**DRM \_ drmHeader \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md) | g \_ wszwmdrm \_ drmHeader \_ IndividualizedVersion | **WMT \_ - \_ Typzeichenfolge**                                |
| [**DRM- \_ drmHeader- \_ keyid**](drm-drmheader-keyid.md)                                 | g \_ wszwmdrm \_ drmHeader- \_ keyid                 | **WMT \_ - \_ Typzeichenfolge**                                |
| [**DRM \_ drmHeader \_ licenanacqurl**](drm-drmheader-licenseacqurl.md)                 | g \_ wszwmdrm \_ drmHeader \_ licengacqurl         | **WMT \_ - \_ Typzeichenfolge**                                |
| [**DRM- \_ drmHeader- \_ abonnemencontentid**](drm-drmheader-subscriptioncontentid.md) | g \_ wszwmdrm \_ drmHeader \_ abonnemencontentid | **WMT \_ - \_ Typzeichenfolge**                                |
| [**DRM- \_ drmHeader**](drm-drmheader.md)                                              | g \_ wszwmdrm \_ drmHeader                        | **WMT \_ - \_ Typzeichenfolge**                                |
| [**DRM- \_ IndividualizedVersion**](drm-individualizedversion.md)                      | g \_ wszwmdrm \_ IndividualizedVersion            | **WMT \_ - \_ Typzeichenfolge**                                |
| [**DRM- \_ Schlüssel-ID**](drm-keyid.md)                                                      | Schlüssel-ID für g \_ wszwmdrm \_                            | **WMT \_ - \_ Typzeichenfolge**                                |
| [**DRM- \_ lasignaturecert**](drm-lasignaturecert.md)                                  | g \_ wszwmdrm \_ lasignaturecert                  | **WMT \_ - \_ Typzeichenfolge**                                |
| [**DRM \_ lasignaturelicsrvcert**](drm-lasignaturelicsrvcert.md)                      | g \_ wszwmdrm \_ lasignaturelicsrvcert            | **WMT \_ - \_ Typzeichenfolge**                                |
| [**DRM- \_ lasignatureprivkey**](drm-lasignatureprivkey.md)                            | g \_ wszwmdrm \_ lasignatureprivkey               | **WMT \_ - \_ Typzeichenfolge**                                |
| [**DRM \_ lasignaturerootcert**](drm-lasignaturerootcert.md)                          | g \_ wszwmdrm \_ lasignaturerootcert              | **WMT \_ - \_ Typzeichenfolge**                                |
| [**DRM- \_ Lizenz-AcqURL**](drm-licenseacqurl.md)                                      | "g \_ wszwmdrm \_ licenanacqurl"                    | **WMT \_ - \_ Typzeichenfolge**                                |
| [**DRM- \_ Lizenz seid**](drm-licenseid.md)                                              | g \_ wszwmdrm \_ licenseid                        | **WMT \_ - \_ Typzeichenfolge**                                |
| [**DRM \_ -SourceID**](drm-sourceid.md)                                                | g \_ wszwmdrm \_ SourceID                         | **WMT- \_ Typ \_ DWORD**                                 |
| [**DRM- \_ V1LicenseAcqURL**](drm-v1licenseacqurl.md)                                  | g \_ wszwmdrm \_ V1LicenseAcqURL                  | **WMT \_ - \_ Typzeichenfolge**                                |
| [**Duration**](duration.md)                                                         | g \_ wszwmduration                              | **WMT- \_ Typ \_ QWORD**                                 |
| [**FileSize**](filesize.md)                                                         | g \_ wszwmfilesize                              | **WMT- \_ Typ \_ QWORD**                                 |
| [**Hasarbiarydatastream**](hasarbitrarydatastream.md)                             | g \_ wszwmhasschiedsrichter arydatastream                | **WMT- \_ Typ \_ bool**                                  |
| [**Hasattachedimages**](hasattachedimages.md)                                       | g \_ wszwmhasattachedimages                     | **WMT- \_ Typ \_ bool**                                  |
| [**Hasaudiodaten**](hasaudio.md)                                                         | g \_ wszwmhasaudiodatei                              | **WMT- \_ Typ \_ bool**                                  |
| [**Hasfiletransferstream**](hasfiletransferstream.md)                               | g \_ wszwmhasfiletransferstream                 | **WMT- \_ Typ \_ bool**                                  |
| [**Hasimage**](hasimage.md)                                                         | g \_ wszwmhasimage                              | **WMT- \_ Typ \_ bool**                                  |
| [**HasScript**](hasscript.md)                                                       | g \_ wszwmhasscript                             | **WMT- \_ Typ \_ bool**                                  |
| [**HasVideo**](hasvideo.md)                                                         | g \_ wszwmhasvideo                              | **WMT- \_ Typ \_ bool**                                  |
| [**Ist \_ geschützt**](is-protected.md)                                                | g \_ wszwmprotected                             | **WMT- \_ Typ \_ bool**                                  |
| [**Ist \_ vertrauenswürdig**](is-trusted.md)                                                    | g \_ wszwmtrusted                               | **WMT- \_ Typ \_ bool**                                  |
| [**ISAN**](isan.md)                                                                 | g \_ wszisan                                    | **WMT \_ - \_ Typzeichenfolge**                                |
| [**Isvbr**](isvbr.md)                                                               | g \_ wszwmisvbr                                 | **WMT- \_ Typ \_ bool**                                  |
| [**NSC- \_ Adresse**](nsc-address.md)                                                  | g \_ wszwmnscaddress                            | **WMT \_ - \_ Typzeichenfolge**                                |
| [**NSC- \_ Beschreibung**](nsc-description.md)                                          | g \_ wszwmnscdescription                        | **WMT \_ - \_ Typzeichenfolge**                                |
| [**NSC \_ -e-Mail**](nsc-email.md)                                                      | g \_ wszwmnscemail                              | **WMT \_ - \_ Typzeichenfolge**                                |
| [**NSC- \_ Name**](nsc-name.md)                                                        | g \_ wszwmnscname                               | **WMT \_ - \_ Typzeichenfolge**                                |
| [**NSC- \_ Telefon**](nsc-phone.md)                                                      | g \_ wszwmnscphone                              | **WMT \_ - \_ Typzeichenfolge**                                |
| [**NumberOfFrames**](numberofframes.md)                                             | g \_ wszwmnumofframes                        | **WMT- \_ Typ \_ QWORD**                                 |
| [**Optimalbitrate**](optimalbitrate.md)                                             | g \_ wszwmoptimalbitrate                        | **WMT- \_ Typ \_ DWORD**                                 |
| [**Peer Value**](peakvalue.md)                                                       | g \_ wszpeer Value                               | **WMT- \_ Typ \_ DWORD**                                 |
| [**Rating**](rating.md)                                                             | g \_ wszwmrating                                | **WMT \_ - \_ Typzeichenfolge**                                |
| [**Durchsuchbar**](seekable.md)                                                         | g \_ wszwmseekable                              | **WMT- \_ Typ \_ bool**                                  |
| [**Signatur \_ Name**](signature-name.md)                                            | g \_ wszwmsignature- \_ Name                       | **WMT \_ - \_ Typzeichenfolge**                                |
| [**Strigbar**](stridable.md)                                                       | g \_ wszwmstridable                             | **WMT- \_ Typ \_ bool**                                  |
| [**Titel**](title.md)                                                               | g \_ wszwmtitle                                 | **WMT \_ - \_ Typzeichenfolge**                                |
| [**Vbrpeak**](vbrpeak.md)                                                           | g \_ wszvbrpeak                                 | **WMT- \_ Typ \_ DWORD**                                 |
| [**WM/albumartist**](wm-albumartist.md)                                             | g \_ wszwmalbumartist                           | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/albumcoverurl**](wm-albumcoverurl.md)                                         | g \_ wszwmalbumcoverurl                         | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/albumtitle**](wm-albumtitle.md)                                               | g \_ wszwmalbumtitle                            | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/asfpacketcount**](wm-asfpacketcount.md)                                       | g \_ wszwmasf-Anzahl                        | **WMT- \_ Typ \_ QWORD**                                 |
| [**WM/asfsecurityobjectssize**](wm-asfsecurityobjectssize.md)                       | g \_ wszwmasf securityobjectssize                | **WMT- \_ Typ \_ QWORD**                                 |
| [**WM/audiofileurl**](wm-audiofileurl.md)                                           | g \_ wszwmaudiofileurl                          | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/audiosourceurl**](wm-audiosourceurl.md)                                       | g \_ wszwmaudiosourceurl                        | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/authorurl**](wm-authorurl.md)                                                 | g \_ wszwmauthorurl                             | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/beatsperminütlich**](wm-beatsperminute.md)                                       | g \_ wszwmbeatsperminute                        | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Kategorie**](wm-category.md)                                                   | g \_ wszwmcategory                              | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Codec**](wm-codec.md)                                                         | g \_ wszwmcodec                                 | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Composer**](wm-composer.md)                                                   | g \_ wszwmcomposer                              | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Dirigent**](wm-conductor.md)                                                 | g \_ wszwmconductor                             | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Containerformat**](wm-containerformat.md)                                     | g \_ wszwmcontainerformat                       | **WMT \_ Speicher \_ Format** (**WMT \_ - \_ typbinär Datei**)     |
| [**WM/contentdistributor**](wm-contentdistributor.md)                               | g \_ wszwmcontentdistributor                    | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/contentgroupdescription**](wm-contentgroupdescription.md)                     | g \_ wszwmcontentgroupdescription               | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Director**](wm-director.md)                                                   | g \_ wszwmdirector                              | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/DRM**](wm-drm.md)                                                             | g \_ wszwmdrm                                   | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/dvdid**](wm-dvdid.md)                                                         | g \_ wszwmdvdid                                 | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/encodby**](wm-encodedby.md)                                                 | g \_ wszwmencodedby                             | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/encodingsettings**](wm-encodingsettings.md)                                   | g \_ wszwmencodingsettings                      | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/encodingtime**](wm-encodingtime.md)                                           | g \_ wszwmencodingtime                          | **FILETIME** (**WMT- \_ Typ \_ QWORD**)                  |
| [**WM/Genre**](wm-genre.md)                                                         | g \_ wszwmgenre                                 | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/GenreID**](wm-genreid.md)                                                     | g \_ wszwmgenreid                               | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/initialkey**](wm-initialkey.md)                                               | g \_ wszwminitialkey                            | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/ISRC**](wm-isrc.md)                                                           | g \_ wszwmisrc                                  | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Sprache**](wm-language.md)                                                   | g \_ wszwmlanguage                              | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Liedtexte**](wm-lyrics.md)                                                       | g \_ wszwmlyrics                                | **WMT \_ - \_ Typzeichenfolge**                                |
| [**Synchronisierte WM/Liedtexte \_**](wm-lyrics-synchronised.md)                            | "g \_ wszwmlyrics" ( \_ synchron)                  | **WM \_ synchierte \_ Texte** (**WMT \_ - \_ typbinär Datei**) |
| [**WM/MCDI**](wm-mcdi.md)                                                           | g \_ wszwmmcdi                                  | **WMT \_ - \_ typbinär Datei**                                |
| [**WM/mediaclassprimaryid**](wm-mediaprimaryid.md)                                  | g \_ wszwmmediaclassprimaryid                   | **WMT- \_ Typ- \_ GUID**                                  |
| [**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)                              | g \_ wszwmmediaclasssecondaryid                 | **WMT- \_ Typ- \_ GUID**                                  |
| [**WM/mediacredits**](wm-mediacredits.md)                                           | g \_ wszwmmediacredits                          | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/mediaisdelay**](wm-mediaisdelay.md)                                           | g \_ wszwmmediaisdelay                          | **WMT- \_ Typ \_ bool**                                  |
| [**WM/mediaisfinal**](wm-mediaisfinale.md)                                         | g \_ wszwmmediaisfinal                         | **WMT- \_ Typ \_ bool**                                  |
| [**WM/mediaislive**](wm-mediaislive.md)                                             | g \_ wszwmmediaislive                           | **WMT- \_ Typ \_ bool**                                  |
| [**WM/mediaiische miere**](wm-mediaispremiere.md)                                     | g \_ wszwmmediaispree miere                       | **WMT- \_ Typ \_ bool**                                  |
| [**WM/mediaisrepeat**](wm-mediaisrepeat.md)                                         | g \_ wszwmmediaisrepeat                         | **WMT- \_ Typ \_ bool**                                  |
| [**WM/mediaissap**](wm-mediaissap.md)                                               | g \_ wszwmmediaissap                            | **WMT- \_ Typ \_ bool**                                  |
| [**WM/mediaisstereo**](wm-mediaisstereo.md)                                         | g \_ wszwmmediaisstereo                         | **WMT- \_ Typ \_ bool**                                  |
| [**WM/mediaissubtitel**](wm-mediaissubtitled.md)                                   | g \_ wszwmmediaissubtitel                      | **WMT- \_ Typ \_ bool**                                  |
| [**WM/mediaistape**](wm-mediaistape.md)                                             | g \_ wszwmmediaistape                           | **WMT- \_ Typ \_ bool**                                  |
| [**WM/medianetworkzugehörigkeit**](wm-medianetworkaffiliation.md)                     | g \_ wszwmmedianetworkzugehörigkeit               | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/mediaoriginalbroadcastdatetime**](wm-mediaoriginalbroadcastdatetime.md)       | g \_ wszwmmediaoriginalbroadcastdatetime        | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/mediaoriginalchannel**](wm-mediaoriginalchannel.md)                           | g \_ wszwmmediaoriginalchannel                  | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/mediastationcallsign**](wm-mediastationcallsign.md)                           | g \_ wszwmmediastationcallsign                  | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/mediastationname**](wm-mediastationname.md)                                   | g \_ wszwmmediastationname                      | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/ModifiedBy**](wm-modifiedby.md)                                               | g \_ wszwmmodifiedby                            | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Stimmung**](wm-mood.md)                                                           | g \_ wszwmmood                                  | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/originalalbumtitle**](wm-originalalbumtitle.md)                               | g \_ wszwmoriginalalbumtitle                    | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/originalartist**](wm-originalartist.md)                                       | g \_ wszwmoriginalartist                        | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/OriginalFileName**](wm-originalfilename.md)                                   | g \_ wszwmoriginalfilename                      | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/originallyriker**](wm-originallyricist.md)                                   | g \_ wszwmoriginallyriker                      | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/originalreleasetime**](wm-originalreleasetime.md)                             | g \_ wszwmoriginalreleasetime                   | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/originalreleaseyear**](wm-originalreleaseyear.md)                             | g \_ wszwmoriginalreleaseyear                   | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/parametrialbewertung**](wm-parentalrating.md)                                       | g \_ wszwmparametrialrating                        | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/parametrialratingreason**](wm-parentalratingreason.md)                           | g \_ wszwmpartalratingreason                  | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Element Satz**](wm-partofset.md)                                                 | g \_ wszwmparametset                             | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Peer-Bitrate**](wm-peakbitrate.md)                                             | g \_ wszwmpeakbitrate                           | **WMT- \_ Typ \_ DWORD**                                 |
| [**WM/Zeitraum**](wm-period.md)                                                       | g \_ wszwmperiod                                | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Bild**](/windows/desktop/wmformat/wmpicture)                                      | g \_ wszwmpicture                               | **WM \_ Bild** (**WMT \_ - \_ typbinär Datei**)              |
| [**WM/playlistdelay**](wm-playlistdelay.md)                                         | g \_ wszwmplaylistdelay                         | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Producer**](wm-producer.md)                                                   | g \_ wszwmproducer                              | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/promotionurl**](wm-promotionurl.md)                                           | g \_ wszwmpromotionurl                          | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Schutztyp**](wm-protectiontype.md)                                       | g \_ wszwmschutztype                        | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Anbieter**](wm-provider.md)                                                   | g \_ wszwmprovider                              | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/providercopyright**](wm-providercopyright.md)                                 | g \_ wszwmprovidercopyright                     | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/providerrating**](wm-providerrating.md)                                       | g \_ wszwmproviderrating                        | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/providerstyle**](wm-providerstyle.md)                                         | g \_ wszwmproviderstyle                         | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Verleger**](wm-publisher.md)                                                 | g \_ wszwmpublisher                             | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/radiostationname**](wm-radiostationname.md)                                   | g \_ wszwmradiostationname                      | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/radiostationowner**](wm-radiostationowner.md)                                 | g \_ wszwmradiostationowner                     | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/shareduserrating**](wm-shareduserrating.md)                                   | g \_ wszwmshareduserrating                      | **WMT- \_ Typ \_ DWORD**                                 |
| [**WM/streamtypeingangs Info**](wm-streamtypeinfo.md)                                       | g \_ wszwmstreamtypeingangs Info                        | **WM \_ \_Streamtyp \_ Info** (**WMT \_ - \_ typbinär Datei**)   |
| [**WM/Abonnement-ID**](wm-subscriptioncontentid.md)                         | g \_ wszwmabonnemencontentid                 | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Untertitel**](wm-subtitle.md)                                                   | g \_ wszwmuntertitel                              | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/subtitledescription**](wm-subtitledescription.md)                             | g \_ wszwmsubtitledescription                   | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Text**](wm-text.md)                                                           | g \_ wszwmtext                                  | **WM \_ Benutzer \_ Text** (**WMT \_ - \_ typbinär Datei**)           |
| [**WM/ToolName**](wm-toolname.md)                                                   | g \_ wszwmtoolname                              | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Toolversion**](wm-toolversion.md)                                             | g \_ wszwmtoolversion                           | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Nachverfolgung**](wm-track.md)                                                         | g \_ wszwmtrack                                 | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/tracknumber**](wm-tracknumber.md)                                             | g \_ wszwmtracknumber                           | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/UniqueFileIdentifier**](wm-uniquefileidentifier.md)                           | g \_ wszwmuniquefileidentifier                  | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/userweburl**](wm-userweburl.md)                                               | g \_ wszwmuserweburl                            | **WM \_ Benutzer- \_ Web- \_ URL** (**WMT- \_ \_ typbinär Datei**)       |
| [**WM/videoclosedbeschriftungen**](wm-videoclosedcaptioning.md)                         | g \_ wszwmvideoclosedcaption                 | **WMT- \_ Typ \_ bool**                                  |
| [**WM/Videoframerate**](wm-videoframerate.md)                                       | g \_ wszwmvideoframerate                        | **WMT- \_ Typ \_ DWORD**                                 |
| [**WM/videoheight**](wm-videoheight.md)                                             | g \_ wszwmvideoheight                           | **WMT- \_ Typ \_ DWORD**                                 |
| [**WM/videowidth**](wm-videowidth.md)                                               | g \_ wszwmvideowidth                            | **WMT- \_ Typ \_ DWORD**                                 |
| [**WM/wmadrcaveragereferenzierung**](wm-wmadrcaveragereference.md)                       | g \_ wszwmwmadrcaveragereferenzierung                | **WMT- \_ Typ \_ DWORD**                                 |
| [**WM/wmadrcaveragetarget**](wm-wmadrcaveragetarget.md)                             | g \_ wszwmwmadrcaveragetarget                   | **WMT- \_ Typ \_ DWORD**                                 |
| [**WM/wmadrcpeer Reference**](wm-wmadrcpeakreference.md)                             | g \_ wszwmwmadrcpeer Reference                   | **WMT- \_ Typ \_ DWORD**                                 |
| [**WM/wmadrcpeer Target**](wm-wmadrcpeaktarget.md)                                   | g \_ wszwmwmadrcpeer-Ziel                      | **WMT- \_ Typ \_ DWORD**                                 |
| [**WM/wmcollectiongroupid**](wm-wmcollectiongroupid.md)                             | g \_ wszwmwmcollectiongroupid                   | **WMT- \_ Typ- \_ GUID**                                  |
| [**WM/wmcollectionid**](wm-wmcollectionid.md)                                       | g \_ wszwmwmcollectionid                        | **WMT- \_ Typ- \_ GUID**                                  |
| [**WM/wmcontentid**](wm-wmcontentid.md)                                             | g \_ wszwmwmcontentid                           | **WMT- \_ Typ- \_ GUID**                                  |
| [**WM/wmshadowfilesourcedrmtype**](wm-wmshadowfilesourcedrmtype.md)                 | g \_ wszwmwmshadowfilesourcedrmtype             | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/wmshadowfilesourcefiletype**](wm-wmshadowfilesourcefiletype.md)               | g \_ wszwmwmshadowfilesourcefiletype            | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Writer**](wm-writer.md)                                                       | g \_ wszwmwriter                                | **WMT \_ - \_ Typzeichenfolge**                                |
| [**WM/Jahr**](wm-year.md)                                                           | g \_ wszwmyear                                  | **WMT \_ - \_ Typzeichenfolge**                                |



 

## <a name="remarks"></a>Bemerkungen

Die folgenden Konstanten werden mit den Attributen definiert. Jeder Wert gibt die Anzahl eines bestimmten Attribut Typs an. Sie müssen diese Werte für nichts in Ihren Anwendungen verwenden.



| Konstante                 | Wert |
|--------------------------|-------|
| g \_ dwwmspecialattribute | 20    |
| g \_ dwwmcontentattribute | 5     |
| g \_ dwwmnscattribute     | 5     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Attribute**](attributes.md)
</dt> </dl>

 

 