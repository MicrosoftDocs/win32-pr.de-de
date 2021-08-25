---
title: WMDM_FORMATCODE-Enumeration
description: Der WMDM \_ FORMATCODE-Enumerationstyp definiert eine Liste von Formatcodes, die Typen von Inhalten beschreiben, die an ein und von einem Gerät übertragen werden.
ms.assetid: 203d9bdf-cbbd-4d06-8292-26c8a472e2aa
keywords:
- WMDM_FORMATCODE-Enumerationsfenster Media Geräte-Manager
topic_type:
- apiref
api_name:
- WMDM_FORMATCODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b09a388926a0f5fc11e24fc17fe4693b710e04aa321202e9cf31890d60d6642
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862910"
---
# <a name="wmdm_formatcode-enumeration"></a>WMDM \_ FORMATCODE-Enumeration

Der **WMDM \_ FORMATCODE-Enumerationstyp** definiert eine Liste von Formatcodes, die Typen von Inhalten beschreiben, die an ein und von einem Gerät übertragen werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_FORMATCODE { 
  WMDM_FORMATCODE_NOTUSED,
  WMDM_FORMATCODE_ALLIMAGES,
  WMDM_FORMATCODE_UNDEFINED,
  WMDM_FORMATCODE_ASSOCIATION,
  WMDM_FORMATCODE_SCRIPT,
  WMDM_FORMATCODE_EXECUTABLE,
  WMDM_FORMATCODE_TEXT,
  WMDM_FORMATCODE_HTML,
  WMDM_FORMATCODE_DPOF,
  WMDM_FORMATCODE_AIFF,
  WMDM_FORMATCODE_WAVE,
  WMDM_FORMATCODE_MP3,
  WMDM_FORMATCODE_AVI,
  WMDM_FORMATCODE_MPEG,
  WMDM_FORMATCODE_ASF,
  WMDM_FORMATCODE_RESERVED_FIRST,
  WMDM_FORMATCODE_RESERVED_LAST,
  WMDM_FORMATCODE_IMAGE_UNDEFINED,
  WMDM_FORMATCODE_IMAGE_EXIF,
  WMDM_FORMATCODE_IMAGE_TIFFEP,
  WMDM_FORMATCODE_IMAGE_FLASHPIX,
  WMDM_FORMATCODE_IMAGE_BMP,
  WMDM_FORMATCODE_IMAGE_CIFF,
  WMDM_FORMATCODE_IMAGE_GIF,
  WMDM_FORMATCODE_IMAGE_JFIF,
  WMDM_FORMATCODE_IMAGE_PCD,
  WMDM_FORMATCODE_IMAGE_PICT,
  WMDM_FORMATCODE_IMAGE_PNG,
  WMDM_FORMATCODE_IMAGE_TIFF,
  WMDM_FORMATCODE_IMAGE_TIFFIT,
  WMDM_FORMATCODE_IMAGE_JP2,
  WMDM_FORMATCODE_IMAGE_JPX,
  WMDM_FORMATCODE_IMAGE_RESERVED_FIRST,
  WMDM_FORMATCODE_IMAGE_RESERVED_LAST,
  WMDM_FORMATCODE_UNDEFINEDFIRMWARE,
          WMDM_FORMATCODE_WBMP
,
                  WMDM_FORMATCODE_JPEGXR
,
  WMDM_FORMATCODE_WINDOWSIMAGEFORMAT,
  WMDM_FORMATCODE_UNDEFINEDAUDIO,
  WMDM_FORMATCODE_WMA,
  WMDM_FORMATCODE_OGG,
  WMDM_FORMATCODE_AAC,
  WMDM_FORMATCODE_AUDIBLE,
  WMDM_FORMATCODE_FLAC,
          WMDM_FORMATCODE_QCELP
,
          WMDM_FORMATCODE_AMR
,
  WMDM_FORMATCODE_UNDEFINEDVIDEO,
  WMDM_FORMATCODE_WMV,
  WMDM_FORMATCODE_MP4,
  WMDM_FORMATCODE_MP2,
          WMDM_FORMATCODE_3G2
,
                  WMDM_FORMATCODE_AVCHD
,
                  WMDM_FORMATCODE_ATSCTS
,
                          WMDM_FORMATCODE_DVBTS
,
  WMDM_FORMATCODE_UNDEFINEDCOLLECTION,
  WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM,
  WMDM_FORMATCODE_ABSTRACTIMAGEALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOALBUM,
  WMDM_FORMATCODE_ABSTRACTVIDEOALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST,
  WMDM_FORMATCODE_ABSTRACTCONTACTGROUP,
  WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER,
  WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION,
  WMDM_FORMATCODE_WPLPLAYLIST,
  WMDM_FORMATCODE_M3UPLAYLIST,
  WMDM_FORMATCODE_MPLPLAYLIST,
  WMDM_FORMATCODE_ASXPLAYLIST,
  WMDM_FORMATCODE_PLSPLAYLIST,
  WMDM_FORMATCODE_UNDEFINEDDOCUMENT,
  WMDM_FORMATCODE_ABSTRACTDOCUMENT,
  WMDM_FORMATCODE_XMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT,
  WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET,
  WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT,
  WMDM_FORMATCODE_UNDEFINEDMESSAGE,
  WMDM_FORMATCODE_ABSTRACTMESSAGE,
  WMDM_FORMATCODE_UNDEFINEDCONTACT,
  WMDM_FORMATCODE_ABSTRACTCONTACT,
  WMDM_FORMATCODE_VCARD2,
  WMDM_FORMATCODE_VCARD3,
  WMDM_FORMATCODE_UNDEFINEDCALENDARITEM,
  WMDM_FORMATCODE_ABSTRACTCALENDARITEM,
  WMDM_FORMATCODE_VCALENDAR1,
  WMDM_FORMATCODE_VCALENDAR2,
  WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE,
  WMDM_FORMATCODE_MEDIA_CAST,
  WMDM_FORMATCODE_SECTION,
                                  WMDM_FORMATCODE_3G2A

} WMDM_FORMATCODE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**\_WMDM-FORMATCODE \_ NOTUSED**
</dt> <dd>

