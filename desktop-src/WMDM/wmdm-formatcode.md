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
# <a name="wmdm_formatcode-enumeration"></a><span data-ttu-id="037a4-104">WMDM- \_ Formatcode-Enumeration</span><span class="sxs-lookup"><span data-stu-id="037a4-104">WMDM\_FORMATCODE enumeration</span></span>

<span data-ttu-id="037a4-105">Der **WMDM \_ Formatcode** -Enumerationstyp definiert eine Liste von Formatcodes, die Typen von Inhalten beschreiben, die an ein und von einem Gerät übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="037a4-105">The **WMDM\_FORMATCODE** enumeration type defines a list of format codes that describe types of content transferred to and from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="037a4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="037a4-106">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="037a4-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="037a4-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="037a4-108"><span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**WMDM- \_ Formatcode wurde \_ notused**</span><span class="sxs-lookup"><span data-stu-id="037a4-108"><span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**WMDM\_FORMATCODE\_NOTUSED**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-109">Es wird kein Format Code verwendet.</span><span class="sxs-lookup"><span data-stu-id="037a4-109">No format code is used.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-110"><span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**WMDM- \_ Formatcode- \_ allimages**</span><span class="sxs-lookup"><span data-stu-id="037a4-110"><span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**WMDM\_FORMATCODE\_ALLIMAGES**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-111">Formatieren Sie Code, der zum Abfragen aller Bilder verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="037a4-111">Format code that can be used to query for all images.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-112"><span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**WMDM- \_ Formatcode nicht \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="037a4-112"><span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**WMDM\_FORMATCODE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-113">Formatierungs Code, mit dem alle nicht definierten Objekte abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="037a4-113">Format code used to query for all undefined objects.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-114"><span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**WMDM- \_ Formatcode-Zuordnung \_**</span><span class="sxs-lookup"><span data-stu-id="037a4-114"><span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**WMDM\_FORMATCODE\_ASSOCIATION**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-115">Formatierungs Code, der zum Definieren eines Links zwischen zwei Objekten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="037a4-115">Format code used to define a link between two objects.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-116"><span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**WMDM- \_ Formatcode- \_ Skript**</span><span class="sxs-lookup"><span data-stu-id="037a4-116"><span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**WMDM\_FORMATCODE\_SCRIPT**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-117">Formatieren von Code für eine Skriptdatei.</span><span class="sxs-lookup"><span data-stu-id="037a4-117">Format code for a script file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-118"><span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**ausführbare WMDM- \_ Formatcode- \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="037a4-118"><span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**WMDM\_FORMATCODE\_EXECUTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-119">Formatieren von Code für eine ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="037a4-119">Format code for an executable file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-120"><span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**WMDM- \_ \_ formatcodetext**</span><span class="sxs-lookup"><span data-stu-id="037a4-120"><span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**WMDM\_FORMATCODE\_TEXT**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-121">Formatieren von Code für eine Textdatei.</span><span class="sxs-lookup"><span data-stu-id="037a4-121">Format code for a text file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-122"><span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**WMDM \_ Formatcode \_ HTML**</span><span class="sxs-lookup"><span data-stu-id="037a4-122"><span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**WMDM\_FORMATCODE\_HTML**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-123">Formatieren von Code für eine HTML-Datei.</span><span class="sxs-lookup"><span data-stu-id="037a4-123">Format code for an HTML file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-124"><span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**WMDM \_ Formatcode \_ DPOF**</span><span class="sxs-lookup"><span data-stu-id="037a4-124"><span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**WMDM\_FORMATCODE\_DPOF**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-125">Formatierungs Code, der zum Darstellen des digitalen Druckauftrags Formats verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="037a4-125">Format code used to represent the digital print order format.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-126"><span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM- \_ Formatcode- \_ AIFF**</span><span class="sxs-lookup"><span data-stu-id="037a4-126"><span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM\_FORMATCODE\_AIFF**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-127">Formatierungs Code, der zum Darstellen des audioaustauschdateiformats verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="037a4-127">Format code used to represent the audio interchange file format.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-128"><span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**WMDM- \_ Formatcode- \_ Wave**</span><span class="sxs-lookup"><span data-stu-id="037a4-128"><span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**WMDM\_FORMATCODE\_WAVE**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-129">Formatierungs Code für eine WAV-Datei.</span><span class="sxs-lookup"><span data-stu-id="037a4-129">Format code used for a WAV file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-130"><span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**WMDM \_ Formatcode \_ MP3**</span><span class="sxs-lookup"><span data-stu-id="037a4-130"><span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**WMDM\_FORMATCODE\_MP3**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-131">Formatierungs Code für eine MP3-Datei.</span><span class="sxs-lookup"><span data-stu-id="037a4-131">Format code used for an MP3 file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-132"><span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**WMDM \_ Formatcode \_ AVI**</span><span class="sxs-lookup"><span data-stu-id="037a4-132"><span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**WMDM\_FORMATCODE\_AVI**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-133">Formatierungs Code für eine AVI-Datei.</span><span class="sxs-lookup"><span data-stu-id="037a4-133">Format code used for an AVI file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-134"><span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**WMDM- \_ Formatcode \_ MPEG**</span><span class="sxs-lookup"><span data-stu-id="037a4-134"><span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**WMDM\_FORMATCODE\_MPEG**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-135">Formatierungs Code für eine MPEG-Datei.</span><span class="sxs-lookup"><span data-stu-id="037a4-135">Format code used for an MPEG file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-136"><span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**WMDM- \_ Formatcode- \_ ASF**</span><span class="sxs-lookup"><span data-stu-id="037a4-136"><span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**WMDM\_FORMATCODE\_ASF**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-137">Formatierungs Code, der zur Darstellung einer ASF-Datei (Advanced Systems Format) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="037a4-137">Format code used to represent an Advanced Systems Format (ASF) file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-138"><span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**WMDM- \_ Formatcode \_ \_ zuerst reserviert**</span><span class="sxs-lookup"><span data-stu-id="037a4-138"><span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**WMDM\_FORMATCODE\_RESERVED\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-139">Formatieren Sie Code, der der erste in einem für das Picture Transfer-Protokoll (PTP) reservierten Bereich ist.</span><span class="sxs-lookup"><span data-stu-id="037a4-139">Format code that is the first in a range reserved for Picture Transfer Protocol (PTP).</span></span>

