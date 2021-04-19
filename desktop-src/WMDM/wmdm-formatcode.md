---
title: WMDM_FORMATCODE-Enumeration
description: Der WMDM \_ Formatcode-Enumerationstyp definiert eine Liste von Formatcodes, die Typen von Inhalten beschreiben, die an ein und von einem Gerät übertragen werden.
ms.assetid: 203d9bdf-cbbd-4d06-8292-26c8a472e2aa
keywords:
- Device Manager der WMDM_FORMATCODE-Enumeration Windows Media
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
ms.openlocfilehash: d04db31578f36455fdf77bb4044ad45e5ca9f9a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352810"
---
# <a name="wmdm_formatcode-enumeration"></a>WMDM- \_ Formatcode-Enumeration

Der **WMDM \_ Formatcode** -Enumerationstyp definiert eine Liste von Formatcodes, die Typen von Inhalten beschreiben, die an ein und von einem Gerät übertragen werden.

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

<span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**WMDM- \_ Formatcode wurde \_ notused**
</dt> <dd>

Es wird kein Format Code verwendet.

</dd> <dt>

<span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**WMDM- \_ Formatcode- \_ allimages**
</dt> <dd>

Formatieren Sie Code, der zum Abfragen aller Bilder verwendet werden kann.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**WMDM- \_ Formatcode nicht \_ definiert**
</dt> <dd>

Formatierungs Code, mit dem alle nicht definierten Objekte abgefragt werden.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**WMDM- \_ Formatcode-Zuordnung \_**
</dt> <dd>

Formatierungs Code, der zum Definieren eines Links zwischen zwei Objekten verwendet wird.

</dd> <dt>

<span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**WMDM- \_ Formatcode- \_ Skript**
</dt> <dd>

Formatieren von Code für eine Skriptdatei.

</dd> <dt>

<span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**ausführbare WMDM- \_ Formatcode- \_ Datei**
</dt> <dd>

Formatieren von Code für eine ausführbare Datei.

</dd> <dt>

<span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**WMDM- \_ \_ formatcodetext**
</dt> <dd>

Formatieren von Code für eine Textdatei.

</dd> <dt>

<span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**WMDM \_ Formatcode \_ HTML**
</dt> <dd>

Formatieren von Code für eine HTML-Datei.

</dd> <dt>

<span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**WMDM \_ Formatcode \_ DPOF**
</dt> <dd>

Formatierungs Code, der zum Darstellen des digitalen Druckauftrags Formats verwendet wird.

</dd> <dt>

<span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM- \_ Formatcode- \_ AIFF**
</dt> <dd>

Formatierungs Code, der zum Darstellen des audioaustauschdateiformats verwendet wird.

</dd> <dt>

<span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**WMDM- \_ Formatcode- \_ Wave**
</dt> <dd>

Formatierungs Code für eine WAV-Datei.

</dd> <dt>

<span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**WMDM \_ Formatcode \_ MP3**
</dt> <dd>

Formatierungs Code für eine MP3-Datei.

</dd> <dt>

<span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**WMDM \_ Formatcode \_ AVI**
</dt> <dd>

Formatierungs Code für eine AVI-Datei.

</dd> <dt>

<span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**WMDM- \_ Formatcode \_ MPEG**
</dt> <dd>

Formatierungs Code für eine MPEG-Datei.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**WMDM- \_ Formatcode- \_ ASF**
</dt> <dd>

Formatierungs Code, der zur Darstellung einer ASF-Datei (Advanced Systems Format) verwendet wird.

</dd> <dt>

<span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**WMDM- \_ Formatcode \_ \_ zuerst reserviert**
</dt> <dd>

Formatieren Sie Code, der der erste in einem für das Picture Transfer-Protokoll (PTP) reservierten Bereich ist.

</dd> <dt>

<span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**\_ \_ zuletzt reservierter WMDM-Formatcode \_**
</dt> <dd>

Formatieren Sie Code, der zuletzt in einem für PTP reservierten Bereich vorliegt.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**WMDM \_ Formatcode- \_ Image nicht \_ definiert**
</dt> <dd>

