---
description: Für Windows-Abbild Beschaffung (WIA)-Hardware Geräte sind Eigenschaftswerte vorhanden, die in der Windows-Registrierung gespeichert sind. Weitere Informationen finden Sie unter Allgemeine Geräte Eigenschafts Konstanten.
ms.assetid: 7893137b-194c-4ea1-b15c-59d2f41f972a
title: Eigenschaften Konstanten für Kamerageräte (wiadef. h)
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
ms.openlocfilehash: 0114fedd7fd4acf811e71db67376afecc2630cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485043"
---
# <a name="camera-device-property-constants"></a>Eigenschaften Konstanten für Kamerageräte

Für Windows-Abbild Beschaffung (WIA)-Hardware Geräte sind Eigenschaftswerte vorhanden, die in der Windows-Registrierung gespeichert sind. Weitere Informationen finden Sie unter [**Allgemeine Geräte Eigenschafts Konstanten**](-wia-wiaitempropcommondevice.md).

Die folgenden Geräteeigenschaften Konstanten, mit den zugehörigen Zeichen folgen, sind für digitale Kameras spezifisch. Das Präfix "WIA \_ DPC \_ " gibt eine Geräte Eigenschaft für Kameras an und ist die Benennungs Konvention, die in C/C++ verwendet wird. Bei der Skripterstellung verwenden diese Konstanten das Präfix "cameradevice" und sind Teil des enumerierten Typs [wiaitempropertyid](-wia-wiaitempropertyid.md) . Der entsprechende Elementname aus dieser Skript Enumeration wird in Klammern neben dem Konstanten Namen C/C++ in der folgenden Liste angezeigt.