</dd> <dt>

<span data-ttu-id="037a4-140"><span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**\_ \_ zuletzt reservierter WMDM-Formatcode \_**</span><span class="sxs-lookup"><span data-stu-id="037a4-140"><span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**WMDM\_FORMATCODE\_RESERVED\_LAST**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-141">Formatieren Sie Code, der zuletzt in einem für PTP reservierten Bereich vorliegt.</span><span class="sxs-lookup"><span data-stu-id="037a4-141">Format code that is last in a range reserved for PTP.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-142"><span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**WMDM \_ Formatcode- \_ Image nicht \_ definiert**</span><span class="sxs-lookup"><span data-stu-id="037a4-142"><span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**WMDM\_FORMATCODE\_IMAGE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-143">Formatieren Sie Code, der zum Darstellen von und Bildern eines nicht definierten Typs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="037a4-143">Format code used to represent and image of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-144"><span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**WMDM \_ Formatcode- \_ Bild ( \_ EXIF)**</span><span class="sxs-lookup"><span data-stu-id="037a4-144"><span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**WMDM\_FORMATCODE\_IMAGE\_EXIF**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-145">Formatieren von Code für eine EXIF-Datei.</span><span class="sxs-lookup"><span data-stu-id="037a4-145">Format code for an EXIF file.</span></span> <span data-ttu-id="037a4-146">Wird auch für JPEG-Bilder verwendet, die nicht von WMDM \_ Formatcode \_ Image \_ JP2 oder WMDM \_ Formatcode \_ Image \_ JPX abgedeckt werden.</span><span class="sxs-lookup"><span data-stu-id="037a4-146">Also used for JPEG images not covered by WMDM\_FORMATCODE\_IMAGE\_JP2 or WMDM\_FORMATCODE\_IMAGE\_JPX.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-147"><span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**WMDM \_ Formatcode- \_ Bild, \_ tiffep**</span><span class="sxs-lookup"><span data-stu-id="037a4-147"><span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFFEP**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-148">Formatieren von Code für Bilder, die vom Typ "Tagged Image File Format für elektronische Fotografie (TIFF/EP)" sind</span><span class="sxs-lookup"><span data-stu-id="037a4-148">Format code used for images that are of type Tagged Image File Format for Electronic Photography (TIFF/EP)</span></span>

</dd> <dt>