Formatieren Sie Code, der zum Darstellen von und Bildern eines nicht definierten Typs verwendet wird.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**WMDM \_ Formatcode- \_ Bild ( \_ EXIF)**
</dt> <dd>

Formatieren von Code für eine EXIF-Datei. Wird auch für JPEG-Bilder verwendet, die nicht von WMDM \_ Formatcode \_ Image \_ JP2 oder WMDM \_ Formatcode \_ Image \_ JPX abgedeckt werden.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**WMDM \_ Formatcode- \_ Bild, \_ tiffep**
</dt> <dd>

Formatieren von Code für Bilder, die vom Typ "Tagged Image File Format für elektronische Fotografie (TIFF/EP)" sind

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**WMDM \_ Formatcode- \_ Bild ( \_ Flash)**
</dt> <dd>

Formatieren Sie den Code für eine Datei vom Typ FPX.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**WMDM \_ Formatcode- \_ Bild \_ BMP**
</dt> <dd>

Formatieren Sie Code für eine Datei vom Typ BMP.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**WMDM \_ Formatcode- \_ Bild- \_ CIFF**
</dt> <dd>

Formatieren von Code für ein Bild im Kamerabild Dateiformat.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**WMDM \_ Formatcode \_ Bild \_ GIF**
</dt> <dd>

Formatieren von Code für eine GIF-Datei.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**WMDM \_ Formatcode- \_ Image \_ JFI f**
</dt> <dd>

Formatieren Sie Code für eine Datei vom Typ jff.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**WMDM \_ Formatcode \_ Image \_ PCD**
</dt> <dd>

Formatieren Sie Code für ein Bild vom Typ Photo CD.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**WMDM \_ Formatcode- \_ Bild- \_ PICT**
</dt> <dd>

Formatieren Sie Code für ein Bild vom Typ PICT.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**WMDM \_ Formatcode- \_ Image \_ PNG**
</dt> <dd>

Formatieren Sie den Code für ein Bild vom Typ PNG.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**WMDM \_ Formatcode- \_ Bild \_ TIFF**
</dt> <dd>

Formatieren Sie Code für eine Datei vom Typ TIFF.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**WMDM \_ Formatcode- \_ Bild ( \_ tiffit)**
</dt> <dd>

Formatieren Sie Code für ein Bild vom Typ Tagged Image File Format mit der Bildtechnologie.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**WMDM \_ Formatcode- \_ Image \_ JP2**
</dt> <dd>

Formatieren von Code für ein Jpeg200-Image.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**WMDM \_ Formatcode- \_ Image \_ JPX**
</dt> <dd>

Formatieren Sie Code für ein Bild, das auf JPEG200 erstellt wurde, mithilfe der erweiterten immer noch Bildregistrierung. Die Dateinamenerweiterung lautet normalerweise ". jpf" oder ". JPX".

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**WMDM \_ Formatcode \_ - \_ Image \_ zuerst reserviert**
</dt> <dd>

Formatieren Sie Code, der der erste in einem Bereich ist, der für einen Bild Verweis in PTP reserviert ist.

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**Das WMDM- \_ Format Code \_ Bild wurde \_ \_ zuletzt reserviert.**
</dt> <dd>

Formatieren Sie Code, der der letzte in einem Bereich ist, der für einen Bild Verweis in PTP reserviert ist.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**WMDM \_ Formatcode \_ undefinedfirmware**
</dt> <dd>

Formatieren Sie Code, wenn die Firmware nicht definiert ist.

</dd> <dt>

<span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span>**WMDM \_ Formatcode- \_ WBMP** 
</dt> <dd>

Formatieren Sie den Code für ein WBMP-Image (drahtlos Anwendungsprotokoll Bitmap).

</dd> <dt>

<span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span>**WMDM \_ Formatcode \_ jpgxr** 
</dt> <dd>

Formatieren von Code für ein HD-Foto

</dd> <dt>

<span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**WMDM \_ Formatcode \_ windowsimageformat**
</dt> <dd>