> [!Note]  
> WIA unterstützt keine Kameras in Windows Vista oder höher. Verwenden Sie für diese Windows-Versionen die im Windows-Treiber Development Kit (DDK) beschriebene Windows-API für portable Geräte, um Images von Kameras abzurufen.

 



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
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_TAKEN"></span><span id="wia_dpc_pictures_taken"></span><dl> <dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>cameradevicepicturestaken</dt> </dl></td>
<td style="text-align: left;">Die Anzahl der Bilder, die die Kamera genommen hat. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.<br/> Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_REMAINING"></span><span id="wia_dpc_pictures_remaining"></span><dl> <dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>cameradevicepicturesrest</dt> </dl></td>
<td style="text-align: left;">Die Anzahl von Bildern, die mit den aktuellen Eigenschaften Einstellungen entnommen werden können. Wenn sich diese Einstellungen ändern und sich die Änderungen auf die Größe der Bilder auswirken, die das Kamera Gerät erzeugt, sollte der WIA-Mini Treiber die Anzahl der verbleibenden Bilder aktualisieren. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.<br/> Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_MODE"></span><span id="wia_dpc_exposure_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>cameradeviceexposuremode</dt> </dl></td>
<td style="text-align: left;">Gibt den aktuellen Anzeigemodus der Kamera an. Diese Eigenschaft wird von einer Anwendung geändert, um den Anzeigemodus des Kamera Geräts zu steuern.<br/> Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a><br/> Die folgende Tabelle enthält die sieben Konstanten, die mit dieser Eigenschaft gültig sind.<br/> 
<table>
<thead>
<tr class="header">
<th>Anzeigemodus</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EXPOSUREMODE_MANUAL</td>
<td>Die Auslösegeschwindigkeit und-Öffnung werden vom Benutzer festgelegt.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_AUTO</td>
<td>Die Auslösegeschwindigkeit und-Öffnung werden automatisch von der Kamera festgelegt.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_APERTURE_PRIORITY</td>
<td>Die Öffnung wird vom Benutzer festgelegt, und die Kamera legt die Auslösegeschwindigkeit automatisch fest.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_SHUTTER_PRIORITY</td>
<td>Die Auslösegeschwindigkeit wird vom Benutzer festgelegt, und die Kamera legt automatisch die Öffnung fest.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PROGRAM_CREATIVE</td>
<td>Die Auslösegeschwindigkeit und die Öffnungs Taste werden automatisch von der Kamera festgelegt, die für eine weitere Gegenfrage optimiert ist.</td>
</tr>
<tr class="even">
<td>EXPOSUREMODE_PROGRAM_ACTION</td>
<td>Die Auslösegeschwindigkeit und-Öffnung werden automatisch von der Kamera festgelegt, die für Szenen optimiert ist, die schnelles Bewegung enthalten.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMODE_PORTRAIT</td>
<td>Die Auslösegeschwindigkeit und die Öffnungs Taste werden automatisch von der Kamera festgelegt, die für hoch Fotografie optimiert ist.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_COMP"></span><span id="wia_dpc_exposure_comp"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>cameradeviceexposurecomp</dt> </dl></td>
<td style="text-align: left;"><p>Ermöglicht die Anpassung des festgelegten Punkts der automatischen verfügbar machung des digitalen Kamera-Steuer Elements. Beispielsweise wird bei einer Einstellung von 0 (null) die Einstellung für die automatische Festlegung der Werkseinstellungen nicht geändert. Die Einheiten werden in &quot; Stopps &quot; skaliert, die mit dem Faktor 1000 skaliert werden, um die Stopp Werte in Bruch Zeiten zu ermöglichen. Eine Einstellung von 2000 entspricht zwei nicht mehr Verfügbarkeit (viermal mehr Energie auf dem Sensor) und liefert hellere Bilder. Eine Einstellung von-1000 entspricht einem ungefährdenden unterlegungs Stand (eine Hälfte der Energie auf dem Sensor) und liefert dunklere Bilder. Die Einstellungs Werte befinden sich in einem Additiven System von Spitze Einheiten (Photo Exposition). Diese Eigenschaft kann entweder als Liste oder als Wertebereich ausgedrückt werden. Diese Eigenschaft wird in der Regel nur verwendet, wenn für das Gerät die <strong>WIA_DPC_EXPOSURE_MODE</strong> -Eigenschaft auf EXPOSUREMODE_MANUAL festgelegt ist.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> oder WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_TIME"></span><span id="wia_dpc_exposure_time"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>cameradeviceexposuretime</dt> </dl></td>
<td style="text-align: left;"><p>Entspricht der Zeit in Sekunden, die von 10.000 skaliert werden. In der Regel wird diese Eigenschaft vom Gerät nur verwendet, wenn die <strong>WIA_DPC_EXPOSURE_MODE</strong> -Eigenschaft auf EXPOSUREMODE_MANUAL oder EXPOSUREMODE_SHUTTER_PRIORITY festgelegt ist.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> oder WIA_PROP_LIST</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FNUMBER"></span><span id="wia_dpc_fnumber"></span><dl> <dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>cameradevicefnumber</dt> </dl></td>
<td style="text-align: left;"><p>Entspricht der Öffnung des Lens in Einheiten der f-Ende-Zahl, die von 100 skaliert wird. Die Einstellung dieser Eigenschaft ist in der Regel nur gültig, wenn die <strong>WIA_DPC_EXPOSURE_MODE</strong> -Eigenschaft auf EXPOSUREMODE_MANUAL oder EXPOSUREMODE_APERTURE_PRIORITY festgelegt ist.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FLASH_MODE"></span><span id="wia_dpc_flash_mode"></span><dl> <dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>cameradeviceflash Mode</dt> </dl></td>
<td style="text-align: left;"><p>Definiert die aktuelle Einstellung für den Flash Modus für das Kamera Gerät. Der Gerätetreiber listet die unterstützten Werte dieser Eigenschaft auf. Diese Eigenschaft wird von einer Anwendung geschrieben, um den Flash Modus für das Kamera Gerät festzulegen.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die sechs Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Flash Modus</th>
<th>Definition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FLASHMODE_AUTO</td>
<td>Das Kamera Gerät legt die richtigen Flash Einstellungen fest.</td>
</tr>
<tr class="even">
<td>FLASHMODE_FILL</td>
<td>Das Kamera Gerät ist so konfiguriert, dass es unabhängig von den aktuellen Beleuchtungsbedingungen blinkt.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_OFF</td>
<td>Das Kamera Gerät ist so konfiguriert, dass es <em>kein</em> Flash für ein Bild erstellt.</td>
</tr>
<tr class="even">
<td>FLASHMODE_REDEYE_AUTO</td>
<td>Das Kamera Gerät bestimmt die richtigen Flash Einstellungen mithilfe der Red-Eye-Reduzierung, unabhängig von den aktuellen Beleuchtungsbedingungen.</td>
</tr>
<tr class="odd">
<td>FLASHMODE_REDEYE_FILL</td>
<td>Das Kamera Gerät ist so konfiguriert, dass es unabhängig von den aktuellen Beleuchtungsbedingungen die Red-Eye-Reduzierung und Flash Flash verwendet.</td>
</tr>
<tr class="even">
<td>FLASHMODE_EXTERNALSYNC</td>
<td>Das Kamera Gerät ist für die Synchronisierung mit externen Flash Einheiten konfiguriert.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MODE"></span><span id="wia_dpc_focus_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>cameradevicefocemode</dt> </dl></td>
<td style="text-align: left;"><p>Definiert die aktuelle Fokus Modus-Einstellung für das Kamera Gerät. Der Gerätetreiber listet die unterstützten Werte dieser Eigenschaft auf. Diese Eigenschaft wird von einer Anwendung geschrieben, um den Fokus Modus für das Kamera Gerät festzulegen.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Fokusmodus</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FOCUSMODE_MANUAL</td>
<td>Das Kamera Gerät ist so konfiguriert, dass der Benutzer sich manuell fokussieren kann.</td>
</tr>
<tr class="even">
<td>FOCUSMODE_AUTO</td>
<td>Das Kamera Gerät ist so konfiguriert, dass es automatisch fokussiert wird.</td>
</tr>
<tr class="odd">
<td>FOCUSMODE_MACROAUTO</td>
<td>Das Kamera Gerät ist so konfiguriert, dass es sich automatisch mithilfe von Makro Einstellungen im kurzen Bereich befindet.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MANUAL_DIST"></span><span id="wia_dpc_focus_manual_dist"></span><dl> <dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ZOOM_POSITION"></span><span id="wia_dpc_zoom_position"></span><dl> <dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PAN_POSITION"></span><span id="wia_dpc_pan_position"></span><dl> <dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>cameradevicepanposition</dt> </dl></td>
<td style="text-align: left;"><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TILT_POSITION"></span><span id="wia_dpc_tilt_position"></span><dl> <dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>cameradevicetiltposition</dt> </dl></td>
<td style="text-align: left;"><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_MODE"></span><span id="wia_dpc_timer_mode"></span><dl> <dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>cameradevicetimermode</dt> </dl></td>
<td style="text-align: left;"><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_VALUE"></span><span id="wia_dpc_timer_value"></span><dl> <dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>cameradevicetimervalue</dt> </dl></td>
<td style="text-align: left;"><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_POWER_MODE"></span><span id="wia_dpc_power_mode"></span><dl> <dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>cameradevicepowermode</dt> </dl></td>
<td style="text-align: left;"><p>Definiert die aktuelle Stromquelle für das Kamera Gerät. Diese Eigenschaft wird von einer Anwendung gelesen, um zu bestimmen, welche Stromquelle von der Kamera verwendet wird.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Die folgende Tabelle enthält die beiden Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Energiesparmodus</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>POWERMODE_LINE</td>
<td>Das Kamera Gerät arbeitet auf einem Strom Adapter.</td>
</tr>
<tr class="even">
<td>POWERMODE_BATTERY</td>
<td>Das Kamera Gerät wird mit Akkuleistung betrieben.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BATTERY_STATUS"></span><span id="wia_dpc_battery_status"></span><dl> <dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>cameradevicebatterystatus</dt> </dl></td>
<td style="text-align: left;"><p>Der Prozentsatz der Akkukapazität, die für die Arbeit mit dem Kamera Gerät übrig bleibt. Dieser Wert sollte eine ganze Zahl zwischen 0 und 100 sein. Diese Eigenschaft wird von einer Anwendung gelesen, um die verbleibende Akku Lebensdauer des Kamera Geräts zu ermitteln.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_WIDTH"></span><span id="wia_dpc_thumb_width"></span><dl> <dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>cameradevicethumbwidth</dt> </dl></td>
<td style="text-align: left;"><p>Die Breite eines Miniatur Bilds, das für neu erfasste Bilder verwendet werden soll, in Pixel. Eine Anwendung liest diesen Wert, um eine geschätzte Größe zum Anzeigen von Miniaturansichten in der Benutzeroberfläche zu erhalten.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) oder schreibgeschützt (WIA_PROP_NONE), gültige Werte: WIA_PROP_LIST oder WIA_PROP_NONE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_HEIGHT"></span><span id="wia_dpc_thumb_height"></span><dl> <dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>cameradevicethumbheight</dt> </dl></td>
<td style="text-align: left;"><p>Die Breite eines Miniatur Bilds, das für neu erfasste Bilder verwendet werden soll, in Pixel. Eine Anwendung liest diesen Wert, um eine geschätzte Größe zum Anzeigen von Miniaturansichten in der Benutzeroberfläche zu erhalten.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) oder schreibgeschützt (WIA_PROP_NONE), gültige Werte: WIA_PROP_LIST oder WIA_PROP_NONE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICT_WIDTH"></span><span id="wia_dpc_pict_width"></span><dl> <dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>cameradevicepictwidth</dt> </dl></td>
<td style="text-align: left;"><p>Die Breite in Pixel, die für neu erfasste Bilder verwendet werden soll. Die Liste gültiger Werte für diese Eigenschaft weist eine eins-zu-eins-Entsprechung zur Liste gültiger Werte für die <strong>WIA_DPC_PICT_HEIGHT</strong> -Eigenschaft auf. Wenn die einzelnen Werte für Breite und Höhe linear feststellbar und orthogonal zueinander stehen, werden Sie möglicherweise als Bereich ausgedrückt.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICT_HEIGHT"></span><span id="wia_dpc_pict_height"></span><dl> <dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>cameradevicepictheight</dt> </dl></td>
<td style="text-align: left;"><p>Die Höhe in Pixel, die für neu erfasste Bilder verwendet werden soll. Die Liste gültiger Werte für diese Eigenschaft weist eine eins-zu-eins-Entsprechung mit der Liste gültiger Werte für die <strong>WIA_DPC_PICT_WIDTH</strong> -Eigenschaft auf. Wenn die einzelnen Werte für Breite und Höhe linear feststellbar und orthogonal zueinander stehen, werden Sie möglicherweise als Bereich ausgedrückt.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIMENSION"></span><span id="wia_dpc_dimension"></span><dl> <dt><strong>WIA_DPC_DIMENSION</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_COMPRESSION_SETTING"></span><span id="wia_dpc_compression_setting"></span><dl> <dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>cameradevicecompressionsetting</dt> </dl></td>
<td style="text-align: left;"><p>Sie sollten in Bezug auf die wahrgenommene Bildqualität für eine breite Palette von Szenen Inhalten ungefähr linear sein, und Sie enthält entweder einen Bereich oder eine Liste mit ganzen Zahlen. Kleinere ganze Zahlen werden verwendet, um eine niedrigere Qualität darzustellen (d. h. maximale Komprimierung), wohingegen größere ganze Zahlen verwendet werden, um eine höhere Qualität darzustellen (d. h. minimale Komprimierung). Alle verfügbaren Einstellungen auf einem Gerät sind nur auf dieses Gerät bezogen und sind daher gerätespezifisch.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING"></span><span id="wia_dpc_focus_metering"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </dl></td>
<td style="text-align: left;"><p>Reserviert, nicht verwenden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_INTERVAL"></span><span id="wia_dpc_timelapse_interval"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>cameradevicetimelapseinterval</dt> </dl></td>
<td style="text-align: left;"><p>Die Zeitspanne (in Millisekunden) zwischen den Bild Erfassungen in einem Erfassungs Vorgang für einen Zeitablauf.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_NUMBER"></span><span id="wia_dpc_timelapse_number"></span><dl> <dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>cameradevicetimelapsenum</dt> </dl></td>
<td style="text-align: left;"><p>Die Anzahl der Images, die das Gerät während einer Zeitverlust Erfassung versucht.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BURST_INTERVAL"></span><span id="wia_dpc_burst_interval"></span><dl> <dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>cameradeviceburstinterval</dt> </dl></td>
<td style="text-align: left;"><p>Die Zeit (in Millisekunden) zwischen Bild Erfassungen während eines Burst Vorgangs.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_BURST_NUMBER"></span><span id="wia_dpc_burst_number"></span><dl> <dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>cameradeviceburstnumber</dt> </dl></td>
<td style="text-align: left;"><p>Die Anzahl der Images, die das Gerät während eines Burst Vorgangs erfasst.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EFFECT_MODE"></span><span id="wia_dpc_effect_mode"></span><dl> <dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>cameradeviceeffectmode</dt> </dl></td>
<td style="text-align: left;"><p>Gibt den speziellen Bild Erwerbs Modus der Kamera an.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Effekt Modus</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EFFECTMODE_STANDARD</td>
<td>Erfassen eines Bilds im Standardmodus für die Kamera.</td>
</tr>
<tr class="even">
<td>EFFECTMODE_BW</td>
<td>Erfassen eines Graustufen Bilds.</td>
</tr>
<tr class="odd">
<td>EFFECTMODE_SEPIA</td>
<td>Erfassen Sie ein Image vom Typ "*".</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIGITAL_ZOOM"></span><span id="wia_dpc_digital_zoom"></span><dl> <dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>cameradevicedigitalzoom</dt> </dl></td>
<td style="text-align: left;"><p>Das effektive Zoomverhältnis des abgerufenen Images der digitalen Kamera, das um den Faktor 10 skaliert wurde. Der Wert 10 entspricht dem Fehlen des digitalen Zoom (1X), der die von der Kamera erfasste Standard Szenengröße ist. Der Wert 20 entspricht einem 2X-Zoom, bei dem ein Viertel der Standard Szenengröße von der Kamera erfasst wird.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_SHARPNESS"></span><span id="wia_dpc_sharpness"></span><dl> <dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>cameradevicesharpness</dt> </dl></td>
<td style="text-align: left;"><p>Die wahrgenommene Schärfe eines aufgezeichneten Bilds. Diese Eigenschaft kann entweder eine Liste von Werten oder einen Wertebereich verwenden. Der minimale Wert stellt die geringste Menge an Schärfe dar, wohingegen der Höchstwert die maximale Schärfe darstellt. In der Regel stellt ein Wert in der Mitte des Bereichs normale oder standardmäßige Schärfe dar.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CONTRAST"></span><span id="wia_dpc_contrast"></span><dl> <dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>cameradevicecontrast</dt> </dl></td>
<td style="text-align: left;"><p>Der erkannte Kontrast eines aufgezeichneten Bilds. Diese Eigenschaft kann entweder eine Liste mit Werten oder einen Wertebereich enthalten. Der unterstützte Mindestwert stellt den geringsten Kontrast dar, wohingegen der Höchstwert den meisten Kontrast darstellt. In der Regel stellt ein Wert in der Mitte des Bereichs einen normalen oder einen Standard Kontrast dar.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_MODE"></span><span id="wia_dpc_capture_mode"></span><dl> <dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>cameradevicecapturemode</dt> </dl></td>
<td style="text-align: left;"><p>Legt den Bild Erfassungs Modus fest.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Aufzeichnungsmodus</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CAPTUREMODE_NORMAL</td>
<td>Normaler Modus für die Kamera.</td>
</tr>
<tr class="even">
<td>CAPTUREMODE_BURST</td>
<td>Erfassen Sie mehr als ein Bild in schneller Folge, wie in den Werten der Eigenschaften <strong>WIA_DPC_BURST_NUMBER</strong> und <strong>WIA_DPC_BURST_INTERVAL</strong> definiert.</td>
</tr>
<tr class="odd">
<td>CAPTUREMODE_TIMELAPSE</td>
<td>Erfassen Sie mehr als ein Bild nacheinander, wie in den Eigenschaften <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> und <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> definiert.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_DELAY"></span><span id="wia_dpc_capture_delay"></span><dl> <dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>cameradevicecapturedelay</dt> </dl></td>
<td style="text-align: left;"><p>Der-Wert, der die Verzögerung in Millisekunden darstellt, die zwischen dem Erfassungs-und der tatsächlichen Initiierung der Datenerfassung eingefügt werden soll. Diese Eigenschaft ist nicht für die Beschreibung der Zeit zwischen Frames für die Einzel Initiierung gedacht, mehrere Erfassungen, wie z. b. Burst oder Zeitwert, die separate Intervall Eigenschaften <strong>WIA_DPC_BURST_INTERVAL</strong> und <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>haben. In diesen Fällen dient sie immer noch als anfängliche Verzögerung, bevor das erste Bild in der Reihe unabhängig von der Zeit zwischen Frames erfasst wird. Für keine vorab Aufzeichnungs Verzögerung sollte diese Eigenschaft auf 0 (null) festgelegt werden.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_INDEX"></span><span id="wia_dpc_exposure_index"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>cameradeviceexposureindex</dt> </dl></td>
<td style="text-align: left;"><p>Ermöglicht die Emulation von Einstellungen für die Filmgeschwindigkeit auf einer digitalen Kamera. Die Einstellungen entsprechen den ISO-Bezeichnungen (ASA/DIN). In der Regel unterstützt ein Gerät diskrete Enumerationswerte, aber eine kontinuierliche Kontrolle über einen Wertebereich ist möglich. Der Wert 0xFFFF entspricht der automatischen ISO-Einstellung.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_METERING_MODE"></span><span id="wia_dpc_exposure_metering_mode"></span><dl> <dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>cameradeviceexposuremeteringmode</dt> </dl></td>
<td style="text-align: left;"><p>Gibt den Modus an, den die Kamera zum automatischen Anpassen der Einstellung für die Festlegung verwendet.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>