<span data-ttu-id="037a4-149"><span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**WMDM \_ Formatcode- \_ Bild ( \_ Flash)**</span><span class="sxs-lookup"><span data-stu-id="037a4-149"><span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**WMDM\_FORMATCODE\_IMAGE\_FLASHPIX**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-150">Formatieren Sie den Code für eine Datei vom Typ FPX.</span><span class="sxs-lookup"><span data-stu-id="037a4-150">Format code for a file of type FPX.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-151"><span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**WMDM \_ Formatcode- \_ Bild \_ BMP**</span><span class="sxs-lookup"><span data-stu-id="037a4-151"><span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**WMDM\_FORMATCODE\_IMAGE\_BMP**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-152">Formatieren Sie Code für eine Datei vom Typ BMP.</span><span class="sxs-lookup"><span data-stu-id="037a4-152">Format code for a file of type BMP.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-153"><span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**WMDM \_ Formatcode- \_ Bild- \_ CIFF**</span><span class="sxs-lookup"><span data-stu-id="037a4-153"><span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**WMDM\_FORMATCODE\_IMAGE\_CIFF**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-154">Formatieren von Code für ein Bild im Kamerabild Dateiformat.</span><span class="sxs-lookup"><span data-stu-id="037a4-154">Format code for an image in the camera image file format.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-155"><span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**WMDM \_ Formatcode \_ Bild \_ GIF**</span><span class="sxs-lookup"><span data-stu-id="037a4-155"><span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**WMDM\_FORMATCODE\_IMAGE\_GIF**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-156">Formatieren von Code für eine GIF-Datei.</span><span class="sxs-lookup"><span data-stu-id="037a4-156">Format code for a GIF file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-157"><span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**WMDM \_ Formatcode- \_ Image \_ JFI f**</span><span class="sxs-lookup"><span data-stu-id="037a4-157"><span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**WMDM\_FORMATCODE\_IMAGE\_JFIF**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-158">Formatieren Sie Code für eine Datei vom Typ jff.</span><span class="sxs-lookup"><span data-stu-id="037a4-158">Format code for a file of type JFIF.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-159"><span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**WMDM \_ Formatcode \_ Image \_ PCD**</span><span class="sxs-lookup"><span data-stu-id="037a4-159"><span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**WMDM\_FORMATCODE\_IMAGE\_PCD**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-160">Formatieren Sie Code für ein Bild vom Typ Photo CD.</span><span class="sxs-lookup"><span data-stu-id="037a4-160">Format code for an image of type photo cd.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-161"><span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**WMDM \_ Formatcode- \_ Bild- \_ PICT**</span><span class="sxs-lookup"><span data-stu-id="037a4-161"><span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**WMDM\_FORMATCODE\_IMAGE\_PICT**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-162">Formatieren Sie Code für ein Bild vom Typ PICT.</span><span class="sxs-lookup"><span data-stu-id="037a4-162">Format code for an image of type PICT.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-163"><span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**WMDM \_ Formatcode- \_ Image \_ PNG**</span><span class="sxs-lookup"><span data-stu-id="037a4-163"><span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**WMDM\_FORMATCODE\_IMAGE\_PNG**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-164">Formatieren Sie den Code für ein Bild vom Typ PNG.</span><span class="sxs-lookup"><span data-stu-id="037a4-164">Format code for an image of type PNG.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-165"><span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**WMDM \_ Formatcode- \_ Bild \_ TIFF**</span><span class="sxs-lookup"><span data-stu-id="037a4-165"><span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFF**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-166">Formatieren Sie Code für eine Datei vom Typ TIFF.</span><span class="sxs-lookup"><span data-stu-id="037a4-166">Format code for a file of type TIFF.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-167"><span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**WMDM \_ Formatcode- \_ Bild ( \_ tiffit)**</span><span class="sxs-lookup"><span data-stu-id="037a4-167"><span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**WMDM\_FORMATCODE\_IMAGE\_TIFFIT**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-168">Formatieren Sie Code für ein Bild vom Typ Tagged Image File Format mit der Bildtechnologie.</span><span class="sxs-lookup"><span data-stu-id="037a4-168">Format code for an image of type Tagged Image File Format with image technology.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-169"><span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**WMDM \_ Formatcode- \_ Image \_ JP2**</span><span class="sxs-lookup"><span data-stu-id="037a4-169"><span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**WMDM\_FORMATCODE\_IMAGE\_JP2**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-170">Formatieren von Code für ein Jpeg200-Image.</span><span class="sxs-lookup"><span data-stu-id="037a4-170">Format code for a jpeg200 image.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-171"><span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**WMDM \_ Formatcode- \_ Image \_ JPX**</span><span class="sxs-lookup"><span data-stu-id="037a4-171"><span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**WMDM\_FORMATCODE\_IMAGE\_JPX**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-172">Formatieren Sie Code für ein Bild, das auf JPEG200 erstellt wurde, mithilfe der erweiterten immer noch Bildregistrierung.</span><span class="sxs-lookup"><span data-stu-id="037a4-172">Format code for an image built on JPEG200, using extended still image registration.</span></span> <span data-ttu-id="037a4-173">Die Dateinamenerweiterung lautet normalerweise ". jpf" oder ". JPX".</span><span class="sxs-lookup"><span data-stu-id="037a4-173">The file name extension is usually .jpf or .jpx.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-174"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**WMDM \_ Formatcode \_ - \_ Image \_ zuerst reserviert**</span><span class="sxs-lookup"><span data-stu-id="037a4-174"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**WMDM\_FORMATCODE\_IMAGE\_RESERVED\_FIRST**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-175">Formatieren Sie Code, der der erste in einem Bereich ist, der für einen Bild Verweis in PTP reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="037a4-175">Format code that is the first in a range reserved for an image reference in PTP.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-176"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**Das WMDM- \_ Format Code \_ Bild wurde \_ \_ zuletzt reserviert.**</span><span class="sxs-lookup"><span data-stu-id="037a4-176"><span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**WMDM\_FORMATCODE\_IMAGE\_RESERVED\_LAST**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-177">Formatieren Sie Code, der der letzte in einem Bereich ist, der für einen Bild Verweis in PTP reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="037a4-177">Format code that is the last in a range reserved for an image reference in PTP.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-178"><span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**WMDM \_ Formatcode \_ undefinedfirmware**</span><span class="sxs-lookup"><span data-stu-id="037a4-178"><span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**WMDM\_FORMATCODE\_UNDEFINEDFIRMWARE**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-179">Formatieren Sie Code, wenn die Firmware nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="037a4-179">Format code when firmware is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-180"><span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span>**WMDM \_ Formatcode- \_ WBMP**</span><span class="sxs-lookup"><span data-stu-id="037a4-180"><span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span> **WMDM\_FORMATCODE\_WBMP**</span></span> 
</dt> <dd>

<span data-ttu-id="037a4-181">Formatieren Sie den Code für ein WBMP-Image (drahtlos Anwendungsprotokoll Bitmap).</span><span class="sxs-lookup"><span data-stu-id="037a4-181">Format code for a Wireless Application Protocol Bitmap (.wbmp) image.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-182"><span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span>**WMDM \_ Formatcode \_ jpgxr**</span><span class="sxs-lookup"><span data-stu-id="037a4-182"><span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span> **WMDM\_FORMATCODE\_JPEGXR**</span></span> 
</dt> <dd>

<span data-ttu-id="037a4-183">Formatieren von Code für ein HD-Foto</span><span class="sxs-lookup"><span data-stu-id="037a4-183">Format code for an HD Photo image</span></span>

</dd> <dt>

