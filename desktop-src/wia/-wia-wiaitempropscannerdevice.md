---
description: Für Windows-Abbild Beschaffung (WIA)-Hardware Geräte sind Eigenschaftswerte vorhanden, die in der Windows-Registrierung gespeichert sind.
ms.assetid: 78caa3af-927b-4143-9e88-4b5c918d00a4
title: Eigenschaften Konstanten für Scanner-Geräte (wiadef. h)
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
ms.openlocfilehash: af50f5d319e368ce2a672c040dc9d23843436121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345733"
---
# <a name="scanner-device-property-constants"></a>Eigenschaften Konstanten für Scanner-Geräte

Für Windows-Abbild Beschaffung (WIA)-Hardware Geräte sind Eigenschaftswerte vorhanden, die in der Windows-Registrierung gespeichert sind. Weitere Informationen finden Sie unter [**Allgemeine Geräte Eigenschafts Konstanten**](-wia-wiaitempropcommondevice.md). Die folgenden Geräteeigenschaften Konstanten, mit den zugehörigen Zeichen folgen, sind spezifisch für digitale Bildscanner.

Das Präfix "WIA \_ DPS \_ " gibt eine Geräte Eigenschaft für Scanner-Geräte an und ist die in C/C++ verwendete Benennungs Konvention. Bei der Skripterstellung verwenden diese Konstanten das Präfix "scannerdevice" und sind Teil des enumerierten Typs " [wiaitempropertyid](-wia-wiaitempropertyid.md) ". Der entsprechende Elementname aus dieser Skript Enumeration wird in Klammern neben dem Konstanten Namen C/C++ in der folgenden Liste angezeigt.



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
<td style="text-align: left;"><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>scannerdeviceabviceid</dt> </dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
Diese Eigenschaft wird nur unter Windows Vista und höher unterstützt.
</blockquote>
<br/> Enthält einen eindeutigen funktionsinstanzbezeichner für ein Webdienst-Scanner-Gerät. Dieser Bezeichner stellt den Webdienst auf dem Scannergerät dar, mit dem der WIA-Mini Treiber kommuniziert. Es sollten keine Annahmen über die Form dieses Bezeichners vorgenommen werden. Der WIA-Mini Treiber erstellt und verwaltet diese Eigenschaft. <br/> WIA-Anwendungen können den Wert von WIA_DPS_DEVICE_ID verwenden, um mithilfe der funktionsermittlungs-API zu suchen, das funktionsinstanzobjekt, das das in der aktuellen WIA 2,0-Sitzung verwendete Webdienst Scanner-Gerät darstellt.<br/> Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </dl></td>
<td style="text-align: left;">Reserviert, nicht verwenden.<br/> Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </dl></td>
<td style="text-align: left;">Reserviert, nicht verwenden.<br/> Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>scannerdevicedocumenthandlingfunktionen</dt> </dl></td>
<td style="text-align: left;">Enthält die Funktionen des Scanners. Der Mini Treiber erstellt und verwaltet diese Eigenschaft. <br/> Eine Anwendung liest diese Eigenschaft, um zu bestimmen, ob für den Scanner ein Flatbed, ein Dokument Server oder ein Duplexer installiert ist. Diese Eigenschaft wird auch verwendet, um die installierten Features weiter zu definieren.<br/> Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> In der folgenden Tabelle werden die Konstanten beschrieben, die nur mit Windows 7 gültig sind.<br/> 
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AUTO_SOURCE</td>
<td>Auf dem Scanner ist ein automatischer Dokument Handler installiert.</td>
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
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ADVANCED_DUP</td>
<td>Das Gerät unterstützt die erweiterte Duplex Scan Konfiguration. Verwenden Sie WIA_IPS_DUPLEX_SETTINGS, um zwischen der Verwendung von grundlegenden und erweiterten Duplex Konfigurationen zu wechseln.</td>
</tr>
<tr class="even">
<td>DETECT_FILM_TPA</td>
<td>Der Scanner kann erkennen, wann der Transparenz-/Filteradapter zum Scannen bereit ist.</td>
</tr>
<tr class="odd">
<td>DETECT_STOR</td>
<td>Der Scanner kann erkennen, wenn Dokumente im internen Speicher vorhanden sind.</td>
</tr>
<tr class="even">
<td>FILM_TPA</td>
<td>Der Scanner verfügt über einen Transparenz-/filterscanneradapter.</td>
</tr>
<tr class="odd">
<td>STOR</td>
<td>Der Scanner ist mit einem internen Image Speichergerät ausgestattet.</td>
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
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DETECT_FEED</td>
<td>Der Scanner kann ein Dokument im-Feeder erkennen.</td>
</tr>
<tr class="even">
<td>DETECT_FLAT</td>
<td>Der Scanner kann ein Dokument auf dem flachen Platen erkennen.</td>
</tr>
<tr class="odd">
<td>DETECT_SCAN</td>
<td>Der Scanner kann ein Dokument im Draht nur durch Scannen erkennen.</td>
</tr>
<tr class="even">
<td>Sammlungen</td>
<td>Der Scanner verfügt über einen Duplexer.</td>
</tr>
<tr class="odd">
<td>Nährt</td>
<td>Auf dem Scanner ist ein automatischer Dokument Handler installiert.</td>
</tr>
<tr class="even">
<td>Rate</td>
<td>Der Scanner verfügt über eine flache Plate.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>In der folgenden Tabelle werden die Konstanten beschrieben, die nur mit Windows XP gültig sind. Diese Werte sind für Windows 7 und Windows Vista veraltet und sollten nicht verwendet werden.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DETECT_DUP</td>
<td>Der Scanner kann eine Duplex Scan Anforderung vom Benutzer erkennen.</td>
</tr>
<tr class="even">
<td>DETECT_DUP_AVAIL</td>
<td>Der Scanner kann erkennen, wenn Duplexer installiert ist.</td>
</tr>
<tr class="odd">
<td>DETECT_FEED_AVAIL</td>
<td>Der Scanner kann erkennen, wann die automatische Dokument-feestallation installiert ist.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>scannerdevicedocumenthandlingselect</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird in Windows Vista und höher nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die aktuelle Scanner-Erfassungs Quelle und den aktuellen Modus. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Eine Anwendung liest diese Eigenschaft, um die aktuelle Erwerbs Quelle des Scanners zu ermitteln oder diese Eigenschaft zu schreiben, um die Quelle und den Modus des Scanners festzulegen. Außerdem verwenden Anwendungen diese Eigenschaft, um die Duplexer-Funktionalität zu aktivieren und zu deaktivieren.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>Die folgende Tabelle enthält die zehn Konstanten, die mit dieser Eigenschaft gültig sind. </p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Draht</td>
<td>Mit dem Dokument-Feeder Scan Vorgang.</td>
</tr>
<tr class="even">
<td>Flach</td>
<td>Überprüfen Sie mit dem Flatbed.</td>
</tr>
<tr class="odd">
<td>Gelegene</td>
<td>Mithilfe von Duplexer-Vorgängen scannen.</td>
</tr>
<tr class="even">
<td>AUTO_ADVANCE</td>
<td>Aktiviert das automatische füttern des nächsten Dokuments nach einem Scanvorgang.</td>
</tr>
<tr class="odd">
<td>FRONT_FIRST</td>
<td>Scannen Sie zuerst den Anfang des Dokuments. Dieser Wert ist gültig, wenn Duplex festgelegt ist.</td>
</tr>
<tr class="even">
<td>BACK_FIRST</td>
<td>Scannen Sie zuerst das Dokument zurück. Dieser Wert ist gültig, wenn Duplex festgelegt ist.</td>
</tr>
<tr class="odd">
<td>FRONT_ONLY</td>
<td>Nur den Vordergrund suchen. Dieser Wert ist gültig, wenn Duplex festgelegt ist.</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>Nur Rück scannen. Dieser Wert ist gültig, wenn Duplex festgelegt ist.</td>
</tr>
<tr class="odd">
<td>NEXT_PAGE</td>
<td>Scannen Sie die nächste Seite des Dokuments.</td>
</tr>
<tr class="even">
<td>Vorab Feed</td>
<td>Aktivieren Sie den Vorfeed-Modus. Das nächste Dokument wird beim Scannen vorab positioniert.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>scannerdevicedocumenthandlingstatus</dt> </dl></td>
<td style="text-align: left;"><p>Enthält den aktuellen Status des installierten, bereinigten, Dokument-oder Duplexer-Elements des Scanners. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Diese Eigenschaft wird von einer Anwendung gelesen, um zu bestimmen, ob das Scanner-Gerät zur Verwendung bereit ist. Dies ist eine ideale Möglichkeit, um zu überprüfen, ob sich das Papier vor dem Erwerb eines Images im Draht befindet.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind. Ein Sternchen * gibt an, dass das Flag in Windows Vista oder höher nicht unterstützt wird. Das Symbol <strong>V</strong> gibt an, dass das Flag nur in Windows Vista und höher unterstützt wird. </p>
<table>
<thead>
<tr class="header">
<th>Flags</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FEED_READY</td>
<td>Der Flatbed ist einsatzbereit.</td>
</tr>
<tr class="even">
<td>FLAT_READY</td>
<td>Der Scanner verfügt über ein Dokument auf der Registerkarte "Flatbed".</td>
</tr>
<tr class="odd">
<td>DUP_READY</td>
<td>Der Duplexer ist aktiviert und kann verwendet werden.</td>
</tr>
<tr class="even">
<td>FLAT_COVER_UP</td>
<td>Die flache Abdeckung ist aktiv.</td>
</tr>
<tr class="odd">
<td>PATH_COVER_UP</td>
<td>Der Papierpfad wird behandelt und verhindert den ordnungsgemäßen Betrieb.</td>
</tr>
<tr class="even">
<td>PAPER_JAM</td>
<td>Ein Dokument wird im Dokument-feemed blockiert.</td>
</tr>
<tr class="odd">
<td>FILM_TPA_READY<strong>V</strong></td>
<td>Der Transparenz Adapter ist installiert und einsatzbereit.</td>
</tr>
<tr class="even">
<td>STORAGE_READY<strong>V</strong></td>
<td>Das interne Speichergerät ist bereit.</td>
</tr>
<tr class="odd">
<td>STORAGE_FULL<strong>V</strong></td>
<td>Der Speicher ist voll, es sind keine Uploadvorgänge möglich.</td>
</tr>
<tr class="even">
<td>MULTIPLE_FEED<strong>V</strong></td>
<td>Es ist eine mehrfach Feed-Bedingung aufgetreten (normalerweise mit einem PAPER_JAM).</td>
</tr>
<tr class="odd">
<td>DEVICE_ATTENTION<strong>V</strong></td>
<td>Es ist ein Fehler aufgetreten, der einen Benutzereingriff auf dem Gerät erfordert.</td>
</tr>
<tr class="even">
<td>LAMP_ERR<strong>V</strong></td>
<td>Der Scanner ist aufgrund eines Lamp-Problems nicht bereit.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>scannerdeviceendorsercharacters</dt> </dl></td>
<td style="text-align: left;"><p>Enthält alle gültigen Zeichen, die eine Anwendung verwenden kann, um gültige Endorser-Zeichen folgen zu erstellen. Ein Endorser ist ein Drucker, der auf einem Scanner installiert ist, der eine Textnachricht auf jeder gescannten Seite ausgibt. Der Mini Treiber sollte die Einstellung der <strong>WIA_DPS_ENDORSER_STRING</strong> -Eigenschaft mit dem gültigen Zeichensatz in dieser Eigenschaft überprüfen. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>scannerdeviceendorserstring</dt> </dl></td>
<td style="text-align: left;"><p>Enthält eine Zeichenfolge, die auf jeder Seite, die der Mini Treiber scannt, unterstützt werden soll (d. h. gedruckt). Eine Anwendung legt diese Eigenschaft mithilfe des gültigen Zeichensatzes fest, der in der <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> -Eigenschaft gemeldet wird. Der Mini Treiber sollte Dokumente nur dann unterstützen, wenn eine Zeichenfolge in dieser Eigenschaft festgelegt ist. Eine leere Zeichenfolge bedeutet, dass die Endorser-Funktionalität deaktiviert ist.</p>
<p>Da es für den Treiber zuständig ist, die Endorser-Zeichenfolge zu interpretieren, kann der Treiber Sonderzeichen in <strong>WIA_DPS_ENDORSER_STRING</strong>verwenden. Diese Zeichen werden jedoch nur von Ihren Anwendungen interpretiert.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
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
<td>$Date $</td>
<td>Das Datum im Format yyyy/mm/dd.</td>
</tr>
<tr class="even">
<td>$Day $</td>
<td>Der Tag in der Form DD.</td>
</tr>
<tr class="odd">
<td>$MONTH $</td>
<td>Der Monat des Jahres in der Form mm.</td>
</tr>
<tr class="even">
<td>$Page _Count $</td>
<td>Die Anzahl der übertragenen Seiten.</td>
</tr>
<tr class="odd">
<td>$Time $</td>
<td>Die Uhrzeit im Format hh: mm: SS.</td>
</tr>
<tr class="even">
<td>$Year $</td>
<td>Das Jahr im Format yyyy.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>scannerdecoeglobalidentity</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur unter Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die SOAP-Adresse eines Webdienst-Scanner-Geräts. Der WIA 2,0-Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>scannerdevicehorizontalbedregistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Registrierung bzw. die horizontale Ausrichtung für Dokumente, die im Flatbed abgelegt werden. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
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
<td>Das Papier wird linksbündig ausgerichtet.</td>
</tr>
<tr class="even">
<td>Ego</td>
<td>Das Dokument wird zentriert.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>Das Dokument ist rechtsbündig ausgerichtet.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Siehe auch</strong></p>
<p><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>scannerdebug size</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt die maximale Breite (in Tausendstel Zoll) an, die in der horizontalen Achse (X-Achse) von den Platen eines Flatbed-Scanners bei der aktuellen Auflösung gescannt wird. Diese Eigenschaft gilt auch für automatische Dokument Feeden, die Blätter zum Scannen in die Plate eines flatsheet-Scanners verschieben. Diese Eigenschaft ist für Scanner mit einem Platen obligatorisch. Andere Scannertypen implementieren stattdessen die <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> -Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>scannerdebug feedsize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt die maximale Breite (in Tausendstel Zoll) an, die auf der horizontalen Achse (X-Achse) von einem Hand Held-oder Blatt Feed-Scanner bei der aktuellen Auflösung gescannt wird. Diese Eigenschaft gilt auch für automatische Dokument Feeden, die durchsucht werden, ohne Blätter in die Plate eines flachen Scanners zu verschieben. Diese Eigenschaft ist für Blatt-, Scroll-und handgehaltene Scanner obligatorisch.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>scannerdevicemaxscantime</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die maximale Zeit zum Scannen einer einzelnen Seite mit den aktuellen Eigenschaften Einstellungen in Millisekunden. Diese Eigenschaft wird von einer Anwendung gelesen, um zu schätzen, wie lange es dauert, bis eine Seite gescannt wird. Dies ist hilfreich, wenn Sie die Bedingungen eines Geräts ermitteln, das nicht mehr reagiert. Der Mini Treiber erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft ist für alle Scanner erforderlich.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>scannerde viceminhorizontalsheetfeedsize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die physischen horizontalen Dimensionen der kleinsten Seite, die der Dokument-Draht Scanner in Tausendstel Zoll Scannen kann. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Siehe auch</strong></p>
<p><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>scannerdecoeminverticalsheetfeedsize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die physischen vertikalen Dimensionen der kleinsten Seite, die der Dokument-Draht Scanner in Tausendstel Zoll Scannen kann. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Siehe auch</strong></p>
<p><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>scannerdeviceopticalxres</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Horizontale optische Auflösung. Höchste unterstützte horizontale optische Auflösung in dpi. Diese Eigenschaft ist ein einzelner Wert. Dabei handelt es sich nicht um eine Liste aller Auflösungen, die vom Gerät generiert werden können. Vielmehr handelt es sich hierbei um die Auflösung der Geräte Optiken. Der Mini Treiber erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft ist für alle Scanner erforderlich.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>scannerdeviceopticalyres</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Vertikale optische Auflösung. Höchste unterstützte vertikale optische Auflösung in dpi. Diese Eigenschaft ist ein einzelner Wert. Dabei handelt es sich nicht um eine Liste aller Auflösungen, die vom Gerät generiert werden. Vielmehr handelt es sich hierbei um die Auflösung der Geräte Optiken. Der Mini Treiber erstellt und verwaltet diese Eigenschaft. Diese Eigenschaft ist für alle Scanner erforderlich.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>scannerdeviceorientation</dt> </dl></td>
<td style="text-align: left;"><p>Enthält die aktuelle Ausrichtungs Einstellung. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>In einer Anwendung wird die <strong>WIA_DPS_ORIENTATION</strong> -Eigenschaft festgelegt, um die ursprüngliche Ausrichtung einer abzurufenden Seite oder eines Bilds zu definieren. Weitere Informationen zur Verwendung von WIA_DPS_ORIENTATION finden Sie unter <strong>WIA_DPS_PAGE_SIZE</strong></p>
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
<td>Landschaf</td>
<td>90-Grad-Drehung gegen den Uhrzeigersinn, relativ zur Hochformat Ausrichtung.</td>
</tr>
<tr class="even">
<td>Hochformat</td>
<td>0 Grad.</td>
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

