---
title: Bluetooth und wsalookupservicebegin für Geräte Anfrage
description: In diesem Thema wird beschrieben, wie Sie die wsalookupservicebegin-Funktion verwenden, um eine Abfrage von sichtbaren und Ghosting-Geräten auszuführen. Weitere Informationen finden Sie unter Ermitteln von Bluetooth-Geräten und-Diensten.
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- Bluetooth und wsalookupservicebegin für Geräte Anfrage Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfbcab2a3134289630b4b301390f85e83d1d3d0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104102474"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a><span data-ttu-id="e3627-105">Bluetooth und wsalookupservicebegin für Geräte Anfrage</span><span class="sxs-lookup"><span data-stu-id="e3627-105">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>

<span data-ttu-id="e3627-106">In diesem Thema wird beschrieben, wie Sie die [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -Funktion verwenden, um eine Abfrage von sichtbaren und Ghosting-Geräten auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e3627-106">This topic describes how to use the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function to perform an inquiry of both visible and ghosted devices.</span></span> <span data-ttu-id="e3627-107">Weitere Informationen finden Sie unter Ermitteln von [Bluetooth-Geräten und-Diensten](discovering-bluetooth-devices-and-services.md).</span><span class="sxs-lookup"><span data-stu-id="e3627-107">For more information, see [Discovering Bluetooth Devices and Services](discovering-bluetooth-devices-and-services.md).</span></span>

<span data-ttu-id="e3627-108">Die [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -Funktion verwendet eine [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur in Ihrem ersten Parameter *lpqsrestrictions*, um Suchkriterien zu definieren.</span><span class="sxs-lookup"><span data-stu-id="e3627-108">The [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function uses a [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure in its first parameter, *lpqsRestrictions*, to define search criteria.</span></span> <span data-ttu-id="e3627-109">Bluetooth bietet spezielle Richtlinien für die Verwendung der **wsalookupservicebegin** -Funktion und von **wsaqueryset**.</span><span class="sxs-lookup"><span data-stu-id="e3627-109">Bluetooth provides specific guidelines for use of the **WSALookupServiceBegin** function and **WSAQUERYSET**.</span></span>

<span data-ttu-id="e3627-110">In der folgenden Tabelle werden die Einschränkungen aufgelistet, die für die [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur gelten, die beim Abfragen von Geräten an den *lpqsrestrictions* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e3627-110">The following table lists restrictions that apply to the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure passed to the *lpqsRestrictions* parameter when querying for devices.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e3627-111">Wsaqueryset-Member</span><span class="sxs-lookup"><span data-stu-id="e3627-111">WSAQUERYSET member</span></span></th>
<th><span data-ttu-id="e3627-112">Einschränkung</span><span class="sxs-lookup"><span data-stu-id="e3627-112">Restriction</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e3627-113"><strong>dwSize</strong></span><span class="sxs-lookup"><span data-stu-id="e3627-113"><strong>dwSize</strong></span></span></td>
<td><span data-ttu-id="e3627-114">Auf <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>wsaqueryset</strong></a>) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e3627-114">Set to <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3627-115"><strong>lpblob</strong></span><span class="sxs-lookup"><span data-stu-id="e3627-115"><strong>lpBlob</strong></span></span></td>
<td><span data-ttu-id="e3627-116">Dieser Member enthält einen optionalen Zeiger auf eine <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e3627-116">This member contains an optional pointer to a <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure.</span></span> <span data-ttu-id="e3627-117">Wenn dieser Member angegeben wird, sind die gültigen Parameter für die Geräte Anfrage für <strong>LUP_FLUSHCACHE</strong> wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e3627-117">If this member is specified, the valid device inquire parameters for <strong>LUP_FLUSHCACHE</strong> are as follows:</span></span>
<ul>
<li><span data-ttu-id="e3627-118">Der <strong>CBSIZE</strong> -Member der <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> -Struktur muss <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>) sein.</span><span class="sxs-lookup"><span data-stu-id="e3627-118">The <strong>cbSize</strong> member of the <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> structure must be <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>).</span></span></li>
<li><span data-ttu-id="e3627-119">Der <strong>pblobdata</strong> -Member ist ein Zeiger auf eine <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> -Struktur, für die das <strong>Lap</strong> -Element der Bluetooth-Abfrage Zugriffs Code ist, und der <strong>Längen</strong> Member ist die Länge der Abfrage in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="e3627-119">The <strong>pBlobData</strong> member is a pointer to a <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> structure, for which the <strong>LAP</strong> member is the Bluetooth inquiry access code, and the <strong>length</strong> member is the length, in seconds, of the inquiry.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3627-120"><strong>dwnamespace</strong></span><span class="sxs-lookup"><span data-stu-id="e3627-120"><strong>dwNameSpace</strong></span></span></td>
<td><span data-ttu-id="e3627-121">Legen Sie auf <strong>NS_BTH</strong>fest.</span><span class="sxs-lookup"><span data-stu-id="e3627-121">Set to <strong>NS_BTH</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3627-122">Andere Member</span><span class="sxs-lookup"><span data-stu-id="e3627-122">Other members</span></span></td>
<td><span data-ttu-id="e3627-123">Andere <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>Member der wsaqueryset</strong></a> -Struktur werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e3627-123">Other members of the <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a> structure are ignored.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="e3627-124">Die in der folgenden Tabelle aufgeführten Flags werden im *dwcontrolflags* -Parameter verwendet, um die Abfrageergebnisse zu steuern.</span><span class="sxs-lookup"><span data-stu-id="e3627-124">The flags listed in the following table are used in the *dwControlFlags* parameter to control the query results.</span></span> <span data-ttu-id="e3627-125">Die Flags " **Lup \_ Containers** " und " **Lup \_ flushcache** " werden von der [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -Funktion verwendet. die restlichen Flags werden bei Aufrufen der [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="e3627-125">The **LUP\_CONTAINERS** and **LUP\_FLUSHCACHE** flags are used by the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function; the rest of the flags are used in calls to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span>

| <span data-ttu-id="e3627-126">Flag</span><span class="sxs-lookup"><span data-stu-id="e3627-126">Flag</span></span>               | <span data-ttu-id="e3627-127">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="e3627-127">Result</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3627-128">\_lupcontainer</span><span class="sxs-lookup"><span data-stu-id="e3627-128">LUP\_CONTAINERS</span></span>    | <span data-ttu-id="e3627-129">Gibt an, dass der Abfrage Zweck darin besteht, eine Liste von Bluetooth-Geräten und keine Liste der Dienste abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e3627-129">Specifies that the query purpose is to obtain a list of Bluetooth devices and not a list of services.</span></span> <span data-ttu-id="e3627-130">Dieses Flag muss festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e3627-130">This flag must be set.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="e3627-131">\_leeren von flushcache</span><span class="sxs-lookup"><span data-stu-id="e3627-131">LUP\_FLUSHCACHE</span></span>    | <span data-ttu-id="e3627-132">Löst eine Abfrage lokaler Geräte aus oder bewirkt, dass zwischengespeicherte Ergebnisse früherer Abfragen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e3627-132">Triggers an inquiry of local devices or causes cached results from previous queries to be returned.</span></span>                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="e3627-133">- \_ \_ Rückgabetyp</span><span class="sxs-lookup"><span data-stu-id="e3627-133">LUP\_RETURN\_TYPE</span></span>  | <span data-ttu-id="e3627-134">Gibt den Bluetooth-COD (Klasse von Device Bits) direkt im **lpserviceclassid-** Member der [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="e3627-134">Return the Bluetooth COD (class of device bits) directly in the **lpServiceClassId** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span> <span data-ttu-id="e3627-135">Der COD wird dem **data1** -Member der GUID zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="e3627-135">The COD is mapped to the **Data1** member of the GUID.</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="e3627-136">Lup \_ Res- \_ Dienst</span><span class="sxs-lookup"><span data-stu-id="e3627-136">LUP\_RES\_SERVICE</span></span>  | <span data-ttu-id="e3627-137">Gibt Informationen für die lokale Bluetooth-Adresse zurück.</span><span class="sxs-lookup"><span data-stu-id="e3627-137">Return information for the local Bluetooth address.</span></span> <span data-ttu-id="e3627-138">Dieses Flag wirkt sich nur dann aus, wenn die **\_ \_ addr-Rückgabe** Wert-Rückgabe ebenfalls angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e3627-138">This flag has an effect only if **LUP\_RETURN\_ADDR** is also specified.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="e3627-139">Name der Lup- \_ Rückgabe \_</span><span class="sxs-lookup"><span data-stu-id="e3627-139">LUP\_RETURN\_NAME</span></span>  | <span data-ttu-id="e3627-140">Gibt den anzeigen amen des Geräts im **lpszserviceinstancename** -Member der [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur für jeden Aufrufen der [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Funktion zurück.</span><span class="sxs-lookup"><span data-stu-id="e3627-140">Return the display name of the device in the **lpszServiceInstanceName** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure for each call to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span> <span data-ttu-id="e3627-141">Dieses Flag muss auch angegeben werden, um das **Name** -Element der [**BTH- \_ Geräte \_ Informations**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) Struktur abzurufen, wenn das **Lup- \_ rückgabeblobflag \_** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e3627-141">This flag must also be specified to retrieve the **name** member of the [**BTH\_DEVICE\_INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) structure when specifying the **LUP\_RETURN\_BLOB** flag.</span></span> |
| <span data-ttu-id="e3627-142">Lup \_ Return \_ addr</span><span class="sxs-lookup"><span data-stu-id="e3627-142">LUP\_RETURN\_ADDR</span></span>  | <span data-ttu-id="e3627-143">Gibt eine [**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) -Struktur zurück, die die 48-Bit-Adresse des Peers im **lpcsabuffer** -Member der [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur für jeden Aufrufe der [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="e3627-143">Return a [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure that contains the 48-bit address of the peer in the **lpcsaBuffer** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure for each call to the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function.</span></span> <span data-ttu-id="e3627-144">Andere Member in der **sockaddr- \_ BTH** -Struktur sind leer.</span><span class="sxs-lookup"><span data-stu-id="e3627-144">Other members in the **SOCKADDR\_BTH** structure will be empty.</span></span>                                                            |
| <span data-ttu-id="e3627-145">Lup- \_ Rückgabe- \_ BLOB</span><span class="sxs-lookup"><span data-stu-id="e3627-145">LUP\_RETURN\_BLOB</span></span>  | <span data-ttu-id="e3627-146">Zurückgeben der [**BTH- \_ Geräte \_ Informations**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) Struktur bei jedem nachfolgenden [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="e3627-146">Return the [**BTH\_DEVICE\_INFO**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) structure on each subsequent call to [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="e3627-147">Lup- \_ flushprevious</span><span class="sxs-lookup"><span data-stu-id="e3627-147">LUP\_FLUSHPREVIOUS</span></span> | <span data-ttu-id="e3627-148">Überspringen Sie das nächste verfügbare Gerät, und geben Sie das Gerät an, das darauf folgt.</span><span class="sxs-lookup"><span data-stu-id="e3627-148">Skip the next available device, and return the device that follows it.</span></span>                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="e3627-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e3627-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3627-150">Bluetooth und wsalookupservicebegin für die Dienst Ermittlung</span><span class="sxs-lookup"><span data-stu-id="e3627-150">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="e3627-151">Bluetooth und WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="e3627-151">Bluetooth and WSALookupServiceNext</span></span>](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="e3627-152">Bluetooth und wsaqueryset für Geräte Anfrage</span><span class="sxs-lookup"><span data-stu-id="e3627-152">Bluetooth and WSAQUERYSET for Device Inquiry</span></span>](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="e3627-153">Ermitteln von Bluetooth-Geräten und -Diensten</span><span class="sxs-lookup"><span data-stu-id="e3627-153">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="e3627-154">**Wsalookupservicebegin**</span><span class="sxs-lookup"><span data-stu-id="e3627-154">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="e3627-155">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="e3627-155">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="e3627-156">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="e3627-156">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="e3627-157">**BLOB**</span><span class="sxs-lookup"><span data-stu-id="e3627-157">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="e3627-158">**BTH- \_ Abfrage \_ Gerät**</span><span class="sxs-lookup"><span data-stu-id="e3627-158">**BTH\_QUERY\_DEVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[<span data-ttu-id="e3627-159">**sockaddr- \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="e3627-159">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="e3627-160">**Wsaqueryset**</span><span class="sxs-lookup"><span data-stu-id="e3627-160">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="e3627-161">Windows-Sockets</span><span class="sxs-lookup"><span data-stu-id="e3627-161">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 