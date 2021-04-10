---
description: COPP-Abfrage Verweis
ms.assetid: 11eb1443-857d-4516-a5cb-c3cc02a5eba4
title: COPP-Abfrage Verweis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41de36f3cdcc37a38e2ebc53caa7b6b37c204d9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041305"
---
# <a name="copp-query-reference"></a><span data-ttu-id="5ed53-103">COPP-Abfrage Verweis</span><span class="sxs-lookup"><span data-stu-id="5ed53-103">COPP Query Reference</span></span>

<span data-ttu-id="5ed53-104">In diesem Abschnitt werden die Statusabfragen beschrieben, die vom Certified Output Protection Protocol (COPP) unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="5ed53-104">This section describes the status queries that are supported by Certified Output Protection Protocol (COPP).</span></span> <span data-ttu-id="5ed53-105">Für jede Abfrage wird die GUID, die die Abfrage definiert, zusammen mit den Eingabedaten und den Rückgabe Daten aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="5ed53-105">For each query, the GUID that defines the query is listed, along with the input data and return data.</span></span>



| <span data-ttu-id="5ed53-106">Abfrage</span><span class="sxs-lookup"><span data-stu-id="5ed53-106">Query</span></span>                   | <span data-ttu-id="5ed53-107">GUID</span><span class="sxs-lookup"><span data-stu-id="5ed53-107">GUID</span></span>                                     |
|-------------------------|------------------------------------------|
| <span data-ttu-id="5ed53-108">Busdaten</span><span class="sxs-lookup"><span data-stu-id="5ed53-108">Bus Data</span></span>                | <span data-ttu-id="5ed53-109">**DXVA- \_ coppquerybusdata**</span><span class="sxs-lookup"><span data-stu-id="5ed53-109">**DXVA\_COPPQueryBusData**</span></span>               |
| <span data-ttu-id="5ed53-110">Connectortyp</span><span class="sxs-lookup"><span data-stu-id="5ed53-110">Connector Type</span></span>          | <span data-ttu-id="5ed53-111">**DXVA " \_ coppqueryconnector Type"**</span><span class="sxs-lookup"><span data-stu-id="5ed53-111">**DXVA\_COPPQueryConnectorType**</span></span>         |
| <span data-ttu-id="5ed53-112">Anzeigen von Daten</span><span class="sxs-lookup"><span data-stu-id="5ed53-112">Display Data</span></span>            | <span data-ttu-id="5ed53-113">**DXVA-" \_ coppquerydisplaydata"**</span><span class="sxs-lookup"><span data-stu-id="5ed53-113">**DXVA\_COPPQueryDisplayData**</span></span>           |
| <span data-ttu-id="5ed53-114">HDCP-Schlüsseldaten</span><span class="sxs-lookup"><span data-stu-id="5ed53-114">HDCP Key Data</span></span>           | <span data-ttu-id="5ed53-115">**DXVA-" \_ coppqueryhdcpkeydata"**</span><span class="sxs-lookup"><span data-stu-id="5ed53-115">**DXVA\_COPPQueryHDCPKeyData**</span></span>           |
| <span data-ttu-id="5ed53-116">Globale Schutz Ebene</span><span class="sxs-lookup"><span data-stu-id="5ed53-116">Global Protection Level</span></span> | <span data-ttu-id="5ed53-117">**DXVA- \_ coppqueryglobalschutzlevel**</span><span class="sxs-lookup"><span data-stu-id="5ed53-117">**DXVA\_COPPQueryGlobalProtectionLevel**</span></span> |
| <span data-ttu-id="5ed53-118">Lokale Schutz Ebene</span><span class="sxs-lookup"><span data-stu-id="5ed53-118">Local Protection Level</span></span>  | <span data-ttu-id="5ed53-119">**DXVA- \_ coppquerylocalschutzlevel**</span><span class="sxs-lookup"><span data-stu-id="5ed53-119">**DXVA\_COPPQueryLocalProtectionLevel**</span></span>  |
| <span data-ttu-id="5ed53-120">Schutztyp</span><span class="sxs-lookup"><span data-stu-id="5ed53-120">Protection Type</span></span>         | <span data-ttu-id="5ed53-121">**DXVA-" \_ coppqueryschutztype"**</span><span class="sxs-lookup"><span data-stu-id="5ed53-121">**DXVA\_COPPQueryProtectionType**</span></span>        |
| <span data-ttu-id="5ed53-122">Signaling</span><span class="sxs-lookup"><span data-stu-id="5ed53-122">Signaling</span></span>               | <span data-ttu-id="5ed53-123">**DXVA- \_ coppquerysignalisierung**</span><span class="sxs-lookup"><span data-stu-id="5ed53-123">**DXVA\_COPPQuerySignaling**</span></span>             |



 

