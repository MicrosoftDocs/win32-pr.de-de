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
# <a name="device-properties-portabledeviceh"></a><span data-ttu-id="d2f52-103">Geräteeigenschaften (portabledevice. h)</span><span class="sxs-lookup"><span data-stu-id="d2f52-103">Device Properties (PortableDevice.h)</span></span>

<span data-ttu-id="d2f52-104">Tragbare Windows-Geräte unterstützen die folgenden Geräteeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d2f52-104">Windows Portable Devices supports the following device properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d2f52-105">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="d2f52-105">Property</span></span></th>
<th><span data-ttu-id="d2f52-106">VarType</span><span class="sxs-lookup"><span data-stu-id="d2f52-106">VarType</span></span></th>
<th><span data-ttu-id="d2f52-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d2f52-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d2f52-108"><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-108"><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></span></span></td>
<td><span data-ttu-id="d2f52-109"><strong>VT_DATE</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-109"><strong>VT_DATE</strong></span></span></td>
<td><span data-ttu-id="d2f52-110">Das aktuelle Datum und die Uhrzeit auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="d2f52-110">The current date and time on the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2f52-111"><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-111"><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></span></span></td>
<td><span data-ttu-id="d2f52-112"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-112"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="d2f52-113">Die Firmwareversion des Geräts.</span><span class="sxs-lookup"><span data-stu-id="d2f52-113">The device's firmware version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2f52-114"><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-114"><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="d2f52-115"><strong>VT_VECTOR | VT_UI1</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-115"><strong>VT_VECTOR | VT_UI1</strong></span></span></td>
<td><span data-ttu-id="d2f52-116">Ein eindeutiger 16-Byte-Bezeichner, der auf mehreren vom Gerät unterstützten Transporten gemeinsam ist.</span><span class="sxs-lookup"><span data-stu-id="d2f52-116">A unique 16-byte identifier that is common across multiple transports supported by the device.</span></span> <span data-ttu-id="d2f52-117">Wenn ein einzelnes Gerät mehrere Transporte unterstützt, kann diese Eigenschaft verwendet werden, um die verschiedenen Transport-WPD-Treiber diesem Gerät zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="d2f52-117">If a single device supports multiple transports, this property may be used to associate the various transport WPD drivers with that device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2f52-118"><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-118"><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></span></span></td>
<td><span data-ttu-id="d2f52-119"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-119"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="d2f52-120">Ein lesbarer Gerätehersteller Name.</span><span class="sxs-lookup"><span data-stu-id="d2f52-120">A human-readable device manufacturer name.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2f52-121"><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-121"><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></span></span></td>
<td><span data-ttu-id="d2f52-122"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-122"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="d2f52-123">Das Gerätemodell.</span><span class="sxs-lookup"><span data-stu-id="d2f52-123">The device model.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2f52-124"><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-124"><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="d2f52-125"><strong>VT_VECTOR | VT_UI1</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-125"><strong>VT_VECTOR | VT_UI1</strong></span></span></td>
<td><span data-ttu-id="d2f52-126">Ein eindeutiger 16-Byte-Bezeichner, der zur Unterscheidung zwischen verschiedenen Modellen eines Geräts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d2f52-126">A unique 16-byte identifier used to differentiate among different models of a device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2f52-127"><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-127"><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></span></span></td>
<td><span data-ttu-id="d2f52-128"><strong>VT_UI8</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-128"><strong>VT_UI8</strong></span></span></td>
<td><span data-ttu-id="d2f52-129">Ein-Wert, der die EUI-64-Netzwerk Kennung des Geräts angibt. Diese Eigenschaft wird für Out-of-Band-Netzwerk Vorgänge verwendet. Wenn das Gerät über Mac-48 physische Netzwerkadressen (typisch für IPv4-Netzwerke) verfügt, wird die Mac-48-Adresse in der EUI-64-Adresse als die zwei Hälften der Mac-48-Adresse durch eine FF-FF-Trennung codiert.</span><span class="sxs-lookup"><span data-stu-id="d2f52-129">A value that specifies the EUI-64 network identifier of the device; this property is used for out-of-band network operations.If the device has MAC-48 physical network addresses (typical of IPv4 networks), the MAC-48 address is encoded in the EUI-64 address as the two halves of the MAC-48 address separated by FF-FF.</span></span> <span data-ttu-id="d2f52-130">Der EUI-64-Wert wird in &quot; &quot; der Netzwerk &quot; -oder Big- &quot; in-Reihenfolge gespeichert, in der die EUI-64-Adresse 01-02-03-FF-FF-04-05-06 in der VT_UI8 platziert wird, sodass der Dezimalwert 72624942021346566 ist.</span><span class="sxs-lookup"><span data-stu-id="d2f52-130">The EUI-64 value is stored in &quot;network&quot; or &quot;big-endian&quot; order, where an EUI-64 address of 01-02-03-FF-FF-04-05-06 would be placed in the VT_UI8 such that the decimal value is 72624942021346566.</span></span> <span data-ttu-id="d2f52-131">Diese Eigenschaft ist auf jedem Gerät erforderlich, das eine nominale oder sichere Authentifizierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2f52-131">This property is required on any device that supports Nominal or Secure Authentication.</span></span> <span data-ttu-id="d2f52-132">Diese Eigenschaft wird auf Geräten empfohlen, die nur die Authentifizierung 0 (null) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d2f52-132">This property is recommended on devices that support only Zero Authentication.</span></span> <span data-ttu-id="d2f52-133">Der-Wert kann vom Host verwendet werden, um ohne Benutzereingriff automatisch Zugriff auf das Gerät einzurichten.</span><span class="sxs-lookup"><span data-stu-id="d2f52-133">The value can be used by the host to automatically establish access to the device without user intervention.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2f52-134"><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-134"><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></span></span></td>
<td><span data-ttu-id="d2f52-135"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-135"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="d2f52-136">Ein Wert zwischen 0 und 100, der die Stromversorgung des Geräts des Geräts angibt, wobei 0 keine ist und 100 vollständig in Rechnung gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d2f52-136">A value from 0 to 100 that specifies the power level of the device's battery, with 0 being none, and 100 being fully charged.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2f52-137"><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-137"><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></span></span></td>
<td><span data-ttu-id="d2f52-138">VT_UI4</span><span class="sxs-lookup"><span data-stu-id="d2f52-138">VT_UI4</span></span></td>
<td><span data-ttu-id="d2f52-139">Eine <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> -Enumeration, die die Stromquelle des Geräts angibt.</span><span class="sxs-lookup"><span data-stu-id="d2f52-139">A <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> enumeration that specifies the power source of the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2f52-140"><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-140"><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></span></span></td>
<td><span data-ttu-id="d2f52-141"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-141"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="d2f52-142">Das verwendete Geräte Protokoll.</span><span class="sxs-lookup"><span data-stu-id="d2f52-142">The device protocol that is being used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2f52-143"><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-143"><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></span></span></td>
<td><span data-ttu-id="d2f52-144"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-144"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="d2f52-145">Die Seriennummer des Geräts.</span><span class="sxs-lookup"><span data-stu-id="d2f52-145">The device's serial number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2f52-146"><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-146"><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></span></span></td>
<td><span data-ttu-id="d2f52-147"><strong>VT_UNKNOWN</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-147"><strong>VT_UNKNOWN</strong></span></span></td>
<td><span data-ttu-id="d2f52-148">Ein-Wert, der angibt, ob die vom Gerät zurückgegebenen unterstützten Formate in einer bevorzugten Reihenfolge vorliegen.</span><span class="sxs-lookup"><span data-stu-id="d2f52-148">A value that specifies whether the supported formats returned from the device are in a preferred order.</span></span> <span data-ttu-id="d2f52-149">Das erste Format in der Liste wird am häufigsten vom Gerät bevorzugt, während das letzte der am wenigsten bevorzugte ist. Anwendungen können diese Eigenschaft verwenden, um zu bestimmen, ob die unterstützten Formate eines Geräts in einer bevorzugten Reihenfolge aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="d2f52-149">The first format in the list is most preferred by the device, while the last is the least preferred.Applications may use this property to determine whether a device's supported formats are listed in a preferred order.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2f52-150"><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-150"><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></span></span></td>
<td><span data-ttu-id="d2f52-151"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-151"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="d2f52-152">Ein boolescher Wert, der angibt, ob die vom Gerät zurückgegebenen unterstützten Formate in einer bevorzugten Reihenfolge vorliegen. Das heißt, das erste zurückgegebene Format wird bevorzugt, während das letzte zurückgegebene Format am wenigsten bevorzugt wird.</span><span class="sxs-lookup"><span data-stu-id="d2f52-152">A Boolean value that specifies whether the supported formats returned from the device are in a preferred order; that is, the first returned format is most preferred while the last returned format is least preferred.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2f52-153"><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-153"><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></span></span></td>
<td><span data-ttu-id="d2f52-154"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-154"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="d2f52-155">Ein boolescher Wert, der angibt, ob das Gerät nicht verwendbare Objekte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d2f52-155">A Boolean value that specifies whether the device supports non-consumable objects.</span></span> <span data-ttu-id="d2f52-156">Dabei handelt es sich um Objekte, die auf dem Gerät nur gespeichert, nicht wiedergegeben oder verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d2f52-156">These are objects that the device is only meant to store, not play or use in any way.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2f52-157"><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-157"><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></span></span></td>
<td><span data-ttu-id="d2f52-158"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-158"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="d2f52-159">Eine lesbare Beschreibung des <em>Synchronisierungs Partners</em>eines Geräts.</span><span class="sxs-lookup"><span data-stu-id="d2f52-159">A human-readable description of a device's <em>synchronization partner</em>.</span></span> <span data-ttu-id="d2f52-160">Hierbei handelt es sich um ein Gerät, eine Anwendung oder einen Server, mit dem das Gerät kommuniziert, um einen gemeinsamen Status oder eine Gruppe von Dateien zwischen beiden Partnern beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="d2f52-160">This is a device, application, or server that the device communicates with to maintain a common state or group of files between both partners.</span></span> <span data-ttu-id="d2f52-161">Beispiele hierfür sind e-Mail-Programme und Musikbibliotheken.</span><span class="sxs-lookup"><span data-stu-id="d2f52-161">Examples include e-mail programs and music libraries.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2f52-162"><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-162"><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></span></span></td>
<td><span data-ttu-id="d2f52-163"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-163"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="d2f52-164">Ein-Wert, der den anzeigen Amen darstellt, der vom Benutzer auf dem Gerät festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d2f52-164">A value that represents the friendly name set by the user on the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2f52-165"><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-165"><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></span></span></td>
<td><span data-ttu-id="d2f52-166"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-166"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="d2f52-167">der vom Gerät unterstützte Transport, z. b. USB, IP oder Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="d2f52-167">the transport supported by the device, such as USB, IP, or Bluetooth.</span></span> <span data-ttu-id="d2f52-168">Gültige Werte sind vom <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> Enumerationstyp.</span><span class="sxs-lookup"><span data-stu-id="d2f52-168">Valid values are of the <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> enumeration type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d2f52-169"><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-169"><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></span></span></td>
<td><span data-ttu-id="d2f52-170"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-170"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="d2f52-171">Ein-Wert, der den Gerätetyp angibt. Anwendungen verwenden diese Eigenschaft nur zu Darstellungs Zwecken.</span><span class="sxs-lookup"><span data-stu-id="d2f52-171">A value that specifies the device type; applications use this property for representation purposes only.</span></span> <span data-ttu-id="d2f52-172">Funktionale Merkmale des Geräts werden durch funktionale Objekte festgelegt. Geräte, die kein Gerätesymbol bereitstellen (z. b. eine <strong>WPD_RESOURCE_ICON</strong> für das Geräte Objekt), werden im WPD-Namespace mit einem generischen Symbol dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d2f52-172">Functional characteristics of the device are decided through functional objects.Devices that do not supply a device icon, for example, a <strong>WPD_RESOURCE_ICON</strong> for the device object, will be represented in the WPD Namespace with a generic icon.</span></span> <span data-ttu-id="d2f52-173">Dieses Symbol hängt vom angegebenen Gerätetyp ab, z. b. wenn es sich bei dem Gerätetyp um ein Mobiltelefon handelt, wird das Symbol für das generische Telefon verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2f52-173">This icon will depend on the specified device type, for example, if the device type is a mobile phone, the generic phone icon is used.</span></span> <span data-ttu-id="d2f52-174">Bei der Erstinstallation des Geräts wird dieser Eigenschafts Wert vom Installationsprogramm der WPD-Klasse abgefragt und in der Geräteregistrierung unter dem PORTABLE_DEVICE_TYPE Wert als REG_DWORD gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d2f52-174">On first install of the device, the WPD Class Installer will query this property value and store it in the device registry under the PORTABLE_DEVICE_TYPE value as a REG_DWORD.</span></span><br/> <span data-ttu-id="d2f52-175">Die möglichen Werte dieses Parameters stammen aus der in portabledevice. h definierten <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> Enumeration.</span><span class="sxs-lookup"><span data-stu-id="d2f52-175">This parameter's possible values are from the <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> enumeration defined in PortableDevice.h.</span></span> <span data-ttu-id="d2f52-176">Gültige Werte:</span><span class="sxs-lookup"><span data-stu-id="d2f52-176">Values are:</span></span><br/> <dl> <span data-ttu-id="d2f52-177"><strong>WPD_DEVICE_TYPE_GENERIC</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-177"><strong>WPD_DEVICE_TYPE_GENERIC</strong></span></span><br /><span data-ttu-id="d2f52-178">
<strong>WPD_DEVICE_TYPE_CAMERA</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-178">
<strong>WPD_DEVICE_TYPE_CAMERA</strong></span></span><br /><span data-ttu-id="d2f52-179">
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-179">
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong></span></span><br /><span data-ttu-id="d2f52-180">
<strong>WPD_DEVICE_TYPE_PHONE</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-180">
<strong>WPD_DEVICE_TYPE_PHONE</strong></span></span><br /><span data-ttu-id="d2f52-181">
<strong>WPD_DEVICE_TYPE_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-181">
<strong>WPD_DEVICE_TYPE_VIDEO</strong></span></span><br /><span data-ttu-id="d2f52-182">
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-182">
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong></span></span><br /><span data-ttu-id="d2f52-183">
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-183">
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d2f52-184"><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-184"><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></span></span></td>
<td><span data-ttu-id="d2f52-185"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="d2f52-185"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="d2f52-186">Wenn diese Eigenschaft vorhanden und auf <strong>true</strong>festgelegt ist, kann das Gerät mit der Geräte Stufe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d2f52-186">If this property exists and is set to <strong>TRUE</strong>, the device can be used with Device Stage .</span></span> <span data-ttu-id="d2f52-187">Dies ist für Geräte gedacht, die Metadaten nicht mithilfe des <strong>Geräte Metadata Service</strong>speichern können, sondern Metadaten auf den Microsoft-Servern bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d2f52-187">This is meant for devices that cannot store metadata using the <strong>Device Metadata Service</strong>, but will provide metadata on the Microsoft servers.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="d2f52-188">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2f52-188">Requirements</span></span>



| <span data-ttu-id="d2f52-189">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2f52-189">Requirement</span></span> | <span data-ttu-id="d2f52-190">Wert</span><span class="sxs-lookup"><span data-stu-id="d2f52-190">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2f52-191">Header</span><span class="sxs-lookup"><span data-stu-id="d2f52-191">Header</span></span><br/> | <dl> <span data-ttu-id="d2f52-192"><dt>Portabledevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2f52-192"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2f52-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2f52-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2f52-194">**WPD-Eigenschaften und-Attribute**</span><span class="sxs-lookup"><span data-stu-id="d2f52-194">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




