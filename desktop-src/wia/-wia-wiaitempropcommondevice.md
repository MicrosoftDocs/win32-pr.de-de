---
description: Zusätzlich zu den Eigenschaften von Geräteinformationen verfügen Windows-Abbild Erfassungsgeräte (WIA) über Eigenschaftswerte, die in der Registrierung gespeichert sind und von Anwendungen gelesen und geschrieben werden.
ms.assetid: 9948318b-7171-45fa-b46f-48f9357fdb32
title: Allgemeine Geräte Eigenschafts Konstanten (wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPA_CONNECT_STATUS
- WIA_DPA_DEVICE_TIME
- WIA_DPA_FIRMWARE_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 23c8faf8317fa7bf2008baffe3e6bf0e89a27a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526399"
---
# <a name="common-device-property-constants"></a><span data-ttu-id="edc77-103">Allgemeine Geräte Eigenschafts Konstanten</span><span class="sxs-lookup"><span data-stu-id="edc77-103">Common Device Property Constants</span></span>

<span data-ttu-id="edc77-104">Zusätzlich zu den Eigenschaften von Geräteinformationen verfügen Windows-Abbild Erfassungsgeräte (WIA) über Eigenschaftswerte, die in der Registrierung gespeichert sind und von Anwendungen gelesen und geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="edc77-104">In addition to device information properties, Windows Image Acquisition (WIA) devices have property values stored in the registry that applications read and write.</span></span> <span data-ttu-id="edc77-105">Sie sind dem [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Objekt oder dem [**IWiaItem2**](-wia-iwiaitem2.md) -Objekt zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="edc77-105">They are associated with the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object or [**IWiaItem2**](-wia-iwiaitem2.md) object.</span></span> <span data-ttu-id="edc77-106">Geräteeigenschaften stellen Geräteinformationen dar, z. b. Verbindungsstatus und Geräte Zeit.</span><span class="sxs-lookup"><span data-stu-id="edc77-106">Device properties represent device information such as connection status and device time.</span></span> <span data-ttu-id="edc77-107">Jede Geräte Eigenschaft verfügt über eine zugeordnete Geräteeigenschaften Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="edc77-107">Each device property has an associated device property string.</span></span>

<span data-ttu-id="edc77-108">Die hier aufgeführten Geräteeigenschaften Konstanten gelten für die meisten oder alle WIA-Hardware Geräte.</span><span class="sxs-lookup"><span data-stu-id="edc77-108">The Device Property Constants listed here are common to most or all WIA hardware devices.</span></span>

<span data-ttu-id="edc77-109">Das Präfix "WIA \_ DPA \_ " gibt eine Geräte Eigenschaft für alle Geräte an und ist die Benennungs Konvention, die in C/C++ verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="edc77-109">The prefix "WIA\_DPA\_" indicates a Device Property for All devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="edc77-110">Bei der Skripterstellung verwenden diese Konstanten das Präfix "Device" und sind Teil des enumerierten Typs [wiaitempropertyid](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="edc77-110">For scripting purposes these constants use the prefix "Device" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="edc77-111">Der entsprechende Elementname aus dieser Skript Enumeration wird in Klammern neben dem Konstanten Namen C/C++ in der folgenden Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="edc77-111">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="edc77-112">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="edc77-112">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="edc77-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="edc77-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_CONNECT_STATUS"></span><span id="wia_dpa_connect_status"></span><dl> <span data-ttu-id="edc77-114"><dt><strong></strong></dt> <dt>Deviceconnectstatus</dt> WIA_DPA_CONNECT_STATUS </span><span class="sxs-lookup"><span data-stu-id="edc77-114"><dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="edc77-115">Der aktuelle Verbindungsstatus für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="edc77-115">The current connection status for the device.</span></span> <span data-ttu-id="edc77-116">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="edc77-116">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="edc77-117">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="edc77-117">Type: <strong>VT_I4</strong>, Access: Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="edc77-118">Die-Eigenschaft kann die folgenden möglichen Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="edc77-118">The property can have the following possible values.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="edc77-119">Verbindungs Status</span><span class="sxs-lookup"><span data-stu-id="edc77-119">Connect Status</span></span></th>
<th><span data-ttu-id="edc77-120">Definition</span><span class="sxs-lookup"><span data-stu-id="edc77-120">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="edc77-121">WIA_DEVICE_NOT_CONNECTED</span><span class="sxs-lookup"><span data-stu-id="edc77-121">WIA_DEVICE_NOT_CONNECTED</span></span></td>
<td><span data-ttu-id="edc77-122">Das Gerät ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="edc77-122">Device is not connected.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edc77-123">WIA_DEVICE_CONNECTED</span><span class="sxs-lookup"><span data-stu-id="edc77-123">WIA_DEVICE_CONNECTED</span></span></td>
<td><span data-ttu-id="edc77-124">Das Gerät ist verbunden und betriebsbereit.</span><span class="sxs-lookup"><span data-stu-id="edc77-124">Device is connected and operational.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPA_DEVICE_TIME"></span><span id="wia_dpa_device_time"></span><dl> <span data-ttu-id="edc77-125"><dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>devicedevicetime</dt> </span><span class="sxs-lookup"><span data-stu-id="edc77-125"><dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="edc77-126">Die aktuelle Uhrzeit, die auf dem Gerät gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="edc77-126">The current clock time that is stored on the device.</span></span> <span data-ttu-id="edc77-127">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="edc77-127">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="edc77-128">Typ: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>, Zugriff: Lese-/Schreibzugriff oder schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="edc77-128">Type: <strong>VT_UI2</strong> | <strong>VT_VECTOR</strong>, Access: Read/Write or Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="edc77-129">Diese Eigenschaft wird nur von Geräten mit einer internen Uhr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="edc77-129">This property is supported only by devices that have an internal clock.</span></span> <span data-ttu-id="edc77-130">Wenn die Geräteuhr festgelegt werden kann, lautet diese Eigenschaft Lese-/Schreibzugriff. Andernfalls ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="edc77-130">If the device clock can be set, this property is Read/Write; otherwise, it is Read-only.</span></span></p>
<p><span data-ttu-id="edc77-131">WIA-Geräte melden Zeit in einer <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="edc77-131">WIA devices report time in a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_FIRMWARE_VERSION"></span><span id="wia_dpa_firmware_version"></span><dl> <span data-ttu-id="edc77-132"><dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>devicefirmwareversion</dt> </span><span class="sxs-lookup"><span data-stu-id="edc77-132"><dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="edc77-133">Die Firmwareversion des Geräts.</span><span class="sxs-lookup"><span data-stu-id="edc77-133">The device firmware version.</span></span> <span data-ttu-id="edc77-134">Dieser Wert muss ein Zeichen folgen Wert sein, z &quot; &quot; . b. 1.0.4 oder &quot; 1.0 ABC &quot; .</span><span class="sxs-lookup"><span data-stu-id="edc77-134">This value must be a string value, such as &quot;1.0.4&quot; or &quot;1.0abc&quot;.</span></span> <span data-ttu-id="edc77-135">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="edc77-135">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="edc77-136">Wenn der WIA-Mini Treiber keine Versions Ressource bereitstellt, liefert der WIA-Dienst den Wert &quot; 0.0.0.0 &quot; als Standardwert.</span><span class="sxs-lookup"><span data-stu-id="edc77-136">If the WIA minidriver does not supply a version resource, the WIA service supplies the value &quot;0.0.0.0&quot; as a default.</span></span> <span data-ttu-id="edc77-137">Eine Anwendung liest diese Eigenschaft, um die Version der WIA Mini Treiber-DLL zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="edc77-137">An application reads this property to determine the version of the WIA minidriver DLL.</span></span></p>
<p><span data-ttu-id="edc77-138">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="edc77-138">Type: <strong>VT_BSTR</strong>, Access: Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="edc77-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="edc77-139">Requirements</span></span>



| <span data-ttu-id="edc77-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="edc77-140">Requirement</span></span> | <span data-ttu-id="edc77-141">Wert</span><span class="sxs-lookup"><span data-stu-id="edc77-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="edc77-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="edc77-142">Minimum supported client</span></span><br/> | <span data-ttu-id="edc77-143">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="edc77-143">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="edc77-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="edc77-144">Minimum supported server</span></span><br/> | <span data-ttu-id="edc77-145">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="edc77-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="edc77-146">Header</span><span class="sxs-lookup"><span data-stu-id="edc77-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="edc77-147"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="edc77-147"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
