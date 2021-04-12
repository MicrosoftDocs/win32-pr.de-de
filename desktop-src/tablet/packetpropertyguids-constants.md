---
description: Definiert Werte, die die Paket Eigenschaften angeben.
ms.assetid: 3e8495f6-0860-4ea8-a258-784eaade85c7
title: Packetpropertyguids-Konstanten (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadb664cb3783932dc2e7063d7cfab07133ad9fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218359"
---
# <a name="packetpropertyguids-constants"></a><span data-ttu-id="e13e3-103">Packetpropertyguids-Konstanten</span><span class="sxs-lookup"><span data-stu-id="e13e3-103">PacketPropertyGuids Constants</span></span>

<span data-ttu-id="e13e3-104">Definiert Werte, die die Paket Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="e13e3-104">Defines values that specify the packet properties.</span></span> <span data-ttu-id="e13e3-105">Das Tablet pcapi verwendet Global Unique Identifier (GUIDs), um Paket Eigenschaften zu identifizieren, die in com Konstante Zeichen folgen sind.</span><span class="sxs-lookup"><span data-stu-id="e13e3-105">The Tablet PCAPI uses globally unique identifiers (GUIDs) to identify packet properties, which in COM are constant strings.</span></span>

<span data-ttu-id="e13e3-106">In C++ können Sie auf diese Konstanten in der Header Datei "msink AUT. h" zugreifen, die sich im <systemdrive> \\ Verzeichnis "Programme \\ Microsoft SDKs \\ Windows \\ v 6.0 include" befindet, \\ Wenn Sie das SDK am Standard Speicherort installiert haben.</span><span class="sxs-lookup"><span data-stu-id="e13e3-106">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Include directory if you installed the SDK in the default location.</span></span> <span data-ttu-id="e13e3-107">In C++ sind diese Konstanten WCHARs, nicht bstrins.</span><span class="sxs-lookup"><span data-stu-id="e13e3-107">In C++, these constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="e13e3-108">Konvertieren Sie diese vor der Verwendung in bstraus.</span><span class="sxs-lookup"><span data-stu-id="e13e3-108">Convert them into BSTRs before use.</span></span> <span data-ttu-id="e13e3-109">Weitere Informationen zum BSTR-Datentyp finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="e13e3-109">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

<span data-ttu-id="e13e3-110">In der folgenden Tabelle sind die verfügbaren Felder der Paket Eigenschaften Globally Unique Identifier (GUID) aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e13e3-110">The following table lists the available packet property globally unique identifier (GUID) fields.</span></span> <span data-ttu-id="e13e3-111">Verwenden Sie diese GUIDs, um anzugeben, welche Eigenschaften das Paket enthält, wenn Sie den Tablet-Kontext erstellen.</span><span class="sxs-lookup"><span data-stu-id="e13e3-111">Use these GUIDs to specify which properties the packet contains when you create the tablet context.</span></span> <span data-ttu-id="e13e3-112">Um den Bereich und die Auflösung einer Eigenschaft zu ermitteln, müssen Sie die [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e13e3-112">To determine the range and resolution of a property, call the [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) method.</span></span> <span data-ttu-id="e13e3-113">Die Konstanten in der Tabelle unten, beginnend mit "Str \_ ", sind Zeichen folgen Darstellungen der entsprechenden binären Konstanten, die in derselben Tabellenzelle angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e13e3-113">The constants in the table below beginning with "STR\_" are string representations of the corresponding binary constants shown in the same table cell.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="e13e3-114">Konstante</span><span class="sxs-lookup"><span data-stu-id="e13e3-114">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="e13e3-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e13e3-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_X_or_GUID_PACKETPROPERTY_GUID_X"></span><span id="str_guid_x_or_guid_packetproperty_guid_x"></span><span id="STR_GUID_X_OR_GUID_PACKETPROPERTY_GUID_X"></span><dl> <span data-ttu-id="e13e3-116"><dt><strong>STR_GUID_X oder GUID_PACKETPROPERTY_GUID_X</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-116"><dt><strong>STR_GUID_X or GUID_PACKETPROPERTY_GUID_X</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-117">Die x-Koordinate im tablettkoordinatenbereich.</span><span class="sxs-lookup"><span data-stu-id="e13e3-117">The x-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="e13e3-118">Jedes Paket enthält diese Eigenschaft standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="e13e3-118">Each packet contains this property by default.</span></span> <span data-ttu-id="e13e3-119">Der Ursprung (0,0) des Tablets ist die linke obere Ecke.</span><span class="sxs-lookup"><span data-stu-id="e13e3-119">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <span data-ttu-id="e13e3-120"><dt><strong>STR_GUID_Y oder GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-120"><dt><strong>STR_GUID_Y or GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-121">Die y-Koordinate im tablettkoordinatenbereich.</span><span class="sxs-lookup"><span data-stu-id="e13e3-121">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="e13e3-122">Jedes Paket enthält diese Eigenschaft standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="e13e3-122">Each packet contains this property by default.</span></span> <span data-ttu-id="e13e3-123">Der Ursprung (0,0) des Tablets ist die linke obere Ecke.</span><span class="sxs-lookup"><span data-stu-id="e13e3-123">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <span data-ttu-id="e13e3-124"><dt><strong>STR_GUID_Y oder GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-124"><dt><strong>STR_GUID_Y or GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-125">Die y-Koordinate im tablettkoordinatenbereich.</span><span class="sxs-lookup"><span data-stu-id="e13e3-125">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="e13e3-126">Jedes Paket enthält diese Eigenschaft standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="e13e3-126">Each packet contains this property by default.</span></span> <span data-ttu-id="e13e3-127">Der Ursprung (0,0) des Tablets ist die linke obere Ecke.</span><span class="sxs-lookup"><span data-stu-id="e13e3-127">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Z_or_GUID_PACKETPROPERTY_GUID_Z"></span><span id="str_guid_z_or_guid_packetproperty_guid_z"></span><span id="STR_GUID_Z_OR_GUID_PACKETPROPERTY_GUID_Z"></span><dl> <span data-ttu-id="e13e3-128"><dt><strong>STR_GUID_Z oder GUID_PACKETPROPERTY_GUID_Z</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-128"><dt><strong>STR_GUID_Z or GUID_PACKETPROPERTY_GUID_Z</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-129">Die z-Koordinate oder den Abstand der Stift Spitze von der Tablet-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="e13e3-129">The z-coordinate or distance of the pen tip from the tablet surface.</span></span> <span data-ttu-id="e13e3-130">Der <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a> -Enumerationstyp bestimmt die Maßeinheit für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="e13e3-130">The <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a> enumeration type determines the unit of measurement for this property.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PAKETSTATUS_or_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><span id="str_guid_paketstatus_or_guid_packetproperty_guid_packet_status"></span><span id="STR_GUID_PAKETSTATUS_OR_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><dl> <span data-ttu-id="e13e3-131"><dt><strong>STR_GUID_PAKETSTATUS oder GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-131"><dt><strong>STR_GUID_PAKETSTATUS or GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-132">Enthält mindestens einen der folgenden Flagwerte:</span><span class="sxs-lookup"><span data-stu-id="e13e3-132">Contains one or more of the following flag values:</span></span><br/>
<ul>
<li><span data-ttu-id="e13e3-133">Der Cursor berührt die Zeichen Oberfläche (Wert = 1).</span><span class="sxs-lookup"><span data-stu-id="e13e3-133">The cursor is touching the drawing surface (Value = 1).</span></span></li>
<li><span data-ttu-id="e13e3-134">Der Cursor wird umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="e13e3-134">The cursor is inverted.</span></span> <span data-ttu-id="e13e3-135">Beispielsweise zeigt das Ende des Stifts auf die Oberfläche (Wert = 2).</span><span class="sxs-lookup"><span data-stu-id="e13e3-135">For example, the eraser end of the pen is pointing toward the surface (Value = 2).</span></span></li>
<li><span data-ttu-id="e13e3-136">Nicht verwendet (Wert = 4).</span><span class="sxs-lookup"><span data-stu-id="e13e3-136">Not used (Value = 4).</span></span></li>
<li><span data-ttu-id="e13e3-137">Die Schaltfläche "Barrel" wird gedrückt (Wert = 8).</span><span class="sxs-lookup"><span data-stu-id="e13e3-137">The barrel button is pressed (Value = 8).</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <span data-ttu-id="e13e3-138"><dt><strong>STR_GUID_TIMERTICK oder GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-138"><dt><strong>STR_GUID_TIMERTICK or GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-139">Der Zeitpunkt, zu dem das Paket generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e13e3-139">The time the packet was generated.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <span data-ttu-id="e13e3-140"><dt><strong>STR_GUID_TIMERTICK oder GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-140"><dt><strong>STR_GUID_TIMERTICK or GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-141">Der Zeitpunkt, zu dem das Paket generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e13e3-141">The time the packet was generated.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_SERIALNUMBER_or_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><span id="str_guid_serialnumber_or_guid_packetproperty_guid_serial_number"></span><span id="STR_GUID_SERIALNUMBER_OR_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><dl> <span data-ttu-id="e13e3-142"><dt><strong>STR_GUID_SERIALNUMBER oder GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-142"><dt><strong>STR_GUID_SERIALNUMBER or GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-143">Die Paket Eigenschaft zum Identifizieren des Pakets.</span><span class="sxs-lookup"><span data-stu-id="e13e3-143">The packet property for identifying the packet.</span></span><br/> <span data-ttu-id="e13e3-144">Dies ist derselbe Wert, den Sie verwenden, um das Paket aus der Paket Warteschlange abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e13e3-144">This is the same value you use to retrieve the packet from the packet queue.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_NORMALPRESSURE_or_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><span id="str_guid_normalpressure_or_guid_packetproperty_guid_normal_pressure"></span><span id="STR_GUID_NORMALPRESSURE_OR_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><dl> <span data-ttu-id="e13e3-145"><dt><strong>STR_GUID_NORMALPRESSURE oder GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-145"><dt><strong>STR_GUID_NORMALPRESSURE or GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-146">Der Druck der Stift Spitze senkrecht zur Tablet-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="e13e3-146">The pressure of the pen tip perpendicular to the tablet surface.</span></span><br/> <span data-ttu-id="e13e3-147">Je größer der Druck der Stift Spitze ist, desto mehr frei Hand Eingaben werden gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e13e3-147">The greater the pressure on the pen tip, the more ink that is drawn.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TANGENTPRESSURE_or_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><span id="str_guid_tangentpressure_or_guid_packetproperty_guid_tangent_pressure"></span><span id="STR_GUID_TANGENTPRESSURE_OR_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><dl> <span data-ttu-id="e13e3-148"><dt><strong>STR_GUID_TANGENTPRESSURE oder GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-148"><dt><strong>STR_GUID_TANGENTPRESSURE or GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-149">Der Druck der Stift Spitze auf der Ebene der Tablet-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="e13e3-149">The pressure of the pen tip along the plane of the tablet surface.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_BUTTONPRESSURE_or_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><span id="str_guid_buttonpressure_or_guid_packetproperty_guid_button_pressure"></span><span id="STR_GUID_BUTTONPRESSURE_OR_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><dl> <span data-ttu-id="e13e3-150"><dt><strong>STR_GUID_BUTTONPRESSURE oder GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-150"><dt><strong>STR_GUID_BUTTONPRESSURE or GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-151">Der Druck auf eine Druck Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="e13e3-151">The pressure on a pressure sensitive button.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_XTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><span id="str_guid_xtiltorientation_or_guid_packetproperty_guid_x_tilt_orientation"></span><span id="STR_GUID_XTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><dl> <span data-ttu-id="e13e3-152"><dt><strong>STR_GUID_XTILTORIENTATION oder GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-152"><dt><strong>STR_GUID_XTILTORIENTATION or GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-153">Der Winkel zwischen der y-, der z-Ebene und dem Stift und der y-Achsen Ebene.</span><span class="sxs-lookup"><span data-stu-id="e13e3-153">The angle between the y,z-plane and the pen and y-axis plane.</span></span><br/> <span data-ttu-id="e13e3-154">Gilt für einen Stift Cursor.</span><span class="sxs-lookup"><span data-stu-id="e13e3-154">Applies to a pen cursor.</span></span><br/> <span data-ttu-id="e13e3-155">Der Wert ist 0 (null), wenn der Stift senkrecht zur Zeichen Oberfläche ist und positiv ist, wenn sich der Stift rechts von senkrecht befindet.</span><span class="sxs-lookup"><span data-stu-id="e13e3-155">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><span id="str_guid_ytiltorientation_or_guid_packetproperty_guid_y_tilt_orientation"></span><span id="STR_GUID_YTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><dl> <span data-ttu-id="e13e3-156"><dt><strong>STR_GUID_YTILTORIENTATION oder GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-156"><dt><strong>STR_GUID_YTILTORIENTATION or GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-157">Der Winkel zwischen der x-, der z-Ebene und der Ebene des Stifts und der x-Achse.</span><span class="sxs-lookup"><span data-stu-id="e13e3-157">The angle between the x,z-plane and the pen and x-axis plane.</span></span><br/> <span data-ttu-id="e13e3-158">Gilt für einen Stift Cursor.</span><span class="sxs-lookup"><span data-stu-id="e13e3-158">Applies to a pen cursor.</span></span><br/> <span data-ttu-id="e13e3-159">Der Wert ist 0 (null), wenn der Stift senkrecht zur Zeichnungs Oberfläche ist und positiv ist, wenn sich der Stift über dem Benutzer befindet oder nicht.</span><span class="sxs-lookup"><span data-stu-id="e13e3-159">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is upward or away from the user.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_AZIMUTHORIENTATION_or_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><span id="str_guid_azimuthorientation_or_guid_packetproperty_guid_azimuth_orientation"></span><span id="STR_GUID_AZIMUTHORIENTATION_OR_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><dl> <span data-ttu-id="e13e3-160"><dt><strong>STR_GUID_AZIMUTHORIENTATION oder GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-160"><dt><strong>STR_GUID_AZIMUTHORIENTATION or GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-161">Die Drehung des Cursors im Uhrzeigersinn um die z-Achse durch einen vollständigen kreisförmigen Bereich.</span><span class="sxs-lookup"><span data-stu-id="e13e3-161">The clockwise rotation of the cursor about the z-axis through a full circular range.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_ALTITUDEORIENTATION_or_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><span id="str_guid_altitudeorientation_or_guid_packetproperty_guid_altitude_orientation"></span><span id="STR_GUID_ALTITUDEORIENTATION_OR_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><dl> <span data-ttu-id="e13e3-162"><dt><strong>STR_GUID_ALTITUDEORIENTATION oder GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-162"><dt><strong>STR_GUID_ALTITUDEORIENTATION or GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-163">Der Winkel zwischen der Achse des Stifts und der Oberfläche des Tablets.</span><span class="sxs-lookup"><span data-stu-id="e13e3-163">The angle between the axis of the pen and the surface of the tablet.</span></span><br/> <span data-ttu-id="e13e3-164">Der Wert ist 0 (null), wenn der Stift parallel zur Oberfläche und 90 ist, wenn der Stift senkrecht zur Oberfläche ist.</span><span class="sxs-lookup"><span data-stu-id="e13e3-164">The value is 0 when the pen is parallel to the surface and 90 when the pen is perpendicular to the surface.</span></span><br/> <span data-ttu-id="e13e3-165">Die Werte sind negativ, wenn der Stift invertiert wird.</span><span class="sxs-lookup"><span data-stu-id="e13e3-165">The values are negative when the pen is inverted.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TWISTORIENTATION_or_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><span id="str_guid_twistorientation_or_guid_packetproperty_guid_twist_orientation"></span><span id="STR_GUID_TWISTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><dl> <span data-ttu-id="e13e3-166"><dt><strong>STR_GUID_TWISTORIENTATION oder GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-166"><dt><strong>STR_GUID_TWISTORIENTATION or GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-167">Die Drehung des Cursors im Uhrzeigersinn um die eigene Achse.</span><span class="sxs-lookup"><span data-stu-id="e13e3-167">The clockwise rotation of the cursor about its own axis.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PITCHROTATION_or_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><span id="str_guid_pitchrotation_or_guid_packetproperty_guid_pitch_rotation"></span><span id="STR_GUID_PITCHROTATION_OR_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><dl> <span data-ttu-id="e13e3-168"><dt><strong>STR_GUID_PITCHROTATION oder GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-168"><dt><strong>STR_GUID_PITCHROTATION or GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-169">Die Paket Eigenschaft, die angibt, ob die Spitze oberhalb oder unterhalb einer horizontalen Linie liegt, die senkrecht zur Schreibfläche ist.</span><span class="sxs-lookup"><span data-stu-id="e13e3-169">The packet property that indicates whether the tip is above or below a horizontal line that is perpendicular to the writing surface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e13e3-170">Hierfür ist ein 3D-Digitalisierer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e13e3-170">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="e13e3-171">Der Wert ist positiv, wenn sich die Spitze oberhalb der Linie befindet, und negativ, wenn Sie sich unterhalb der Linie befindet.</span><span class="sxs-lookup"><span data-stu-id="e13e3-171">The value is positive if the tip is above the line and negative if it is below the line.</span></span> <span data-ttu-id="e13e3-172">Wenn Sie z. b. den Stift vor Ihnen halten und auf eine imaginäre Wand schreiben, ist die Tonhöhe positiv, wenn der Tipp über einer Linie liegt, die von Ihnen bis zur Wand reicht.</span><span class="sxs-lookup"><span data-stu-id="e13e3-172">For example, if you hold the pen in front of you and write on an imaginary wall, the pitch is positive if the tip is above a line extending from you to the wall.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_ROLLROTATION_or_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><span id="str_guid_rollrotation_or_guid_packetproperty_guid_roll_rotation"></span><span id="STR_GUID_ROLLROTATION_OR_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><dl> <span data-ttu-id="e13e3-173"><dt><strong>STR_GUID_ROLLROTATION oder GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-173"><dt><strong>STR_GUID_ROLLROTATION or GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-174">Die Drehung im Uhrzeigersinn um die eigene Achse.</span><span class="sxs-lookup"><span data-stu-id="e13e3-174">The clockwise rotation of the pen around its own axis.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e13e3-175">Hierfür ist ein 3D-Digitalisierer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e13e3-175">This requires a 3D digitizer.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <span data-ttu-id="e13e3-176"><dt><strong>STR_GUID_YAWROTATION oder GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-176"><dt><strong>STR_GUID_YAWROTATION or GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-177">Der Winkel des Stifts links oder rechts um den Mittelpunkt der horizontalen Achse, wenn der Stift horizontal ist.</span><span class="sxs-lookup"><span data-stu-id="e13e3-177">The angle of the pen to the left or right around the center of its horizontal axis when the pen is horizontal.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e13e3-178">Hierfür ist ein 3D-Digitalisierer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e13e3-178">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="e13e3-179">Wenn Sie den Stift vor Ihnen halten und auf eine imaginäre Wand schreiben, gibt 0 (null), dass der Stift senkrecht zur Wand ist.</span><span class="sxs-lookup"><span data-stu-id="e13e3-179">If you hold the pen in front of you and write on an imaginary wall, zero yaw indicates that the pen is perpendicular to the wall.</span></span> <span data-ttu-id="e13e3-180">Der Wert ist negativ, wenn der Tipp Links von senkrecht und positiv ist, wenn der Tipp rechts von senkrecht ist.</span><span class="sxs-lookup"><span data-stu-id="e13e3-180">The value is negative if the tip is to the left of perpendicular and positive if the tip is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <span data-ttu-id="e13e3-181"><dt><strong>STR_GUID_YAWROTATION oder GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-181"><dt><strong>STR_GUID_YAWROTATION or GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-182">Der Winkel des Stifts links oder rechts um den Mittelpunkt der horizontalen Achse, wenn der Stift horizontal ist.</span><span class="sxs-lookup"><span data-stu-id="e13e3-182">The angle of the pen to the left or right around the center of its horizontal axis when the pen is horizontal.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e13e3-183">Hierfür ist ein 3D-Digitalisierer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e13e3-183">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="e13e3-184">Wenn Sie den Stift vor Ihnen halten und auf eine imaginäre Wand schreiben, gibt 0 (null), dass der Stift senkrecht zur Wand ist.</span><span class="sxs-lookup"><span data-stu-id="e13e3-184">If you hold the pen in front of you and write on an imaginary wall, zero yaw indicates that the pen is perpendicular to the wall.</span></span> <span data-ttu-id="e13e3-185">Der Wert ist negativ, wenn der Tipp Links von senkrecht und positiv ist, wenn der Tipp rechts von senkrecht ist.</span><span class="sxs-lookup"><span data-stu-id="e13e3-185">The value is negative if the tip is to the left of perpendicular and positive if the tip is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_WIDTH_or_GUID_PACKETPROPERTY_GUID_WIDTH"></span><span id="str_guid_width_or_guid_packetproperty_guid_width"></span><span id="STR_GUID_WIDTH_OR_GUID_PACKETPROPERTY_GUID_WIDTH"></span><dl> <span data-ttu-id="e13e3-186"><dt><strong>STR_GUID_WIDTH oder GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-186"><dt><strong>STR_GUID_WIDTH or GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-187">Die Breite des Kontakt Bereichs für einen Fingerabdruck-Digitalisierer.</span><span class="sxs-lookup"><span data-stu-id="e13e3-187">The width of the contact area on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_HEIGHT_or_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><span id="str_guid_height_or_guid_packetproperty_guid_height"></span><span id="STR_GUID_HEIGHT_OR_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><dl> <span data-ttu-id="e13e3-188"><dt><strong>STR_GUID_HEIGHT oder GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-188"><dt><strong>STR_GUID_HEIGHT or GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-189">Die Höhe des Kontakt Bereichs für einen Fingerabdruck-Digitalisierer.</span><span class="sxs-lookup"><span data-stu-id="e13e3-189">The height of the contact area on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_FINGERCONTACTCONFIDENCE_or_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><span id="str_guid_fingercontactconfidence_or_guid_packetproperty_guid_fingercontactconfidence"></span><span id="STR_GUID_FINGERCONTACTCONFIDENCE_OR_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><dl> <span data-ttu-id="e13e3-190"><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE oder GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-190"><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE or GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-191">Das Maß an Vertrauen, dass es Fingerkontakt für einen Touch-Digitalisierer gab.</span><span class="sxs-lookup"><span data-stu-id="e13e3-191">The level of confidence that there was finger contact on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_DEVICE_CONTACT_ID_or_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><span id="str_guid_device_contact_id_or_guid_packetproperty_guid_device_contact_id"></span><span id="STR_GUID_DEVICE_CONTACT_ID_OR_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><dl> <span data-ttu-id="e13e3-192"><dt><strong>STR_GUID_DEVICE_CONTACT_ID oder GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="e13e3-192"><dt><strong>STR_GUID_DEVICE_CONTACT_ID or GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e13e3-193">Der Bezeichner des Geräte Kontakts für ein Paket.</span><span class="sxs-lookup"><span data-stu-id="e13e3-193">The device contact identifier for a packet.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="e13e3-194">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e13e3-194">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e13e3-195">Alle Paket Werte, die von der Tablet-Hardware stammen, sind 32-Bit-Ganzzahlen.</span><span class="sxs-lookup"><span data-stu-id="e13e3-195">All packet values coming from the tablet hardware are 32-bit size integers.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e13e3-196">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e13e3-196">Requirements</span></span>



| <span data-ttu-id="e13e3-197">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e13e3-197">Requirement</span></span> | <span data-ttu-id="e13e3-198">Wert</span><span class="sxs-lookup"><span data-stu-id="e13e3-198">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e13e3-199">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e13e3-199">Minimum supported client</span></span><br/> | <span data-ttu-id="e13e3-200">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e13e3-200">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e13e3-201">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e13e3-201">Minimum supported server</span></span><br/> | <span data-ttu-id="e13e3-202">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e13e3-202">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e13e3-203">Header</span><span class="sxs-lookup"><span data-stu-id="e13e3-203">Header</span></span><br/>                   | <dl> <span data-ttu-id="e13e3-204"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="e13e3-204"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e13e3-205">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e13e3-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e13e3-206">**IsPacketPropertySupported-Methode**</span><span class="sxs-lookup"><span data-stu-id="e13e3-206">**IsPacketPropertySupported Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported)
</dt> <dt>

[<span data-ttu-id="e13e3-207">**GetPropertyMetrics-Methode**</span><span class="sxs-lookup"><span data-stu-id="e13e3-207">**GetPropertyMetrics Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics)
</dt> <dt>

[<span data-ttu-id="e13e3-208">**Iinktablet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e13e3-208">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




