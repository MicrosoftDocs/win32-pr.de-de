---
description: Windows WIA-Hardwaregeräte (Image Acquisition) verfügen über Eigenschaftswerte, die in der registrierung Windows werden. Weitere Informationen finden Sie unter Common Device Property Constants.
ms.assetid: 7893137b-194c-4ea1-b15c-59d2f41f972a
title: Eigenschaftenkonst constants des Kamerageräts (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPC_PICTURES_TAKEN
- WIA_DPC_PICTURES_REMAINING
- WIA_DPC_EXPOSURE_MODE
- WIA_DPC_EXPOSURE_COMP
- WIA_DPC_EXPOSURE_TIME
- WIA_DPC_FNUMBER
- WIA_DPC_FLASH_MODE
- WIA_DPC_FOCUS_MODE
- WIA_DPC_FOCUS_MANUAL_DIST
- WIA_DPC_ZOOM_POSITION
- WIA_DPC_PAN_POSITION
- WIA_DPC_TILT_POSITION
- WIA_DPC_TIMER_MODE
- WIA_DPC_TIMER_VALUE
- WIA_DPC_POWER_MODE
- WIA_DPC_BATTERY_STATUS
- WIA_DPC_THUMB_WIDTH
- WIA_DPC_THUMB_HEIGHT
- WIA_DPC_PICT_WIDTH
- WIA_DPC_PICT_HEIGHT
- WIA_DPC_DIMENSION
- WIA_DPC_COMPRESSION_SETTING
- WIA_DPC_FOCUS_METERING
- WIA_DPC_TIMELAPSE_INTERVAL
- WIA_DPC_TIMELAPSE_NUMBER
- WIA_DPC_BURST_INTERVAL
- WIA_DPC_BURST_NUMBER
- WIA_DPC_EFFECT_MODE
- WIA_DPC_DIGITAL_ZOOM
- WIA_DPC_SHARPNESS
- WIA_DPC_CONTRAST
- WIA_DPC_CAPTURE_MODE
- WIA_DPC_CAPTURE_DELAY
- WIA_DPC_EXPOSURE_INDEX
- WIA_DPC_EXPOSURE_METERING_MODE
- WIA_DPC_FOCUS_METERING_MODE
- WIA_DPC_FOCUS_DISTANCE
- WIA_DPC_FOCAL_LENGTH
- WIA_DPC_RGB_GAIN
- WIA_DPC_WHITE_BALANCE
- WIA_DPC_UPLOAD_URL
- WIA_DPC_ARTIST
- WIA_DPC_COPYRIGHT_INFO
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f33e7f2dfd17e535e47026aee173feccb7c69584
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624196"
---
# <a name="camera-device-property-constants"></a>Eigenschaftenkonst constants des Kamerageräts

Windows WIA-Hardwaregeräte (Image Acquisition) verfügen über Eigenschaftswerte, die in der registrierung Windows werden. Weitere Informationen finden Sie unter [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).

Die folgenden Geräteeigenschaftskonst constants mit den zugehörigen Zeichenfolgen sind spezifisch für Digitalkameras. Das Präfix "WIA DPC" gibt eine Geräteeigenschaft für Kameras an und ist \_ \_ die benennungskonvention, die in C/C++ verwendet wird. Zu Skriptzwecken verwenden diese Konstanten das Präfix "CameraDevice" und sind Teil des [aufzählten WiaItemPropertyId-Typs.](-wia-wiaitempropertyid.md) Der entsprechende Membername aus dieser Skriptenumeration wird in Klammern neben dem C/C++-Konstantennamen in der folgenden Liste angezeigt.

> [!Note]  
> WIA unterstützt keine Kameras in Windows Vista oder höher. Verwenden Sie für diese Versionen des Windows die Windows Portable Device (WPD)-API, die im Windows Driver Development Kit (DDK) beschrieben ist, um Bilder von Kameras zu erhalten.

 



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
<td ><span id="WIA_DPC_PICTURES_TAKEN"></span><span id="wia_dpc_pictures_taken"></span><dl> <dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </dl></td>
<td >Die Anzahl der Bilder, die die Kamera aufgenommen hat. Der Minitreiber erstellt und verwaltet diese Eigenschaft.<br/> Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_PICTURES_REMAINING"></span><span id="wia_dpc_pictures_remaining"></span><dl> <dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </dl></td>
<td >Die Anzahl der Bilder, die mit den aktuellen Eigenschafteneinstellungen aufgenommen werden können. Wenn sich diese Einstellungen ändern und sich die Änderungen auf die Größe der Bilder auswirken, die das Kameragerät erzeugt, sollte der WIA-Minitreiber die Anzahl der verbleibenden Bilder aktualisieren. Der Minitreiber erstellt und verwaltet diese Eigenschaft.<br/> Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_EXPOSURE_MODE"></span><span id="wia_dpc_exposure_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </dl></td>
<td >Gibt den aktuellen Belichtungsmodus der Kamera an. Eine Anwendung ändert diese Eigenschaft, um den Belichtungsmodus des Kamerageräts zu steuern.<br/> Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a><br/> Die folgende Tabelle enthält die sieben Konstanten, die mit dieser Eigenschaft gültig sind.<br/> 
<table>
<thead>
<tr class="header">
<th>Belichtungsmodus</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EXPOSUREMODE_MANUAL</td>
<td>Die Geschwindigkeit und Blende der Brille werden vom Benutzer festgelegt.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_AUTO</td>
<td>Die Dreh- und Öffnungsgeschwindigkeit wird automatisch von der Kamera festgelegt.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_APERTURE_PRIORITY</td>
<td>Die Öffnung wird vom Benutzer festgelegt, und die Kamera legt automatisch die Drehgeschwindigkeit fest.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_SHUTTER_PRIORITY</td>
<td>Die Geschwindigkeit wird vom Benutzer festgelegt, und die Kamera legt die Blende automatisch fest.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PROGRAM_CREATIVE</td>
<td>Die Dreh- und Öffnungsgeschwindigkeit wird automatisch von der Kamera festgelegt, die für noch Subjekte optimiert ist.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_PROGRAM_ACTION</td>
<td>Die Dreh- und Öffnungsgeschwindigkeit wird automatisch von der Kamera festgelegt und für Szenen optimiert, die schnelle Bewegung enthalten.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PORTRAIT</td>
<td>Die Dreh- und Öffnungsgeschwindigkeit wird automatisch von der Kamera festgelegt, die für hochformatige Brillen optimiert ist.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_EXPOSURE_COMP"></span><span id="wia_dpc_exposure_comp"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </dl></td>
<td ><p>Ermöglicht die Anpassung des Festgelegtpunkts des Steuerelements für die automatische Belichtung der Digitalkamera. Die Einstellung 0 (null) ändert z. B. nicht die von der Factory festgelegten automatischen Belichtungsstufe. Die Einheiten befinden sich in Stopps, die um den Faktor 1000 skaliert werden, um &quot; Bruchstoppwerte &quot; zu ermöglichen. Eine Einstellung von 2000 entspricht zwei Stopps mehr Belichtung (viermal mehr Energie auf dem Sensor), was zu besseren Bildern führt. Eine Einstellung von -1.000 entspricht einer 1-Stopp-Weniger-Belichtung (die Hälfte der Energie auf dem Sensor), die dunklere Bilder ergibt. Die Einstellungswerte befinden sich in APEX-Einheiten (Additive System of Exposure). Diese Eigenschaft kann entweder als Liste oder als Bereich von Werten ausgedrückt werden. Diese Eigenschaft wird in der Regel nur verwendet, wenn auf dem Gerät die <strong>WIA_DPC_EXPOSURE_MODE-Eigenschaft</strong> auf EXPOSUREMODE_MANUAL.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> oder WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_EXPOSURE_TIME"></span><span id="wia_dpc_exposure_time"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </dl></td>
<td ><p>Entspricht der Geschwindigkeit in Sekunden, die um 10.000 skaliert werden. In der Regel verwendet das Gerät diese Eigenschaft nur, wenn die <strong>WIA_DPC_EXPOSURE_MODE-Eigenschaft</strong> auf EXPOSUREMODE_MANUAL oder EXPOSUREMODE_SHUTTER_PRIORITY.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> oder WIA_PROP_LIST</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_FNUMBER"></span><span id="wia_dpc_fnumber"></span><dl> <dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </dl></td>
<td ><p>Entspricht der Öffnung der Brille in Einheiten der f-Stoppnummer, die um 100 skaliert wird. Die Einstellung dieser Eigenschaft ist in der Regel nur gültig, wenn die <strong>WIA_DPC_EXPOSURE_MODE-Eigenschaft</strong> auf EXPOSUREMODE_MANUAL oder EXPOSUREMODE_APERTURE_PRIORITY.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_FLASH_MODE"></span><span id="wia_dpc_flash_mode"></span><dl> <dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </dl></td>
<td ><p>Definiert die aktuelle Einstellung für den Flashmodus für das Kameragerät. Der Gerätetreiber aufzählt die unterstützten Werte dieser Eigenschaft. Eine Anwendung schreibt diese Eigenschaft, um den Flashmodus für das Kameragerät festlegen.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die sechs Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Flashmodus</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FLASHMODE_AUTO</td>
<td>Das Kameragerät bestimmt die richtigen Flasheinstellungen.</td>
</tr>
<tr class="even">
<td>FLASHMODE_FILL</td>
<td>Das Kameragerät ist so konfiguriert, dass es unabhängig von den aktuellen Beleuchtungsbedingungen blinkt.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_OFF</td>
<td>Das Kameragerät ist so konfiguriert, <em>dass es nicht</em> auf aufgenommene Bilder blinkt.</td>
</tr>
<tr class="even">
<td>FLASHMODE_REDEYE_AUTO</td>
<td>Das Kameragerät bestimmt die richtigen Flasheinstellungen mithilfe der Reduzierung der roten Augen, unabhängig von den aktuellen Beleuchtungsbedingungen.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_REDEYE_FILL</td>
<td>Das Kameragerät ist so konfiguriert, dass es unabhängig von den aktuellen Beleuchtungsbedingungen red-eye reduction und flash verwendet.</td>
</tr>
<tr class="even">
<td>FLASHMODE_EXTERNALSYNC</td>
<td>Das Kameragerät ist für die Synchronisierung mit externen Flasheinheiten konfiguriert.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_FOCUS_MODE"></span><span id="wia_dpc_focus_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </dl></td>
<td ><p>Definiert die aktuelle Fokusmoduseinstellung für das Kameragerät. Der Gerätetreiber aufzählt die unterstützten Werte dieser Eigenschaft. Eine Anwendung schreibt diese Eigenschaft, um den Fokusmodus für das Kameragerät zu festlegen.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Fokusmodus</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FOCUSMODE_MANUAL</td>
<td>Das Kameragerät ist so konfiguriert, dass der Benutzer sich manuell konzentrieren kann.</td>
</tr>
<tr class="even">
<td>FOCUSMODE_AUTO</td>
<td>Das Kameragerät ist so konfiguriert, dass es sich automatisch auf den Fokus konzentriert.</td>
</tr>
<tr class="odd">
<td>FOCUSMODE_MACROAUTO</td>
<td>Das Kameragerät ist so konfiguriert, dass der Fokus automatisch mithilfe von Makroeinstellungen für kurze Reichweiten erfolgt.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_FOCUS_MANUAL_DIST"></span><span id="wia_dpc_focus_manual_dist"></span><dl> <dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </dl></td>
<td ><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_ZOOM_POSITION"></span><span id="wia_dpc_zoom_position"></span><dl> <dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </dl></td>
<td ><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_PAN_POSITION"></span><span id="wia_dpc_pan_position"></span><dl> <dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </dl></td>
<td ><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_TILT_POSITION"></span><span id="wia_dpc_tilt_position"></span><dl> <dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </dl></td>
<td ><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_TIMER_MODE"></span><span id="wia_dpc_timer_mode"></span><dl> <dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </dl></td>
<td ><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_TIMER_VALUE"></span><span id="wia_dpc_timer_value"></span><dl> <dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </dl></td>
<td ><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_POWER_MODE"></span><span id="wia_dpc_power_mode"></span><dl> <dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </dl></td>
<td ><p>Definiert die aktuelle Stromquelle für das Kameragerät. Eine Anwendung liest diese Eigenschaft, um zu bestimmen, welche Stromquelle die Kamera verwendet.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die folgende Tabelle enthält die beiden Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Energiesparmodus</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>POWERMODE_LINE</td>
<td>Das Kameragerät wird auf einem Netzadapter betrieben.</td>
</tr>
<tr class="even">
<td>POWERMODE_BATTERY</td>
<td>Das Kameragerät wird mit Akkubetrieb betrieben.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_BATTERY_STATUS"></span><span id="wia_dpc_battery_status"></span><dl> <dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </dl></td>
<td ><p>Der Prozentsatz der Akkuleistung, der für den Betrieb des Kamerageräts übrig bleibt. Dieser Wert sollte eine ganze Zahl zwischen 0 und 100 sein. Eine Anwendung liest diese Eigenschaft, um die verbleibende Akkulaufzeit des Kamerageräts zu bestimmen.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_THUMB_WIDTH"></span><span id="wia_dpc_thumb_width"></span><dl> <dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </dl></td>
<td ><p>Die Breite eines Miniaturbilds in Pixel, das für neu erfasste Bilder verwendet werden soll. Eine Anwendung liest diesen Wert, um eine geschätzte Größe zum Anzeigen von Miniaturansichten auf ihrer Benutzeroberfläche zu erhalten.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) oder Schreibgeschütztes (WIA_PROP_NONE), Gültige Werte: WIA_PROP_LIST oder WIA_PROP_NONE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_THUMB_HEIGHT"></span><span id="wia_dpc_thumb_height"></span><dl> <dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </dl></td>
<td ><p>Die Breite eines Miniaturbilds in Pixel, das für neu erfasste Bilder verwendet werden soll. Eine Anwendung liest diesen Wert, um eine geschätzte Größe zum Anzeigen von Miniaturansichten auf ihrer Benutzeroberfläche zu erhalten.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) oder Schreibgeschütztes (WIA_PROP_NONE), Gültige Werte: WIA_PROP_LIST oder WIA_PROP_NONE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_PICT_WIDTH"></span><span id="wia_dpc_pict_width"></span><dl> <dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </dl></td>
<td ><p>Die Breite in Pixel, die für neu erfasste Bilder verwendet werden soll. Die Liste der gültigen Werte für diese Eigenschaft weist eine 1:1-Entsprechung zur Liste der gültigen Werte für die <strong>WIA_DPC_PICT_HEIGHT-Eigenschaft</strong> auf. Wenn die individuelle Breite und Höhe linear festlegbar und orthogonal sind, können sie als Bereich ausgedrückt werden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_PICT_HEIGHT"></span><span id="wia_dpc_pict_height"></span><dl> <dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </dl></td>
<td ><p>Die Höhe in Pixel, die für neu erfasste Bilder verwendet werden soll. Die Liste der gültigen Werte für diese Eigenschaft weist eine 1:1-Entsprechung mit der Liste der gültigen Werte für die <strong>WIA_DPC_PICT_WIDTH-Eigenschaft</strong> auf. Wenn die individuelle Breite und Höhe linear festlegbar und orthogonal sind, können sie als Bereich ausgedrückt werden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_DIMENSION"></span><span id="wia_dpc_dimension"></span><dl> <dt><strong>WIA_DPC_DIMENSION</strong></dt> </dl></td>
<td ><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_COMPRESSION_SETTING"></span><span id="wia_dpc_compression_setting"></span><dl> <dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </dl></td>
<td ><p>Sie sollte in Bezug auf die wahrgenommene Bildqualität über einen breiten Bereich von Szeneninhalten ungefähr linear sein und enthält entweder einen Bereich oder eine Liste von ganzen Zahlen. Kleinere ganze Zahlen werden verwendet, um eine niedrigere Qualität (d. b. maximale Komprimierung) darzustellen, während größere ganze Zahlen verwendet werden, um eine höhere Qualität (d. b. minimale Komprimierung) darzustellen. Alle verfügbaren Einstellungen auf einem Gerät sind nur relativ zu diesem Gerät und daher gerätespezifisch.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_FOCUS_METERING"></span><span id="wia_dpc_focus_metering"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </dl></td>
<td ><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_TIMELAPSE_INTERVAL"></span><span id="wia_dpc_timelapse_interval"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </dl></td>
<td ><p>Die Zeit in Millisekunden zwischen Bilderfassungen in einem Zeitraffererfassungsvorgang.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_TIMELAPSE_NUMBER"></span><span id="wia_dpc_timelapse_number"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </dl></td>
<td ><p>Die Anzahl der Bilder, die das Gerät während einer Zeitraffererfassung zu erfassen versucht.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_BURST_INTERVAL"></span><span id="wia_dpc_burst_interval"></span><dl> <dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </dl></td>
<td ><p>Die Zeit in Millisekunden zwischen Bilderfassungen während eines Burstvorgangs.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_BURST_NUMBER"></span><span id="wia_dpc_burst_number"></span><dl> <dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </dl></td>
<td ><p>Die Anzahl der Bilder, die das Gerät während eines Burstvorgangs zu erfassen versucht.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_EFFECT_MODE"></span><span id="wia_dpc_effect_mode"></span><dl> <dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </dl></td>
<td ><p>Gibt den speziellen Bilderfassungsmodus der Kamera an.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Effektmodus</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EFFECTMODE_STANDARD</td>
<td>Erfassen Sie ein Bild im Standardmodus für die Kamera.</td>
</tr>
<tr class="even">
<td>EFFECTMODE_BW</td>
<td>Erfassen sie ein Graustufenbild.</td>
</tr>
<tr class="odd">
<td>EFFECTMODE_SEPIA</td>
<td>Erfassen sie ein Sepia-Bild.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_DIGITAL_ZOOM"></span><span id="wia_dpc_digital_zoom"></span><dl> <dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </dl></td>
<td ><p>Das effektive Zoomverhältnis des erfassten Bilds der Digitalkamera, skaliert um den Faktor 10. Der Wert 10 entspricht dem Fehlen des digitalen Zooms (1X), was der von der Kamera erfassten Standardszenengröße entspricht. Der Wert 20 entspricht einem 2X-Zoom, bei dem ein Viertel der Standardszenengröße von der Kamera erfasst wird.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_SHARPNESS"></span><span id="wia_dpc_sharpness"></span><dl> <dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </dl></td>
<td ><p>Die wahrgenommene Schärfe eines erfassten Bilds. Diese Eigenschaft kann entweder eine Liste von Werten oder einen Wertebereich verwenden. Der Mindestwert stellt die geringste Schärfe dar, während der Höchstwert die maximale Schärfe darstellt. In der Regel stellt ein Wert in der Mitte des Bereichs eine normale oder standardmäßige Schärfe dar.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_CONTRAST"></span><span id="wia_dpc_contrast"></span><dl> <dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </dl></td>
<td ><p>Der wahrgenommene Kontrast eines erfassten Bilds. Diese Eigenschaft kann entweder eine Liste von Werten oder einen Wertebereich enthalten. Der unterstützte Mindestwert stellt die geringste Kontrastmenge dar, während der Höchstwert den meisten Kontrast darstellt. In der Regel stellt ein Wert in der Mitte des Bereichs einen normalen Oder Standardkontrast dar.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_CAPTURE_MODE"></span><span id="wia_dpc_capture_mode"></span><dl> <dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </dl></td>
<td ><p>Legt den Bilderfassungsmodus fest.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Aufzeichnungsmodus</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CAPTUREMODE_NORMAL</td>
<td>Normaler Modus für die Kamera.</td>
</tr>
<tr class="even">
<td>CAPTUREMODE_BURST</td>
<td>Erfassen Sie mehrere Bilder in schneller Folge, wie durch die Werte der eigenschaften WIA_DPC_BURST_NUMBER <strong>und</strong> <strong>WIA_DPC_BURST_INTERVAL</strong> definiert.</td>
</tr>
<tr class="odd">
<td>CAPTUREMODE_TIMELAPSE</td>
<td>Erfassen Sie mehr als ein Bild nacheinander, wie durch die eigenschaften WIA_DPC_TIMELAPSE_NUMBER <strong>und</strong> <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> definiert.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_CAPTURE_DELAY"></span><span id="wia_dpc_capture_delay"></span><dl> <dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </dl></td>
<td ><p>Der Wert, der die Zeitverzögerung in Millisekunden darstellt, die zwischen dem Erfassungstrigger und der tatsächlichen Initiierung der Datenerfassung eingefügt werden soll. Diese Eigenschaft ist nicht für die Beschreibung der Zeit zwischen Frames für die einzelinitiierung, mehrere <strong></strong> Erfassungen wie Burst oder Zeitraffer vorgesehen, die über separate Intervalleigenschaften WIA_DPC_BURST_INTERVAL und <strong>WIA_DPC_TIMELAPSE_INTERVAL.</strong> In diesen Fällen dient sie immer noch als anfängliche Verzögerung, bevor das erste Bild in der Reihe unabhängig von der Zeit zwischen den Frames erfasst wird. Für keine Präcaptureverzögerung sollte diese Eigenschaft auf 0 (null) festgelegt werden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_EXPOSURE_INDEX"></span><span id="wia_dpc_exposure_index"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </dl></td>
<td ><p>Ermöglicht die Emulation von Einstellungen für die Filmgeschwindigkeit auf einer Digitalkamera. Die Einstellungen entsprechen den ISO-Bezeichnungen (ASA/DIN). In der Regel unterstützt ein Gerät diskrete aufzählte Werte, aber eine kontinuierliche Kontrolle über einen Bereich von Werten ist möglich. Der Wert 0xFFFF der Einstellung Automatisches ISO entspricht.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_EXPOSURE_METERING_MODE"></span><span id="wia_dpc_exposure_metering_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </dl></td>
<td ><p>Gibt den Modus an, den die Kamera verwendet, um die Belichtungseinstellung automatisch anzupassen.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>

