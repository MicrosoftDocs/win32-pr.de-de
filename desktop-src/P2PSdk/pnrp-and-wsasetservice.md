---
description: PNRP verwendet die wsasetservice-Funktion, um Peer Namen zu registrieren oder zu entfernen.
ms.assetid: ea7941cd-2b3c-42d1-a291-759cbc32db0c
title: PNRP und wsasetservice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 005a04251a8b038c5895ae5dfafd65be9263edfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349226"
---
# <a name="pnrp-and-wsasetservice"></a><span data-ttu-id="19b0a-103">PNRP und wsasetservice</span><span class="sxs-lookup"><span data-stu-id="19b0a-103">PNRP and WSASetService</span></span>

<span data-ttu-id="19b0a-104">PNRP verwendet die [**wsasetservice**](winsock-nsp-reference-links.md) -Funktion, um [Peer Namen](peer-names.md)zu registrieren oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="19b0a-104">PNRP uses the [**WSASetService**](winsock-nsp-reference-links.md) function to register or remove [peer names](peer-names.md).</span></span>

## <a name="registering-a-name"></a><span data-ttu-id="19b0a-105">Registrieren eines Namens</span><span class="sxs-lookup"><span data-stu-id="19b0a-105">Registering a Name</span></span>

<span data-ttu-id="19b0a-106">Die Registrierung umfasst einen Peernamen und eine Gruppe von Endpunkten, an die ein Dienst kontaktiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="19b0a-106">Registration includes a peer name and set of endpoints where a service can be contacted.</span></span> <span data-ttu-id="19b0a-107">Eine Registrierung ist spezifisch für eine PNRP-Cloud.</span><span class="sxs-lookup"><span data-stu-id="19b0a-107">A registration is specific to a PNRP cloud.</span></span> <span data-ttu-id="19b0a-108">Nachdem ein Peer registriert wurde, gibt es eine Verzögerung zwischen der Registrierung und der Weitergabe der Registrierungsinformationen an andere Knoten.</span><span class="sxs-lookup"><span data-stu-id="19b0a-108">After a peer is registered, there is a delay between the registration and the propagation of the registration information to other nodes.</span></span> <span data-ttu-id="19b0a-109">Während dieser Zeit sind andere Knoten möglicherweise nicht in der Lage, einen neu registrierten Peer aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="19b0a-109">During this time, other nodes may not be able to resolve a newly registered peer.</span></span>

<span data-ttu-id="19b0a-110">Die Dienst Registrierung ist nicht persistent.</span><span class="sxs-lookup"><span data-stu-id="19b0a-110">Service registration is not persistent.</span></span>

-   <span data-ttu-id="19b0a-111">Wenn ein Client Prozess, der einen [**Peernamen registriert, das WSACleanup**](winsock-nsp-reference-links.md)-Ereignis beendet oder aufruft, wird die Registrierung des Peer namens aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="19b0a-111">If a client process that registers a peer name exits or calls [**WSACleanup**](winsock-nsp-reference-links.md), then the peer name is unregistered.</span></span>
-   <span data-ttu-id="19b0a-112">Wenn ein angegebener PeerName bereits vom aktuellen Prozess in der gleichen Cloud registriert ist, wird er durch neue Registrierungs Werte ersetzt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-112">If a specified peer name is already registered in the same cloud by the current process, it is replaced with new registration values.</span></span>

<span data-ttu-id="19b0a-113">Beim Registrieren eines Peer namens müssen die folgenden Parameterwerte angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="19b0a-113">When registering a peer name, the following parameter values must be indicated:</span></span>

-   <span data-ttu-id="19b0a-114">der *ESS Operation* -Parameter muss den Wert " **rnrservice \_ Register**" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="19b0a-114">*essOperation* parameter must have a value of **RNRSERVICE\_REGISTER**.</span></span>
-   <span data-ttu-id="19b0a-115">der *dwcontrolflags* -Parameter muss NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="19b0a-115">*dwControlFlags* parameter must be zero (0).</span></span>

