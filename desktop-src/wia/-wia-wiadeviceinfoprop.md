---
description: 'Eigenschaftenkonstanten für Geräteinformationen: Geräteinformationseigenschaften sind Eigenschaften, die das Setup und die Installation des Geräts beschreiben.'
ms.assetid: ff6771ac-491e-4765-8cfe-11c7efc1c971
title: Eigenschaftenkonstanten für Geräteinformationen (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DIP_DEV_ID
- WIA_DIP_VEND_DESC
- WIA_DIP_DEV_DESC
- WIA_DIP_DEV_TYPE
- WIA_DIP_PORT_NAME
- WIA_DIP_DEV_NAME
- WIA_DIP_SERVER_NAME
- WIA_DIP_REMOTE_DEV_ID
- WIA_DIP_UI_CLSID
- WIA_DIP_HW_CONFIG
- WIA_DIP_BAUDRATE
- WIA_DIP_STI_GEN_CAPABILITIES
- WIA_DIP_WIA_VERSION
- WIA_DIP_DRIVER_VERSION
- WIA_DIP_PNP_ID
- WIA_DIP_STI_DRIVER_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: aec37ae84eed6b15bc10a4e979a5d95d21be3423
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097238"
---
# <a name="device-information-property-constants"></a><span data-ttu-id="464f3-103">Eigenschaftenkonstanten für Geräteinformationen</span><span class="sxs-lookup"><span data-stu-id="464f3-103">Device Information Property Constants</span></span>

<span data-ttu-id="464f3-104">Geräteinformationseigenschaften sind Eigenschaften, die das Setup und die Installation des Geräts beschreiben.</span><span class="sxs-lookup"><span data-stu-id="464f3-104">Device Information Properties are properties that describe the setup and installation of the device.</span></span> <span data-ttu-id="464f3-105">Diese Eigenschaften sind über die [**Schnittstellen IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) oder [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) und auch über das Stammelement verfügbar.</span><span class="sxs-lookup"><span data-stu-id="464f3-105">These properties are available through the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interfaces and also through the root item.</span></span> <span data-ttu-id="464f3-106">Geräteinformationseigenschaften haben das Präfix "WIA \_ \_ DIP" (Device Information Property) und werden von Windows Image Acquisition (WIA) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="464f3-106">Device information properties are prefixed with "WIA\_DIP\_" (Device Information Property) and are supplied by Windows Image Acquisition (WIA).</span></span> <span data-ttu-id="464f3-107">Zu Skriptzwecken verwenden diese Konstanten das Präfix "DeviceInfo" und sind Teil des Aufzählungstyps [WiaDeviceInfoPropertyId.](-wia-wiadeviceinfopropertyid.md)</span><span class="sxs-lookup"><span data-stu-id="464f3-107">For scripting purposes, these constants use the prefix "DeviceInfo" and are part of the [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) enumerated type.</span></span> <span data-ttu-id="464f3-108">Der entsprechende Membername aus dieser Skriptenumeration wird in Klammern neben dem C/C++-Konstantennamen in der folgenden Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="464f3-108">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="464f3-109">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="464f3-109">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="464f3-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="464f3-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <span data-ttu-id="464f3-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span><span class="sxs-lookup"><span data-stu-id="464f3-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="464f3-112">Die Geräte-ID-Zeichenfolge für den WIA-Minitreiber.</span><span class="sxs-lookup"><span data-stu-id="464f3-112">The device ID string for the WIA minidriver.</span></span> <span data-ttu-id="464f3-113">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="464f3-113">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="464f3-114">Typ: VT_BSTR, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="464f3-114">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <span data-ttu-id="464f3-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span><span class="sxs-lookup"><span data-stu-id="464f3-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="464f3-116">Die Beschreibungszeichenfolge des Anbieters für den WIA-Minitreiber.</span><span class="sxs-lookup"><span data-stu-id="464f3-116">The vendor description string for the WIA minidriver.</span></span> <span data-ttu-id="464f3-117">Die Herstellerbeschreibung wird aus der INF-Datei abgerufen.</span><span class="sxs-lookup"><span data-stu-id="464f3-117">The vendor description is obtained from the INF file.</span></span> <span data-ttu-id="464f3-118">Eine Anwendung liest diese Eigenschaft, um eine Beschreibung des Geräteanbieters abzurufen.</span><span class="sxs-lookup"><span data-stu-id="464f3-118">An application reads this property to get a description of the device vendor.</span></span> <span data-ttu-id="464f3-119">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="464f3-119">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="464f3-120">Typ: VT_BSTR, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="464f3-120">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <span data-ttu-id="464f3-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span><span class="sxs-lookup"><span data-stu-id="464f3-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="464f3-122">Die Gerätebeschreibungszeichenfolge für den WIA-Minitreiber.</span><span class="sxs-lookup"><span data-stu-id="464f3-122">The device description string for the WIA minidriver.</span></span> <span data-ttu-id="464f3-123">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="464f3-123">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="464f3-124">Die gerätebeschreibungszeichenfolge, die diese Eigenschaft enthält, wird aus der INF-Datei ermittelt.</span><span class="sxs-lookup"><span data-stu-id="464f3-124">The device description string this property contains is obtained from the INF file.</span></span> <span data-ttu-id="464f3-125">Eine Anwendung liest diese Eigenschaft, um eine Beschreibung des Geräts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="464f3-125">An application reads this property to get a description of the device.</span></span><br/> <span data-ttu-id="464f3-126">Typ: VT_BSTR, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="464f3-126">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <span data-ttu-id="464f3-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span><span class="sxs-lookup"><span data-stu-id="464f3-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="464f3-128">Der Gerätetyp und der Geräteuntertyp.</span><span class="sxs-lookup"><span data-stu-id="464f3-128">The device type and device subtype.</span></span> <span data-ttu-id="464f3-129">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="464f3-129">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="464f3-130">Verwenden Sie GET_STIDEVICE_TYPE Makro , um den Gerätetyp zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="464f3-130">Use the GET_STIDEVICE_TYPE macro to get the device type.</span></span> <span data-ttu-id="464f3-131">Der Gerätetyp und der Untertyp werden aus der INF-Datei ermittelt.</span><span class="sxs-lookup"><span data-stu-id="464f3-131">The device type and subtype are obtained from the INF file.</span></span> <span data-ttu-id="464f3-132">Eine Anwendung liest diese Eigenschaft, um zu bestimmen, ob sie einen Scanner, eine Kamera oder ein Videogerät verwendet.</span><span class="sxs-lookup"><span data-stu-id="464f3-132">An application reads this property to determine whether it is using a scanner, camera, or video device.</span></span><br/> <span data-ttu-id="464f3-133">Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="464f3-133">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="464f3-134">Derzeit werden Gerätetypen wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="464f3-134">Currently, device types are defined as follows.</span></span> <span data-ttu-id="464f3-135">Das Sternchen \* gibt an, dass der Gerätetyp von Windows Vista und höher nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="464f3-135">The asterisk \* indicates that the device type is not supported by Windows Vista and later.</span></span> <span data-ttu-id="464f3-136">Das doppelte Sternchen \*\* gibt an, dass der Gerätetyp von Windows Server 2003, Windows Vista oder höher nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="464f3-136">The double asterisk \*\* indicates that the device type is not supported by either Windows Server 2003, Windows Vista, or later.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="464f3-137">type</span><span class="sxs-lookup"><span data-stu-id="464f3-137">Type</span></span></th>
<th><span data-ttu-id="464f3-138">Wert</span><span class="sxs-lookup"><span data-stu-id="464f3-138">Value</span></span></th>
<th><span data-ttu-id="464f3-139">Definition</span><span class="sxs-lookup"><span data-stu-id="464f3-139">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="464f3-140">StiDeviceTypeDefault</span><span class="sxs-lookup"><span data-stu-id="464f3-140">StiDeviceTypeDefault</span></span></td>
<td><span data-ttu-id="464f3-141">0x0000</span><span class="sxs-lookup"><span data-stu-id="464f3-141">0x0000</span></span></td>
<td><span data-ttu-id="464f3-142">Standardgerät</span><span class="sxs-lookup"><span data-stu-id="464f3-142">Default device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="464f3-143">StiDeviceTypeScanner</span><span class="sxs-lookup"><span data-stu-id="464f3-143">StiDeviceTypeScanner</span></span></td>
<td><span data-ttu-id="464f3-144">0x0001</span><span class="sxs-lookup"><span data-stu-id="464f3-144">0x0001</span></span></td>
<td><span data-ttu-id="464f3-145">Scannergerät (siehe <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES,</strong></a> um zu ermitteln, ob der Scanner flach oder mit Blättern ausgestattet ist.)</span><span class="sxs-lookup"><span data-stu-id="464f3-145">Scanner device (See the <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> to determine if the scanner is flatbed or sheet-fed.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="464f3-146">StiDeviceTypeDigitalCamera\*</span><span class="sxs-lookup"><span data-stu-id="464f3-146">StiDeviceTypeDigitalCamera\*</span></span></td>
<td><span data-ttu-id="464f3-147">0x0002</span><span class="sxs-lookup"><span data-stu-id="464f3-147">0x0002</span></span></td>
<td><span data-ttu-id="464f3-148">Kameragerät</span><span class="sxs-lookup"><span data-stu-id="464f3-148">Camera device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="464f3-149">StiDeviceTypeStreamingVideo\*\*</span><span class="sxs-lookup"><span data-stu-id="464f3-149">StiDeviceTypeStreamingVideo\*\*</span></span></td>
<td><span data-ttu-id="464f3-150">0x0003</span><span class="sxs-lookup"><span data-stu-id="464f3-150">0x0003</span></span></td>
<td><span data-ttu-id="464f3-151">Videogerät</span><span class="sxs-lookup"><span data-stu-id="464f3-151">Video device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <span data-ttu-id="464f3-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span><span class="sxs-lookup"><span data-stu-id="464f3-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="464f3-153">Der Portname des installierten Geräts, der vom Kernelmodustreiber zugewiesen wird, der das Gerät betreibt.</span><span class="sxs-lookup"><span data-stu-id="464f3-153">The installed device's port name, which is assigned by the kernel-mode driver that operates the device.</span></span> <span data-ttu-id="464f3-154">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="464f3-154">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="464f3-155">Eine Anwendung liest diese Eigenschaft, um den Portnamen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="464f3-155">An application reads this property to determine the port name.</span></span></p>
<p><span data-ttu-id="464f3-156">Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="464f3-156">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <span data-ttu-id="464f3-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span><span class="sxs-lookup"><span data-stu-id="464f3-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="464f3-158">Der Name des Geräts.</span><span class="sxs-lookup"><span data-stu-id="464f3-158">The name of the device.</span></span> <span data-ttu-id="464f3-159">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="464f3-159">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="464f3-160">Der in dieser Eigenschaft enthaltene Gerätename wird aus der INF-Datei abgerufen.</span><span class="sxs-lookup"><span data-stu-id="464f3-160">The device name contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="464f3-161">Eine Anwendung liest diese Eigenschaft, um den Namen des Geräts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="464f3-161">An application reads this property to obtain the name of the device.</span></span></p>
<p><span data-ttu-id="464f3-162">Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="464f3-162">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <span data-ttu-id="464f3-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span><span class="sxs-lookup"><span data-stu-id="464f3-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="464f3-164">Der Name des Servers, auf dem der WIA-Minitreiber ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="464f3-164">The name of the server that the WIA minidriver is running on.</span></span> <span data-ttu-id="464f3-165">Diese Eigenschaft ist für Windows XP und höher optional.</span><span class="sxs-lookup"><span data-stu-id="464f3-165">This property is optional for Windows XP and later.</span></span></p>
<p><span data-ttu-id="464f3-166">Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="464f3-166">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <span data-ttu-id="464f3-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span><span class="sxs-lookup"><span data-stu-id="464f3-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="464f3-168">Die Geräte-ID des WIA-Geräts, das auf einem Remotecomputer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="464f3-168">The device ID of the WIA device that is installed on a remote computer.</span></span> <span data-ttu-id="464f3-169">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="464f3-169">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="464f3-170">Sie wird nur intern vom WIA-Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="464f3-170">It is only used internally by the WIA service.</span></span></p>
<p><span data-ttu-id="464f3-171">Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="464f3-171">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <span data-ttu-id="464f3-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span><span class="sxs-lookup"><span data-stu-id="464f3-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="464f3-173">Die vom Hersteller bereitgestellte CLSID für alle COM-Objekte der UI-Erweiterung, die mit dem WIA-Minitreiber installiert werden.</span><span class="sxs-lookup"><span data-stu-id="464f3-173">The vendor-supplied CLSID for any UI extension COM object that is installed with the WIA minidriver.</span></span> <span data-ttu-id="464f3-174">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="464f3-174">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="464f3-175">Der INF-Wert der UI-CLSID, der in dieser Eigenschaft enthalten ist, wird aus der INF-Datei abgerufen.</span><span class="sxs-lookup"><span data-stu-id="464f3-175">The UI CLSID value contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="464f3-176">Wenn keine UI-CLSID angegeben ist, stellt der WIA-Dienst einen Standardwert zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="464f3-176">If no UI CLSID is specified, the WIA service supplies a default value.</span></span> <span data-ttu-id="464f3-177">Diese Eigenschaft wird nur intern vom WIA-Dienst verwendet, wenn die Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="464f3-177">This property is only used internally by the WIA service when UI is being displayed.</span></span></p>
<p><span data-ttu-id="464f3-178">Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="464f3-178">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <span data-ttu-id="464f3-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span><span class="sxs-lookup"><span data-stu-id="464f3-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="464f3-180">Der Verbindungstyp, der vom Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="464f3-180">The type of connection that the device is using.</span></span> <span data-ttu-id="464f3-181">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft, und nur der WIA-Dienst kann sie ändern.</span><span class="sxs-lookup"><span data-stu-id="464f3-181">The WIA service creates and maintains this property, and only the WIA service can change it.</span></span></p>
<p><span data-ttu-id="464f3-182">Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="464f3-182">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="464f3-183">Die -Eigenschaft kann die folgenden möglichen Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="464f3-183">The property can have the following possible values.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="464f3-184">Wert</span><span class="sxs-lookup"><span data-stu-id="464f3-184">Value</span></span></th>
<th><span data-ttu-id="464f3-185">Definition</span><span class="sxs-lookup"><span data-stu-id="464f3-185">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="464f3-186">1</span><span class="sxs-lookup"><span data-stu-id="464f3-186">1</span></span></td>
<td><span data-ttu-id="464f3-187">Generisches WDM-Gerät</span><span class="sxs-lookup"><span data-stu-id="464f3-187">Generic WDM device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="464f3-188">2</span><span class="sxs-lookup"><span data-stu-id="464f3-188">2</span></span></td>
<td><span data-ttu-id="464f3-189">SCSI-Gerät</span><span class="sxs-lookup"><span data-stu-id="464f3-189">SCSI device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="464f3-190">4</span><span class="sxs-lookup"><span data-stu-id="464f3-190">4</span></span></td>
<td><span data-ttu-id="464f3-191">USB-Gerät</span><span class="sxs-lookup"><span data-stu-id="464f3-191">USB device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="464f3-192">8</span><span class="sxs-lookup"><span data-stu-id="464f3-192">8</span></span></td>
<td><span data-ttu-id="464f3-193">Serielles Gerät</span><span class="sxs-lookup"><span data-stu-id="464f3-193">Serial device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="464f3-194">16</span><span class="sxs-lookup"><span data-stu-id="464f3-194">16</span></span></td>
<td><span data-ttu-id="464f3-195">Paralleles Gerät</span><span class="sxs-lookup"><span data-stu-id="464f3-195">Parallel device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <span data-ttu-id="464f3-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span><span class="sxs-lookup"><span data-stu-id="464f3-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="464f3-197">Die aktuelle Einstellung der Baudrate für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="464f3-197">The current baud rate setting for the device.</span></span> <span data-ttu-id="464f3-198">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="464f3-198">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="464f3-199">Der Wert sollte Leer &quot; &quot; sein, wenn das Gerät nicht über ein serielles Kabel verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="464f3-199">The value should be &quot;Empty&quot; if the device is not connected by a serial cable.</span></span></p>
<p><span data-ttu-id="464f3-200">Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="464f3-200">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <span data-ttu-id="464f3-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="464f3-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="464f3-202">Die generischen STI-Funktionen für das Gerät aus der INF-Datei.</span><span class="sxs-lookup"><span data-stu-id="464f3-202">The generic STI capabilities for the device as obtained from the INF file.</span></span> <span data-ttu-id="464f3-203">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="464f3-203">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="464f3-204">Eine Anwendung liest diese Eigenschaft, um die generischen STI-Funktionen des Geräts zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="464f3-204">An application reads this property to determine the generic STI capabilities of the device.</span></span></p>
<p><span data-ttu-id="464f3-205">Typ: <strong>VT_I4</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="464f3-205">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <span data-ttu-id="464f3-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="464f3-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="464f3-207">Die Zahl (als Zeichenfolge) der aktuellen WIA-Version, die auf dem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="464f3-207">The number (as a string) of the current WIA version that is installed on the system.</span></span> <span data-ttu-id="464f3-208">Eine Anwendung liest diese Eigenschaft, um die Version von WIA zu bestimmen, die auf dem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="464f3-208">An application reads this property to determine the version of WIA that is installed on the system.</span></span> <span data-ttu-id="464f3-209">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="464f3-209">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="464f3-210">Diese Eigenschaft ist in Windows XP und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="464f3-210">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="464f3-211">Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="464f3-211">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <span data-ttu-id="464f3-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="464f3-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="464f3-213">Die aktuelle DLL-Version des WIA-Minitreibers.</span><span class="sxs-lookup"><span data-stu-id="464f3-213">The current DLL version of the WIA minidriver.</span></span> <span data-ttu-id="464f3-214">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="464f3-214">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="464f3-215">Diese Eigenschaft ist in Windows XP und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="464f3-215">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="464f3-216">Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützt, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="464f3-216">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <span data-ttu-id="464f3-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span><span class="sxs-lookup"><span data-stu-id="464f3-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="464f3-218">Die aktuelle PnP-ID für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="464f3-218">The current PnP id for the device.</span></span> <span data-ttu-id="464f3-219">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="464f3-219">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="464f3-220">Diese Eigenschaft ist in Windows Vista und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="464f3-220">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="464f3-221">Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="464f3-221">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <span data-ttu-id="464f3-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="464f3-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="464f3-223">Die generische Version des STI-Treibers.</span><span class="sxs-lookup"><span data-stu-id="464f3-223">The generic STI driver version.</span></span> <span data-ttu-id="464f3-224">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="464f3-224">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="464f3-225">Eine Anwendung liest diese Eigenschaft, um die generische Version des STI-Treibers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="464f3-225">An application reads this property to determine the generic STI driver version.</span></span> <span data-ttu-id="464f3-226">Diese Eigenschaft ist in Windows Vista und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="464f3-226">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="464f3-227">Typ: <strong>VT_BSTR</strong>, Zugriff: Schreibgeschützte Werte, Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="464f3-227">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="464f3-228">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="464f3-228">Requirements</span></span>



| <span data-ttu-id="464f3-229">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="464f3-229">Requirement</span></span> | <span data-ttu-id="464f3-230">Wert</span><span class="sxs-lookup"><span data-stu-id="464f3-230">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="464f3-231">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="464f3-231">Minimum supported client</span></span><br/> | <span data-ttu-id="464f3-232">Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="464f3-232">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="464f3-233">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="464f3-233">Minimum supported server</span></span><br/> | <span data-ttu-id="464f3-234">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="464f3-234">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="464f3-235">Header</span><span class="sxs-lookup"><span data-stu-id="464f3-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="464f3-236"><dt>Wiadef.h</dt></span><span class="sxs-lookup"><span data-stu-id="464f3-236"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




