---
description: Tragbare Windows-Geräte unterstützen die folgenden Geräteeigenschaften.
ms.assetid: 1caf4c1a-ceb6-4aa5-b430-df01c9fb22ce
title: Geräteeigenschaften (portabledevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Device
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 696d5fefd65d194f9bb451b0095ed87b90f8a22c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371153"
---
# <a name="device-properties-portabledeviceh"></a>Geräteeigenschaften (portabledevice. h)

Tragbare Windows-Geräte unterstützen die folgenden Geräteeigenschaften.



<table>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>VarType</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></td>
<td><strong>VT_DATE</strong></td>
<td>Das aktuelle Datum und die Uhrzeit auf dem Gerät.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Die Firmwareversion des Geräts.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></td>
<td><strong>VT_VECTOR | VT_UI1</strong></td>
<td>Ein eindeutiger 16-Byte-Bezeichner, der auf mehreren vom Gerät unterstützten Transporten gemeinsam ist. Wenn ein einzelnes Gerät mehrere Transporte unterstützt, kann diese Eigenschaft verwendet werden, um die verschiedenen Transport-WPD-Treiber diesem Gerät zuzuordnen.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Ein lesbarer Gerätehersteller Name.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Das Gerätemodell.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></td>
<td><strong>VT_VECTOR | VT_UI1</strong></td>
<td>Ein eindeutiger 16-Byte-Bezeichner, der zur Unterscheidung zwischen verschiedenen Modellen eines Geräts verwendet wird.</td>
</tr>
<tr class="odd">
<td><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></td>
<td><strong>VT_UI8</strong></td>
<td>Ein-Wert, der die EUI-64-Netzwerk Kennung des Geräts angibt. Diese Eigenschaft wird für Out-of-Band-Netzwerk Vorgänge verwendet. Wenn das Gerät über Mac-48 physische Netzwerkadressen (typisch für IPv4-Netzwerke) verfügt, wird die Mac-48-Adresse in der EUI-64-Adresse als die zwei Hälften der Mac-48-Adresse durch eine FF-FF-Trennung codiert. Der EUI-64-Wert wird in &quot; &quot; der Netzwerk &quot; -oder Big- &quot; in-Reihenfolge gespeichert, in der die EUI-64-Adresse 01-02-03-FF-FF-04-05-06 in der VT_UI8 platziert wird, sodass der Dezimalwert 72624942021346566 ist. Diese Eigenschaft ist auf jedem Gerät erforderlich, das eine nominale oder sichere Authentifizierung unterstützt. Diese Eigenschaft wird auf Geräten empfohlen, die nur die Authentifizierung 0 (null) unterstützen. Der-Wert kann vom Host verwendet werden, um ohne Benutzereingriff automatisch Zugriff auf das Gerät einzurichten.<br/></td>
</tr>
<tr class="even">
<td><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Ein Wert zwischen 0 und 100, der die Stromversorgung des Geräts des Geräts angibt, wobei 0 keine ist und 100 vollständig in Rechnung gestellt wird.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></td>
<td>VT_UI4</td>
<td>Eine <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> -Enumeration, die die Stromquelle des Geräts angibt.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Das verwendete Geräte Protokoll.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Die Seriennummer des Geräts.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></td>
<td><strong>VT_UNKNOWN</strong></td>
<td>Ein-Wert, der angibt, ob die vom Gerät zurückgegebenen unterstützten Formate in einer bevorzugten Reihenfolge vorliegen. Das erste Format in der Liste wird am häufigsten vom Gerät bevorzugt, während das letzte der am wenigsten bevorzugte ist. Anwendungen können diese Eigenschaft verwenden, um zu bestimmen, ob die unterstützten Formate eines Geräts in einer bevorzugten Reihenfolge aufgelistet werden.<br/></td>
</tr>
<tr class="odd">
<td><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Ein boolescher Wert, der angibt, ob die vom Gerät zurückgegebenen unterstützten Formate in einer bevorzugten Reihenfolge vorliegen. Das heißt, das erste zurückgegebene Format wird bevorzugt, während das letzte zurückgegebene Format am wenigsten bevorzugt wird.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Ein boolescher Wert, der angibt, ob das Gerät nicht verwendbare Objekte unterstützt. Dabei handelt es sich um Objekte, die auf dem Gerät nur gespeichert, nicht wiedergegeben oder verwendet werden sollen.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Eine lesbare Beschreibung des <em>Synchronisierungs Partners</em>eines Geräts. Hierbei handelt es sich um ein Gerät, eine Anwendung oder einen Server, mit dem das Gerät kommuniziert, um einen gemeinsamen Status oder eine Gruppe von Dateien zwischen beiden Partnern beizubehalten. Beispiele hierfür sind e-Mail-Programme und Musikbibliotheken.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Ein-Wert, der den anzeigen Amen darstellt, der vom Benutzer auf dem Gerät festgelegt wird.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></td>
<td><strong>VT_UI4</strong></td>
<td>der vom Gerät unterstützte Transport, z. b. USB, IP oder Bluetooth. Gültige Werte sind vom <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> Enumerationstyp.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Ein-Wert, der den Gerätetyp angibt. Anwendungen verwenden diese Eigenschaft nur zu Darstellungs Zwecken. Funktionale Merkmale des Geräts werden durch funktionale Objekte festgelegt. Geräte, die kein Gerätesymbol bereitstellen (z. b. eine <strong>WPD_RESOURCE_ICON</strong> für das Geräte Objekt), werden im WPD-Namespace mit einem generischen Symbol dargestellt. Dieses Symbol hängt vom angegebenen Gerätetyp ab, z. b. wenn es sich bei dem Gerätetyp um ein Mobiltelefon handelt, wird das Symbol für das generische Telefon verwendet. Bei der Erstinstallation des Geräts wird dieser Eigenschafts Wert vom Installationsprogramm der WPD-Klasse abgefragt und in der Geräteregistrierung unter dem PORTABLE_DEVICE_TYPE Wert als REG_DWORD gespeichert.<br/> Die möglichen Werte dieses Parameters stammen aus der in portabledevice. h definierten <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> Enumeration. Gültige Werte:<br/> <dl> <strong>WPD_DEVICE_TYPE_GENERIC</strong><br />
<strong>WPD_DEVICE_TYPE_CAMERA</strong><br />
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong><br />
<strong>WPD_DEVICE_TYPE_PHONE</strong><br />
<strong>WPD_DEVICE_TYPE_VIDEO</strong><br />
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong><br />
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Wenn diese Eigenschaft vorhanden und auf <strong>true</strong>festgelegt ist, kann das Gerät mit der Geräte Stufe verwendet werden. Dies ist für Geräte gedacht, die Metadaten nicht mithilfe des <strong>Geräte Metadata Service</strong>speichern können, sondern Metadaten auf den Microsoft-Servern bereitstellen.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Portabledevice. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und-Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