Formatieren Sie Code für das Windows-Bildformat.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**WMDM \_ Formatcode \_ undefinedaudiodatei**
</dt> <dd>

Formatieren Sie Code für eine Audiodatei mit einem nicht definierten Typ.

</dd> <dt>

<span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**WMDM \_ Formatcode \_ WMA**
</dt> <dd>

Formatieren von Code für eine Windows Media Audio-Datei (WMA).

</dd> <dt>

<span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**WMDM- \_ Formatcode \_ OGG**
</dt> <dd>

Formatieren von Code für eine vorals-codierte Audiodatei in einem OGG-Container.

</dd> <dt>

<span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM- \_ Formatcode- \_ AAC**
</dt> <dd>

Formatieren Sie Code für eine AAC-Datei (Advanced audiocoding).

</dd> <dt>

<span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**WMDM- \_ Formatcode \_ hörbar**
</dt> <dd>

Formatieren Sie Code für eine akustische Datei.

</dd> <dt>

<span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**WMDM \_ Formatcode \_ FLAC**
</dt> <dd>

Formatieren Sie den Code für eine kostenlose FLAC-Datei (Lossless Audiocodec).

</dd> <dt>

<span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span>**WMDM \_ Formatcode- \_ QCELP** 
</dt> <dd>

Formatieren von Code für eine "Qualcomm"-Codelisting (QCELP)-Codec-Datei

</dd> <dt>

<span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span>**WMDM \_ Formatcode \_ AMR** 
</dt> <dd>

Formatieren Sie den Code für eine Adaptive Multi-Rate Audiodatei (AMR).

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**WMDM \_ Formatcode \_ undefinedvideo**
</dt> <dd>

Formatieren von Code für eine Videodatei mit einem nicht definierten Typ.

</dd> <dt>

<span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**WMDM \_ Formatcode \_ WMV**
</dt> <dd>

Formatieren von Code für eine Windows Media Video Datei (WMV).

</dd> <dt>

<span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**WMDM \_ Formatcode \_ MP4**
</dt> <dd>

Formatieren von Code für eine MP4-Datei.

</dd> <dt>

<span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**WMDM- \_ Formatcode- \_ MP2**
</dt> <dd>

Formatieren von Code für eine MP2-Datei.

</dd> <dt>

<span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span>**WMDM \_ Formatcode \_ 3G2** 
</dt> <dd>

Formatieren Sie den Code für das 3G2-multimediacontainerformat (3GPP2). Eine Datei mit diesem Typ kann Audiodateien, Videos oder Text enthalten.

</dd> <dt>

<span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span>**WMDM \_ Formatcode \_ AVCHD** 
</dt> <dd>

Formatieren von Code für eine AVCHD-Videodatei (Advanced Video Coding High Definition).

</dd> <dt>

<span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span>**WMDM \_ Formatcode- \_ atscts** 
</dt> <dd>

Formatieren Sie den Code für den Format Standard des Advanced Fernsehen Systems Committee (atscts).

</dd> <dt>

<span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span>**WMDM \_ Formatcode \_ dvbts** 
</dt> <dd>

Formatieren Sie den Code für ein MPEG-2-Video und MPEG-1 Layer II-oder AC-3-Audiodaten innerhalb eines mit einem DVB kompatiblen MPEG-2-Transport Datenstroms.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM \_ Formatcode \_ undefinedcollection**
</dt> <dd>

Formatieren von Code für eine Auflistung eines nicht definierten Typs.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**WMDM \_ Formatcode \_ abstractmultimediaalbum**
</dt> <dd>

Formatieren von Code für ein multimediarester, bei dem das Objekt die Eigenschaften eines Multimedia-Albums und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**WMDM \_ Formatcode \_ abstractimagealbum**
</dt> <dd>

Formatieren von Code für ein Bild-Album, bei dem das-Objekt die Eigenschaften eines imagealbums und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**WMDM \_ Formatcode \_ abstractaudioalbum**
</dt> <dd>

