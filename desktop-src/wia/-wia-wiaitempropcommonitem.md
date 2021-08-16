---
description: Die folgenden Geräteeigenschaftskonstanten müssen von allen Schnittstellen IWiaItem, IWiaItem2 und IWiaDrvItem-Schnittstelle unterstützt werden, sofern in ihren Beschreibungen nichts anderes angegeben ist.
ms.assetid: ef48313e-4df4-4ccd-a085-f714100885a7
title: Allgemeine WIA-Elementeigenschaftskonstanten (Wiadef.h)
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
ms.openlocfilehash: 6cf9c102e5ba9732369604bea21876af66ca525b596736521e92e59e52ddf9e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207527"
---
# <a name="common-wia-item-property-constants"></a>Allgemeine WIA-Elementeigenschaftskonstanten

Die folgenden Geräteeigenschaftskonstanten müssen von allen [**Schnittstellen IWiaItem,**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) [**IWiaItem2**](-wia-iwiaitem2.md) und [IWiaDrvItem-Schnittstelle](https://msdn.microsoft.com/library/ms793976.aspx) unterstützt werden, sofern in ihren Beschreibungen nichts anderes angegeben ist.

Das Präfix "WIA \_ \_ IPA" gibt eine Elementeigenschaft für alle Geräte an und ist die in C/C++ verwendete Namenskonvention. Zu Skriptzwecken verwenden diese Konstanten das Präfix "Picture" und sind Teil des [wiaItemPropertyId-Enumerationstyps.](-wia-wiaitempropertyid.md) Der entsprechende Membername aus dieser Skriptenumeration wird in Klammern neben dem C/C++-Konstantennamen in der folgenden Liste angezeigt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante/Wert</th>
<th style="text-align: left;">Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ACCESS_RIGHTS"></span><span id="wia_ipa_access_rights"></span><dl> <dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </dl></td>
<td style="text-align: left;">Dieses Flag steuert den Zugriff auf das Element und ob das Element gelöscht wird.<br/> Erforderlich für alle WIA 2.0-Elemente.<br/> Typ: <strong>VT_I4</strong>; Lesen/Schreiben oder Schreibzugriff, abhängig von der Fähigkeit des Elements, seine Zugriffsrechte zu ändern; Gültige Werte: WIA_PROP_FLAG<br/> Die folgende Tabelle enthält die fünf Flags, die mit dieser Eigenschaft gültig sind.<br/> 
<table>
<thead>
<tr class="header">
<th>Zugriffsrecht</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_ITEM_READ</td>
<td>Das Element hat schreibgeschützten Zugriff.</td>
</tr>
<tr class="even">
<td>WIA_ITEM_WRITE</td>
<td>Das Element verfügt nur über Schreibzugriff.</td>
</tr>
<tr class="odd">
<td>WIA_ITEM_CAN_BE_DELETED</td>
<td>Das Element verfügt nur über Löschzugriff.</td>
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
<td style="text-align: left;"><span id="WIA_IPA_APP_COLOR_MAPPING"></span><span id="wia_ipa_app_color_mapping"></span><dl> <dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </dl></td>
<td style="text-align: left;"><p>Diese Eigenschaft ist für die zukünftige Verwendung durch reserviert und wird derzeit nicht implementiert.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BITS_PER_CHANNEL"></span><span id="wia_ipa_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die Anzahl der Bits pro Kanal für das Bild. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Erforderlich für alle WIA 2.0-Erfassungs- oder gespeicherten Imageelemente.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_BUFFER_SIZE"></span><span id="wia_ipa_buffer_size"></span><dl> <dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die Größe des Puffers in Bytes, der während einer Datenübertragung verwendet wird. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung kann diese Eigenschaft lesen, um die vom Treiber angegebene Puffergröße für Datenübertragungen zu bestimmen. Der WIA-Dienst liest diese Eigenschaft auch, um arbeitsspeicher für den Minitreiber während der Datenübertragung zuzuweisen.</p>
<p>Optional für alle übertragungsfähigen WIA 2.0-Elemente.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<div class="alert">
<blockquote>
[!Note]<br />
Die <strong>WIA_IPA_BUFFER_SIZE</strong> -Eigenschaft enthält die Minimale Datenmenge, die eine Anwendung jederzeit anfordern kann. Je größer der Puffer, desto größer sind die Anforderungen an das Gerät. Dadurch kann das Gerät langsam und nicht reagieren, die Gesamtleistung des Systems beeinträchtigen und übermäßige Ressourcen verbrauchen. Zu kleine Puffergrößen können die Leistung der Datenübertragung verlangsamen, da viele kleinere Anforderungen erforderlich sind. Wählen Sie eine angemessene Puffergröße aus, indem Sie die typische Größe einer Datenanforderung an Ihr Gerät berücksichtigen und die Anzahl der Anforderungen mit der Größe dieser Anforderungen abgleichen.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BYTES_PER_LINE"></span><span id="wia_ipa_bytes_per_line"></span><dl> <dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die Anzahl der Bytes in einer Scanzeile des Bilds. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Optional für alle WIA 2.0-Elemente.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_CHANNELS_PER_PIXEL"></span><span id="wia_ipa_channels_per_pixel"></span><dl> <dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die Anzahl der Kanäle pro Pixel für das Bild. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Erforderlich für alle WIA 2.0-Erfassungs- oder gespeicherten Imageelemente.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_COLOR_PROFILE"></span><span id="wia_ipa_color_profile"></span><dl> <dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </dl></td>
<td style="text-align: left;"><p>Diese Eigenschaft ist für die zukünftige Verwendung durch reserviert und wird derzeit nicht implementiert.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_COMPRESSION"></span><span id="wia_ipa_compression"></span><dl> <dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </dl></td>
<td style="text-align: left;"><p>Enthält den aktuellen verwendeten Komprimierungstyp. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung liest diese Eigenschaft, um den Bildkomprimierungstyp zu bestimmen, oder legt diese Eigenschaft fest, um die Komprimierungseinstellung zu konfigurieren.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind. Das <strong>Symbol V</strong> gibt an, dass die Konstante nur in Windows Vista und höher unterstützt wird. (Sie ist nur über die <a href="-wia-iwiaitem2.md"><strong>IWiaItem2-Schnittstelle</strong></a> verfügbar.)</p>

<table>
<thead>
<tr class="header">
<th>Komprimierungstyp</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_COMPRESSION_NONE</td>
<td>Keine Komprimierung. Weitere Informationen finden Sie unter <strong>Hinweis.</strong></td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_AUTO</td>
<td>Automatischer Komprimierungsmodus. Weitere Informationen finden Sie unter <strong>Hinweis.</strong></td>
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
<td>Gruppen-3-Komprimierung</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_G4</td>
<td>Gruppen-4-Komprimierung</td>
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
<p>Wenn diese Eigenschaft WIA_COMPRESSION_NONE ist und WIA_IPA_FORMAT entweder WiaImgFmt_PDFA oder WiaImgFmt_XPS ist; WIA_COMPRESSION_NONE bedeutet dann, dass der Komprimierungsmodus nicht definiert ist und der Scanner sich für einen Modus entscheiden muss.</p>
<p>WIA_COMPRESSION_AUTO ist ein neuer Eigenschaftswert, der für die WIA_IPA_COMPRESSION -Eigenschaft definiert ist. Dieser Wert ist für alle programmierbaren Imagedatenquellelemente gültig, einschließlich Flatbed und Feeder. Wenn dieser Wert vom WIA-Minitreiber unterstützt wird, kann der WIA-Anwendungsclient WIA_IPA_COMPRESSION festlegen, um die automatische Erkennung des Komprimierungsmodus auf dem Gerät zu aktivieren. WIA_COMPRESSION_AUTO können mit und arbeiten, ohne dass die vollständige automatische Farbe unterstützt oder aktiviert wird (WIA_DATA_AUTO und WIA_DEPTH_AUTO).</p>
<p>WIA_COMPRESSION_AUTO ist besonders nützlich bei Übertragungsdateiformaten, die mehrere Datentypen und Bittiefe unterstützen, z. B. WiaImgFmt_RAW. Weitere Informationen zu Übertragungsdateiformaten finden Sie unter WIA_IPA_FORMAT in dieser Tabelle.</p>
<p>Es ist für den WIA-Minitreiber nicht mehr erforderlich, WIA_COMPRESSION_AUTO zu WIA_COMPRESSION_AUTO. Wenn dies unterstützt wird, darf der WIA-Minitreiber ihn nie als Standardwert für WIA_IPA_COMPRESSION festlegen. nur die WIA-Anwendung kann diesen Wert festlegen.</p>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_DATATYPE"></span><span id="wia_ipa_datatype"></span><dl> <dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die aktuelle Datentypeinstellung für das Gerät. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung liest diese Eigenschaft, um den Datentyp des Bilds zu bestimmen. Eine Anwendung schreibt diese Eigenschaft, um den aktuellen Datentyp des Bilds festzulegen, das übertragen werden soll.</p>
<p>Diese Eigenschaft ist für alle WIA 2.0-Elemente erforderlich. Sie muss für alle WIA 2.0-Erwerb aktivierten Elemente Lese-/Schreibzugriff und für WIA 2.0-Speicherelemente schreibgeschützte Elemente sein.</p>
<p>Typ: <strong>VT_I4</strong>; Zugriff für Betriebssysteme vor Windows Vista: Diese Eigenschaft ist schreibgeschützt für Kameras und Lese-/Schreibzugriff für Scanner. Zugriff für Windows Vista und höher: Diese Eigenschaft ist schreibgeschützte Eigenschaft für WIA_CATEGORY_FOLDER und WIA_CATEGORY_FINISHED_FILE Elemente und Lese-/Schreibzugriff für alle anderen WIA 2.0-Elementkategorien. Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die sechs Konstanten, die mit gültig sind, wenn <strong>WIA_IPA_FORMAT</strong> nicht auf WiaImgFmt_RAW festgelegt ist.</p>

<table>
<thead>
<tr class="header">
<th>Datentyp</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DATA_AUTO</td>
<td>Gültig für alle programmierbaren Bilddatenquellelemente, einschließlich Flatbed und Feeder. Wenn dieser Wert vom WIA-Minitreiber unterstützt wird, kann der WIA-Anwendungsclient WIA_IPA_DATATYPE festlegen, um die automatische Farberkennung auf dem Gerät zu aktivieren. Wenn WIA_DATA_AUTO festgelegt ist, muss der WIA-Minitreiber WIA_IPA_DEPTH für dasselbe Element auf WIA_DEPTH_AUTO aktualisieren (der ein unterstützter Wert sein muss, wenn das Gerät automatische Farben unterstützt).<br/> Dies ist ein optionaler Wert, aber er ist erforderlich, wenn WIA_DEPTH_AUTO für WIA_IPA_DEPTH unterstützt wird.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR</td>
<td>Scandaten sind rot, grün, blau (RGB). Das Vollfarbformat wird mit den folgenden WIA-Eigenschaften beschrieben: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong><br/> <strong>WIA_IPA_BITS_PER_CHANNEL</strong><br/> <strong>WIA_IPA_PLANAR</strong><br/> <strong>WIA_IPA_PIXELS_PER_LINE</strong><br/> <strong>WIA_IPA_BYTES_PER_LINE</strong><br/> <strong>WIA_IPA_NUMBER_OF_LINES</strong><br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_COLOR_DITHER</td>
<td>Identisch mit WIA_DATA_COLOR, außer dass die Daten mithilfe des aktuell ausgewählten Dithermusters geblendet werden.</td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR_THRESHOLD</td>
<td>Identisch mit WIA_DATA_COLOR, außer dass der Schwellenwert beim Scannen der Daten verwendet wird. Farbwerte über dem <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> Wert werden in vollständige Helligkeit konvertiert. Farben unter diesem Wert werden in Schwarz konvertiert.</td>
</tr>
<tr class="odd">
<td>WIA_DATA_DITHER</td>
<td>Scandaten werden mithilfe des aktuell ausgewählten Dithermusters dithered.</td>
</tr>
<tr class="even">
<td>WIA_DATA_GRAYSCALE</td>
<td>Scandaten stellen die Intensität dar. Die Palette ist eine feste graue Skala mit gleichem Abstand mit einer Tiefe, die durch <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> -Eigenschaft angegeben wird.</td>
</tr>
<tr class="odd">
<td>WIA_DATA_THRESHOLD</td>
<td>Der Schwellenwert beträgt ein Bit pro Pixel von Schwarz-Weiß-Daten. Daten über dem aktuellen Wert von <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> werden in Weiß konvertiert. Daten unter diesem Wert werden in Schwarz konvertiert.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Die <strong>WIA_IPA_DATATYPE</strong> -Eigenschaft wird auch verwendet, um den Typ der RAW-Datenübertragung zu beschreiben, die verwendet werden soll, wenn die Anwendung WiaImgFmt_RAW festlegt. Der Treiber sollte die <strong>eigenschaft WIA_IPA_DATATYPE</strong> auf eine Liste zulässiger Werte festlegen, aus der die Anwendung einen auswählen kann.</p>
<p>Wenn das Gerät nur auf einen einzelnen Wert festgelegt werden kann, erstellen Sie einen <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> Typ, und platzieren Sie den gültigen Wert darin.</p>
<p>Überprüfen Sie die <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> Eigenschaft, um die Bittiefe zu bestimmen. Diese Eigenschaft enthält in der Regel einen einzelnen Wert für Kameras.</p>
<p>In der folgenden Tabelle sind die Konstanten aufgeführt, die mit <strong>WIA_IPA_DATATYPE</strong> gültig sind, wenn <strong>WIA_IPA_FORMAT</strong> auf WiaImgFmt_RAW festgelegt ist.</p>

<table>
<thead>
<tr class="header">
<th>Datentyp</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DATA_GRAYSCALE</td>
<td>Scandaten stellen die Intensität dar. Die Palette ist eine feste Graustufenebene mit gleichem Abstand mit einer tiefe, die von der <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> -Eigenschaft angegeben wird. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 1 festgelegt werden.</td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_BGR</td>
<td>Scandaten sind im BGR-Farbraum (blau-grün-rot) enthalten. Das Vollfarbformat wird mithilfe der folgendenWIA-Eigenschaften beschrieben: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a><br/> <a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a><br/> <a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a><br/> <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 3 festgelegt werden.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_CMY</td>
<td>Scandaten sind im Farbraum cyan-magenta-yellow (CMY) enthalten. Das Vollfarbformat wird mit den gleichen WIA-Eigenschaften wie in WIA_DATA_RAW_BGR beschrieben. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 3 festgelegt werden.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_CMYK</td>
<td>Scandaten sind im Farbraum cyan-magenta-yellow-black (CMYK) enthalten. Das Vollfarbformat wird mit den gleichen WIA-Eigenschaften wie in WIA_DATA_RAW_BGR beschrieben. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 4 festgelegt werden.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_RGB</td>
<td>Scandaten sind im RGB-Farbraum (Rot-Grün-Blau) enthalten. Das Vollfarbformat wird mit den gleichen WIA-Eigenschaften wie in WIA_DATA_RAW_BGR beschrieben. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 3 festgelegt werden.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_YUV</td>
<td>Scandaten sind im Farbraum luminance-blue difference-red difference (YUV) enthalten. Das Vollfarbformat wird mit den gleichen WIA-Eigenschaften wie in WIA_DATA_RAW_BGR beschrieben. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 3 festgelegt werden.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_YUVK</td>
<td>Scandaten sind im Farbraum luminance-blue difference-red difference-black (YUVK) enthalten. Das Vollfarbformat wird mit den gleichen WIA-Eigenschaften wie in WIA_DATA_RAW_BGR beschrieben. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> muss auf 4 festgelegt werden.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_DEPTH"></span><span id="wia_ipa_depth"></span><dl> <dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </dl></td>
<td style="text-align: left;"><p>WIA_IPA_DEPTH Enthält die Bittiefeeinstellung eines Bilds. Der Minitreiber erstellt und verwaltet diese Eigenschaft. Eine Anwendung liest diese Eigenschaft, um die Bittiefeeinstellung des Bilds zu bestimmen. Die Anwendung kann diesen Wert möglicherweise auch auf die gewünschte Bittiefe festlegen.</p>
<p>Wenn das Gerät nur auf einen einzelnen Wert festgelegt werden kann, erstellen Sie einen <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> Typ, und platzieren Sie den gültigen Wert darin.</p>
<p>Diese Eigenschaft ist für alle WIA 2.0-Elemente erforderlich. Sie muss für alle WIA 2.0-Erwerb aktivierten Elemente Lese-/Schreibzugriff und für WIA 2.0-Speicherelemente schreibgeschützte Elemente sein.</p>
<p>Typ: <strong>VT_I4</strong>; Zugriff für Betriebssysteme vor Windows Vista: Lesen/Schreiben; Zugriff für Windows Vista und höher: Diese Eigenschaft ist schreibgeschützte Eigenschaft für WIA_CATEGORY_FOLDER und WIA_CATEGORY_FINISHED_FILE Elemente und Lese-/Schreibzugriff für alle anderen WIA 2.0-Elementkategorien. Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>WIA_DEPTH_AUTO ist als 0 Bits pro Pixel definiert, und es handelt sich um einen neuen Eigenschaftswert, der für die WIA_IPA_DEPTH definiert ist. Dieser Wert ist für alle programmierbaren Imagedatenquellelemente gültig, einschließlich Flatbed und Feeder. Wenn WIA_DEPTH_AUTO vom WIA-Minitreiber unterstützt wird, kann der WIA-Anwendungsclient WIA_IPA_DEPTH auf diesen Wert festlegen, um die automatische Farberkennung auf dem Gerät zu aktivieren. Wenn WIA_DEPTH_AUTO festgelegt ist, muss der WIA-Minitreiber WIA_IPA_DATATYPE für dasselbe Element auf WIA_DATA_AUTO aktualisieren (dies muss ein unterstützter Wert sein, wenn das Gerät automatische Farben unterstützt).</p>
<p>WIA_DEPTH_AUTO ist ein optionaler Wert, wird jedoch erforderlich, wenn WIA_DATA_AUTO für WIA_IPA_DATATYPE unterstützt wird.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FILENAME_EXTENSION"></span><span id="wia_ipa_filename_extension"></span><dl> <dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die Dateinamenerweiterung für ein bestimmtes Dateiformat. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Optional für alle übertragungsfähigen WIA 2.0-Elemente.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützte, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Der Treiber aktualisiert diese Eigenschaft, um den aktuellen Wert der <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> -Eigenschaft widerzuspiegeln.</p>
<p>Wenn beispielsweise <strong>WIA_IPA_FORMAT</strong> WiaImgFmt_JPEG ist, sollte <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> <strong>jpg</strong>sein. Wenn <strong>WIA_IPA_FORMAT</strong> WiaImgFmt_BMP ist, sollte WIA_IPA_FILENAME_EXTENSION BMP sein.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Die Dateinamenerweiterung enthält den Punkt nicht.
</blockquote>
</div>
<div>
 
</div>
<p>Diese Eigenschaft wird für Treiber empfohlen, die Standardformate unterstützen, und ist für Treiber erforderlich, die benutzerdefinierte Formate implementieren. Er informiert die Anwendung über die richtige Dateinamenerweiterung, die während der Übertragung von privat formatierten Dateien verwendet werden soll. Wenn die A. Datum Corporation beispielsweise einen WIA-Treiber erstellt hat, der eine Datei in einem neuen Format übertrug, könnte das Unternehmen die Erweiterung &quot; adc &quot; angeben. Dadurch können Anwendungen Daten in diesem Format in eine Datei übertragen und einen Dateinamen wie <em>myfile.adc</em>erstellen. Dies ist nützlich für andere Benutzer, die die neue Erweiterung verstehen.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_FORMAT"></span><span id="wia_ipa_format"></span><dl> <dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </dl></td>
<td style="text-align: left;"><p>Enthält das aktuelle Format des Images, das übertragen werden soll.</p>
<p>Eine Anwendung liest diese Eigenschaft, um das Format des Images zu bestimmen, das sie empfangen wird. Eine Anwendung schreibt diese Eigenschaft, um das Format zu festlegen. Diese Eigenschaft hängt von <a href="https://msdn.microsoft.com/library/ms795488.aspx">der</a> WIA_IPA_TYMED ab. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Wenn das Gerät nur auf einen einzelnen <a href="-wia-property-attributes.md"></a> Wert festgelegt werden kann, erstellen Sie einen WIA_PROP_LIST, und platzieren Sie den gültigen Wert.</p>
<p>Typ: <strong>CLSID</strong>, Zugriff: Lesen/Schreiben, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>In der folgenden Tabelle sind die Konstanten aufgeführt, die mit dieser Eigenschaft gültig sind. Das Sternchen * gibt an, dass die Konstante in vista nicht Windows wird. (Sie ist nur über die <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem-Schnittstelle</strong></a> verfügbar.) Das doppelte Sternchen ** gibt an, dass die Konstante weder in Windows Server 2003 noch in Windows Vista unterstützt wird. Das <strong>V-Symbol</strong> gibt an, dass die Konstante nur in Windows Vista und höher unterstützt wird. (Sie ist nur über die <a href="-wia-iwiaitem2.md"><strong>IWiaItem2-Schnittstelle</strong></a> verfügbar.)</p>

<table>
<thead>
<tr class="header">
<th>Format</th>
<th>Beschreibung</th>
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
<td>WiaImgFmt_ASF**</td>
<td>ASF-Videoformat</td>
</tr>
<tr class="even">
<td>WiaImgFmt_AVI**</td>
<td>AVI-Videoformat</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_BMP</td>
<td>Windows Bitmap mit einer Headerdatei</td>
</tr>
<tr class="even">
<td>WiaImgFmt_CIFF*</td>
<td>Dateiformat der Kamerabilddatei</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_DPOF</td>
<td>DPOF-Druckformat</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EMF</td>
<td>Erweiterte Windows Metadatei</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_EXEC</td>
<td>Ausführbare Datei</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EXIF</td>
<td>Austauschbares Dateiformat</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_FLASHPIX</td>
<td>FlashPix-Format</td>
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
<td>Windows-Symboldateiformat</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JBIG<strong>V</strong></td>
<td>Das JBIG-Format (Joint Bi-Level Image Experts Group).</td>
</tr>
<tr class="even">
<td>WiaImgFmt_JPEG</td>
<td>Komprimiertes JPEG-Format</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JPEG2K</td>
<td>Komprimiertes JPEG 2000-Format</td>
</tr>
<tr class="even">
<td>WiaImgFmt_JPEG2KX</td>
<td>Komprimiertes JPEG 2000-Format</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_MEMORYBMP</td>
<td>Windows Bitmap ohne Headerdatei</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PDFA<strong>V</strong></td>
<td>Das PDF/A-Format (ISO/CD 19005-1).</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_MPG**</td>
<td>MPEG-Videoformat</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Eastman-Format (Eastman- Und-Eastman-Format)</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PICT</td>
<td>Apple-Dateiformat</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PNG</td>
<td>W3C PNG-Format</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_RAW</td>
<td>Rohformat nur für Datenübertragungen</td>
</tr>
<tr class="even">
<td>WiaImgFmt_RAWRGB</td>
<td>Rgb-Rohformat</td>
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
<td>UNICODE-16-Bit-Codierung</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>Windows Metadatei</td>
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
Wenn diese Eigenschaft entweder WiaImgFmt_PDFA oder WiaImgFmt_XPS ist und WIA_IPA_COMPRESSION nicht WIA_COMPRESSION_NONE; Der zweite Wert bedeutet dann, dass der Komprimierungsmodus nicht definiert ist und der Scanner sich für einen Modus entscheiden muss.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FULL_ITEM_NAME"></span><span id="wia_ipa_full_item_name"></span><dl> <dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </dl></td>
<td style="text-align: left;"><p>Enthält den vollständigen Elementnamen (den Elementnamen zusammen mit Pfadinformationen). Der vollständige Elementname ist identisch mit dem <em>Parameter bstrFullItemName</em> der <a href="https://msdn.microsoft.com/library/ms794649.aspx">Hilfsprogrammfunktion wiasCreateDrvItem.</a> Eine Anwendung liest diese Eigenschaft, um zu bestimmen, welches Element derzeit verwendet wird und wo sich das Element in der Elementstruktur befindet. Jedes Element sollte einen eindeutigen Namen haben. Anwendungen verwenden häufig den vollständigen Elementnamen, um nach Elementen in der Elementstruktur zu suchen. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</p>
<p>Erforderlich für alle WIA 2.0-Elemente.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_GAMMA_CURVES"></span><span id="wia_ipa_gamma_curves"></span><dl> <dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </dl></td>
<td style="text-align: left;"><p>Diese Eigenschaft ist für die zukünftige Verwendung reserviert und derzeit nicht implementiert.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ICM_PROFILE_NAME"></span><span id="wia_ipa_icm_profile_name"></span><dl> <dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </dl></td>
<td style="text-align: left;"><p>Enthält den ICM Profilnamen, der zum ordnungsgemäßen Decodieren des Bilds erforderlich ist. Eine Anwendung liest diese Eigenschaft, um das ICM Profil zu bestimmen, das bei der Verarbeitung des Bilds verwendet werden soll. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft basierend auf dem ICMProfiles-Eintrag in der Treiberinstallationsdatei.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützte, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_CATEGORY"></span><span id="wia_ipa_item_category"></span><dl> <dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </dl></td>
<td style="text-align: left;"><p>Wird nur in Windows Vista und höher unterstützt.</p>
<p>WIA 2.0-Elemente werden in Kategorien gruppiert, die definieren, wie ein <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> behandelt oder verwendet werden soll. Wenn das Element beispielsweise einen Feeder darstellt, sollte die Anwendung davon ausgehen, dass es die erforderlichen Eigenschaften des Dokumentfeeders enthält und wie ein Dokumentfeeder funktioniert. Wenn das Element eine fertige Datei darstellt, sollte es von einer WIA 2.0-Anwendung auf diese Weise behandelt werden, vorausgesetzt, die Daten sind statisch und befinden sich auf dem Gerät. (Die Regeln für jedes Element werden in den einzelnen Spezifikationsdokumenten definiert.)</p>
<p>Erforderlich für alle WIA 2.0-Elemente.</p>
<p>Typ: <strong>VT_CLSID</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-wia2-itemcategoryguids.md"><strong>Elementkategorie-GUIDs</strong></a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_FLAGS"></span><span id="wia_ipa_item_flags"></span><dl> <dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die beschreibenden Flags für ein WIA-Element. Die Elementflags sind identisch mit denen im <em>lObjectFlags-Parameter</em> der <a href="https://msdn.microsoft.com/library/ms794649.aspx">WiasCreateDrvItem-Diensthilfsprogrammfunktion.</a> Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung liest diese Eigenschaft, um die beschreibenden Flagwerte des Elements zu bestimmen.</p>
<p>Typ: <strong>VT_I4</strong> Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die folgende Tabelle enthält die Flags, die mit dieser Eigenschaft gültig sind. Ein Sternchen * gibt an, dass das Flag in Windows Vista oder höher nicht unterstützt wird. (Sie ist nur über die <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem-Schnittstelle</strong></a> verfügbar.) Ein doppeltes Sternchen ** gibt an, dass das Flag in Windows Server 2003 oder Windows Vista oder höher nicht unterstützt wird. Das <strong>V-Symbol</strong> gibt an, dass das Flag nur in Windows Vista und höher unterstützt wird. (Sie ist nur über die <a href="-wia-iwiaitem2.md"><strong>IWiaItem2-Schnittstelle</strong></a> verfügbar.)</p>

<table>
<thead>
<tr class="header">
<th>Flag</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaItemTypeAnalyze*</td>
<td>Dieses Element unterstützt die <strong>IWiaItem::AnalyzeItem-Methode</strong> (in der Dokumentation zum Plattform-SDK beschrieben). Dieses Element unterstützt auch die automatische Generierung untergeordneter Elemente. Diese Funktion ist nützlich für die Regionserkennung oder Seitenzerlegung.</td>
</tr>
<tr class="even">
<td>WiaItemTypeAudio</td>
<td>Dieses Element unterstützt Audio. Dieses Flag ist nur für Elemente gültig, für die auch das <strong>WiaItemTypeFile-Flag</strong> festgelegt ist.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeBurst*</td>
<td>Nur für Ordner. Dieses Flag gibt an, dass die Bilder in diesem Ordner in einer kontinuierlichen Zeitsequenz erstellt wurden.</td>
</tr>
<tr class="even">
<td>WiaItemTypeDeleted</td>
<td>Dieses Element ist zum Löschen markiert, dieses Element wurde gelöscht, dieses Element ist nicht vorhanden, oder der Inhalt dieses Elements ist ungültig.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeDocument<strong>V</strong></td>
<td>Dieses Element ist eine Dokumentdatei in einem der Dokumentformate, die die <strong>WIA_IPA_FORMAT</strong> -Eigenschaft enthält. (Diese Formate umfassen die Formate für Nichtimagedateien, z. B. .txt, .htm und .doc Dateien.)</td>
</tr>
<tr class="even">
<td>WiaItemTypeDevice</td>
<td>Dieses Element stellt ein verbundenes Gerät dar.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeDisconnected</td>
<td>Dieses Element stellt ein nicht verbundenes Gerät dar.</td>
</tr>
<tr class="even">
<td>WiaItemTypeFile</td>
<td>Das Element unterstützt Dateiübertragungen.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeFolder</td>
<td>Das Element ist ein Ordner.</td>
</tr>
<tr class="even">
<td>WiaItemTypeFree</td>
<td>Das Element ist nicht initialisiert oder wurde gelöscht.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeGenerated</td>
<td>Dieses Element wurde von einer Anwendung oder vom Treiber generiert.</td>
</tr>
<tr class="even">
<td>WiaItemTypeHasAttachments*</td>
<td>Dieses Element unterstützt Anlagen und enthält derzeit Anlagen.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeHPanoanne*</td>
<td>Dieses Element stellt ein horizontales Bild dar. Dieses Flag ist nur für Elemente gültig, für die auch das <strong>WiaItemTypeFolder-Flag</strong> festgelegt ist.</td>
</tr>
<tr class="even">
<td>WiaItemTypeImage</td>
<td>Das Element ist eine Bilddatei. Dieses Flag ist nur für Elemente gültig, für die auch das <strong>WiaItemTypeFile-Flag</strong> festgelegt ist.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeProgrammableDataSource<strong>V</strong></td>
<td>Das Element ist eine programmierbare Datenquelle und folgt einer Reihe vordefinierter Konfigurationsregeln, die auf <strong>WIA_IPA_ITEM_CATEGORY</strong>basieren.</td>
</tr>
<tr class="even">
<td>WiaItemTypeRoot<strong>V</strong></td>
<td>Dieses Element ist das Stammelement, das allen Featureelementen übergeordnet ist, die das Gerät unterstützt.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeStorage</td>
<td>Dieses Flag gibt zusätzlichen Speicher für Ordnerelemente an. WIA-Treiber geben ihre Elemente in Bezug auf Bilder und Ordner an. Es sind keine WIA-Eigenschaften vorhanden, die die Merkmale eines Speicherelements beschreiben (z. B. verbleibender Speicherplatz, Schreibgeschwindigkeit oder Medientyp). Anbieterspezifische Eigenschaften, die diese Informationen verfügbar machen, können hinzugefügt werden. Auf diese Eigenschaften kann nur für Anwendungen oder Erweiterungen zugegriffen werden, die geschrieben wurden, um sie zu erkennen.</td>
</tr>
<tr class="even">
<td>WiaItemTypeTransfer</td>
<td>Dieses Element kann zum Übertragen von Daten verwendet werden.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeTwainCapabilityPassThrough</td>
<td>Dieser Typ gibt an, dass das WIA-Gerät TWAIN-Funktionsdaten von der TWAIN-Kompatibilitätsebene empfangen kann. Wenn dieser Typ festgelegt ist, werden alle TWAIN-Funktionen, die von der TWAIN-Kompatibilitätsschicht nicht verstanden werden, an denWIA-Treiber übergeben. Dies ist nur für das Stammelement gültig.</td>
</tr>
<tr class="even">
<td>WiaItemTypeVideo**</td>
<td>Dieses Element unterstützt das Streamen von Videos.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeVPanoero*</td>
<td>Dieses Element stellt ein vertikales Bild dar. Dieses Flag ist nur für Elemente gültig, für die auch das <strong>WiaItemTypeFolder-Flag</strong> festgelegt ist.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Einige dieser Flags sind für WIA 2.0-Elemente gemäß der Kategorie des Elements erforderlich oder optional, wie in dieser Tabelle dargestellt.</p>

<table>
<thead>
<tr class="header">
<th>Elementkategorie</th>
<th>Erforderlich</th>
<th>Optional</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_CATEGORY_ROOT</td>
<td>WiaItemTypeRoot WiaItemTypeFolder</td>
<td>WiaItemTypeDevice WiaItemTypeDisconnected</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FLATBED</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>WiaItemTypeFolder (Wenn mehrere Scanbereiche unterstützt werden, ist dieses Flag nur für das WIA_CATEGORY_FLATBED Stammelement optional.)</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>WiaItemTypeFolder (Wenn WIA_CATEGORY_FEEDER_FRONT und WIA_CATEGORY_FEEDER_BACK Elemente vorhanden sind, ist dieses Flag nur für das WIA_CATEGORY_FEEDER Stammelement optional.)</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FILM (Root)</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</td>
<td>Keine</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM (children)</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FOLDER</td>
<td>WiaItemTypeStorage WiaItemTypeFolder</td>
<td>WiaItemTypeDeleted</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FINISHED_FILE</td>
<td>WiaItemTypeFile WiaItemTypeTransfer</td>
<td>WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_NAME"></span><span id="wia_ipa_item_name"></span><dl> <dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </dl></td>
<td style="text-align: left;"><p>Enthält den Elementnamen. Eine Anwendung liest diese Eigenschaft, um zu bestimmen, welches Element sie derzeit verwendet. Jedes Element hat einen eindeutigen Namen. Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</p>
<p>Erforderlich für alle WIA 2.0-Elemente.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_SIZE"></span><span id="wia_ipa_item_size"></span><dl> <dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die aktuelle Größe der Daten in Bytes, die dem Element zugeordnet sind. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Enthält die Gesamtgröße der übertragenen Daten. Wenn dieser Wert 0 (null) ist, bedeutet dies, dass der Minitreiber keine Informationen über die genaue Größe der Daten hat. (Dies ist bei komprimierten Daten üblich.) Eine Anwendung liest diesen Wert, um die Größe des Kaufs zu bestimmen, bevor er stattfindet. Der WIA-Dienst liest diese Eigenschaft, um die Zuweisung von Arbeitsspeicher für Datenübertragungen zu unterstützen. Weitere Informationen finden Sie unter Übertragen von Daten an eine <a href="https://msdn.microsoft.com/library/ms792198.aspx">WIA-Anwendung,</a> wenn die -Eigenschaft auf 0 festgelegt ist und TYMED für eine Dateiübertragung konfiguriert ist. Der WIA-Dienst weist dem WIA-Minitreiber keinen Arbeitsspeicher zu.</p>
<p>Erforderlich für alle übertragungsfähigen WIA 2.0-Elemente.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_TIME"></span><span id="wia_ipa_item_time"></span><dl> <dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die Zeit, zu der das Bild ursprünglich erfasst wurde. Der Minitreiber erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft sollte als Vektor von acht <strong>WORD-Werten</strong> in Form einer SYSTEMTIME-Struktur gemeldet werden (in der Dokumentation zum Plattform-SDK beschrieben).</p>
<p>Optional für alle WIA 2.0-Elemente.</p>
<p>Typ: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong> Access: Read/Write or Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </dl></td>
<td style="text-align: left;"><p>Wird nur in Windows Vista und höher unterstützt.</p>
<p>Gibt an, wie viele Elemente im -Element WIA_CATEGORY_FOLDER werden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_MIN_BUFFER_SIZE"></span><span id="wia_ipa_min_buffer_size"></span><dl> <dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </dl></td>
<td style="text-align: left;"><p>Gibt die minimale Puffergröße an, die bei Datenübertragungen verwendet wird. Wenn die Datenübertragung über einen Rückrufmechanismus durchgeführt wird, kann der Eigenschaftswert bis zu 64 KB beträgt. Wenn die Übertragung jedoch in eine Datei übertragen wird, entspricht der Eigenschaftswert der Anzahl von Bytes, die zum Übertragen einer Datenseite gleichzeitig erforderlich sind. Der Minitreiber erstellt und verwaltet diese WIA-Eigenschaft.</p>
<p>Optional für alle übertragungsfähigen WIA 2.0-Elemente.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_NUMBER_OF_LINES"></span><span id="wia_ipa_number_of_lines"></span><dl> <dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die Anzahl der im Bild enthaltenen Zeilen (die vertikale Höhe des Bilds in Pixel). Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Optional für alle WIA 2.0-Elemente.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PIXELS_PER_LINE"></span><span id="wia_ipa_pixels_per_line"></span><dl> <dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die Anzahl der Pixel in jeder Zeile des Bilds (die Breite des Bilds in Pixel). Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Optional für alle WIA 2.0-Elemente.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PLANAR"></span><span id="wia_ipa_planar"></span><dl> <dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </dl></td>
<td style="text-align: left;"><p>Diese Eigenschaft wird in Windows Vista und höher nicht unterstützt.</p>
<p>Enthält Bilddaten-Packoptionen. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung liest diese Eigenschaft, um die Bildpackoptionen zu bestimmen, oder legt die aktuellen Bildpackungsoptionen fest.</p>
<p>Typ: <strong>VT_I4</strong>; Zugriff: Lesen/Schreiben; Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>. Wenn das Gerät nur auf einen einzelnen Wert festgelegt werden kann, erstellen Sie einen WIA_PROP_LIST, und platzieren Sie den gültigen Wert.</p>
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
<td>Bilddaten haben ein gepacktes Pixelformat.</td>
</tr>
<tr class="even">
<td>WIA_PLANAR</td>
<td>Bilddaten haben das planare Format.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PREFERRED_FORMAT"></span><span id="wia_ipa_preferred_format"></span><dl> <dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </dl></td>
<td style="text-align: left;"><p>Enthält das bevorzugte Format für Bilder, die dieser Minitreiber überträgt. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Erforderlich für alle übertragungsfähigen WIA 2.0-Elemente.</p>
<p>Typ: <strong>CLSID</strong>, Access: Schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PROP_STREAM_COMPAT_ID"></span><span id="wia_ipa_prop_stream_compat_id"></span><dl> <dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </dl></td>
<td style="text-align: left;"><p>Gibt eine CLSID an, die einen Satz von Geräteeigenschaftswerten darstellt. Wenn ein Gerätetreiber dieses Feature implementiert, verwenden Anwendungen diese Eigenschaft, um zu bestimmen, ob das Gerät einen Satz von Werten unterstützt.</p>
<p>Typ: <strong>CLSID</strong>, Access: Schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die 12 Konstanten, die für diese Eigenschaft gültig sind.</p>

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
<td>MicrosoftWindows-Bitmap mit einer Headerdatei</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EMF</td>
<td>Erweiterte Windows Metadatei</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_EXIF</td>
<td>Austauschbares Dateiformat</td>
</tr>
<tr class="even">
<td>WiaImgFmt_FLASHPIX</td>
<td>FlashPix-Format</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_GIF</td>
<td>GIF-Bildformat</td>
</tr>
<tr class="even">
<td>WiaImgFmt_ICO</td>
<td>Windows-Symboldateiformat</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JPEG</td>
<td>Komprimiertes JPEG-Format</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Eastman-Format (Eastman- Und-Eastman-Format)</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PNG</td>
<td>W3C PNG-Format</td>
</tr>
<tr class="even">
<td>WiaImgFmt_MEMORYBMP</td>
<td>Windows Bitmap ohne Headerdatei</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_TIFF</td>
<td>Tag Image File Format</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>Windows Metadatei</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_RAW_BITS_PER_CHANNEL"></span><span id="wia_ipa_raw_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </dl></td>
<td style="text-align: left;"><p>Wird nur in Windows Vista und höher unterstützt.</p>
<p>Enthält die Anzahl der Bits in jedem Kanal. Diese Eigenschaft sollte als Vektor von so vielen BYTE-Werten wie Kanäle gemeldet werden, wobei das erste BYTE der Anzahl der Bits im ersten Kanal entspricht, das zweite Byte der Anzahl der Bits im zweiten Kanal und so weiter. Es müssen so viele Einträge wie Kanäle entsprechend der WIA_IPA_CHANNELS_PER_PIXEL. Der Treiber legt diese Eigenschaft fest, wenn die Anwendung zu WiaImgFmt_RAW. Für die bekannten Untertypen gibt es so viele Einträge wie in der Tabelle unter WIA_IPA_RAW_SUBTYPE.</p>
<p>Typ: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_REGION_TYPE"></span><span id="wia_ipa_region_type"></span><dl> <dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </dl></td>
<td style="text-align: left;"><p>Diese Eigenschaft wird von für die zukünftige Verwendung reserviert und derzeit nicht implementiert.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_SUPPRESS_PROPERTY_PAGE"></span><span id="wia_ipa_suppress_property_page"></span><dl> <dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </dl></td>
<td style="text-align: left;"><p>Gibt an, ob die allgemeinen Eigenschaftenseiten für Elemente auf dem Gerät unterdrückt werden.</p>
<p>Diese Eigenschaft ist für Windows XP und höher verfügbar.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind. Das Sternchen * gibt an, dass die Konstante mit Windows Vista und höher ungültig ist. (Sie ist nur über die <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem-Schnittstelle</strong></a> verfügbar.)</p>

<table>
<thead>
<tr class="header">
<th>Konstante</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PROPPAGE_CAMERA_ITEM_GENERAL*</td>
<td>Unterdrücken Sie die allgemeine Elementeigenschaftsseite für eine Kamera.</td>
</tr>
<tr class="even">
<td>WIA_PROPPAGE_SCANNER_ITEM_GENERAL</td>
<td>Unterdrücken Sie die Eigenschaftenseite für allgemeine Elemente für einen Scanner.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_TYMED"></span><span id="wia_ipa_tymed"></span><dl> <dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </dl></td>
<td style="text-align: left;"><p>Diese Eigenschaft enthält die Einstellung der Übertragungsmethode. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung liest diese Eigenschaft, um die Datenübertragungsmethode des Minitreibers zu bestimmen.</p>
<p>Erforderlich für alle übertragungsfähigen WIA 2.0-Elemente.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind. Das Sternchen * gibt Konstanten an, die für vista Windows und höher ungültig sind. (Sie sind nur über die <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem-Schnittstelle</strong></a> verfügbar.)</p>

<table>
<thead>
<tr class="header">
<th>Transfertyp</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TYMED_CALLBACK*</td>
<td>Übertragen sie ein Bild in Bänder in den Arbeitsspeicher.</td>
</tr>
<tr class="even">
<td>TYMED_MULTIPAGE_CALLBACK*</td>
<td>Übertragen Sie mehrere Bilder in Bänder in den Arbeitsspeicher.</td>
</tr>
<tr class="odd">
<td>TYMED_FILE</td>
<td>Übertragen sie ein Bild in eine Datei.</td>
</tr>
<tr class="even">
<td>TYMED_MULTIPAGE_FILE</td>
<td>Übertragen sie ein Bild in eine Datei.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </dl></td>
<td style="text-align: left;"><p>Wird nur in Windows Vista und höher unterstützt.</p>
<p>Gibt die Anzahl von Bytes an, die für ein Element hochgeladen werden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 




