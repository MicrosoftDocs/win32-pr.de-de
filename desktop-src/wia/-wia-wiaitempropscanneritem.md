---
description: Die folgenden Konstanten geben den gültigen Satz von Eigenschaften des Windows-Abbild Erfassungs Elements (WIA) an.
ms.assetid: c7c5b10b-81e8-4a30-b20a-ea187724ddd4
title: Eigenschaften Konstanten für Scanner-WIA-Elemente (wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPS_AUTO_DESKEW
- WIA_IPS_BRIGHTNESS
- WIA_IPS_CONTRAST
- WIA_IPS_CUR_INTENT
- WIA_IPS_DESKEW_X
- WIA_IPS_DESKEW_Y
- WIA_IPS_DOCUMENT_HANDLING_SELECT
- WIA_IPS_FILM_NODE_NAME
- WIA_IPS_FILM_SCAN_MODE
- WIA_IPS_INVERT
- WIA_IPA_ITEMS_STORED
- WIA_IPS_LAMP
- WIA_IPS_LAMP_AUTO_OFF
- WIA_IPS_MAX_HORIZONTAL_SIZE
- WIA_IPS_MAX_VERTICAL_SIZE
- WIA_IPS_MIN_HORIZONTAL_SIZE
- WIA_IPS_MIN_VERTICAL_SIZE
- WIA_IPS_MIRROR
- WIA_IPS_OPTICAL_XRES
- WIA_IPS_OPTICAL_YRES
- WIA_IPS_ORIENTATION
- WIA_IPS_PAGE_SIZE
- WIA_IPS_PAGE_HEIGHT
- WIA_IPS_PAGE_WIDTH
- WIA_IPS_PAGES
- WIA_IPS_PHOTOMETRIC_INTERP
- WIA_IPS_PREVIEW
- WIA_IPS_PREVIEW_TYPE
- WIA_IPS_ROTATION
- WIA_IPS_SEGMENTATION
- WIA_IPS_SHEET_FEEDER_REGISTRATION
- WIA_IPS_SHOW_PREVIEW_CONTROL
- WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION
- WIA_IPS_THRESHOLD
- WIA_IPS_TRANSFER_CAPABILITIES
- WIA_IPA_UPLOAD_ITEM_SIZE
- WIA_IPS_WARM_UP_TIME
- WIA_IPS_XEXTENT
- WIA_IPS_XPOS
- WIA_IPS_XRES
- WIA_IPS_XSCALING
- WIA_IPS_YEXTENT
- WIA_IPS_YPOS
- WIA_IPS_YRES
- WIA_IPS_YSCALING
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: aa3b1cc4ae14a9460a24f652a9599035cacca2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346954"
---
# <a name="scanner-wia-item-property-constants"></a>Eigenschaften Konstanten für Scanner-WIA-Elemente

Die folgenden Konstanten geben den gültigen Satz von Eigenschaften des Windows-Abbild Erfassungs Elements (WIA) an.

Das Präfix "WIA \_ IPS \_ " gibt eine Element Eigenschaft für Scanner-Geräte an und ist die Namenskonvention, die in C/C++ verwendet wird. Bei der Skripterstellung verwenden diese Konstanten das Präfix "scannerpicture" und sind Teil des enumerierten Typs " [wiaitempropertyid](-wia-wiaitempropertyid.md) ". Der entsprechende Elementname aus dieser Skript Enumeration wird in Klammern neben dem Konstanten Namen C/C++ in der folgenden Liste angezeigt.



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
<td style="text-align: left;"><span id="WIA_IPS_AUTO_DESKEW"></span><span id="wia_ips_auto_deskew"></span><dl> <dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>scannerpictureautodebug</dt> </dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
<br/> Schaltet die automatische deschiefe ein bzw. aus.<br/> Optional nur für WIA_CATEGORY_FEEDER.<br/> Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a><br/> Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind. 
<table>
<thead>
<tr class="header">
<th>Konstante</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_AUTO_DESKEW_ON</td>
<td>Aktivieren Sie die automatische deschiefe.</td>
</tr>
<tr class="even">
<td>WIA_AUTO_DESKEW_OFF</td>
<td>Deaktivieren Sie die automatische deschiefe.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_BRIGHTNESS"></span><span id="wia_ips_brightness"></span><dl> <dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>scannerpicturehelligkeit</dt> </dl></td>
<td style="text-align: left;"><p>Die Bildhelligkeit-Werte, die innerhalb des Scanners verfügbar sind.</p>
<p>Enthält die aktuelle Hardware Helligkeitseinstellung für das Gerät. Eine Anwendung legt diese Eigenschaft auf den Helligkeitswert der Hardware fest. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Werte sollten in einem Bereich zwischen-1000 und 1000 zugeordnet werden, wobei 1000 der maximalen Helligkeit entspricht, 0 der normalen Helligkeit entspricht und-1000 der minimalen Helligkeit entspricht.</p>
<p>Erforderlich für alle Elemente in den Kategorien: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK und WIA_CATEGORY_FILM. Optional, jedoch empfohlen, für WIA_CATEGORY_FINISHED_FILE Elemente, die Vorschau unterstützen.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_CONTRAST"></span><span id="wia_ips_contrast"></span><dl> <dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>scannerpicturecontrast</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die aktuelle Hardware Kontrasteinstellung für ein Gerät. Eine Anwendung legt diese Eigenschaft auf den Kontrastwert der Hardware fest. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Werte sollten in einem Bereich zwischen-1000 und 1000 zugeordnet werden, wobei-1000 dem minimalen Kontrast entspricht, 0 dem normalen Kontrast entspricht und 1000 dem maximalen Kontrast entspricht.</p>
<p>Erforderlich für alle Elemente in den Kategorien: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK und WIA_CATEGORY_FILM. Optional, jedoch empfohlen, für WIA_CATEGORY_FINISHED_FILE Elemente, die Vorschau unterstützen.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_CUR_INTENT"></span><span id="wia_ips_cur_intent"></span><dl> <dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>scannerpicturecurintent</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die aktuellen Intent-Einstellungen. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Erforderlich für alle Erwerbs aktivierten Elemente; Das heißt, Elemente in den Kategorien: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK und WIA_CATEGORY_FILM. Sie wird für WIA_CATEGORY_FINISHED_FILE-oder WIA_CATEGORY_FOLDER-Elemente nicht unterstützt.</p>
<p>Typ: <strong>VT_I4</strong> Access: Read/Write, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></p>
<p>Der Treiber verwendet diese, um die Element Eigenschaften basierend auf der beabsichtigten Verwendung des Bilds einer Anwendung vorzusetzen. Dies kann z. b. die maximale Qualität, die minimale Größe usw. einschließen.</p>
<p>Der Treiber wählt die Bittiefe in dpi (Punkte pro Zoll) und andere Einstellungen aus, die für die ausgewählte Absicht festgelegt sind. Die Anwendung kann die aktuellen Einstellungen lesen, um zu bestimmen, welche Eigenschaften geändert wurden. Eine Anwendung legt diese Eigenschaft fest, um die WIA-Eigenschaften für eine bestimmte Erwerbs Absicht automatisch festzulegen. Diese Eigenschaft ist für alle Scanner erforderlich.</p>
<p>Eine Anwendung legt diese Eigenschaft fest, um die WIA-Eigenschaften für eine bestimmte Erwerbs Absicht automatisch festzulegen.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Die Flags können mit einem bitweisen <strong>or</strong> -Operator kombiniert werden, aber ein Bild kann nicht gleichzeitig Graustufen und Farben sein.
</blockquote>
</div>
<div>
 
</div>
<p>Diese Eigenschaft ist für alle Scanner erforderlich.</p>
<p>In der folgenden Tabelle sind die Abbildtyp-Flags und ihre Definitionen enthalten. Diese Flags werden verwendet, um festzulegen, welcher Typ von Image gemeint ist: Color, Grayscale usw.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Vorgesehene Abbildtyp-Flags</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_INTENT_NONE</td>
<td>Standardwert. Es wurde keine Absicht angegeben.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_IMAGE_TYPE_COLOR</td>
<td>Die Anwendung soll das Gerät auf einen Farbscan vorbereiten.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_IMAGE_TYPE_GRAYSCALE</td>
<td>Die Anwendung soll das Gerät auf eine Graustufen Überprüfung vorbereiten.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_IMAGE_TYPE_TEXT</td>
<td>Die Anwendung soll das Gerät für das Scannen von Text vorbereiten.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_IMAGE_TYPE_MASK</td>
<td>Maske für alle Bildtyp-Flags.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>In der folgenden Tabelle sind die Metriken für Qualität und Größe sowie deren Definitionen enthalten. Diese Flags werden verwendet, um festzulegen, welche Qualität gemeint ist.</p>

<table>
<thead>
<tr class="header">
<th>Vorgesehene Image Größe/qualitätsflags</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_INTENT_MINIMIZE_SIZE</td>
<td>Die Anwendung soll das Gerät für die Überprüfung eines Abbilds vorbereiten, das sich auf eine kleine Überprüfung ergibt.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_MAXIMIZE_QUALITY</td>
<td>Die Anwendung soll das Gerät für das Scannen eines hochwertigen Images vorbereiten.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_SIZE_MASK</td>
<td>Dieses Flag ist eine Maske für alle Größen-/qualitätsflags.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_BEST_PREVIEW</td>
<td>Die Anwendung soll das Gerät für das Scannen einer Vorschau vorbereiten.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_X"></span><span id="wia_ips_deskew_x"></span><dl> <dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>scannerpicturedebug</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Anzahl der Pixel in der x-Richtung, von WIA_IPS_XPOS bis zur x-Koordinate der obersten Ecke des Bilds, die verzerrt werden soll. Daher wird in Verbindung mit WIA_IPS_DESKEW_Y beschrieben, wo sich die beiden oberen Ecken des schrägten Bilds innerhalb des umgebenden Rechtecks befinden, das durch WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT und WIA_IPS_YEXTENT definiert ist. seine-Eigenschaft wird vom Scanner-Treiber implementiert, wenn er das aufschrauben unterstützt.</p>
<p>Die gültigen Werte für WIA_IPS_DESKEW_X müssen zwischen 0 und (WIA_IPS_XEXTENT-1) liegen. Der Wert 0 bedeutet, dass keine Abweichung ausgeführt werden soll.</p>
<p>Diese Eigenschaft ist für Elemente der Kategorien WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER und WIA_CATEGORY_FILM optional. und ist für WIA_CATEGORY_FINISHED_FILE-oder WIA_CATEGORY_FOLDER-Elemente nicht verfügbar.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_DESKEW_Y"></span><span id="wia_ips_deskew_y"></span><dl> <dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>scannerpicturedebug</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Anzahl der Pixel in der y-Richtung von WIA_IPS_YPOS bis zur y-Koordinate der linken linken Ecke des Bilds, die verzerrt werden soll. Daher wird in Verbindung mit WIA_IPS_DESKEW_X beschrieben, wo sich die beiden oberen Ecken des schrägten Bilds innerhalb des umgebenden Rechtecks befinden, das durch WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT und WIA_IPS_YEXTENT definiert ist. Diese Eigenschaft wird vom Scanner-Treiber implementiert, wenn Sie die Unterstützung von "Debug" unterstützt.</p>
<p>Die gültigen Werte für WIA_IPS_DESKEW_Y müssen zwischen 0 und (WIA_IPS_YEXTENT-1) liegen. Der Wert 0 bedeutet, dass keine Abweichung ausgeführt werden soll.</p>
<p>Diese Eigenschaft ist für Elemente der Kategorien WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER und WIA_CATEGORY_FILM optional. und ist für WIA_CATEGORY_FINISHED_FILE-oder WIA_CATEGORY_FOLDER-Elemente nicht verfügbar.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_ips_document_handling_select"></span><dl> <dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>scannerpicturedocumenthandlingselect</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die aktuelle Scanner-Erfassungs Quelle und den aktuellen Modus. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung liest diese Eigenschaft, um die aktuelle Erwerbs Quelle des Scanners zu ermitteln oder diese Eigenschaft zu schreiben, um die Quelle und den Modus des Scanners festzulegen. Außerdem verwenden Anwendungen diese Eigenschaft, um die Duplexer-Funktionalität zu aktivieren und zu deaktivieren.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind. </p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Gelegene</td>
<td>Mithilfe von Duplexer-Vorgängen scannen. Überprüfen Sie beide Dokument Seiten mithilfe der für das Feedelement (WIA_CATEGORY_FEEDER) konfigurierten allgemeinen Einstellungen. Duplex und ADVANCE_DUPLEX können nicht gleichzeitig festgelegt werden.</td>
</tr>
<tr class="even">
<td>ADVANCED_DUPLEX</td>
<td>Überprüfen Sie die einzelnen Einstellungen, die für jedes untergeordnete Feedelement (WIA_CATEGORY_FEEDER_FRONT und WIA_CATEGORY_FEEDER_BACK) konfiguriert sind. Duplex und ADVANCE_DUPLEX können nicht gleichzeitig festgelegt werden.</td>
</tr>
<tr class="odd">
<td>FRONT_FIRST</td>
<td>Scannen Sie zuerst den Anfang des Dokuments. Dieser Wert ist gültig, wenn Duplex oder ADVANCED_DUPLEX festgelegt ist.</td>
</tr>
<tr class="even">
<td>BACK_FIRST</td>
<td>Scannen Sie zuerst das Dokument zurück. Dieser Wert ist gültig, wenn Duplex oder ADVANCED_DUPLEX festgelegt ist.</td>
</tr>
<tr class="odd">
<td>FRONT_ONLY</td>
<td>Nur den Vordergrund suchen.</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>Nur Rück scannen. Dieser Wert ist gültig, wenn Duplex oder ADVANCED_DUPLEX festgelegt ist.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_FILM_NODE_NAME"></span><span id="wia_ips_film_node_name"></span><dl> <dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>scannerpicturefilmnodename</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Ermöglicht die Angabe einer bestimmten filmscaninganlage, wenn mehrere vorhanden sind.</p>
<p>Diese Eigenschaft ist für die WIA_CATEGORY_FILM Elemente erforderlich, wenn mehrere Film Scan Elemente vorhanden sind. Wenn das Gerät nur ein Stamm Scanner-Film Element unterstützt, ist diese Eigenschaft optional.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Zulässige Werte: der BSTR sollte die Form aufweisen @ResourceBinary , <ResourceID> um die Lokalisierung zuzulassen, da diese Zeichenfolge für den Benutzer über die Benutzeroberfläche der Film Überprüfung verfügbar gemacht wird.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_FILM_SCAN_MODE"></span><span id="wia_ips_film_scan_mode"></span><dl> <dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>scannerpicturefilmscanmode</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Aktiviert die Konfiguration des aktuellen videoscans.</p>
<p>Diese Eigenschaft ist für das WIA_CATEGORY_FILM Element erforderlich.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind. </p>
<table>
<thead>
<tr class="header">
<th>Konstante</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_FILM_COLOR_SLIDE</td>
<td>Eine Farb Folie suchen.</td>
</tr>
<tr class="even">
<td>WIA_FILM_COLOR_NEGATIVE</td>
<td>Sucht nach einer Farbe, die negativ ist.</td>
</tr>
<tr class="odd">
<td>WIA_FILM_BW_NEGATIVE</td>
<td>Sucht nach einem schwarzen und weißen negativen Wert.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_INVERT"></span><span id="wia_ips_invert"></span><dl> <dt><strong>WIA_IPS_INVERT</strong></dt> <dt>scannerpictureinvert</dt> </dl></td>
<td style="text-align: left;"><p>Reserviert für zukünftige Verwendung und wird zurzeit nicht implementiert.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>scannerpictureinvert</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt an, wie viele Elemente im WIA_CATEGORY_FOLDER Element gespeichert werden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_LAMP"></span><span id="wia_ips_lamp"></span><dl> <dt><strong>WIA_IPS_LAMP</strong></dt> <dt>scannerpicturelamp</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Schaltet die scannerlamp ein bzw. aus.</p>
<p>Optional für die Elemente WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER und WIA_CATEGORY_FILM und empfohlen für WIA_CATEGORY_FILM.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind. </p>
<table>
<thead>
<tr class="header">
<th>Konstante</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_LAMP_ON</td>
<td>Schalten Sie die Lamp ein.</td>
</tr>
<tr class="even">
<td>WIA_LAMP_OFF</td>
<td>Schalten Sie den Lamp aus.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_LAMP_AUTO_OFF"></span><span id="wia_ips_lamp_auto_off"></span><dl> <dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>scannerpicturelampautooff</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Legt die maximale Zeit fest, in der die Lamp beibehalten werden soll, wenn der Scanner nicht verwendet wird.</p>
<p>Optional für die Elemente WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER und WIA_CATEGORY_FILM und empfohlen für WIA_CATEGORY_FILM.</p>
<p>Typ: <strong>VT_UI4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: 0-0xfff Sekunden</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MAX_HORIZONTAL_SIZE"></span><span id="wia_ips_max_horizontal_size"></span><dl> <dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>scannerpicturemaxhorizontalsize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt die maximale Breite (in Tausendstel Zoll) an, die in der horizontalen Achse (X) der aktuellen Auflösung gescannt wird. Dabei kann es sich um die Breite des Blatt-Feeds oder des Scannens handeln, je nach Typ des Elements.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MAX_VERTICAL_SIZE"></span><span id="wia_ips_max_vertical_size"></span><dl> <dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>scannerpicturemaxverticalsize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt die maximale Höhe in Tausendstel Zoll an, die auf der vertikalen Achse (Y-Achse) bei der aktuellen Auflösung gescannt wird. Dabei kann es sich um die Höhe des Blatt-Feeds oder des Scannens handeln, je nach Typ des Elements.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIN_HORIZONTAL_SIZE"></span><span id="wia_ips_min_horizontal_size"></span><dl> <dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>scannerpictureminhorizontalsize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt die minimale Breite (in Tausendstel Zoll) an, die in der horizontalen Achse (X) der aktuellen Auflösung gescannt wird.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_MIN_VERTICAL_SIZE"></span><span id="wia_ips_min_vertical_size"></span><dl> <dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>scannerpictureminverticalsize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt die minimale Höhe in Tausendstel Zoll an, die auf der vertikalen Achse (Y-Achse) bei der aktuellen Auflösung gescannt wird.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_MIRROR"></span><span id="wia_ips_mirror"></span><dl> <dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>scannerpicturemirror</dt> </dl></td>
<td style="text-align: left;"><p>Reserviert für zukünftige Verwendung und wird zurzeit nicht implementiert.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_XRES"></span><span id="wia_ips_optical_xres"></span><dl> <dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>scannerpictureopticalxres</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Horizontale optische Auflösung. Höchste unterstützte horizontale optische Auflösung in dpi. Diese Eigenschaft ist ein einzelner Wert. Dabei handelt es sich nicht um eine Liste aller Auflösungen, die vom Gerät generiert werden können. Vielmehr handelt es sich hierbei um die Auflösung der Geräte Optiken. Der Mini Treiber erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft ist für alle Elemente erforderlich.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_OPTICAL_YRES"></span><span id="wia_ips_optical_yres"></span><dl> <dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>scannerpictureopticalyres</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Vertikale optische Auflösung. Höchste unterstützte vertikale optische Auflösung in dpi. Diese Eigenschaft ist ein einzelner Wert. Dabei handelt es sich nicht um eine Liste aller Auflösungen, die vom Gerät generiert werden. Vielmehr handelt es sich hierbei um die Auflösung der Geräte Optiken. Der Mini Treiber erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft ist für alle Elemente erforderlich.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ORIENTATION"></span><span id="wia_ips_orientation"></span><dl> <dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>scannerpictureorientation</dt> </dl></td>
<td style="text-align: left;"><p>Gibt die aktuelle Ausrichtung der zu scannenden Dokumente an. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung legt diese Eigenschaft fest, um die ursprüngliche Ausrichtung einer Seite oder eines Bilds zu definieren, die abgerufen werden soll. Weitere Informationen zur Verwendung von WIA_IPS_ORIENTATION finden Sie unter <strong>WIA_IPS_PAGE_SIZE</strong>.</p>
<div class="alert">
<blockquote>
[!Note]<br />
WIA_IPS_ORIENTATION bezieht sich auf die Position des Dokuments, das auf dem Scanner-oder-Feeder gescannt werden soll. Dabei handelt es sich um die Ausrichtung des Dokuments in Relation zur Richtung des Scans. WIA_IPS_ROTATION bezieht sich auf die Drehung, die auf das Bild angewendet wird, nachdem es gescannt wurde, kurz bevor das Bild an die Anwendung übertragen wird.
</blockquote>
</div>
<div>
 
</div>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die vier Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hochformat</td>
<td>0 Grad.</td>
</tr>
<tr class="even">
<td>Landschaf</td>
<td>90-Grad-Drehung gegen den Uhrzeigersinn, relativ zur Hochformat Ausrichtung.</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>180-Grad-Drehung gegen den Uhrzeigersinn, relativ zur Hochformat Ausrichtung.</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>270-Grad-Drehung gegen den Uhrzeigersinn, relativ zur Hochformat Ausrichtung.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_SIZE"></span><span id="wia_ips_page_size"></span><dl> <dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>scannerpicturepagesize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Größe der Seite, die zurzeit als gescannt festgelegt ist. Eine Anwendung legt diese Eigenschaft fest, um die Dimensionen der zu überprüfenden Seite auszuwählen. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Informationen zu den Konstanten, die mit dieser Eigenschaft verwendet werden können, finden Sie unter <a href="-wia-wia2-pagesizeconstants.md"><strong>WIA 2,0 page size Konstanten</strong></a>. Beachten Sie diese nicht festgelegten Größen, insbesondere: </p>
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PAGE_CUSTOM</td>
<td>Definiert durch die Werte der Eigenschaften <strong>WIA_IPS_PAGE_HEIGHT</strong> und <strong>WIA_IPS_PAGE_WIDTH</strong> .</td>
</tr>
<tr class="even">
<td>WIA_PAGE_AUTO</td>
<td>Die Seitengröße wird automatisch vom Gerät festgelegt.</td>
</tr>
<tr class="odd">
<td>WIA_PAGE_CUSTOM_BASE</td>
<td>Eine benutzerdefinierte Seitengröße, deren Dimensionen der Anwendung und dem Gerätetreiber bereits bekannt sind.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Der Wert der <strong>WIA_IPS_ORIENTATION</strong> -Eigenschaft bestimmt die Ausrichtung der aktuell ausgewählten Seite. Die Eigenschaften " <strong>WIA_IPS_PAGE_WIDTH</strong> " und " <strong>WIA_IPS_PAGE_HEIGHT</strong> " melden die Dimensionen der Seite in Tausendstel Zoll. Diese Eigenschaften müssen mit <strong>WIA_IPS_XEXTENT</strong> und <strong>WIA_IPS_YEXTENT</strong>übereinstimmen, die die Abmessungen der Seite in Pixel enthalten.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Gültige Werte vom Typ WIA_PROP_LIST abhängig von gültigen Einstellungen der Eigenschaft <strong>WIA_IPS_ORIENTATION</strong> . Wenn das Gerät z. b. keine Querformat orientierten Dokumente mit einer WIA_PAGE_A4 Einstellung Scannen kann, ist WIA_PAGE_A4 kein gültiger Wert für die Eigenschaft <strong>WIA_IPS_PAGE_SIZE</strong> , wenn <strong>WIA_IPS_ORIENTATION</strong> auf Querformat festgelegt ist.
</blockquote>
</div>
<div>
 
</div>
<p>Wenn eine Anwendung <strong>WIA_IPS_PAGE_SIZE</strong> auf einen anderen Wert als die drei in der obigen Tabelle festlegt, sollte der Mini Treiber die Werte <strong>WIA_IPS_PAGE_WIDTH</strong> und <strong>WIA_IPS_PAGE_HEIGHT</strong> den Dimensionen der Seite in Tausendstel Zoll anpassen. Außerdem sollten die Werte <strong>WIA_IPS_XEXTENT</strong> und <strong>WIA_IPS_YEXTENT</strong> auf die Dimensionen der Seite in Pixel angepasst werden.</p>
<p>Wenn eine Block Einstellung (<strong>WIA_IPS_XEXTENT</strong> oder <strong>WIA_IPS_YEXTENT</strong>) in einen Wert geändert wird, der nicht mit der aktuellen Einstellung der Seitengröße identisch ist, sollte der Mini Treiber den Wert der <strong>WIA_IPS_PAGE_SIZE</strong> -Eigenschaft in WIA_PAGE_CUSTOM ändern. Der Mini Treiber sollte auch <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> oder <strong>WIA_IPS_PAGE_HEIGHT</strong> entsprechend der neuen Block Einstellung ändern.</p>
<p>Wenn <strong>WIA_IPS_ORIENTATION</strong> auf Landscape festgelegt ist, werden die Block Einstellungen relativ zu ihren üblichen Werten ausgetauscht. Wenn eine Anwendung z. b. <strong>WIA_IPS_PAGE_SIZE</strong> auf WIA_PAGE_A4 festlegt, legt der Mini Treiber <strong>WIA_IPS_PAGE_WIDTH</strong> auf 11692 und <strong>WIA_IPS_PAGE_HEIGHT</strong> auf 8267 fest. (Der Mini Treiber sollte auch <strong>WIA_IPS_XEXTENT</strong> anpassen und entsprechend <strong>WIA_IPS_YEXTENT</strong> .)</p>
<div class="alert">
<blockquote>
[!Note]<br />
Wenn <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> auf WIA_PAGE_CUSTOM festgelegt ist, wird die Ausrichtung nicht verwendet, um die Bereichs Dimensionen der zu scannenden Seite zu bestimmen.
</blockquote>
</div>
<div>
 
</div>
<p>Der Mini Treiber ist dafür verantwortlich, sicherzustellen, dass die <strong>WIA_IPS_ORIENTATION</strong> -Eigenschaft mit dem aktuellen Auswahlbereich übereinstimmt. Wenn eine Anwendung den Wert von <strong>WIA_IPS_ORIENTATION</strong> in einen Wert ändert, der für die aktuell ausgewählte Seitengröße ungültig ist, sollte der Mini Treiber den Wert <strong>WIA_IPS_PAGE_SIZE</strong> in eine Seitengröße ändern, die vom neuen Wert für die Ausrichtung unterstützt wird.</p>
<p>Wenn eine Anwendung die <strong>WIA_IPS_PAGE_SIZE</strong> -Eigenschaft auf WIA_PAGE_CUSTOM festlegt, ist der aktuelle Auswahlbereich nicht betroffen. Der WIA-Mini Treiber sollte das aktuelle Bild Layout abrufen, beginnend mit den aktuellen Einstellungen der Eigenschaften " <strong>WIA_IPS_XPOS</strong> " und " <strong>WIA_IPS_YPOS</strong> ". Wenn die Einstellung für die Seitengröße zu einem Auswahlbereich führt, der sich außerhalb des Scanners befindet, muss der Mini Treiber automatisch die Werte der Eigenschaften <strong>WIA_IPS_XPOS</strong> und <strong>WIA_IPS_YPOS</strong> an gültige Einstellungen anpassen. Wenn die Eigenschaften <strong>WIA_IPS_PAGE_SIZE</strong> und <strong>WIA_IPS_ORIENTATION</strong> gleichzeitig festgelegt sind und Sie in Kombination mit der Anwendung ungültig sind, sollte der Mini Treiber die Einstellungen der Anwendung nicht durch Zurückgeben eines Fehlers in <a href="https://msdn.microsoft.com/library/ms794145.aspx">iwiaminidrv::d rvvalidateitemproperties</a>ausführen.</p>
<p>In den folgenden vier Beispielen werden verschiedene <strong>WIA_IPS_PAGE_SIZE</strong> Szenarios gezeigt.</p>
<ol>
<li>Der Treiber meldet die Einstellungen.</li>
<li>In einer Anwendung wird die <strong>WIA_IPS_PAGE_SIZE</strong> -Eigenschaft auf WIA_PAGE_LETTER festgelegt.</li>
<li>In einer Anwendung wird die <strong>WIA_IPS_ORIENTATION</strong> -Eigenschaft auf Landscape festgelegt.</li>
<li>Die <strong>WIA_IPS_XEXTENT</strong> -Eigenschaft wird von einer Anwendung in einen kleineren Wert geändert.</li>
</ol>
<p><strong>Beispiel 1: der Mini Treiber meldet die Einstellungen.</strong></p>
<p>Im folgenden Beispiel legt der Mini Treiber einen benutzerdefinierten Auswahlbereich fest, bevor eine Anwendung WIA-Eigenschaften festlegt. In diesem Fall stellt der Auswahlbereich das gesamte Flatbed dar.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_WIDTH = 11500
WIA_IPS_PAGE_HEIGHT = 14000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1150
WIA_IPS_YEXTENT = 1400
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><strong>Beispiel 2: eine Anwendung legt die</strong> <strong>WIA_IPS_PAGE_SIZE</strong>-<strong>Eigenschaft auf fest WIA_PAGE_LETTER</strong>  </p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 850
WIA_IPS_YEXTENT = 1100
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><strong>Beispiel 3: eine Anwendung legt die</strong> <strong>WIA_IPS_ORIENTATION</strong>-<strong>Eigenschaft auf Landscape</strong> fest.  </p>
<p>Das physische Bett muss in der Lage sein, eine Seite abzurufen, die sich ursprünglich in Querformat orientiert.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1100
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><strong>Beispiel 4: eine Anwendung ändert die</strong> <strong>WIA_IPS_XEXTENT</strong> - <strong>Eigenschaft in einen kleineren Wert</strong></p>
<p>Im folgenden Beispiel ändert eine Anwendung die <strong>WIA_IPS_XEXTENT</strong> -Eigenschaft in 1000. Der Mini Treiber sollte davon ausgehen, dass der in <strong>WIA_IPS_XEXTENT</strong> enthaltene neue Wert für die Eigenschaft <strong>WIA_IPS_PAGE_SIZE</strong> nicht mehr gültig ist und daher <strong>WIA_IPS_PAGE_SIZE</strong> in WIA_PAGE_CUSTOM ändern sollte. Der Mini Treiber muss auch <strong>WIA_IPS_PAGE_WIDTH</strong>anpassen.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_HEIGHT = 10000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1000
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_HEIGHT"></span><span id="wia_ips_page_height"></span><dl> <dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>scannerpicturepageheight</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Höhe der aktuell ausgewählten Seite in Tausendstel Zoll. Der Mini Treiber erstellt und verwaltet die <strong>WIA_IPS_PAGE_HEIGHT</strong> -Eigenschaft. Eine Anwendung liest diese Eigenschaft, um die physischen Dimensionen der zu scannenden Seite zu bestimmen. Wenn sich die Block Einstellungen von den bekannten Seitengrößen unterscheiden, meldet diese Eigenschaft die Höhe der Seite, deren <strong>WIA_IPS_PAGE_SIZE</strong> -Eigenschaft auf WIA_PAGE_CUSTOM festgelegt ist (ein Wert der <strong>WIA_IPS_PAGE_SIZE</strong> -Eigenschaft). <strong>WIA_IPS_PAGE_HEIGHT</strong> müssen mit <strong>WIA_IPS_XEXTENT</strong>synchronisiert sein, das die Höhe der zu scannenden Seite in Pixel meldet.</p>
<p>Diese Eigenschaft ist für WIA_CATEGORY_FEEDER Elemente erforderlich.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PAGE_WIDTH"></span><span id="wia_ips_page_width"></span><dl> <dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>ScannerPicturePageWidth</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Breite der aktuell ausgewählten Seite in Tausendstel Zoll. Eine Anwendung liest diese Eigenschaft, um die physischen Dimensionen der zu scannenden Seite zu bestimmen. Wenn sich die Block Einstellungen von den bekannten Seitengrößen unterscheiden, meldet diese Eigenschaft die Breite der Seite, deren <strong>WIA_IPS_PAGE_SIZE</strong> -Eigenschaft auf WIA_PAGE_CUSTOM festgelegt ist. <strong>WIA_IPS_PAGE_WIDTH</strong> muss mit dem Wert von <strong>WIA_IPS_XEXTENT</strong>synchronisiert sein, der die Breite der zu scannenden Seite in Pixel meldet. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Diese Eigenschaft ist für WIA_CATEGORY_FEEDER Elemente erforderlich.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PAGES"></span><span id="wia_ips_pages"></span><dl> <dt><strong>WIA_IPS_PAGES</strong></dt> <dt>scannerpicturepages</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die aktuelle Anzahl der Seiten, die von einem automatischen Dokument-feedwert abgerufen werden sollen. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>; Zugriff: Lesen/Schreiben; Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> null bis zur maximalen Anzahl von Seiten, die der Scanner überprüfen kann. Der Wert ist all_pages (= 0), wenn der Scanner fortlaufend überprüfen kann.</p>
<p>Eine Anwendung liest diese Eigenschaft, um die Seiten Kapazität des Dokument Anlegers zu bestimmen. Diese Eigenschaft wird von der Anwendung auch auf die Anzahl der Seiten festgelegt, die gescannt werden.</p>
<div class="alert">
<blockquote>
[!Note]<br />
, Wenn der Duplex Modus aktiviert ist (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> ist auf "Fee" festgelegt | Duplex | ADVANCED_DUPLEX) ist <strong>WIA_IPS_PAGES</strong> weiterhin gleich der Anzahl der zu scanenden Seiten.
</blockquote>
</div>
<div>
 
</div>
<p>Ein Papierblatt enthält automatisch zwei Seiten, wenn Duplex aktiviert ist, auch wenn die Rückseite der Seite leer ist.</p>
<p>Das Festlegen von <strong>WIA_IPS_PAGES</strong> auf 1 bewirkt, dass ein Scanner eine Seite der Seite verarbeitet. Wenn ein Scanner nicht nur eine Seite einer Seite im Duplex Modus scannen kann, wird empfohlen, den <strong>WIA_IPS_PAGES</strong> Wert für das Inc-Element des Bereichs Elements der WIA_PROPERTY_INFO Struktur in 2 zu ändern. Dieser Wert signalisiert der Anwendung, dass Seiten in Vielfachen von zwei Anforderungen angefordert werden müssen. Der Wert ALL_PAGES (= 0) bedeutet, dass <em>alle</em> Seiten, die zurzeit in den Dokument-Feeden geladen werden, gescannt werden sollen.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PHOTOMETRIC_INTERP"></span><span id="wia_ips_photometric_interp"></span><dl> <dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>scannerpicturephotomezcinterp</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die aktuelle Einstellung für weiß und schwarze Pixel. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung liest diesen Wert, um den Wert weiß oder schwarz zu bestimmen (abhängig von der Funktionsweise der Anwendung).</p>
<p>Erforderlich für alle Erwerbs aktivierten oder gespeicherten Elemente; Das heißt, Elemente in den Kategorien: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE und WIA_CATEGORY_FILM. Die WIA_CATEGORY_FOLDER Elemente werden nicht unterstützt.</p>
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
<td>WIA_PHOTO_WHITE_0</td>
<td>Weiß ist 0 und schwarz ist 1.</td>
</tr>
<tr class="even">
<td>WIA_PHOTO_WHITE_1</td>
<td>Weiß ist 1, und schwarz ist 0.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW"></span><span id="wia_ips_preview"></span><dl> <dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>scannerpicturepreview</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt den Vorschaumodus für ein Gerät an. Eine Anwendung legt diese Eigenschaft fest, um das Gerät in einen Vorschaumodus zu versetzen.</p>
<p>Diese Eigenschaft ist für die WIA_CATEGORY_FLATBED-und WIA_CATEGORY_FILM Elemente erforderlich, die für das WIA_CATEGORY_FEEDER Element optional sind.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind. </p>
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_FINAL_SCAN</td>
<td>Die Anwendung führt eine abschließende Überprüfung aus.</td>
</tr>
<tr class="even">
<td>WIA_PREVIEW_SCAN</td>
<td>Die Anwendung führt eine Vorschau Überprüfung durch.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_PREVIEW_TYPE"></span><span id="wia_ips_preview_type"></span><dl> <dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>scannerpicturepreviewtype</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt an, ob das vorhandene Vorschaubild während einer Bildvorschau (als Reaktion auf eine Änderung in den Eigenschaften WIA_IPA_DATATYPE oder WIA_IPA_DEPTH aktualisiert werden kann).</p>
<p>Diese Eigenschaft ist für alle Erwerbs aktivierten Elemente, die Vorschau Scans unterstützen, optional. Das heißt, WIA_IPS_PREVIEW wird mit WIA_PREVIEW_SCAN unterstützt. Dies schließt Elemente vom Typ WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK und WIA_CATEGORY_FILM ein.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind. </p>
<table>
<thead>
<tr class="header">
<th>Konstante</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_ADVANCED_PREVIEW</td>
<td>Das vorhandene Image kann nicht aktualisiert werden.</td>
</tr>
<tr class="even">
<td>WIA_BASIC_PREVIEW</td>
<td>Eine andere Vorschau Überprüfung muss ausgeführt werden, da das vorhandene Image nicht aktualisiert werden kann.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_ROTATION"></span><span id="wia_ips_rotation"></span><dl> <dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>scannerpicturerotations</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die aktuelle Rotations Einstellung, wenn diese implementiert ist. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung legt diese Eigenschaft fest, um den Treiber darüber zu informieren, wie viel (wenn überhaupt) das Bild gedreht wird, bevor der Treiber es an die Anwendung zurückgibt.</p>
<div class="alert">
<blockquote>
[!Note]<br />
WIA_IPS_ORIENTATION bezieht sich auf die Position des Dokuments, das auf dem Scanner-oder-Feeder gescannt werden soll. Dabei handelt es sich um die Ausrichtung des Dokuments in Relation zur Richtung des Scans. WIA_IPS_ROTATION bezieht sich auf die Drehung, die auf das Bild angewendet wird, nachdem es gescannt wurde, kurz bevor das Bild an die Anwendung übertragen wird.
</blockquote>
</div>
<div>
 
</div>
<p>Der WIA-Mini Treiber ist für das Drehen der Bilddaten verantwortlich, bevor Sie an die Anwendung zurückgesendet werden. Die Anwendung ist dafür verantwortlich, die Bild Header zu überprüfen, um die neu gedrehten Werte anzuzeigen.</p>
<p>Eine beträchtliche Verwirrung besteht darin, die Auswirkung der Drehung auf den Auswahlbereich des aktuellen Bilds (der durch die Eigenschaften <strong>WIA_IPS_XPOS</strong>, <strong>WIA_IPS_YPOS</strong>, <strong>WIA_IPS_XEXTENT</strong> und <strong>WIA_IPS_YEXTENT</strong> definiert ist) aufzulösen.</p>
<p><em>Auswahlbereich</em> bezieht sich auf den ausgewählten Bereich im Bereich physischer Scanner, von dem ein Abbild abgerufen wird. <strong>WIA_IPS_ROTATION</strong> ändert den Auswahlbereich nicht. Der Treiber wendet die Drehung gegen den Uhrzeigersinn gemäß <strong>WIA_IPS_ROTATION</strong> erst an, nachdem der Treiber den entsprechenden Auswahlbereich abgerufen hat. <strong>WIA_IPS_ROTATION</strong> wirkt sich auf die Dimensionen des Ausgabe Bilds aus, sodass diese Dimensionen im Daten Header des resultierenden Bilds wiedergegeben werden müssen.</p>
<p>Optional für alle Erwerbs aktivierten Elemente; Das heißt, Elemente in den Kategorien: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK und WIA_CATEGORY_FILM.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgenden Rotations Konstanten sind definiert.</p>

<table>
<thead>
<tr class="header">
<th>Konstante</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hochformat</td>
<td>Der Treiber wird das Bild nicht drehen.</td>
</tr>
<tr class="even">
<td>Landschaf</td>
<td>Der Treiber dreht das Bild 90 Grad gegen den Uhrzeigersinn.</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>Der Treiber dreht das Bild 180 Grad gegen den Uhrzeigersinn.</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>Der Treiber dreht das Bild 270 Grad gegen den Uhrzeigersinn.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SEGMENTATION"></span><span id="wia_ips_segmentation"></span><dl> <dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>scannerpicturesegmentierung</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt an, ob die Anwendung den Segmentierungs Filter des Treibers für die Überprüfung in mehreren Regionen verwenden soll. WIA_IPS_SEGMENTATION müssen für WIA_CATEGORY_FLATBED-und WIA_CATEGORY_FILM Elemente implementiert werden, wenn Sie entweder das Erstellen von untergeordneten Elementen mit einem Segmentierungs Filter unterstützen, oder wenn der Treiber selbst untergeordnete Elemente für fixierte Frames erstellt.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
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
<td>WIA_USE_SEGMENTATION_FILTER</td>
<td>Die Anwendung sollte den Segmentierungs Filter für das Scannen in mehreren Regionen verwenden.</td>
</tr>
<tr class="even">
<td>WIA_DONT_USE_SEGMENTATION_FILTER</td>
<td>Der Treiber erstellt die untergeordneten Elemente selbst für das Scannen in mehreren Regionen. Dies ist normalerweise der Fall, wenn der Scanner zu diesem Zweck fixierte Frames verwendet.</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
Es ist möglich, dass ein Treiber mit einem Segmentierungs Filter ausgestattet ist, aber WIA_IPS_SEGMENTATION für eines seiner Elemente WIA_DONT_USE_SEGMENTATION_FILTER festgelegt ist (z. b. das WIA_CATEGORY_FILM Element). Dies kann der Fall sein, wenn die Überprüfung fixierte Frames für die Film Überprüfung verwendet, nicht aber für reguläre Scans aus WIA_CATEGORY_FLATBED Elementen.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_ips_sheet_feeder_registration"></span><dl> <dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>scannerpicturesheetfeederregistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Registrierung bzw. die Ausrichtung und Kantenerkennung für Dokumente, die im Flatbed abgelegt werden. Der Mini Treiber erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft gibt an, wie das Blatt horizontal auf der Scan Kopfzeile eines Hand Buch-oder Sheet-Scans positioniert ist. Die-Eigenschaft wird verwendet, um vorherzusagen, wo ein Dokument über die Scan Kopfzeile platziert wird.</p>
<p>Für Scanner, die mehr als einen scanhead unterstützen, ist diese Eigenschaft relativ zum obersten scanhead. Diese Eigenschaft ist für Blatt-, Scroll-und Hand Buchscanner obligatorisch.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Konstante</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LEFT_JUSTIFIED</td>
<td>Das Blatt wird in Bezug auf die scannerkopfzeile links positioniert.</td>
</tr>
<tr class="even">
<td>Ego</td>
<td>Das Blatt ist auf die scannerkopfzeile zentriert.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>Das Blatt wird in Bezug auf den Scan Kopf rechts positioniert.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_ips_show_preview_control"></span><dl> <dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>scannerpictureshowpreviewcontrol</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt an, ob ein Element ein Vorschau Steuerelement benötigt, das für den Benutzer angezeigt wird. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Optional für alle übertragungaktivierten Elemente. Dies sind in der Regel nur Elemente der Kategorien WIA_ITEM_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM und WIA_CATEGORY_FINISHED_FILE.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind. </p>
<table>
<thead>
<tr class="header">
<th>Konstante</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_SHOW_PREVIEW_CONTROL</td>
<td>Zeigen Sie dem Benutzer ein Vorschau Steuerelement an, da auf diesem Gerät eine Vorschauversion durchgeführt werden kann.</td>
</tr>
<tr class="even">
<td>WIA_DONT_SHOW_PREVIEW_CONTROL</td>
<td>Zeigen Sie dem Benutzer kein Vorschau Steuerelement an, da auf diesem Gerät keine Vorschauversion durchgeführt werden kann.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION"></span><span id="wia_ips_supports_child_item_creation"></span><dl> <dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>scannerpicturesupportschilditemcreation</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt an, ob die Anwendung (oder die Filter) untergeordnete Elemente unter dem aktuellen Element erstellen kann.</p>
<p>Optional für alle Element Kategorien, die für die Übertragung aktiviert sind: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM und sogar WIA_CATEGORY_FOLDER. (Wenn der Speicher das Hochladen neuer Elemente nicht unterstützt, sollte diese Eigenschaft entweder nicht unterstützt werden oder mit dem Wert <strong>false</strong> unterstützt werden.)</p>
<p>Elemente, die WIA_IPS_SEGMENTATION und WIA_USE_SEGMENTATION_FILTER unterstützen, müssen auch WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION unterstützen und auf " <strong>true</strong>" festgelegt sein.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <strong>true</strong> und <strong>false</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_THRESHOLD"></span><span id="wia_ips_threshold"></span><dl> <dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>scannerpicturethreshold</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt den Graustufenwert an, der bestimmt, ob ein Pixel in weiß oder schwarz konvertiert wird, wenn ein Bild in monochrome konvertiert wird. Pixel oberhalb des Schwellenwerts werden weiß. Pixel unterhalb des Schwellenwerts werden weiß.</p>
<p>Diese Eigenschaft ist für Erwerbs Elemente erforderlich, die 1-bpp-Scans unterstützen und deren WIA_IPA_DATATYPE-Eigenschaft auf WIA_DATA_THRESHOLD festgelegt ist.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_TRANSFER_CAPABILITIES"></span><span id="wia_ips_transfer_capabilities"></span><dl> <dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>scannerpicturetransfer-Funktionen</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt an, ob der Treiber mehrere untergeordnete Elemente in einem einzelnen Übertragungs Befehl übertragen kann.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>Der einzig mögliche Wert für diese Eigenschaft ist WIA_TRANSFER_CHILDREN_SINGLE_SCAN. Wenn dieses Flag festgelegt ist, kann der Treiber mehrere untergeordnete Elemente in einem einzelnen Übertragungs Aufrufer übertragen. Wenn das Flag nicht festgelegt ist, durchläuft der WIA-Dienst die untergeordneten Elemente rekursiv und überträgt dann jedes dieser Elemente.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>scannerpictureinvert</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt die Anzahl der Bytes an, die für das Element hochgeladen werden sollen.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_WARM_UP_TIME"></span><span id="wia_ips_warm_up_time"></span><dl> <dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>scannerpicturewarmuptime</dt> </dl></td>
<td style="text-align: left;"><p>Gibt die maximale Aufwärm Dauer (in Millisekunden) an, die das Gerät benötigt, bevor der Scanvorgang gestartet wird. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung kann diese Eigenschaft lesen, um die maximale Aufwärm Dauer für dieses Gerät zu bestimmen. Anschließend kann &quot; das Dialogfeld warten, bis das Gerät bereinigt &quot; wird, damit der Benutzer weiß, dass ein warte Vorgang oder eine Pause auftreten kann, bevor etwas passiert.</p>
<p>Diese Eigenschaft ist für alle Erwerbs aktivierten Elemente erforderlich. Das heißt, Elemente in den Kategorien: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK und WIA_CATEGORY_FILM.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XEXTENT"></span><span id="wia_ips_xextent"></span><dl> <dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>scannerpicturexblock</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die aktuelle Breite des ausgewählten abzurufenden Bilds in Pixel. Eine Anwendung legt diese Eigenschaft fest, um die Breite eines Auswahl Bereichs zu markieren, der abgerufen werden soll. Diese Eigenschaft muss mit der <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> -Eigenschaft übereinstimmen. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Erforderlich für alle Erwerbs aktivierten Elemente; Das heißt, Elemente in den Kategorien: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK und WIA_CATEGORY_FILM.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XPOS"></span><span id="wia_ips_xpos"></span><dl> <dt><strong>WIA_IPS_XPOS</strong></dt> <dt>scannerpicturexpos</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die x-Koordinate der oberen linken Ecke des ausgewählten Bilds in Pixel. Eine Anwendung legt diese Eigenschaft fest, um die linke obere Ecke des Auswahl Bereichs zu markieren. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Erforderlich für alle Erwerbs aktivierten Elemente; Das heißt, Elemente in den Kategorien: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE und WIA_CATEGORY_FILM. Die WIA_CATEGORY_FOLDER Elemente werden nicht unterstützt.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_XRES"></span><span id="wia_ips_xres"></span><dl> <dt><strong>WIA_IPS_XRES</strong></dt> <dt>scannerpicturexres</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die aktuelle horizontale Auflösung (in Pixel pro Zoll) für das Gerät. Eine Anwendung legt diese Eigenschaft fest, um die horizontale Auflösung festzulegen. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Wenn das Gerät nur auf einen einzelnen Wert festgelegt werden kann, erstellen Sie einen <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> Typ, und platzieren Sie den gültigen Wert darin. Dies ist auch dann der Fall, wenn eine Auflösungseinstellung von einer anderen Auflösung abhängig ist. (Die vertikale Auflösung kann von der horizontalen Auflösung abhängen.)</p>
<p>Erforderlich für alle Erwerbs aktivierten Elemente; Das heißt, Elemente in den Kategorien: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE und WIA_CATEGORY_FILM. Die WIA_CATEGORY_FOLDER Elemente werden nicht unterstützt.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff oder schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> oder WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_XSCALING"></span><span id="wia_ips_xscaling"></span><dl> <dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>scannerpicturexscaling</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Legt die horizontale Skalierung als Prozentsatz fest, die auf gescannte Abbilder innerhalb des scannergeräts oder seines Treibers angewendet werden kann.</p>
<p>Diese Eigenschaft ist für alle Erwerbs aktivierten Elemente optional. Das heißt, Elemente vom Typ WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK und WIA_CATEGORY_FILM.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff oder schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE.</p>
<p>Die Werte können zwischen 1 und der maximalen VT_I4 (0xFFFF) liegen. 100 bedeutet beispielsweise keine Skalierung, 050 bedeutet, dass eine Skalierung auf 50% der ursprünglicher-Größe durchführt, und 200 bedeutet, dass eine Skalierung von bis zu 200% der ursprünglichen Größe durchführt.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YEXTENT"></span><span id="wia_ips_yextent"></span><dl> <dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>scannerpictureyblock</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die aktuelle Höhe des ausgewählten abzurufenden Bilds in Pixel. Eine Anwendung legt diese Eigenschaft fest, um die Höhe eines Auswahl Bereichs zu markieren. Diese Eigenschaft muss mit dem Wert der <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> -Eigenschaft übereinstimmen. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Erforderlich für alle Erwerbs aktivierten Elemente; Das heißt, Elemente in den Kategorien: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK und WIA_CATEGORY_FILM.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YPOS"></span><span id="wia_ips_ypos"></span><dl> <dt><strong>WIA_IPS_YPOS</strong></dt> <dt>scannerpictureypos</dt> </dl></td>
<td style="text-align: left;"><p>Aktuelle y-Koordinate der oberen linken Ecke des ausgewählten Bilds in Pixel. Eine Anwendung legt diese Eigenschaft fest, um die linke obere Ecke des Auswahl Bereichs zu markieren. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Erforderlich für alle Erwerbs aktivierten Elemente; Das heißt, Elemente in den Kategorien: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE und WIA_CATEGORY_FILM. Die WIA_CATEGORY_FOLDER Elemente werden nicht unterstützt.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPS_YRES"></span><span id="wia_ips_yres"></span><dl> <dt><strong>WIA_IPS_YRES</strong></dt> <dt>scannerpictureyres</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die aktuelle vertikale Auflösung (in Pixel pro Zoll) für das Gerät. Diese Eigenschaft wird von einer Anwendung festgelegt, um die vertikale Auflösung festzulegen. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Wenn das Gerät nur auf einen einzelnen Wert festgelegt werden kann, erstellen Sie einen <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> Typ, und platzieren Sie den gültigen Wert darin. Dies ist auch dann der Fall, wenn eine Auflösungseinstellung von einer anderen Auflösung abhängig ist. (Die horizontale Auflösung kann von der vertikalen Auflösung abhängen.)</p>
<p>Erforderlich für alle Erwerbs aktivierten Elemente; Das heißt, Elemente in den Kategorien: WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE und WIA_CATEGORY_FILM. Die WIA_CATEGORY_FOLDER Elemente werden nicht unterstützt.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff oder schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> oder WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPS_YSCALING"></span><span id="wia_ips_yscaling"></span><dl> <dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>scannerpictureyscaling</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Legt die vertikale Skalierung als Prozentsatz fest, die auf gescannte Abbilder innerhalb des scannergeräts oder seines Treibers angewendet werden kann.</p>
<p>Diese Eigenschaft ist für alle Erwerbs aktivierten Elemente optional. Das heißt, Elemente vom Typ WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK und WIA_CATEGORY_FILM.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff oder schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE.</p>
<p>Die Werte können zwischen 1 und der maximalen VT_I4 (0xFFFF) liegen. 100 bedeutet beispielsweise keine Skalierung, 050 bedeutet, dass eine Skalierung auf 50% der ursprünglicher-Größe durchführt, und 200 bedeutet, dass eine Skalierung von bis zu 200% der ursprünglichen Größe durchführt.</p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