Es wird kein Formatcode verwendet.

</dd> <dt>

<span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**\_WMDM-FORMATCODE \_ ALLIMAGES**
</dt> <dd>

Formatcode, der zum Abfragen aller Bilder verwendet werden kann.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**WMDM \_ FORMATCODE \_ UNDEFINED**
</dt> <dd>

Formatieren Sie Code, der zum Abfragen aller nicht definierten Objekte verwendet wird.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**WMDM \_ FORMATCODE \_ ASSOCIATION**
</dt> <dd>

Formatcode, der verwendet wird, um einen Link zwischen zwei -Objekten zu definieren.

</dd> <dt>

<span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**\_WMDM-FORMATCODESKRIPT \_**
</dt> <dd>

Formatieren von Code für eine Skriptdatei.

</dd> <dt>

<span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**WMDM \_ FORMATCODE \_ EXECUTABLE**
</dt> <dd>

Formatieren von Code für eine ausführbare Datei.

</dd> <dt>

<span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**\_WMDM-FORMATCODETEXT \_**
</dt> <dd>

Formatieren von Code für eine Textdatei.

</dd> <dt>

<span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**\_WMDM-FORMATCODE \_ HTML**
</dt> <dd>

Formatieren von Code für eine HTML-Datei.

</dd> <dt>

<span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**\_WMDM-FORMATCODE \_ DPOF**
</dt> <dd>

Formatcode, der verwendet wird, um das Format der digitalen Druckreihenfolge darzustellen.

</dd> <dt>

<span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM \_ FORMATCODE \_ AIFF**
</dt> <dd>

Formatcode, der zum Darstellen des Audioaustauschdateiformats verwendet wird.

</dd> <dt>

<span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**WMDM \_ FORMATCODE \_ WAVE**
</dt> <dd>

Formatcode, der für eine WAV-Datei verwendet wird.

</dd> <dt>

