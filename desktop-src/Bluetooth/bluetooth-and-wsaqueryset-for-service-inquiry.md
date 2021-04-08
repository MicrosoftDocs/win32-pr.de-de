---
title: Bluetooth und wsaqueryset für die Dienst Anfrage
description: Verwenden der wsaqueryset-Struktur mit den Funktionen wsalookupservicebegin und WSALookupServiceNext, um Informationen über den Dienst Anfrage Prozess zu erhalten.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth und wsaqueryset für Dienst Anfrage Bluetooth
- Wsaqueryset Bluetooth, für Dienst Anfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656fa407829112005c9c54c5ab84c9c1bf2f4e33
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732201"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a><span data-ttu-id="d7556-105">Bluetooth und wsaqueryset für die Dienst Anfrage</span><span class="sxs-lookup"><span data-stu-id="d7556-105">Bluetooth and WSAQUERYSET for Service Inquiry</span></span>

<span data-ttu-id="d7556-106">Bluetooth verwendet die [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur mit verschiedenen Funktionen, um die Ermittlung von Geräten und Diensten im Bluetooth-Namespace (NS BTH) zu vereinfachen \_ .</span><span class="sxs-lookup"><span data-stu-id="d7556-106">Bluetooth uses the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure, with various functions, to facilitate the discovery of devices and services in the Bluetooth namespace, NS\_BTH.</span></span>

<span data-ttu-id="d7556-107">Die Funktionen [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) und [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) verwenden die [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur zum Abrufen von Daten über den Dienst Anfrage Prozess.</span><span class="sxs-lookup"><span data-stu-id="d7556-107">The [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) and [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) functions use the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure to obtain data about the service inquiry process.</span></span> <span data-ttu-id="d7556-108">In der folgenden Tabelle wird beschrieben, wie die Element Werte in der **wsaqueryset** -Struktur zu diesem Zweck festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d7556-108">The following table describes how to set the member values in the **WSAQUERYSET** structure for this purpose.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d7556-109">Member</span><span class="sxs-lookup"><span data-stu-id="d7556-109">Member</span></span></th>
<th><span data-ttu-id="d7556-110">Eingabe für wsalookupservicebegin</span><span class="sxs-lookup"><span data-stu-id="d7556-110">Input to WSALookupServiceBegin</span></span></th>
<th><span data-ttu-id="d7556-111">Rückgabewert von WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="d7556-111">Returned value from WSALookupServiceNext</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d7556-112"><strong>dwSize</strong></span><span class="sxs-lookup"><span data-stu-id="d7556-112"><strong>dwSize</strong></span></span></td>
<td><span data-ttu-id="d7556-113">Muss auf <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>wsaqueryset</strong></a>) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d7556-113">Must be set to <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span></span></td>
<td><span data-ttu-id="d7556-114"><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>wsaqueryset</strong></a>) vom System zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7556-114"><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) returned by system.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7556-115"><strong>dwoutputflags</strong></span><span class="sxs-lookup"><span data-stu-id="d7556-115"><strong>dwOutputFlags</strong></span></span></td>
<td><span data-ttu-id="d7556-116">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-116">Not used.</span></span></td>
<td><span data-ttu-id="d7556-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-117">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7556-118"><strong>lpszserviceingestancename</strong></span><span class="sxs-lookup"><span data-stu-id="d7556-118"><strong>lpszServiceInstanceName</strong></span></span></td>
<td><span data-ttu-id="d7556-119">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-119">Not used.</span></span></td>
<td><span data-ttu-id="d7556-120">Der Anzeige Name des dienstans, der als UTF-8-codierte Zeichenfolge aus der Standard sprach Codierung des SDP-Attributs für Bluetooth Service Name konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d7556-120">Display name of the service, converted as a UTF-8 encoded string from the default language encoding of the Bluetooth ServiceName SDP attribute.</span></span> <span data-ttu-id="d7556-121">Wird zurückgegeben, wenn LUP_RETURN_NAME angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d7556-121">Returned if LUP_RETURN_NAME is specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7556-122"><strong>lpserviceclassid</strong></span><span class="sxs-lookup"><span data-stu-id="d7556-122"><strong>lpServiceClassId</strong></span></span></td>
<td><span data-ttu-id="d7556-123">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d7556-123">Required.</span></span> <span data-ttu-id="d7556-124">Die spezifischere einzelne Bluetooth-UUID für die Dienste, für die die Suche durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d7556-124">The most specific single Bluetooth UUID for the services for which the search is being conducted.</span></span> <span data-ttu-id="d7556-125">Wenn dieser Wert beispielsweise auf die UUID des L2CAP-Protokolls festgelegt ist, werden alle Dienste zurückgegeben, die das L2CAP-Protokoll auf dem Zielgerät verwenden.</span><span class="sxs-lookup"><span data-stu-id="d7556-125">For example, if this value is set to the UUID of the L2CAP protocol, it returns all services using the L2CAP protocol on the target device.</span></span> <span data-ttu-id="d7556-126">Wenn die UUID für einen bestimmten Dienst auf festgelegt ist, werden nur die Instanzen dieses Dienstanbieter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7556-126">If set to the UUID of a specific service, it would return only the instances of that service.</span></span></td>
<td><span data-ttu-id="d7556-127">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-127">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7556-128"><strong>lpversion</strong></span><span class="sxs-lookup"><span data-stu-id="d7556-128"><strong>lpVersion</strong></span></span></td>
<td><span data-ttu-id="d7556-129">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-129">Not used.</span></span></td>
<td><span data-ttu-id="d7556-130">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-130">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7556-131"><strong>lpszcomment</strong></span><span class="sxs-lookup"><span data-stu-id="d7556-131"><strong>lpszComment</strong></span></span></td>
<td><span data-ttu-id="d7556-132">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-132">Not used.</span></span></td>
<td><span data-ttu-id="d7556-133">Die Beschreibung des Dienstes, konvertiert als UTF-8-codierte Zeichenfolge aus der Standard sprach Codierung des SDP-Attributs für Bluetooth Service Description.</span><span class="sxs-lookup"><span data-stu-id="d7556-133">Description of the service, converted as a UTF-8 encoded string from the default language encoding of the Bluetooth ServiceDescription SDP attribute.</span></span> <span data-ttu-id="d7556-134">Wird zurückgegeben, wenn <strong>LUP_RETURN_COMMENT</strong> angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d7556-134">Returned if <strong>LUP_RETURN_COMMENT</strong> is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7556-135"><strong>dwnamespace</strong></span><span class="sxs-lookup"><span data-stu-id="d7556-135"><strong>dwNameSpace</strong></span></span></td>
<td><span data-ttu-id="d7556-136">Muss NS_BTH werden.</span><span class="sxs-lookup"><span data-stu-id="d7556-136">Must be NS_BTH.</span></span></td>
<td><span data-ttu-id="d7556-137">Gibt NS_BTH zurück.</span><span class="sxs-lookup"><span data-stu-id="d7556-137">Returns NS_BTH.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7556-138"><strong>lpnsproviderid</strong></span><span class="sxs-lookup"><span data-stu-id="d7556-138"><strong>lpNSProviderId</strong></span></span></td>
<td><span data-ttu-id="d7556-139">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-139">Not used.</span></span></td>
<td><span data-ttu-id="d7556-140">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-140">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7556-141"><strong>lpszcontext</strong></span><span class="sxs-lookup"><span data-stu-id="d7556-141"><strong>lpszContext</strong></span></span></td>
<td><span data-ttu-id="d7556-142">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d7556-142">Required.</span></span> <span data-ttu-id="d7556-143">Die Bluetooth-Geräteadresse, mit der eine SDP-Verbindung hergestellt und Dienste abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="d7556-143">The Bluetooth Device Address with which to establish an SDP connection and query for services.</span></span> <span data-ttu-id="d7556-144">Dieser Wert muss eine Zeichenfolge sein, die mithilfe des <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>wsaadresssstostring</strong></a> -Funktions Aufrufes konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d7556-144">This value must be a string that was converted by using the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString</strong></a> function call.</span></span> <span data-ttu-id="d7556-145">Wenn die lokale Bluetooth-Geräteadresse angegeben wird, wird die lokale SDP-Datenbank durchsucht.</span><span class="sxs-lookup"><span data-stu-id="d7556-145">If the local Bluetooth device address is provided, the local SDP database is searched.</span></span></td>
<td><span data-ttu-id="d7556-146">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-146">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7556-147"><strong>dwnumofprotokolle</strong></span><span class="sxs-lookup"><span data-stu-id="d7556-147"><strong>dwNumberOfProtocols</strong></span></span></td>
<td><span data-ttu-id="d7556-148">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-148">Not used.</span></span></td>
<td><span data-ttu-id="d7556-149">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-149">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7556-150"><strong>lpafpprotokolle</strong></span><span class="sxs-lookup"><span data-stu-id="d7556-150"><strong>lpafpProtocols</strong></span></span></td>
<td><span data-ttu-id="d7556-151">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-151">Not used.</span></span></td>
<td><span data-ttu-id="d7556-152">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-152">Not used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7556-153"><strong>lpszquerystring</strong></span><span class="sxs-lookup"><span data-stu-id="d7556-153"><strong>lpszQueryString</strong></span></span></td>
<td><span data-ttu-id="d7556-154">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-154">Not used.</span></span></td>
<td><span data-ttu-id="d7556-155">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-155">Not used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7556-156"><strong>dwnumofcsaddrs</strong></span><span class="sxs-lookup"><span data-stu-id="d7556-156"><strong>dwNumberOfCsAddrs</strong></span></span></td>
<td><span data-ttu-id="d7556-157">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-157">Not used.</span></span></td>
<td><span data-ttu-id="d7556-158">Gibt die Anzahl der Elemente im Array von <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> Strukturen an.</span><span class="sxs-lookup"><span data-stu-id="d7556-158">Indicates the number of elements in the array of <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> structures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7556-159"><strong>lpcsabuffer</strong></span><span class="sxs-lookup"><span data-stu-id="d7556-159"><strong>lpcsaBuffer</strong></span></span></td>
<td><span data-ttu-id="d7556-160">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7556-160">Not used.</span></span></td>
<td><span data-ttu-id="d7556-161">Ein Zeiger auf eine <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> -Struktur, deren <strong>localaddr. lpsockaddr</strong> -Member auf einen <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> verweist, der die komplette Verbindungs fähigen-Adresse des Remote Dienes enthält, die aus dem ersten Eintrag des SDP-Attributs für Bluetooth protocoldescriptorlist konvertiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d7556-161">Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> structure whose <strong>LocalAddr.lpSockaddr</strong> member points to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> that contains the complete connectable address of the remote service, converted from the first entry of the Bluetooth ProtocolDescriptorList SDP attribute.</span></span> <span data-ttu-id="d7556-162">Wird zurückgegeben, wenn <strong>LUP_RETURN_ADDR</strong> angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d7556-162">Returned if <strong>LUP_RETURN_ADDR</strong> is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d7556-163"><strong>lpblob</strong></span><span class="sxs-lookup"><span data-stu-id="d7556-163"><strong>lpBlob</strong></span></span></td>
<td><span data-ttu-id="d7556-164">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d7556-164">Optional.</span></span> <span data-ttu-id="d7556-165">Ein Zeiger auf eine <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> Struktur, die erweiterte Parameter enthält, um die Suchergebnisse einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="d7556-165">Pointer to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> structure that contains advanced parameters to limit the results of the search.</span></span> <span data-ttu-id="d7556-166">Wenn angegeben, wird " <strong>lpserviceclassid</strong> " ignoriert, und zwischengespeicherte Abfragen sind nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="d7556-166">If provided, <strong>lpServiceClassId</strong> is ignored and cached queries do not succeed.</span></span></td>
<td><ul>
<li><span data-ttu-id="d7556-167">Wenn eine Dienst Suche durchgeführt wird: Zeiger auf eine <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> -Struktur, die die Dienst Handles zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d7556-167">If a service search is performed: Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure that returns the service handles.</span></span> <span data-ttu-id="d7556-168">(<strong>BLOB. cbSize</strong>)/<strong>sizeof</strong>(ULONG) berechnet die Anzahl der Handles.</span><span class="sxs-lookup"><span data-stu-id="d7556-168">(<strong>BLOB.cbSize</strong>)/<strong>sizeof</strong>(ULONG) calculates the number of handles.</span></span> <span data-ttu-id="d7556-169"><strong>BLOB. pblobdata</strong> ist ein Array von ULONG-Werten, die die Dienst Handles darstellen.</span><span class="sxs-lookup"><span data-stu-id="d7556-169"><strong>BLOB.pBlobData</strong> is an array of ULONG values representing the service handles.</span></span></li>
<li><span data-ttu-id="d7556-170">Wenn ein Attribut oder eine Service Attribute-Suche ausgeführt wird: Zeiger auf eine <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> -Struktur, die den binären SDP-Datensatz zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d7556-170">If an attribute or serviceAttribute search is performed: Pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure that returns the binary SDP record.</span></span> <span data-ttu-id="d7556-171"><strong>BLOB. cbSize</strong> ist die Größe des binären SDP-Datensatzes.</span><span class="sxs-lookup"><span data-stu-id="d7556-171"><strong>BLOB.cbSize</strong> is the size of the binary SDP record.</span></span> <span data-ttu-id="d7556-172"><strong>BLOB. pblobdata</strong> verweist auf den Datensatz selbst.</span><span class="sxs-lookup"><span data-stu-id="d7556-172"><strong>BLOB.pBlobData</strong> points to the record itself.</span></span> <span data-ttu-id="d7556-173">Der binäre SDP-Datensatz ist in vielen Fällen erforderlich, da nur eine begrenzte Anzahl von SDP-Attributen in die <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>wsaqueryset</strong></a> -Struktur konvertiert werden kann und nur standardmäßige verschlüsselte UTF-8-Zeichen folgen konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="d7556-173">The binary SDP record is necessary in many cases because only a limited number of SDP attributes are able to be converted to the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> structure, and only default encoded UTF-8 strings are converted.</span></span> <span data-ttu-id="d7556-174">Funktionen zur Unterstützung bei der Verarbeitung des binären SDP-Datensatzes finden Sie im Abschnitt zur <a href="bluetooth-reference.md">Bluetooth-Referenz</a> .</span><span class="sxs-lookup"><span data-stu-id="d7556-174">Functions to assist in parsing the binary SDP record are provided in the <a href="bluetooth-reference.md">Bluetooth Reference</a> section.</span></span></li>
<li><span data-ttu-id="d7556-175">Wird zurückgegeben, wenn LUP_RETURN_BLOB angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d7556-175">Returned if LUP_RETURN_BLOB is specified.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="d7556-176">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d7556-176">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7556-177">Bluetooth und wsaqueryset für Set Service</span><span class="sxs-lookup"><span data-stu-id="d7556-177">Bluetooth and WSAQUERYSET for Set Service</span></span>](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[<span data-ttu-id="d7556-178">Bluetooth und wsaqueryset für Geräte Anfrage</span><span class="sxs-lookup"><span data-stu-id="d7556-178">Bluetooth and WSAQUERYSET for Device Inquiry</span></span>](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="d7556-179">Bluetooth und BLOB</span><span class="sxs-lookup"><span data-stu-id="d7556-179">Bluetooth and BLOB</span></span>](bluetooth-and-blob.md)
</dt> <dt>