<p> </p>
<p><strong>Siehe auch</strong></p>
<p><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>scannerdecoepadcolor</dt> </dl></td>
<td style="text-align: left;"><p>Die Farbe, die zum Auffüllen verwendet wird, wenn nicht genügend Bild Daten zum Auffüllen eines angeforderten Puffers vorhanden sind. Diese Eigenschaft wird für Scanner implementiert, die den Puffer auffüllen. Diese Eigenschaft ist für alle Scanner optional. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Das Format der Farbinformationen ist <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">rgbquad</a>.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>scannerdevicepageheight</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Höhe der aktuell ausgewählten Seite in Tausendstel Zoll. Der Mini Treiber erstellt und verwaltet die <strong>WIA_DPS_PAGE_HEIGHT</strong> -Eigenschaft. Eine Anwendung liest diese Eigenschaft, um die physischen Dimensionen der zu scannenden Seite zu bestimmen. Wenn sich die Block Einstellungen von den bekannten Seitengrößen unterscheiden, meldet diese Eigenschaft die Höhe der Seite, deren <strong>WIA_DPS_PAGE_SIZE</strong> -Eigenschaft auf WIA_PAGE_CUSTOM festgelegt ist (ein Wert der <strong>WIA_DPS_PAGE_SIZE</strong> -Eigenschaft). <strong>WIA_DPS_PAGE_HEIGHT</strong> müssen mit <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>synchronisiert sein, das die Höhe der zu scannenden Seite in Pixel meldet.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>scannerdevicepagesize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Größe der Seite, die derzeit zum Scannen ausgewählt ist. Um die Dimensionen der zu überprüfenden Seite auszuwählen, legt eine Anwendung diese Eigenschaft fest. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
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
<td>8267 X 11692 (Hochformat Ausrichtung)</td>
</tr>
<tr class="even">
<td>WIA_PAGE_CUSTOM</td>
<td>Definiert durch die Werte der Eigenschaften " <strong>WIA_DPS_PAGE_HEIGHT</strong> " und " <strong>WIA_DPS_PAGE_WIDTH</strong> ".</td>
</tr>
<tr class="odd">
<td>WIA_PAGE_LETTER</td>
<td>8500 X 11000 (Hochformat Ausrichtung)</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Der Wert der <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> -Eigenschaft bestimmt die Ausrichtung der aktuell ausgewählten Seite. Die Eigenschaften " <strong>WIA_DPS_PAGE_WIDTH</strong> " und " <strong>WIA_DPS_PAGE_HEIGHT</strong> " melden die Dimensionen der Seite in Tausendstel Zoll. Beachten Sie, dass diese Eigenschaften mit <strong>WIA_IPS_XEXTENT</strong> und <strong>WIA_IPS_YEXTENT</strong>übereinstimmen müssen, die die Abmessungen der Seite in Pixel enthalten. Gültige Werte vom Typ "WIA_PROP_LIST" sollten von gültigen Einstellungen der Eigenschaft " <strong>WIA_IPS_ORIENTATION</strong> " abhängen. Wenn das Gerät keine Querformat orientierten Dokumente mit einer WIA_PAGE_A4 Einstellung Scannen kann, sollten WIA_PAGE_A4 nicht in der Liste der gültigen Werte für die <strong>WIA_DPS_PAGE_SIZE</strong> -Eigenschaft angezeigt werden, wenn <strong>WIA_IPS_ORIENTATION</strong> auf lanscape festgelegt ist.</p>
<p>Wenn eine Anwendung <strong>WIA_DPS_PAGE_SIZE</strong> auf einen anderen Wert als WIA_PAGE_CUSTOM festlegt, sollte der Mini Treiber die Werte <strong>WIA_DPS_PAGE_WIDTH</strong> und <strong>WIA_DPS_PAGE_HEIGHT</strong> in Tausendstel Zoll an die Dimensionen der Seite anpassen. Außerdem sollten die Werte <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> und <strong>WIA_IPS_YEXTENT</strong> auf die Dimensionen der Seite in Pixel angepasst werden.</p>
<p>Wenn eine Block Einstellung (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> oder <strong>WIA_IPS_YEXTENT</strong>) in einen Wert geändert wird, der nicht mit der aktuellen Einstellung der Seitengröße identisch ist, sollte der Mini Treiber den Wert der Eigenschaft <strong>WIA_DPS_PAGE_SIZE</strong> in WIA_PAGE_CUSTOM ändern. Der Mini Treiber sollte auch <strong>WIA_DPS_PAGE_WIDTH</strong> oder <strong>WIA_DPS_PAGE_HEIGHT</strong> entsprechend der neuen Block Einstellung ändern.</p>
<p>Wenn <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> auf lanscape festgelegt ist, werden die Block Einstellungen gekippt &quot; . &quot; Wenn eine Anwendung z. b. <strong>WIA_DPS_PAGE_SIZE</strong> auf WIA_PAGE_A4 festlegt, sollte der Mini Treiber <strong>WIA_DPS_PAGE_WIDTH</strong> auf 11692 und <strong>WIA_DPS_PAGE_HEIGHT</strong> auf 8267 festlegen. (Der Mini Treiber sollte auch <strong>WIA_IPS_XEXTENT</strong> festlegen und entsprechend <strong>WIA_IPS_YEXTENT</strong> .) Beachten Sie Folgendes: Wenn <strong>WIA_DPS_PAGE_SIZE</strong> auf WIA_PAGE_CUSTOM festgelegt ist, wird die Ausrichtung nicht verwendet, um die Bereichs Dimensionen der zu scannenden Seite zu bestimmen.</p>
<p>Der Mini Treiber ist dafür verantwortlich, sicherzustellen, dass die <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> -Eigenschaft mit dem aktuellen Auswahlbereich übereinstimmt. Wenn eine Anwendung den Wert von <strong>WIA_IPS_ORIENTATION</strong> in einen Wert ändert, der für die aktuell ausgewählte Seitengröße ungültig ist, sollte der Mini Treiber den Wert <strong>WIA_DPS_PAGE_SIZE</strong> in eine Seitengröße ändern, die vom neuen Wert für die Ausrichtung unterstützt wird.</p>
<p>Wenn eine Anwendung die <strong>WIA_DPS_PAGE_SIZE</strong> -Eigenschaft auf WIA_PAGE_CUSTOM festlegt, ist der aktuelle Auswahlbereich nicht betroffen. Der WIA-Mini Treiber sollte das aktuelle Bild Layout abrufen, beginnend mit den aktuellen Einstellungen der Eigenschaften " <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> " und " <strong>WIA_IPS_YPOS</strong> ". Wenn die Einstellung für die Seitengröße zu einem Auswahlbereich führt, der sich außerhalb des Scanners befindet, muss der Mini Treiber automatisch die Werte der Eigenschaften <strong>WIA_IPS_XPOS</strong> und <strong>WIA_IPS_YPOS</strong> an gültige Einstellungen anpassen. Wenn die Eigenschaften <strong>WIA_DPS_PAGE_SIZE</strong> und <strong>WIA_IPS_ORIENTATION</strong> gleichzeitig festgelegt sind und Sie in Kombination mit der Anwendung ungültig sind, sollte der Mini Treiber die Einstellungen der Anwendung nicht durch Zurückgeben eines Fehlers in <a href="https://msdn.microsoft.com/library/ms794145.aspx">iwiaminidrv::d rvvalidateitemproperties</a>ausführen. .</p>
<p>In den folgenden vier Beispielen werden verschiedene <strong>WIA_DPS_PAGE_SIZE</strong> Szenarios gezeigt.</p>
<ol>
<li>Der Treiber meldet die Einstellungen.</li>
<li>In einer Anwendung wird die <strong>WIA_DPS_PAGE_SIZE</strong> -Eigenschaft auf WIA_PAGE_LETTER festgelegt.</li>
<li>Eine Anwendung legt die <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> -Eigenschaft auf lanscape fest.</li>
<li>Die <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> -Eigenschaft wird von einer Anwendung in einen kleineren Wert geändert.</li>
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
<p><strong>Beispiel 2: eine Anwendung legt die</strong> <strong>WIA_DPS_PAGE_SIZE</strong>-<strong>Eigenschaft auf fest WIA_PAGE_LETTER</strong>  </p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<p><strong>Beispiel 3: eine Anwendung legt die</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a>-<strong>Eigenschaft auf lanscape</strong> fest.  </p>
<p>Das physische Bett muss in der Lage sein, eine Seite abzurufen, die sich ursprünglich in Querformat orientiert.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<p><strong>Beispiel 4: eine Anwendung ändert die</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>-<strong>Eigenschaft in einen kleineren Wert</strong>  </p>
<p>Im folgenden Beispiel ändert eine Anwendung die <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> -Eigenschaft in 1000. Der Mini Treiber sollte davon ausgehen, dass der in <strong>WIA_IPS_XEXTENT</strong> enthaltene neue Wert für die Eigenschaft <strong>WIA_DPS_PAGE_SIZE</strong> nicht mehr gültig ist und daher <strong>WIA_DPS_PAGE_SIZE</strong> in WIA_PAGE_CUSTOM ändern sollte. Der Mini Treiber muss auch <strong>WIA_DPS_PAGE_WIDTH</strong>anpassen.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<td style="text-align: left;"><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Breite der aktuell ausgewählten Seite in Tausendstel Zoll. Eine Anwendung liest diese Eigenschaft, um die physischen Dimensionen der zu scannenden Seite zu bestimmen. Wenn sich die Block Einstellungen von den bekannten Seitengrößen unterscheiden, meldet diese Eigenschaft die Breite der Seite, deren <strong>WIA_DPS_PAGE_SIZE</strong> -Eigenschaft auf WIA_PAGE_CUSTOM festgelegt ist. <strong>WIA_DPS_PAGE_WIDTH</strong> muss mit dem Wert von <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>synchronisiert sein, der die Breite der zu scannenden Seite in Pixel meldet. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <dt><strong>WIA_DPS_PAGES</strong></dt> <dt>scannerentvicepages</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die aktuelle Anzahl der Seiten, die von einem automatischen Dokument-feedwert abgerufen werden sollen. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>; Zugriff: Lesen/Schreiben; Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (null bis zur maximalen Anzahl von Seiten, die der Dokument-feedwert aufnehmen kann)</p>
<p>Eine Anwendung liest diese Eigenschaft, um die Seiten Kapazität des Dokument Anlegers zu bestimmen. Diese Eigenschaft wird von der Anwendung auch auf die Anzahl der Seiten festgelegt, die gescannt werden.</p>
<div class="alert">
<blockquote>
[!Note]<br />
, Wenn der Duplex Modus aktiviert ist (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> ist auf "Fee" festgelegt | Duplex), <strong>WIA_DPS_PAGES</strong> gleichzeitig gleich der Anzahl der zu scanenden Seiten ist.
</blockquote>
</div>
<div>
 