<span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**\_WMDM-FORMATCODE \_ MP3**
</dt> <dd>

Formatcode, der für eine MP3-Datei verwendet wird.

</dd> <dt>

<span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**WMDM \_ FORMATCODE \_ AVI**
</dt> <dd>

Formatcode, der für eine AVI-Datei verwendet wird.

</dd> <dt>

<span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**WMDM \_ FORMATCODE \_ MPEG**
</dt> <dd>

Formatcode, der für eine MPEG-Datei verwendet wird.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**WMDM \_ FORMATCODE \_ ASF**
</dt> <dd>

Formatcode, der verwendet wird, um eine ASF-Datei (Advanced Systems Format) darzustellen.

</dd> <dt>

<span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**WMDM \_ FORMATCODE \_ RESERVED \_ FIRST**
</dt> <dd>

Formatieren Sie Code, der der erste in einem Bereich ist, der für das Picture Transfer Protocol (PTP) reserviert ist.

</dd> <dt>

<span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**WMDM \_ FORMATCODE \_ RESERVED \_ LAST**
</dt> <dd>

Formatieren Sie Code, der sich zuletzt in einem für PTP reservierten Bereich befindet.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ UNDEFINED**
</dt> <dd>

Formatcode, der zum Darstellen und Darstellen eines nicht definierten Typs verwendet wird.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ EXIF**
</dt> <dd>

Formatcode für eine EXIF-Datei. Wird auch für JPEG-Bilder verwendet, die nicht von WMDM \_ FORMATCODE \_ IMAGE \_ JP2 oder WMDM \_ FORMATCODE IMAGE JPX abgedeckt \_ \_ werden.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ TIFFEP**
</dt> <dd>

Formatcode, der für Bilder vom Typ Tagged Image File Format für elektronische Fotos (TIFF/EP) verwendet wird

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**\_WMDM-FORMATCODEBILD \_ \_ FLASHPIX**
</dt> <dd>

Formatieren Sie Code für eine Datei vom Typ FPX.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ BMP**
</dt> <dd>

Formatcode für eine Datei vom Typ BMP.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ CIFF**
</dt> <dd>

Formatcode für ein Bild im Kamerabilddateiformat.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**\_WMDM-FORMATCODEBILD \_ \_ GIF**
</dt> <dd>

Formatieren von Code für eine GIF-Datei.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ JFIF**
</dt> <dd>

Formatieren Sie Code für eine Datei vom Typ JFIF.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ PCD**
</dt> <dd>

Formatcode für ein Bild vom Typ "photo cd".

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ PICT**
</dt> <dd>

Formatieren Sie Code für ein Bild vom Typ PICT.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**\_WMDM-FORMATCODEBILD \_ \_ PNG**
</dt> <dd>

Formatieren Sie Code für ein Bild vom Typ PNG.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ TIFF**
</dt> <dd>

Formatieren Sie Code für eine Datei vom Typ TIFF.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ TIFFIT**
</dt> <dd>

Formatieren Sie Code für ein Bild vom Typ Tagged Image File Format mit Bildtechnologie.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**\_WMDM-FORMATCODEBILD \_ \_ JP2**
</dt> <dd>

Formatcode für ein jpeg200-Bild.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**\_WMDM-FORMATCODEBILD \_ \_ JPX**
</dt> <dd>

Formatieren Sie Code für ein Bild, das auf JPEG200 basiert und die erweiterte Registrierung von Standbildern verwendet. Die Dateinamenerweiterung ist normalerweise .jpf oder .jpx.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ RESERVED \_ FIRST**
</dt> <dd>

Formatieren Sie Code, der der erste in einem Bereich ist, der für einen Bildverweis in PTP reserviert ist.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**WMDM \_ FORMATCODE \_ IMAGE \_ RESERVED \_ LAST**
</dt> <dd>

Formatieren Sie Code, der der letzte in einem Bereich ist, der für einen Bildverweis in PTP reserviert ist.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**\_WMDM-FORMATCODE \_ UNDEFINEDFIRMWARE**
</dt> <dd>