[<span data-ttu-id="d7556-180">Bluetooth und wsalookupservicebegin</span><span class="sxs-lookup"><span data-stu-id="d7556-180">Bluetooth and WSALookupServiceBegin</span></span>](bluetooth-and-wsasetservice.md)
</dt> <dt>

<span data-ttu-id="d7556-181">Bluetooth und WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="d7556-181">Bluetooth and WSALookupServiceNext</span></span>
</dt> <dt>

[<span data-ttu-id="d7556-182">Bluetooth-Referenz</span><span class="sxs-lookup"><span data-stu-id="d7556-182">Bluetooth Reference</span></span>](bluetooth-reference.md)
</dt> <dt>

[<span data-ttu-id="d7556-183">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="d7556-183">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="d7556-184">**BTH- \_ Abfrage \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="d7556-184">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="d7556-185">**csaddr- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="d7556-185">**CSADDR\_INFO**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[<span data-ttu-id="d7556-186">**sockaddr- \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="d7556-186">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="d7556-187">**Wsaadresssstostring**</span><span class="sxs-lookup"><span data-stu-id="d7556-187">**WSAAddressToString**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[<span data-ttu-id="d7556-188">**Wsaqueryset**</span><span class="sxs-lookup"><span data-stu-id="d7556-188">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="d7556-189">Windows-Sockets</span><span class="sxs-lookup"><span data-stu-id="d7556-189">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 