<span data-ttu-id="037a4-184"><span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**WMDM \_ Formatcode \_ windowsimageformat**</span><span class="sxs-lookup"><span data-stu-id="037a4-184"><span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**WMDM\_FORMATCODE\_WINDOWSIMAGEFORMAT**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-185">Formatieren Sie Code für das Windows-Bildformat.</span><span class="sxs-lookup"><span data-stu-id="037a4-185">Format code for Windows image format.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-186"><span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**WMDM \_ Formatcode \_ undefinedaudiodatei**</span><span class="sxs-lookup"><span data-stu-id="037a4-186"><span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**WMDM\_FORMATCODE\_UNDEFINEDAUDIO**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-187">Formatieren Sie Code für eine Audiodatei mit einem nicht definierten Typ.</span><span class="sxs-lookup"><span data-stu-id="037a4-187">Format code for an audio file of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-188"><span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**WMDM \_ Formatcode \_ WMA**</span><span class="sxs-lookup"><span data-stu-id="037a4-188"><span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**WMDM\_FORMATCODE\_WMA**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-189">Formatieren von Code für eine Windows Media Audio-Datei (WMA).</span><span class="sxs-lookup"><span data-stu-id="037a4-189">Format code for a Windows Media Audio (WMA) file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-190"><span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**WMDM- \_ Formatcode \_ OGG**</span><span class="sxs-lookup"><span data-stu-id="037a4-190"><span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**WMDM\_FORMATCODE\_OGG**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-191">Formatieren von Code für eine vorals-codierte Audiodatei in einem OGG-Container.</span><span class="sxs-lookup"><span data-stu-id="037a4-191">Format code for a Vorbis-encoded audio file in an Ogg container.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-192"><span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM- \_ Formatcode- \_ AAC**</span><span class="sxs-lookup"><span data-stu-id="037a4-192"><span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM\_FORMATCODE\_AAC**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-193">Formatieren Sie Code für eine AAC-Datei (Advanced audiocoding).</span><span class="sxs-lookup"><span data-stu-id="037a4-193">Format code for an Advanced Audio Coding (AAC) file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-194"><span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**WMDM- \_ Formatcode \_ hörbar**</span><span class="sxs-lookup"><span data-stu-id="037a4-194"><span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**WMDM\_FORMATCODE\_AUDIBLE**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-195">Formatieren Sie Code für eine akustische Datei.</span><span class="sxs-lookup"><span data-stu-id="037a4-195">Format code for an Audible file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-196"><span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**WMDM \_ Formatcode \_ FLAC**</span><span class="sxs-lookup"><span data-stu-id="037a4-196"><span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**WMDM\_FORMATCODE\_FLAC**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-197">Formatieren Sie den Code für eine kostenlose FLAC-Datei (Lossless Audiocodec).</span><span class="sxs-lookup"><span data-stu-id="037a4-197">Format code for a Free Lossless Audio Codec (FLAC) file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-198"><span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span>**WMDM \_ Formatcode- \_ QCELP**</span><span class="sxs-lookup"><span data-stu-id="037a4-198"><span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span> **WMDM\_FORMATCODE\_QCELP**</span></span> 
</dt> <dd>

<span data-ttu-id="037a4-199">Formatieren von Code für eine "Qualcomm"-Codelisting (QCELP)-Codec-Datei</span><span class="sxs-lookup"><span data-stu-id="037a4-199">Format code for a Qualcomm Code Excited Linear Prediction (QCELP) codec file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-200"><span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span>**WMDM \_ Formatcode \_ AMR**</span><span class="sxs-lookup"><span data-stu-id="037a4-200"><span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span> **WMDM\_FORMATCODE\_AMR**</span></span> 
</dt> <dd>

<span data-ttu-id="037a4-201">Formatieren Sie den Code für eine Adaptive Multi-Rate Audiodatei (AMR).</span><span class="sxs-lookup"><span data-stu-id="037a4-201">Format code for an Adaptive Multi-Rate audio (AMR) codec file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-202"><span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**WMDM \_ Formatcode \_ undefinedvideo**</span><span class="sxs-lookup"><span data-stu-id="037a4-202"><span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**WMDM\_FORMATCODE\_UNDEFINEDVIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-203">Formatieren von Code für eine Videodatei mit einem nicht definierten Typ.</span><span class="sxs-lookup"><span data-stu-id="037a4-203">Format code for a video file with an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-204"><span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**WMDM \_ Formatcode \_ WMV**</span><span class="sxs-lookup"><span data-stu-id="037a4-204"><span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**WMDM\_FORMATCODE\_WMV**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-205">Formatieren von Code für eine Windows Media Video Datei (WMV).</span><span class="sxs-lookup"><span data-stu-id="037a4-205">Format code for a Windows Media Video (WMV) file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-206"><span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**WMDM \_ Formatcode \_ MP4**</span><span class="sxs-lookup"><span data-stu-id="037a4-206"><span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**WMDM\_FORMATCODE\_MP4**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-207">Formatieren von Code für eine MP4-Datei.</span><span class="sxs-lookup"><span data-stu-id="037a4-207">Format code for an MP4 file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-208"><span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**WMDM- \_ Formatcode- \_ MP2**</span><span class="sxs-lookup"><span data-stu-id="037a4-208"><span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**WMDM\_FORMATCODE\_MP2**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-209">Formatieren von Code für eine MP2-Datei.</span><span class="sxs-lookup"><span data-stu-id="037a4-209">Format code for an MP2 file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-210"><span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span>**WMDM \_ Formatcode \_ 3G2**</span><span class="sxs-lookup"><span data-stu-id="037a4-210"><span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span> **WMDM\_FORMATCODE\_3G2**</span></span> 
</dt> <dd>

<span data-ttu-id="037a4-211">Formatieren Sie den Code für das 3G2-multimediacontainerformat (3GPP2).</span><span class="sxs-lookup"><span data-stu-id="037a4-211">Format code for a 3G2 (3GPP2) multimedia container format.</span></span> <span data-ttu-id="037a4-212">Eine Datei mit diesem Typ kann Audiodateien, Videos oder Text enthalten.</span><span class="sxs-lookup"><span data-stu-id="037a4-212">A file of this type may contain audio, video, or text.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-213"><span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span>**WMDM \_ Formatcode \_ AVCHD**</span><span class="sxs-lookup"><span data-stu-id="037a4-213"><span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span> **WMDM\_FORMATCODE\_AVCHD**</span></span> 
</dt> <dd>