<table>
<thead>
<tr class="header">
<th>Belichtungsmessungsmodus</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EXPOSUREMETERING_AVERAGE</td>
<td>Legen Sie die Belichtung basierend auf dem Durchschnitt der gesamten Szene fest.</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERWEIGHT</td>
<td>Legen Sie die Belichtung basierend auf einem mittleren gewichteten Durchschnitt fest.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMETERING_MULTISPOT</td>
<td>Legen Sie die Belichtung basierend auf einem Multispotmuster fest.</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERSPOT</td>
<td>Legen Sie die Belichtung basierend auf einem Mittelpunkt fest.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_FOCUS_METERING_MODE"></span><span id="wia_dpc_focus_metering_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </dl></td>
<td ><p>Gibt den Modus an, den die Kamera verwendet, um den Fokus automatisch anzupassen.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die beiden Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Fokusmessungsmodus</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FOCUSMETERING_CENTERSPOT</td>
<td>Passen Sie den Fokus basierend auf einem Mittelpunkt an.</td>
</tr>
<tr class="even">
<td>FOCUSMETERING_MULTISPOT</td>
<td>Passen Sie den Fokus basierend auf einem Multispotmuster an.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_FOCUS_DISTANCE"></span><span id="wia_dpc_focus_distance"></span><dl> <dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </dl></td>
<td ><p>Der Abstand zwischen der Bilderfassungsebene der Digitalkamera und dem Fokuspunkt in Millimeter. Der Wert 0xFFFF entspricht einer Einstellung größer als 655 Meter.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_FOCAL_LENGTH"></span><span id="wia_dpc_focal_length"></span><dl> <dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </dl></td>
<td ><p>Die 35mm-äquivalente Fokuslänge. Die Werte dieser Eigenschaft entsprechen der Fokuslänge in Millimeter multipliziert mit 100. Die Fokuslänge bestimmt den optischen Zoom.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_RGB_GAIN"></span><span id="wia_dpc_rgb_gain"></span><dl> <dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </dl></td>
<td ><p>Eine auf NULL beendete Unicode-Zeichenfolge, die die rote, grüne und blaue Verstärkung darstellt, die auf Bilddaten angewendet wird. Beispielsweise stellt &quot; 4:25:50 einen roten Gewinn von 4, einen grünen Gewinn von 25 und einen blauen Gewinn von &quot; 50 dar.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_WHITE_BALANCE"></span><span id="wia_dpc_white_balance"></span><dl> <dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </dl></td>
<td ><p>Gibt an, wie die Digitalkamera Farbkanäle gewichtet.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Im Folgenden finden Sie eine Liste der möglichen Werte für diese Eigenschaft.</p>