<table>
<thead>
<tr class="header">
<th>Expositions Messungs Modus</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>EXPOSUREMETERING_AVERAGE</td>
<td>Legen Sie die Festlegung auf Grundlage eines Durchschnitts der gesamten Szene fest.</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERWEIGHT</td>
<td>Legen Sie die Verfügbarkeit basierend auf einem Mittel gewichteten Durchschnitt fest.</td>
</tr>
<tr class="odd">
<td>EXPOSUREMETERING_MULTISPOT</td>
<td>Legen Sie die Verfügbarkeit basierend auf einem multiSpot-Muster fest.</td>
</tr>
<tr class="even">
<td>EXPOSUREMETERING_CENTERSPOT</td>
<td>Legen Sie die Verfügbarkeit basierend auf einem Mittelpunkt fest.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING_MODE"></span><span id="wia_dpc_focus_metering_mode"></span><dl> <dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>cameradevicefocemeteringmode</dt> </dl></td>
<td style="text-align: left;"><p>Gibt den Modus an, den die Kamera zum automatischen Anpassen des Fokus verwendet.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Die folgende Tabelle enthält die beiden Konstanten, die mit dieser Eigenschaft gültig sind.</p>

<table>
<thead>
<tr class="header">
<th>Fokus Messungs Modus</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FOCUSMETERING_CENTERSPOT</td>
<td>Passen Sie den Fokus auf der Grundlage eines Mittelpunkts an.</td>
</tr>
<tr class="even">
<td>FOCUSMETERING_MULTISPOT</td>
<td>Passen Sie den Fokus basierend auf einem multiSpot-Muster an.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_DISTANCE"></span><span id="wia_dpc_focus_distance"></span><dl> <dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>cameradevicefocudistance</dt> </dl></td>
<td style="text-align: left;"><p>Der Abstand zwischen der Bild Erfassungs Ebene der digitalen Kamera und dem Punkt des Fokus in Millimeter. Der Wert 0xFFFF entspricht einer Einstellung größer als 655 Meter.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> oder WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCAL_LENGTH"></span><span id="wia_dpc_focal_length"></span><dl> <dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>cameradevicefocallength</dt> </dl></td>
<td style="text-align: left;"><p>Die 35-mm-äquivalente Fokuslänge. Die Werte dieser Eigenschaft entsprechen der Fokuslänge in Millimeter multipliziert mit 100. Die Fokuslänge bestimmt den optischen Zoomfaktor.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_RGB_GAIN"></span><span id="wia_dpc_rgb_gain"></span><dl> <dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>cameradevicergbgewinn</dt> </dl></td>
<td style="text-align: left;"><p>Eine auf NULL endende Unicode-Zeichenfolge, die den roten, grünen und blauen Gewinn darstellt, der auf Bilddaten angewendet wird. &quot;4:25:50 &quot; stellt z. b. einen roten Gewinn von 4, einen grünen Gewinn von 25 und einen blauen Gewinn von 50 dar.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_WHITE_BALANCE"></span><span id="wia_dpc_white_balance"></span><dl> <dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>cameradevicewhitebalance</dt> </dl></td>
<td style="text-align: left;"><p>Gibt an, wie die digitale Kamera Farbkanäle gewichtet.</p>
<p>Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Im folgenden finden Sie eine Liste möglicher Werte für diese Eigenschaft.</p>