<span data-ttu-id="037a4-214">Formatieren von Code für eine AVCHD-Videodatei (Advanced Video Coding High Definition).</span><span class="sxs-lookup"><span data-stu-id="037a4-214">Format code for an AVCHD (Advanced Video Coding High Definition) video file.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-215"><span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span>**WMDM \_ Formatcode- \_ atscts**</span><span class="sxs-lookup"><span data-stu-id="037a4-215"><span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span> **WMDM\_FORMATCODE\_ATSCTS**</span></span> 
</dt> <dd>

<span data-ttu-id="037a4-216">Formatieren Sie den Code für den Format Standard des Advanced Fernsehen Systems Committee (atscts).</span><span class="sxs-lookup"><span data-stu-id="037a4-216">Format code for the Advanced Television Systems Committee (ATSCTS) format standard.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-217"><span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span>**WMDM \_ Formatcode \_ dvbts**</span><span class="sxs-lookup"><span data-stu-id="037a4-217"><span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span> **WMDM\_FORMATCODE\_DVBTS**</span></span> 
</dt> <dd>

<span data-ttu-id="037a4-218">Formatieren Sie den Code für ein MPEG-2-Video und MPEG-1 Layer II-oder AC-3-Audiodaten innerhalb eines mit einem DVB kompatiblen MPEG-2-Transport Datenstroms.</span><span class="sxs-lookup"><span data-stu-id="037a4-218">Format code for an MPEG-2 video and MPEG-1 Layer II, or AC-3, audio within a DVB-compliant MPEG-2 Transport Stream.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-219"><span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM \_ Formatcode \_ undefinedcollection**</span><span class="sxs-lookup"><span data-stu-id="037a4-219"><span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM\_FORMATCODE\_UNDEFINEDCOLLECTION**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-220">Formatieren von Code für eine Auflistung eines nicht definierten Typs.</span><span class="sxs-lookup"><span data-stu-id="037a4-220">Format code for a collection of an undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-221"><span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**WMDM \_ Formatcode \_ abstractmultimediaalbum**</span><span class="sxs-lookup"><span data-stu-id="037a4-221"><span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTMULTIMEDIAALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-222">Formatieren von Code für ein multimediarester, bei dem das Objekt die Eigenschaften eines Multimedia-Albums und optional Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="037a4-222">Format code for a multimedia album where the object contains the properties of a multimedia album and, optionally, data.</span></span> <span data-ttu-id="037a4-223">Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="037a4-223">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-224"><span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**WMDM \_ Formatcode \_ abstractimagealbum**</span><span class="sxs-lookup"><span data-stu-id="037a4-224"><span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**WMDM\_FORMATCODE\_ABSTRACTIMAGEALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-225">Formatieren von Code für ein Bild-Album, bei dem das-Objekt die Eigenschaften eines imagealbums und optional Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="037a4-225">Format code for an image album where the object contains the properties of an image album and, optionally, data.</span></span> <span data-ttu-id="037a4-226">Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="037a4-226">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-227"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**WMDM \_ Formatcode \_ abstractaudioalbum**</span><span class="sxs-lookup"><span data-stu-id="037a4-227"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTAUDIOALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-228">Formatieren von Code für ein Audioalbum, bei dem das-Objekt die Eigenschaften eines audioalbums und optional Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="037a4-228">Format code for an audio album where the object contains the properties of an audio album and, optionally, data.</span></span> <span data-ttu-id="037a4-229">Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="037a4-229">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-230"><span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**WMDM \_ Formatcode \_ abstractvideoalbum**</span><span class="sxs-lookup"><span data-stu-id="037a4-230"><span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**WMDM\_FORMATCODE\_ABSTRACTVIDEOALBUM**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-231">Formatieren von Code für ein Video Album, bei dem das-Objekt die Eigenschaften eines Video Albums und optional Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="037a4-231">Format code for a video album where the object contains the properties of a video album and, optionally, data.</span></span> <span data-ttu-id="037a4-232">Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="037a4-232">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-233"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**WMDM \_ Formatcode \_ abstractaudiovideoplaylist**</span><span class="sxs-lookup"><span data-stu-id="037a4-233"><span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**WMDM\_FORMATCODE\_ABSTRACTAUDIOVIDEOPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-234">Formatieren Sie Code für eine Audiowiedergabe-Wiedergabeliste, in der das-Objekt die Eigenschaften einer Audiowiedergabe-Wiedergabeliste und optional Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="037a4-234">Format code for an audio/video playlist where the object contains the properties of an audio/video playlist and, optionally, data.</span></span> <span data-ttu-id="037a4-235">Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="037a4-235">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-236"><span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**WMDM \_ Formatcode \_ abstractcontactgroup**</span><span class="sxs-lookup"><span data-stu-id="037a4-236"><span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**WMDM\_FORMATCODE\_ABSTRACTCONTACTGROUP**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-237">Formatieren Sie Code für eine Kontaktgruppe, in der das-Objekt die Eigenschaften einer Kontaktgruppe und optional Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="037a4-237">Format code for a contact group where the object contains the properties of a contact group and, optionally, data.</span></span> <span data-ttu-id="037a4-238">Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="037a4-238">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-239"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**WMDM \_ Formatcode \_ abstractmessagefolder**</span><span class="sxs-lookup"><span data-stu-id="037a4-239"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**WMDM\_FORMATCODE\_ABSTRACTMESSAGEFOLDER**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-240">Formatieren Sie den Code für einen Nachrichten Ordner, in dem das Objekt die Eigenschaften eines Nachrichten Ordners und optional Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="037a4-240">Format code for a message folder where the object contains the properties of a message folder and, optionally, data.</span></span> <span data-ttu-id="037a4-241">Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="037a4-241">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-242"><span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**WMDM \_ Formatcode \_ abstractchapteredproduction**</span><span class="sxs-lookup"><span data-stu-id="037a4-242"><span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**WMDM\_FORMATCODE\_ABSTRACTCHAPTEREDPRODUCTION**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-243">Formatieren Sie den Code für eine in einem Kapitel enthaltene Produktionsumgebung, in der das-Objekt die Eigenschaften einer in Kapitel unterteilten Produktion und optional Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="037a4-243">Format code for a chaptered production where the object contains the properties of a chaptered production and, optionally, data.</span></span> <span data-ttu-id="037a4-244">Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="037a4-244">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-245"><span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**WMDM- \_ Formatcode \_ wplwiedergabe**</span><span class="sxs-lookup"><span data-stu-id="037a4-245"><span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**WMDM\_FORMATCODE\_WPLPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-246">Formatieren von Code für eine Wiedergabeliste, die mit der Formatierung der Windows Media-Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="037a4-246">Format code for a playlist formatted with Windows Media playlist formatting.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-247"><span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**WMDM- \_ Formatcode \_ M3UPLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="037a4-247"><span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**WMDM\_FORMATCODE\_M3UPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-248">Formatieren von Code für eine Wiedergabeliste mit m3u-Formatierung.</span><span class="sxs-lookup"><span data-stu-id="037a4-248">Format code for a playlist with M3U formatting.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-249"><span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**WMDM \_ Formatcode- \_ mplwiedergabe**</span><span class="sxs-lookup"><span data-stu-id="037a4-249"><span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**WMDM\_FORMATCODE\_MPLPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-250">Formatieren von Code für eine Wiedergabeliste mit MPL-Formatierung.</span><span class="sxs-lookup"><span data-stu-id="037a4-250">Format code for a playlist with MPL formatting.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-251"><span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**WMDM \_ Formatcode \_ asxwiedergabe**</span><span class="sxs-lookup"><span data-stu-id="037a4-251"><span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**WMDM\_FORMATCODE\_ASXPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-252">Formatieren von Code für eine Wiedergabeliste mit der ASX-Formatierung.</span><span class="sxs-lookup"><span data-stu-id="037a4-252">Format code for a playlist with ASX formatting.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-253"><span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**WMDM \_ Formatcode \_ plsplaylist**</span><span class="sxs-lookup"><span data-stu-id="037a4-253"><span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**WMDM\_FORMATCODE\_PLSPLAYLIST**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-254">Formatieren von Code für eine Wiedergabeliste mit pls-Formatierung.</span><span class="sxs-lookup"><span data-stu-id="037a4-254">Format code for a playlist with PLS formatting.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-255"><span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**WMDM \_ Formatcode \_ undefineddocument**</span><span class="sxs-lookup"><span data-stu-id="037a4-255"><span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**WMDM\_FORMATCODE\_UNDEFINEDDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-256">Formatieren von Code für ein Dokument mit nicht definiertem Typ.</span><span class="sxs-lookup"><span data-stu-id="037a4-256">Format code for a document of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-257"><span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**WMDM \_ Formatcode \_ AbstractDocument**</span><span class="sxs-lookup"><span data-stu-id="037a4-257"><span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**WMDM\_FORMATCODE\_ABSTRACTDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-258">Formatieren von Code für ein Dokument, in dem das Objekt die Eigenschaften eines Dokuments und optional Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="037a4-258">Format code for a document where the object contains the properties of a document and, optionally, data.</span></span> <span data-ttu-id="037a4-259">Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="037a4-259">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-260"><span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**WMDM \_ Formatcode \_ XmlDocument**</span><span class="sxs-lookup"><span data-stu-id="037a4-260"><span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**WMDM\_FORMATCODE\_XMLDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-261">Formatieren von Code für ein XML-Dokument.</span><span class="sxs-lookup"><span data-stu-id="037a4-261">Format code for an XML document.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-262"><span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**WMDM \_ Formatcode \_ microsoftworddocument**</span><span class="sxs-lookup"><span data-stu-id="037a4-262"><span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**WMDM\_FORMATCODE\_MICROSOFTWORDDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-263">Formatieren von Code für ein Microsoft Word-Dokument.</span><span class="sxs-lookup"><span data-stu-id="037a4-263">Format code for a Microsoft Word document.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-264"><span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**WMDM \_ Formatcode \_ mhtcompiledhtmldocument**</span><span class="sxs-lookup"><span data-stu-id="037a4-264"><span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**WMDM\_FORMATCODE\_MHTCOMPILEDHTMLDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-265">Formatieren von Code für ein kompiliertes HTML-Dokument</span><span class="sxs-lookup"><span data-stu-id="037a4-265">Format code for a compiled HTML document.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-266"><span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**WMDM \_ Formatcode- \_ mikrosoftexcelkalkulations Tabelle**</span><span class="sxs-lookup"><span data-stu-id="037a4-266"><span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**WMDM\_FORMATCODE\_MICROSOFTEXCELSPREADSHEET**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-267">Formatieren von Code für eine Microsoft Excel-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="037a4-267">Format code for a Microsoft Excel spreadsheet.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-268"><span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**WMDM \_ Formatcode \_ microsoftpowerpointdocument**</span><span class="sxs-lookup"><span data-stu-id="037a4-268"><span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**WMDM\_FORMATCODE\_MICROSOFTPOWERPOINTDOCUMENT**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-269">Formatieren von Code für ein Microsoft PowerPoint-Dokument.</span><span class="sxs-lookup"><span data-stu-id="037a4-269">Format code for a Microsoft PowerPoint document.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-270"><span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**WMDM \_ Formatcode \_ undefinedmessage**</span><span class="sxs-lookup"><span data-stu-id="037a4-270"><span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**WMDM\_FORMATCODE\_UNDEFINEDMESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-271">Formatieren Sie Code für eine Meldung mit einem nicht definierten Typ.</span><span class="sxs-lookup"><span data-stu-id="037a4-271">Format code for a message of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-272"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**WMDM \_ Formatcode \_ abstractmessage**</span><span class="sxs-lookup"><span data-stu-id="037a4-272"><span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**WMDM\_FORMATCODE\_ABSTRACTMESSAGE**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-273">Formatieren von Code für eine Nachricht, bei der das-Objekt die Eigenschaften einer Nachricht und optional Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="037a4-273">Format code for a message where the object contains the properties of a message and, optionally, data.</span></span> <span data-ttu-id="037a4-274">Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="037a4-274">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-275"><span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**WMDM- \_ Formatcode \_ undefinedcontact**</span><span class="sxs-lookup"><span data-stu-id="037a4-275"><span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**WMDM\_FORMATCODE\_UNDEFINEDCONTACT**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-276">Formatieren von Code für einen Kontakt mit einem nicht definierten Typ.</span><span class="sxs-lookup"><span data-stu-id="037a4-276">Format code for a contact of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-277"><span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**WMDM \_ Formatcode \_ abstractcontact**</span><span class="sxs-lookup"><span data-stu-id="037a4-277"><span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**WMDM\_FORMATCODE\_ABSTRACTCONTACT**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-278">Formatieren von Code für einen Kontakt, bei dem das Objekt die Eigenschaften eines Kontakts und optional Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="037a4-278">Format code for a contact where the object contains the properties of a contact and, optionally, data.</span></span> <span data-ttu-id="037a4-279">Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="037a4-279">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-280"><span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**WMDM- \_ Formatcode \_ VCARD2**</span><span class="sxs-lookup"><span data-stu-id="037a4-280"><span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**WMDM\_FORMATCODE\_VCARD2**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-281">Formatieren von Code für eine elektronische Karte mit vCard-Formatierung, Version 2.</span><span class="sxs-lookup"><span data-stu-id="037a4-281">Format code for an electronic card with vcard version 2 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-282"><span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**WMDM- \_ Formatcode \_ VCARD3**</span><span class="sxs-lookup"><span data-stu-id="037a4-282"><span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**WMDM\_FORMATCODE\_VCARD3**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-283">Formatieren Sie Code für eine elektronische Karte mit vCard-Formatierung, Version 3.</span><span class="sxs-lookup"><span data-stu-id="037a4-283">Format code for an electronic card with vcard version 3 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-284"><span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**WMDM \_ Formatcode \_ undefinedcalendaritem**</span><span class="sxs-lookup"><span data-stu-id="037a4-284"><span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**WMDM\_FORMATCODE\_UNDEFINEDCALENDARITEM**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-285">Formatieren von Code für ein elektronisches Kalender Element mit nicht definiertem Typ.</span><span class="sxs-lookup"><span data-stu-id="037a4-285">Format code for an electronic calendar item of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-286"><span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**WMDM \_ Formatcode \_ abstractcalendaritem**</span><span class="sxs-lookup"><span data-stu-id="037a4-286"><span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**WMDM\_FORMATCODE\_ABSTRACTCALENDARITEM**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-287">Formatieren von Code für ein Kalender Element, bei dem das-Objekt die Eigenschaften eines Kalender Elements und optional Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="037a4-287">Format code for a calendar item where the object contains the properties of a calendar item and, optionally, data.</span></span> <span data-ttu-id="037a4-288">Alle enthaltenen Daten haben ein nicht definiertes Format in Bezug auf die MTP-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="037a4-288">Any contained data is of an undefined format with respect to the MTP specification.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-289"><span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**WMDM- \_ Formatcode \_ VCALENDAR1**</span><span class="sxs-lookup"><span data-stu-id="037a4-289"><span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**WMDM\_FORMATCODE\_VCALENDAR1**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-290">Formatieren von Code für ein elektronisches Kalender Element mit der vCalendar Version 1-Formatierung.</span><span class="sxs-lookup"><span data-stu-id="037a4-290">Format code for an electronic calendar item with vcalendar version 1 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-291"><span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**WMDM- \_ Formatcode \_ VCALENDAR2**</span><span class="sxs-lookup"><span data-stu-id="037a4-291"><span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**WMDM\_FORMATCODE\_VCALENDAR2**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-292">Formatieren Sie den Code für ein elektronisches Kalender Element mit Formatierung von vCalendar Version 2.</span><span class="sxs-lookup"><span data-stu-id="037a4-292">Format code for an electronic calendar item with vcalendar version 2 formatting.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-293"><span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**WMDM \_ Formatcode \_ undefinedwindowsexecutor**</span><span class="sxs-lookup"><span data-stu-id="037a4-293"><span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**WMDM\_FORMATCODE\_UNDEFINEDWINDOWSEXECUTABLE**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-294">Formatieren von Code für eine Windows-basierte ausführbare Datei des undefinierten Typs.</span><span class="sxs-lookup"><span data-stu-id="037a4-294">Format code for a Windows-based executable of undefined type.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-295"><span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**WMDM- \_ Formatcode- \_ Medien Umwandlung \_**</span><span class="sxs-lookup"><span data-stu-id="037a4-295"><span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**WMDM\_FORMATCODE\_MEDIA\_CAST**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-296">Formatieren von Code für ein Medienobjekt.</span><span class="sxs-lookup"><span data-stu-id="037a4-296">Format code for a media cast object.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-297"><span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**Abschnitt "WMDM \_ Formatcode" \_**</span><span class="sxs-lookup"><span data-stu-id="037a4-297"><span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**WMDM\_FORMATCODE\_SECTION**</span></span>
</dt> <dd>