Formatieren Sie Code, wenn die Firmware nicht definiert ist.

</dd> <dt>

<span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span>**WMDM \_ FORMATCODE \_ WBMP** 
</dt> <dd>

Formatieren Sie Code für ein WBMP-Bild (Wireless Application Protocol Bitmap).

</dd> <dt>

<span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span>**WMDM \_ FORMATCODE \_ JPEGXR** 
</dt> <dd>

Formatieren von Code für ein HD-Fotobild

</dd> <dt>

<span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**\_WMDM-FORMATCODE \_ WINDOWSIMAGEFORMAT**
</dt> <dd>

Formatcode für Windows Bildformat.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**\_WMDM-FORMATCODE \_ UNDEFINEDAUDIO**
</dt> <dd>

Formatieren sie Code für eine Audiodatei vom typ "undefiniert".

</dd> <dt>

<span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**WMDM \_ FORMATCODE \_ WMA**
</dt> <dd>

Formatieren Sie Code für eine Windows-WMA-Datei (Media Audio).

</dd> <dt>

<span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**WMDM \_ FORMATCODE \_ OGG**
</dt> <dd>

Formatieren sie Code für eine Vorladungscodierte Audiodatei in einem Ogg-Container.

</dd> <dt>

<span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM \_ FORMATCODE \_ AAC**
</dt> <dd>

Formatieren von Code für eine AAC-Datei (Advanced Audio Coding).

</dd> <dt>

<span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**WMDM \_ FORMATCODE \_ AUDIOBLE**
</dt> <dd>

Formatieren von Code für eine Akustische Datei.

</dd> <dt>

<span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**WMDM \_ FORMATCODE \_ FLAC**
</dt> <dd>

Formatieren Sie Code für eine FLAC-Datei (Free Lossless Audio Codec).

</dd> <dt>

<span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span>**WMDM \_ FORMATCODE \_ QCELP** 
</dt> <dd>

Formatieren Sie Code für eine QCELP-Codecdatei (Qualcomm Code Excited Linear Prediction).

</dd> <dt>

<span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span>**WMDM \_ FORMATCODE \_ AMR** 
</dt> <dd>

Formatcode für eine ADAPTIVE AMR-Codecdatei (Multi-Rate Audio).

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO**
</dt> <dd>

Formatieren Sie Code für eine Videodatei mit einem nicht definierten Typ.

</dd> <dt>

<span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**WMDM \_ FORMATCODE \_ WMV**
</dt> <dd>

Formatieren Sie Code für eine Windows-Medienvideodatei (WMV).

</dd> <dt>

<span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**WMDM \_ FORMATCODE \_ MP4**
</dt> <dd>

Formatieren sie Code für eine MP4-Datei.

</dd> <dt>

<span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**WMDM \_ FORMATCODE \_ MP2**
</dt> <dd>

Formatieren sie Code für eine MP2-Datei.

</dd> <dt>

<span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span>**WMDM \_ FORMATCODE \_ 3G2** 
</dt> <dd>

Formatcode für ein 3G2-Multimediacontainerformat (3GPP2). Eine Datei dieses Typs kann Audio, Video oder Text enthalten.

</dd> <dt>

<span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span>**WMDM \_ FORMATCODE \_ AVCHD** 
</dt> <dd>

Formatcode für eine AVCHD-Videodatei (Advanced Video Coding High Definition).

</dd> <dt>

<span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span>**WMDM \_ FORMATCODE \_ ATSCTS** 
</dt> <dd>

Formatcode für den ATSCTS-Formatstandard (Advanced Tv Systems Committee).

</dd> <dt>

<span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span>**WMDM \_ \_FORMATCODE-CODIERUNGEN** 
</dt> <dd>

Formatieren Sie Code für ein MPEG-2-Video und MPEG-1 Layer II- oder AC-3-Audio innerhalb eines MPEG-2-Transportstreams, der mit MPEG-2 kompatibel ist.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCOLLECTION**
</dt> <dd>

