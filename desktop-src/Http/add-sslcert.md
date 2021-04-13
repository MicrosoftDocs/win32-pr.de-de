---
title: add sslcert
description: Fügt eine neue SSL-Serverzertifikat Bindung (Secure Sockets Layer) und die entsprechenden Client Zertifikat Richtlinien für eine IP-Adresse und einen Port hinzu.
ms.assetid: 4ba3d2cb-050f-46e3-81f9-5f7e360b19fb
keywords:
- Hinzufügen von sslcert http
topic_type:
- apiref
api_name:
- add sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a43569edd400b824876dff991f95e79cbfd6a96
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104389394"
---
# <a name="add-sslcert"></a><span data-ttu-id="7073a-104">add sslcert</span><span class="sxs-lookup"><span data-stu-id="7073a-104">add sslcert</span></span>

<span data-ttu-id="7073a-105">Fügt eine neue SSL-Serverzertifikat Bindung (Secure Sockets Layer) und die entsprechenden Client Zertifikat Richtlinien für eine IP-Adresse und einen Port hinzu.</span><span class="sxs-lookup"><span data-stu-id="7073a-105">Adds a new Secure Sockets Layer (SSL) server certificate binding and the corresponding client certificate policies for an IP address and port.</span></span>

``` syntax
add sslcert [ipport=]IP Address:port
            [certhash=]string
            [appid=]GUID
            [certstorename=]string
            [verifyclientcertrevocation={enable|disable}]
            [verifyrevocationwithcachedclientcertonly={enable|disable}]
            [usagecheck={enable|disable}]
            [revocationfreshnesstime=]u-int
            [urlretrievaltimeout=]u-int
            [sslctlidentifier=]string
            [sslctlstorename=]string
            [dsmapperusage={enable|disable}]
            [clientcertnegotiation={enable|disable}]

 
```

## <a name="parameters"></a><span data-ttu-id="7073a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7073a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7073a-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[IPPort = \] \* \* \* IP-Adresse: Port*</span><span class="sxs-lookup"><span data-stu-id="7073a-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport=\]\*\*\*IP Address:port*</span></span>
</dt> <dd>

<span data-ttu-id="7073a-108">Gibt die IP-Adresse und den Port für die Bindung an.</span><span class="sxs-lookup"><span data-stu-id="7073a-108">Specifies the IP address and port for the binding.</span></span>

</dd> <dt>

