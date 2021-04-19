---
description: PNRP verwendet die WSALookupServiceNext-Funktion, um Abfragen abzugleichen, die in einem vorherigen wsalookupservicebegin-Befehl angegeben wurden.
ms.assetid: b3e1abf4-ff59-481d-b96e-f8916a47cd52
title: PNRP und WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398beca2f16e4920ab7fbe43bb648cbc22d9f336
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106367944"
---
# <a name="pnrp-and-wsalookupservicenext"></a><span data-ttu-id="10ed6-103">PNRP und WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="10ed6-103">PNRP and WSALookupServiceNext</span></span>

<span data-ttu-id="10ed6-104">PNRP verwendet die [**WSALookupServiceNext**](winsock-nsp-reference-links.md) -Funktion, um Abfragen abzugleichen, die in einem vorherigen **wsalookupservicebegin**-Befehl angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="10ed6-104">PNRP uses the [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function to match queries specified in a previous call to **WSALookupServiceBegin**.</span></span> <span data-ttu-id="10ed6-105">Die Ergebnisse der **WSALookupServiceNext** -Funktion werden durch Einstellungen in der **wsaqueryset** -Struktur festgelegt, die im anfänglichen **wsalookupservicebegin** -Funktions aufruft übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="10ed6-105">The results of the **WSALookupServiceNext** function are determined by settings in the **WSAQUERYSET** structure passed in the initial **WSALookupServiceBegin** function call.</span></span> <span data-ttu-id="10ed6-106">Diese Funktion wird verwendet, um die folgenden zwei Funktionen auszuführen:</span><span class="sxs-lookup"><span data-stu-id="10ed6-106">This function is used to perform the following two functions:</span></span>

-   <span data-ttu-id="10ed6-107">Auflösen eines Peer namens in eine Liste von Adressen</span><span class="sxs-lookup"><span data-stu-id="10ed6-107">Resolving a peer name to a list of addresses</span></span>
-   <span data-ttu-id="10ed6-108">Auflisten von Netzwerk Clouds</span><span class="sxs-lookup"><span data-stu-id="10ed6-108">Enumerating network clouds</span></span>

<span data-ttu-id="10ed6-109">Mithilfe von [**wsanspioctl**](winsock-nsp-reference-links.md)kann der Suchdienst asynchron verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10ed6-109">By using [**WSANSPIoctl**](winsock-nsp-reference-links.md), the lookup service can be used asynchronously.</span></span> <span data-ttu-id="10ed6-110">Weitere Informationen zur asynchronen Verwendung der Suche-Dienstfunktionen finden Sie unter [PNRP und wsanspioctl](pnrp-and-wsanspioctl.md).</span><span class="sxs-lookup"><span data-stu-id="10ed6-110">For information about using the lookup service functions asynchronously, see [PNRP and WSANSPIoctl](pnrp-and-wsanspioctl.md).</span></span>

<span data-ttu-id="10ed6-111">Die [**WSALookupServiceNext**](winsock-nsp-reference-links.md) -Funktion wird blockiert, auch wenn **wsanspioctl** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="10ed6-111">The [**WSALookupServiceNext**](winsock-nsp-reference-links.md) function blocks even if **WSANSPIoctl** is called.</span></span> <span data-ttu-id="10ed6-112">Vor dem Aufrufen von **WSALookupServiceNext** muss eine Anwendung warten, bis Sie eine Benachrichtigung erhält – Wenn die Blockierung ein Problem ist.</span><span class="sxs-lookup"><span data-stu-id="10ed6-112">Before calling **WSALookupServiceNext**, an application must wait until it receives a notification—if blocking is an issue.</span></span>

## <a name="resolving-a-peer-name-to-a-list-of-addresses"></a><span data-ttu-id="10ed6-113">Auflösen eines Peer namens in eine Liste von Adressen</span><span class="sxs-lookup"><span data-stu-id="10ed6-113">Resolving a Peer Name to a List of Addresses</span></span>

<span data-ttu-id="10ed6-114">Beim Auflösen eines Peer namens in eine Liste von Adressen enthält die im *lpqsresults* -Parameter zurückgegebene [**lpwsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="10ed6-114">When resolving a peer name to a list of addresses, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure returned in the *lpqsResults* parameter contains the following values:</span></span>

<dl> <dt>

<span data-ttu-id="10ed6-115"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="10ed6-115"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-116">Gibt die Größe der-Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-116">Returns the size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-117"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszserviceingestancename**</span><span class="sxs-lookup"><span data-stu-id="10ed6-117"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-118">Gibt einen Peernamen zurück – wenn ein **luprückgabetame \_ \_**, eine **Lup \_ Return \_ all** oder **null** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="10ed6-118">Returns a peer name—if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-119"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpserviceclassid**</span><span class="sxs-lookup"><span data-stu-id="10ed6-119"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-120">Gibt **svcid \_ pnrpname** zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-120">Returns **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-121"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpversion**</span><span class="sxs-lookup"><span data-stu-id="10ed6-121"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-122">Gibt **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-122">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-123"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszcomment**</span><span class="sxs-lookup"><span data-stu-id="10ed6-123"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-124">Gibt einen Kommentar zurück – wenn ein **luprückgabetcomment \_ \_**, eine **Lup \_ Return \_ all** oder **null** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="10ed6-124">Returns a comment—if **LUP\_RETURN\_COMMENT**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-125"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwnamespace**</span><span class="sxs-lookup"><span data-stu-id="10ed6-125"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-126">Gibt **NS \_ pnrpname** zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-126">Returns **NS\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-127"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpnsproviderid**</span><span class="sxs-lookup"><span data-stu-id="10ed6-127"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-128">Gibt den **NS- \_ Anbieter \_ pnrpname** zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-128">Returns **NS\_PROVIDER\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-129"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszcontext**</span><span class="sxs-lookup"><span data-stu-id="10ed6-129"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-130">Gibt den cloudnamen zurück, wenn der **\_ Rückgabe \_ Name** des PPS, die **Lup- \_ Rückgabe \_ all** oder **null** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="10ed6-130">Returns the cloud name if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-131"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwnumofprotokolle**</span><span class="sxs-lookup"><span data-stu-id="10ed6-131"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-132">Gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-132">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-133"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszquerystring**</span><span class="sxs-lookup"><span data-stu-id="10ed6-133"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-134">Gibt **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-134">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-135"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwnumofcsaddrs**</span><span class="sxs-lookup"><span data-stu-id="10ed6-135"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-136">Gibt die Anzahl der Einträge im csaddr- \_ Informations Array zurück, wenn " **Lup \_ Return \_ addr**", " **Lup \_ Return \_ all**" oder " **null** " angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="10ed6-136">Returns the number of entries in the CSADDR\_INFO array if **LUP\_RETURN\_ADDR**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span> <span data-ttu-id="10ed6-137">Dieser Wert und die Informationen in **lpcsabuffer** sind die Schlüssel Bits der Informationen, die in dieser Struktur zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="10ed6-137">This value and the information in **lpcsaBuffer** are the key bits of information returned in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-138"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsabuffer**</span><span class="sxs-lookup"><span data-stu-id="10ed6-138"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-139">Gibt einen Zeiger auf ein Array von csaddr- \_ Informationsstrukturen zurück, wenn " **Lup \_ Return \_ addr**", " **Lup \_ Return \_ all**" oder " **null** " angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="10ed6-139">Returns a pointer to an array of CSADDR\_INFO structures if **LUP\_RETURN\_ADDR**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span> <span data-ttu-id="10ed6-140">Dieser Puffer und der Wert in **dwnumofcsaddrs** sind die wichtigsten Informations Bits, die in dieser Struktur zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="10ed6-140">This buffer and the value in **dwNumberOfCsAddrs** are the key information bits returned in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-141"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwoutputflags**</span><span class="sxs-lookup"><span data-stu-id="10ed6-141"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-142">Gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-142">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-143"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpblob**</span><span class="sxs-lookup"><span data-stu-id="10ed6-143"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-144">Gibt **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-144">Returns **NULL**.</span></span>

</dd> </dl>

## <a name="enumerating-network-clouds"></a><span data-ttu-id="10ed6-145">Auflisten von Netzwerk Clouds</span><span class="sxs-lookup"><span data-stu-id="10ed6-145">Enumerating Network Clouds</span></span>

<span data-ttu-id="10ed6-146">Beim Auflisten von Clouds enthält die im *lpqsresults* -Parameter zurückgegebene [**lpwsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="10ed6-146">When enumerating clouds, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure returned in the *lpqsResults* parameter contains the following values:</span></span>

<dl> <dt>

<span data-ttu-id="10ed6-147"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="10ed6-147"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-148">Gibt die Größe der-Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-148">Returns the size of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-149"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszserviceingestancename**</span><span class="sxs-lookup"><span data-stu-id="10ed6-149"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-150">Gibt einen cloudnamen zurück – wenn der **\_ Rückgabe \_ Name** des PPS, die **Lup- \_ Rückgabe \_ all** oder **null** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="10ed6-150">Returns a cloud name—if **LUP\_RETURN\_NAME**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-151"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpserviceclassid**</span><span class="sxs-lookup"><span data-stu-id="10ed6-151"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-152">Gibt **svcid \_ pnrpcloud** zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-152">Returns **SVCID\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-153"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpversion**</span><span class="sxs-lookup"><span data-stu-id="10ed6-153"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-154">Gibt **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-154">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-155"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszcomment**</span><span class="sxs-lookup"><span data-stu-id="10ed6-155"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-156">Gibt **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-156">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-157"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwnamespace**</span><span class="sxs-lookup"><span data-stu-id="10ed6-157"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-158">Gibt **NS \_ pnrpcloud** zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-158">Returns **NS\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-159"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpnsproviderid**</span><span class="sxs-lookup"><span data-stu-id="10ed6-159"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-160">Gibt den **NS- \_ Anbieter \_ pnrpcloud** zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-160">Returns **NS\_PROVIDER\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-161"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszcontext**</span><span class="sxs-lookup"><span data-stu-id="10ed6-161"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-162">Gibt **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-162">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-163"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwnumofprotokolle**</span><span class="sxs-lookup"><span data-stu-id="10ed6-163"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-164">Gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-164">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-165"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszquerystring**</span><span class="sxs-lookup"><span data-stu-id="10ed6-165"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-166">Gibt **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-166">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-167"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwnumofcsaddrs**</span><span class="sxs-lookup"><span data-stu-id="10ed6-167"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-168">Gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-168">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-169"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsabuffer**</span><span class="sxs-lookup"><span data-stu-id="10ed6-169"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-170">Gibt **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-170">Returns **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-171"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwoutputflags**</span><span class="sxs-lookup"><span data-stu-id="10ed6-171"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-172">Gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="10ed6-172">Returns zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-173"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpblob**</span><span class="sxs-lookup"><span data-stu-id="10ed6-173"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-174">Gibt einen Zeiger auf eine [**BLOB**](winsock-nsp-reference-links.md) -Struktur zurück, die auf eine [**pnrpcloudinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) -Struktur zeigt – Wenn ein **luprückgabeblob \_ \_**, eine **Lup \_ Return \_ all** oder **null** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="10ed6-174">Returns a pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure—if **LUP\_RETURN\_BLOB**, **LUP\_RETURN\_ALL**, or **NULL** are specified.</span></span>

</dd> </dl>

## <a name="pnrpcloudinfo-structure"></a><span data-ttu-id="10ed6-175">Pnrpcloudinfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="10ed6-175">PNRPCLOUDINFO Structure</span></span>

<span data-ttu-id="10ed6-176">Beim Auflisten von cloudnamen werden die folgenden Werte in der [**pnrpcloudinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) -Struktur zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="10ed6-176">When enumerating cloud names, the following values are returned in the [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure:</span></span>

<dl> <dt>

<span data-ttu-id="10ed6-177"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="10ed6-177"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-178">Die Größe dieser Struktur.</span><span class="sxs-lookup"><span data-stu-id="10ed6-178">The size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-179"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span><span class="sxs-lookup"><span data-stu-id="10ed6-179"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-180">Der tatsächliche cloudwert.</span><span class="sxs-lookup"><span data-stu-id="10ed6-180">The actual cloud value.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-181"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**umcloudstate**</span><span class="sxs-lookup"><span data-stu-id="10ed6-181"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-182">Der aktuelle Zustand einer Cloud.</span><span class="sxs-lookup"><span data-stu-id="10ed6-182">The current state of a cloud.</span></span> <span data-ttu-id="10ed6-183">[**PNRP \_ Der \_ cloudstatus**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) gibt die gültigen Werte an.</span><span class="sxs-lookup"><span data-stu-id="10ed6-183">[**PNRP\_CLOUD\_STATE**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_state) specifies the valid values.</span></span>

</dd> <dt>

<span data-ttu-id="10ed6-184"><span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**encloudflags**</span><span class="sxs-lookup"><span data-stu-id="10ed6-184"><span id="enCloudFlags"></span><span id="encloudflags"></span><span id="ENCLOUDFLAGS"></span>**enCloudFlags**</span></span>
</dt> <dd>

<span data-ttu-id="10ed6-185">Gibt an, dass ein cloudName in einem Netzwerk oder nur auf einem aktuellen Computer gültig ist.</span><span class="sxs-lookup"><span data-stu-id="10ed6-185">Indicates that a cloud name is valid on a network, or only valid on a current computer.</span></span> <span data-ttu-id="10ed6-186">[**PNRP \_ Cloud- \_ Flags**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) gibt die gültigen Werte an.</span><span class="sxs-lookup"><span data-stu-id="10ed6-186">[**PNRP\_CLOUD\_FLAGS**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_cloud_flags) specifies the valid values.</span></span> <span data-ttu-id="10ed6-187">Einige cloudnamen sind auf einem beliebigen Computer im selben Netzwerk gültig.</span><span class="sxs-lookup"><span data-stu-id="10ed6-187">Some cloud names are valid on any computer on the same network.</span></span> <span data-ttu-id="10ed6-188">Andere cloudnamen gelten nur auf einem aktuellen Computer und sind möglicherweise nur für einen bestimmten Zeitraum gültig.</span><span class="sxs-lookup"><span data-stu-id="10ed6-188">Other cloud names are valid only on a current computer, and may be valid only for a period of time.</span></span>

-   <span data-ttu-id="10ed6-189">Wenn " **encloudflags** " auf " **PNRP \_ Cloud \_ Name \_ local** " festgelegt ist, ist der Name nur lokal gültig.</span><span class="sxs-lookup"><span data-stu-id="10ed6-189">If **enCloudFlags** is set to **PNRP\_CLOUD\_NAME\_LOCAL,** the name is only valid locally.</span></span>
-   <span data-ttu-id="10ed6-190">Wenn **encloudflags** nicht festgelegt ist, kann der cloudName an andere Computer übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="10ed6-190">If **enCloudFlags** is not set, then the cloud name can be transferred to other computers.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="10ed6-191">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="10ed6-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10ed6-192">PNRP und BLOB</span><span class="sxs-lookup"><span data-stu-id="10ed6-192">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="10ed6-193">PNRP und WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="10ed6-193">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="10ed6-194">PNRP und wsanspioctl</span><span class="sxs-lookup"><span data-stu-id="10ed6-194">PNRP and WSANSPIoctl</span></span>](pnrp-and-wsanspioctl.md)
</dt> <dt>

[<span data-ttu-id="10ed6-195">PNRP und wsaqueryset</span><span class="sxs-lookup"><span data-stu-id="10ed6-195">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="10ed6-196">**Pnrpcloudinfo**</span><span class="sxs-lookup"><span data-stu-id="10ed6-196">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[<span data-ttu-id="10ed6-197">**Pnrpinfo**</span><span class="sxs-lookup"><span data-stu-id="10ed6-197">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="10ed6-198">PNRP-NSP-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="10ed6-198">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="10ed6-199">**Wsalookupservicebegin**</span><span class="sxs-lookup"><span data-stu-id="10ed6-199">**WSALookupServiceBegin**</span></span>](winsock-nsp-reference-links.md)
</dt> </dl>

 

 



