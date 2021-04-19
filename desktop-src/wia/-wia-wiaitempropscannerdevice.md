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
# <a name="scanner-device-property-constants"></a><span data-ttu-id="dc195-103">Eigenschaften Konstanten für Scanner-Geräte</span><span class="sxs-lookup"><span data-stu-id="dc195-103">Scanner Device Property Constants</span></span>

<span data-ttu-id="dc195-104">Für Windows-Abbild Beschaffung (WIA)-Hardware Geräte sind Eigenschaftswerte vorhanden, die in der Windows-Registrierung gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="dc195-104">Windows Image Acquisition (WIA) hardware devices have property values that are stored in the Windows registry.</span></span> <span data-ttu-id="dc195-105">Weitere Informationen finden Sie unter [**Allgemeine Geräte Eigenschafts Konstanten**](-wia-wiaitempropcommondevice.md).</span><span class="sxs-lookup"><span data-stu-id="dc195-105">For more information, see [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).</span></span> <span data-ttu-id="dc195-106">Die folgenden Geräteeigenschaften Konstanten, mit den zugehörigen Zeichen folgen, sind spezifisch für digitale Bildscanner.</span><span class="sxs-lookup"><span data-stu-id="dc195-106">The following device property constants, with their associated strings, are specific to digital image scanners.</span></span>

