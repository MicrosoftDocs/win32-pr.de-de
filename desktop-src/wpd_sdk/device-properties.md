---
description: Windows Portable Geräte unterstützen die folgenden Geräteeigenschaften.
ms.assetid: 1caf4c1a-ceb6-4aa5-b430-df01c9fb22ce
title: Geräteeigenschaften (PortableDevice.h)
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
ms.openlocfilehash: 5490323e60d353fade6dfb7f517533ecb5fa26ca9e78ae221b9ff584d8c13a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430979"
---
# <a name="device-properties-portabledeviceh"></a>Geräteeigenschaften (PortableDevice.h)

Windows Portable Geräte unterstützen die folgenden Geräteeigenschaften.



<table>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>VarType</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></td>
<td><strong>VT_DATE</strong></td>
<td>Das aktuelle Datum und die aktuelle Uhrzeit auf dem Gerät.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Die Firmwareversion des Geräts.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></td>
<td><strong>VT_VECTOR | VT_UI1</strong></td>
<td>Ein eindeutiger 16-Byte-Bezeichner, der für mehrere vom Gerät unterstützte Transporte verwendet wird. Wenn ein einzelnes Gerät mehrere Transporte unterstützt, kann diese Eigenschaft verwendet werden, um die verschiedenen WPD-Transporttreiber diesem Gerät zu zuordnen.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Ein für Menschen lesbarer Geräteherstellername.</td>
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
<td>Ein -Wert, der den EUI-64-Netzwerkbezeichner des Geräts angibt. diese Eigenschaft wird für Out-of-Band-Netzwerkvorgänge verwendet. Wenn das Gerät über physische MAC-48-Netzwerkadressen verfügt (typisch für IPv4-Netzwerke), wird die MAC-48-Adresse in der EUI-64-Adresse als die beiden Hälften der MAC-48-Adresse codiert, die durch FF-FF getrennt sind. Der EUI-64-Wert wird in netzwerk- oder &quot; &quot; &quot; big-endian-Reihenfolge gespeichert, wobei eine &quot; EUI-64-Adresse von 01-02-03-FF-FF-04-05-06 im VT_UI8 platziert wird, damit der Dezimalwert 72624942021346566. Diese Eigenschaft ist auf jedem Gerät erforderlich, das nominale oder sichere Authentifizierung unterstützt. Diese Eigenschaft wird auf Geräten empfohlen, die nur die Nullauthentifizierung unterstützen. Der Wert kann vom Host verwendet werden, um den Zugriff auf das Gerät ohne Benutzereingriff automatisch zu erstellen.<br/></td>
</tr>
<tr class="even">
<td><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Ein Wert zwischen 0 und 100, der den Akkustand des Geräts angibt, bei dem 0 kein Wert ist und 100 vollständig aufgeladen ist.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></td>
<td>VT_UI4</td>
<td>Eine <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> Enumeration, die die Stromquelle des Geräts angibt.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Das verwendete Geräteprotokoll.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Die Seriennummer des Geräts.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></td>
<td><strong>VT_UNKNOWN</strong></td>
<td>Ein -Wert, der angibt, ob die vom Gerät zurückgegebenen unterstützten Formate in einer bevorzugten Reihenfolge vorliegen. Das erste Format in der Liste wird vom Gerät am meisten bevorzugt, während das letzte das am wenigsten bevorzugte Format ist. Anwendungen können diese Eigenschaft verwenden, um zu bestimmen, ob die unterstützten Formate eines Geräts in einer bevorzugten Reihenfolge aufgeführt werden.<br/></td>
</tr>
<tr class="odd">
<td><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Ein boolescher Wert, der angibt, ob die vom Gerät zurückgegebenen unterstützten Formate in einer bevorzugten Reihenfolge vorliegen. Das heißt, das erste zurückgegebene Format wird am meisten bevorzugt, während das zuletzt zurückgegebene Format am wenigsten bevorzugt wird.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Ein boolescher Wert, der angibt, ob das Gerät nicht verwertbare Objekte unterstützt. Dabei handelt es sich um Objekte, die das Gerät nur speichern, nicht wiederspielen oder in irgendeiner Weise verwenden soll.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Eine lesbare Beschreibung des Synchronisierungspartners <em>eines Geräts.</em> Dies ist ein Gerät, eine Anwendung oder ein Server, mit dem das Gerät kommuniziert, um einen gemeinsamen Zustand oder eine Gruppe von Dateien zwischen beiden Partnern zu verwalten. Beispiele hierfür sind E-Mail-Programme und Musikbibliotheken.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Ein -Wert, der den vom Benutzer auf dem Gerät festgelegten Benutzernamen darstellt.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></td>
<td><strong>VT_UI4</strong></td>
<td>der vom Gerät unterstützte Transport, z. B. USB, IP oder Bluetooth. Gültige Werte sind vom <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> Enumerationstyp.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Ein -Wert, der den Gerätetyp angibt. -Anwendungen verwenden diese Eigenschaft nur zu Darstellungszwecken. Funktionale Merkmale des Geräts werden durch funktionale Objekte entschieden. Geräte, die kein Gerätesymbol angeben, <strong></strong> z. B. eine WPD_RESOURCE_ICON für das Geräteobjekt, werden im WPD-Namespace mit einem generischen Symbol dargestellt. Dieses Symbol hängt vom angegebenen Gerätetyp ab. Wenn der Gerätetyp beispielsweise ein Mobiltelefon ist, wird das generische Telefonsymbol verwendet. Bei der ersten Installation des Geräts wird dieser Eigenschaftswert vom WPD-Klasseninstaller abfragen und in der Geräteregistrierung unter dem wert PORTABLE_DEVICE_TYPE als REG_DWORD.<br/> Die möglichen Werte dieses Parameters <a href="object-properties.md"><strong></strong></a> sind aus der WPD_DEVICE_TYPES Enumeration, die in PortableDevice.h definiert ist. Gültige Werte:<br/> <dl> <strong>WPD_DEVICE_TYPE_GENERIC</strong><br />
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
<td>Wenn diese Eigenschaft vorhanden ist und auf <strong>TRUE festgelegt</strong>ist, kann das Gerät mit der Device Stage. Dies ist für Geräte gedacht, die keine Metadaten mithilfe des Device Metadata Service speichern <strong>können,</strong>aber Metadaten auf den Microsoft-Servern bereitstellen.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WPD-Eigenschaften und -Attribute**](properties-and-attributes.md)
</dt> </dl>

 

 




