---
description: Windows WIA-Hardwaregeräte (Image Acquisition) verfügen über Eigenschaftswerte, die in der registrierung Windows werden.
ms.assetid: 78caa3af-927b-4143-9e88-4b5c918d00a4
title: Scanner-Geräteeigenschaftskonst constants (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPS_DEVICE_ID
- WIA_DPS_DITHER_PATTERN_DATA
- WIA_DPS_DITHER_SELECT
- WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES
- WIA_DPS_DOCUMENT_HANDLING_SELECT
- WIA_DPS_DOCUMENT_HANDLING_STATUS
- WIA_DPS_ENDORSER_CHARACTERS
- WIA_DPS_ENDORSER_STRING
- WIA_DPS_FILTER_SELECT
- WIA_DPS_GLOBAL_IDENTITY
- WIA_DPS_HORIZONTAL_BED_REGISTRATION
- WIA_DPS_HORIZONTAL_BED_SIZE
- WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MAX_SCAN_TIME
- WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE
- WIA_DPS_OPTICAL_XRES
- WIA_DPS_OPTICAL_YRES
- WIA_DPS_ORIENTATION
- WIA_DPS_PAD_COLOR
- WIA_DPS_PAGE_HEIGHT
- WIA_DPS_PAGE_SIZE
- WIA_DPS_PAGE_WIDTH
- WIA_DPS_PAGES
- WIA_DPS_PLATEN_COLOR
- WIA_DPS_PREVIEW
- WIA_DPS_SCAN_AHEAD_PAGES
- WIA_DPS_SCAN_AVAILABLE_ITEM
- WIA_DPS_SERVICE_ID
- WIA_DPS_SHEET_FEEDER_REGISTRATION
- WIA_DPS_SHOW_PREVIEW_CONTROL
- WIA_DPS_USER_NAME
- WIA_DPS_VERTICAL_BED_REGISTRATION
- WIA_DPS_VERTICAL_BED_SIZE
- WIA_DPS_VERTICAL_SHEET_FEED_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: d9e7afee9b5b639c21e52dc797e7ad42a6ee0dd0
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627186"
---
# <a name="scanner-device-property-constants"></a>Eigenschaftenkonst constants des Scannergeräts

Windows WIA-Hardwaregeräte (Image Acquisition) verfügen über Eigenschaftswerte, die in der registrierung Windows werden. Weitere Informationen finden Sie unter [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md). Die folgenden Geräteeigenschaftskonst constants mit den zugehörigen Zeichenfolgen sind spezifisch für digitale Bildscanner.

Das Präfix "WIA DPS" gibt eine Geräteeigenschaft für Scannergeräte an und ist die \_ \_ in C/C++ verwendete Namenskonvention. Zu Skriptzwecken verwenden diese Konstanten das Präfix "ScannerDevice" und sind Teil des [aufzählten WiaItemPropertyId-Typs.](-wia-wiaitempropertyid.md) Der entsprechende Membername aus dieser Skriptenumeration wird in Klammern neben dem C/C++-Konstantennamen in der folgenden Liste angezeigt.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Konstante/Wert</th>
<th >Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </dl></td>
<td ><blockquote>
[!Note]<br />
Diese Eigenschaft wird nur auf Windows Vista und höher unterstützt.
</blockquote>
<br/> Enthält einen eindeutigen Funktionsinstanzbezeichner für ein Webdienstscannergerät. Dieser Bezeichner stellt den Webdienst auf dem Scannergerät dar, mit dem der WIA-Minitreiber kommuniziert. Es sollten keine Annahmen über die Form dieses Bezeichners getroffen werden. Der WIA-Minitreiber erstellt und verwaltet diese Eigenschaft. <br/> WIA-Anwendungen können den Wert von WIA_DPS_DEVICE_ID verwenden, um mithilfe der Funktionsermittlungs-API das Funktionsinstanzobjekt zu finden, das das in der aktuellen WIA 2.0-Sitzung verwendete Webdienstscannergerät darstellt.<br/> Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </dl></td>
<td >Reserviert, nicht verwenden.<br/> Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </dl></td>
<td >Reserviert, nicht verwenden.<br/> Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </dl></td>
<td >Enthält die Funktionen der Scanner. Der Minitreiber erstellt und verwaltet diese Eigenschaft. <br/> Eine Anwendung liest diese Eigenschaft, um zu bestimmen, ob für die Scanner ein Flatbed, ein Dokumentfeed oder ein Duplexer installiert ist. Diese Eigenschaft wird auch verwendet, um die installierten Features weiter zu definieren.<br/> Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> In der folgenden Tabelle werden die Konstanten beschrieben, die nur mit Windows 7 gültig sind.<br/> 
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AUTO_SOURCE</td>
<td>Der Scanner verfügt über einen automatischen Dokumenthandler.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>In der folgenden Tabelle werden die Konstanten beschrieben, die nur mit Windows 7 und Windows Vista gültig sind.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ADVANCED_DUP</td>
<td>Das Gerät unterstützt die erweiterte Duplexscankonfiguration. Verwenden WIA_IPS_DUPLEX_SETTINGS, um zwischen der Verwendung von grundlegenden und erweiterten Duplexkonfigurationen zu wechseln.</td>
</tr>
<tr class="even">
<td>DETECT_FILM_TPA</td>
<td>Der Scanner kann erkennen, wann der Transparenz-/Filmadapter für die Überprüfung bereit ist.</td>
</tr>
<tr class="odd">
<td>DETECT_STOR</td>
<td>Der Scanner kann erkennen, wenn sich Dokumente im internen Speicher befinden.</td>
</tr>
<tr class="even">
<td>FILM_TPA</td>
<td>Der Scanner ist mit einem Transparenz-/Filmscanadapter ausgestattet.</td>
</tr>
<tr class="odd">
<td>STOR</td>
<td>Der Scanner ist mit einem internen Imagespeichergerät ausgestattet.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>In der folgenden Tabelle werden die Konstanten beschrieben, die mit Windows XP oder höher gültig sind.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DETECT_FEED</td>
<td>Der Scanner kann ein Dokument im Feeder erkennen.</td>
</tr>
<tr class="even">
<td>DETECT_FLAT</td>
<td>Der Scanner kann ein Dokument auf dem Flachbildschirm erkennen.</td>
</tr>
<tr class="odd">
<td>DETECT_SCAN</td>
<td>Der Scanner kann ein Dokument im Feeder nur durch Scannen erkennen.</td>
</tr>
<tr class="even">
<td>DUP</td>
<td>Der Scanner verfügt über einen Duplexer.</td>
</tr>
<tr class="odd">
<td>FEED</td>
<td>Der Scanner verfügt über einen automatischen Dokumenthandler.</td>
</tr>
<tr class="even">
<td>FLACH</td>
<td>Der Scanner verfügt über einen Flatbed-Schild.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>In der folgenden Tabelle werden die Konstanten beschrieben, die nur bei Windows XP gültig sind. Diese Werte sind für die Versionen Windows 7 und Windows Vista veraltet und sollten nicht verwendet werden.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DETECT_DUP</td>
<td>Der Scanner kann eine Duplexscananforderung vom Benutzer erkennen.</td>
</tr>
<tr class="even">
<td>DETECT_DUP_AVAIL</td>
<td>Der Scanner kann erkennen, wann der Duplexer installiert ist.</td>
</tr>
<tr class="odd">
<td>DETECT_FEED_AVAIL</td>
<td>Der Scanner kann erkennen, wann der automatische Dokumentfeeder installiert ist.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird in Windows Vista und höher nicht unterstützt. Verwenden <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die aktuelle Quelle und den aktuellen Modus für den Scannererwerb. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung liest diese Eigenschaft, um die aktuelle Erfassungsquelle des Scanners zu bestimmen oder diese Eigenschaft zu schreiben, um die Quelle und den Modus der Scanner festzulegen. Darüber hinaus verwenden Anwendungen diese Eigenschaft, um duplexer-Funktionen zu aktivieren und zu deaktivieren.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>Die folgende Tabelle enthält die zehn Konstanten, die mit dieser Eigenschaft gültig sind. </p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FEEDER</td>
<td>Überprüfen Sie mithilfe des Dokumentfeeders.</td>
</tr>
<tr class="even">
<td>FLACHBETT</td>
<td>Überprüfen Sie mithilfe des Flatbeds.</td>
</tr>
<tr class="odd">
<td>DUPLEX</td>
<td>Überprüfung mit Duplexervorgängen.</td>
</tr>
<tr class="even">
<td>AUTO_ADVANCE</td>
<td>Aktiviert die automatische Einführung des nächsten Dokuments nach einer Überprüfung.</td>
</tr>
<tr class="odd">
<td>FRONT_FIRST</td>
<td>Überprüfen Sie zuerst den Anfang des Dokuments. Dieser Wert ist gültig, wenn DUPLEX festgelegt ist.</td>
</tr>
<tr class="even">
<td>BACK_FIRST</td>
<td>Überprüfen Sie zuerst die Rückseite des Dokuments. Dieser Wert ist gültig, wenn DUPLEX festgelegt ist.</td>
</tr>
<tr class="odd">
<td>FRONT_ONLY</td>
<td>Überprüfen Sie nur die Front. Dieser Wert ist gültig, wenn DUPLEX festgelegt ist.</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>Überprüfen Sie nur die Rückseite. Dieser Wert ist gültig, wenn DUPLEX festgelegt ist.</td>
</tr>
<tr class="odd">
<td>NEXT_PAGE</td>
<td>Überprüfen Sie die nächste Seite des Dokuments.</td>
</tr>
<tr class="even">
<td>VORABFEED</td>
<td>Aktivieren Sie den Vorfeedmodus. Vorabpositionieren des nächsten Dokuments während des Scannens.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </dl></td>
<td ><p>Enthält den aktuellen Zustand des installierten Flatbeds, des Dokumentfeeds oder des Duplexers des Scanners. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung liest diese Eigenschaft, um zu bestimmen, ob das Scannergerät einsatzbereit ist. Dies ist eine ideale Möglichkeit, um vor dem Abrufen eines Bilds zu überprüfen, ob papier sich im Feeder befindet.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind. Ein Sternchen * gibt an, dass das Flag in Windows Vista oder höher nicht unterstützt wird. Das <strong>Symbol V</strong> gibt an, dass das Flag nur in Windows Vista und höher unterstützt wird. </p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FEED_READY</td>
<td>Das Flatbed ist einsatzbereit.</td>
</tr>
<tr class="even">
<td>FLAT_READY</td>
<td>Der Scanner verfügt über ein Dokument auf dem Flatbed-Kennzeichen.</td>
</tr>
<tr class="odd">
<td>DUP_READY</td>
<td>Der Duplexer ist aktiviert und einsatzbereit.</td>
</tr>
<tr class="even">
<td>FLAT_COVER_UP</td>
<td>Die flache Beetabdeckung ist hoch.</td>
</tr>
<tr class="odd">
<td>PATH_COVER_UP</td>
<td>Der Papierpfad ist verdeckt und verhindert den ordnungsgemäßen Betrieb.</td>
</tr>
<tr class="even">
<td>PAPER_JAM</td>
<td>Ein Dokument wird im Dokumentfeeder blockiert.</td>
</tr>
<tr class="odd">
<td>FILM_TPA_READY<strong>V</strong></td>
<td>Der Transparenzadapter ist installiert und einsatzbereit.</td>
</tr>
<tr class="even">
<td>STORAGE_READY<strong>V</strong></td>
<td>Das interne Speichergerät ist bereit.</td>
</tr>
<tr class="odd">
<td>STORAGE_FULL<strong>V</strong></td>
<td>Der Speicher ist voll, keine Uploadvorgänge möglich.</td>
</tr>
<tr class="even">
<td>MULTIPLE_FEED<strong>V</strong></td>
<td>Es ist eine Bedingung für mehrere Feeds aufgetreten (in der Regel mit einem PAPER_JAM).</td>
</tr>
<tr class="odd">
<td>DEVICE_ATTENTION<strong>V</strong></td>
<td>Es gibt einen Fehler, der einen Benutzereingriff auf dem Gerät erfordert.</td>
</tr>
<tr class="even">
<td>LAMP_ERR<strong>V</strong></td>
<td>Der Scanner ist aufgrund eines Lampeproblems nicht bereit.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </dl></td>
<td ><p>Enthält alle gültigen Zeichen, die eine Anwendung zum Erstellen gültiger Unterstützungszeichenfolgen verwenden kann. Ein Unterstützter ist ein Drucker, der auf einem Scanner installiert ist, der eine Textnachricht auf jeder gescannten Seite ausdrückt. Der Minitreiber sollte die Einstellung der <strong>WIA_DPS_ENDORSER_STRING</strong> Eigenschaft anhand des gültigen Zeichensatzes in dieser Eigenschaft überprüfen. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </dl></td>
<td ><p>Enthält eine Zeichenfolge, die auf jeder Seite, die vom Minitreiber überprüft wird, unterstützt (d. h. gedruckt) werden soll. Eine Anwendung legt diese Eigenschaft mithilfe des gültigen Zeichensatzes fest, der in der <strong>eigenschaft WIA_DPS_ENDORSER_CHARACTERS</strong> gemeldet wird. Der Minitreiber sollte Dokumente nur unterstützen, wenn in dieser Eigenschaft eine Zeichenfolge festgelegt ist. Eine leere Zeichenfolge bedeutet, dass die Unterstützungsfunktion deaktiviert ist.</p>
<p>Da es aufgabe des Treibers ist, die Empfehlungszeichenfolge zu interpretieren, kann Ihr Treiber Sonderzeichen in <strong>WIA_DPS_ENDORSER_STRING</strong>verwenden. Allerdings würden nur Ihre Anwendungen diese Zeichen verstehen.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Ein Treiber, der die <strong>WIA_DPS_ENDORSER_STRING</strong> -Eigenschaft unterstützt, muss die folgende Liste von Token unterstützen. </p>
<table>
<thead>
<tr class="header">
<th>Token</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>$DATE$</td>
<td>Das Datum im Format YYYY/MM/DD.</td>
</tr>
<tr class="even">
<td>$DAY$</td>
<td>Der Tag im Format DD.</td>
</tr>
<tr class="odd">
<td>$MONTH$</td>
<td>Der Monat des Jahres im Format MM.</td>
</tr>
<tr class="even">
<td>$PAGE_COUNT$</td>
<td>Die Anzahl der übertragenen Seiten.</td>
</tr>
<tr class="odd">
<td>$TIME$</td>
<td>Die Tageszeit im Format HH:MM:SS.</td>
</tr>
<tr class="even">
<td>$YEAR$</td>
<td>Das Jahr im Format YYYY.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </dl></td>
<td ><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur für Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die SOAP-Adresse eines Webdienstscannergeräts. Der WIA 2.0-Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird mit Windows Vista und höher nicht unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Registrierung oder horizontale Ausrichtung für Dokumente, die auf dem Flatbed platziert sind. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Konstante</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LEFT_JUSTIFIED</td>
<td>Das Papier bleibt berechtigt.</td>
</tr>
<tr class="even">
<td>ZENTRIERT</td>
<td>Das Papier ist zentriert.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>Das Papier ist richtig ausgerichtet.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Siehe auch</strong></p>
<p><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird mit Windows Vista und höher nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt die maximale Breite in Tausendstel zoll an, die auf der horizontalen (X)-Achse aus dem Belag eines Flatbedscanners bei der aktuellen Auflösung gescannt wird. Diese Eigenschaft gilt auch für automatische Dokumentfeeder, die Blätter zum Scannen auf die Vorzeichen eines Flatbedscanners verschieben. Diese Eigenschaft ist für Scanner mit einem Kennzeichen obligatorisch. Andere Scannertypen implementieren <strong></strong> stattdessen die WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE-Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird mit Windows Vista und höher nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt die maximale Breite in Tausendstel zoll an, die auf der horizontalen Achse (X) von einem Scanner mit einem Linien- oder Blattfeed mit der aktuellen Auflösung gescannt wird. Diese Eigenschaft gilt auch für automatische Dokumentfeeder, die ohne Verschieben von Blättern auf die Beschilderung eines Flatbedscanners scannen. Diese Eigenschaft ist für Scanner mit Blättern, Scrollen und handgehaltenen Scannern obligatorisch.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </dl></td>
<td ><p>Enthält die maximale Zeit zum Überprüfen einer einzelnen Seite mit den aktuellen Eigenschafteneinstellungen in Millisekunden. Eine Anwendung liest diese Eigenschaft, um die Zeit einzuschätzen, die zum Überprüfen einer Seite dauert. Dies ist hilfreich, wenn Sie die Bedingungen eines Geräts bestimmen, das nicht mehr reagiert. Der Minitreiber erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft ist für alle Scanner erforderlich.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird mit Windows Vista und höher nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die physischen horizontalen Dimensionen der kleinsten Seite, die der Dokumentfeeder des Scanners scannen kann (in Tausendstel Zoll). Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Siehe auch</strong></p>
<p><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird mit Windows Vista und höher nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die physischen vertikalen Abmessungen der kleinsten Seite, die der Dokumentfeeder des Scanners scannen kann (in Tausendstel Zoll). Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Siehe auch</strong></p>
<p><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Horizontale optische Auflösung. Höchste unterstützte horizontale optische Auflösung in DPI. Diese Eigenschaft ist ein einzelner Wert. Dies ist nicht eine Liste aller Auflösungen, die vom Gerät generiert werden können. Stattdessen ist dies die Auflösung des Geräts. Der Minitreiber erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft ist für alle Scanner erforderlich.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Vertikale optische Auflösung. Höchste unterstützte vertikale optische Auflösung in DPI. Diese Eigenschaft ist ein einzelner Wert. Dies ist nicht eine Liste aller Auflösungen, die vom Gerät generiert werden. Stattdessen ist dies die Auflösung des Geräts. Der Minitreiber erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft ist für alle Scanner erforderlich.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </dl></td>
<td ><p>Enthält die aktuelle Ausrichtungseinstellung. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung legt die <strong>WIA_DPS_ORIENTATION</strong> -Eigenschaft fest, um die ursprüngliche Ausrichtung einer Seite oder eines Bilds zu definieren, die bzw. das erworben werden soll. Informationen zur Verwendung von WIA_DPS_ORIENTATION finden Sie unter <strong>WIA_DPS_PAGE_SIZE</strong></p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die vier Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Defination</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LANDSCHAFT</td>
<td>Drehung um 90 Grad gegen den Uhrzeigersinn relativ zur PORTRAIT-Ausrichtung.</td>
</tr>
<tr class="even">
<td>PORTRÄT</td>
<td>0 Grad.</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>Drehung um 180 Grad gegen den Uhrzeigersinn relativ zur PORTRAIT-Ausrichtung.</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>Drehung um 270 Grad gegen den Uhrzeigersinn relativ zur PORTRAIT-Ausrichtung.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Siehe auch</strong></p>
<p><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </dl></td>
<td ><p>Farbe, die zum Auffüllen verwendet wird, wenn nicht genügend Bilddaten vorhanden sind, um einen angeforderten Puffer zu füllen. Diese Eigenschaft wird für Scanner implementiert, die den Puffer aufgefüllt haben. Diese Eigenschaft ist für alle Scanner optional. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Zugriff: Schreibgeschützter Zugriff, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Das Format der Farbinformationen ist <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD.</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Höhe der aktuell ausgewählten Seite in Tausendstel Zoll. Der Minitreiber erstellt und <strong></strong> verwaltet die WIA_DPS_PAGE_HEIGHT-Eigenschaft. Eine Anwendung liest diese Eigenschaft, um die physischen Dimensionen der zu überprüfenden Seite zu bestimmen. Wenn sich die Erweiterungseinstellungen von den bekannten Seitengrößen unterscheiden, meldet diese Eigenschaft die Höhe der Seite, deren <strong>WIA_DPS_PAGE_SIZE</strong> -Eigenschaft auf WIA_PAGE_CUSTOM festgelegt ist (ein Wert der <strong>WIA_DPS_PAGE_SIZE-Eigenschaft).</strong> <strong>WIA_DPS_PAGE_HEIGHT</strong> müssen mit <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>synchron sein, der die Höhe der zu scannenden Seite in Pixel meldet.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Größe der Seite, die derzeit überprüft werden soll. Um die Dimensionen der zu überprüfende Seite auszuwählen, legt eine Anwendung diese Eigenschaft fest. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind. </p>
<table>
<thead>
<tr class="header">
<th>Wert</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PAGE_A4</td>
<td>8267 x 11692 (HOCHFORMATausrichtung)</td>
</tr>
<tr class="even">
<td>WIA_PAGE_CUSTOM</td>
<td>Definiert durch die Werte der <strong>eigenschaften WIA_DPS_PAGE_HEIGHT</strong> und <strong>WIA_DPS_PAGE_WIDTH</strong></td>
</tr>
<tr class="odd">
<td>WIA_PAGE_LETTER</td>
<td>8500 x 11000 (HOCHFORMATausrichtung)</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Der Wert der <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION-Eigenschaft</strong></a> bestimmt die Ausrichtung der aktuell ausgewählten Seite. Die <strong>eigenschaften WIA_DPS_PAGE_WIDTH</strong> und <strong>WIA_DPS_PAGE_HEIGHT</strong> melden die Dimensionen der Seite in Tausendstel Zoll. Beachten Sie, dass diese Eigenschaften mit <strong>WIA_IPS_XEXTENT</strong> und <strong>WIA_IPS_YEXTENT</strong>übereinstimmen müssen, die die Abmessungen der Seite in Pixel enthalten. Gültige Werte vom Typ WIA_PROP_LIST sollten von gültigen Einstellungen der <strong>WIA_IPS_ORIENTATION-Eigenschaft</strong> abhängen. Wenn das Gerät keine querformatorientierten Dokumente mit einer WIA_PAGE_A4-Einstellung scannen kann, sollten WIA_PAGE_A4 nicht in der Liste der gültigen Werte für die <strong>WIA_DPS_PAGE_SIZE</strong> -Eigenschaft angezeigt werden, wenn <strong>WIA_IPS_ORIENTATION</strong> auf LANSCAPE festgelegt ist.</p>
<p>Wenn eine Anwendung <strong>WIA_DPS_PAGE_SIZE</strong> auf einen anderen Wert als WIA_PAGE_CUSTOM festlegt, sollte der Minitreiber die Werte von <strong>WIA_DPS_PAGE_WIDTH</strong> anpassen und <strong>WIA_DPS_PAGE_HEIGHT</strong> in Tausendstel Zoll an die Seitendimensionen anpassen. Außerdem sollten die Werte von <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> und <strong>WIA_IPS_YEXTENT</strong> an die Abmessungen der Seite in Pixel angepasst werden.</p>
<p>Wenn eine Erweiterungseinstellung (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> oder <strong>WIA_IPS_YEXTENT</strong>) in einen Wert geändert wird, der nicht mit der aktuellen Einstellung für die Seitengröße übereinstimmt, sollte der Minitreiber den Wert der <strong>eigenschaft WIA_DPS_PAGE_SIZE</strong> in WIA_PAGE_CUSTOM ändern. Der Minitreiber sollte auch <strong>WIA_DPS_PAGE_WIDTH</strong> oder <strong>WIA_DPS_PAGE_HEIGHT</strong> entsprechend der neuen Erweiterungseinstellung ändern.</p>
<p>Wenn <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> auf LANSCAPE festgelegt ist, werden die Erweiterungseinstellungen &quot; gekippt. &quot; Wenn eine Anwendung beispielsweise <strong>WIA_DPS_PAGE_SIZE</strong> auf WIA_PAGE_A4 festlegt, sollte der Minitreiber <strong>WIA_DPS_PAGE_WIDTH</strong> auf 11692 und <strong>WIA_DPS_PAGE_HEIGHT</strong> auf 8267 festlegen. (Der Minitreiber sollte auch <strong>WIA_IPS_XEXTENT</strong> und <strong>WIA_IPS_YEXTENT</strong> entsprechend festlegen.) Beachten Sie Folgendes: Wenn <strong>WIA_DPS_PAGE_SIZE</strong> auf WIA_PAGE_CUSTOM festgelegt ist, wird die Ausrichtungseinstellung nicht verwendet, um die Erweiterungsdimensionen der zu überprüfenden Seite zu bestimmen.</p>
<p>Der Minitreiber ist dafür verantwortlich, sicherzustellen, dass die <a href="-wia-wiaitempropscanneritem.md"><strong>eigenschaft WIA_IPS_ORIENTATION</strong></a> mit dem aktuellen Auswahlbereich in Übereinstimmung steht. Wenn eine Anwendung den Wert von <strong>WIA_IPS_ORIENTATION</strong> in einen Wert ändert, der für die aktuell ausgewählte Seitengröße ungültig ist, sollte der Minitreiber den Wert von <strong>WIA_DPS_PAGE_SIZE</strong> in eine Seitengröße ändern, die vom neuen Ausrichtungswert unterstützt wird.</p>
<p>Wenn eine Anwendung die <strong>eigenschaft WIA_DPS_PAGE_SIZE</strong> auf WIA_PAGE_CUSTOM festlegt, ist der aktuelle Auswahlbereich nicht betroffen. Der WIA-Minitreiber sollte das aktuelle Bildlayout abrufen, beginnend mit den aktuellen Einstellungen der <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> und <strong>WIA_IPS_YPOS</strong> Eigenschaften. Wenn die Einstellung für die Seitengröße zu einem Auswahlbereich außerhalb des Scannerbetts führt, muss der Minitreiber automatisch die Werte der <strong>eigenschaften WIA_IPS_XPOS</strong> und <strong>WIA_IPS_YPOS</strong> an gültige Einstellungen anpassen. Wenn die <strong>Eigenschaften WIA_DPS_PAGE_SIZE</strong> und <strong>WIA_IPS_ORIENTATION</strong> gleichzeitig festgelegt sind und sie ungültig sind, wenn sie in Kombination angewendet werden, sollte der Minitreiber die Einstellungen der Anwendung fehlschlagen lassen, indem er einen Fehler in <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::d rvValidateItemProperties</a>zurückgibt. .</p>
<p>Die folgenden vier Beispiele zeigen verschiedene <strong>WIA_DPS_PAGE_SIZE</strong> Szenarien.</p>
<ol>
<li>Der Treiber meldet die Einstellungen.</li>
<li>Eine Anwendung legt die <strong>eigenschaft WIA_DPS_PAGE_SIZE</strong> auf WIA_PAGE_LETTER fest.</li>
<li>Eine Anwendung legt die <a href="-wia-wiaitempropscanneritem.md"><strong>eigenschaft WIA_IPS_ORIENTATION</strong></a> auf LANSCAPE fest.</li>
<li>Eine Anwendung ändert die <a href="-wia-wiaitempropscanneritem.md"><strong>eigenschaft WIA_IPS_XEXTENT</strong></a> in einen kleineren Wert.</li>
</ol>
<p><strong>Beispiel 1: Der Minitreiber meldet die Einstellungen.</strong></p>
<p>Im folgenden Beispiel legt der Minitreiber einen benutzerdefinierten Auswahlbereich fest, bevor eine Anwendung WIA-Eigenschaften festlegt. In diesem Fall stellt der Auswahlbereich das gesamte Flatbed dar.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_WIDTH = 11500
WIA_DPS_PAGE_HEIGHT = 14000
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
<p><strong>Beispiel 2: Eine Anwendung legt die</strong> eigenschaft <strong>WIA_DPS_PAGE_SIZE</strong>  <strong>auf WIA_PAGE_LETTER</strong></p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_WIDTH = 8500
WIA_DPS_PAGE_HEIGHT = 11000
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
<p><strong>Beispiel 3: Eine Anwendung legt die</strong> <strong>WIA_IPS_ORIENTATION-Eigenschaft auf LANSCAPE</strong> fest. <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a>  </p>
<p>Das physische Bett muss in der Lage sein, eine Seite zu erhalten, die sich ursprünglich im Querformat befand.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_HEIGHT = 11000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
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
<p><strong>Beispiel 4: Eine Anwendung ändert die</strong> eigenschaft <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>in einen<strong>kleineren Wert.</strong>  </p>
<p>Im folgenden Beispiel ändert eine Anwendung die <a href="-wia-wiaitempropscanneritem.md"><strong>eigenschaft WIA_IPS_XEXTENT</strong></a> in 1000. Der Minitreiber sollte davon ausgehen, dass der in <strong>WIA_IPS_XEXTENT</strong> enthaltene neue Wert für die <strong>eigenschaft WIA_DPS_PAGE_SIZE</strong> nicht mehr gültig ist, und daher <strong>WIA_DPS_PAGE_SIZE</strong> in WIA_PAGE_CUSTOM ändern. Der Minitreiber muss auch <strong>WIA_DPS_PAGE_WIDTH</strong>anpassen.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_HEIGHT = 10000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
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
<td ><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Breite der ausgewählten aktuellen Seite in Tausendstel Zoll. Eine Anwendung liest diese Eigenschaft, um die physischen Dimensionen der zu überprüfenden Seite zu bestimmen. Wenn sich die Erweiterungseinstellungen von bekannten Seitengrößen unterscheiden, meldet diese Eigenschaft die Breite der Seite, deren <strong>WIA_DPS_PAGE_SIZE</strong> -Eigenschaft auf WIA_PAGE_CUSTOM festgelegt ist. <strong>WIA_DPS_PAGE_WIDTH</strong> müssen mit dem Wert <a href="-wia-wiaitempropscanneritem.md"><strong>von WIA_IPS_XEXTENT</strong></a>synchronisiert sein, der die Breite der zu scannenden Seite in Pixel angibt. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die aktuelle Anzahl von Seiten, die von einem automatischen Dokumentfeeder bezogen werden sollen. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>; Zugriff: Lesen/Schreiben; Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (null bis zur maximalen Anzahl von Seiten, die der Dokumentfeeder enthalten kann)</p>
<p>Eine Anwendung liest diese Eigenschaft, um die Seitenkapazität des Dokumentfeeders zu bestimmen. Die Anwendung legt diese Eigenschaft auch auf die Anzahl der Seiten fest, die überprüft werden sollen.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Wenn der Duplexmodus aktiviert ist (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> auf FEEDER | DUPLEX ), <strong>WIA_DPS_PAGES</strong> ist immer noch gleich der Anzahl der zu überprüfende Seiten.
</blockquote>
</div>
<div>
 
</div>
<p>Ein Blatt Papier enthält automatisch zwei Seiten, wenn DUPLEX aktiviert ist, auch wenn die Rückseite der Seite leer ist.</p>
<p>Wenn <strong>WIA_DPS_PAGES</strong> auf 1 festgelegt wird, verarbeitet ein Scanner eine der Seiten. Wenn ein Scanner im Duplexmodus nicht nur eine Seite einer Seite überprüfen kann, sollte der <strong>WIA_DPS_PAGES</strong> gültige Wert für den Inc-Member der WIA_PROPERTY_INFO-Struktur in 2 geändert werden. Dieser Wert signalisiert der Anwendung, dass seiten in Vielfachen von zwei angefordert werden müssen. Der Wert 0 bedeutet, dass <em>alle</em> Seiten, die derzeit in den Dokumentfeeder geladen sind, überprüft werden sollen.</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </dl></td>
<td ><p>Gibt die Farbe des Hintergrunds des zu scannenden Blatts an. Diese Eigenschaft ist für Scanner mit einem Nummernschild optional. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Zugriff: Schreibgeschützter Zugriff, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Das Format der Farbinformationen ist <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD.</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt den Vorschaumodus für ein Gerät an. Eine Anwendung legt diese Eigenschaft fest, um das Gerät in einen Vorschaumodus zu versetzen.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die beiden Konstanten, die mit dieser Eigenschaft gültig sind. </p>
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
<td>Die Anwendung führt eine abschließende Überprüfung durch.</td>
</tr>
<tr class="even">
<td>WIA_PREVIEW_SCAN</td>
<td>Die Anwendung führt eine Vorschauüberprüfung durch.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </dl></td>
<td ><p>Enthält einen Wert, der angibt, ob der Scanner Seiten in einem Scannerpuffer zwischenspeichert, bevor sie an die Anwendung gesendet werden.</p>
<p>Der Wert 0 (null) deaktiviert die Überprüfung im Voraus, und es werden keine Seiten im Voraus überprüft. Bei normalen Datenübertragungen für das gepufferte Scan-Ahead-Element werden die gepufferten Seiten abgerufen. WIA-Eigenschaften können während eines Scan-Ahead-Vorgangs nicht geändert werden. Diese Eigenschaft ist optional.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> von 0 (null) bis zur maximalen Anzahl von Seiten, die der Dokumentfeeder enthalten kann.</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows 7 und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt die Zu überprüfende Eingabequelle (Flatbed, automatischer Dokumentfeeder oder Adapter für Filescans) oder den Speicherort an, von dem Daten übertragen werden sollen.</p>
<p>Ein Scanereignis benachrichtigt die Anwendung, dass der Benutzer eine Überprüfung initiiert hat, aber das Ereignis gibt nicht den Namen des WIA-Elements an, das die Eingabequelle darstellt. Der Ereignishandler der Anwendung kann die WIA_DPS_SCAN_AVAILABLE_ITEM-Eigenschaft des Stammelements abfragen, um den Namen des Eingabequellelements abzurufen.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> von 0 (null) bis zur maximalen Anzahl von Seiten, die der Dokumentfeeder enthalten kann.</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Dienst-ID eines Webdienstscannergeräts. Der WIA 2.0-Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird mit Windows Vista und höher nicht unterstützt. Verwenden <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Registrierung bzw. Ausrichtungs- und Edgeerkennung für Dokumente, die auf dem Flatbed platziert werden. Der Minitreiber erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft gibt an, wie das Blatt horizontal auf dem Scankopf eines Scanners oder eines Scanners mit Blättern positioniert wird. Die -Eigenschaft wird verwendet, um vorherzusagen, wo auf dem Scankopf ein Dokument platziert wird.</p>
<p>Bei Scannern, die mehr als einen Scankopf unterstützen, ist diese Eigenschaft relativ zum obersten Scankopf. Diese Eigenschaft ist für Sheet-Fed-, Scroll-Fed- und Scanner-Scanner obligatorisch.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Konstante</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LEFT_JUSTIFIED</td>
<td>Das Blatt wird in Bezug auf den Scankopf links positioniert.</td>
</tr>
<tr class="even">
<td>ZENTRIERT</td>
<td>Das Blatt wird auf dem Scankopf zentriert.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>Das Blatt wird in Bezug auf den Scankopf rechts positioniert.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista nicht unterstützt. Verwenden <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt an, ob ein Element ein Vorschausteuerelement benötigt, das dem Benutzer angezeigt wird. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die folgende Tabelle enthält die beiden Konstanten, die mit dieser Eigenschaft gültig sind. </p>
<table>
<thead>
<tr class="header">
<th>Konstante</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_SHOW_PREVIEW_CONTROL</td>
<td>Zeigen Sie dem Benutzer ein Vorschausteuer steuerelement an, da dieses Gerät eine Vorschau ausführen kann.</td>
</tr>
<tr class="even">
<td>WIA_DONT_SHOW_PREVIEW_CONTROL</td>
<td>Zeigen Sie dem Benutzer kein Vorschausteuer steuerelement an, da dieses Gerät keine Vorschau ausführen kann.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Wird vom WIA-Dienst verwendet, um den Minitreiber über den Benutzerkontonamen (ggf. einschließlich des Netzwerkdomänennamens) der Sitzung zu informieren, in der die aktuelle WIA-Anwendung ausgeführt wird.</p>
<p>Dies ist eine Stammelementeigenschaft, die vom WIA-Dienst verwaltet wird.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird mit Windows Vista und höher nicht unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Registrierung oder vertikale Ausrichtung und Kantenerkennung für Dokumente, die auf dem Flatbed platziert sind. Der Minitreiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind. </p>
<table>
<thead>
<tr class="header">
<th>Konstante</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TOP_JUSTIFIED</td>
<td>Das Papier ist obenbiert.</td>
</tr>
<tr class="even">
<td>ZENTRIERT</td>
<td>Das Papier ist zentriert.</td>
</tr>
<tr class="odd">
<td>BOTTOM_JUSTIFIED</td>
<td>Das Papier ist unten rechtsbiert.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Siehe auch</strong>.</p>
<p><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird mit Windows Vista und höher nicht unterstützt. Verwenden <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt die maximale Höhe in Tausendstel Zoll an, die auf der vertikalen Achse (Y) von der Tafel eines Flatbed-Scanners bei der aktuellen Auflösung gescannt wird. Diese Eigenschaft gilt auch für automatische Dokumentfeeder, die Blätter zum Scannen auf die Tafel eines Flatbed-Scanners verschieben. Diese Eigenschaft ist für Scanner mit einem Schild obligatorisch. Andere Scannertypen implementieren stattdessen die <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird mit Windows Vista und höher nicht unterstützt. Verwenden <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt die maximale Höhe (in Tausendstel Zoll) an, die in der vertikalen Achse (Y) von einer Hand oder einem Blattfeedscanner bei der aktuellen Auflösung gescannt wird. Diese Eigenschaft gilt auch für automatische Dokumentfeeder, die scannen, ohne Blätter auf die Tafel eines Flatbed-Scanners zu verschieben. Diese Eigenschaft ist für Scanner mit Blattfähre obligatorisch. Scroll-Fed- und Hand-Held-Scanner sollten diese Eigenschaft nicht implementieren.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 