Formatieren Sie Code für eine Auflistung eines nicht definierten Typs.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**\_WMDM-FORMATCODE \_ ABSTRACTMULTIMEDIA WIES**
</dt> <dd>

Formatieren Sie Code für ein Multimedia-Album, bei dem das -Objekt die Eigenschaften eines Multimediaalbens und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**\_WMDM-FORMATCODE \_ ABSTRACTIMAGEIMAGE**
</dt> <dd>

Formatcode für ein Bildalb, in dem das -Objekt die Eigenschaften eines Bildalbens und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**\_WMDM-FORMATCODE \_ ABSTRACTAUDIO WIES**
</dt> <dd>

Formatieren Sie Code für ein Audioalb, in dem das -Objekt die Eigenschaften eines Audioalbens und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**\_WMDM-FORMATCODE \_ ABSTRACTVIDEO WIES**
</dt> <dd>

Formatieren Sie Code für ein Videoalb, in dem das -Objekt die Eigenschaften eines Videoalbens und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**WMDM \_ FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST**
</dt> <dd>

Formatieren Sie Code für eine Audio-/Videowiedergabeliste, in der das Objekt die Eigenschaften einer Audio-/Videowiedergabeliste und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCONTACTGROUP**
</dt> <dd>

Formatieren Sie Code für eine Kontaktgruppe, in der das -Objekt die Eigenschaften einer Kontaktgruppe und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMESSAGEFOLDER**
</dt> <dd>

Formatieren Sie Code für einen Nachrichtenordner, in dem das -Objekt die Eigenschaften eines Nachrichtenordners und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCHAPTEREDPRODUCTION**
</dt> <dd>

Formatieren Sie Code für eine Kapitelproduktion, in der das -Objekt die Eigenschaften einer Kapitelproduktion und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**WMDM \_ FORMATCODE \_ WPLPLAYLIST**
</dt> <dd>

Formatieren Sie Code für eine Wiedergabeliste, die mit Windows Medienwiedergabelistenformatierung formatiert ist.

</dd> <dt>

<span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**\_WMDM-FORMATCODE \_ M3UPLAYLIST**
</dt> <dd>

Formatieren sie Code für eine Wiedergabeliste mit M3U-Formatierung.

</dd> <dt>

<span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**WMDM \_ FORMATCODE \_ MPLPLAYLIST**
</dt> <dd>

Formatieren sie Code für eine Wiedergabeliste mit MPL-Formatierung.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**WMDM \_ FORMATCODE \_ ASXPLAYLIST**
</dt> <dd>

Formatieren Sie Code für eine Wiedergabeliste mit ASX-Formatierung.

</dd> <dt>

<span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**\_WMDM-FORMATCODE \_ PLSPLAYLIST**
</dt> <dd>

Formatieren sie Code für eine Wiedergabeliste mit PLS-Formatierung.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDDOCUMENT**
</dt> <dd>

Formatieren Sie Code für ein Dokument mit einem nicht definierten Typ.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**WMDM \_ FORMATCODE \_ ABSTRACTDOCUMENT**
</dt> <dd>

Formatieren Sie Code für ein Dokument, in dem das -Objekt die Eigenschaften eines Dokuments und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**WMDM \_ FORMATCODE \_ XMLDOCUMENT**
</dt> <dd>

Formatieren von Code für ein XML-Dokument.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**WMDM \_ FORMATCODE \_ MICROSOFTWORDDOCUMENT**
</dt> <dd>

Formatieren sie Code für Microsoft Word Dokument.

</dd> <dt>

<span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**WMDM \_ FORMATCODE \_ MHTCOMPILEDHTMLDOCUMENT**
</dt> <dd>

Formatieren sie Code für ein kompiliertes HTML-Dokument.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**\_WMDM-FORMATCODE \_ MICROSOFTEXCELSPREADSHEET**
</dt> <dd>

Formatieren sie Code für ein Microsoft Excel Arbeitsblatt.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**\_WMDM-FORMATCODE \_ MICROSOFTPOWERPOINTDOCUMENT**
</dt> <dd>