<span data-ttu-id="19b0a-116">Beim Registrieren eines Peer namens muss die [**lpwsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur, auf die durch den *lpqsreginfo* -Parameter verwiesen wird, die folgenden Werte enthalten:</span><span class="sxs-lookup"><span data-stu-id="19b0a-116">When registering a peer name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure referenced by the *lpqsRegInfo* parameter must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="19b0a-117"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="19b0a-117"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-118">Gibt die Größe der-Struktur an.</span><span class="sxs-lookup"><span data-stu-id="19b0a-118">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-119"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszserviceingestancename**</span><span class="sxs-lookup"><span data-stu-id="19b0a-119"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-120">Gibt einen zu Registrier ingpeer Namen an.</span><span class="sxs-lookup"><span data-stu-id="19b0a-120">Specifies a peer name to register.</span></span> <span data-ttu-id="19b0a-121">Wenn der [PeerName](peer-names.md) nicht gesichert ist, ist die Identität optional.</span><span class="sxs-lookup"><span data-stu-id="19b0a-121">If the [peer name](peer-names.md) is unsecured, then the identity is optional.</span></span> <span data-ttu-id="19b0a-122">Wenn die Identität als **null** angegeben ist, verwendet PNRP die lokale Identität des Computers – standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="19b0a-122">If the identity is specified as **NULL**, PNRP uses the machine local identity—by default.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-123"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpserviceclassid**</span><span class="sxs-lookup"><span data-stu-id="19b0a-123"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-124">Muss "svcid \_ pnrpname" lauten.</span><span class="sxs-lookup"><span data-stu-id="19b0a-124">Must be SVCID\_PNRPNAME.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-125"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpversion**</span><span class="sxs-lookup"><span data-stu-id="19b0a-125"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-126">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19b0a-126">Ignored.</span></span> <span data-ttu-id="19b0a-127">Auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-127">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-128"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszcomment**</span><span class="sxs-lookup"><span data-stu-id="19b0a-128"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-129">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19b0a-129">Ignored.</span></span> <span data-ttu-id="19b0a-130">Allerdings muss die Zeichenfolge weiterhin weniger als 40 Zeichen enthalten, einschließlich des **null** -Terminator.</span><span class="sxs-lookup"><span data-stu-id="19b0a-130">However, the string is still required to be fewer than 40 characters, including the **NULL** terminator.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-131"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwnamespace**</span><span class="sxs-lookup"><span data-stu-id="19b0a-131"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-132">Muss entweder ' **NS \_ ' pnrpname** ' oder ' **NS \_ all**' sein.</span><span class="sxs-lookup"><span data-stu-id="19b0a-132">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-133"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpnsproviderid**</span><span class="sxs-lookup"><span data-stu-id="19b0a-133"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-134">Muss entweder der **NS- \_ Anbieter \_ pnrpname** oder **null** sein.</span><span class="sxs-lookup"><span data-stu-id="19b0a-134">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-135"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszcontext**</span><span class="sxs-lookup"><span data-stu-id="19b0a-135"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-136">Muss ein cloudName, eine leere Zeichenfolge oder **null** sein.</span><span class="sxs-lookup"><span data-stu-id="19b0a-136">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="19b0a-137">Wenn dieser Wert **null** oder eine leere Zeichenfolge ist, wird die Standard-Cloud "Global" verwendet.</span><span class="sxs-lookup"><span data-stu-id="19b0a-137">If this value is **NULL** or an empty string, the default cloud, "Global", is used.</span></span> <span data-ttu-id="19b0a-138">Andernfalls muss Sie auf einen gültigen cloudnamen verweisen.</span><span class="sxs-lookup"><span data-stu-id="19b0a-138">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-139"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwnumofprotokolle**</span><span class="sxs-lookup"><span data-stu-id="19b0a-139"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-140">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19b0a-140">Ignored.</span></span> <span data-ttu-id="19b0a-141">Auf NULL (0) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-141">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-142"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszquerystring**</span><span class="sxs-lookup"><span data-stu-id="19b0a-142"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-143">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19b0a-143">Ignored.</span></span> <span data-ttu-id="19b0a-144">Auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-144">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-145"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwnumofcsaddrs**</span><span class="sxs-lookup"><span data-stu-id="19b0a-145"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-146">Gibt die Anzahl der Adressen an, die von einem Dienst registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="19b0a-146">Specifies the number of addresses registered by a service.</span></span> <span data-ttu-id="19b0a-147">Die maximale Anzahl von Adressen, die für einen einzelnen Namen registriert werden kann, ist 10.</span><span class="sxs-lookup"><span data-stu-id="19b0a-147">The maximum number of addresses that can be registered for a single name is 10.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-148"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsabuffer**</span><span class="sxs-lookup"><span data-stu-id="19b0a-148"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-149">Zeiger auf eine Liste von Adressen, die registriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="19b0a-149">Pointer to a list of addresses to register.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-150"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwoutputflags**</span><span class="sxs-lookup"><span data-stu-id="19b0a-150"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-151">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19b0a-151">Ignored.</span></span> <span data-ttu-id="19b0a-152">Auf NULL (0) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-152">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-153"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpblob**</span><span class="sxs-lookup"><span data-stu-id="19b0a-153"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-154">Ein Zeiger auf eine [**BLOB**](winsock-nsp-reference-links.md) -Struktur, die auf eine [**pnrpinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) -Struktur zeigt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-154">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span> <span data-ttu-id="19b0a-155">Bestimmte Parameter in der **pnrpinfo** -Struktur müssen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="19b0a-155">Specific parameters in the **PNRPINFO** structure must be set.</span></span> <span data-ttu-id="19b0a-156">Weitere Informationen finden Sie im folgenden Abschnitt der **pnrpinfo** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="19b0a-156">For more information, see the following **PNRPINFO** structure section.</span></span>

</dd> </dl>

## <a name="pnrpinfo-structure"></a><span data-ttu-id="19b0a-157">Pnrpinfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="19b0a-157">PNRPINFO Structure</span></span>

<span data-ttu-id="19b0a-158">Wenn das **lpblob** -Element der [**lpwsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur festgelegt ist, müssen die folgenden Member der [**pnrpinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) -Struktur festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="19b0a-158">If the **lpBlob** member of the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure is set, the following members of the [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure must be set:</span></span>

<dl> <dt>

<span data-ttu-id="19b0a-159"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="19b0a-159"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-160">Gibt die Größe der-Struktur an.</span><span class="sxs-lookup"><span data-stu-id="19b0a-160">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-161"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszidentity**</span><span class="sxs-lookup"><span data-stu-id="19b0a-161"><span id="lpwszIdentity"></span><span id="lpwszidentity"></span><span id="LPWSZIDENTITY"></span>**lpwszIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-162">Gibt die Identität des Peer namens an, der mit [**peeridentitycreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate)erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="19b0a-162">Specifies the identity of the peer name that is created by using [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate).</span></span> <span data-ttu-id="19b0a-163">Wenn ein PeerName nicht gesichert ist, ist die Identität optional.</span><span class="sxs-lookup"><span data-stu-id="19b0a-163">If a peer name is unsecured, then the identity is optional.</span></span> <span data-ttu-id="19b0a-164">Wenn die Identität als **null** angegeben ist, verwendet PNRP die lokale Identität des Computers – standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="19b0a-164">If the identity is specified as **NULL**, PNRP uses the computer local identity—by default.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-165"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nmaxresolve**</span><span class="sxs-lookup"><span data-stu-id="19b0a-165"><span id="nMaxResolve"></span><span id="nmaxresolve"></span><span id="NMAXRESOLVE"></span>**nMaxResolve**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-166">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19b0a-166">Ignored.</span></span> <span data-ttu-id="19b0a-167">Auf NULL (0) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-167">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-168"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwtimeout**</span><span class="sxs-lookup"><span data-stu-id="19b0a-168"><span id="dwTimeout"></span><span id="dwtimeout"></span><span id="DWTIMEOUT"></span>**dwTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-169">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19b0a-169">Ignored.</span></span> <span data-ttu-id="19b0a-170">Auf NULL (0) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-170">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-171"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwlifetime**</span><span class="sxs-lookup"><span data-stu-id="19b0a-171"><span id="dwLifetime"></span><span id="dwlifetime"></span><span id="DWLIFETIME"></span>**dwLifetime**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-172">Gibt die Anzahl der Sekunden zwischen Aktualisierungs Vorgängen an.</span><span class="sxs-lookup"><span data-stu-id="19b0a-172">Specifies the number of seconds between refresh operations.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-173"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**einlösungs Vektor**</span><span class="sxs-lookup"><span data-stu-id="19b0a-173"><span id="enResolveCriteria"></span><span id="enresolvecriteria"></span><span id="ENRESOLVECRITERIA"></span>**enResolveCriteria**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-174">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19b0a-174">Ignored.</span></span> <span data-ttu-id="19b0a-175">Auf NULL (0) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-175">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-176"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="19b0a-176"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-177">Muss entweder NULL (0) oder **pnrpinfo- \_ Hinweis** sein.</span><span class="sxs-lookup"><span data-stu-id="19b0a-177">Must be either zero (0) or **PNRPINFO\_HINT**.</span></span> <span data-ttu-id="19b0a-178">Der Standardwert ist null (0).</span><span class="sxs-lookup"><span data-stu-id="19b0a-178">The default is zero (0).</span></span> <span data-ttu-id="19b0a-179">Dies bedeutet, dass der Dienst identifizierungsort der PNRP-ID mit der IP-Adresse in **sahint** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="19b0a-179">This means that the service location portion of the PNRP ID is built by using the IP address in **saHint**.</span></span> <span data-ttu-id="19b0a-180">Andernfalls wird der Dienst Speicherort erstellt, indem die erste IP-Adresse im ersten IPv6-Eintrag des **lpcsabuffer** -Members verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="19b0a-180">Otherwise, the service location is built by using the first IP address in the first IPv6 entry of the **lpcsaBuffer** member.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-181"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**sahint**</span><span class="sxs-lookup"><span data-stu-id="19b0a-181"><span id="saHint"></span><span id="sahint"></span><span id="SAHINT"></span>**saHint**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-182">Gibt die IPv6-Adresse für den Hinweis an.</span><span class="sxs-lookup"><span data-stu-id="19b0a-182">Specifies the IPv6 address for the hint.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-183"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**ennamestate**</span><span class="sxs-lookup"><span data-stu-id="19b0a-183"><span id="enNameState"></span><span id="ennamestate"></span><span id="ENNAMESTATE"></span>**enNameState**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-184">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19b0a-184">Ignored.</span></span> <span data-ttu-id="19b0a-185">Auf NULL (0) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-185">Set to zero (0).</span></span>

</dd> </dl>

## <a name="unregistering-a-peer-name"></a><span data-ttu-id="19b0a-186">Aufheben der Registrierung eines Peer namens</span><span class="sxs-lookup"><span data-stu-id="19b0a-186">Unregistering a Peer Name</span></span>

<span data-ttu-id="19b0a-187">In der folgenden Liste sind wichtige Informationen zum Aufheben der Registrierung eines Peer namens aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-187">The following list identifies the important information about unregistering a peer name.</span></span>

-   <span data-ttu-id="19b0a-188">Nur eine Anwendung, die einen Peernamen registriert, kann die Registrierung aufheben.</span><span class="sxs-lookup"><span data-stu-id="19b0a-188">Only an application that registers a peer name can unregister it.</span></span>
-   <span data-ttu-id="19b0a-189">Die Registrierung eines Peer namens wird automatisch aufgeh [**oben, wenn WSACleanup**](winsock-nsp-reference-links.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="19b0a-189">A peer name is unregistered automatically if [**WSACleanup**](winsock-nsp-reference-links.md) is called.</span></span>
-   <span data-ttu-id="19b0a-190">PNRP entfernt immer die gesamte Dienstnamen Registrierung.</span><span class="sxs-lookup"><span data-stu-id="19b0a-190">PNRP always removes the entire service name registration.</span></span> <span data-ttu-id="19b0a-191">Das Entfernen einzelner Adressen ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="19b0a-191">It does not allow removal of individual addresses.</span></span>
-   <span data-ttu-id="19b0a-192">Beim Aufheben der Registrierung eines Namens muss der Wert des Parameters " *ESS Operation* " den Wert " **rnrservice \_ Delete**" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="19b0a-192">When unregistering a name, the *essOperation* parameter must have a value of **RNRSERVICE\_DELETE**.</span></span>
-   <span data-ttu-id="19b0a-193">PNRP unterstützt den **rnrservice \_**-Registrierungs Wert nicht.</span><span class="sxs-lookup"><span data-stu-id="19b0a-193">PNRP does not support the value **RNRSERVICE\_DEREGISTER**.</span></span>
-   <span data-ttu-id="19b0a-194">Der *dwcontrolflags* -Parameter muss NULL (0) sein.</span><span class="sxs-lookup"><span data-stu-id="19b0a-194">The *dwControlFlags* parameter must be zero (0).</span></span>

<span data-ttu-id="19b0a-195">Beim Aufheben der Registrierung eines Namens muss die [**lpwsaqueryset**](pnrp-and-wsaqueryset.md) -Struktur, auf die der *lpqsreginfo* -Parameter verweist, die folgenden Werte enthalten:</span><span class="sxs-lookup"><span data-stu-id="19b0a-195">When unregistering a name, the [**LPWSAQUERYSET**](pnrp-and-wsaqueryset.md) structure that the *lpqsRegInfo* parameter references must contain the following values:</span></span>

<dl> <dt>

<span data-ttu-id="19b0a-196"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span><span class="sxs-lookup"><span data-stu-id="19b0a-196"><span id="dwSize"></span><span id="dwsize"></span><span id="DWSIZE"></span>**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-197">Gibt die Größe der-Struktur an.</span><span class="sxs-lookup"><span data-stu-id="19b0a-197">Specifies the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-198"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszserviceingestancename**</span><span class="sxs-lookup"><span data-stu-id="19b0a-198"><span id="lpszServiceInstanceName"></span><span id="lpszserviceinstancename"></span><span id="LPSZSERVICEINSTANCENAME"></span>**lpszServiceInstanceName**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-199">Gibt einen Peer Namen für die Aufhebung der Registrierung an.</span><span class="sxs-lookup"><span data-stu-id="19b0a-199">Specifies a peer name to unregister.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-200"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpserviceclassid**</span><span class="sxs-lookup"><span data-stu-id="19b0a-200"><span id="lpServiceClassID"></span><span id="lpserviceclassid"></span><span id="LPSERVICECLASSID"></span>**lpServiceClassID**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-201">Muss " **svcid \_ pnrpname**" lauten.</span><span class="sxs-lookup"><span data-stu-id="19b0a-201">Must be **SVCID\_PNRPNAME**.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-202"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpversion**</span><span class="sxs-lookup"><span data-stu-id="19b0a-202"><span id="lpVersion"></span><span id="lpversion"></span><span id="LPVERSION"></span>**lpVersion**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-203">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19b0a-203">Ignored.</span></span> <span data-ttu-id="19b0a-204">Auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-204">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-205"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszcomment**</span><span class="sxs-lookup"><span data-stu-id="19b0a-205"><span id="lpszComment"></span><span id="lpszcomment"></span><span id="LPSZCOMMENT"></span>**lpszComment**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-206">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19b0a-206">Ignored.</span></span> <span data-ttu-id="19b0a-207">Auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-207">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-208"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwnamespace**</span><span class="sxs-lookup"><span data-stu-id="19b0a-208"><span id="dwNameSpace"></span><span id="dwnamespace"></span><span id="DWNAMESPACE"></span>**dwNameSpace**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-209">Muss entweder ' **NS \_ ' pnrpname** ' oder ' **NS \_ all**' sein.</span><span class="sxs-lookup"><span data-stu-id="19b0a-209">Must be either **NS\_PNRPNAME** or **NS\_ALL**.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-210"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpnsproviderid**</span><span class="sxs-lookup"><span data-stu-id="19b0a-210"><span id="lpNSProviderID"></span><span id="lpnsproviderid"></span><span id="LPNSPROVIDERID"></span>**lpNSProviderID**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-211">Muss entweder der **NS- \_ Anbieter \_ pnrpname** oder **null** sein.</span><span class="sxs-lookup"><span data-stu-id="19b0a-211">Must be either **NS\_PROVIDER\_PNRPNAME** or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-212"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszcontext**</span><span class="sxs-lookup"><span data-stu-id="19b0a-212"><span id="lpszContext"></span><span id="lpszcontext"></span><span id="LPSZCONTEXT"></span>**lpszContext**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-213">Muss ein cloudName, eine leere Zeichenfolge oder **null** sein.</span><span class="sxs-lookup"><span data-stu-id="19b0a-213">Must be a cloud name, an empty string, or **NULL**.</span></span> <span data-ttu-id="19b0a-214">Wenn dieser Wert **null** oder eine leere Zeichenfolge ist, wird die Standard-Cloud "Global" verwendet.</span><span class="sxs-lookup"><span data-stu-id="19b0a-214">If this value is **NULL** or an empty string, the default cloud, "Global" is used.</span></span> <span data-ttu-id="19b0a-215">Andernfalls muss Sie auf einen gültigen cloudnamen verweisen.</span><span class="sxs-lookup"><span data-stu-id="19b0a-215">Otherwise, it must point to a valid cloud name.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-216"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwnumofprotokolle**</span><span class="sxs-lookup"><span data-stu-id="19b0a-216"><span id="dwNumberOfProtocols"></span><span id="dwnumberofprotocols"></span><span id="DWNUMBEROFPROTOCOLS"></span>**dwNumberOfProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-217">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19b0a-217">Ignored.</span></span> <span data-ttu-id="19b0a-218">Auf NULL (0) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-218">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-219"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszquerystring**</span><span class="sxs-lookup"><span data-stu-id="19b0a-219"><span id="lpszQueryString"></span><span id="lpszquerystring"></span><span id="LPSZQUERYSTRING"></span>**lpszQueryString**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-220">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19b0a-220">Ignored.</span></span> <span data-ttu-id="19b0a-221">Auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-221">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-222"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwnumofcsaddrs**</span><span class="sxs-lookup"><span data-stu-id="19b0a-222"><span id="dwNumberOfCsAddrs"></span><span id="dwnumberofcsaddrs"></span><span id="DWNUMBEROFCSADDRS"></span>**dwNumberOfCsAddrs**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-223">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19b0a-223">Ignored.</span></span> <span data-ttu-id="19b0a-224">Auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-224">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-225"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsabuffer**</span><span class="sxs-lookup"><span data-stu-id="19b0a-225"><span id="lpcsaBuffer"></span><span id="lpcsabuffer"></span><span id="LPCSABUFFER"></span>**lpcsaBuffer**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-226">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19b0a-226">Ignored.</span></span> <span data-ttu-id="19b0a-227">Auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-227">Set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-228"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwoutputflags**</span><span class="sxs-lookup"><span data-stu-id="19b0a-228"><span id="dwOutputFlags"></span><span id="dwoutputflags"></span><span id="DWOUTPUTFLAGS"></span>**dwOutputFlags**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-229">Ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19b0a-229">Ignored.</span></span> <span data-ttu-id="19b0a-230">Auf NULL (0) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-230">Set to zero (0).</span></span>

</dd> <dt>

<span data-ttu-id="19b0a-231"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpblob**</span><span class="sxs-lookup"><span data-stu-id="19b0a-231"><span id="lpBlob"></span><span id="lpblob"></span><span id="LPBLOB"></span>**lpBlob**</span></span>
</dt> <dd>

<span data-ttu-id="19b0a-232">Ein Zeiger auf eine [**BLOB**](winsock-nsp-reference-links.md) -Struktur, die auf eine [**pnrpinfo**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) -Struktur zeigt.</span><span class="sxs-lookup"><span data-stu-id="19b0a-232">Pointer to a [**BLOB**](winsock-nsp-reference-links.md) structure that points to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span> <span data-ttu-id="19b0a-233">Der **lpszidentity** -Member der **lpblob** -Struktur identifiziert den Namen der Identität, die zum Registrieren eines Peer namens verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="19b0a-233">The **lpszIdentity** member of the **lpBlob** structure identifies the name of the identity that is used to register a peer name.</span></span> <span data-ttu-id="19b0a-234">Die übrigen Elemente müssen auf dieselben Werte festgelegt werden, die beim Registrieren eines Namens verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19b0a-234">The remaining members must be set to the same values that are used when registering a name.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="19b0a-235">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="19b0a-235">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19b0a-236">PNRP und BLOB</span><span class="sxs-lookup"><span data-stu-id="19b0a-236">PNRP and BLOB</span></span>](pnrp-and-blob.md)
</dt> <dt>

[<span data-ttu-id="19b0a-237">PNRP und wsaqueryset</span><span class="sxs-lookup"><span data-stu-id="19b0a-237">PNRP and WSAQUERYSET</span></span>](pnrp-and-wsaqueryset.md)
</dt> <dt>

[<span data-ttu-id="19b0a-238">**Pnrpinfo**</span><span class="sxs-lookup"><span data-stu-id="19b0a-238">**PNRPINFO**</span></span>](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1)
</dt> <dt>

[<span data-ttu-id="19b0a-239">PNRP-NSP-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="19b0a-239">PNRP NSP Error Codes</span></span>](pnrp-nsp-error-codes.md)
</dt> <dt>

[<span data-ttu-id="19b0a-240">**WSACleanup**</span><span class="sxs-lookup"><span data-stu-id="19b0a-240">**WSACleanup**</span></span>](winsock-nsp-reference-links.md)
</dt> <dt>

<span data-ttu-id="19b0a-241">**Wsasetservice**</span><span class="sxs-lookup"><span data-stu-id="19b0a-241">**WSASetService**</span></span>
</dt> </dl>

 

 



