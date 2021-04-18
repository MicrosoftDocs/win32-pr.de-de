---
description: PNRP verwendet die wsalookupservicebegin-Funktion, um den Prozess zu starten, mit dem eine Anwendung folgende Aktionen ausführen kann.
ms.assetid: 71cca892-89e7-44d1-920d-987587eeed50
title: PNRP und wsalookupservicebegin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78efd0ee28284cb41866795aea8a2a8d5f17e871
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "106354344"
---
# <a name="pnrp-and-wsalookupservicebegin"></a><span data-ttu-id="c917e-103">PNRP und wsalookupservicebegin</span><span class="sxs-lookup"><span data-stu-id="c917e-103">PNRP and WSALookupServiceBegin</span></span>

<span data-ttu-id="c917e-104">PNRP verwendet die [**wsalookupservicebegin**](winsock-nsp-reference-links.md) -Funktion, um den Prozess zu starten, mit dem eine Anwendung folgende Aktionen ausführen kann:</span><span class="sxs-lookup"><span data-stu-id="c917e-104">PNRP uses the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) function to start the process that allows an application to do the following:</span></span>

-   [<span data-ttu-id="c917e-105">Auflösen eines Namens</span><span class="sxs-lookup"><span data-stu-id="c917e-105">Resolving a name</span></span>](#resolving-a-name)
-   [<span data-ttu-id="c917e-106">Auflisten von Netzwerk Clouds</span><span class="sxs-lookup"><span data-stu-id="c917e-106">Enumerating network clouds</span></span>](#enumerating-network-clouds)

<span data-ttu-id="c917e-107">Clients, die versuchen, eine der Funktionen auszuführen, verwenden die Funktionen [**wsalookupservicebegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext** und **WSALookupServiceEnd** .</span><span class="sxs-lookup"><span data-stu-id="c917e-107">Clients that attempt to perform one of the functions use the [**WSALookupServiceBegin**](winsock-nsp-reference-links.md), **WSALookupServiceNext**, and **WSALookupServiceEnd** functions.</span></span>

<span data-ttu-id="c917e-108">Mithilfe von [**wsanspioctl**](winsock-nsp-reference-links.md)kann der Suchdienst asynchron verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c917e-108">By using [**WSANSPIoctl**](winsock-nsp-reference-links.md), the lookup service can be used asynchronously.</span></span> <span data-ttu-id="c917e-109">Weitere Informationen zur asynchronen Verwendung der Suche-Dienstfunktionen finden Sie unter [PNRP und wsanspioctl](pnrp-and-wsanspioctl.md).</span><span class="sxs-lookup"><span data-stu-id="c917e-109">For information about using the lookup service functions asynchronously, see [PNRP and WSANSPIoctl](pnrp-and-wsanspioctl.md).</span></span>

<span data-ttu-id="c917e-110">Der Prozess zum Arbeiten mit Peernamen unterscheidet sich von der Arbeit mit Clouds.</span><span class="sxs-lookup"><span data-stu-id="c917e-110">The process for working with peer names is different from working with clouds.</span></span> <span data-ttu-id="c917e-111">Jeder Prozess wird in diesem Thema separat beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c917e-111">Each process is described separately in this topic.</span></span>

## <a name="resolving-a-name"></a><span data-ttu-id="c917e-112">Auflösen eines Namens</span><span class="sxs-lookup"><span data-stu-id="c917e-112">Resolving a Name</span></span>

<span data-ttu-id="c917e-113">Die IP-Adresse, der Port und das Protokoll für einen Peer Dienst, der auf einem anderen Computer registriert ist, werden von einer Anwendung mithilfe von [**wsalookupservicebegin**](winsock-nsp-reference-links.md) abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c917e-113">An application uses [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) to obtain the IP address, port, and protocol for a peer service that is registered on another computer.</span></span> <span data-ttu-id="c917e-114">Die **wsalookupservicebegin** -Funktion wird verwendet, um den namens Auflösungsprozess zu starten und die Parameter und Einschränkungen einzurichten.</span><span class="sxs-lookup"><span data-stu-id="c917e-114">The **WSALookupServiceBegin** function is used to start the name resolution process, and set up the parameters and restrictions.</span></span> <span data-ttu-id="c917e-115">Ein Handle wird zurückgegeben und muss beim Aufrufen von **WSALookupServiceNext** und **wsanspioctl** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c917e-115">A handle is returned, and must be used when calling **WSALookupServiceNext** and **WSANSPIoctl**.</span></span>

### <a name="lpqsrestrictions"></a><span data-ttu-id="c917e-116">lpqsrestrictions</span><span class="sxs-lookup"><span data-stu-id="c917e-116">lpqsRestrictions</span></span>

<span data-ttu-id="c917e-117">Beim Auflösen eines Peer namens muss die [**lpwsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur, auf die der *lpqsrestrictions* -Parameter verweist, die folgenden Werte enthalten:</span><span class="sxs-lookup"><span data-stu-id="c917e-117">When resolving a peer name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRestrictions* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c917e-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="c917e-118"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-119">Gibt die Größe der-Struktur an.</span><span class="sxs-lookup"><span data-stu-id="c917e-119">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-120"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszserviceingestancename**</span><span class="sxs-lookup"><span data-stu-id="c917e-120"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-121">Gibt einen aufzulösenden Peernamen an.</span><span class="sxs-lookup"><span data-stu-id="c917e-121">Specifies a peer name to resolve.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-122"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpserviceclassid**</span><span class="sxs-lookup"><span data-stu-id="c917e-122"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-123">Muss " **svcid \_ pnrpname**" lauten.</span><span class="sxs-lookup"><span data-stu-id="c917e-123">Must be **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-124"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpversion**</span><span class="sxs-lookup"><span data-stu-id="c917e-124"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-125">Reserviert, muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-125">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-126"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszcomment**</span><span class="sxs-lookup"><span data-stu-id="c917e-126"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-127">Reserviert, muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-127">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-128"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwnamespace**</span><span class="sxs-lookup"><span data-stu-id="c917e-128"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-129">Muss entweder ' **NS \_ ' pnrpname** ' oder ' **NS \_ all**' sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-129">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-130"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpnsproviderid**</span><span class="sxs-lookup"><span data-stu-id="c917e-130"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-131">Muss entweder der **NS- \_ Anbieter \_ pnrpname** oder **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-131">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-132"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszcontext**</span><span class="sxs-lookup"><span data-stu-id="c917e-132"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-133">Muss ein cloudName, eine leere Zeichenfolge oder **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-133">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="c917e-134">Wenn dieser Wert **null** oder eine leere Zeichenfolge ist, wird die Standard-Cloud "Global \_ " verwendet.</span><span class="sxs-lookup"><span data-stu-id="c917e-134">If this value is **NULL** or an empty string, the default cloud, "Global\_" is used.</span></span> <span data-ttu-id="c917e-135">Andernfalls muss Sie auf einen gültigen cloudnamen verweisen.</span><span class="sxs-lookup"><span data-stu-id="c917e-135">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-136"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwnumofprotokolle**</span><span class="sxs-lookup"><span data-stu-id="c917e-136"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-137">Reserviert, muss NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-137">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="c917e-138"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszquerystring**</span><span class="sxs-lookup"><span data-stu-id="c917e-138"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-139">Reserviert, muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-139">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-140"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwnumofcsaddrs**</span><span class="sxs-lookup"><span data-stu-id="c917e-140"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-141">Reserviert, muss NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-141">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="c917e-142"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsabuffer**</span><span class="sxs-lookup"><span data-stu-id="c917e-142"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-143">Reserviert, muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-143">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-144"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwoutputflags**</span><span class="sxs-lookup"><span data-stu-id="c917e-144"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-145">Reserviert, muss NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-145">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="c917e-146"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpblob**</span><span class="sxs-lookup"><span data-stu-id="c917e-146"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-147">Muss entweder ein Zeiger auf eine [**BLOB**](winsock-nsp-reference-links.md) -Struktur oder **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-147">Must be either a pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure or **NULL**.</span></span> <span data-ttu-id="c917e-148">Wenn er **null** ist, werden Standardwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="c917e-148">If it is **NULL**, default values are used.</span></span> <span data-ttu-id="c917e-149">Wenn Sie festgelegt ist, verweist **lpblob** auf eine [**pnrpinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) -Struktur, und bestimmte Parameter in der **pnrpinfo** -Struktur müssen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c917e-149">If it is set, **lpBlob** points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure, and specific parameters in the **PNRPINFO** structure must be set.</span></span> <span data-ttu-id="c917e-150">Weitere Informationen finden Sie in den folgenden Beschreibungen der pnrpinfo-Struktur.</span><span class="sxs-lookup"><span data-stu-id="c917e-150">For more information, see the following descriptions for the PNRPINFO Structure.</span></span>

</dd> </dl>

<span data-ttu-id="c917e-151">Pnrpinfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="c917e-151">PNRPINFO Structure</span></span>

<span data-ttu-id="c917e-152">Wenn das **lpblob** -Element der [**lpwsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur festgelegt ist, müssen die folgenden Member der [**pnrpinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) -Struktur festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c917e-152">If the **lpBlob** member of the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure is set, the following members of the [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="c917e-153"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="c917e-153"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-154">Gibt die Größe der-Struktur an.</span><span class="sxs-lookup"><span data-stu-id="c917e-154">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-155"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszidentity**</span><span class="sxs-lookup"><span data-stu-id="c917e-155"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-156">Reserviert, muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-156">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-157"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nmaxresolve**</span><span class="sxs-lookup"><span data-stu-id="c917e-157"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-158">Gibt die angeforderte Anzahl von Auflösungen an.</span><span class="sxs-lookup"><span data-stu-id="c917e-158">Specifies the requested number of resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-159"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwtimeout**</span><span class="sxs-lookup"><span data-stu-id="c917e-159"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-160">Gibt den angeforderten Timeout Zeitraum an, der auf Antworten gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c917e-160">Specifies the requested timeout period to wait for responses.</span></span> <span data-ttu-id="c917e-161">Der Standardwert ist 30 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="c917e-161">The default is 30 seconds.</span></span> <span data-ttu-id="c917e-162">Der Höchstwert beträgt 600 Sekunden (10 Minuten).</span><span class="sxs-lookup"><span data-stu-id="c917e-162">The maximum is 600 seconds (10 minutes).</span></span>

</dd> <dt>

<span data-ttu-id="c917e-163"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwlifetime**</span><span class="sxs-lookup"><span data-stu-id="c917e-163"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-164">Reserviert, muss NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-164">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="c917e-165"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**einlösungs Vektor**</span><span class="sxs-lookup"><span data-stu-id="c917e-165"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-166">Muss einer der zulässigen Werte sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-166">Must be one of the allowed values.</span></span> <span data-ttu-id="c917e-167">Der Standardwert ist **PNRP \_ Auflösungs \_ Kriterien \_ nicht \_ aktueller \_ Prozess \_ Peer \_ Name**.</span><span class="sxs-lookup"><span data-stu-id="c917e-167">The default is **PNRP\_RESOLVE\_CRITERIA\_NON\_CURRENT\_PROCESS\_PEER\_NAME**.</span></span> <span data-ttu-id="c917e-168">Gültige Werte werden von [**PNRP- \_ Auflösungs \_ Kriterien**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria)angegeben.</span><span class="sxs-lookup"><span data-stu-id="c917e-168">Valid values are specified by [**PNRP\_RESOLVE\_CRITERIA**](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria).</span></span>

</dd> <dt>

<span data-ttu-id="c917e-169"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="c917e-169"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-170">Muss entweder NULL (0) oder **pnrpinfo- \_ Hinweis** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-170">Must be either zero (0) or **PNRPINFO\_HINT**.</span></span> <span data-ttu-id="c917e-171">Der Standardwert ist null (0).</span><span class="sxs-lookup"><span data-stu-id="c917e-171">The default is zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="c917e-172"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**sahint**</span><span class="sxs-lookup"><span data-stu-id="c917e-172"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-173">Gibt die IP-Adresse für den Hinweis an.</span><span class="sxs-lookup"><span data-stu-id="c917e-173">Specifies the IP address for the hint.</span></span> <span data-ttu-id="c917e-174">Der Hinweis wird verwendet, wenn versucht wird, den nächsten Peernamen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="c917e-174">The hint is used when attempting to find the nearest peer name.</span></span> <span data-ttu-id="c917e-175">Das Format des Hinweises ist eine IPv6-Adresse.</span><span class="sxs-lookup"><span data-stu-id="c917e-175">The format of the hint is an IPv6 address.</span></span> <span data-ttu-id="c917e-176">Wenn bei der Suche nach dem nächstgelegenen Peernamen **sahint** nicht angegeben wird, wird stattdessen eine IPv6-Adresse des lokalen Computers verwendet.</span><span class="sxs-lookup"><span data-stu-id="c917e-176">If **saHint** is not specified when finding the closest peer name, then an IPv6 address of the local computer is used instead.</span></span> <span data-ttu-id="c917e-177">Dieser Member wird ignoriert, wenn **dwFlags** nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c917e-177">This member is ignored if **dwFlags** is not set.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-178"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**ennamestate**</span><span class="sxs-lookup"><span data-stu-id="c917e-178"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-179">Reserviert, muss NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-179">Reserved, must be zero (0).</span></span>

</dd> </dl>

### <a name="dwcontrolflags"></a><span data-ttu-id="c917e-180">dwcontrolflags</span><span class="sxs-lookup"><span data-stu-id="c917e-180">dwControlFlags</span></span>

<span data-ttu-id="c917e-181">Die folgenden Lup \_ - \_ \* rückgabeflags werden von PNRP unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c917e-181">The following LUP\_RETURN\_\* flags are supported by PNRP:</span></span>



| <span data-ttu-id="c917e-182">Wert</span><span class="sxs-lookup"><span data-stu-id="c917e-182">Value</span></span>                | <span data-ttu-id="c917e-183">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c917e-183">Description</span></span>                                |
|----------------------|--------------------------------------------|
| <span data-ttu-id="c917e-184">Name der Lup- \_ Rückgabe \_</span><span class="sxs-lookup"><span data-stu-id="c917e-184">LUP\_RETURN\_NAME</span></span>    | <span data-ttu-id="c917e-185">Gibt einen Namen und einen Kontext zurück.</span><span class="sxs-lookup"><span data-stu-id="c917e-185">Returns a name and context.</span></span>                |
| <span data-ttu-id="c917e-186">Lup- \_ Rückgabe \_ Kommentar</span><span class="sxs-lookup"><span data-stu-id="c917e-186">LUP\_RETURN\_COMMENT</span></span> | <span data-ttu-id="c917e-187">Gibt einen Kommentar zurück, der einem Namen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c917e-187">Returns a comment associated with a name.</span></span>  |
| <span data-ttu-id="c917e-188">Lup \_ Return \_ addr</span><span class="sxs-lookup"><span data-stu-id="c917e-188">LUP\_RETURN\_ADDR</span></span>    | <span data-ttu-id="c917e-189">Gibt eine Adresse zurück, die einem Namen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c917e-189">Returns an address associated with a name.</span></span> |



 

## <a name="enumerating-network-clouds"></a><span data-ttu-id="c917e-190">Auflisten von Netzwerk Clouds</span><span class="sxs-lookup"><span data-stu-id="c917e-190">Enumerating Network Clouds</span></span>

### <a name="lpqsrestrictions"></a><span data-ttu-id="c917e-191">lpqsrestrictions</span><span class="sxs-lookup"><span data-stu-id="c917e-191">lpqsRestrictions</span></span>

<span data-ttu-id="c917e-192">Beim Auflisten von Clouds muss die [**lpwsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur, auf die der *lpqsrestrictions* -Parameter verweist, die folgenden Werte enthalten:</span><span class="sxs-lookup"><span data-stu-id="c917e-192">When enumerating clouds, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRestrictions* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="c917e-193"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="c917e-193"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-194">Gibt die Größe der-Struktur an.</span><span class="sxs-lookup"><span data-stu-id="c917e-194">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-195"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszserviceingestancename**</span><span class="sxs-lookup"><span data-stu-id="c917e-195"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-196">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-196">Must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-197"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpserviceclassid**</span><span class="sxs-lookup"><span data-stu-id="c917e-197"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-198">Muss **svcid \_ pnrpcloud** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-198">Must be **SVCID\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-199"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpversion**</span><span class="sxs-lookup"><span data-stu-id="c917e-199"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-200">Reserviert, muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-200">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-201"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszcomment**</span><span class="sxs-lookup"><span data-stu-id="c917e-201"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-202">Reserviert, muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-202">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-203"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwnamespace**</span><span class="sxs-lookup"><span data-stu-id="c917e-203"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-204">Muss **NS \_ pnrpcloud** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-204">Must be **NS\_PNRPCLOUD**.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-205"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpnsproviderid**</span><span class="sxs-lookup"><span data-stu-id="c917e-205"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-206">Muss entweder der **NS- \_ Anbieter \_ pnrpcloud** oder **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-206">Must be either **NS\_PROVIDER\_PNRPCLOUD** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-207"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszcontext**</span><span class="sxs-lookup"><span data-stu-id="c917e-207"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-208">Reserviert, muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-208">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-209"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwnumofprotokolle**</span><span class="sxs-lookup"><span data-stu-id="c917e-209"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-210">Reserviert, muss NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-210">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="c917e-211"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszquerystring**</span><span class="sxs-lookup"><span data-stu-id="c917e-211"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-212">Reserviert, muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-212">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-213"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwnumofcsaddrs**</span><span class="sxs-lookup"><span data-stu-id="c917e-213"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-214">Reserviert, muss NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-214">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="c917e-215"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsabuffer**</span><span class="sxs-lookup"><span data-stu-id="c917e-215"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-216">Reserviert, muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-216">Reserved, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-217"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwoutputflags**</span><span class="sxs-lookup"><span data-stu-id="c917e-217"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-218">Reserviert, muss NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-218">Reserved, must be zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="c917e-219"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpblob**</span><span class="sxs-lookup"><span data-stu-id="c917e-219"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-220">Zeiger auf eine [**BLOB**](winsock-nsp-reference-links.md) -Struktur, die auf eine [**pnrpcloudinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) -Struktur zeigt.</span><span class="sxs-lookup"><span data-stu-id="c917e-220">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure.</span></span> <span data-ttu-id="c917e-221">Wenn **lpblob** den Wert **null** hat, werden alle Clouds aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c917e-221">If **lpBlob** is **NULL**, all clouds are enumerated.</span></span>

</dd> </dl>

<span data-ttu-id="c917e-222">Pnrpcloudinfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="c917e-222">PNRPCLOUDINFO Structure</span></span>

<span data-ttu-id="c917e-223">Beim Auflisten von Clouds müssen die folgenden Member der [**pnrpcloudinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) -Struktur festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c917e-223">When enumerating clouds, the following members of the [**PNRPCLOUDINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="c917e-224"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="c917e-224"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-225">Gibt die Größe der-Struktur an.</span><span class="sxs-lookup"><span data-stu-id="c917e-225">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-226"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span><span class="sxs-lookup"><span data-stu-id="c917e-226"><span id="Cloud"></span><span id="cloud"></span><span id="CLOUD"></span>**Cloud**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-227">Verweist auf eine-Struktur, die Kriterien angibt, die Sie zum Filtern von Suchergebnissen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c917e-227">Points to a structure that specifies criteria that you can use to filter search results.</span></span> <span data-ttu-id="c917e-228">Das Element **Cloud. Scope** kann den **PNRP \_ -Bereich \_ any**, den **globalen PNRP- \_ \_ Bereich**, den **lokalen PNRP- \_ Standort \_ \_ Bereich** oder den **lokalen PNRP- \_ Link \_ \_** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c917e-228">The **Cloud.Scope** member can be **PNRP\_SCOPE\_ANY**, **PNRP\_GLOBAL\_SCOPE**, **PNRP\_SITE\_LOCAL\_SCOPE**, or **PNRP\_LINK\_LOCAL\_SCOPE**.</span></span> <span data-ttu-id="c917e-229">Wenn **PNRP- \_ Bereich \_ any** angegeben ist, werden alle Clouds zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c917e-229">If **PNRP\_SCOPE\_ANY** is specified, all clouds are returned.</span></span> <span data-ttu-id="c917e-230">Andernfalls werden nur Clouds zurückgegeben, die dem **Cloud. Scope** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c917e-230">Otherwise, only clouds that match the **Cloud.Scope** are returned.</span></span>

</dd> <dt>

<span data-ttu-id="c917e-231"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**umcloudstate**</span><span class="sxs-lookup"><span data-stu-id="c917e-231"><span id="enCloudState"></span><span id="encloudstate"></span><span id="ENCLOUDSTATE"></span>**enCloudState**</span></span>
</dt> <dd>

<span data-ttu-id="c917e-232">Reserviert, muss NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="c917e-232">Reserved, must be zero (0).</span></span>

</dd> </dl>

### <a name="dwcontrolflags"></a><span data-ttu-id="c917e-233">dwcontrolflags</span><span class="sxs-lookup"><span data-stu-id="c917e-233">dwControlFlags</span></span>

<span data-ttu-id="c917e-234">Die folgenden Lup \_ - \_ \* rückgabeflags werden von PNRP unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c917e-234">The following LUP\_RETURN\_\* flags are supported by PNRP:</span></span>



| <span data-ttu-id="c917e-235">Wert</span><span class="sxs-lookup"><span data-stu-id="c917e-235">Value</span></span>             | <span data-ttu-id="c917e-236">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c917e-236">Description</span></span>                                                       |
|-------------------|-------------------------------------------------------------------|
| <span data-ttu-id="c917e-237">Name der Lup- \_ Rückgabe \_</span><span class="sxs-lookup"><span data-stu-id="c917e-237">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="c917e-238">Gibt einen Namen und einen Kontext zurück.</span><span class="sxs-lookup"><span data-stu-id="c917e-238">Returns a name and context.</span></span>                                       |
| <span data-ttu-id="c917e-239">Lup- \_ Rückgabe- \_ BLOB</span><span class="sxs-lookup"><span data-stu-id="c917e-239">LUP\_RETURN\_BLOB</span></span> | <span data-ttu-id="c917e-240">Gibt das [BLOB](pnrp-and-blob.md) zurück, das dieser Cloud zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c917e-240">Returns the [BLOB](pnrp-and-blob.md) associated with this cloud.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c917e-241">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c917e-241">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c917e-242">PNRP und BLOB</span><span class="sxs-lookup"><span data-stu-id="c917e-242">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="c917e-243">PNRP und WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="c917e-243">PNRP and WSALookupServiceEnd</span></span>](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="c917e-244">PNRP und WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="c917e-244">PNRP and WSALookupServiceNext</span></span>](pnrp-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="c917e-245">PNRP und wsanspioctl</span><span class="sxs-lookup"><span data-stu-id="c917e-245">PNRP and WSANSPIoctl</span></span>](pnrp-and-wsanspioctl.md)
</dt> <dt>

[<span data-ttu-id="c917e-246">PNRP und wsaqueryset</span><span class="sxs-lookup"><span data-stu-id="c917e-246">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="c917e-247">**Pnrpcloudinfo**</span><span class="sxs-lookup"><span data-stu-id="c917e-247">**PNRPCLOUDINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpcloudinfo)
</dt> <dt>

[<span data-ttu-id="c917e-248">**Pnrpinfo**</span><span class="sxs-lookup"><span data-stu-id="c917e-248">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="c917e-249">PNRP-NSP-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="c917e-249">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> </dl>

 

 