<span data-ttu-id="dc195-107">Das Präfix "WIA \_ DPS \_ " gibt eine Geräte Eigenschaft für Scanner-Geräte an und ist die in C/C++ verwendete Benennungs Konvention.</span><span class="sxs-lookup"><span data-stu-id="dc195-107">The prefix "WIA\_DPS\_" indicates a Device Property for Scanner devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="dc195-108">Bei der Skripterstellung verwenden diese Konstanten das Präfix "scannerdevice" und sind Teil des enumerierten Typs " [wiaitempropertyid](-wia-wiaitempropertyid.md) ".</span><span class="sxs-lookup"><span data-stu-id="dc195-108">For scripting purposes these constants use the prefix "ScannerDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="dc195-109">Der entsprechende Elementname aus dieser Skript Enumeration wird in Klammern neben dem Konstanten Namen C/C++ in der folgenden Liste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dc195-109">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="dc195-110">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="dc195-110">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="dc195-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc195-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <span data-ttu-id="dc195-112"><dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>scannerdeviceabviceid</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-112"><dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </span></span></dl></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
<span data-ttu-id="dc195-113">Diese Eigenschaft wird nur unter Windows Vista und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-113">This property is supported only on Windows Vista and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="dc195-114">Enthält einen eindeutigen funktionsinstanzbezeichner für ein Webdienst-Scanner-Gerät.</span><span class="sxs-lookup"><span data-stu-id="dc195-114">Contains a unique function instance identifier for a web services scanner device.</span></span> <span data-ttu-id="dc195-115">Dieser Bezeichner stellt den Webdienst auf dem Scannergerät dar, mit dem der WIA-Mini Treiber kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="dc195-115">This identifier represents the web service on the scanner device with which the WIA mini-driver is communicating.</span></span> <span data-ttu-id="dc195-116">Es sollten keine Annahmen über die Form dieses Bezeichners vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="dc195-116">No assumptions about the form of this identifier should be made.</span></span> <span data-ttu-id="dc195-117">Der WIA-Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-117">The WIA mini-driver creates and maintains this property.</span></span> <br/> <span data-ttu-id="dc195-118">WIA-Anwendungen können den Wert von WIA_DPS_DEVICE_ID verwenden, um mithilfe der funktionsermittlungs-API zu suchen, das funktionsinstanzobjekt, das das in der aktuellen WIA 2,0-Sitzung verwendete Webdienst Scanner-Gerät darstellt.</span><span class="sxs-lookup"><span data-stu-id="dc195-118">WIA applications can use the value of WIA_DPS_DEVICE_ID to find, using the Function Discovery API, the function instance object representing the web services scanner device used in the current WIA 2.0 session.</span></span><br/> <span data-ttu-id="dc195-119">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-119">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <span data-ttu-id="dc195-120"><dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-120"><dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="dc195-121">Reserviert, nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="dc195-121">Reserved, do not use.</span></span><br/> <span data-ttu-id="dc195-122">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-122">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <span data-ttu-id="dc195-123"><dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-123"><dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="dc195-124">Reserviert, nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="dc195-124">Reserved, do not use.</span></span><br/> <span data-ttu-id="dc195-125">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-125">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <span data-ttu-id="dc195-126"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>scannerdevicedocumenthandlingfunktionen</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-126"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="dc195-127">Enthält die Funktionen des Scanners.</span><span class="sxs-lookup"><span data-stu-id="dc195-127">Contains the capabilities of the scanner.</span></span> <span data-ttu-id="dc195-128">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-128">The minidriver creates and maintains this property.</span></span> <br/> <span data-ttu-id="dc195-129">Eine Anwendung liest diese Eigenschaft, um zu bestimmen, ob für den Scanner ein Flatbed, ein Dokument Server oder ein Duplexer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="dc195-129">An application reads this property to determine whether the scanner has a flatbed, document feeder, or duplexer installed.</span></span> <span data-ttu-id="dc195-130">Diese Eigenschaft wird auch verwendet, um die installierten Features weiter zu definieren.</span><span class="sxs-lookup"><span data-stu-id="dc195-130">This property is also used to further define the installed features.</span></span><br/> <span data-ttu-id="dc195-131">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-131">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="dc195-132">In der folgenden Tabelle werden die Konstanten beschrieben, die nur mit Windows 7 gültig sind.</span><span class="sxs-lookup"><span data-stu-id="dc195-132">The following table describes the constants that are valid with Windows 7 only.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dc195-133">Flags</span><span class="sxs-lookup"><span data-stu-id="dc195-133">Flags</span></span></th>
<th><span data-ttu-id="dc195-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc195-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc195-135">AUTO_SOURCE</span><span class="sxs-lookup"><span data-stu-id="dc195-135">AUTO_SOURCE</span></span></td>
<td><span data-ttu-id="dc195-136">Auf dem Scanner ist ein automatischer Dokument Handler installiert.</span><span class="sxs-lookup"><span data-stu-id="dc195-136">The scanner has an automatic document handler installed.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="dc195-137">In der folgenden Tabelle werden die Konstanten beschrieben, die nur mit Windows 7 und Windows Vista gültig sind.</span><span class="sxs-lookup"><span data-stu-id="dc195-137">The following table describes the constants that are valid with Windows 7 and Windows Vista only.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dc195-138">Flags</span><span class="sxs-lookup"><span data-stu-id="dc195-138">Flags</span></span></th>
<th><span data-ttu-id="dc195-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc195-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc195-140">ADVANCED_DUP</span><span class="sxs-lookup"><span data-stu-id="dc195-140">ADVANCED_DUP</span></span></td>
<td><span data-ttu-id="dc195-141">Das Gerät unterstützt die erweiterte Duplex Scan Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="dc195-141">The device supports advanced duplex scan configuration.</span></span> <span data-ttu-id="dc195-142">Verwenden Sie WIA_IPS_DUPLEX_SETTINGS, um zwischen der Verwendung von grundlegenden und erweiterten Duplex Konfigurationen zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="dc195-142">Use WIA_IPS_DUPLEX_SETTINGS to switch between using basic and advanced duplex configurations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-143">DETECT_FILM_TPA</span><span class="sxs-lookup"><span data-stu-id="dc195-143">DETECT_FILM_TPA</span></span></td>
<td><span data-ttu-id="dc195-144">Der Scanner kann erkennen, wann der Transparenz-/Filteradapter zum Scannen bereit ist.</span><span class="sxs-lookup"><span data-stu-id="dc195-144">The scanner can detect when the transparency/film adapter is ready to scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-145">DETECT_STOR</span><span class="sxs-lookup"><span data-stu-id="dc195-145">DETECT_STOR</span></span></td>
<td><span data-ttu-id="dc195-146">Der Scanner kann erkennen, wenn Dokumente im internen Speicher vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="dc195-146">The scanner can detect when there are documents in the internal storage.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-147">FILM_TPA</span><span class="sxs-lookup"><span data-stu-id="dc195-147">FILM_TPA</span></span></td>
<td><span data-ttu-id="dc195-148">Der Scanner verfügt über einen Transparenz-/filterscanneradapter.</span><span class="sxs-lookup"><span data-stu-id="dc195-148">The scanner is equipped with a transparency/film scanning adapter.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-149">STOR</span><span class="sxs-lookup"><span data-stu-id="dc195-149">STOR</span></span></td>
<td><span data-ttu-id="dc195-150">Der Scanner ist mit einem internen Image Speichergerät ausgestattet.</span><span class="sxs-lookup"><span data-stu-id="dc195-150">The scanner is equipped with an internal image storage device.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="dc195-151">In der folgenden Tabelle werden die Konstanten beschrieben, die mit Windows XP oder höher gültig sind.</span><span class="sxs-lookup"><span data-stu-id="dc195-151">The following table describes the constants that are valid with Windows XP or later.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dc195-152">Flags</span><span class="sxs-lookup"><span data-stu-id="dc195-152">Flags</span></span></th>
<th><span data-ttu-id="dc195-153">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc195-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc195-154">DETECT_FEED</span><span class="sxs-lookup"><span data-stu-id="dc195-154">DETECT_FEED</span></span></td>
<td><span data-ttu-id="dc195-155">Der Scanner kann ein Dokument im-Feeder erkennen.</span><span class="sxs-lookup"><span data-stu-id="dc195-155">The scanner can detect a document in the feeder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-156">DETECT_FLAT</span><span class="sxs-lookup"><span data-stu-id="dc195-156">DETECT_FLAT</span></span></td>
<td><span data-ttu-id="dc195-157">Der Scanner kann ein Dokument auf dem flachen Platen erkennen.</span><span class="sxs-lookup"><span data-stu-id="dc195-157">The scanner can detect a document on the flatbed platen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-158">DETECT_SCAN</span><span class="sxs-lookup"><span data-stu-id="dc195-158">DETECT_SCAN</span></span></td>
<td><span data-ttu-id="dc195-159">Der Scanner kann ein Dokument im Draht nur durch Scannen erkennen.</span><span class="sxs-lookup"><span data-stu-id="dc195-159">The scanner can detect a document in the feeder only by scanning.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-160">Sammlungen</span><span class="sxs-lookup"><span data-stu-id="dc195-160">DUP</span></span></td>
<td><span data-ttu-id="dc195-161">Der Scanner verfügt über einen Duplexer.</span><span class="sxs-lookup"><span data-stu-id="dc195-161">The scanner has a duplexer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-162">Nährt</span><span class="sxs-lookup"><span data-stu-id="dc195-162">FEED</span></span></td>
<td><span data-ttu-id="dc195-163">Auf dem Scanner ist ein automatischer Dokument Handler installiert.</span><span class="sxs-lookup"><span data-stu-id="dc195-163">The scanner has an automatic document handler installed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-164">Rate</span><span class="sxs-lookup"><span data-stu-id="dc195-164">FLAT</span></span></td>
<td><span data-ttu-id="dc195-165">Der Scanner verfügt über eine flache Plate.</span><span class="sxs-lookup"><span data-stu-id="dc195-165">The scanner has a flatbed platen.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="dc195-166">In der folgenden Tabelle werden die Konstanten beschrieben, die nur mit Windows XP gültig sind.</span><span class="sxs-lookup"><span data-stu-id="dc195-166">The following table describes the constants that are valid with Windows XP only.</span></span> <span data-ttu-id="dc195-167">Diese Werte sind für Windows 7 und Windows Vista veraltet und sollten nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc195-167">These values have been deprecated for Windows 7 and Windows Vista and should not be used.</span></span></p>
<p></p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dc195-168">Flags</span><span class="sxs-lookup"><span data-stu-id="dc195-168">Flags</span></span></th>
<th><span data-ttu-id="dc195-169">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc195-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc195-170">DETECT_DUP</span><span class="sxs-lookup"><span data-stu-id="dc195-170">DETECT_DUP</span></span></td>
<td><span data-ttu-id="dc195-171">Der Scanner kann eine Duplex Scan Anforderung vom Benutzer erkennen.</span><span class="sxs-lookup"><span data-stu-id="dc195-171">The scanner can detect a duplex scan request from the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-172">DETECT_DUP_AVAIL</span><span class="sxs-lookup"><span data-stu-id="dc195-172">DETECT_DUP_AVAIL</span></span></td>
<td><span data-ttu-id="dc195-173">Der Scanner kann erkennen, wenn Duplexer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="dc195-173">The scanner can tell when the duplexer is installed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-174">DETECT_FEED_AVAIL</span><span class="sxs-lookup"><span data-stu-id="dc195-174">DETECT_FEED_AVAIL</span></span></td>
<td><span data-ttu-id="dc195-175">Der Scanner kann erkennen, wann die automatische Dokument-feestallation installiert ist.</span><span class="sxs-lookup"><span data-stu-id="dc195-175">The scanner can tell when the automatic document feeder is installed.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <span data-ttu-id="dc195-176"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>scannerdevicedocumenthandlingselect</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-176"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-177">Diese Eigenschaft wird in Windows Vista und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-177">This property is not supported in Windows Vista and later.</span></span> <span data-ttu-id="dc195-178">Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-178">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-179">Enthält die aktuelle Scanner-Erfassungs Quelle und den aktuellen Modus. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-179">Contains the current scanner acquisition source and mode.The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="dc195-180">Eine Anwendung liest diese Eigenschaft, um die aktuelle Erwerbs Quelle des Scanners zu ermitteln oder diese Eigenschaft zu schreiben, um die Quelle und den Modus des Scanners festzulegen.</span><span class="sxs-lookup"><span data-stu-id="dc195-180">An application reads this property to determine the current acquisition source of the scanner or to write this property to set the source and mode of the scanner.</span></span> <span data-ttu-id="dc195-181">Außerdem verwenden Anwendungen diese Eigenschaft, um die Duplexer-Funktionalität zu aktivieren und zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="dc195-181">In addition, applications use this property to enable and disable duplexer functionality.</span></span></p>
<p><span data-ttu-id="dc195-182">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span><span class="sxs-lookup"><span data-stu-id="dc195-182">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></span></span></p>
<p><span data-ttu-id="dc195-183">Die folgende Tabelle enthält die zehn Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="dc195-183">The following table has the ten constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dc195-184">Flags</span><span class="sxs-lookup"><span data-stu-id="dc195-184">Flags</span></span></th>
<th><span data-ttu-id="dc195-185">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc195-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc195-186">Draht</span><span class="sxs-lookup"><span data-stu-id="dc195-186">FEEDER</span></span></td>
<td><span data-ttu-id="dc195-187">Mit dem Dokument-Feeder Scan Vorgang.</span><span class="sxs-lookup"><span data-stu-id="dc195-187">Scan using the document feeder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-188">Flach</span><span class="sxs-lookup"><span data-stu-id="dc195-188">FLATBED</span></span></td>
<td><span data-ttu-id="dc195-189">Überprüfen Sie mit dem Flatbed.</span><span class="sxs-lookup"><span data-stu-id="dc195-189">Scan using the flatbed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-190">Gelegene</span><span class="sxs-lookup"><span data-stu-id="dc195-190">DUPLEX</span></span></td>
<td><span data-ttu-id="dc195-191">Mithilfe von Duplexer-Vorgängen scannen.</span><span class="sxs-lookup"><span data-stu-id="dc195-191">Scan using duplexer operations.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-192">AUTO_ADVANCE</span><span class="sxs-lookup"><span data-stu-id="dc195-192">AUTO_ADVANCE</span></span></td>
<td><span data-ttu-id="dc195-193">Aktiviert das automatische füttern des nächsten Dokuments nach einem Scanvorgang.</span><span class="sxs-lookup"><span data-stu-id="dc195-193">Enables automatic feeding of the next document after a scan.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-194">FRONT_FIRST</span><span class="sxs-lookup"><span data-stu-id="dc195-194">FRONT_FIRST</span></span></td>
<td><span data-ttu-id="dc195-195">Scannen Sie zuerst den Anfang des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="dc195-195">Scan the front of the document first.</span></span> <span data-ttu-id="dc195-196">Dieser Wert ist gültig, wenn Duplex festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dc195-196">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-197">BACK_FIRST</span><span class="sxs-lookup"><span data-stu-id="dc195-197">BACK_FIRST</span></span></td>
<td><span data-ttu-id="dc195-198">Scannen Sie zuerst das Dokument zurück.</span><span class="sxs-lookup"><span data-stu-id="dc195-198">Scan the back of the document first.</span></span> <span data-ttu-id="dc195-199">Dieser Wert ist gültig, wenn Duplex festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dc195-199">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-200">FRONT_ONLY</span><span class="sxs-lookup"><span data-stu-id="dc195-200">FRONT_ONLY</span></span></td>
<td><span data-ttu-id="dc195-201">Nur den Vordergrund suchen.</span><span class="sxs-lookup"><span data-stu-id="dc195-201">Scan the front only.</span></span> <span data-ttu-id="dc195-202">Dieser Wert ist gültig, wenn Duplex festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dc195-202">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-203">BACK_ONLY</span><span class="sxs-lookup"><span data-stu-id="dc195-203">BACK_ONLY</span></span></td>
<td><span data-ttu-id="dc195-204">Nur Rück scannen.</span><span class="sxs-lookup"><span data-stu-id="dc195-204">Scan the back only.</span></span> <span data-ttu-id="dc195-205">Dieser Wert ist gültig, wenn Duplex festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dc195-205">This value is valid when DUPLEX is set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-206">NEXT_PAGE</span><span class="sxs-lookup"><span data-stu-id="dc195-206">NEXT_PAGE</span></span></td>
<td><span data-ttu-id="dc195-207">Scannen Sie die nächste Seite des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="dc195-207">Scan the next page of the document.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-208">Vorab Feed</span><span class="sxs-lookup"><span data-stu-id="dc195-208">PREFEED</span></span></td>
<td><span data-ttu-id="dc195-209">Aktivieren Sie den Vorfeed-Modus.</span><span class="sxs-lookup"><span data-stu-id="dc195-209">Enable pre-feed mode.</span></span> <span data-ttu-id="dc195-210">Das nächste Dokument wird beim Scannen vorab positioniert.</span><span class="sxs-lookup"><span data-stu-id="dc195-210">Pre-position next document while scanning.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <span data-ttu-id="dc195-211"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>scannerdevicedocumenthandlingstatus</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-211"><dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="dc195-212">Enthält den aktuellen Status des installierten, bereinigten, Dokument-oder Duplexer-Elements des Scanners.</span><span class="sxs-lookup"><span data-stu-id="dc195-212">Contains current state of the scanner's installed flatbed, document feeder, or duplexer.</span></span> <span data-ttu-id="dc195-213">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-213">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="dc195-214">Diese Eigenschaft wird von einer Anwendung gelesen, um zu bestimmen, ob das Scanner-Gerät zur Verwendung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="dc195-214">An application reads this property to determine whether the scanner device is ready to be used.</span></span> <span data-ttu-id="dc195-215">Dies ist eine ideale Möglichkeit, um zu überprüfen, ob sich das Papier vor dem Erwerb eines Images im Draht befindet.</span><span class="sxs-lookup"><span data-stu-id="dc195-215">This is an ideal way to check whether paper is in the feeder prior to acquiring an image.</span></span></p>
<p><span data-ttu-id="dc195-216">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-216">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="dc195-217">Die folgende Tabelle enthält die Konstanten, die mit dieser Eigenschaft gültig sind. Ein Sternchen \* gibt an, dass das Flag in Windows Vista oder höher nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="dc195-217">The following table has the constants that are valid with this property.An asterisk \* indicates that the flag is not supported in Windows Vista or later.</span></span> <span data-ttu-id="dc195-218">Das Symbol <strong>V</strong> gibt an, dass das Flag nur in Windows Vista und höher unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="dc195-218">The <strong>V</strong> symbol indicates that the flag is supported only in Windows Vista and later.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dc195-219">Flags</span><span class="sxs-lookup"><span data-stu-id="dc195-219">Flags</span></span></th>
<th><span data-ttu-id="dc195-220">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc195-220">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc195-221">FEED_READY</span><span class="sxs-lookup"><span data-stu-id="dc195-221">FEED_READY</span></span></td>
<td><span data-ttu-id="dc195-222">Der Flatbed ist einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="dc195-222">The flatbed is ready for use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-223">FLAT_READY</span><span class="sxs-lookup"><span data-stu-id="dc195-223">FLAT_READY</span></span></td>
<td><span data-ttu-id="dc195-224">Der Scanner verfügt über ein Dokument auf der Registerkarte "Flatbed".</span><span class="sxs-lookup"><span data-stu-id="dc195-224">The scanner has a document on the flatbed platen.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-225">DUP_READY</span><span class="sxs-lookup"><span data-stu-id="dc195-225">DUP_READY</span></span></td>
<td><span data-ttu-id="dc195-226">Der Duplexer ist aktiviert und kann verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc195-226">The duplexer is enabled and ready to be used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-227">FLAT_COVER_UP</span><span class="sxs-lookup"><span data-stu-id="dc195-227">FLAT_COVER_UP</span></span></td>
<td><span data-ttu-id="dc195-228">Die flache Abdeckung ist aktiv.</span><span class="sxs-lookup"><span data-stu-id="dc195-228">The flat bed cover is up.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-229">PATH_COVER_UP</span><span class="sxs-lookup"><span data-stu-id="dc195-229">PATH_COVER_UP</span></span></td>
<td><span data-ttu-id="dc195-230">Der Papierpfad wird behandelt und verhindert den ordnungsgemäßen Betrieb.</span><span class="sxs-lookup"><span data-stu-id="dc195-230">The paper path is covered up and is preventing proper operation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-231">PAPER_JAM</span><span class="sxs-lookup"><span data-stu-id="dc195-231">PAPER_JAM</span></span></td>
<td><span data-ttu-id="dc195-232">Ein Dokument wird im Dokument-feemed blockiert.</span><span class="sxs-lookup"><span data-stu-id="dc195-232">A document is jammed in the document feeder.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-233">FILM_TPA_READY<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="dc195-233">FILM_TPA_READY<strong>V</strong></span></span></td>
<td><span data-ttu-id="dc195-234">Der Transparenz Adapter ist installiert und einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="dc195-234">The transparency adapter is installed and ready for use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-235">STORAGE_READY<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="dc195-235">STORAGE_READY<strong>V</strong></span></span></td>
<td><span data-ttu-id="dc195-236">Das interne Speichergerät ist bereit.</span><span class="sxs-lookup"><span data-stu-id="dc195-236">The internal storage device is ready.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-237">STORAGE_FULL<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="dc195-237">STORAGE_FULL<strong>V</strong></span></span></td>
<td><span data-ttu-id="dc195-238">Der Speicher ist voll, es sind keine Uploadvorgänge möglich.</span><span class="sxs-lookup"><span data-stu-id="dc195-238">The storage is full, no upload operations possible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-239">MULTIPLE_FEED<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="dc195-239">MULTIPLE_FEED<strong>V</strong></span></span></td>
<td><span data-ttu-id="dc195-240">Es ist eine mehrfach Feed-Bedingung aufgetreten (normalerweise mit einem PAPER_JAM).</span><span class="sxs-lookup"><span data-stu-id="dc195-240">A multiple feed condition occurred (usually with a PAPER_JAM).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-241">DEVICE_ATTENTION<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="dc195-241">DEVICE_ATTENTION<strong>V</strong></span></span></td>
<td><span data-ttu-id="dc195-242">Es ist ein Fehler aufgetreten, der einen Benutzereingriff auf dem Gerät erfordert.</span><span class="sxs-lookup"><span data-stu-id="dc195-242">There is an error that requires user intervention on the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-243">LAMP_ERR<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="dc195-243">LAMP_ERR<strong>V</strong></span></span></td>
<td><span data-ttu-id="dc195-244">Der Scanner ist aufgrund eines Lamp-Problems nicht bereit.</span><span class="sxs-lookup"><span data-stu-id="dc195-244">The scanner is not ready due to a lamp problem.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <span data-ttu-id="dc195-245"><dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>scannerdeviceendorsercharacters</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-245"><dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="dc195-246">Enthält alle gültigen Zeichen, die eine Anwendung verwenden kann, um gültige Endorser-Zeichen folgen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dc195-246">Contains all the valid characters that an application can use to create valid endorser strings.</span></span> <span data-ttu-id="dc195-247">Ein Endorser ist ein Drucker, der auf einem Scanner installiert ist, der eine Textnachricht auf jeder gescannten Seite ausgibt.</span><span class="sxs-lookup"><span data-stu-id="dc195-247">An endorser is a printer installed on a scanner that imprints a text message on every page scanned.</span></span> <span data-ttu-id="dc195-248">Der Mini Treiber sollte die Einstellung der <strong>WIA_DPS_ENDORSER_STRING</strong> -Eigenschaft mit dem gültigen Zeichensatz in dieser Eigenschaft überprüfen.</span><span class="sxs-lookup"><span data-stu-id="dc195-248">The minidriver should validate the setting of the <strong>WIA_DPS_ENDORSER_STRING</strong> property against the valid character set in this property.</span></span> <span data-ttu-id="dc195-249">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-249">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="dc195-250">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-250">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <span data-ttu-id="dc195-251"><dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>scannerdeviceendorserstring</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-251"><dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="dc195-252">Enthält eine Zeichenfolge, die auf jeder Seite, die der Mini Treiber scannt, unterstützt werden soll (d. h. gedruckt).</span><span class="sxs-lookup"><span data-stu-id="dc195-252">Contains a string that is to be endorsed (in other words, printed) on each page that the minidriver scans.</span></span> <span data-ttu-id="dc195-253">Eine Anwendung legt diese Eigenschaft mithilfe des gültigen Zeichensatzes fest, der in der <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> -Eigenschaft gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="dc195-253">An application sets this property using the valid character set that is reported in the <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> property.</span></span> <span data-ttu-id="dc195-254">Der Mini Treiber sollte Dokumente nur dann unterstützen, wenn eine Zeichenfolge in dieser Eigenschaft festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dc195-254">The minidriver should endorse documents only if a string is set in this property.</span></span> <span data-ttu-id="dc195-255">Eine leere Zeichenfolge bedeutet, dass die Endorser-Funktionalität deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="dc195-255">An empty string means that the endorser functionality is disabled.</span></span></p>
<p><span data-ttu-id="dc195-256">Da es für den Treiber zuständig ist, die Endorser-Zeichenfolge zu interpretieren, kann der Treiber Sonderzeichen in <strong>WIA_DPS_ENDORSER_STRING</strong>verwenden.</span><span class="sxs-lookup"><span data-stu-id="dc195-256">Because it is the driver's responsibility to interpret the endorser string, your driver can use special characters in <strong>WIA_DPS_ENDORSER_STRING</strong>.</span></span> <span data-ttu-id="dc195-257">Diese Zeichen werden jedoch nur von Ihren Anwendungen interpretiert.</span><span class="sxs-lookup"><span data-stu-id="dc195-257">However, only your applications would understand these characters.</span></span></p>
<p><span data-ttu-id="dc195-258">Typ: <strong>VT_BSTR</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-258">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="dc195-259">Ein Treiber, der die <strong>WIA_DPS_ENDORSER_STRING</strong> -Eigenschaft unterstützt, muss die folgende Liste von Token unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dc195-259">A driver supporting the <strong>WIA_DPS_ENDORSER_STRING</strong> property must support the following list of tokens.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dc195-260">Token</span><span class="sxs-lookup"><span data-stu-id="dc195-260">Token</span></span></th>
<th><span data-ttu-id="dc195-261">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc195-261">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc195-262">$Date $</span><span class="sxs-lookup"><span data-stu-id="dc195-262">$DATE$</span></span></td>
<td><span data-ttu-id="dc195-263">Das Datum im Format yyyy/mm/dd.</span><span class="sxs-lookup"><span data-stu-id="dc195-263">The date in the form YYYY/MM/DD.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-264">$Day $</span><span class="sxs-lookup"><span data-stu-id="dc195-264">$DAY$</span></span></td>
<td><span data-ttu-id="dc195-265">Der Tag in der Form DD.</span><span class="sxs-lookup"><span data-stu-id="dc195-265">The day in the form DD.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-266">$MONTH $</span><span class="sxs-lookup"><span data-stu-id="dc195-266">$MONTH$</span></span></td>
<td><span data-ttu-id="dc195-267">Der Monat des Jahres in der Form mm.</span><span class="sxs-lookup"><span data-stu-id="dc195-267">The month of the year in the form MM.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-268">$Page _Count $</span><span class="sxs-lookup"><span data-stu-id="dc195-268">$PAGE_COUNT$</span></span></td>
<td><span data-ttu-id="dc195-269">Die Anzahl der übertragenen Seiten.</span><span class="sxs-lookup"><span data-stu-id="dc195-269">The number of pages transferred.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-270">$Time $</span><span class="sxs-lookup"><span data-stu-id="dc195-270">$TIME$</span></span></td>
<td><span data-ttu-id="dc195-271">Die Uhrzeit im Format hh: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="dc195-271">The time of day in the form HH:MM:SS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-272">$Year $</span><span class="sxs-lookup"><span data-stu-id="dc195-272">$YEAR$</span></span></td>
<td><span data-ttu-id="dc195-273">Das Jahr im Format yyyy.</span><span class="sxs-lookup"><span data-stu-id="dc195-273">The year in the form YYYY.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <span data-ttu-id="dc195-274"><dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-274"><dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="dc195-275">Reserviert, nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="dc195-275">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="dc195-276">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-276">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <span data-ttu-id="dc195-277"><dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>scannerdecoeglobalidentity</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-277"><dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-278">Diese Eigenschaft wird nur unter Windows Vista und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-278">This property is supported only on Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-279">Enthält die SOAP-Adresse eines Webdienst-Scanner-Geräts.</span><span class="sxs-lookup"><span data-stu-id="dc195-279">Contains the SOAP address of a web services scanner device.</span></span> <span data-ttu-id="dc195-280">Der WIA 2,0-Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-280">The WIA 2.0 mini-driver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="dc195-281">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-281">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <span data-ttu-id="dc195-282"><dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>scannerdevicehorizontalbedregistration</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-282"><dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-283">Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-283">This property is not supported with Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-284">Enthält die Registrierung bzw. die horizontale Ausrichtung für Dokumente, die im Flatbed abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dc195-284">Contains the registration, or horizontal alignment, for documents placed on the flatbed.</span></span> <span data-ttu-id="dc195-285">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-285">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="dc195-286">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-286">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="dc195-287">Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="dc195-287">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dc195-288">Konstante</span><span class="sxs-lookup"><span data-stu-id="dc195-288">Constant</span></span></th>
<th><span data-ttu-id="dc195-289">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc195-289">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc195-290">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="dc195-290">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="dc195-291">Das Papier wird linksbündig ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="dc195-291">The paper is left justified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-292">Ego</span><span class="sxs-lookup"><span data-stu-id="dc195-292">CENTERED</span></span></td>
<td><span data-ttu-id="dc195-293">Das Dokument wird zentriert.</span><span class="sxs-lookup"><span data-stu-id="dc195-293">The paper is centered.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-294">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="dc195-294">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="dc195-295">Das Dokument ist rechtsbündig ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="dc195-295">The paper is right justified.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="dc195-296"><strong>Siehe auch</strong></span><span class="sxs-lookup"><span data-stu-id="dc195-296"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="dc195-297"><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="dc195-297"><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <span data-ttu-id="dc195-298"><dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>scannerdebug size</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-298"><dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-299">Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-299">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="dc195-300">Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-300">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-301">Gibt die maximale Breite (in Tausendstel Zoll) an, die in der horizontalen Achse (X-Achse) von den Platen eines Flatbed-Scanners bei der aktuellen Auflösung gescannt wird.</span><span class="sxs-lookup"><span data-stu-id="dc195-301">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis from the platen of a flatbed scanner at the current resolution.</span></span> <span data-ttu-id="dc195-302">Diese Eigenschaft gilt auch für automatische Dokument Feeden, die Blätter zum Scannen in die Plate eines flatsheet-Scanners verschieben.</span><span class="sxs-lookup"><span data-stu-id="dc195-302">This property also applies to automatic document feeders that move sheets to the platen of a flatbed scanner for scanning.</span></span> <span data-ttu-id="dc195-303">Diese Eigenschaft ist für Scanner mit einem Platen obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="dc195-303">This property is mandatory for scanners that have a platen.</span></span> <span data-ttu-id="dc195-304">Andere Scannertypen implementieren stattdessen die <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-304">Other scanner types will instead implement the <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> property.</span></span></p>
<p><span data-ttu-id="dc195-305">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-305">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <span data-ttu-id="dc195-306"><dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>scannerdebug feedsize</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-306"><dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-307">Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-307">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="dc195-308">Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-308">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-309">Gibt die maximale Breite (in Tausendstel Zoll) an, die auf der horizontalen Achse (X-Achse) von einem Hand Held-oder Blatt Feed-Scanner bei der aktuellen Auflösung gescannt wird.</span><span class="sxs-lookup"><span data-stu-id="dc195-309">Specifies the maximum width, in thousandths of an inch, that is scanned in the horizontal (X) axis from a handheld or sheet feed scanner at the current resolution.</span></span> <span data-ttu-id="dc195-310">Diese Eigenschaft gilt auch für automatische Dokument Feeden, die durchsucht werden, ohne Blätter in die Plate eines flachen Scanners zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="dc195-310">This property also applies to automatic document feeders that scan without moving sheets to the platen of a flatbed scanner.</span></span> <span data-ttu-id="dc195-311">Diese Eigenschaft ist für Blatt-, Scroll-und handgehaltene Scanner obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="dc195-311">This property is mandatory for sheet-fed, scroll-fed, and hand-held scanners.</span></span></p>
<p><span data-ttu-id="dc195-312">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-312">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <span data-ttu-id="dc195-313"><dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>scannerdevicemaxscantime</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-313"><dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="dc195-314">Enthält die maximale Zeit zum Scannen einer einzelnen Seite mit den aktuellen Eigenschaften Einstellungen in Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="dc195-314">Contains the maximum time to scan a single page with the current property settings, in milliseconds.</span></span> <span data-ttu-id="dc195-315">Diese Eigenschaft wird von einer Anwendung gelesen, um zu schätzen, wie lange es dauert, bis eine Seite gescannt wird.</span><span class="sxs-lookup"><span data-stu-id="dc195-315">An application reads this property to estimate the time it will take to scan a page.</span></span> <span data-ttu-id="dc195-316">Dies ist hilfreich, wenn Sie die Bedingungen eines Geräts ermitteln, das nicht mehr reagiert.</span><span class="sxs-lookup"><span data-stu-id="dc195-316">This is helpful when determining the conditions of a device that has stopped responding.</span></span> <span data-ttu-id="dc195-317">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-317">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="dc195-318">Diese Eigenschaft ist für alle Scanner erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dc195-318">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="dc195-319">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-319">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <span data-ttu-id="dc195-320"><dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>scannerde viceminhorizontalsheetfeedsize</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-320"><dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-321">Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-321">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="dc195-322">Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-322">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-323">Enthält die physischen horizontalen Dimensionen der kleinsten Seite, die der Dokument-Draht Scanner in Tausendstel Zoll Scannen kann.</span><span class="sxs-lookup"><span data-stu-id="dc195-323">Contains the physical horizontal dimensions of the smallest page that the scanner's document feeder can scan, in thousandths of an inch.</span></span> <span data-ttu-id="dc195-324">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-324">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="dc195-325">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-325">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="dc195-326"><strong>Siehe auch</strong></span><span class="sxs-lookup"><span data-stu-id="dc195-326"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="dc195-327"><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="dc195-327"><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <span data-ttu-id="dc195-328"><dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>scannerdecoeminverticalsheetfeedsize</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-328"><dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-329">Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-329">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="dc195-330">Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-330">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-331">Enthält die physischen vertikalen Dimensionen der kleinsten Seite, die der Dokument-Draht Scanner in Tausendstel Zoll Scannen kann.</span><span class="sxs-lookup"><span data-stu-id="dc195-331">Contains the physical vertical dimensions of the smallest page that the scanner's document feeder can scan, in thousandths of an inch.</span></span> <span data-ttu-id="dc195-332">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-332">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="dc195-333">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-333">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="dc195-334"><strong>Siehe auch</strong></span><span class="sxs-lookup"><span data-stu-id="dc195-334"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="dc195-335"><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="dc195-335"><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <span data-ttu-id="dc195-336"><dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>scannerdeviceopticalxres</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-336"><dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-337">Diese Eigenschaft wird von Windows Vista nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-337">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="dc195-338">Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-338">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-339">Horizontale optische Auflösung.</span><span class="sxs-lookup"><span data-stu-id="dc195-339">Horizontal Optical Resolution.</span></span> <span data-ttu-id="dc195-340">Höchste unterstützte horizontale optische Auflösung in dpi.</span><span class="sxs-lookup"><span data-stu-id="dc195-340">Highest supported horizontal optical resolution in DPI.</span></span> <span data-ttu-id="dc195-341">Diese Eigenschaft ist ein einzelner Wert.</span><span class="sxs-lookup"><span data-stu-id="dc195-341">This property is a single value.</span></span> <span data-ttu-id="dc195-342">Dabei handelt es sich nicht um eine Liste aller Auflösungen, die vom Gerät generiert werden können.</span><span class="sxs-lookup"><span data-stu-id="dc195-342">This is not a list of all resolutions that can be generated by the device.</span></span> <span data-ttu-id="dc195-343">Vielmehr handelt es sich hierbei um die Auflösung der Geräte Optiken.</span><span class="sxs-lookup"><span data-stu-id="dc195-343">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="dc195-344">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-344">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="dc195-345">Diese Eigenschaft ist für alle Scanner erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dc195-345">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="dc195-346">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-346">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <span data-ttu-id="dc195-347"><dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>scannerdeviceopticalyres</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-347"><dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-348">Diese Eigenschaft wird von Windows Vista nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-348">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="dc195-349">Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-349">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-350">Vertikale optische Auflösung.</span><span class="sxs-lookup"><span data-stu-id="dc195-350">Vertical Optical Resolution.</span></span> <span data-ttu-id="dc195-351">Höchste unterstützte vertikale optische Auflösung in dpi.</span><span class="sxs-lookup"><span data-stu-id="dc195-351">Highest supported vertical optical resolution in DPI.</span></span> <span data-ttu-id="dc195-352">Diese Eigenschaft ist ein einzelner Wert.</span><span class="sxs-lookup"><span data-stu-id="dc195-352">This property is a single value.</span></span> <span data-ttu-id="dc195-353">Dabei handelt es sich nicht um eine Liste aller Auflösungen, die vom Gerät generiert werden.</span><span class="sxs-lookup"><span data-stu-id="dc195-353">This is not a list of all resolutions that are generated by the device.</span></span> <span data-ttu-id="dc195-354">Vielmehr handelt es sich hierbei um die Auflösung der Geräte Optiken.</span><span class="sxs-lookup"><span data-stu-id="dc195-354">Rather, this is the resolution of the device's optics.</span></span> <span data-ttu-id="dc195-355">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-355">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="dc195-356">Diese Eigenschaft ist für alle Scanner erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dc195-356">This property is required for all scanners.</span></span></p>
<p><span data-ttu-id="dc195-357">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-357">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <span data-ttu-id="dc195-358"><dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>scannerdeviceorientation</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-358"><dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="dc195-359">Enthält die aktuelle Ausrichtungs Einstellung. Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-359">Contains the current orientation setting.The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="dc195-360">In einer Anwendung wird die <strong>WIA_DPS_ORIENTATION</strong> -Eigenschaft festgelegt, um die ursprüngliche Ausrichtung einer abzurufenden Seite oder eines Bilds zu definieren.</span><span class="sxs-lookup"><span data-stu-id="dc195-360">An application sets the <strong>WIA_DPS_ORIENTATION</strong> property to define the original orientation of a page or image to be acquired.</span></span> <span data-ttu-id="dc195-361">Weitere Informationen zur Verwendung von WIA_DPS_ORIENTATION finden Sie unter <strong>WIA_DPS_PAGE_SIZE</strong></span><span class="sxs-lookup"><span data-stu-id="dc195-361">For information on how to use WIA_DPS_ORIENTATION, see <strong>WIA_DPS_PAGE_SIZE</strong></span></span></p>
<p><span data-ttu-id="dc195-362">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="dc195-362">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="dc195-363">Die folgende Tabelle enthält die vier Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="dc195-363">The following table has the four constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dc195-364">Wert</span><span class="sxs-lookup"><span data-stu-id="dc195-364">Value</span></span></th>
<th><span data-ttu-id="dc195-365">Definition</span><span class="sxs-lookup"><span data-stu-id="dc195-365">Defination</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc195-366">Landschaf</span><span class="sxs-lookup"><span data-stu-id="dc195-366">LANDSCAPE</span></span></td>
<td><span data-ttu-id="dc195-367">90-Grad-Drehung gegen den Uhrzeigersinn, relativ zur Hochformat Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="dc195-367">90-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-368">Hochformat</span><span class="sxs-lookup"><span data-stu-id="dc195-368">PORTRAIT</span></span></td>
<td><span data-ttu-id="dc195-369">0 Grad.</span><span class="sxs-lookup"><span data-stu-id="dc195-369">0 degrees.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-370">ROT180</span><span class="sxs-lookup"><span data-stu-id="dc195-370">ROT180</span></span></td>
<td><span data-ttu-id="dc195-371">180-Grad-Drehung gegen den Uhrzeigersinn, relativ zur Hochformat Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="dc195-371">180-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-372">ROT270</span><span class="sxs-lookup"><span data-stu-id="dc195-372">ROT270</span></span></td>
<td><span data-ttu-id="dc195-373">270-Grad-Drehung gegen den Uhrzeigersinn, relativ zur Hochformat Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="dc195-373">270-degree counter-clockwise rotation, relative to the PORTRAIT orientation.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="dc195-374"><strong>Siehe auch</strong></span><span class="sxs-lookup"><span data-stu-id="dc195-374"><strong>See Also</strong></span></span></p>
<p><span data-ttu-id="dc195-375"><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="dc195-375"><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <span data-ttu-id="dc195-376"><dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>scannerdecoepadcolor</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-376"><dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="dc195-377">Die Farbe, die zum Auffüllen verwendet wird, wenn nicht genügend Bild Daten zum Auffüllen eines angeforderten Puffers vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="dc195-377">Color used to pad when there is not enough image data to fill a requested buffer.</span></span> <span data-ttu-id="dc195-378">Diese Eigenschaft wird für Scanner implementiert, die den Puffer auffüllen.</span><span class="sxs-lookup"><span data-stu-id="dc195-378">This property is implemented for scanners that pad the buffer.</span></span> <span data-ttu-id="dc195-379">Diese Eigenschaft ist für alle Scanner optional.</span><span class="sxs-lookup"><span data-stu-id="dc195-379">This property is optional for all scanners.</span></span> <span data-ttu-id="dc195-380">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-380">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="dc195-381">Typ: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-381">Type: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="dc195-382">Das Format der Farbinformationen ist <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">rgbquad</a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-382">The format of the color information is <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <span data-ttu-id="dc195-383"><dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>scannerdevicepageheight</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-383"><dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-384">Diese Eigenschaft wird von Windows Vista nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-384">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="dc195-385">Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-385">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-386">Enthält die Höhe der aktuell ausgewählten Seite in Tausendstel Zoll.</span><span class="sxs-lookup"><span data-stu-id="dc195-386">Contains the height, in thousandths of an inch, of the currently selected page.</span></span> <span data-ttu-id="dc195-387">Der Mini Treiber erstellt und verwaltet die <strong>WIA_DPS_PAGE_HEIGHT</strong> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-387">The minidriver creates and maintains the <strong>WIA_DPS_PAGE_HEIGHT</strong> property.</span></span> <span data-ttu-id="dc195-388">Eine Anwendung liest diese Eigenschaft, um die physischen Dimensionen der zu scannenden Seite zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="dc195-388">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="dc195-389">Wenn sich die Block Einstellungen von den bekannten Seitengrößen unterscheiden, meldet diese Eigenschaft die Höhe der Seite, deren <strong>WIA_DPS_PAGE_SIZE</strong> -Eigenschaft auf WIA_PAGE_CUSTOM festgelegt ist (ein Wert der <strong>WIA_DPS_PAGE_SIZE</strong> -Eigenschaft).</span><span class="sxs-lookup"><span data-stu-id="dc195-389">If the extent settings are different from the known page sizes, this property reports the height of the page whose <strong>WIA_DPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM (which is a value of the <strong>WIA_DPS_PAGE_SIZE</strong> property).</span></span> <span data-ttu-id="dc195-390"><strong>WIA_DPS_PAGE_HEIGHT</strong> müssen mit <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>synchronisiert sein, das die Höhe der zu scannenden Seite in Pixel meldet.</span><span class="sxs-lookup"><span data-stu-id="dc195-390"><strong>WIA_DPS_PAGE_HEIGHT</strong> must be in sync with <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, which reports the height, in pixels, of the page to be scanned.</span></span></p>
<p><span data-ttu-id="dc195-391">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-391">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <span data-ttu-id="dc195-392"><dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>scannerdevicepagesize</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-392"><dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-393">Diese Eigenschaft wird von Windows Vista nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-393">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="dc195-394">Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-394">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-395">Enthält die Größe der Seite, die derzeit zum Scannen ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="dc195-395">Contains the size of the page that is currently selected to be scanned.</span></span> <span data-ttu-id="dc195-396">Um die Dimensionen der zu überprüfenden Seite auszuwählen, legt eine Anwendung diese Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="dc195-396">To select the dimensions of the page to scan, an application sets this property.</span></span> <span data-ttu-id="dc195-397">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-397">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="dc195-398">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="dc195-398">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="dc195-399">Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="dc195-399">The following table has the three constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dc195-400">Wert</span><span class="sxs-lookup"><span data-stu-id="dc195-400">Value</span></span></th>
<th><span data-ttu-id="dc195-401">Definition</span><span class="sxs-lookup"><span data-stu-id="dc195-401">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc195-402">WIA_PAGE_A4</span><span class="sxs-lookup"><span data-stu-id="dc195-402">WIA_PAGE_A4</span></span></td>
<td><span data-ttu-id="dc195-403">8267 X 11692 (Hochformat Ausrichtung)</span><span class="sxs-lookup"><span data-stu-id="dc195-403">8267 X 11692 (PORTRAIT orientation)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-404">WIA_PAGE_CUSTOM</span><span class="sxs-lookup"><span data-stu-id="dc195-404">WIA_PAGE_CUSTOM</span></span></td>
<td><span data-ttu-id="dc195-405">Definiert durch die Werte der Eigenschaften " <strong>WIA_DPS_PAGE_HEIGHT</strong> " und " <strong>WIA_DPS_PAGE_WIDTH</strong> ".</span><span class="sxs-lookup"><span data-stu-id="dc195-405">Defined by the values of the <strong>WIA_DPS_PAGE_HEIGHT</strong> and <strong>WIA_DPS_PAGE_WIDTH</strong> properties</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-406">WIA_PAGE_LETTER</span><span class="sxs-lookup"><span data-stu-id="dc195-406">WIA_PAGE_LETTER</span></span></td>
<td><span data-ttu-id="dc195-407">8500 X 11000 (Hochformat Ausrichtung)</span><span class="sxs-lookup"><span data-stu-id="dc195-407">8500 X 11000 (PORTRAIT orientation)</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="dc195-408">Der Wert der <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> -Eigenschaft bestimmt die Ausrichtung der aktuell ausgewählten Seite.</span><span class="sxs-lookup"><span data-stu-id="dc195-408">The value of the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property determines the orientation of the currently selected page.</span></span> <span data-ttu-id="dc195-409">Die Eigenschaften " <strong>WIA_DPS_PAGE_WIDTH</strong> " und " <strong>WIA_DPS_PAGE_HEIGHT</strong> " melden die Dimensionen der Seite in Tausendstel Zoll.</span><span class="sxs-lookup"><span data-stu-id="dc195-409">The <strong>WIA_DPS_PAGE_WIDTH</strong> and <strong>WIA_DPS_PAGE_HEIGHT</strong> properties report the page's dimensions, in thousandths of an inch.</span></span> <span data-ttu-id="dc195-410">Beachten Sie, dass diese Eigenschaften mit <strong>WIA_IPS_XEXTENT</strong> und <strong>WIA_IPS_YEXTENT</strong>übereinstimmen müssen, die die Abmessungen der Seite in Pixel enthalten.</span><span class="sxs-lookup"><span data-stu-id="dc195-410">Note that these properties must be in agreement with <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong>, which contain the page's dimensions in pixels.</span></span> <span data-ttu-id="dc195-411">Gültige Werte vom Typ "WIA_PROP_LIST" sollten von gültigen Einstellungen der Eigenschaft " <strong>WIA_IPS_ORIENTATION</strong> " abhängen.</span><span class="sxs-lookup"><span data-stu-id="dc195-411">Valid values of type WIA_PROP_LIST should depend on valid settings of the <strong>WIA_IPS_ORIENTATION</strong> property.</span></span> <span data-ttu-id="dc195-412">Wenn das Gerät keine Querformat orientierten Dokumente mit einer WIA_PAGE_A4 Einstellung Scannen kann, sollten WIA_PAGE_A4 nicht in der Liste der gültigen Werte für die <strong>WIA_DPS_PAGE_SIZE</strong> -Eigenschaft angezeigt werden, wenn <strong>WIA_IPS_ORIENTATION</strong> auf lanscape festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dc195-412">If the device cannot scan landscape-oriented documents with a WIA_PAGE_A4 setting, WIA_PAGE_A4 should not appear in the list of valid values for the <strong>WIA_DPS_PAGE_SIZE</strong> property when <strong>WIA_IPS_ORIENTATION</strong> is set to LANSCAPE.</span></span></p>
<p><span data-ttu-id="dc195-413">Wenn eine Anwendung <strong>WIA_DPS_PAGE_SIZE</strong> auf einen anderen Wert als WIA_PAGE_CUSTOM festlegt, sollte der Mini Treiber die Werte <strong>WIA_DPS_PAGE_WIDTH</strong> und <strong>WIA_DPS_PAGE_HEIGHT</strong> in Tausendstel Zoll an die Dimensionen der Seite anpassen.</span><span class="sxs-lookup"><span data-stu-id="dc195-413">If an application sets <strong>WIA_DPS_PAGE_SIZE</strong> to any value other than WIA_PAGE_CUSTOM, the minidriver should adjust the values of <strong>WIA_DPS_PAGE_WIDTH</strong> and <strong>WIA_DPS_PAGE_HEIGHT</strong> to the page's dimensions in thousandths of an inch.</span></span> <span data-ttu-id="dc195-414">Außerdem sollten die Werte <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> und <strong>WIA_IPS_YEXTENT</strong> auf die Dimensionen der Seite in Pixel angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="dc195-414">It should also adjust the values of <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> and <strong>WIA_IPS_YEXTENT</strong> to the page's dimensions in pixels.</span></span></p>
<p><span data-ttu-id="dc195-415">Wenn eine Block Einstellung (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> oder <strong>WIA_IPS_YEXTENT</strong>) in einen Wert geändert wird, der nicht mit der aktuellen Einstellung der Seitengröße identisch ist, sollte der Mini Treiber den Wert der Eigenschaft <strong>WIA_DPS_PAGE_SIZE</strong> in WIA_PAGE_CUSTOM ändern.</span><span class="sxs-lookup"><span data-stu-id="dc195-415">If an extent setting (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> or <strong>WIA_IPS_YEXTENT</strong>) is changed to a value that does not match the current page-size setting, the minidriver should change the value of the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="dc195-416">Der Mini Treiber sollte auch <strong>WIA_DPS_PAGE_WIDTH</strong> oder <strong>WIA_DPS_PAGE_HEIGHT</strong> entsprechend der neuen Block Einstellung ändern.</span><span class="sxs-lookup"><span data-stu-id="dc195-416">The minidriver should also modify <strong>WIA_DPS_PAGE_WIDTH</strong> or <strong>WIA_DPS_PAGE_HEIGHT</strong> in accordance with the new extent setting.</span></span></p>
<p><span data-ttu-id="dc195-417">Wenn <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> auf lanscape festgelegt ist, werden die Block Einstellungen gekippt &quot; . &quot; Wenn eine Anwendung z. b. <strong>WIA_DPS_PAGE_SIZE</strong> auf WIA_PAGE_A4 festlegt, sollte der Mini Treiber <strong>WIA_DPS_PAGE_WIDTH</strong> auf 11692 und <strong>WIA_DPS_PAGE_HEIGHT</strong> auf 8267 festlegen.</span><span class="sxs-lookup"><span data-stu-id="dc195-417">If <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> is set to LANSCAPE, the extent settings will be &quot;flipped.&quot; For example, if an application sets <strong>WIA_DPS_PAGE_SIZE</strong> to WIA_PAGE_A4, the minidriver should set <strong>WIA_DPS_PAGE_WIDTH</strong> to 11692 and <strong>WIA_DPS_PAGE_HEIGHT</strong> to 8267.</span></span> <span data-ttu-id="dc195-418">(Der Mini Treiber sollte auch <strong>WIA_IPS_XEXTENT</strong> festlegen und entsprechend <strong>WIA_IPS_YEXTENT</strong> .) Beachten Sie Folgendes: Wenn <strong>WIA_DPS_PAGE_SIZE</strong> auf WIA_PAGE_CUSTOM festgelegt ist, wird die Ausrichtung nicht verwendet, um die Bereichs Dimensionen der zu scannenden Seite zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="dc195-418">(The minidriver should also set <strong>WIA_IPS_XEXTENT</strong> and <strong>WIA_IPS_YEXTENT</strong> accordingly.) Note that if <strong>WIA_DPS_PAGE_SIZE</strong> is set to WIA_PAGE_CUSTOM, the orientation setting is not used to determine the extent dimensions of the page to be scanned.</span></span></p>
<p><span data-ttu-id="dc195-419">Der Mini Treiber ist dafür verantwortlich, sicherzustellen, dass die <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> -Eigenschaft mit dem aktuellen Auswahlbereich übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="dc195-419">The minidriver is responsible for ensuring that the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property is in agreement with the current selection area.</span></span> <span data-ttu-id="dc195-420">Wenn eine Anwendung den Wert von <strong>WIA_IPS_ORIENTATION</strong> in einen Wert ändert, der für die aktuell ausgewählte Seitengröße ungültig ist, sollte der Mini Treiber den Wert <strong>WIA_DPS_PAGE_SIZE</strong> in eine Seitengröße ändern, die vom neuen Wert für die Ausrichtung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="dc195-420">If an application changes the value of <strong>WIA_IPS_ORIENTATION</strong> to one that is invalid for the currently selected page size, the minidriver should change the value of <strong>WIA_DPS_PAGE_SIZE</strong> to a page size that is supported by the new orientation value.</span></span></p>
<p><span data-ttu-id="dc195-421">Wenn eine Anwendung die <strong>WIA_DPS_PAGE_SIZE</strong> -Eigenschaft auf WIA_PAGE_CUSTOM festlegt, ist der aktuelle Auswahlbereich nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="dc195-421">If an application sets the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_CUSTOM, the current selection area is not affected.</span></span> <span data-ttu-id="dc195-422">Der WIA-Mini Treiber sollte das aktuelle Bild Layout abrufen, beginnend mit den aktuellen Einstellungen der Eigenschaften " <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> " und " <strong>WIA_IPS_YPOS</strong> ".</span><span class="sxs-lookup"><span data-stu-id="dc195-422">The WIA minidriver should obtain the current image layout, starting from the current settings of the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> and <strong>WIA_IPS_YPOS</strong> properties.</span></span> <span data-ttu-id="dc195-423">Wenn die Einstellung für die Seitengröße zu einem Auswahlbereich führt, der sich außerhalb des Scanners befindet, muss der Mini Treiber automatisch die Werte der Eigenschaften <strong>WIA_IPS_XPOS</strong> und <strong>WIA_IPS_YPOS</strong> an gültige Einstellungen anpassen.</span><span class="sxs-lookup"><span data-stu-id="dc195-423">If the page-size setting results in a selection area that is outside the scanner's bed, the minidriver must automatically adjust the values of the <strong>WIA_IPS_XPOS</strong> and <strong>WIA_IPS_YPOS</strong> properties to valid settings.</span></span> <span data-ttu-id="dc195-424">Wenn die Eigenschaften <strong>WIA_DPS_PAGE_SIZE</strong> und <strong>WIA_IPS_ORIENTATION</strong> gleichzeitig festgelegt sind und Sie in Kombination mit der Anwendung ungültig sind, sollte der Mini Treiber die Einstellungen der Anwendung nicht durch Zurückgeben eines Fehlers in <a href="https://msdn.microsoft.com/library/ms794145.aspx">iwiaminidrv::d rvvalidateitemproperties</a>ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc195-424">If the <strong>WIA_DPS_PAGE_SIZE</strong> and <strong>WIA_IPS_ORIENTATION</strong> properties are set at the same time, and they are invalid when applied in combination, the minidriver should fail the application's settings by returning an error in the <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv::drvValidateItemProperties</a>.</span></span> <span data-ttu-id="dc195-425">.</span><span class="sxs-lookup"><span data-stu-id="dc195-425">.</span></span></p>
<p><span data-ttu-id="dc195-426">In den folgenden vier Beispielen werden verschiedene <strong>WIA_DPS_PAGE_SIZE</strong> Szenarios gezeigt.</span><span class="sxs-lookup"><span data-stu-id="dc195-426">The following four examples show different <strong>WIA_DPS_PAGE_SIZE</strong> scenarios.</span></span></p>
<ol>
<li><span data-ttu-id="dc195-427">Der Treiber meldet die Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="dc195-427">The driver reports the settings.</span></span></li>
<li><span data-ttu-id="dc195-428">In einer Anwendung wird die <strong>WIA_DPS_PAGE_SIZE</strong> -Eigenschaft auf WIA_PAGE_LETTER festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dc195-428">An application sets the <strong>WIA_DPS_PAGE_SIZE</strong> property to WIA_PAGE_LETTER.</span></span></li>
<li><span data-ttu-id="dc195-429">Eine Anwendung legt die <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> -Eigenschaft auf lanscape fest.</span><span class="sxs-lookup"><span data-stu-id="dc195-429">An application sets the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> property to LANSCAPE.</span></span></li>
<li><span data-ttu-id="dc195-430">Die <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> -Eigenschaft wird von einer Anwendung in einen kleineren Wert geändert.</span><span class="sxs-lookup"><span data-stu-id="dc195-430">An application changes the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> property to a smaller value.</span></span></li>
</ol>
<p><span data-ttu-id="dc195-431"><strong>Beispiel 1: der Mini Treiber meldet die Einstellungen.</strong></span><span class="sxs-lookup"><span data-stu-id="dc195-431"><strong>Example 1: The minidriver reports the settings</strong></span></span></p>
<p><span data-ttu-id="dc195-432">Im folgenden Beispiel legt der Mini Treiber einen benutzerdefinierten Auswahlbereich fest, bevor eine Anwendung WIA-Eigenschaften festlegt.</span><span class="sxs-lookup"><span data-stu-id="dc195-432">In the following example, the minidriver sets a custom selection area before an application sets any WIA properties.</span></span> <span data-ttu-id="dc195-433">In diesem Fall stellt der Auswahlbereich das gesamte Flatbed dar.</span><span class="sxs-lookup"><span data-stu-id="dc195-433">In this case, the selection area represents the entire flatbed.</span></span></p>
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
<p><span data-ttu-id="dc195-434"><strong>Beispiel 2: eine Anwendung legt die</strong> <strong>WIA_DPS_PAGE_SIZE</strong>-<strong>Eigenschaft auf fest WIA_PAGE_LETTER</strong>  </span><span class="sxs-lookup"><span data-stu-id="dc195-434"><strong>Example 2: An application sets the</strong> <strong>WIA_DPS_PAGE_SIZE</strong>  <strong>property to WIA_PAGE_LETTER</strong></span></span></p>
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
<p><span data-ttu-id="dc195-435"><strong>Beispiel 3: eine Anwendung legt die</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a>-<strong>Eigenschaft auf lanscape</strong> fest.  </span><span class="sxs-lookup"><span data-stu-id="dc195-435"><strong>Example 3: An application sets the</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a>  <strong>property to LANSCAPE</strong></span></span></p>
<p><span data-ttu-id="dc195-436">Das physische Bett muss in der Lage sein, eine Seite abzurufen, die sich ursprünglich in Querformat orientiert.</span><span class="sxs-lookup"><span data-stu-id="dc195-436">The physical bed must be able to acquire a page that was originally in landscape orientation.</span></span></p>
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
<p><span data-ttu-id="dc195-437"><strong>Beispiel 4: eine Anwendung ändert die</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>-<strong>Eigenschaft in einen kleineren Wert</strong>  </span><span class="sxs-lookup"><span data-stu-id="dc195-437"><strong>Example 4: An application changes the</strong> <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>  <strong>property to a smaller value</strong></span></span></p>
<p><span data-ttu-id="dc195-438">Im folgenden Beispiel ändert eine Anwendung die <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> -Eigenschaft in 1000.</span><span class="sxs-lookup"><span data-stu-id="dc195-438">In the following example, an application changes the <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> property to 1000.</span></span> <span data-ttu-id="dc195-439">Der Mini Treiber sollte davon ausgehen, dass der in <strong>WIA_IPS_XEXTENT</strong> enthaltene neue Wert für die Eigenschaft <strong>WIA_DPS_PAGE_SIZE</strong> nicht mehr gültig ist und daher <strong>WIA_DPS_PAGE_SIZE</strong> in WIA_PAGE_CUSTOM ändern sollte.</span><span class="sxs-lookup"><span data-stu-id="dc195-439">The minidriver should assume that the new value contained in <strong>WIA_IPS_XEXTENT</strong> is no longer valid for the <strong>WIA_DPS_PAGE_SIZE</strong> property and should thus change <strong>WIA_DPS_PAGE_SIZE</strong> to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="dc195-440">Der Mini Treiber muss auch <strong>WIA_DPS_PAGE_WIDTH</strong>anpassen.</span><span class="sxs-lookup"><span data-stu-id="dc195-440">The minidriver must also adjust <strong>WIA_DPS_PAGE_WIDTH</strong>.</span></span></p>
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
<td style="text-align: left;"><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <span data-ttu-id="dc195-441"><dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-441"><dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-442">Diese Eigenschaft wird von Windows Vista nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-442">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="dc195-443">Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-443">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-444">Enthält die Breite der aktuell ausgewählten Seite in Tausendstel Zoll.</span><span class="sxs-lookup"><span data-stu-id="dc195-444">Contains the width of the current page selected, in thousandths of an inch.</span></span> <span data-ttu-id="dc195-445">Eine Anwendung liest diese Eigenschaft, um die physischen Dimensionen der zu scannenden Seite zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="dc195-445">An application reads this property to determine the physical dimensions of the page being scanned.</span></span> <span data-ttu-id="dc195-446">Wenn sich die Block Einstellungen von den bekannten Seitengrößen unterscheiden, meldet diese Eigenschaft die Breite der Seite, deren <strong>WIA_DPS_PAGE_SIZE</strong> -Eigenschaft auf WIA_PAGE_CUSTOM festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dc195-446">If the extent settings are different from known page sizes, this property reports the width of the page whose <strong>WIA_DPS_PAGE_SIZE</strong> property is set to WIA_PAGE_CUSTOM.</span></span> <span data-ttu-id="dc195-447"><strong>WIA_DPS_PAGE_WIDTH</strong> muss mit dem Wert von <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>synchronisiert sein, der die Breite der zu scannenden Seite in Pixel meldet.</span><span class="sxs-lookup"><span data-stu-id="dc195-447"><strong>WIA_DPS_PAGE_WIDTH</strong> must be in sync with the value of <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, which reports the width, in pixels, of the page to be scanned.</span></span> <span data-ttu-id="dc195-448">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-448">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="dc195-449">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-449">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <span data-ttu-id="dc195-450"><dt><strong>WIA_DPS_PAGES</strong></dt> <dt>scannerentvicepages</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-450"><dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-451">Diese Eigenschaft wird von Windows Vista nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-451">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="dc195-452">Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-452">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-453">Enthält die aktuelle Anzahl der Seiten, die von einem automatischen Dokument-feedwert abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dc195-453">Contains the current number of pages to be acquired from an automatic document feeder.</span></span> <span data-ttu-id="dc195-454">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-454">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="dc195-455">Typ: <strong>VT_I4</strong>; Zugriff: Lesen/Schreiben; Gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (null bis zur maximalen Anzahl von Seiten, die der Dokument-feedwert aufnehmen kann)</span><span class="sxs-lookup"><span data-stu-id="dc195-455">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (zero through the maximum number of pages that the document feeder can hold)</span></span></p>
<p><span data-ttu-id="dc195-456">Eine Anwendung liest diese Eigenschaft, um die Seiten Kapazität des Dokument Anlegers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="dc195-456">An application reads this property to determine the document feeder's page capacity.</span></span> <span data-ttu-id="dc195-457">Diese Eigenschaft wird von der Anwendung auch auf die Anzahl der Seiten festgelegt, die gescannt werden.</span><span class="sxs-lookup"><span data-stu-id="dc195-457">The application also sets this property to the number of pages it is going to scan.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-458">, Wenn der Duplex Modus aktiviert ist (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> ist auf "Fee" festgelegt | Duplex), <strong>WIA_DPS_PAGES</strong> gleichzeitig gleich der Anzahl der zu scanenden Seiten ist.</span><span class="sxs-lookup"><span data-stu-id="dc195-458">If duplex mode is enabled (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> is set to FEEDER | DUPLEX ), <strong>WIA_DPS_PAGES</strong> is still equal to the number of pages to scan.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-459">Ein Papierblatt enthält automatisch zwei Seiten, wenn Duplex aktiviert ist, auch wenn die Rückseite der Seite leer ist.</span><span class="sxs-lookup"><span data-stu-id="dc195-459">One sheet of paper will automatically contain two pages if DUPLEX is enabled, even if the back side of the page is blank.</span></span></p>
<p><span data-ttu-id="dc195-460">Das Festlegen von <strong>WIA_DPS_PAGES</strong> auf 1 bewirkt, dass ein Scanner eine der Seiten der Seite verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="dc195-460">Setting <strong>WIA_DPS_PAGES</strong> to 1 causes a scanner to process one of the sides of the page.</span></span> <span data-ttu-id="dc195-461">Wenn ein Scanner nicht nur eine Seite einer Seite im Duplex Modus überprüfen kann, sollte der <strong>WIA_DPS_PAGES</strong> gültigen Wert für das Inc-Mitglied der WIA_PROPERTY_INFO Struktur in 2 geändert werden.</span><span class="sxs-lookup"><span data-stu-id="dc195-461">It is recommended that if a scanner is unable to scan only one side of a page while in duplex mode, the <strong>WIA_DPS_PAGES</strong> valid value for the Inc member of the WIA_PROPERTY_INFO structure should be changed to 2.</span></span> <span data-ttu-id="dc195-462">Dieser Wert signalisiert der Anwendung, dass Seiten in Vielfachen von zwei Anforderungen angefordert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="dc195-462">This value signals the application that it must request pages in multiples of two.</span></span> <span data-ttu-id="dc195-463">Der Wert 0 (null) bedeutet, dass <em>alle</em> Seiten, die derzeit in den Dokument-feedergeladen werden, gescannt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dc195-463">A value of zero means that <em>all</em> pages that are currently loaded into the document feeder are to be scanned.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <span data-ttu-id="dc195-464"><dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>scannerdeviceplatkocolor</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-464"><dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="dc195-465">Gibt die Farbe der Platen auf der Rückseite des zu scannenden Blatts an.</span><span class="sxs-lookup"><span data-stu-id="dc195-465">Specifies the color of the platen in back of the sheet to be scanned.</span></span> <span data-ttu-id="dc195-466">Diese Eigenschaft ist für Scanner mit Platen optional.</span><span class="sxs-lookup"><span data-stu-id="dc195-466">This property is optional for scanners that have a platen.</span></span> <span data-ttu-id="dc195-467">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-467">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="dc195-468">Typ: <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-468">Type: <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="dc195-469">Das Format der Farbinformationen ist <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">rgbquad</a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-469">The format of the color information is <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <span data-ttu-id="dc195-470"><dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>scannerdevicepreview</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-470"><dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-471">Diese Eigenschaft wird von Windows Vista nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-471">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="dc195-472">Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-472">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-473">Gibt den Vorschaumodus für ein Gerät an.</span><span class="sxs-lookup"><span data-stu-id="dc195-473">Indicates the preview mode for a device.</span></span> <span data-ttu-id="dc195-474">Eine Anwendung legt diese Eigenschaft fest, um das Gerät in einen Vorschaumodus zu versetzen.</span><span class="sxs-lookup"><span data-stu-id="dc195-474">An application sets this property to place the device into a preview mode.</span></span></p>
<p><span data-ttu-id="dc195-475">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="dc195-475">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="dc195-476">Die folgende Tabelle enthält die beiden Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="dc195-476">The following table has the two constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dc195-477">Wert</span><span class="sxs-lookup"><span data-stu-id="dc195-477">Value</span></span></th>
<th><span data-ttu-id="dc195-478">Definition</span><span class="sxs-lookup"><span data-stu-id="dc195-478">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc195-479">WIA_FINAL_SCAN</span><span class="sxs-lookup"><span data-stu-id="dc195-479">WIA_FINAL_SCAN</span></span></td>
<td><span data-ttu-id="dc195-480">Die Anwendung führt eine abschließende Überprüfung aus.</span><span class="sxs-lookup"><span data-stu-id="dc195-480">The application will perform a final scan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-481">WIA_PREVIEW_SCAN</span><span class="sxs-lookup"><span data-stu-id="dc195-481">WIA_PREVIEW_SCAN</span></span></td>
<td><span data-ttu-id="dc195-482">Die Anwendung führt eine Vorschau Überprüfung durch.</span><span class="sxs-lookup"><span data-stu-id="dc195-482">The application will perform a preview scan.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <span data-ttu-id="dc195-483"><dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>scannerdebug Pages</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-483"><dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="dc195-484">Enthält einen Wert, der angibt, ob der Scanner Seiten in einem Scanner-Puffer zwischenspeichert, bevor Sie an die Anwendung gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="dc195-484">Contains a value that indicates whether the scanner will cache pages in a scanner buffer before sending them to the application.</span></span></p>
<p><span data-ttu-id="dc195-485">Der Wert 0 deaktiviert die Überprüfung voraus, und es werden keine Seiten vor der Überprüfung durchsucht.</span><span class="sxs-lookup"><span data-stu-id="dc195-485">A value of zero disables scan ahead and no pages will be scanned ahead.</span></span> <span data-ttu-id="dc195-486">Wenn Sie normale Datenübertragungen für das gepufferte Scan-Ahead-Element durchgehen, werden die gepufferten Seiten abgerufen.</span><span class="sxs-lookup"><span data-stu-id="dc195-486">Doing normal data transfers on the buffered scan-ahead item retrieves the buffered pages.</span></span> <span data-ttu-id="dc195-487">WIA-Eigenschaften können während eines Scanvorgangs nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="dc195-487">WIA properties cannot be changed during a scan-ahead operation.</span></span> <span data-ttu-id="dc195-488">Diese Eigenschaft ist optional.</span><span class="sxs-lookup"><span data-stu-id="dc195-488">This property is optional.</span></span></p>
<p><span data-ttu-id="dc195-489">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 0 (null) bis zur maximalen Anzahl von Seiten, die der Dokument-feedvorgang enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="dc195-489">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> of zero to the maximum number of pages that the document feeder can hold.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <span data-ttu-id="dc195-490"><dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>scannerabvicescanavailableitem</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-490"><dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-491">Diese Eigenschaft wird nur von Windows 7 und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-491">This property is supported only by Windows 7 and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-492">Gibt die Eingabe Quelle ("Flatbed", "Automatic Document" oder "fil-Scan Adapter") an, die überprüft werden soll, oder den Speicherort, von dem Daten übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="dc195-492">Indicates the input source (flatbed, automatic document feeder, or fil-scanning adapter) to scan from, or the storage location to transfer data from.</span></span></p>
<p><span data-ttu-id="dc195-493">Ein Scan-Ereignis benachrichtigt die Anwendung, dass der Benutzer einen Scan initiiert hat, aber das Ereignis stellt nicht den Namen des WIA-Elements bereit, das die Eingabe Quelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="dc195-493">A scan event notifies the application that the user has initiated a scan, but the event does not supply the name of the WIA item that represents the input source.</span></span> <span data-ttu-id="dc195-494">Der-Ereignishandler der Anwendung kann die WIA_DPS_SCAN_AVAILABLE_ITEM-Eigenschaft des Stamm Elements Abfragen, um den Namen des Eingabe Quell Elements zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="dc195-494">The application's event handler can query the root item's WIA_DPS_SCAN_AVAILABLE_ITEM property to get the name of the input source item.</span></span></p>
<p><span data-ttu-id="dc195-495">Typ: <strong>VT_I4</strong>, Zugriff: Lese-/Schreibzugriff, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> 0 (null) bis zur maximalen Anzahl von Seiten, die der Dokument-feedvorgang enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="dc195-495">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> of zero to the maximum number of pages that the document feeder can hold.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <span data-ttu-id="dc195-496"><dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>scannerdecoeserviceid</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-496"><dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-497">Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-497">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-498">Enthält die Dienst-ID eines Webdienst-Scanner-Geräts.</span><span class="sxs-lookup"><span data-stu-id="dc195-498">Contains the Service ID of a Web Services scanner device.</span></span> <span data-ttu-id="dc195-499">Der WIA 2,0-Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-499">The WIA 2.0 mini-driver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="dc195-500">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-500">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <span data-ttu-id="dc195-501"><dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>scannerdevicesheetfeederregistration</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-501"><dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-502">Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-502">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="dc195-503">Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-503">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-504">Enthält die Registrierung bzw. die Ausrichtung und Kantenerkennung für Dokumente, die im Flatbed abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dc195-504">Contains the registration, or alignment and edge detection, for documents that are placed on the flatbed.</span></span> <span data-ttu-id="dc195-505">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-505">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="dc195-506">Diese Eigenschaft gibt an, wie das Blatt horizontal auf der Scan Kopfzeile eines Hand Buch-oder Sheet-Scans positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="dc195-506">This property indicates how the sheet is horizontally positioned on the scanning head of a handheld or sheet-fed scanner.</span></span> <span data-ttu-id="dc195-507">Die-Eigenschaft wird verwendet, um vorherzusagen, wo ein Dokument über die Scan Kopfzeile platziert wird.</span><span class="sxs-lookup"><span data-stu-id="dc195-507">The property is used to predict where across the scan head a document is placed.</span></span></p>
<p><span data-ttu-id="dc195-508">Für Scanner, die mehr als einen scanhead unterstützen, ist diese Eigenschaft relativ zum obersten scanhead.</span><span class="sxs-lookup"><span data-stu-id="dc195-508">For scanners that support more than one scan head, this property is relative to the topmost scan head.</span></span> <span data-ttu-id="dc195-509">Diese Eigenschaft ist für Blatt-, Scroll-und Hand Buchscanner obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="dc195-509">This property is mandatory for sheet-fed, scroll-fed, and handheld scanners.</span></span></p>
<p><span data-ttu-id="dc195-510">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-510">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="dc195-511">Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="dc195-511">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dc195-512">Konstante</span><span class="sxs-lookup"><span data-stu-id="dc195-512">Constant</span></span></th>
<th><span data-ttu-id="dc195-513">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc195-513">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc195-514">LEFT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="dc195-514">LEFT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="dc195-515">Das Blatt wird in Bezug auf die scannerkopfzeile links positioniert.</span><span class="sxs-lookup"><span data-stu-id="dc195-515">The sheet is positioned to the left with respect to the scanning head.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-516">Ego</span><span class="sxs-lookup"><span data-stu-id="dc195-516">CENTERED</span></span></td>
<td><span data-ttu-id="dc195-517">Das Blatt ist auf die scannerkopfzeile zentriert.</span><span class="sxs-lookup"><span data-stu-id="dc195-517">The sheet is centered on the scanning head.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-518">RIGHT_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="dc195-518">RIGHT_JUSTIFIED</span></span></td>
<td><span data-ttu-id="dc195-519">Das Blatt wird in Bezug auf den Scan Kopf rechts positioniert.</span><span class="sxs-lookup"><span data-stu-id="dc195-519">The sheet is positioned to the right with respect to the scanning head.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <span data-ttu-id="dc195-520"><dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>scannerdebug-Steuer</dt> Element </span><span class="sxs-lookup"><span data-stu-id="dc195-520"><dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-521">Diese Eigenschaft wird von Windows Vista nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-521">This property is not supported by Windows Vista.</span></span> <span data-ttu-id="dc195-522">Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-522">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-523">Gibt an, ob ein Element ein Vorschau Steuerelement benötigt, das für den Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dc195-523">Indicates whether an item needs a preview control displayed to the user.</span></span> <span data-ttu-id="dc195-524">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-524">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="dc195-525">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-525">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="dc195-526">Die folgende Tabelle enthält die beiden Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="dc195-526">The following table has the two constants that are valid with this property.</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dc195-527">Konstante</span><span class="sxs-lookup"><span data-stu-id="dc195-527">Constant</span></span></th>
<th><span data-ttu-id="dc195-528">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc195-528">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc195-529">WIA_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="dc195-529">WIA_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="dc195-530">Zeigen Sie dem Benutzer ein Vorschau Steuerelement an, da auf diesem Gerät eine Vorschauversion durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="dc195-530">Show a preview control to the user, because this device can perform a preview.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-531">WIA_DONT_SHOW_PREVIEW_CONTROL</span><span class="sxs-lookup"><span data-stu-id="dc195-531">WIA_DONT_SHOW_PREVIEW_CONTROL</span></span></td>
<td><span data-ttu-id="dc195-532">Zeigen Sie dem Benutzer kein Vorschau Steuerelement an, da auf diesem Gerät keine Vorschauversion durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="dc195-532">Do not show a preview control to the user, because this device cannot perform a preview.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <span data-ttu-id="dc195-533"><dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>scannerenviceusername</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-533"><dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-534">Diese Eigenschaft wird nur von Windows Vista und höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-534">This property is supported only by Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-535">Wird vom WIA-Dienst verwendet, um den Mini Treiber über den Benutzerkonto Namen (z. b. den ggf. den Netzwerk Domänen Namen) der Sitzung zu informieren, in der die aktuelle WIA-Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dc195-535">Used by the WIA service to inform the mini-driver about the user account name (including the network domain name when applicable) of the session in which the current WIA application is running.</span></span></p>
<p><span data-ttu-id="dc195-536">Dabei handelt es sich um eine Stamm Element Eigenschaft, die vom WIA-Dienst verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="dc195-536">This is a root item property, managed by the WIA service.</span></span></p>
<p><span data-ttu-id="dc195-537">Typ: <strong>VT_BSTR</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-537">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <span data-ttu-id="dc195-538"><dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>scannerdeviceverticalbedregistration</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-538"><dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-539">Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-539">This property is not supported with Windows Vista and later.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-540">Enthält die Registrierung bzw. die vertikale Ausrichtung und Kantenerkennung für Dokumente, die im Flatbed abgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dc195-540">Contains the registration, or vertical alignment and edge detection, for documents placed on the flatbed.</span></span> <span data-ttu-id="dc195-541">Der Mini Treiber erstellt und verwaltet diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-541">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="dc195-542">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-542">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="dc195-543">Die folgende Tabelle enthält die drei Konstanten, die mit dieser Eigenschaft gültig sind.</span><span class="sxs-lookup"><span data-stu-id="dc195-543">The following table has the three constants that are valid with this property..</span></span> </p>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="dc195-544">Konstante</span><span class="sxs-lookup"><span data-stu-id="dc195-544">Constant</span></span></th>
<th><span data-ttu-id="dc195-545">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dc195-545">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dc195-546">TOP_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="dc195-546">TOP_JUSTIFIED</span></span></td>
<td><span data-ttu-id="dc195-547">Das Dokument ist oberstes Recht.</span><span class="sxs-lookup"><span data-stu-id="dc195-547">The paper is top justified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dc195-548">Ego</span><span class="sxs-lookup"><span data-stu-id="dc195-548">CENTERED</span></span></td>
<td><span data-ttu-id="dc195-549">Das Dokument wird zentriert.</span><span class="sxs-lookup"><span data-stu-id="dc195-549">The paper is centered.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dc195-550">BOTTOM_JUSTIFIED</span><span class="sxs-lookup"><span data-stu-id="dc195-550">BOTTOM_JUSTIFIED</span></span></td>
<td><span data-ttu-id="dc195-551">Das Papier ist unten bündig ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="dc195-551">The paper is bottom justified.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="dc195-552"><strong>Siehe auch</strong>.</span><span class="sxs-lookup"><span data-stu-id="dc195-552"><strong>See Also</strong>.</span></span></p>
<p><span data-ttu-id="dc195-553"><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="dc195-553"><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <span data-ttu-id="dc195-554"><dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>scannerdecoeverticalbedsize</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-554"><dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-555">Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-555">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="dc195-556">Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-556">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-557">Gibt die maximale Höhe in Tausendstel Zoll an, die auf der vertikalen Achse (Y-Achse) von der Plate eines Flatbed-Scanners bei der aktuellen Auflösung gescannt wird.</span><span class="sxs-lookup"><span data-stu-id="dc195-557">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis from the platen of a flatbed scanner at the current resolution.</span></span> <span data-ttu-id="dc195-558">Diese Eigenschaft gilt auch für automatische Dokument Feeden, die Blätter zum Scannen in die Plate eines flachen Scanners verschieben.</span><span class="sxs-lookup"><span data-stu-id="dc195-558">This property also applies to automatic document feeders, that move sheets to the platen of a flatbed scanner for scanning.</span></span> <span data-ttu-id="dc195-559">Diese Eigenschaft ist für Scanner mit einem Platen obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="dc195-559">This property is mandatory for scanners that have a platen.</span></span> <span data-ttu-id="dc195-560">Andere Scannertypen implementieren stattdessen die <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="dc195-560">Other scanner types will instead implement the <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> property.</span></span></p>
<p><span data-ttu-id="dc195-561">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-561">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <span data-ttu-id="dc195-562"><dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>scannerdecoeverticalsheetfeedsize</dt> </span><span class="sxs-lookup"><span data-stu-id="dc195-562"><dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dc195-563">Diese Eigenschaft wird von Windows Vista und höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc195-563">This property is not supported with Windows Vista and later.</span></span> <span data-ttu-id="dc195-564">Verwenden Sie <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="dc195-564">Use <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="dc195-565">Gibt die maximale Höhe (in Tausendstel Zoll) an, die in der vertikalen Achse (Y-Achse) von einem Hand Held-oder Blatt Feed-Scanner bei der aktuellen Auflösung gescannt wird.</span><span class="sxs-lookup"><span data-stu-id="dc195-565">Specifies the maximum height, in thousandths of an inch, that is scanned in the vertical (Y) axis from a handheld or sheet feed scanner at the current resolution.</span></span> <span data-ttu-id="dc195-566">Diese Eigenschaft gilt auch für automatische Dokument Feeden, die durchsucht werden, ohne Blätter in die Plate eines flachen Scanners zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="dc195-566">This property also applies to automatic document feeders that scan without moving sheets to the platen of a flatbed scanner.</span></span> <span data-ttu-id="dc195-567">Diese Eigenschaft ist für Blatt Scanner obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="dc195-567">This property is mandatory for sheet-fed scanners.</span></span> <span data-ttu-id="dc195-568">Scrollgesteuerte und handgehaltene Scanner sollten diese Eigenschaft nicht implementieren.</span><span class="sxs-lookup"><span data-stu-id="dc195-568">Scroll-fed and hand-held scanners should not implement this property.</span></span></p>
<p><span data-ttu-id="dc195-569">Typ: <strong>VT_I4</strong>, Zugriff: schreibgeschützt, gültige Werte: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="dc195-569">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="dc195-570">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dc195-570">Requirements</span></span>



| <span data-ttu-id="dc195-571">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc195-571">Requirement</span></span> | <span data-ttu-id="dc195-572">Wert</span><span class="sxs-lookup"><span data-stu-id="dc195-572">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dc195-573">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc195-573">Minimum supported client</span></span><br/> | <span data-ttu-id="dc195-574">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc195-574">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="dc195-575">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc195-575">Minimum supported server</span></span><br/> | <span data-ttu-id="dc195-576">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc195-576">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dc195-577">Header</span><span class="sxs-lookup"><span data-stu-id="dc195-577">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc195-578"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc195-578"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
