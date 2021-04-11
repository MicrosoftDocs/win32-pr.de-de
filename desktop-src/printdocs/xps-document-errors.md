---
description: In der folgenden Tabelle werden alle HRESULT-Werte aufgelistet, die von den Methoden der XPS-Dokument-API zurückgegeben werden können.
ms.assetid: 9e6db1e3-7151-4538-8607-b7185ebc0110
title: XPS-Dokument Fehler (xpsobjectmodel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a221858e177172a0062185cbe1bcc127ccc728fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215405"
---
# <a name="xps-document-errors"></a>XPS-Dokument Fehler

In der folgenden Tabelle werden alle **HRESULT** -Werte aufgelistet, die von den Methoden der XPS-Dokument-API zurückgegeben werden können. Beachten Sie, dass nicht jede Methode jeden in dieser Tabelle aufgelisteten Rückgabewert zurückgibt.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rückgabecode/-wert</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="XPS_E_ALREADY_OWNED"></span><span id="xps_e_already_owned"></span><dl> <dt><strong>XPS_E_ALREADY_OWNED</strong></dt> <dt>0x80520503</dt> </dl></td>
<td>Die Schnittstelle verfügt bereits über einen Besitzer.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC"></span><span id="xps_e_bleed_box_page_dimensions_not_in_sync"></span><dl> <dt><strong>XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC</strong></dt> <dt>0x80520509</dt> </dl></td>
<td>Die ausgebfteten Feld Abmessungen sind nicht mit den Seiten Dimensionen kompatibel.<br/> Der Wert der gebfteten Feldbreite muss größer als oder gleich der Seitenbreite plus dem absoluten Wert der x-Koordinate des Ursprungs der gebfteten Box sein. Der Wert für die Höhe der ausgeblendenden Box muss größer als oder gleich der Seitenhöhe plus dem absoluten Wert der y-Koordinate für den ursprünglichen Feld Ursprung sein. <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT"></span><span id="xps_e_both_pathfigure_and_abbr_syntax_present"></span><dl> <dt><strong>XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT</strong></dt> <dt>0x80520507</dt> </dl></td>
<td>Ein <strong>PathGeometry</strong> -Element enthält einen Satz von Pfad Abbildungen, die entweder mit dem <strong>Figures</strong> -Attribut oder mit einem untergeordneten <strong>PathFigure</strong> -Element angegeben werden. Die Pfad Abbildungen einer Geometrie dürfen nicht sowohl das <strong>Figures</strong> -Attribut als auch ein untergeordnetes <strong>PathFigure</strong> -Element aufweisen. <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT"></span><span id="xps_e_both_resource_and_sourceattr_present"></span><dl> <dt><strong>XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT</strong></dt> <dt>0x80520508</dt> </dl></td>
<td>Ein <strong>ResourceDictionary</strong> -Element, das ein Remote Ressourcen Wörterbuch in seinem <strong>Quell</strong> Attribut angibt, darf keine untergeordneten Ressourcen Definitionen enthalten.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_CARET_OUT_OF_ORDER"></span><span id="xps_e_caret_out_of_order"></span><dl> <dt><strong>XPS_E_CARET_OUT_OF_ORDER</strong></dt> <dt>0x80520306</dt> </dl></td>
<td>Der Speicherort des Caretzeichen ist nicht in der richtigen Reihenfolge. Die Location-Werte müssen in aufsteigender Reihenfolge sortiert werden. <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_CARET_OUTSIDE_STRING"></span><span id="xps_e_caret_outside_string"></span><dl> <dt><strong>XPS_E_CARET_OUTSIDE_STRING</strong></dt> <dt>0x80520305</dt> </dl></td>
<td>Caretzeichen wurden für eine leere Zeichenfolge angegeben. oder der Sprung Index des Caretzeichen hat die Länge der Unicode-Zeichenfolge überschritten. <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_COLOR_COMPONENT_OUT_OF_RANGE"></span><span id="xps_e_color_component_out_of_range"></span><dl> <dt><strong>XPS_E_COLOR_COMPONENT_OUT_OF_RANGE</strong></dt> <dt>0x80520506</dt> </dl></td>
<td>Ein Farbwert liegt außerhalb des zulässigen Bereichs.<br/> Für <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_SCRGB</strong></a> Farbtypen muss der Alphakanal Wert größer oder gleich 0,0 und kleiner oder gleich + 1,0 sein.<br/> Für <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a> Farbtypen müssen die <strong>channelvalues [0]</strong> , die den Alphakanal Wert darstellen, größer oder gleich 0,0 und kleiner oder gleich + 1,0 sein. <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_DICTIONARY_ITEM_NAMED"></span><span id="xps_e_dictionary_item_named"></span><dl> <dt><strong>XPS_E_DICTIONARY_ITEM_NAMED</strong></dt> <dt>0x80520401</dt> </dl></td>
<td>Ein visuelles Element in einem Ressourcen Wörterbuch verfügt über das <strong>Name</strong> -Attribut, das für keine untergeordneten Elemente eines <strong>ResourceDictionary</strong> -Elements angegeben werden kann.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_DUPLICATE_NAMES"></span><span id="xps_e_duplicate_names"></span><dl> <dt><strong>XPS_E_DUPLICATE_NAMES</strong></dt> <dt>0x80520209</dt> </dl></td>
<td>Ein Objekt mit diesem Namen ist bereits im Wörterbuch vorhanden.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_DUPLICATE_RESOURCE_KEYS"></span><span id="xps_e_duplicate_resource_keys"></span><dl> <dt><strong>XPS_E_DUPLICATE_RESOURCE_KEYS</strong></dt> <dt>0x80520200</dt> </dl></td>
<td>Ein Objekt mit diesem Schlüsselnamen ist bereits im Wörterbuch vorhanden.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INDEX_OUT_OF_RANGE"></span><span id="xps_e_index_out_of_range"></span><dl> <dt><strong>XPS_E_INDEX_OUT_OF_RANGE</strong></dt> <dt>0x80520500</dt> </dl></td>
<td>Reserviert.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_BLEED_BOX"></span><span id="xps_e_invalid_bleed_box"></span><dl> <dt><strong>XPS_E_INVALID_BLEED_BOX</strong></dt> <dt>0x80520004</dt> </dl></td>
<td>Das Rechteck mit dem Feld mit dem gebfteten Feld enthält mindestens einen ungültigen Wert. Die gültigen Werte finden Sie in der Parameter Beschreibung. <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_CONTENT_BOX"></span><span id="xps_e_invalid_content_box"></span><dl> <dt><strong>XPS_E_INVALID_CONTENT_BOX</strong></dt> <dt>0x8052000b</dt> </dl></td>
<td>Das Inhaltsfeld Rechteck enthält mindestens einen ungültigen Wert. Die gültigen Werte finden Sie in der Parameter Beschreibung. <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_CONTENT_TYPE"></span><span id="xps_e_invalid_content_type"></span><dl> <dt><strong>XPS_E_INVALID_CONTENT_TYPE</strong></dt> <dt>0x8052000E</dt> </dl></td>
<td>Die Inhaltstyp Zeichenfolge ist ungültig.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_FLOAT"></span><span id="xps_e_invalid_float"></span><dl> <dt><strong>XPS_E_INVALID_FLOAT</strong></dt> <dt>0x80520007</dt> </dl></td>
<td>Ein <strong>float</strong> -Wert ist ungültig. Dabei handelt es sich entweder um eine unbegrenzte oder nicht um eine Zahl (NaN).<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_FONT_URI"></span><span id="xps_e_invalid_font_uri"></span><dl> <dt><strong>XPS_E_INVALID_FONT_URI</strong></dt> <dt>0x8052000a</dt> </dl></td>
<td>Der Schriftart-URI ist ungültig, möglicherweise, weil er ein leeres Fragment oder ungültige Zeichen enthält.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_LANGUAGE"></span><span id="xps_e_invalid_language"></span><dl> <dt><strong>XPS_E_INVALID_LANGUAGE</strong></dt> <dt>0x80520000</dt> </dl></td>
<td>Die angegebene Sprache ist entweder ungültig oder nicht ordnungsgemäß formatiert.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_LOOKUP_TYPE"></span><span id="xps_e_invalid_lookup_type"></span><dl> <dt><strong>XPS_E_INVALID_LOOKUP_TYPE</strong></dt> <dt>0x80520006</dt> </dl></td>
<td>Der Name des Suchschlüssels verweist auf ein Objekt, das nicht der richtige Typ für den-Befehl ist. Wenn die Methode z. b. einen Pinsel zurückgibt, aber der Name des Suchschlüssels auf ein Geometry-Objekt verweist.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_MARKUP"></span><span id="xps_e_invalid_markup"></span><dl> <dt><strong>XPS_E_INVALID_MARKUP</strong></dt> <dt>0x8052000c</dt> </dl></td>
<td>Das gelesene Markup enthält ein-Element oder ein-Attribut, das nicht mit der <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>übereinstimmt.<br/>
<blockquote>
[!Note]<br />
Zum Darstellen von Gleit Komma Werten verwendet das XPS-om den <strong>float</strong> -Datentyp anstelle von <strong>Double</strong>. Wenn ein XPS-Dokument ein Element mit Gleit Komma Daten aufweist, das nicht in einen <strong>float</strong> -Wert passt, wird dieser Fehler zurückgegeben, wenn dieser Wert während der Deserialisierung auftritt.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_NAME"></span><span id="xps_e_invalid_name"></span><dl> <dt><strong>XPS_E_INVALID_NAME</strong></dt> <dt>0x80520001</dt> </dl></td>
<td>Die über gegebene Zeichenfolge ist gemäß der XML Paper Specification kein gültiger Name. <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_OBFUSCATED_FONT_URI"></span><span id="xps_e_invalid_obfuscated_font_uri"></span><dl> <dt><strong>XPS_E_INVALID_OBFUSCATED_FONT_URI</strong></dt> <dt>0x8052000f</dt> </dl></td>
<td>Reserviert.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_PAGE_SIZE"></span><span id="xps_e_invalid_page_size"></span><dl> <dt><strong>XPS_E_INVALID_PAGE_SIZE</strong></dt> <dt>0x80520003</dt> </dl></td>
<td>Die Seiten Dimensionen enthalten einen ungültigen Seitengrößen Wert. <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_RESOURCE_KEY"></span><span id="xps_e_invalid_resource_key"></span><dl> <dt><strong>XPS_E_INVALID_RESOURCE_KEY</strong></dt> <dt>0x80520002</dt> </dl></td>
<td>Gemäß der <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>ist die Zeichenfolge der Suchschlüssel ungültig.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE"></span><span id="xps_e_invalid_thumbnail_image_type"></span><dl> <dt><strong>XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE</strong></dt> <dt>0x80520005</dt> </dl></td>
<td>Der Miniatur Bildtyp wird nicht unterstützt.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_XML_ENCODING"></span><span id="xps_e_invalid_xml_encoding"></span><dl> <dt><strong>XPS_E_INVALID_XML_ENCODING</strong></dt> <dt>0x8052000d</dt> </dl></td>
<td>Es wurde ein falsches oder falsch formatiertes XML-Markup gefunden<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MAPPING_OUT_OF_ORDER"></span><span id="xps_e_mapping_out_of_order"></span><dl> <dt><strong>XPS_E_MAPPING_OUT_OF_ORDER</strong></dt> <dt>0x80520302</dt> </dl></td>
<td>In mindestens einer <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping"><strong>XPS_GLYPH_MAPPING</strong></a> Struktur ist ein Element außerhalb der Reihenfolge. <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MAPPING_OUTSIDE_INDICES"></span><span id="xps_e_mapping_outside_indices"></span><dl> <dt><strong>XPS_E_MAPPING_OUTSIDE_INDICES</strong></dt> <dt>0x80520304</dt> </dl></td>
<td>Die Symbol Zuordnungen überschreiten die Anzahl der Glyphe-Indizes.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MAPPING_OUTSIDE_STRING"></span><span id="xps_e_mapping_outside_string"></span><dl> <dt><strong>XPS_E_MAPPING_OUTSIDE_STRING</strong></dt> <dt>0x80520303</dt> </dl></td>
<td>Fehler in den Symbol Mappings.<br/> Wenn die Unicode-Zeichenfolge leer ist, bedeutet dieser Fehler, dass auch eine Symbol Zuordnung definiert wurde. Symbol Zuordnungen dürfen nicht definiert werden, wenn die Unicode-Zeichenfolge leer ist.<br/> Wenn die Unicode-Zeichenfolge nicht leer ist, bedeutet dieser Fehler, dass eine Symbol Zuordnung für Symbole außerhalb der Unicode-Zeichenfolge definiert wurde. Symbol Zuordnungen können nicht für Symbole definiert werden, die außerhalb der Länge der Unicode-Zeichenfolge liegen.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_COLORPROFILE"></span><span id="xps_e_missing_colorprofile"></span><dl> <dt><strong>XPS_E_MISSING_COLORPROFILE</strong></dt> <dt>0x80520104</dt> </dl></td>
<td>Der Farbprofil Parameter ist <strong>null</strong>, es wird jedoch ein Farbprofil erwartet. Ein Farbprofil ist erforderlich, wenn der Farbtyp XPS_COLOR_TYPE_CONTEXT ist. <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_DISCARDCONTROL"></span><span id="xps_e_missing_discardcontrol"></span><dl> <dt><strong>XPS_E_MISSING_DISCARDCONTROL</strong></dt> <dt>0x80520112</dt> </dl></td>
<td>Eine Seite verweist auf verwerfbare Ressourcen, gibt jedoch keinen verwerfen-Elementnamen an.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_DOCUMENT"></span><span id="xps_e_missing_document"></span><dl> <dt><strong>XPS_E_MISSING_DOCUMENT</strong></dt> <dt>0x80520109</dt> </dl></td>
<td><a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage"><strong>Ixpsompackagewriter:: addPage</strong></a> wurde vor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>ixpsompackagewriter:: startnewdocument</strong></a>aufgerufen.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP"></span><span id="xps_e_missing_documentsequence_relationship"></span><dl> <dt><strong>XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP</strong></dt> <dt>0x80520108</dt> </dl></td>
<td>Das Paket enthält keine "FixedDocumentSequence".<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_FONTURI"></span><span id="xps_e_missing_fonturi"></span><dl> <dt><strong>XPS_E_MISSING_FONTURI</strong></dt> <dt>0x80520107</dt> </dl></td>
<td>Die <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>ixpsomglyphs</strong></a> -Schnittstelle erfordert einen Schriftart-URI, aber eine ist nicht angegeben.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_GLYPHS"></span><span id="xps_e_missing_glyphs"></span><dl> <dt><strong>XPS_E_MISSING_GLYPHS</strong></dt> <dt>0x80520102</dt> </dl></td>
<td>Die <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>ixpsomglyphs</strong></a> -Schnittstelle ohne Unicode-Zeichenfolge gibt keine Glyphe-Indizes an. Eine <strong>ixpsomglyphs</strong> -Schnittstelle muss entweder eine Unicode-Zeichenfolge oder ein Array von Glyphe-Indizes angeben.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH"></span><span id="xps_e_missing_image_in_imagebrush"></span><dl> <dt><strong>XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH</strong></dt> <dt>0x8052010E</dt> </dl></td>
<td>Für den Bild Pinsel konnte keine Bildressource gefunden werden.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_LOOKUP"></span><span id="xps_e_missing_lookup"></span><dl> <dt><strong>XPS_E_MISSING_LOOKUP</strong></dt> <dt>0x80520101</dt> </dl></td>
<td>Die Remote Ressource weist ein unerwartetes Objekt auf.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_NAME"></span><span id="xps_e_missing_name"></span><dl> <dt><strong>XPS_E_MISSING_NAME</strong></dt> <dt>0x80520100</dt> </dl></td>
<td>Die Seite wurde nicht benannt. der Status des Hyperlink-Ziels kann nur festgelegt werden, wenn die Seite einen Namen hat.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_PAGE_IN_DOCUMENT"></span><span id="xps_e_missing_page_in_document"></span><dl> <dt><strong>XPS_E_MISSING_PAGE_IN_DOCUMENT</strong></dt> <dt>0x8052010c</dt> </dl></td>
<td>Das FixedDocument enthält keine FixedPage-Teile. Ein XPS-Dokument muss mindestens einen FixedPage-Teil enthalten.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_PAGE_IN_PAGEREFERENCE"></span><span id="xps_e_missing_page_in_pagereference"></span><dl> <dt><strong>XPS_E_MISSING_PAGE_IN_PAGEREFERENCE</strong></dt> <dt>0x8052010d</dt> </dl></td>
<td>Der Seiten Verweis weist keine entsprechende Seite auf.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_PART_REFERENCE"></span><span id="xps_e_missing_part_reference"></span><dl> <dt><strong>XPS_E_MISSING_PART_REFERENCE</strong></dt> <dt>0x80520110</dt> </dl></td>
<td>Auf einen erforderlichen Zielteil wurde nicht verwiesen.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_PART_STREAM"></span><span id="xps_e_missing_part_stream"></span><dl> <dt><strong>XPS_E_MISSING_PART_STREAM</strong></dt> <dt>0x80520113</dt> </dl></td>
<td>Für die Ressource wurde kein Stream angegeben.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_REFERRED_DOCUMENT"></span><span id="xps_e_missing_referred_document"></span><dl> <dt><strong>XPS_E_MISSING_REFERRED_DOCUMENT</strong></dt> <dt>0x8052010a</dt> </dl></td>
<td>Der FixedDocument-Teil, auf den von "FixedDocumentSequence" verwiesen wird, wurde nicht gefunden. Ein XPS-Dokument muss mindestens ein FixedDocument-Dokument enthalten.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_REFERRED_PAGE"></span><span id="xps_e_missing_referred_page"></span><dl> <dt><strong>XPS_E_MISSING_REFERRED_PAGE</strong></dt> <dt>0x8052010b</dt> </dl></td>
<td>Der FixedPage-Teil, auf den vom FixedDocument verwiesen wird, wurde nicht gefunden. Ein XPS-Dokument muss mindestens einen FixedPage-Teil enthalten.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_RELATIONSHIP_TARGET"></span><span id="xps_e_missing_relationship_target"></span><dl> <dt><strong>XPS_E_MISSING_RELATIONSHIP_TARGET</strong></dt> <dt>0x80520105</dt> </dl></td>
<td>Das Beziehungs Zielpart ist nicht in der Paket Beziehung vorhanden.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_RESOURCE_KEY"></span><span id="xps_e_missing_resource_key"></span><dl> <dt><strong>XPS_E_MISSING_RESOURCE_KEY</strong></dt> <dt>0x8052010f</dt> </dl></td>
<td>Für die Ressource wurde kein <strong>x:Key</strong> -Attribut angegeben.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_RESOURCE_RELATIONSHIP"></span><span id="xps_e_missing_resource_relationship"></span><dl> <dt><strong>XPS_E_MISSING_RESOURCE_RELATIONSHIP</strong></dt> <dt>0x80520106</dt> </dl></td>
<td>Die Ressource, auf die der Inhalt der Seite oder des Remote Wörterbuchs verweist, ist nicht als Seiten Beziehung vorhanden.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP"></span><span id="xps_e_missing_restricted_font_relationship"></span><dl> <dt><strong>XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520111</dt> </dl></td>
<td>Die beschränkte Schriftart, auf die verwiesen wird, wurde im Aufrufen von <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>ixpsompackagewriter:: startnewdocument</strong></a>nicht angegeben.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_SEGMENT_DATA"></span><span id="xps_e_missing_segment_data"></span><dl> <dt><strong>XPS_E_MISSING_SEGMENT_DATA</strong></dt> <dt>0x80520103</dt> </dl></td>
<td>Das Segment Daten Array weist weniger Einträge als das Array Segmenttypen auf. <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS"></span><span id="xps_e_multiple_documentsequence_relationships"></span><dl> <dt><strong>XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS</strong></dt> <dt>0x80520202</dt> </dl></td>
<td>Es wurde versucht, einem Paket, das bereits ein Paket enthält, eine "FixedDocumentSequence" hinzuzufügen. Ein XPS-Dokument muss nur einen FixedDocumentSequence-Teil enthalten.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT"></span><span id="xps_e_multiple_printtickets_on_document"></span><dl> <dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT</strong></dt> <dt>0x80520206</dt> </dl></td>
<td>Es wurde versucht, ein Druck Ticket auf Dokument Ebene zu einem FixedDocument hinzuzufügen, das bereits über eines verfügt. Ein "FixedDocument" in einem XPS-Dokument kann nur ein Druck Ticket auf Dokument Ebene enthalten.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE"></span><span id="xps_e_multiple_printtickets_on_documentsequence"></span><dl> <dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE</strong></dt> <dt>0x80520207</dt> </dl></td>
<td>Es wurde versucht, ein Druck Ticket auf Auftrags Ebene zu einer FixedDocumentSequence hinzuzufügen, die bereits über eine verfügt. Die "FixedDocumentSequence" in einem XPS-Dokument kann nur ein Druck Ticket auf Auftrags Ebene enthalten.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE"></span><span id="xps_e_multiple_printtickets_on_page"></span><dl> <dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE</strong></dt> <dt>0x80520205</dt> </dl></td>
<td>Es wurde versucht, ein Druck Ticket auf Seitenebene zu einer FixedPage hinzuzufügen, die bereits über eine verfügt. Eine FixedPage in einem XPS-Dokument kann nur ein Druck Ticket auf Seitenebene enthalten.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_REFERENCES_TO_PART"></span><span id="xps_e_multiple_references_to_part"></span><dl> <dt><strong>XPS_E_MULTIPLE_REFERENCES_TO_PART</strong></dt> <dt>0x80520208</dt> </dl></td>
<td>Die eingeschränkte Schriftart Auflistung enthielt einen eingeschränkten Schriftart Eintrag, der wiederholt wurde. Jeder Schriftart Eintrag kann in der Auflistung nur einmal vorkommen.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_RESOURCES"></span><span id="xps_e_multiple_resources"></span><dl> <dt><strong>XPS_E_MULTIPLE_RESOURCES</strong></dt> <dt>0x80520201</dt> </dl></td>
<td>Eine Ressource mit diesem Teilnamen ist bereits vorhanden.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE"></span><span id="xps_e_multiple_thumbnails_on_package"></span><dl> <dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE</strong></dt> <dt>0x80520204</dt> </dl></td>
<td>Es wurde versucht, einem Paket, das bereits über eine Miniaturansicht verfügt, ein Miniaturbild hinzuzufügen. Ein XPS-Dokument kann nur ein Miniaturbild auf Paketebene enthalten.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE"></span><span id="xps_e_multiple_thumbnails_on_page"></span><dl> <dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE</strong></dt> <dt>0x80520203</dt> </dl></td>
<td>Es wurde versucht, ein Miniaturbild auf Seitenebene zu einer FixedPage hinzuzufügen, die bereits über ein Bild verfügt. Eine FixedPage in einem XPS-Dokument kann nur ein Miniaturbild der Seitenebene enthalten.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_NEGATIVE_FLOAT"></span><span id="xps_e_negative_float"></span><dl> <dt><strong>XPS_E_NEGATIVE_FLOAT</strong></dt> <dt>0x8052030a</dt> </dl></td>
<td>Ein Eintrag enthält einen negativen Wert, er muss jedoch einen nicht negativen Wert enthalten. <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_NESTED_REMOTE_DICTIONARY"></span><span id="xps_e_nested_remote_dictionary"></span><dl> <dt><strong>XPS_E_NESTED_REMOTE_DICTIONARY</strong></dt> <dt>0x80520402</dt> </dl></td>
<td>Es wurde versucht, einen Remote-Wörterbuch Verweis zu einem Remote Wörterbuch hinzuzufügen. Ein Remote Wörterbuch kann nicht auf ein anderes Remote Wörterbuch<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_NO_CUSTOM_OBJECTS"></span><span id="xps_e_no_custom_objects"></span><dl> <dt><strong>XPS_E_NO_CUSTOM_OBJECTS</strong></dt> <dt>0x80520502</dt> </dl></td>
<td>Ein Schnittstellen Zeiger verweist nicht auf eine erkannte Schnittstellen Implementierung. Benutzerdefinierte Implementierungen von XPS-Dokument-API-Schnittstellen werden nicht unterstützt.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_NOT_ENOUGH_GRADIENT_STOPS"></span><span id="xps_e_not_enough_gradient_stops"></span><dl> <dt><strong>XPS_E_NOT_ENOUGH_GRADIENT_STOPS</strong></dt> <dt>0x8052050b</dt> </dl></td>
<td>Die Auflistung der Farbverlaufs Stopps weist weniger als zwei Stopps auf. Eine Auflistung von Farbverlaufs Stopps muss über mindestens zwei Farbverlaufs Stopps verfügen.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_ODD_BIDILEVEL"></span><span id="xps_e_odd_bidilevel"></span><dl> <dt><strong>XPS_E_ODD_BIDILEVEL</strong></dt> <dt>0x80520307</dt> </dl></td>
<td>Die Text Zeichenfolge wurde als ausgerichtete Seite und von rechts nach Links angegeben. Wenn der Text seitwärts ausgerichtet ist, kann er nicht über eine Bidi-Ebene verfügen, bei der es sich um einen ungeraden Wert handelt (von rechts nach links). Ebenso kann, wenn die Bidi-Ebene ein ungerader Wert ist, der Text nicht seitwärts ausgerichtet werden.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_ONE_TO_ONE_MAPPING_EXPECTED"></span><span id="xps_e_one_to_one_mapping_expected"></span><dl> <dt><strong>XPS_E_ONE_TO_ONE_MAPPING_EXPECTED</strong></dt> <dt>0x80520308</dt> </dl></td>
<td>Die Symbol Zuordnungen stimmen nicht mit dem Inhalt der Unicode-Zeichenfolge identisch.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_PACKAGE_WRITER_NOT_CLOSED"></span><span id="xps_e_package_writer_not_closed"></span><dl> <dt><strong>XPS_E_PACKAGE_WRITER_NOT_CLOSED</strong></dt> <dt>0x8052050c</dt> </dl></td>
<td>Der paketwriter wurde vor der Freigabe nicht geschlossen.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_RELATIONSHIP_EXTERNAL"></span><span id="xps_e_relationship_external"></span><dl> <dt><strong>XPS_E_RELATIONSHIP_EXTERNAL</strong></dt> <dt>0x8052050a</dt> </dl></td>
<td>Eine Beziehung verweist auf einen Teil außerhalb des XPS-Dokuments. Alle Inhalte, die in einem XPS-Dokument gerendert werden sollen, müssen im XPS-Dokument enthalten sein.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_RESOURCE_NOT_OWNED"></span><span id="xps_e_resource_not_owned"></span><dl> <dt><strong>XPS_E_RESOURCE_NOT_OWNED</strong></dt> <dt>0x80520504</dt> </dl></td>
<td>Reserviert.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED"></span><span id="xps_e_restricted_font_not_obfuscated"></span><dl> <dt><strong>XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED</strong></dt> <dt>0x80520309</dt> </dl></td>
<td><em>Reserviert</em>.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_STRING_TOO_LONG"></span><span id="xps_e_string_too_long"></span><dl> <dt><strong>XPS_E_STRING_TOO_LONG</strong></dt> <dt>0x80520300</dt> </dl></td>
<td>Bei dem Versuch, eine Zeichenfolge in einen neuen Puffer zu kopieren, ist ein <strong>size_t</strong> Überlauf aufgetreten.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_TOO_MANY_INDICES"></span><span id="xps_e_too_many_indices"></span><dl> <dt><strong>XPS_E_TOO_MANY_INDICES</strong></dt> <dt>0x80520301</dt> </dl></td>
<td>Es gab mehr Symbol Indizes als Unicode-Code Punkte. Wenn keine Symbol Zuordnungen vorhanden sind, muss die Anzahl von Glyphe-Indizes kleiner oder gleich der Anzahl von Unicode-Code Punkten sein.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNAVAILABLE_PACKAGE"></span><span id="xps_e_unavailable_package"></span><dl> <dt><strong>XPS_E_UNAVAILABLE_PACKAGE</strong></dt> <dt>0x80520114</dt> </dl></td>
<td>Ein schwerwiegender Fehler ist aufgetreten, und der Inhalt des XPS OM kann nicht wieder hergestellt werden können. Einige Komponenten des XPS OM sind möglicherweise weiterhin verwendbar, müssen jedoch vor der weiteren Verwendung überprüft werden. Da der Zustand des XPS-OMS nach dem zurückgeben dieses Fehlers nicht vorhergesagt werden kann, sollten alle Komponenten des XPS-OM freigegeben und verworfen werden.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_UNEXPECTED_COLORPROFILE"></span><span id="xps_e_unexpected_colorprofile"></span><dl> <dt><strong>XPS_E_UNEXPECTED_COLORPROFILE</strong></dt> <dt>0x80520505</dt> </dl></td>
<td>Ein Farbprofil war vorhanden, als es nicht erwartet wurde. Ein Farbprofil ist nur zulässig, wenn der Farbtyp <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a>ist. <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNEXPECTED_CONTENT_TYPE"></span><span id="xps_e_unexpected_content_type"></span><dl> <dt><strong>XPS_E_UNEXPECTED_CONTENT_TYPE</strong></dt> <dt>0x80520008</dt> </dl></td>
<td>Das Ziel einer Beziehung ist nicht der Typ, der vom Kontext der Beziehung erwartet wird. <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_UNEXPECTED_RELATIONSHIP_TYPE"></span><span id="xps_e_unexpected_relationship_type"></span><dl> <dt><strong>XPS_E_UNEXPECTED_RELATIONSHIP_TYPE</strong></dt> <dt>0x80520010</dt> </dl></td>
<td>Der Beziehungstyp wurde nicht erkannt.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP"></span><span id="xps_e_unexpected_restricted_font_relationship"></span><dl> <dt><strong>XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520011</dt> </dl></td>
<td>Die eingeschränkte Schriftart Auflistung enthält eine uneingeschränkte Schriftart.<br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_VISUAL_CIRCULAR_REF"></span><span id="xps_e_visual_circular_ref"></span><dl> <dt><strong>XPS_E_VISUAL_CIRCULAR_REF</strong></dt> <dt>0x80520501</dt> </dl></td>
<td>Reserviert.<br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT"></span><span id="xps_e_xkey_attr_present_outside_res_dict"></span><dl> <dt><strong>XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT</strong></dt> <dt>0x80520400</dt> </dl></td>
<td>Für eine Pfad Geometrie, die nicht in einem Ressourcen Wörterbuch enthalten ist, ist ein <strong>x:Key</strong> -Attribut angegeben. Pfadgeometrien, die nicht in einem Ressourcen Wörterbuch enthalten sind, dürfen kein <strong>x:Key</strong> -Attribut aufweisen.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Einige XPS-Dokument-API-Methoden führen Aufrufe an die [Paketierungs](/previous-versions/windows/desktop/opc/packaging) -API aus. Informationen zu den Rückgabe Werten der Packungs-API finden Sie unter [Packen von Fehlern](/previous-versions/windows/desktop/opc/packaging-errors).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop-Apps\]<br/> |
| Header<br/>                   | <dl> <dt>Xpsobjectmodel. h</dt> </dl>                                       |
| IDL<br/>                      | <dl> <dt>Xpsobjectmodel. idl</dt> </dl>                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Fehlerbehandlung in com](../com/error-handling-in-com.md)
</dt> </dl>

 