<table>
<thead>
<tr class="header">
<th>Weiß Saldo</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WHITEBALANCE_MANUAL</td>
<td>Der weiße Saldo wird direkt mithilfe der <strong>WIA_DPC_RGB_GAIN</strong> -Eigenschaft festgelegt.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_AUTO</td>
<td>Die Kamera verwendet einen automatischen Mechanismus, um den weißen Saldo festzulegen.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_ONEPUSH_AUTO</td>
<td>Die Kamera bestimmt die Einstellung für das weiße Gleichgewicht, wenn ein Benutzer die Erfassungs Schaltfläche drückt, während er auf eine weiße Oberfläche zeigt.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_DAYLIGHT</td>
<td>Die Kamera legt den weißen Saldo auf einen Wert fest, der für die Verwendung in Sommerzeit Bedingungen geeignet ist.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLORESCENT</td>
<td>Die Kamera legt den weißen Saldo auf einen Wert fest, der für die Verwendung mit einer Leuchtstoff Quelle geeignet ist.</td>
</tr>
<tr class="even">
<td>WHITEBALANCE_TUNGSTEN</td>
<td>Die Kamera legt den weißen Saldo auf einen Wert fest, der für die Verwendung mit einer Wolfram-Light-Quelle geeignet ist.</td>
</tr>
<tr class="odd">
<td>WHITEBALANCE_FLASH</td>
<td>Die Kamera legt den weißen Saldo auf einen Wert fest, der für die Verwendung mit einem elektronischen Flash geeignet ist.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_UPLOAD_URL"></span><span id="wia_dpc_upload_url"></span><dl> <dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>cameradeviceuploadurl</dt> </dl></td>
<td style="text-align: left;"><p>Beschreibt eine URL. Die URL, die von diesem Anteils Operator beschrieben wird, ist eine, die Bilder oder Objekte, nachdem Sie vom Gerät abgerufen wurden, nach einem der folgenden Szenarien in – hochgeladen werden können.</p>
<ul>
<li>Eine WIA-Anwendung liest diese Eigenschaft und ermöglicht dem Benutzer das automatische Hochladen von Bildern in die URL.</li>
<li>Eine Anwendung legt die URL fest, und andere Geräte (Kiosk usw.) verwenden diese Eigenschaft.</li>
</ul>
<p>Microsoft Windows lädt Bilder nicht allein hoch.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ARTIST"></span><span id="wia_dpc_artist"></span><dl> <dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>cameradeviceartist</dt> </dl></td>
<td style="text-align: left;"><p>Der Name des Besitzers (der der aktuelle Benutzer ist) des Geräts. Das Gerät verwendet diese Eigenschaft, um das Feld "Artist" in jedem von ihm erfassten EXIF-Bild aufzufüllen.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_COPYRIGHT_INFO"></span><span id="wia_dpc_copyright_info"></span><dl> <dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>cameradevicecopyrightinfo</dt> </dl></td>
<td style="text-align: left;"><p>Die Copyright Benachrichtigung. Das Gerät verwendet diese Eigenschaft, um das Feld "Copyright" in jedem von ihm erfassten Exif-Image aufzufüllen.</p>
<p>Typ: <strong>VT_BSTR</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