Formatieren von Code für ein Audioalbum, bei dem das-Objekt die Eigenschaften eines audioalbums und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**WMDM \_ Formatcode \_ abstractvideoalbum**
</dt> <dd>

Formatieren von Code für ein Video Album, bei dem das-Objekt die Eigenschaften eines Video Albums und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**WMDM \_ Formatcode \_ abstractaudiovideoplaylist**
</dt> <dd>

Formatieren Sie Code für eine Audiowiedergabe-Wiedergabeliste, in der das-Objekt die Eigenschaften einer Audiowiedergabe-Wiedergabeliste und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**WMDM \_ Formatcode \_ abstractcontactgroup**
</dt> <dd>

Formatieren Sie Code für eine Kontaktgruppe, in der das-Objekt die Eigenschaften einer Kontaktgruppe und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**WMDM \_ Formatcode \_ abstractmessagefolder**
</dt> <dd>

Formatieren Sie den Code für einen Nachrichten Ordner, in dem das Objekt die Eigenschaften eines Nachrichten Ordners und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**WMDM \_ Formatcode \_ abstractchapteredproduction**
</dt> <dd>

Formatieren Sie den Code für eine in einem Kapitel enthaltene Produktionsumgebung, in der das-Objekt die Eigenschaften einer in Kapitel unterteilten Produktion und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**WMDM- \_ Formatcode \_ wplwiedergabe**
</dt> <dd>

Formatieren von Code für eine Wiedergabeliste, die mit der Formatierung der Windows Media-Wiedergabe

</dd> <dt>

<span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**WMDM- \_ Formatcode \_ M3UPLAYLIST**
</dt> <dd>

Formatieren von Code für eine Wiedergabeliste mit m3u-Formatierung.

</dd> <dt>

<span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**WMDM \_ Formatcode- \_ mplwiedergabe**
</dt> <dd>

Formatieren von Code für eine Wiedergabeliste mit MPL-Formatierung.

</dd> <dt>

<span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**WMDM \_ Formatcode \_ asxwiedergabe**
</dt> <dd>

Formatieren von Code für eine Wiedergabeliste mit der ASX-Formatierung.

</dd> <dt>

<span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**WMDM \_ Formatcode \_ plsplaylist**
</dt> <dd>

Formatieren von Code für eine Wiedergabeliste mit pls-Formatierung.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**WMDM \_ Formatcode \_ undefineddocument**
</dt> <dd>

Formatieren von Code für ein Dokument mit nicht definiertem Typ.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**WMDM \_ Formatcode \_ AbstractDocument**
</dt> <dd>

Formatieren von Code für ein Dokument, in dem das Objekt die Eigenschaften eines Dokuments und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**WMDM \_ Formatcode \_ XmlDocument**
</dt> <dd>

Formatieren von Code für ein XML-Dokument.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**WMDM \_ Formatcode \_ microsoftworddocument**
</dt> <dd>

Formatieren von Code für ein Microsoft Word-Dokument.

</dd> <dt>

<span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**WMDM \_ Formatcode \_ mhtcompiledhtmldocument**
</dt> <dd>

Formatieren von Code für ein kompiliertes HTML-Dokument

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**WMDM \_ Formatcode- \_ mikrosoftexcelkalkulations Tabelle**
</dt> <dd>

Formatieren von Code für eine Microsoft Excel-Tabelle.

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**WMDM \_ Formatcode \_ microsoftpowerpointdocument**
</dt> <dd>

Formatieren von Code für ein Microsoft PowerPoint-Dokument.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**WMDM \_ Formatcode \_ undefinedmessage**
</dt> <dd>

Formatieren Sie Code für eine Meldung mit einem nicht definierten Typ.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**WMDM \_ Formatcode \_ abstractmessage**
</dt> <dd>

Formatieren von Code für eine Nachricht, bei der das-Objekt die Eigenschaften einer Nachricht und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**WMDM- \_ Formatcode \_ undefinedcontact**
</dt> <dd>

Formatieren von Code für einen Kontakt mit einem nicht definierten Typ.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**WMDM \_ Formatcode \_ abstractcontact**
</dt> <dd>