</div>
<p>Ein Papierblatt enthält automatisch zwei Seiten, wenn Duplex aktiviert ist, auch wenn die Rückseite der Seite leer ist.</p>
<p>Das Festlegen von <strong>WIA_DPS_PAGES</strong> auf 1 bewirkt, dass ein Scanner eine der Seiten der Seite verarbeitet. Wenn ein Scanner nicht nur eine Seite einer Seite im Duplex Modus überprüfen kann, sollte der <strong>WIA_DPS_PAGES</strong> gültigen Wert für das Inc-Mitglied der WIA_PROPERTY_INFO Struktur in 2 geändert werden. Dieser Wert signalisiert der Anwendung, dass Seiten in Vielfachen von zwei Anforderungen angefordert werden müssen. Der Wert 0 (null) bedeutet, dass <em>alle</em> Seiten, die derzeit in den Dokument-feedergeladen werden, gescannt werden sollen.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>scannerdeviceplatkocolor</dt> </dl></td>
<td style="text-align: left;"><p>Gibt die Farbe der Platen auf der Rückseite des zu scannenden Blatts an. Diese Eigenschaft ist für Scanner mit Platen optional. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Das Format der Farbinformationen ist <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">rgbquad</a>.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>scannerdevicepreview</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt den Vorschaumodus für ein Gerät an. Eine Anwendung legt diese Eigenschaft fest, um das Gerät in einen Vorschaumodus zu versetzen.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
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
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>scannerdebug Pages</dt> </dl></td>
<td style="text-align: left;"><p>Enthält einen Wert, der angibt, ob der Scanner Seiten in einem Scanner-Puffer zwischenspeichert, bevor Sie an die Anwendung gesendet werden.</p>
<p>Der Wert 0 deaktiviert die Überprüfung voraus, und es werden keine Seiten vor der Überprüfung durchsucht. Wenn Sie normale Datenübertragungen für das gepufferte Scan-Ahead-Element durchgehen, werden die gepufferten Seiten abgerufen. WIA-Eigenschaften können während eines Scanvorgangs nicht geändert werden. Diese Eigenschaft ist optional.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 0 (null) bis zur maximalen Anzahl von Seiten, die der Dokument-feedvorgang enthalten kann.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>scannerabvicescanavailableitem</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows 7 und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt die Eingabe Quelle ("Flatbed", "Automatic Document" oder "fil-Scan Adapter") an, die überprüft werden soll, oder den Speicherort, von dem Daten übertragen werden.</p>
<p>Ein Scan-Ereignis benachrichtigt die Anwendung, dass der Benutzer einen Scan initiiert hat, aber das Ereignis stellt nicht den Namen des WIA-Elements bereit, das die Eingabe Quelle darstellt. Der-Ereignishandler der Anwendung kann die WIA_DPS_SCAN_AVAILABLE_ITEM-Eigenschaft des Stamm Elements Abfragen, um den Namen des Eingabe Quell Elements zu erhalten.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 0 (null) bis zur maximalen Anzahl von Seiten, die der Dokument-feedvorgang enthalten kann.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>scannerdecoeserviceid</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Dienst-ID eines Webdienst-Scanner-Geräts. Der WIA 2,0-Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>scannerdevicesheetfeederregistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.
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
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>scannerdebug-Steuer</dt> Element </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt an, ob ein Element ein Vorschau Steuerelement benötigt, das für den Benutzer angezeigt wird. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die folgende Tabelle enthält die beiden Konstanten, die mit dieser Eigenschaft gültig sind. </p>
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
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>scannerenviceusername</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Wird vom WIA-Dienst verwendet, um den Mini Treiber über den Benutzerkonto Namen (z. b. den ggf. den Netzwerk Domänen Namen) der Sitzung zu informieren, in der die aktuelle WIA-Anwendung ausgeführt wird.</p>
<p>Dabei handelt es sich um eine Stamm Element Eigenschaft, die vom WIA-Dienst verwaltet wird.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>scannerdeviceverticalbedregistration</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt.
</blockquote>
</div>
<div>
 
