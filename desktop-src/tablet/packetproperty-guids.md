---
description: In der folgenden Tabelle werden die von der Paket Eigenschafts Struktur verwendeten Paket Eigenschaften-GUIDs aufgelistet \_ .
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: PacketProperty-GUIDs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94591ccda5cd1f40b79c5cbb4fe80ca3ef99d2e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868928"
---
# <a name="packetproperty-guids"></a><span data-ttu-id="4dc06-103">PacketProperty-GUIDs</span><span class="sxs-lookup"><span data-stu-id="4dc06-103">PacketProperty GUIDs</span></span>

<span data-ttu-id="4dc06-104">In der folgenden Tabelle werden die von der [**Paket \_ Eigenschafts**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) Struktur verwendeten Paket Eigenschaften-GUIDs aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="4dc06-104">The following table lists packet property GUIDs used by the [**PACKET\_PROPERTY**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) structure.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4dc06-105">GUID</span><span class="sxs-lookup"><span data-stu-id="4dc06-105">GUID</span></span></th>
<th><span data-ttu-id="4dc06-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4dc06-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4dc06-107">GUID_ALTITUDE_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="4dc06-107">GUID_ALTITUDE_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="4dc06-108">Der Winkel zwischen der Achse des Stifts und der Oberfläche des Tablets.</span><span class="sxs-lookup"><span data-stu-id="4dc06-108">Angle between the axis of the pen and the surface of the tablet.</span></span> <span data-ttu-id="4dc06-109">Der Wert ist 0 (null), wenn der Stift parallel zur Oberfläche und 90 ist, wenn der Stift senkrecht zur Oberfläche ist.</span><span class="sxs-lookup"><span data-stu-id="4dc06-109">The value is 0 when the pen is parallel to the surface and 90 when the pen is perpendicular to the surface.</span></span> <span data-ttu-id="4dc06-110">Die Werte sind negativ, wenn der Stift invertiert wird.</span><span class="sxs-lookup"><span data-stu-id="4dc06-110">The values are negative when the pen is inverted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4dc06-111">GUID_AZIMUTH_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="4dc06-111">GUID_AZIMUTH_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="4dc06-112">Drehung im Uhrzeigersinn um die z-Achse um die z-Achse durch einen vollständigen kreisförmigen Bereich.</span><span class="sxs-lookup"><span data-stu-id="4dc06-112">Clockwise rotation of the cursor around the z-axis through a full circular range.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4dc06-113">GUID_BOXNUMBER</span><span class="sxs-lookup"><span data-stu-id="4dc06-113">GUID_BOXNUMBER</span></span><br/></td>
<td><span data-ttu-id="4dc06-114">Die GUID, die verwendet wird, um die Box-Nummer für eine frei Handerkennung abzurufen, wenn die Erkennung im Box-Modus ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4dc06-114">The GUID that is used to retrieve the box number for an ink recognition alternate when the recognizer is operating in box mode.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4dc06-115">GUID_BUTTON_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="4dc06-115">GUID_BUTTON_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="4dc06-116">Druck auf eine druckempfindliche Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="4dc06-116">Pressure on a pressure-sensitive button.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4dc06-117">GUID_NORMAL_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="4dc06-117">GUID_NORMAL_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="4dc06-118">Die GUID für das PacketProperty-Objekt, das den Druck der Stift Spitze senkrecht zur Tablet-Oberfläche darstellt.</span><span class="sxs-lookup"><span data-stu-id="4dc06-118">The GUID for the PacketProperty object that represents pressure of the pen tip perpendicular to the tablet surface.</span></span> <span data-ttu-id="4dc06-119">Je größer der Druck der Stift Spitze ist, desto mehr frei Hand Eingaben werden gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="4dc06-119">The greater the pressure put on the pen tip, the more ink that is drawn.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4dc06-120">GUID_PACKET_STATUS</span><span class="sxs-lookup"><span data-stu-id="4dc06-120">GUID_PACKET_STATUS</span></span><br/></td>
<td><span data-ttu-id="4dc06-121">Enthält mindestens einen der folgenden Flagwerte:</span><span class="sxs-lookup"><span data-stu-id="4dc06-121">Contains one or more of the following flag values:</span></span><br/>
<ul>
<li><span data-ttu-id="4dc06-122">Der Cursor berührt die Zeichen Oberfläche (Wert = 1).</span><span class="sxs-lookup"><span data-stu-id="4dc06-122">The cursor is touching the drawing surface (Value = 1).</span></span></li>
<li><span data-ttu-id="4dc06-123">Der Cursor wird umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="4dc06-123">The cursor is inverted.</span></span> <span data-ttu-id="4dc06-124">Beispielsweise zeigt das Ende des Stifts auf die Oberfläche (Wert = 2).</span><span class="sxs-lookup"><span data-stu-id="4dc06-124">For example, the eraser end of the pen is pointing toward the surface (Value = 2).</span></span></li>
<li><span data-ttu-id="4dc06-125">Nicht verwendet (Wert = 4).</span><span class="sxs-lookup"><span data-stu-id="4dc06-125">Not used (Value = 4).</span></span></li>
<li><span data-ttu-id="4dc06-126">Die Schaltfläche "Barrel" wird gedrückt (Wert = 8).</span><span class="sxs-lookup"><span data-stu-id="4dc06-126">The barrel button is pressed (Value = 8).</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4dc06-127">GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</span><span class="sxs-lookup"><span data-stu-id="4dc06-127">GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</span></span><br/></td>
<td><span data-ttu-id="4dc06-128">Der Bezeichner des Geräte Kontakts für ein Paket.</span><span class="sxs-lookup"><span data-stu-id="4dc06-128">The device contact identifier for a packet.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4dc06-129">GUID_SERIAL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="4dc06-129">GUID_SERIAL_NUMBER</span></span><br/></td>
<td><span data-ttu-id="4dc06-130">Identifiziert das Paket.</span><span class="sxs-lookup"><span data-stu-id="4dc06-130">Identifies the packet.</span></span> <span data-ttu-id="4dc06-131">Dies ist derselbe Wert, den Sie verwenden, um das Paket aus der Paket Warteschlange abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4dc06-131">This is the same value you use to retrieve the packet from the packet queue.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4dc06-132">GUID_TANGENT_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="4dc06-132">GUID_TANGENT_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="4dc06-133">Die GUID für das PacketProperty-Objekt, das den Druck der Stift Spitze auf der Ebene der Tablet-Oberfläche darstellt.</span><span class="sxs-lookup"><span data-stu-id="4dc06-133">The GUID for the PacketProperty object that represents pressure of the pen tip along the plane of the tablet surface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4dc06-134">GUID_TIMER_TICK</span><span class="sxs-lookup"><span data-stu-id="4dc06-134">GUID_TIMER_TICK</span></span><br/></td>
<td><span data-ttu-id="4dc06-135">Zeitpunkt, zu dem das Paket generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4dc06-135">Time the packet was generated.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4dc06-136">GUID_TWIST_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="4dc06-136">GUID_TWIST_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="4dc06-137">Drehung des Cursors im Uhrzeigersinn um die eigene Achse.</span><span class="sxs-lookup"><span data-stu-id="4dc06-137">Clockwise rotation of the cursor around its own axis.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4dc06-138">GUID_X</span><span class="sxs-lookup"><span data-stu-id="4dc06-138">GUID_X</span></span><br/></td>
<td><span data-ttu-id="4dc06-139">Die x-Koordinate im tablettkoordinatenbereich.</span><span class="sxs-lookup"><span data-stu-id="4dc06-139">The x-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="4dc06-140">Jedes Paket enthält diese Eigenschaft standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="4dc06-140">Each packet contains this property by default.</span></span> <span data-ttu-id="4dc06-141">Der Ursprung (0,0) des Tablets ist die linke obere Ecke.</span><span class="sxs-lookup"><span data-stu-id="4dc06-141">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4dc06-142">GUID_X_TILT_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="4dc06-142">GUID_X_TILT_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="4dc06-143">Bei einem Stift Cursor ist die x-Neigungs Ausrichtung der Winkel zwischen der y-, z-und der Stift-und der y-Achsen Ebene.</span><span class="sxs-lookup"><span data-stu-id="4dc06-143">For a pen cursor, the x-tilt orientation is the angle between the y,z-plane and the pen and y-axis plane.</span></span> <span data-ttu-id="4dc06-144">Der Wert ist 0 (null), wenn der Stift senkrecht zur Zeichen Oberfläche ist und positiv ist, wenn sich der Stift rechts von senkrecht befindet.</span><span class="sxs-lookup"><span data-stu-id="4dc06-144">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4dc06-145">GUID_Y</span><span class="sxs-lookup"><span data-stu-id="4dc06-145">GUID_Y</span></span><br/></td>
<td><span data-ttu-id="4dc06-146">Die y-Koordinate im tablettkoordinatenbereich.</span><span class="sxs-lookup"><span data-stu-id="4dc06-146">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="4dc06-147">Jedes Paket enthält diese Eigenschaft standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="4dc06-147">Each packet contains this property by default.</span></span> <span data-ttu-id="4dc06-148">Der Ursprung (0,0) des Tablets ist die linke obere Ecke.</span><span class="sxs-lookup"><span data-stu-id="4dc06-148">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4dc06-149">GUID_Y_TILT_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="4dc06-149">GUID_Y_TILT_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="4dc06-150">Bei einem Stift Cursor ist die y-Neigungs Ausrichtung der Winkel zwischen der x-, der z-Ebene und der Ebene des Stifts und der x-Achse.</span><span class="sxs-lookup"><span data-stu-id="4dc06-150">For a pen cursor, the y-tilt orientation is the angle between the x,z-plane and the pen and x-axis plane.</span></span> <span data-ttu-id="4dc06-151">Der Wert ist 0 (null), wenn der Stift senkrecht zur Zeichnungs Oberfläche ist und positiv ist, wenn sich der Stift nach oben oder vom Benutzer entfernt.</span><span class="sxs-lookup"><span data-stu-id="4dc06-151">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is upward, or away from the user.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4dc06-152">GUID_Z</span><span class="sxs-lookup"><span data-stu-id="4dc06-152">GUID_Z</span></span><br/></td>
<td><span data-ttu-id="4dc06-153">Die z-Koordinate oder den Abstand der Stift Spitze von der Tablet-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="4dc06-153">The z-coordinate or distance of the pen tip from the tablet surface.</span></span> <span data-ttu-id="4dc06-154">Der <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> Enumerationstyp bestimmt die Maßeinheit für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4dc06-154">The <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> enumeration type determines the unit of measurement for this property.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="4dc06-155">Das TangentPressure-Feld stellt den Druck auf der Ebene der Tablet-Oberfläche dar. das Feld für den normalen Druck steht für den Druck senkrecht zur Ebene der Tablet-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="4dc06-155">The TangentPressure field represents pressure along the plane of the tablet surface; the NormalPressure field represents pressure perpendicular to the plane of the tablet surface.</span></span>

 

 

 