<table>
<thead>
<tr class="header">
<th>Weißabgleich</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WHITEBALANCE_MANUAL</td>
<td>Der Weißabgleich wird direkt mithilfe der <strong>eigenschaft</strong> WIA_DPC_RGB_GAIN festgelegt.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_AUTO</td>
<td>Die Kamera verwendet einen automatischen Mechanismus, um den Weißabgleich zu setzen.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_ONEPUSH_AUTO</td>
<td>Die Kamera bestimmt die Einstellung für den Weißabgleich, wenn ein Benutzer die Aufnahmetaste drückt, während er die Kamera auf eine weiße Oberfläche klickt.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_DAYLIGHT</td>
<td>Die Kamera legt den Weißabgleich auf einen Wert fest, der für die Verwendung bei Sommerzeit geeignet ist.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLORESCENT</td>
<td>Die Kamera legt den Weißabgleich auf einen Wert fest, der für die Verwendung mit einer Glühbirnenquelle geeignet ist.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_TUNGSTEN</td>
<td>Die Kamera legt den Weißabgleich auf einen Wert fest, der für die Verwendung mit einer Lichtquelle geeignet ist.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLASH</td>
<td>Die Kamera legt den Weißabgleich auf einen Wert fest, der für die Verwendung mit einem elektronischen Flash geeignet ist.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_UPLOAD_URL"></span><span id="wia_dpc_upload_url"></span><dl> <dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </dl></td>
<td ><p>Beschreibt eine URL. Die von dieser Proroperty beschriebene URL ist eine URL, in die Bilder oder Objekte hochgeladen werden können, nachdem sie vom Gerät erworben wurden– je nach einem der folgenden Szenarien.</p>
<ul>
<li>Eine WIA-Anwendung liest diese Eigenschaft und ermöglicht dem Benutzer das automatische Hochladen von Bildern in die URL.</li>
<li>Eine Anwendung legt die URL fest, und andere Geräte (Kioske usw.) verwenden diese Eigenschaft.</li>
</ul>
<p>Microsoft Windows lädt keine Bilder selbst hoch.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPC_ARTIST"></span><span id="wia_dpc_artist"></span><dl> <dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </dl></td>
<td ><p>Der Name des Besitzers (der aktuelle Benutzer) des Geräts. Das Gerät verwendet diese Eigenschaft, um das Feld "Interpret" in jedem erfassten EXIF-Bild zu füllen.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPC_COPYRIGHT_INFO"></span><span id="wia_dpc_copyright_info"></span><dl> <dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </dl></td>
<td ><p>Die Copyrightbenachrichtigung. Das Gerät verwendet diese Eigenschaft, um das Feld Copyright in jedem erfassten EXIF-Bild zu füllen.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Lesen/Schreiben, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 