Formatieren von Code für einen Kontakt, bei dem das Objekt die Eigenschaften eines Kontakts und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**WMDM- \_ Formatcode \_ VCARD2**
</dt> <dd>

Formatieren von Code für eine elektronische Karte mit vCard-Formatierung, Version 2.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**WMDM- \_ Formatcode \_ VCARD3**
</dt> <dd>

Formatieren Sie Code für eine elektronische Karte mit vCard-Formatierung, Version 3.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**WMDM \_ Formatcode \_ undefinedcalendaritem**
</dt> <dd>

Formatieren von Code für ein elektronisches Kalender Element mit nicht definiertem Typ.

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**WMDM \_ Formatcode \_ abstractcalendaritem**
</dt> <dd>

Formatieren von Code für ein Kalender Element, bei dem das-Objekt die Eigenschaften eines Kalender Elements und optional Daten enthält. Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**WMDM- \_ Formatcode \_ VCALENDAR1**
</dt> <dd>

Formatieren von Code für ein elektronisches Kalender Element mit der vCalendar Version 1-Formatierung.

</dd> <dt>

<span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**WMDM- \_ Formatcode \_ VCALENDAR2**
</dt> <dd>

Formatieren Sie den Code für ein elektronisches Kalender Element mit Formatierung von vCalendar Version 2.

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**WMDM \_ Formatcode \_ undefinedwindowsexecutor**
</dt> <dd>

Formatieren von Code für eine Windows-basierte ausführbare Datei des undefinierten Typs.

</dd> <dt>

<span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**WMDM- \_ Formatcode- \_ Medien Umwandlung \_**
</dt> <dd>

Formatieren von Code für ein Medienobjekt.

</dd> <dt>

<span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**Abschnitt "WMDM \_ Formatcode" \_**
</dt> <dd>

Formatieren von Code für einen Abschnitt von Daten, der in einem anderen Objekt enthalten ist.

</dd> <dt>

<span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span>**WMDM \_ Formatcode \_ 3g2a** 
</dt> <dd>

Formatieren Sie den Code für ein 3g2a-multimediacontainerformat (3gpp2a).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Zum Ermitteln der Formate, die von einem Gerät unterstützt werden, kann eine Anwendung [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) verwenden, um die Eigenschaft " **g \_ wszwmdmformatssupported** Device" abzufragen.

Eine Anwendung kann [**IWMDMDevice3:: getformatcapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)aufrufen, um Gerätefunktionen für ein bestimmtes Format zu ermitteln.

Eine Anwendung kann den Formatierungs Code beim Erstellen eines Speichers auf dem Gerät festlegen, indem Sie die **g \_ wszwmdmformatcode** -Eigenschaft in Metadaten einschließt, die im *pMetaData* -Parameter eines Aufrufens von [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)übergeben werden.

Eine Anwendung kann den Format Code eines Speichers Abfragen, indem [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) oder [**IWMDMStorage4:: getspecifiedmetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) aufgerufen und die Eigenschaft **g \_ wszwmdmformatcode** abgerufen wird.

Wenn das Gerät das Festlegen des Formatcodes nach der Speicher Erstellung unterstützt, kann eine Anwendung [**IWMDMStorage3:: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) verwenden, um die Eigenschaft " **g \_ wszwmdmformatcode** " festzulegen. Einige Geräte erlauben möglicherweise nicht das Ändern des Formatcodes, nachdem der Speicher auf dem Gerät erstellt wurde. Daher wird dringend empfohlen, diese Eigenschaft zusammen mit den in [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) übergebenen Metadaten festzulegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Enumerationstypen**](enumeration-types.md)
</dt> <dt>

[**IWMDMDevice3:: getformatcapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)
</dt> <dt>

[**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)
</dt> <dt>

[**IWMDMStorage3:: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)
</dt> <dt>

[**IWMDMStorage4:: getspecifiedmetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)
</dt> <dt>

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)
</dt> <dt>

[**Metadatenkonstanten**](metadata-constants.md)
</dt> </dl>

 

 