</div>
<p>Enthält die Registrierung bzw. die vertikale Ausrichtung und Kantenerkennung für Dokumente, die im Flatbed abgelegt werden. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind. </p>
<table>
<thead>
<tr class="header">
<th>Konstante</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TOP_JUSTIFIED</td>
<td>Das Dokument ist oberstes Recht.</td>
</tr>
<tr class="even">
<td>Ego</td>
<td>Das Dokument wird zentriert.</td>
</tr>
<tr class="odd">
<td>BOTTOM_JUSTIFIED</td>
<td>Das Papier ist unten bündig ausgerichtet.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Siehe auch</strong>.</p>
<p><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>scannerdecoeverticalbedsize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt die maximale Höhe in Tausendstel Zoll an, die auf der vertikalen Achse (Y-Achse) von der Plate eines Flatbed-Scanners bei der aktuellen Auflösung gescannt wird. Diese Eigenschaft gilt auch für automatische Dokument Feeden, die Blätter zum Scannen in die Plate eines flachen Scanners verschieben. Diese Eigenschaft ist für Scanner mit einem Platen obligatorisch. Andere Scannertypen implementieren stattdessen die <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> -Eigenschaft.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>scannerdecoeverticalsheetfeedsize</dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt. Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Gibt die maximale Höhe (in Tausendstel Zoll) an, die in der vertikalen Achse (Y-Achse) von einem Hand Held-oder Blatt Feed-Scanner bei der aktuellen Auflösung gescannt wird. Diese Eigenschaft gilt auch für automatische Dokument Feeden, die durchsucht werden, ohne Blätter in die Plate eines flachen Scanners zu verschieben. Diese Eigenschaft ist für Blatt Scanner obligatorisch. Scrollgesteuerte und handgehaltene Scanner sollten diese Eigenschaft nicht implementieren.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
