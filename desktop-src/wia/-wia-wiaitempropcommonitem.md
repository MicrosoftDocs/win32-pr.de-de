---
description: Die folgenden Geräteeigenschaften Konstanten müssen von allen iwiaitem-, IWiaItem2-und iwiadrvitem-Schnittstellen Schnittstellen unterstützt werden, sofern in ihren Beschreibungen nichts anderes angegeben ist.
ms.assetid: ef48313e-4df4-4ccd-a085-f714100885a7
title: Allgemeine WIA-Element Eigenschaften Konstanten (wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPA_ACCESS_RIGHTS
- WIA_IPA_APP_COLOR_MAPPING
- WIA_IPA_BITS_PER_CHANNEL
- WIA_IPA_BUFFER_SIZE
- WIA_IPA_BYTES_PER_LINE
- WIA_IPA_CHANNELS_PER_PIXEL
- WIA_IPA_COLOR_PROFILE
- WIA_IPA_COMPRESSION
- WIA_IPA_DATATYPE
- WIA_IPA_DEPTH
- WIA_IPA_FILENAME_EXTENSION
- WIA_IPA_FORMAT
- WIA_IPA_FULL_ITEM_NAME
- WIA_IPA_GAMMA_CURVES
- WIA_IPA_ICM_PROFILE_NAME
- WIA_IPA_ITEM_CATEGORY
- WIA_IPA_ITEM_FLAGS
- WIA_IPA_ITEM_NAME
- WIA_IPA_ITEM_SIZE
- WIA_IPA_ITEM_TIME
- WIA_IPA_ITEMS_STORED
- WIA_IPA_MIN_BUFFER_SIZE
- WIA_IPA_NUMBER_OF_LINES
- WIA_IPA_PIXELS_PER_LINE
- WIA_IPA_PLANAR
- WIA_IPA_PREFERRED_FORMAT
- WIA_IPA_PROP_STREAM_COMPAT_ID
- WIA_IPA_RAW_BITS_PER_CHANNEL
- WIA_IPA_REGION_TYPE
- WIA_IPA_SUPPRESS_PROPERTY_PAGE
- WIA_IPA_TYMED
- WIA_IPA_UPLOAD_ITEM_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: d36a390256c6a9d183caa0f9231d2a92035d83da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344453"
---
# <a name="common-wia-item-property-constants"></a>Allgemeine WIA-Element Eigenschaften Konstanten

Die folgenden Geräteeigenschaften Konstanten müssen von allen [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)-, [**IWiaItem2**](-wia-iwiaitem2.md) -und [iwiadrvitem-Schnittstellen](https://msdn.microsoft.com/library/ms793976.aspx) Schnittstellen unterstützt werden, sofern in ihren Beschreibungen nichts anderes angegeben ist.

Das Präfix "WIA \_ IPA \_ " gibt eine Element Eigenschaft für alle Geräte an und ist die Benennungs Konvention, die in C/C++ verwendet wird. Bei der Skripterstellung verwenden diese Konstanten das Präfix "Bild" und sind Teil des enumerierten Typs " [wiaitempropertyid](-wia-wiaitempropertyid.md) ". Der entsprechende Elementname aus dieser Skript Enumeration wird in Klammern neben dem Konstanten Namen C/C++ in der folgenden Liste angezeigt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante/Wert</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ACCESS_RIGHTS"></span><span id="wia_ipa_access_rights"></span><dl> <dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>pictureaccessrights</dt> </dl></td>
<td style="text-align: left;">Dieses Flag steuert den Zugriff auf das Element und gibt an, ob das Element gelöscht wird.<br/> Erforderlich für alle WIA 2,0-Elemente.<br/> Typ: <strong>VT_I4</strong>; Lese-/Schreibzugriff oder schreibgeschützt, abhängig von der Fähigkeit des Elements, die Zugriffsrechte zu ändern; Gültige Werte: WIA_PROP_FLAG<br/> Die folgende Tabelle enthält die fünf Flags, die mit dieser Eigenschaft gültig sind.<br/> 
<table>
<thead>
<tr class="header">
<th>Zugriffsrecht</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_ITEM_READ</td>
<td>Das Element hat schreibgeschützten Zugriff.</td>
</tr>
<tr class="even">
<td>WIA_ITEM_WRITE</td>
<td>Das Element hat schreibgeschützten Zugriff.</td>
</tr>
<tr class="odd">
<td>WIA_ITEM_CAN_BE_DELETED</td>
<td>Das Element hat nur den Lösch Zugriff.</td>
</tr>
<tr class="even">
<td>WIA_ITEM_RD</td>
<td>WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</td>
</tr>
<tr class="odd">
<td>WIA_ITEM_RWD</td>
<td>WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_APP_COLOR_MAPPING"></span><span id="wia_ipa_app_color_mapping"></span><dl> <dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>pictureappcolormapping</dt> </dl></td>
<td style="text-align: left;"><p>Diese Eigenschaft ist für die zukünftige Verwendung reserviert und wird zu diesem Zeitpunkt nicht implementiert.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BITS_PER_CHANNEL"></span><span id="wia_ipa_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>picturebitsperchannel</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die Anzahl der Bits pro Kanal für das Bild. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Erforderlich für alle Erfassungs fähigen oder gespeicherten Bildelemente von WIA 2,0.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_BUFFER_SIZE"></span><span id="wia_ipa_buffer_size"></span><dl> <dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>picturebuffersize</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die Größe des Puffers in Bytes, der während einer Datenübertragung verwendet wird. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung kann diese Eigenschaft lesen, um die vom Treiber angegebene Puffergröße für Datenübertragungen zu ermitteln. Der WIA-Dienst liest auch diese Eigenschaft, um während der Datenübertragung Arbeitsspeicher für den Mini Treiber zuzuweisen.</p>
<p>Optional für alle für die Übertragung aktivierten WIA 2,0-Elemente.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<div class="alert">
<blockquote>
[!Note]<br />
Die <strong>WIA_IPA_BUFFER_SIZE</strong> -Eigenschaft enthält die minimale Datenmenge, die von einer Anwendung zu einem beliebigen Zeitpunkt angefordert werden kann. Je größer die Puffergröße ist, desto größer sind die Anforderungen an das Gerät. Dies kann dazu führen, dass das Gerät langsam und nicht mehr reagiert, die Gesamtleistung des Systems verlangsamt und übermäßige Ressourcen beanspruchen kann. Puffergrößen, die zu klein sind, können die Leistung der Datenübertragung beeinträchtigen, da viele kleinere Anforderungen erforderlich sind. Wählen Sie eine angemessene Puffergröße aus, indem Sie die typische Größe einer Daten Anforderung an Ihr Gerät berücksichtigen und die Anzahl der Anforderungen mit der Größe dieser Anforderungen ausgleichen.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BYTES_PER_LINE"></span><span id="wia_ipa_bytes_per_line"></span><dl> <dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>picturebytesperline</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die Anzahl der Bytes in einer Scan Zeile des Bilds. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Optional für alle WIA 2,0-Elemente.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_CHANNELS_PER_PIXEL"></span><span id="wia_ipa_channels_per_pixel"></span><dl> <dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>picturechannelsperpixel</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die Anzahl der Kanäle pro Pixel für das Bild. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Erforderlich für alle Erfassungs fähigen oder gespeicherten Bildelemente von WIA 2,0.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_COLOR_PROFILE"></span><span id="wia_ipa_color_profile"></span><dl> <dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> von " <dt>picturecolorprofile</dt> " </dl></td>
<td style="text-align: left;"><p>Diese Eigenschaft ist für die zukünftige Verwendung reserviert und wird zu diesem Zeitpunkt nicht implementiert.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_COMPRESSION"></span><span id="wia_ipa_compression"></span><dl> <dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>picturecompression</dt> </dl></td>
<td style="text-align: left;"><p>Enthält den verwendeten aktuellen Komprimierungstyp. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung liest diese Eigenschaft, um den Bild Komprimierungstyp zu bestimmen, oder legt diese Eigenschaft fest, um die Komprimierungs Einstellung zu konfigurieren.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind. Das Symbol <strong>V</strong> gibt an, dass die Konstante nur in Windows Vista und höher unterstützt wird. (Er ist nur über die <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> -Schnittstelle verfügbar.)</p>

<table>
<thead>
<tr class="header">
<th>Komprimierungstyp</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_COMPRESSION_NONE</td>
<td>Keine Komprimierung. Weitere Informationen finden <strong>Sie unter Hinweis</strong> .</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_AUTO</td>
<td>Automatischer Komprimierungs Modus. Weitere Informationen finden <strong>Sie unter Hinweis</strong> .</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_BI_RLE4</td>
<td>RLE4-Komprimierung</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_BI_RLE8</td>
<td>RLE8-Komprimierung</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_G3</td>
<td>Komprimierung in Gruppe 3</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_G4</td>
<td>Komprimierung in Gruppe 4</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_JPEG</td>
<td>JPEG-Komprimierung.</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_JBIG<strong>V</strong></td>
<td>JBIG-Komprimierung.</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_JPEG2K<strong>V</strong></td>
<td>JPEG 2000-Komprimierung.</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_PNG<strong>V</strong></td>
<td>PNG-Komprimierung.</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
<p>[!Note]</p>
<p>Wenn diese Eigenschaft WIA_COMPRESSION_NONE ist und WIA_IPA_FORMAT entweder WiaImgFmt_PDFA oder WiaImgFmt_XPS ist; WIA_COMPRESSION_NONE bedeutet dann, dass der Komprimierungs Modus nicht definiert ist und der Scanner einen Modus treffen muss.</p>
<p>WIA_COMPRESSION_AUTO ist ein neuer Eigenschafts Wert, der für die WIA_IPA_COMPRESSION-Eigenschaft definiert ist. Dieser Wert gilt für alle programmierbaren Image-Datenquellen Elemente, einschließlich des Flatbed und des Feeds. Wenn dieser Wert vom WIA-Mini Treiber unterstützt wird, kann der WIA-Anwendungs Client WIA_IPA_COMPRESSION festlegen, um die automatische Komprimierung des Komprimierungs Modus auf dem Gerät zu aktivieren. WIA_COMPRESSION_AUTO kann mit und ohne vollständige automatische Farbe unterstützt oder aktiviert werden (WIA_DATA_AUTO und WIA_DEPTH_AUTO).</p>
<p>WIA_COMPRESSION_AUTO ist besonders nützlich bei Übertragungs Dateiformaten, die mehrere Datentypen und Bitraten unterstützen, z. b. WiaImgFmt_RAW. Weitere Informationen zu Übertragungs Dateiformaten finden Sie unter WIA_IPA_FORMAT in dieser Tabelle.</p>
<p>Es ist opitonale, wenn der WIA-Mini Treiber WIA_COMPRESSION_AUTO unterstützt. Wenn es unterstützt wird, darf der WIA-Mini Treiber ihn nie als Standardwert für WIA_IPA_COMPRESSION festlegen. Dieser Wert kann nur von der WIA-Anwendung festgelegt werden.</p>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_DATATYPE"></span><span id="wia_ipa_datatype"></span><dl> <dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>picturedatatype</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die aktuelle Datentyp Einstellung für das Gerät. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung liest diese Eigenschaft, um den Datentyp des Bilds zu bestimmen. Diese Eigenschaft wird von einer Anwendung geschrieben, um den aktuellen Datentyp des zu übertragenden Bilds festzulegen.</p>
<p>Diese Eigenschaft ist für alle WIA 2,0-Elemente erforderlich. Der Lese-/Schreibzugriff muss für alle für WIA 2,0 Erwerbs aktivierten Elemente und für WIA 2,0-Speicherelemente schreibgeschützt sein.</p>
<p>Typ: <strong>VT_I4</strong>; Zugriff für Windows Vista-Betriebssysteme vor Windows Vista: Diese Eigenschaft ist für Kameras und Lese-/Schreibzugriff auf Scanner schreibgeschützt. Access für Windows Vista und höher: Diese Eigenschaft ist nur für WIA_CATEGORY_FOLDER-und WIA_CATEGORY_FINISHED_FILE Elemente und Lese-/Schreibzugriff für alle anderen WIA 2,0-Element Kategorien schreibgeschützt. Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die sechs Konstanten, die mit gültig sind, wenn <strong>WIA_IPA_FORMAT</strong> nicht auf WiaImgFmt_RAW festgelegt ist.</p>

<table>
<thead>
<tr class="header">
<th>Datentyp</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DATA_AUTO</td>
<td>Gültig für alle programmierbaren Image-Datenquellen Elemente, einschließlich des Flatbed und des Feeds. Wenn dieser Wert vom WIA-Mini Treiber unterstützt wird, kann der WIA-Anwendungs Client WIA_IPA_DATATYPE festlegen, um die automatische Farberkennung auf dem Gerät zu aktivieren. Wenn WIA_DATA_AUTO festgelegt ist, muss der WIA-Mini Treiber WIA_IPA_DEPTH auf demselben Element auf WIA_DEPTH_AUTO aktualisieren (Dies muss ein unterstützter Wert sein, wenn das Gerät automatische Farbe unterstützt).<br/> Dies ist ein optionaler Wert, der jedoch erforderlich ist, wenn WIA_DEPTH_AUTO für WIA_IPA_DEPTH unterstützt wird.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR</td>
<td>Scan Daten sind rot, grün, blau (RGB). Das vollständige Farb Format wird mit den folgenden WIA-Eigenschaften beschrieben: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong><br/> <strong>WIA_IPA_BITS_PER_CHANNEL</strong><br/> <strong>WIA_IPA_PLANAR</strong><br/> <strong>WIA_IPA_PIXELS_PER_LINE</strong><br/> <strong>WIA_IPA_BYTES_PER_LINE</strong><br/> <strong>WIA_IPA_NUMBER_OF_LINES</strong><br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_COLOR_DITHER</td>
<td>Identisch mit WIA_DATA_COLOR, mit dem Unterschied, dass die Daten mit dem aktuell ausgewählten Dithering-Muster ausgeblendet werden.</td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR_THRESHOLD</td>
<td>Identisch mit WIA_DATA_COLOR, mit dem Unterschied, dass der Schwellenwert beim Scannen der Daten verwendet wird. Farbwerte für den <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> Wert werden in vollständige Helligkeit konvertiert. Farben unter diesem Wert werden in schwarz konvertiert.</td>
</tr>
<tr class="odd">
<td>WIA_DATA_DITHER</td>
<td>Scandaten werden mit dem aktuell ausgewählten Dithering-Muster ausgeblendet.</td>
</tr>
<tr class="even">
<td>WIA_DATA_GRAYSCALE</td>
<td>Scan Daten repräsentieren die Intensität. Die Palette ist eine festgelegte, gleichmäßig entfernte graue Größe mit einer Tiefe, die durch <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> -Eigenschaft angegeben wird.</td>
</tr>
<tr class="odd">
<td>WIA_DATA_THRESHOLD</td>
<td>Der Schwellenwert ist ein Bit pro Pixel von schwarzen und weißen Daten. Daten über den aktuellen Wert <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> werden in weiß konvertiert. Daten unter diesem Wert werden in schwarz konvertiert.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Die <strong>WIA_IPA_DATATYPE</strong> -Eigenschaft wird auch verwendet, um den Typ der zu verwendenden rohdatenübertragung zu beschreiben, wenn die Anwendung WiaImgFmt_RAW festlegt. Der Treiber sollte die <strong>WIA_IPA_DATATYPE</strong> -Eigenschaft auf eine Liste zulässiger Werte festlegen, von denen die Anwendung eine Auswahl treffen kann.</p>
<p>Wenn das Gerät nur auf einen einzelnen Wert festgelegt werden kann, erstellen Sie einen <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> Typ, und platzieren Sie den gültigen Wert darin.</p>
<p>Überprüfen Sie die <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> -Eigenschaft, um die Bittiefe zu ermitteln. Diese Eigenschaft enthält in der Regel einen einzelnen Wert für Kameras.</p>
<p>In der folgenden Tabelle werden die Konstanten aufgelistet, die mit <strong>WIA_IPA_DATATYPE</strong> gültig sind, wenn <strong>WIA_IPA_FORMAT</strong> auf WiaImgFmt_RAW festgelegt ist.</p>

<table>
<thead>
<tr class="header">
<th>Datentyp</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DATA_GRAYSCALE</td>
<td>Scan Daten repräsentieren die Intensität. Die Palette ist eine festgelegte, gleichmäßig entfernte Graustufen mit einer Tiefe, die durch die <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> -Eigenschaft angegeben wird. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 1 festgelegt werden.</td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_BGR</td>
<td>Scandaten befinden sich im BGR-colorspace (blau-grün-rot). Das vollständige Farb Format wird mithilfe der folgenden Eigenschaften beschrieben: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a><br/> <a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a><br/> <a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a><br/> <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 3 festgelegt werden.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_CMY</td>
<td>Scandaten befinden sich in der "Cyan-Magenta-Yellow (CMY)"-colorspace. Das vollständige Farb Format wird mit denselben WIA-Eigenschaften wie in WIA_DATA_RAW_BGR beschrieben. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 3 festgelegt werden.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_CMYK</td>
<td>Scandaten befinden sich im "Cyan-Magenta-Yellow-Black (CMYK) ColorSpace". Das vollständige Farb Format wird mit denselben WIA-Eigenschaften wie in WIA_DATA_RAW_BGR beschrieben. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 4 festgelegt werden.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_RGB</td>
<td>Überprüfungs Daten befinden sich in der Farbe Rot-Grün-Blau (RGB). Das vollständige Farb Format wird mit denselben WIA-Eigenschaften wie in WIA_DATA_RAW_BGR beschrieben. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 3 festgelegt werden.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_YUV</td>
<td>Die Überprüfungs Daten befinden sich im YUV-colorspace (Leuchtkraft-Blue Difference-Red Difference). Das vollständige Farb Format wird mit denselben WIA-Eigenschaften wie in WIA_DATA_RAW_BGR beschrieben. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 3 festgelegt werden.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_YUVK</td>
<td>Scandaten befinden sich in der "Leuchtkraft-Blue Difference-Red Difference-Black (yuvk) ColorSpace". Das vollständige Farb Format wird mit denselben WIA-Eigenschaften wie in WIA_DATA_RAW_BGR beschrieben. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 4 festgelegt werden.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_DEPTH"></span><span id="wia_ipa_depth"></span><dl> <dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>picturetiefe</dt> </dl></td>
<td style="text-align: left;"><p>WIA_IPA_DEPTH enthält die Bittiefe-Einstellung eines Bilds. Der Mini Treiber erstellt und verwaltet diese Eigenschaft. Eine Anwendung liest diese Eigenschaft, um die Bittiefe-Einstellung des Bilds zu bestimmen. Die Anwendung kann diesen Wert möglicherweise auch auf die gewünschte Bittiefe festlegen.</p>
<p>Wenn das Gerät nur auf einen einzelnen Wert festgelegt werden kann, erstellen Sie einen <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> Typ, und platzieren Sie den gültigen Wert darin.</p>
<p>Diese Eigenschaft ist für alle WIA 2,0-Elemente erforderlich. Der Lese-/Schreibzugriff muss für alle für WIA 2,0 Erwerbs aktivierten Elemente und für WIA 2,0-Speicherelemente schreibgeschützt sein.</p>
<p>Typ: <strong>VT_I4</strong>; Zugriff für Windows Vista-Betriebssysteme vor Windows Vista: Lesen/Schreiben; Access für Windows Vista und höher: Diese Eigenschaft ist nur für WIA_CATEGORY_FOLDER-und WIA_CATEGORY_FINISHED_FILE Elemente und Lese-/Schreibzugriff für alle anderen WIA 2,0-Element Kategorien schreibgeschützt. Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>WIA_DEPTH_AUTO ist als 0 Bits pro Pixel definiert, und es handelt sich um einen neuen Eigenschafts Wert, der für die WIA_IPA_DEPTH definiert ist. Dieser Wert gilt für alle programmierbaren Image-Datenquellen Elemente, einschließlich des Flatbed und des Feeds. Wenn WIA_DEPTH_AUTO vom WIA-Mini Treiber unterstützt wird, kann der WIA-Anwendungs Client WIA_IPA_DEPTH auf diesen Wert festlegen, um die automatische Erkennung von Farben auf dem Gerät zu aktivieren. Wenn WIA_DEPTH_AUTO festgelegt ist, muss der WIA-Mini Treiber WIA_IPA_DATATYPE auf demselben Element auf WIA_DATA_AUTO aktualisieren (Dies muss ein unterstützter Wert sein, wenn das Gerät automatische Farbe unterstützt).</p>
<p>WIA_DEPTH_AUTO ist ein optionaler Wert, wird jedoch benötigt, wenn WIA_DATA_AUTO für WIA_IPA_DATATYPE unterstützt wird.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FILENAME_EXTENSION"></span><span id="wia_ipa_filename_extension"></span><dl> <dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>picturedateinameextension</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die Dateinamenerweiterung für ein bestimmtes Dateiformat. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Optional für alle für die Übertragung aktivierten WIA 2,0-Elemente.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Der Treiber aktualisiert diese Eigenschaft, um den aktuellen Wert der <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> -Eigenschaft widerzuspiegeln.</p>
<p>Wenn <strong>WIA_IPA_FORMAT</strong> z. b. WiaImgFmt_JPEG ist, sollte <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> <strong>JPG</strong>lauten. Wenn <strong>WIA_IPA_FORMAT</strong> WiaImgFmt_BMP ist, sollte WIA_IPA_FILENAME_EXTENSION BMP lauten.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Die Dateinamenerweiterung enthält nicht den Punkt.
</blockquote>
</div>
<div>
 
</div>
<p>Diese Eigenschaft wird für Treiber empfohlen, die Standardformate unterstützen und für Treiber erforderlich sind, die benutzerdefinierte Formate implementieren. Er informiert die Anwendung über die richtige Dateierweiterung, die während der Übertragung privat formatierter Dateien verwendet werden soll. Wenn z. b. der a. Datum Corporation einen WIA-Treiber erstellt hat, der eine Datei in einem neuen Format übertragen hat, könnte das Unternehmen eine Erweiterung von &quot; ADC angeben &quot; . Dies ermöglicht es Anwendungen, Daten in diesem Format in eine Datei zu übertragen und einen Dateinamen zu erstellen, z <em>. b. MyFile. ADC</em>, was für andere nützlich ist, die die neue Erweiterung verstanden haben.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_FORMAT"></span><span id="wia_ipa_format"></span><dl> <dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </dl></td>
<td style="text-align: left;"><p>Enthält das aktuelle Format des zu übertragenden Bilds.</p>
<p>Eine Anwendung liest diese Eigenschaft, um das Format des Abbilds zu ermitteln, das Sie erhalten soll. Diese Eigenschaft wird von einer Anwendung geschrieben, um das Format festzulegen. Diese Eigenschaft hängt von der <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> -Eigenschaft ab. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Wenn das Gerät nur auf einen einzelnen Wert festgelegt werden kann, erstellen Sie einen <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> Typ, und platzieren Sie den gültigen Wert darin.</p>
<p>Typ: <strong>CLSID</strong>, Access: Read/Write, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>In der folgenden Tabelle werden die Konstanten aufgelistet, die mit dieser Eigenschaft gültig sind. Das Sternchen * gibt an, dass die Konstante in Windows Vista nicht unterstützt wird. (Er ist nur über die <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>iwiaitem</strong></a> -Schnittstelle verfügbar.) Das doppelte Sternchen * * gibt an, dass die Konstante weder in Windows Server 2003 noch in Windows Vista unterstützt wird. Das Symbol <strong>V</strong> gibt an, dass die Konstante nur in Windows Vista und höher unterstützt wird. (Er ist nur über die <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> -Schnittstelle verfügbar.)</p>

<table>
<thead>
<tr class="header">
<th>Format</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaAudFmt_AIFF</td>
<td>AIFF-Audioformat</td>
</tr>
<tr class="even">
<td>WiaAudFmt_MP3</td>
<td>MP3-Audioformat</td>
</tr>
<tr class="odd">
<td>WiaAudFmt_WAV</td>
<td>WAV-Audioformat</td>
</tr>
<tr class="even">
<td>WiaAudFmt_WMA</td>
<td>WMA-Audioformat</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_ASF * *</td>
<td>ASF-Videoformat</td>
</tr>
<tr class="even">
<td>WiaImgFmt_AVI * *</td>
<td>AVI-Videoformat</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_BMP</td>
<td>Windows-Bitmap mit einer Header Datei</td>
</tr>
<tr class="even">
<td>WiaImgFmt_CIFF *</td>
<td>Kamerabild-Dateiformat</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_DPOF</td>
<td>DPOF-Druckformat</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EMF</td>
<td>Erweiterte Windows-Metadatendatei</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_EXEC</td>
<td>Ausführbare Datei</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EXIF</td>
<td>Austauschbares Datei Format</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_FLASHPIX</td>
<td>Format von Flash pix</td>
</tr>
<tr class="even">
<td>WiaImgFmt_GIF</td>
<td>GIF-Bildformat</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_HTML</td>
<td>HTML-Format</td>
</tr>
<tr class="even">
<td>WiaImgFmt_ICO</td>
<td>Windows-Symbol Dateiformat</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JBIG<strong>V</strong></td>
<td>Das gemeinsame Format der Abbildung Experts Group (JBIG) der bidirektionalen Ebene.</td>
</tr>
<tr class="even">
<td>WiaImgFmt_JPEG</td>
<td>Komprimiertes JPEG-Format</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JPEG2K</td>
<td>JPEG 2000 komprimiertes Format</td>
</tr>
<tr class="even">
<td>WiaImgFmt_JPEG2KX</td>
<td>JPEG 2000 komprimiertes Format</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_MEMORYBMP</td>
<td>Windows-Bitmap ohne Header Datei</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PDFA<strong>V</strong></td>
<td>Das Format PDF/A (ISO/CD 19005-1).</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_MPG * *</td>
<td>MPEG-Videoformat</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Eastman-Dateiformat von Kodak</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PICT</td>
<td>Apple-Dateiformat</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PNG</td>
<td>W3C-PNG-Format</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_RAW</td>
<td>Rohdaten Format nur für Datenübertragungen</td>
</tr>
<tr class="even">
<td>WiaImgFmt_RAWRGB</td>
<td>Formatierte RGB-Format</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_RTF</td>
<td>Rich-Text-Dateiformat</td>
</tr>
<tr class="even">
<td>WiaImgFmt_SCRIPT</td>
<td>Skriptdatei</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_TIFF</td>
<td>Tag Image File Format</td>
</tr>
<tr class="even">
<td>WiaImgFmt_TXT</td>
<td>Textdatei</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_UNICODE16</td>
<td>Unicode-16-Bit-Codierung</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>Windows-Metadatendatei</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_XML</td>
<td>XML-Datei:</td>
</tr>
<tr class="even">
<td>WiaImgFmt_XPS<strong>V</strong></td>
<td>XPS-Paketformat</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
Wenn diese Eigenschaft entweder WiaImgFmt_PDFA oder WiaImgFmt_XPS ist und WIA_IPA_COMPRESSION WIA_COMPRESSION_NONE ist. der letztere Wert bedeutet, dass der Komprimierungs Modus nicht definiert ist und der Scanner einen Modus treffen muss.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FULL_ITEM_NAME"></span><span id="wia_ipa_full_item_name"></span><dl> <dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>picturefullitemname</dt> </dl></td>
<td style="text-align: left;"><p>Enthält den vollständigen Elementnamen (der Elementname und die Pfadinformationen). Der vollständige Elementname ist identisch mit dem <em>bstraufullitemname</em> -Parameter der Dienstprogramm Funktion <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiaskreatedrvitem</a> . Eine Anwendung liest diese Eigenschaft, um zu bestimmen, welches Element aktuell verwendet wird und wo sich dieses Element in der Elementstruktur befindet. Jedes Element muss einen eindeutigen Namen aufweisen. Anwendungen verwenden häufig den vollständigen Elementnamen, um nach Elementen in der Elementstruktur zu suchen. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</p>
<p>Erforderlich für alle WIA 2,0-Elemente.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_GAMMA_CURVES"></span><span id="wia_ipa_gamma_curves"></span><dl> <dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> von " <dt>picturegammacurves</dt> " </dl></td>
<td style="text-align: left;"><p>Diese Eigenschaft ist für die zukünftige Verwendung reserviert und wird zurzeit nicht implementiert.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ICM_PROFILE_NAME"></span><span id="wia_ipa_icm_profile_name"></span><dl> <dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>pictureicmprofilename</dt> </dl></td>
<td style="text-align: left;"><p>Enthält den Namen des ICM-Profils, der zum ordnungsgemäßen Decodieren des Bilds erforderlich ist. Eine Anwendung liest diese Eigenschaft, um das bei der Verarbeitung des Abbilds zu verwendende ICM-Profil zu ermitteln. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft basierend auf dem Eintrag icmprofiles in der Treiber Installationsdatei.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_CATEGORY"></span><span id="wia_ipa_item_category"></span><dl> <dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>pictureitemcategory</dt> </dl></td>
<td style="text-align: left;"><p>Wird nur in Windows Vista und höher unterstützt.</p>
<p>WIA 2,0-Elemente sind in Kategorien unterteilt, die definieren, wie ein <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> behandelt oder verwendet werden soll. Wenn das Element z. b. einen feedvorgang darstellt, sollte die Anwendung erwarten, dass Sie die erforderlichen Eigenschaften für die Dokument feederstellung enthält und wie ein Dokument-feedvorgang funktioniert. Wenn das Element eine fertige Datei darstellt, sollte eine WIA 2,0-Anwendung diese auf diese Weise behandeln, wobei angenommen wird, dass die Daten statisch sind und sich auf dem Gerät befinden. (Die Regeln für jedes Element werden in den einzelnen Spezifikations Dokumenten definiert.)</p>
<p>Erforderlich für alle WIA 2,0-Elemente.</p>
<p>Typ: <strong>VT_CLSID</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-wia2-itemcategoryguids.md"><strong>Element Kategorie-GUIDs</strong></a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_FLAGS"></span><span id="wia_ipa_item_flags"></span><dl> <dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>pictureitemflags</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die beschreibenden Flags für ein WIA-Element. Die elementflags sind identisch mit denen im <em>lobjectflags</em> -Parameter der Dienstprogramm Funktion <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiaskreatedrvitem</a> . Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung liest diese Eigenschaft, um die beschreibenden Flagwerte des Elements zu bestimmen.</p>
<p>Typ: <strong>VT_I4</strong> Access: Read Only, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die folgende Tabelle enthält die Flags, die mit dieser Eigenschaft gültig sind. Ein Sternchen * gibt an, dass das Flag in Windows Vista oder höher nicht unterstützt wird. (Er ist nur über die <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>iwiaitem</strong></a> -Schnittstelle verfügbar.) Ein doppeltes Sternchen * * gibt an, dass das Flag weder in Windows Server 2003 noch in Windows Vista oder höher unterstützt wird. Das Symbol <strong>V</strong> gibt an, dass das Flag nur in Windows Vista und höher unterstützt wird. (Er ist nur über die <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> -Schnittstelle verfügbar.)</p>

<table>
<thead>
<tr class="header">
<th>Flag</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Wiaitemtypeanalysis *</td>
<td>Dieses Element unterstützt die <strong>iwiaitem:: analyzeitem</strong> -Methode (beschrieben in der Platform SDK-Dokumentation). Dieses Element unterstützt auch die automatische Generierung von untergeordneten Elementen. Diese Funktion ist nützlich für die Bereichs Erkennung oder die Seiten Zerlegung.</td>
</tr>
<tr class="even">
<td>Wiaitemtypeaudiodatei</td>
<td>Dieses Element unterstützt Audiodaten. Dieses Flag ist nur für Elemente gültig, für die das <strong>wiaitemtypefile</strong> -Flag ebenfalls festgelegt ist.</td>
</tr>
<tr class="odd">
<td>Wiaitemtypeburst *</td>
<td>Nur für Ordner. Dieses Flag gibt an, dass die Bilder in diesem Ordner in einer kontinuierlichen Zeitsequenz erstellt wurden.</td>
</tr>
<tr class="even">
<td>Wiaitemtypedeleted</td>
<td>Dieses Element ist zum Löschen markiert, dieses Element wurde gelöscht, dieses Element ist nicht vorhanden, oder der Inhalt dieses Elements ist ungültig.</td>
</tr>
<tr class="odd">
<td>Wiaitemtypedocument<strong>V</strong></td>
<td>Bei diesem Element handelt es sich um eine Dokument Datei in einem Dokumentformat, das in der <strong>WIA_IPA_FORMAT</strong> -Eigenschaft enthalten ist. (Zu diesen Formaten gehören die Dateien für nicht Bilddateien, z. b. txt-, htm-und doc-Dateien.)</td>
</tr>
<tr class="even">
<td>Wiaitemtypedevice</td>
<td>Dieses Element stellt ein verbundenes Gerät dar.</td>
</tr>
<tr class="odd">
<td>Wiaitemtypegetrennte</td>
<td>Dieses Element stellt ein nicht verbundenes Gerät dar.</td>
</tr>
<tr class="even">
<td>Wiaitemtypefile</td>
<td>Das Element unterstützt Dateiübertragungen.</td>
</tr>
<tr class="odd">
<td>Wiaitemtypefolder</td>
<td>Das Element ist ein Ordner.</td>
</tr>
<tr class="even">
<td>Wiaitemtypefree</td>
<td>Das Element ist nicht initialisiert oder wurde gelöscht.</td>
</tr>
<tr class="odd">
<td>Wiaitemtypegenerated</td>
<td>Dieses Element wurde von einer Anwendung oder vom Treiber generiert.</td>
</tr>
<tr class="even">
<td>Wiaitemtypehasattachments *</td>
<td>Dieses Element unterstützt Anlagen und enthält zurzeit Anlagen.</td>
</tr>
<tr class="odd">
<td>Wiaitemtypehpanorama *</td>
<td>Dieses Element stellt ein horizontales Panoramabild dar. Dieses Flag ist nur für Elemente gültig, für die das <strong>wiaitemtypefolder</strong> -Flag ebenfalls festgelegt ist.</td>
</tr>
<tr class="even">
<td>Wiaitemtypeimage</td>
<td>Das Element ist eine Bilddatei. Dieses Flag ist nur für Elemente gültig, für die das <strong>wiaitemtypefile</strong> -Flag ebenfalls festgelegt ist.</td>
</tr>
<tr class="odd">
<td>Wiaitemtypeprogrammiabledatasource<strong>V</strong></td>
<td>Das Element ist eine programmierbare Datenquelle und folgt einem Satz vordefinierter Konfigurations Regeln, die auf <strong>WIA_IPA_ITEM_CATEGORY</strong>basieren.</td>
</tr>
<tr class="even">
<td>Wiaitemtyperoot<strong>V</strong></td>
<td>Dieses Element ist das Stamm Element, das allen Funktions Elementen übergeordnet ist, die das Gerät unterstützt.</td>
</tr>
<tr class="odd">
<td>Wiaitemtypestorage</td>
<td>Dieses Flag gibt zusätzlichen Speicher für Ordner Elemente an. WIA-Treiber geben ihre Elemente in Form von Bildern und Ordnern an. Es sind keine WIA-Eigenschaften vorhanden, die die Merkmale eines Speicher Elements beschreiben (z. b. den verbleibenden Speicherplatz, die Schreibgeschwindigkeit oder den Medientyp). Anbieterspezifische Eigenschaften, die diese Informationen verfügbar machen, können hinzugefügt werden. Diese Eigenschaften sind nur für Anwendungen oder Erweiterungen zugänglich, die geschrieben wurden, um Sie zu erkennen.</td>
</tr>
<tr class="even">
<td>Wiaitemtypetransfer</td>
<td>Dieses Element kann zum Übertragen von Daten verwendet werden.</td>
</tr>
<tr class="odd">
<td>Wiaitemtypetwaincapabilitypassthrough</td>
<td>Dieser Typ gibt an, dass das WIA-Gerät die TWAIN-Funktionsdaten von der TWAIN-Kompatibilitätsschicht empfangen kann. Wenn dieser Typ festgelegt ist, wird jede TWAIN-Funktion, die nicht von der TWAIN-Kompatibilitätsschicht verstanden wird, an den WIA-Treiber übermittelt. Dies gilt nur für das Stamm Element.</td>
</tr>
<tr class="even">
<td>Wiaitemtypevideo * *</td>
<td>Dieses Element unterstützt Streaming-Videos.</td>
</tr>
<tr class="odd">
<td>Wiaitemtypevpanorama *</td>
<td>Dieses Element stellt ein vertikales Panoramabild dar. Dieses Flag ist nur für Elemente gültig, für die das <strong>wiaitemtypefolder</strong> -Flag ebenfalls festgelegt ist.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Einige dieser Flags sind gemäß der Kategorie des Elements, wie in dieser Tabelle dargestellt, für WIA 2,0-Elemente erforderlich oder optional.</p>

<table>
<thead>
<tr class="header">
<th>Kategorie des Elements</th>
<th>Erforderlich</th>
<th>Optional</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_CATEGORY_ROOT</td>
<td>Wiaitemtyperoot wiaitemtypefolder</td>
<td>Wiaitemtypedevice wiaitemtypegetrennte</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FLATBED</td>
<td>Wiaitemtypeprogrammiabledatasource wiaitemtypetransfer wiaitemtypeimage wiaitemtypefile</td>
<td>Wiaitemtypefolder (wenn mehrere Scan Regions Elemente unterstützt werden, ist dieses Flag nur für das Stamm Element WIA_CATEGORY_FLATBED optional.)</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</td>
<td>Wiaitemtypeprogrammiabledatasource wiaitemtypetransfer wiaitemtypeimage wiaitemtypefile</td>
<td>Wiaitemtypefolder (wenn WIA_CATEGORY_FEEDER_FRONT und WIA_CATEGORY_FEEDER_BACK Elemente vorhanden sind, ist dieses Flag nur für das Stamm Element WIA_CATEGORY_FEEDER optional.)</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FILM (root)</td>
<td>Wiaitemtypeprogrammiabledatasource wiaitemtypetransfer wiaitemtypeimage wiaitemtypefile wiaitemtypefolder</td>
<td>Keine</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM (untergeordnete Elemente)</td>
<td>Wiaitemtypeprogrammiabledatasource wiaitemtypetransfer wiaitemtypeimage wiaitemtypefile</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FOLDER</td>
<td>Wiaitemtypestorage wiaitemtypefolder</td>
<td>Wiaitemtypedeleted</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FINISHED_FILE</td>
<td>Wiaitemtypefile wiaitemtypetransfer</td>
<td>Wiaitemtypeimage wiaitemtypeaudiowiaitemtypedeleted</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_NAME"></span><span id="wia_ipa_item_name"></span><dl> <dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>pictureitemname</dt> </dl></td>
<td style="text-align: left;"><p>Enthält den Elementnamen. Diese Eigenschaft wird von einer Anwendung gelesen, um zu bestimmen, welches Element zurzeit verwendet wird. Jedes Element hat einen eindeutigen Namen. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</p>
<p>Erforderlich für alle WIA 2,0-Elemente.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_SIZE"></span><span id="wia_ipa_item_size"></span><dl> <dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>pictureitemsize</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die aktuelle Größe (in Bytes) der Daten, die dem Element zugeordnet sind. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Enthält die Gesamtgröße der übertragenen Daten. Wenn dieser Wert 0 (null) ist, bedeutet dies, dass der Mini Treiber keine Informationen über die genaue Größe der Daten hat. (Dies ist häufig bei komprimierten Daten der gibt.) Eine Anwendung liest diesen Wert, um die Größe des Erwerbs zu ermitteln, bevor Sie stattfindet. Der WIA-Dienst liest diese Eigenschaft, um die Zuweisung von Speicher für Datenübertragungen zu unterstützen. Weitere Informationen finden Sie unter über <a href="https://msdn.microsoft.com/library/ms792198.aspx">tragen von Daten an eine WIA-Anwendung</a> , wenn die-Eigenschaft auf NULL festgelegt ist und TYMED für eine Dateiübertragung konfiguriert ist. der WIA-Dienst ordnet keinen Arbeitsspeicher für den WIA-Mini Treiber zu.</p>
<p>Erforderlich für alle für die Übertragung aktivierten WIA 2,0-Elemente.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_TIME"></span><span id="wia_ipa_item_time"></span><dl> <dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>pictureitemtime</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die Uhrzeit, zu der das Image ursprünglich aufgezeichnet wurde. Der Mini Treiber erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft sollte als Vektor von acht <strong>Wort</strong> Werten in Form einer SYSTEMTIME-Struktur (beschrieben in der Platform SDK-Dokumentation) gemeldet werden.</p>
<p>Optional für alle WIA 2,0-Elemente.</p>
<p>Typ: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong> Access: Lese-/Schreibzugriff oder schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>pictureitemitemsgespeicherter</dt> </dl></td>
<td style="text-align: left;"><p>Wird nur in Windows Vista und höher unterstützt.</p>
<p>Gibt an, wie viele Elemente im WIA_CATEGORY_FOLDER Element gespeichert werden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_MIN_BUFFER_SIZE"></span><span id="wia_ipa_min_buffer_size"></span><dl> <dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> von " <dt>pictureminbuffersize</dt> " </dl></td>
<td style="text-align: left;"><p>Gibt die minimale Puffergröße an, die für Datenübertragungen verwendet wird. Wenn die Datenübertragung über einen Rückrufmechanismus durchgeführt wird, kann der Eigenschafts Wert bis zu 64 KB betragen. Wenn die Übertragung jedoch in eine Datei erfolgt, ist der Eigenschafts Wert die Anzahl von Bytes, die zum Übertragen einer Datenseite gleichzeitig benötigt werden. Der Mini Treiber erstellt und verwaltet diese WIA-Eigenschaft.</p>
<p>Optional für alle für die Übertragung aktivierten WIA 2,0-Elemente.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_NUMBER_OF_LINES"></span><span id="wia_ipa_number_of_lines"></span><dl> <dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>picturenumberoflines</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die Anzahl der im Bild enthaltenen Zeilen (die vertikale Höhe des Bilds in Pixel). Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Optional für alle WIA 2,0-Elemente.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PIXELS_PER_LINE"></span><span id="wia_ipa_pixels_per_line"></span><dl> <dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>picturepixelsperline</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die Anzahl der Pixel in jeder Zeile des Bilds (die Breite des Bilds in Pixel). Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Optional für alle WIA 2,0-Elemente.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PLANAR"></span><span id="wia_ipa_planar"></span><dl> <dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>pictureplanar</dt> </dl></td>
<td style="text-align: left;"><p>Diese Eigenschaft wird in Windows Vista und höher nicht unterstützt.</p>
<p>Enthält Optionen für das Packen von Bild Daten. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung liest diese Eigenschaft, um die Bild Verpackungs Optionen zu bestimmen, oder legt die aktuellen Bild Verpackungs Optionen fest.</p>
<p>Typ: <strong>VT_I4</strong>; Zugriff: Lesen/Schreiben; Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>. Wenn das Gerät nur auf einen einzelnen Wert festgelegt werden kann, erstellen Sie einen WIA_PROP_LIST Typ, und platzieren Sie den gültigen Wert darin.</p>
<p>Die folgende Tabelle enthält die beiden Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PACKED_PIXEL</td>
<td>Bilddaten verfügen über ein gepacktes Pixel Format.</td>
</tr>
<tr class="even">
<td>WIA_PLANAR</td>
<td>Bilddaten liegen im planaren Format vor.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PREFERRED_FORMAT"></span><span id="wia_ipa_preferred_format"></span><dl> <dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>picturepreferredformat</dt> </dl></td>
<td style="text-align: left;"><p>Enthält das bevorzugte Format für Images, die dieser Mini Treiber überträgt. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Erforderlich für alle für die Übertragung aktivierten WIA 2,0-Elemente.</p>
<p>Typ: <strong>CLSID</strong>, Access: Read Only, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PROP_STREAM_COMPAT_ID"></span><span id="wia_ipa_prop_stream_compat_id"></span><dl> <dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>picturepropstreamcompatid</dt> </dl></td>
<td style="text-align: left;"><p>Gibt eine CLSID an, die einen Satz von Geräte Eigenschafts Werten darstellt. Wenn ein Gerätetreiber diese Funktion implementiert, verwenden Anwendungen diese Eigenschaft, um zu bestimmen, ob das Gerät eine Reihe von Werten unterstützt.</p>
<p>Typ: <strong>CLSID</strong>, Access: Read Only, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die 12 Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaImgFmt_BMP</td>
<td>MicrosoftWindows-Bitmap mit einer Header Datei</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EMF</td>
<td>Erweiterte Windows-Metadatendatei</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_EXIF</td>
<td>Austauschbares Datei Format</td>
</tr>
<tr class="even">
<td>WiaImgFmt_FLASHPIX</td>
<td>Format von Flash pix</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_GIF</td>
<td>GIF-Bildformat</td>
</tr>
<tr class="even">
<td>WiaImgFmt_ICO</td>
<td>Windows-Symbol Dateiformat</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JPEG</td>
<td>Komprimiertes JPEG-Format</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Eastman-Dateiformat von Kodak</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PNG</td>
<td>W3C-PNG-Format</td>
</tr>
<tr class="even">
<td>WiaImgFmt_MEMORYBMP</td>
<td>Windows-Bitmap ohne Header Datei</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_TIFF</td>
<td>Tag Image File Format</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>Windows-Metadatendatei</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_RAW_BITS_PER_CHANNEL"></span><span id="wia_ipa_raw_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>picturerawbitsperchannel</dt> </dl></td>
<td style="text-align: left;"><p>Wird nur in Windows Vista und höher unterstützt.</p>
<p>Enthält die Anzahl der Bits in jedem Kanal. Diese Eigenschaft sollte als Vektor von so vielen Byte Werten als Channels gemeldet werden, wobei das erste Byte der Anzahl von Bits im ersten Kanal entspricht, dem zweiten Byte der Anzahl von Bits im zweiten Kanal usw. Es müssen beliebig viele Einträge vorhanden sein, da Kanäle gemäß WIA_IPA_CHANNELS_PER_PIXEL vorhanden sind. Der Treiber legt diese Eigenschaft fest, wenn die Anwendung zu WiaImgFmt_RAW wechselt. Bei den bekannten Untertypen sind in der Tabelle unter WIA_IPA_RAW_SUBTYPE beliebig viele Einträge aufgeführt.</p>
<p>Typ: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_REGION_TYPE"></span><span id="wia_ipa_region_type"></span><dl> <dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>pictureregiontype</dt> </dl></td>
<td style="text-align: left;"><p>Diese Eigenschaft ist für die zukünftige Verwendung reserviert und wird zu diesem Zeitpunkt nicht implementiert.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_SUPPRESS_PROPERTY_PAGE"></span><span id="wia_ipa_suppress_property_page"></span><dl> <dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>picturesuppresspropertypage</dt> </dl></td>
<td style="text-align: left;"><p>Gibt an, ob die allgemeinen Eigenschaften Seiten für Elemente auf dem Gerät unterdrückt werden sollen.</p>
<p>Diese Eigenschaft ist unter Windows XP und höher verfügbar.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind. Das Sternchen * gibt an, dass die Konstante mit Windows Vista und höher nicht gültig ist. (Er ist nur über die <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>iwiaitem</strong></a> -Schnittstelle verfügbar.)</p>

<table>
<thead>
<tr class="header">
<th>Konstante</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PROPPAGE_CAMERA_ITEM_GENERAL *</td>
<td>Unterdrücken Sie die Eigenschaften Seite für allgemeine Elemente für eine Kamera.</td>
</tr>
<tr class="even">
<td>WIA_PROPPAGE_SCANNER_ITEM_GENERAL</td>
<td>Unterdrücken Sie die Eigenschaften Seite für allgemeine Elemente für einen Scanner.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_TYMED"></span><span id="wia_ipa_tymed"></span><dl> <dt><strong>WIA_IPA_TYMED</strong></dt> <dt>picturetymed</dt> </dl></td>
<td style="text-align: left;"><p>Diese Eigenschaft enthält die Übertragungsmethoden Einstellung. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung liest diese Eigenschaft, um die Methode der Minidriver-Methode für die Datenübertragung zu bestimmen.</p>
<p>Erforderlich für alle für die Übertragung aktivierten WIA 2,0-Elemente.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind. Das Sternchen * gibt Konstanten an, die mit Windows Vista und höher nicht gültig sind. (Sie sind nur über die <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>iwiaitem</strong></a> -Schnittstelle verfügbar.)</p>

<table>
<thead>
<tr class="header">
<th>Transfertyp</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TYMED_CALLBACK *</td>
<td>Übertragen Sie ein Bild in Bänder in den Arbeitsspeicher.</td>
</tr>
<tr class="even">
<td>TYMED_MULTIPAGE_CALLBACK *</td>
<td>Übertragen Sie mehrere Abbilder in Bänder in den Arbeitsspeicher.</td>
</tr>
<tr class="odd">
<td>TYMED_FILE</td>
<td>Übertragen eines Bilds in eine Datei.</td>
</tr>
<tr class="even">
<td>TYMED_MULTIPAGE_FILE</td>
<td>Übertragen eines Bilds in eine Datei.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>pictureitemuploaditemsize</dt> </dl></td>
<td style="text-align: left;"><p>Wird nur in Windows Vista und höher unterstützt.</p>
<p>Gibt die Anzahl der Bytes an, die für ein Element hochgeladen werden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