Formatieren von Code für ein Microsoft PowerPoint Dokument.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDMESSAGE**
</dt> <dd>

Formatieren Sie Code für eine Nachricht vom nicht definierten Typ.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMESSAGE**
</dt> <dd>

Formatieren Sie Code für eine Nachricht, in der das -Objekt die Eigenschaften einer Nachricht und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCONTACT**
</dt> <dd>

Formatieren Sie Code für einen Kontakt mit einem nicht definierten Typ.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCONTACT**
</dt> <dd>

Formatcode für einen Kontakt, in dem das -Objekt die Eigenschaften eines Kontakts und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**WMDM \_ FORMATCODE \_ VCARD2**
</dt> <dd>

Formatieren Sie Code für eine elektronische Karte mit VCard-Formatierung der Version 2.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**WMDM \_ FORMATCODE \_ VCARD3**
</dt> <dd>

Formatieren Sie Code für eine elektronische Karte mit VCard-Formatierung der Version 3.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCALENDARITEM**
</dt> <dd>

Formatcode für ein elektronisches Kalenderelement vom nicht definierten Typ.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCALENDARITEM**
</dt> <dd>

Formatcode für ein Kalenderelement, in dem das -Objekt die Eigenschaften eines Kalenderelements und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**\_WMDM-FORMATCODE \_ VCALENDAR1**
</dt> <dd>

Formatieren Sie Code für ein elektronisches Kalenderelement mit vcalendar Version 1-Formatierung.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**WMDM \_ FORMATCODE \_ VCALENDAR2**
</dt> <dd>

Formatcode für ein elektronisches Kalenderelement mit Vcalendar Version 2-Formatierung.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDWINDOWSEXECUTABLE**
</dt> <dd>

Formatieren Sie Code für Windows ausführbare Datei mit nicht definiertem Typ.

</dd> <dt>

<span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**WMDM \_ FORMATCODE \_ MEDIA \_ CAST**
</dt> <dd>

Formatcode für ein Medien cast-Objekt.

</dd> <dt>

<span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**\_WMDM-FORMATCODEABSCHNITT \_**
</dt> <dd>

Formatieren Sie Code für einen Datenabschnitt, der in einem anderen -Objekt enthalten ist.

</dd> <dt>

<span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span>**WMDM \_ FORMATCODE \_ 3G2A** 
</dt> <dd>

Formatcode für ein 3G2A-Multimediacontainerformat (3GPP2A).

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um die von einem Gerät unterstützten Formate zu ermitteln, kann eine Anwendung [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) verwenden, um die **Geräteeigenschaft g \_ wszWMDMFormatsSupported** abzufragen.

Um Gerätefunktionen für ein bestimmtes Format zu ermitteln, kann eine Anwendung [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)aufrufen.

Eine Anwendung kann den Formatcode beim Erstellen eines Speichers auf dem Gerät festlegen, indem sie die **g \_ wszWMDMFormatCode-Eigenschaft** in Metadaten einschließt, die im *pMetaData-Parameter* eines Aufrufs von [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)übergeben werden.

Eine Anwendung kann den Formatcode eines Speichers abfragen, indem [**sie IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) oder [**IWMDMStorage4::GetSpecifiedMetadata aufruft**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) und die **g \_ wszWMDMFormatCode-Eigenschaft** abruft.

Wenn das Gerät das Festlegen des Formatcodes nach der Speichererstellung unterstützt, kann eine Anwendung [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) verwenden, um die **g \_ wszWMDMFormatCode-Eigenschaft** festzulegen. Einige Geräte lassen möglicherweise keine Änderung des Formatcodes zu, nachdem der Speicher auf dem Gerät erstellt wurde. Daher wird dringend empfohlen, diese Eigenschaft zusammen mit den metadaten festzulegen, die in [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) übergeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)
</dt> <dt>

[**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)
</dt> <dt>

[**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)
</dt> <dt>

[**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)
</dt> <dt>

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)
</dt> <dt>

[**Metadatenkonstanten**](metadata-constants.md)
</dt> </dl>

 

 