<span data-ttu-id="7073a-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>\**\[CertHash = \] \* \* \* Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="7073a-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>\**\[certhash=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="7073a-110">Gibt den SHA-Hash des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="7073a-110">Specifies the SHA hash of the certificate.</span></span> <span data-ttu-id="7073a-111">Dieser Hash ist 20 Bytes lang und wird als hexadezimale Zeichenfolge angegeben.</span><span class="sxs-lookup"><span data-stu-id="7073a-111">This hash is 20 bytes long and specified as a hexadecimal string.</span></span>

</dd> <dt>

<span data-ttu-id="7073a-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>\**\[AppID = \] \* \* \* GUID*</span><span class="sxs-lookup"><span data-stu-id="7073a-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>\**\[appid=\]\*\*\*GUID*</span></span>
</dt> <dd>

<span data-ttu-id="7073a-113">Gibt die GUID zum Identifizieren der besitzenden Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="7073a-113">Specifies the GUID to identify the owning application.</span></span>

</dd> <dt>

<span data-ttu-id="7073a-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>\**\[certstorename = \] \* \* \* Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="7073a-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>\**\[certstorename=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="7073a-115">Gibt den Speichernamen für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="7073a-115">Specifies the store name for the certificate.</span></span> <span data-ttu-id="7073a-116">Die Standardeinstellung ist MY.</span><span class="sxs-lookup"><span data-stu-id="7073a-116">Defaults to MY.</span></span> <span data-ttu-id="7073a-117">Das Zertifikat muss im Kontext des lokalen Computers gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7073a-117">Certificate must be stored in the local computer context.</span></span>

</dd> <dt>

<span data-ttu-id="7073a-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation = {enable enable \| }\]**</span><span class="sxs-lookup"><span data-stu-id="7073a-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="7073a-119">Schaltet die Überprüfung des Sperrens von Client Zertifikaten ein oder die Überprüfung wird durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="7073a-119">Turns on or turnsoff verification of revocation of client certificates.</span></span>

</dd> <dt>

<span data-ttu-id="7073a-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly = {enable \| Deaktivieren}\]**</span><span class="sxs-lookup"><span data-stu-id="7073a-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="7073a-121">Schaltet die Verwendung des zwischengespeicherten Client Zertifikats für die Sperr Überprüfung ein oder aus.</span><span class="sxs-lookup"><span data-stu-id="7073a-121">Turns on or turns off usage of only cached client certificate for revocation checking.</span></span>

</dd> <dt>

<span data-ttu-id="7073a-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck = {enable \| Deaktivieren}\]**</span><span class="sxs-lookup"><span data-stu-id="7073a-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="7073a-123">Schaltet die Nutzungs Überprüfung ein oder aus.</span><span class="sxs-lookup"><span data-stu-id="7073a-123">Turns on or turns off usage check.</span></span> <span data-ttu-id="7073a-124">Die Standardeinstellung ist „Aktiviert“.</span><span class="sxs-lookup"><span data-stu-id="7073a-124">Default is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="7073a-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>\**\[RevocationFreshnessTime = \] \* \* \* u-int*</span><span class="sxs-lookup"><span data-stu-id="7073a-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>\**\[revocationfreshnesstime=\]\*\*\*u-int*</span></span>
</dt> <dd>

<span data-ttu-id="7073a-126">Gibt das Zeitintervall an, nach dem eine aktualisierte Zertifikat Sperr Liste (CRL) überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="7073a-126">Specifies the time interval to check for an updated certificate revocation list (CRL).</span></span> <span data-ttu-id="7073a-127">Wenn dieser Wert 0 ist, wird die neue Zertifikat Sperr Liste nur aktualisiert, wenn der vorherige Wert (in Sekunden) abläuft.</span><span class="sxs-lookup"><span data-stu-id="7073a-127">If this value is 0, then the new CRL is updated only if the previous one expires (in seconds).</span></span>

</dd> <dt>

<span data-ttu-id="7073a-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>\**\[UrlRetrievalTimeout = \] \* \* \* u-int*</span><span class="sxs-lookup"><span data-stu-id="7073a-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>\**\[urlretrievaltimeout=\]\*\*\*u-int*</span></span>
</dt> <dd>

<span data-ttu-id="7073a-129">Gibt das Timeout Intervall für das Abrufen der Zertifikats Sperr Liste für die Remote-URL (in Millisekunden) an.</span><span class="sxs-lookup"><span data-stu-id="7073a-129">Specifies the timeout interval on attempts to retrieve the certificate revocation list for the remote URL (in milliseconds).</span></span>

</dd> <dt>

<span data-ttu-id="7073a-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>\**\[sslctlidentifier = \] \* \* \* Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="7073a-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>\**\[sslctlidentifier=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="7073a-131">Listet die Zertifikat Aussteller auf, denen vertraut werden kann.</span><span class="sxs-lookup"><span data-stu-id="7073a-131">Lists the certificate issuers that can be trusted.</span></span> <span data-ttu-id="7073a-132">Diese Liste kann eine Teilmenge der Zertifikatsaussteller sein, denen der Computer vertraut.</span><span class="sxs-lookup"><span data-stu-id="7073a-132">This list can be a subset of the certificate issuers that are trusted by the computer.</span></span>

</dd> <dt>

<span data-ttu-id="7073a-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>\**\[SslCtlStoreName = \] \* \* \* Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="7073a-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>\**\[sslctlstorename=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="7073a-134">Gibt den Speicher Namen unter dem lokalen Computer an, auf \_ dem sslctlidentifier gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7073a-134">Specifies the store name under LOCAL\_MACHINE where SslCtlIdentifier is stored.</span></span>

</dd> <dt>

<span data-ttu-id="7073a-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage = {enable \| Deaktivieren}\]**</span><span class="sxs-lookup"><span data-stu-id="7073a-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="7073a-136">Schaltet DS-Mapper ein oder aus.</span><span class="sxs-lookup"><span data-stu-id="7073a-136">Turns on or turns off DS mappers.</span></span> <span data-ttu-id="7073a-137">Die Standardeinstellung ist „Deaktiviert“.</span><span class="sxs-lookup"><span data-stu-id="7073a-137">Default is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="7073a-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertaushandlung = {enable \| Deaktivieren}\]**</span><span class="sxs-lookup"><span data-stu-id="7073a-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="7073a-139">Schaltet die Aushandlung des Zertifikats ein oder aus.</span><span class="sxs-lookup"><span data-stu-id="7073a-139">Turns on or turns off negotiation of certificate.</span></span> <span data-ttu-id="7073a-140">Die Standardeinstellung ist „Deaktiviert“.</span><span class="sxs-lookup"><span data-stu-id="7073a-140">Default is disabled.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="7073a-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7073a-141">Examples</span></span>

<span data-ttu-id="7073a-142">**Hinzufügen von sslcert IPPort = 1.1.1.1:443**</span><span class="sxs-lookup"><span data-stu-id="7073a-142">**add sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="7073a-143">**CertHash = 0102030405060708090a0b0c0d0e0f 1011121314**</span><span class="sxs-lookup"><span data-stu-id="7073a-143">**certhash=0102030405060708090A0B0C0D0E0F1011121314**</span></span>

<span data-ttu-id="7073a-144">**AppID = {00112233-4455-6677-8899-aabbccddeeff}**</span><span class="sxs-lookup"><span data-stu-id="7073a-144">**appid={00112233-4455-6677-8899-AABBCCDDEEFF}**</span></span>

 

 