<span data-ttu-id="5ed53-124">Busdaten Abfrage</span><span class="sxs-lookup"><span data-stu-id="5ed53-124">Bus Data Query</span></span>

<span data-ttu-id="5ed53-125">Gibt den Typ des e/a-Busses zurück, der vom Grafikadapter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ed53-125">Returns the type of I/O bus used by the graphics adapter.</span></span>

-   <span data-ttu-id="5ed53-126">**GUID**: DXVA \_ coppquerybusdata</span><span class="sxs-lookup"><span data-stu-id="5ed53-126">**GUID**: DXVA\_COPPQueryBusData</span></span>
-   <span data-ttu-id="5ed53-127">**Eingabedaten**: keine.</span><span class="sxs-lookup"><span data-stu-id="5ed53-127">**Input data**: None.</span></span>
-   <span data-ttu-id="5ed53-128">**Return Data**: gibt eine [**DXVA-Struktur " \_ coppstatus Data**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) " zurück.</span><span class="sxs-lookup"><span data-stu-id="5ed53-128">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="5ed53-129">Der Bustyp wird im **dwdata** -Member als Flag aus der [**COPP \_ BusType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) -Enumeration zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5ed53-129">The bus type is returned in the **dwData** member as a flag from the [**COPP\_BusType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_bustype) enumeration.</span></span>

<span data-ttu-id="5ed53-130">Connector-typabfrage</span><span class="sxs-lookup"><span data-stu-id="5ed53-130">Connector Type Query</span></span>

<span data-ttu-id="5ed53-131">Gibt den physischen Verbindungstyp zurück.</span><span class="sxs-lookup"><span data-stu-id="5ed53-131">Returns the physical connector type.</span></span>

-   <span data-ttu-id="5ed53-132">**GUID**: DXVA-" \_ coppqueryconnector Type"</span><span class="sxs-lookup"><span data-stu-id="5ed53-132">**GUID**: DXVA\_COPPQueryConnectorType</span></span>
-   <span data-ttu-id="5ed53-133">**Eingabedaten**: keine.</span><span class="sxs-lookup"><span data-stu-id="5ed53-133">**Input data**: None.</span></span>
-   <span data-ttu-id="5ed53-134">**Return Data**: gibt eine [**DXVA-Struktur " \_ coppstatus Data**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) " zurück.</span><span class="sxs-lookup"><span data-stu-id="5ed53-134">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="5ed53-135">Der connectiontyp wird im **dwdata** -Member als Flag aus der [**COPP \_ Stecker Type**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) -Enumeration zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5ed53-135">The connector type is returned in the **dwData** member as a flag from the [**COPP\_ConnectorType**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_connectortype) enumeration.</span></span>

<span data-ttu-id="5ed53-136">Datenabfrage anzeigen</span><span class="sxs-lookup"><span data-stu-id="5ed53-136">Display Data Query</span></span>

<span data-ttu-id="5ed53-137">Gibt eine Beschreibung des Videosignals zurück, das über den Connector übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="5ed53-137">Returns a description of the video signal that is being transmitted over the connector.</span></span>

<span data-ttu-id="5ed53-138">Das über den Connector übertragene Videosignal weist nicht notwendigerweise dasselbe Format wie der Desktop Anzeigemodus auf.</span><span class="sxs-lookup"><span data-stu-id="5ed53-138">The video signal that is transmitted over the connector does not necessarily have the same format as the desktop display mode.</span></span> <span data-ttu-id="5ed53-139">Der Desktop Anzeigemodus kann z. b. 1024 x 768 Pixel um 85 Hz betragen, während der Connector ein S-Video-Connector sein kann, der ein Video Signal mit 720x480 Pixel, 60/1.01 Hz mit Zeilen Sprung überträgt.</span><span class="sxs-lookup"><span data-stu-id="5ed53-139">For example, the desktop display mode might be 1024x768 pixels at 85 Hz, while the connector might be an S-Video connector that transmits a video signal at 720x480 pixels, 60/1.01 Hz interlaced.</span></span> <span data-ttu-id="5ed53-140">In diesem Fall würde der Treiber die Auflösung des S-Video Signals und nicht die Desktop Auflösung zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5ed53-140">In that case, the driver would return the resolution of the S-Video signal, not the desktop resolution.</span></span>

-   <span data-ttu-id="5ed53-141">**GUID**: DXVA \_ coppquerydisplaydata</span><span class="sxs-lookup"><span data-stu-id="5ed53-141">**GUID**: DXVA\_COPPQueryDisplayData</span></span>
-   <span data-ttu-id="5ed53-142">**Eingabedaten**: keine.</span><span class="sxs-lookup"><span data-stu-id="5ed53-142">**Input data**: None.</span></span>
-   <span data-ttu-id="5ed53-143">**Return Data**: gibt eine [**DXVA-Struktur von " \_ coppstatus-displayData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) " zurück.</span><span class="sxs-lookup"><span data-stu-id="5ed53-143">**Return data**: Returns a [**DXVA\_COPPStatusDisplayData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdisplaydata) structure.</span></span>

<span data-ttu-id="5ed53-144">HDCP-Schlüsseldaten Abfrage</span><span class="sxs-lookup"><span data-stu-id="5ed53-144">HDCP Key Data Query</span></span>

<span data-ttu-id="5ed53-145">Gibt den HDCP-Schlüsselauswahl Vektor (B-KSV) des Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="5ed53-145">Returns the device's HDCP key selection vector (B-KSV).</span></span>

<span data-ttu-id="5ed53-146">Der KSV ist ein Bezeichner, der dem Gerätehersteller zur Verfügung gestellt wird und im HDCP-Authentifizierungs-und-Setup Prozess verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ed53-146">The KSV is an identifier provided to the device manufacturer, and is used in the HDCP authentication and setup process.</span></span> <span data-ttu-id="5ed53-147">Die Anwendung sollte diesen Wert mit der Liste der gesperrten ksvs überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5ed53-147">The application should check this value against the list of revoked KSVs.</span></span> <span data-ttu-id="5ed53-148">Der Mechanismus zum Abrufen der KSV-Sperr Liste liegt außerhalb des Gültigkeits Bereichs des COPP-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="5ed53-148">The mechanism for obtaining the KSV revocation list is outside the scope of the COPP protocol.</span></span> <span data-ttu-id="5ed53-149">Weitere Informationen finden Sie in der HDCP-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="5ed53-149">For more information, consult the HDCP specification.</span></span>

<span data-ttu-id="5ed53-150">Diese Abfrage bestimmt auch, ob das verbundene HDCP-Gerät ein Monitor oder ein HDCP-Wiederholungs Modul ist.</span><span class="sxs-lookup"><span data-stu-id="5ed53-150">This query also determines whether the connected HDCP device is a monitor or an HDCP repeater.</span></span> <span data-ttu-id="5ed53-151">Die Anwendung sollte geschützte Inhalte nicht wiedergeben, wenn das HDCP-Gerät ein HDCP-Repeater ist, da diese nicht von COPP unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="5ed53-151">The application should not play protected content if the HDCP device is an HDCP repeater, because these are not supported by COPP.</span></span>

-   <span data-ttu-id="5ed53-152">**GUID**: DXVA \_ coppqueryhdcpkeydata</span><span class="sxs-lookup"><span data-stu-id="5ed53-152">**GUID**: DXVA\_COPPQueryHDCPKeyData</span></span>
-   <span data-ttu-id="5ed53-153">**Eingabedaten**: keine.</span><span class="sxs-lookup"><span data-stu-id="5ed53-153">**Input data**: None.</span></span>
-   <span data-ttu-id="5ed53-154">**Return Data**: gibt eine [**DXVA- \_ coppstatuushdcpkeydata**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="5ed53-154">**Return data**: Returns a [**DXVA\_COPPStatusHDCPKeyData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatushdcpkeydata) structure.</span></span>

<span data-ttu-id="5ed53-155">Abfrage der globalen Schutz Ebene</span><span class="sxs-lookup"><span data-stu-id="5ed53-155">Global Protection Level Query</span></span>

<span data-ttu-id="5ed53-156">Gibt die globale Schutz Ebene für einen angegebenen Schutzmechanismus zurück.</span><span class="sxs-lookup"><span data-stu-id="5ed53-156">Returns the global protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="5ed53-157">Die globale Schutz Ebene ist die Schutz Ebene, die zurzeit auf den Connector angewendet wird, unabhängig davon, wie der Grafiktreiber angewiesen wurde, den Schutz anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="5ed53-157">The global protection level is the protection level that is currently being applied on the connector, regardless of how the graphics driver was instructed to apply the protection.</span></span> <span data-ttu-id="5ed53-158">Beispielsweise kann eine Anwendung die ACP-Schutz Ebene durch Aufrufen der **changedisplaysettingsex** -Funktion festlegen.</span><span class="sxs-lookup"><span data-stu-id="5ed53-158">For example, an application can set the ACP protection level by calling the **ChangeDisplaySettingsEx** function.</span></span> <span data-ttu-id="5ed53-159">In diesem Fall würde die globale Schutz Ebene diese Einstellung widerspiegeln, auch wenn Sie nicht über COPP angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="5ed53-159">In that case, the global protection level would reflect this setting, even though it was not requested through COPP.</span></span>

-   <span data-ttu-id="5ed53-160">**GUID**: DXVA \_ coppqueryglobalschutzlevel</span><span class="sxs-lookup"><span data-stu-id="5ed53-160">**GUID**: DXVA\_COPPQueryGlobalProtectionLevel</span></span>
-   <span data-ttu-id="5ed53-161">**Eingabedaten**: der abzufragende Schutzmechanismus, der als 32-Bit-Ganzzahl angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5ed53-161">**Input data**: The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="5ed53-162">Siehe [COPP-Schutztyp-Flags](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5ed53-162">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span>
-   <span data-ttu-id="5ed53-163">**Return Data**: gibt eine [**DXVA-Struktur " \_ coppstatus Data**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) " zurück.</span><span class="sxs-lookup"><span data-stu-id="5ed53-163">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="5ed53-164">Die aktuelle Schutz Ebene wird im **dwdata** -Member zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5ed53-164">The current protection level is returned in the **dwData** member.</span></span> <span data-ttu-id="5ed53-165">Die Bedeutung dieses Werts hängt von dem abgefragten Schutzmechanismus ab.</span><span class="sxs-lookup"><span data-stu-id="5ed53-165">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="5ed53-166">Für jeden Schutzmechanismus ist der Wert des **dwdata** -Members ein Flag aus einer anderen Enumeration, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5ed53-166">For each protection mechanism, the value of the **dwData** member is a flag from a different enumeration, as shown in the following table.</span></span>

    | <span data-ttu-id="5ed53-167">Schutzmechanismus</span><span class="sxs-lookup"><span data-stu-id="5ed53-167">Protection mechanism</span></span> | <span data-ttu-id="5ed53-168">Enumeration</span><span class="sxs-lookup"><span data-stu-id="5ed53-168">Enumeration</span></span>                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | <span data-ttu-id="5ed53-169">ACP</span><span class="sxs-lookup"><span data-stu-id="5ed53-169">ACP</span></span>                  | [<span data-ttu-id="5ed53-170">**COPP \_ -ACP- \_ Schutz \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="5ed53-170">**COPP\_ACP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | <span data-ttu-id="5ed53-171">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="5ed53-171">CGMS-A</span></span>               | [<span data-ttu-id="5ed53-172">**COPP- \_ cgmsa- \_ Schutz \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="5ed53-172">**COPP\_CGMSA\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | <span data-ttu-id="5ed53-173">HDCP</span><span class="sxs-lookup"><span data-stu-id="5ed53-173">HDCP</span></span>                 | [<span data-ttu-id="5ed53-174">**COPP- \_ HDCP- \_ Schutz \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="5ed53-174">**COPP\_HDCP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

<span data-ttu-id="5ed53-175">Abfrage der lokalen Schutz Ebene</span><span class="sxs-lookup"><span data-stu-id="5ed53-175">Local Protection Level Query</span></span>

<span data-ttu-id="5ed53-176">Gibt die lokale Schutz Ebene für einen angegebenen Schutzmechanismus zurück.</span><span class="sxs-lookup"><span data-stu-id="5ed53-176">Returns the local protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="5ed53-177">Die lokale Schutz Ebene ist die Schutz Ebene, die durch die aktuelle COPP-Sitzung angefordert wurde.</span><span class="sxs-lookup"><span data-stu-id="5ed53-177">The local protection level is the protection level that was requested through the current COPP session.</span></span> <span data-ttu-id="5ed53-178">Der Treiber kann eine höhere Schutz Ebene festlegen.</span><span class="sxs-lookup"><span data-stu-id="5ed53-178">The driver might set a higher protection level.</span></span>

-   <span data-ttu-id="5ed53-179">**GUID**: DXVA \_ coppquerylocalschutzlevel</span><span class="sxs-lookup"><span data-stu-id="5ed53-179">**GUID**: DXVA\_COPPQueryLocalProtectionLevel</span></span>
-   <span data-ttu-id="5ed53-180">**Eingabedaten**: der zu Abfrage Ende Schutzmechanismus als 32-Bit-Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="5ed53-180">**Input data**: The protection mechanism to query, as a 32-bit integer.</span></span> <span data-ttu-id="5ed53-181">Siehe [COPP-Schutztyp-Flags](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5ed53-181">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span>
-   <span data-ttu-id="5ed53-182">**Return Data**: gibt eine [**DXVA-Struktur " \_ coppstatus Data**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) " zurück.</span><span class="sxs-lookup"><span data-stu-id="5ed53-182">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="5ed53-183">Die aktuelle Schutz Ebene wird im **dwdata** -Member zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5ed53-183">The current protection level is returned in the **dwData** member.</span></span> <span data-ttu-id="5ed53-184">Die Bedeutung dieses Werts hängt von dem abgefragten Schutzmechanismus ab.</span><span class="sxs-lookup"><span data-stu-id="5ed53-184">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="5ed53-185">Für jeden Schutzmechanismus ist der Wert des **dwdata** -Members ein Flag aus einer anderen Enumeration, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5ed53-185">For each protection mechanism, the value of the **dwData** member is a flag from a different enumeration, as shown in the following table.</span></span>

    | <span data-ttu-id="5ed53-186">Schutzmechanismus</span><span class="sxs-lookup"><span data-stu-id="5ed53-186">Protection mechanism</span></span> | <span data-ttu-id="5ed53-187">Enumeration</span><span class="sxs-lookup"><span data-stu-id="5ed53-187">Enumeration</span></span>                                                           |
    |----------------------|-----------------------------------------------------------------------|
    | <span data-ttu-id="5ed53-188">ACP</span><span class="sxs-lookup"><span data-stu-id="5ed53-188">ACP</span></span>                  | [<span data-ttu-id="5ed53-189">**COPP \_ -ACP- \_ Schutz \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="5ed53-189">**COPP\_ACP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_acp_protection_level)     |
    | <span data-ttu-id="5ed53-190">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="5ed53-190">CGMS-A</span></span>               | [<span data-ttu-id="5ed53-191">**COPP- \_ cgmsa- \_ Schutz \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="5ed53-191">**COPP\_CGMSA\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_cgmsa_protection_level) |
    | <span data-ttu-id="5ed53-192">HDCP</span><span class="sxs-lookup"><span data-stu-id="5ed53-192">HDCP</span></span>                 | [<span data-ttu-id="5ed53-193">**COPP- \_ HDCP- \_ Schutz \_ Ebene**</span><span class="sxs-lookup"><span data-stu-id="5ed53-193">**COPP\_HDCP\_Protection\_Level**</span></span>](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_hdcp_protection_level)   |

    

     

<span data-ttu-id="5ed53-194">Schutztyp Abfrage</span><span class="sxs-lookup"><span data-stu-id="5ed53-194">Protection Type Query</span></span>

<span data-ttu-id="5ed53-195">Gibt die Schutzmechanismen zurück, die für den Connector verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5ed53-195">Returns the protection mechanisms that are available for the connector.</span></span>

-   <span data-ttu-id="5ed53-196">**GUID**: DXVA " \_ coppqueryschutztype"</span><span class="sxs-lookup"><span data-stu-id="5ed53-196">**GUID**: DXVA\_COPPQueryProtectionType</span></span>
-   <span data-ttu-id="5ed53-197">**Eingabedaten**: keine.</span><span class="sxs-lookup"><span data-stu-id="5ed53-197">**Input data**: None.</span></span>
-   <span data-ttu-id="5ed53-198">**Return Data**: gibt eine [**DXVA-Struktur " \_ coppstatus Data**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) " zurück.</span><span class="sxs-lookup"><span data-stu-id="5ed53-198">**Return data**: Returns a [**DXVA\_COPPStatusData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatusdata) structure.</span></span> <span data-ttu-id="5ed53-199">Die Schutzmechanismen werden im **dwdata** -Member als eine Kombination aus null oder mehr Flags zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5ed53-199">The protection mechanisms are returned in the **dwData** member as a combination of zero or more flags.</span></span> <span data-ttu-id="5ed53-200">Siehe [COPP-Schutztyp-Flags](copp-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5ed53-200">See [COPP Protection Type Flags](copp-protection-type-flags.md).</span></span> <span data-ttu-id="5ed53-201">Wenn mehr als ein Schutzmechanismus verfügbar ist, werden die Flags mit einem bitweisen **or** kombiniert.</span><span class="sxs-lookup"><span data-stu-id="5ed53-201">If more than one protection mechanism is available, the flags are combined with a bitwise **OR**.</span></span>

<span data-ttu-id="5ed53-202">Signalisierungs Abfrage</span><span class="sxs-lookup"><span data-stu-id="5ed53-202">Signaling Query</span></span>

<span data-ttu-id="5ed53-203">Gibt eine Liste mit allen Schutzstandards zurück, die vom Treiber unterstützt werden, dem derzeit aktiven Standard und dem aktuellen Seitenverhältnis oder anderen Signalisierungs Daten.</span><span class="sxs-lookup"><span data-stu-id="5ed53-203">Returns a list of all the protection standards that are supported by the driver, the standard that is currently active, and the current aspect ratio or other signaling data.</span></span>

-   <span data-ttu-id="5ed53-204">**GUID**: DXVA- \_ coppquerysignalisierung</span><span class="sxs-lookup"><span data-stu-id="5ed53-204">**GUID**: DXVA\_COPPQuerySignaling</span></span>
-   <span data-ttu-id="5ed53-205">**Eingabedaten**: keine.</span><span class="sxs-lookup"><span data-stu-id="5ed53-205">**Input data**: None.</span></span>
-   <span data-ttu-id="5ed53-206">**Return Data**: gibt eine [**DXVA-Struktur von " \_ coppstatuussignalingcmddata**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) " zurück.</span><span class="sxs-lookup"><span data-stu-id="5ed53-206">**Return data**: Returns a [**DXVA\_COPPStatusSignalingCmdData**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxva_coppstatussignalingcmddata) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5ed53-207">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5ed53-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ed53-208">Verwenden des Certified Output Protection-Protokolls (COPP)</span><span class="sxs-lookup"><span data-stu-id="5ed53-208">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