<span data-ttu-id="037a4-298">Formatieren von Code für einen Abschnitt von Daten, der in einem anderen Objekt enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="037a4-298">Format code for a section of data that is contained in another object.</span></span>

</dd> <dt>

<span data-ttu-id="037a4-299"><span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span>**WMDM \_ Formatcode \_ 3g2a**</span><span class="sxs-lookup"><span data-stu-id="037a4-299"><span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span> **WMDM\_FORMATCODE\_3G2A**</span></span> 
</dt> <dd>

<span data-ttu-id="037a4-300">Formatieren Sie den Code für ein 3g2a-multimediacontainerformat (3gpp2a).</span><span class="sxs-lookup"><span data-stu-id="037a4-300">Format code for a 3G2A (3GPP2A) multimedia container format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="037a4-301">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="037a4-301">Remarks</span></span>

<span data-ttu-id="037a4-302">Zum Ermitteln der Formate, die von einem Gerät unterstützt werden, kann eine Anwendung [**IWMDMDevice3:: GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) verwenden, um die Eigenschaft " **g \_ wszwmdmformatssupported** Device" abzufragen.</span><span class="sxs-lookup"><span data-stu-id="037a4-302">To discover the formats supported by a device, an application can use [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) to query the **g\_wszWMDMFormatsSupported** device property.</span></span>

