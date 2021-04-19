---
description: Geräte Informations Eigenschaften sind Eigenschaften, die das Setup und die Installation des Geräts beschreiben.
ms.assetid: ff6771ac-491e-4765-8cfe-11c7efc1c971
title: Eigenschaften Konstanten für Geräteinformationen (wiadef. h)
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
ms.openlocfilehash: 18c44bb310c2dcee5bb227e0885a71b58f5b362e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353092"
---
# <a name="device-information-property-constants"></a><span data-ttu-id="6ccb0-103">Eigenschaften Konstanten für Geräteinformationen</span><span class="sxs-lookup"><span data-stu-id="6ccb0-103">Device Information Property Constants</span></span>

<span data-ttu-id="6ccb0-104">Geräte Informations Eigenschaften sind Eigenschaften, die das Setup und die Installation des Geräts beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-104">Device Information Properties are properties that describe the setup and installation of the device.</span></span> <span data-ttu-id="6ccb0-105">Diese Eigenschaften sind über die [**iwiadevmgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) -oder [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) -Schnittstelle und auch über das root-Element verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-105">These properties are available through the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interfaces and also through the root item.</span></span> <span data-ttu-id="6ccb0-106">Den Eigenschaften für Geräteinformationen wird das Präfix "WIA \_ DIP \_ " (Geräte Informations Eigenschaft) vorangestellt, die von der Windows-Abbild Beschaffung (WIA) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-106">Device information properties are prefixed with "WIA\_DIP\_" (Device Information Property) and are supplied by Windows Image Acquisition (WIA).</span></span> <span data-ttu-id="6ccb0-107">Zu Skript Zwecken verwenden diese Konstanten das Präfix "deviceInfo" und sind Teil des Enumerationstyps [wiadeviceinf opropertyid](-wia-wiadeviceinfopropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="6ccb0-107">For scripting purposes, these constants use the prefix "DeviceInfo" and are part of the [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) enumerated type.</span></span> <span data-ttu-id="6ccb0-108">Der entsprechende Elementname aus dieser Skript Enumeration wird in Klammern neben dem Konstanten Namen C/C++ in der folgenden Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-108">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="6ccb0-109">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="6ccb0-109">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="6ccb0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6ccb0-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <span data-ttu-id="6ccb0-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> (Geräte <dt>-</dt> ID) </span><span class="sxs-lookup"><span data-stu-id="6ccb0-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="6ccb0-112">Die Geräte-ID-Zeichenfolge für den WIA-Mini Treiber.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-112">The device ID string for the WIA minidriver.</span></span> <span data-ttu-id="6ccb0-113">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-113">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="6ccb0-114">Typ: VT_BSTR, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ccb0-114">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <span data-ttu-id="6ccb0-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> "Geräte- <dt>fovendde</dt> " </span><span class="sxs-lookup"><span data-stu-id="6ccb0-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="6ccb0-116">Die Hersteller Beschreibungs Zeichenfolge für den WIA-Mini Treiber.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-116">The vendor description string for the WIA minidriver.</span></span> <span data-ttu-id="6ccb0-117">Die Herstellerbeschreibung wird aus der INF-Datei abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-117">The vendor description is obtained from the INF file.</span></span> <span data-ttu-id="6ccb0-118">Diese Eigenschaft wird von einer Anwendung gelesen, um eine Beschreibung des Geräte Anbieters zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-118">An application reads this property to get a description of the device vendor.</span></span> <span data-ttu-id="6ccb0-119">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-119">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="6ccb0-120">Typ: VT_BSTR, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ccb0-120">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <span data-ttu-id="6ccb0-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>deviceingefodevdesc</dt> </span><span class="sxs-lookup"><span data-stu-id="6ccb0-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="6ccb0-122">Die Geräte Beschreibungs Zeichenfolge für den WIA-Mini Treiber.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-122">The device description string for the WIA minidriver.</span></span> <span data-ttu-id="6ccb0-123">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-123">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="6ccb0-124">Die Geräte Beschreibungs Zeichenfolge, die diese Eigenschaft enthält, wird aus der INF-Datei abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-124">The device description string this property contains is obtained from the INF file.</span></span> <span data-ttu-id="6ccb0-125">Diese Eigenschaft wird von einer Anwendung gelesen, um eine Beschreibung des Geräts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-125">An application reads this property to get a description of the device.</span></span><br/> <span data-ttu-id="6ccb0-126">Typ: VT_BSTR, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ccb0-126">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <span data-ttu-id="6ccb0-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> " <dt>deviceinfodevtype</dt> " </span><span class="sxs-lookup"><span data-stu-id="6ccb0-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="6ccb0-128">Der Gerätetyp und der Geräte Untertyp.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-128">The device type and device subtype.</span></span> <span data-ttu-id="6ccb0-129">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-129">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="6ccb0-130">Verwenden Sie das GET_STIDEVICE_TYPE-Makro, um den Gerätetyp zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-130">Use the GET_STIDEVICE_TYPE macro to get the device type.</span></span> <span data-ttu-id="6ccb0-131">Gerätetyp und Untertyp werden aus der INF-Datei abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-131">The device type and subtype are obtained from the INF file.</span></span> <span data-ttu-id="6ccb0-132">Eine Anwendung liest diese Eigenschaft, um zu bestimmen, ob Sie einen Scanner, eine Kamera oder ein Videogerät verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-132">An application reads this property to determine whether it is using a scanner, camera, or video device.</span></span><br/> <span data-ttu-id="6ccb0-133">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ccb0-133">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="6ccb0-134">Derzeit werden Gerätetypen wie folgt definiert.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-134">Currently, device types are defined as follows.</span></span> <span data-ttu-id="6ccb0-135">Das Sternchen \* gibt an, dass der Gerätetyp von Windows Vista und höher nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-135">The asterisk \* indicates that the device type is not supported by Windows Vista and later.</span></span> <span data-ttu-id="6ccb0-136">Das doppelte Sternchen \* \* gibt an, dass der Gerätetyp weder von Windows Server 2003 noch von Windows Vista oder höher unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-136">The double asterisk \*\* indicates that the device type is not supported by either Windows Server 2003, Windows Vista, or later.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6ccb0-137">type</span><span class="sxs-lookup"><span data-stu-id="6ccb0-137">Type</span></span></th>
<th><span data-ttu-id="6ccb0-138">Wert</span><span class="sxs-lookup"><span data-stu-id="6ccb0-138">Value</span></span></th>
<th><span data-ttu-id="6ccb0-139">Definition</span><span class="sxs-lookup"><span data-stu-id="6ccb0-139">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6ccb0-140">Stide vicetypeer default</span><span class="sxs-lookup"><span data-stu-id="6ccb0-140">StiDeviceTypeDefault</span></span></td>
<td><span data-ttu-id="6ccb0-141">0x0000</span><span class="sxs-lookup"><span data-stu-id="6ccb0-141">0x0000</span></span></td>
<td><span data-ttu-id="6ccb0-142">Standardgerät</span><span class="sxs-lookup"><span data-stu-id="6ccb0-142">Default device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ccb0-143">Stide vicetypescanner</span><span class="sxs-lookup"><span data-stu-id="6ccb0-143">StiDeviceTypeScanner</span></span></td>
<td><span data-ttu-id="6ccb0-144">0x0001</span><span class="sxs-lookup"><span data-stu-id="6ccb0-144">0x0001</span></span></td>
<td><span data-ttu-id="6ccb0-145">Überprüfungs Gerät (Weitere Informationen finden Sie in den <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> , um zu ermitteln, ob die Überprüfung ein flatsheet oder eine Blatt Überprüfung ist)</span><span class="sxs-lookup"><span data-stu-id="6ccb0-145">Scanner device (See the <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> to determine if the scanner is flatbed or sheet-fed.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ccb0-146">Stide vicetyetdigitalcamera \*</span><span class="sxs-lookup"><span data-stu-id="6ccb0-146">StiDeviceTypeDigitalCamera\*</span></span></td>
<td><span data-ttu-id="6ccb0-147">0x0002</span><span class="sxs-lookup"><span data-stu-id="6ccb0-147">0x0002</span></span></td>
<td><span data-ttu-id="6ccb0-148">Kamera Gerät</span><span class="sxs-lookup"><span data-stu-id="6ccb0-148">Camera device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ccb0-149">Stidebug-Video \* \*</span><span class="sxs-lookup"><span data-stu-id="6ccb0-149">StiDeviceTypeStreamingVideo\*\*</span></span></td>
<td><span data-ttu-id="6ccb0-150">0x0003</span><span class="sxs-lookup"><span data-stu-id="6ccb0-150">0x0003</span></span></td>
<td><span data-ttu-id="6ccb0-151">Video Gerät</span><span class="sxs-lookup"><span data-stu-id="6ccb0-151">Video device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <span data-ttu-id="6ccb0-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> "Geräte <dt>Name</dt> " </span><span class="sxs-lookup"><span data-stu-id="6ccb0-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6ccb0-153">Der Port Name des installierten Geräts, der durch den Kernelmodustreiber zugewiesen wird, der das Gerät bedient.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-153">The installed device's port name, which is assigned by the kernel-mode driver that operates the device.</span></span> <span data-ttu-id="6ccb0-154">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-154">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="6ccb0-155">Eine Anwendung liest diese Eigenschaft, um den Portnamen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-155">An application reads this property to determine the port name.</span></span></p>
<p><span data-ttu-id="6ccb0-156">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ccb0-156">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <span data-ttu-id="6ccb0-157"><dt><strong></strong></dt> <dt>Deviceinfodevname</dt> WIA_DIP_DEV_NAME </span><span class="sxs-lookup"><span data-stu-id="6ccb0-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6ccb0-158">Der Name des Geräts.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-158">The name of the device.</span></span> <span data-ttu-id="6ccb0-159">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-159">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="6ccb0-160">Der in dieser Eigenschaft enthaltene Gerätename wird aus der INF-Datei abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-160">The device name contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="6ccb0-161">Diese Eigenschaft wird von einer Anwendung gelesen, um den Namen des Geräts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-161">An application reads this property to obtain the name of the device.</span></span></p>
<p><span data-ttu-id="6ccb0-162">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ccb0-162">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <span data-ttu-id="6ccb0-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> Geräte <dt>Name</dt> </span><span class="sxs-lookup"><span data-stu-id="6ccb0-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6ccb0-164">Der Name des Servers, auf dem der WIA-Mini Treiber ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-164">The name of the server that the WIA minidriver is running on.</span></span> <span data-ttu-id="6ccb0-165">Diese Eigenschaft ist optional für Windows XP und höher.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-165">This property is optional for Windows XP and later.</span></span></p>
<p><span data-ttu-id="6ccb0-166">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ccb0-166">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <span data-ttu-id="6ccb0-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> "Geräte <dt>-</dt> ID" </span><span class="sxs-lookup"><span data-stu-id="6ccb0-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6ccb0-168">Die Geräte-ID des WIA-Geräts, das auf einem Remote Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-168">The device ID of the WIA device that is installed on a remote computer.</span></span> <span data-ttu-id="6ccb0-169">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-169">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="6ccb0-170">Sie wird nur intern vom WIA-Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-170">It is only used internally by the WIA service.</span></span></p>
<p><span data-ttu-id="6ccb0-171">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ccb0-171">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <span data-ttu-id="6ccb0-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> "Geräte- <dt>CLSID</dt> " </span><span class="sxs-lookup"><span data-stu-id="6ccb0-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6ccb0-173">Die vom Hersteller bereitgestellte CLSID für alle COM-Objekte der UI-Erweiterung, die mit dem WIA-Mini Treiber installiert werden.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-173">The vendor-supplied CLSID for any UI extension COM object that is installed with the WIA minidriver.</span></span> <span data-ttu-id="6ccb0-174">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-174">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="6ccb0-175">Der in dieser Eigenschaft enthaltene Benutzeroberflächen-CLSID-Wert wird aus der INF-Datei abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-175">The UI CLSID value contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="6ccb0-176">Wenn keine Benutzeroberflächen-CLSID angegeben ist, stellt der WIA-Dienst einen Standardwert bereit.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-176">If no UI CLSID is specified, the WIA service supplies a default value.</span></span> <span data-ttu-id="6ccb0-177">Diese Eigenschaft wird nur intern vom WIA-Dienst verwendet, wenn die Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-177">This property is only used internally by the WIA service when UI is being displayed.</span></span></p>
<p><span data-ttu-id="6ccb0-178">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ccb0-178">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <span data-ttu-id="6ccb0-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> "Geräte- <dt>/Konfigurations-config</dt> " </span><span class="sxs-lookup"><span data-stu-id="6ccb0-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6ccb0-180">Der Verbindungstyp, der vom Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-180">The type of connection that the device is using.</span></span> <span data-ttu-id="6ccb0-181">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft, und nur der WIA-Dienst kann Sie ändern.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-181">The WIA service creates and maintains this property, and only the WIA service can change it.</span></span></p>
<p><span data-ttu-id="6ccb0-182">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ccb0-182">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="6ccb0-183">Die-Eigenschaft kann die folgenden möglichen Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-183">The property can have the following possible values.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6ccb0-184">Wert</span><span class="sxs-lookup"><span data-stu-id="6ccb0-184">Value</span></span></th>
<th><span data-ttu-id="6ccb0-185">Definition</span><span class="sxs-lookup"><span data-stu-id="6ccb0-185">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6ccb0-186">1</span><span class="sxs-lookup"><span data-stu-id="6ccb0-186">1</span></span></td>
<td><span data-ttu-id="6ccb0-187">Generisches WDM-Gerät</span><span class="sxs-lookup"><span data-stu-id="6ccb0-187">Generic WDM device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ccb0-188">2</span><span class="sxs-lookup"><span data-stu-id="6ccb0-188">2</span></span></td>
<td><span data-ttu-id="6ccb0-189">SCSI-Gerät</span><span class="sxs-lookup"><span data-stu-id="6ccb0-189">SCSI device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ccb0-190">4</span><span class="sxs-lookup"><span data-stu-id="6ccb0-190">4</span></span></td>
<td><span data-ttu-id="6ccb0-191">USB-Gerät</span><span class="sxs-lookup"><span data-stu-id="6ccb0-191">USB device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6ccb0-192">8</span><span class="sxs-lookup"><span data-stu-id="6ccb0-192">8</span></span></td>
<td><span data-ttu-id="6ccb0-193">Serielles Gerät</span><span class="sxs-lookup"><span data-stu-id="6ccb0-193">Serial device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6ccb0-194">16</span><span class="sxs-lookup"><span data-stu-id="6ccb0-194">16</span></span></td>
<td><span data-ttu-id="6ccb0-195">Paralleles Gerät</span><span class="sxs-lookup"><span data-stu-id="6ccb0-195">Parallel device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <span data-ttu-id="6ccb0-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> (Geräte <dt>Einstellungs</dt> Paket) </span><span class="sxs-lookup"><span data-stu-id="6ccb0-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6ccb0-197">Die aktuelle Baudrate-Einstellung für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-197">The current baud rate setting for the device.</span></span> <span data-ttu-id="6ccb0-198">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-198">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="6ccb0-199">Der Wert sollte leer sein, &quot; &quot; Wenn das Gerät nicht mit einem seriellen Kabel verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-199">The value should be &quot;Empty&quot; if the device is not connected by a serial cable.</span></span></p>
<p><span data-ttu-id="6ccb0-200">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ccb0-200">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <span data-ttu-id="6ccb0-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>deviceingefostigenfunktionalitäten</dt> </span><span class="sxs-lookup"><span data-stu-id="6ccb0-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6ccb0-202">Die generischen STI-Funktionen für das Gerät, wie Sie aus der INF-Datei abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-202">The generic STI capabilities for the device as obtained from the INF file.</span></span> <span data-ttu-id="6ccb0-203">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-203">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="6ccb0-204">Diese Eigenschaft wird von einer Anwendung gelesen, um die generischen Verwaltungsfunktionen des Geräts zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-204">An application reads this property to determine the generic STI capabilities of the device.</span></span></p>
<p><span data-ttu-id="6ccb0-205">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ccb0-205">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <span data-ttu-id="6ccb0-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> "Geräte- <dt>fowiaversion</dt> " </span><span class="sxs-lookup"><span data-stu-id="6ccb0-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6ccb0-207">Die Zahl (als Zeichenfolge) der aktuellen WIA-Version, die auf dem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-207">The number (as a string) of the current WIA version that is installed on the system.</span></span> <span data-ttu-id="6ccb0-208">Eine Anwendung liest diese Eigenschaft, um die Version von WIA zu bestimmen, die auf dem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-208">An application reads this property to determine the version of WIA that is installed on the system.</span></span> <span data-ttu-id="6ccb0-209">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-209">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="6ccb0-210">Diese Eigenschaft ist in Windows XP und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-210">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="6ccb0-211">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ccb0-211">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <span data-ttu-id="6ccb0-212"><dt><strong></strong></dt> <dt>Deviceingefodriverversion</dt> WIA_DIP_DRIVER_VERSION </span><span class="sxs-lookup"><span data-stu-id="6ccb0-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6ccb0-213">Die aktuelle dll-Version des WIA-Mini Treibers.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-213">The current DLL version of the WIA minidriver.</span></span> <span data-ttu-id="6ccb0-214">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-214">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="6ccb0-215">Diese Eigenschaft ist in Windows XP und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-215">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="6ccb0-216">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ccb0-216">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <span data-ttu-id="6ccb0-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt></dt> "Geräte-ID" </span><span class="sxs-lookup"><span data-stu-id="6ccb0-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6ccb0-218">Die aktuelle PNP-ID für das Gerät.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-218">The current PnP id for the device.</span></span> <span data-ttu-id="6ccb0-219">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-219">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="6ccb0-220">Diese Eigenschaft ist in Windows Vista und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-220">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="6ccb0-221">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ccb0-221">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <span data-ttu-id="6ccb0-222"><dt><strong></strong></dt> <dt>Deviceingefostidriverversion</dt> WIA_DIP_STI_DRIVER_VERSION </span><span class="sxs-lookup"><span data-stu-id="6ccb0-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="6ccb0-223">Die Version des generischen STI-Treibers.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-223">The generic STI driver version.</span></span> <span data-ttu-id="6ccb0-224">Der WIA-Dienst erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-224">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="6ccb0-225">Eine Anwendung liest diese Eigenschaft, um die Version des generischen STI-Treibers zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-225">An application reads this property to determine the generic STI driver version.</span></span> <span data-ttu-id="6ccb0-226">Diese Eigenschaft ist in Windows Vista und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6ccb0-226">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="6ccb0-227">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="6ccb0-227">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="6ccb0-228">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ccb0-228">Requirements</span></span>



| <span data-ttu-id="6ccb0-229">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ccb0-229">Requirement</span></span> | <span data-ttu-id="6ccb0-230">Wert</span><span class="sxs-lookup"><span data-stu-id="6ccb0-230">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6ccb0-231">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ccb0-231">Minimum supported client</span></span><br/> | <span data-ttu-id="6ccb0-232">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ccb0-232">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6ccb0-233">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ccb0-233">Minimum supported server</span></span><br/> | <span data-ttu-id="6ccb0-234">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ccb0-234">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6ccb0-235">Header</span><span class="sxs-lookup"><span data-stu-id="6ccb0-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ccb0-236"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ccb0-236"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