<span data-ttu-id="037a4-303">Eine Anwendung kann [**IWMDMDevice3:: getformatcapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)aufrufen, um Gerätefunktionen für ein bestimmtes Format zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="037a4-303">To discover device capabilities for a particular format, an application can call [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability).</span></span>

<span data-ttu-id="037a4-304">Eine Anwendung kann den Formatierungs Code beim Erstellen eines Speichers auf dem Gerät festlegen, indem Sie die **g \_ wszwmdmformatcode** -Eigenschaft in Metadaten einschließt, die im *pMetaData* -Parameter eines Aufrufens von [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="037a4-304">An application can set the format code while creating a storage on device by including the **g\_wszWMDMFormatCode** property in metadata passed in the *pMetaData* parameter of a call to [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).</span></span>

<span data-ttu-id="037a4-305">Eine Anwendung kann den Format Code eines Speichers Abfragen, indem [**IWMDMStorage3:: GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) oder [**IWMDMStorage4:: getspecifiedmetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) aufgerufen und die Eigenschaft **g \_ wszwmdmformatcode** abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="037a4-305">An application can query the format code of a storage by calling [**IWMDMStorage3::GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) or [**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) and retrieving the **g\_wszWMDMFormatCode** property.</span></span>

<span data-ttu-id="037a4-306">Wenn das Gerät das Festlegen des Formatcodes nach der Speicher Erstellung unterstützt, kann eine Anwendung [**IWMDMStorage3:: SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) verwenden, um die Eigenschaft " **g \_ wszwmdmformatcode** " festzulegen.</span><span class="sxs-lookup"><span data-stu-id="037a4-306">If the device supports setting the format code after the creation of storage, an application can use [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) to set the **g\_wszWMDMFormatCode** property.</span></span> <span data-ttu-id="037a4-307">Einige Geräte erlauben möglicherweise nicht das Ändern des Formatcodes, nachdem der Speicher auf dem Gerät erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="037a4-307">Some devices may not allow changing the format code after the storage is created on the device.</span></span> <span data-ttu-id="037a4-308">Daher wird dringend empfohlen, diese Eigenschaft zusammen mit den in [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) übergebenen Metadaten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="037a4-308">Therefore, setting this property along with the metadata passed in [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) is strongly recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="037a4-309">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="037a4-309">Requirements</span></span>



| <span data-ttu-id="037a4-310">Anforderung</span><span class="sxs-lookup"><span data-stu-id="037a4-310">Requirement</span></span> | <span data-ttu-id="037a4-311">Wert</span><span class="sxs-lookup"><span data-stu-id="037a4-311">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="037a4-312">Header</span><span class="sxs-lookup"><span data-stu-id="037a4-312">Header</span></span><br/> | <dl> <span data-ttu-id="037a4-313"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="037a4-313"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="037a4-314">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="037a4-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="037a4-315">**Enumerationstypen**</span><span class="sxs-lookup"><span data-stu-id="037a4-315">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="037a4-316">**IWMDMDevice3:: getformatcapability**</span><span class="sxs-lookup"><span data-stu-id="037a4-316">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="037a4-317">**IWMDMDevice3:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="037a4-317">**IWMDMDevice3::GetProperty**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)
</dt> <dt>

[<span data-ttu-id="037a4-318">**IWMDMStorage3:: GetMetadata**</span><span class="sxs-lookup"><span data-stu-id="037a4-318">**IWMDMStorage3::GetMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)
</dt> <dt>

[<span data-ttu-id="037a4-319">**IWMDMStorage3:: SetMetadata**</span><span class="sxs-lookup"><span data-stu-id="037a4-319">**IWMDMStorage3::SetMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)
</dt> <dt>

[<span data-ttu-id="037a4-320">**IWMDMStorage4:: getspecifiedmetadata**</span><span class="sxs-lookup"><span data-stu-id="037a4-320">**IWMDMStorage4::GetSpecifiedMetadata**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)
</dt> <dt>

[<span data-ttu-id="037a4-321">**IWMDMStorageControl3::Insert3**</span><span class="sxs-lookup"><span data-stu-id="037a4-321">**IWMDMStorageControl3::Insert3**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)
</dt> <dt>

[<span data-ttu-id="037a4-322">**Metadatenkonstanten**</span><span class="sxs-lookup"><span data-stu-id="037a4-322">**Metadata Constants**</span></span>](metadata-constants.md)
</dt> </dl>

 

 





