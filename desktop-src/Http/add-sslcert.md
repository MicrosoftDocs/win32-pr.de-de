---
title: add sslcert
description: Fügt eine neue SECURE SOCKETS LAYER(SSL)-Serverzertifikatbindung und die entsprechenden Clientzertifikatrichtlinien für eine IP-Adresse und einen Port hinzu.
ms.assetid: 4ba3d2cb-050f-46e3-81f9-5f7e360b19fb
keywords:
- sslcert HTTP hinzufügen
topic_type:
- apiref
api_name:
- add sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309050be35748f39eefc8b40b8e590f8f6889fde
ms.sourcegitcommit: 07ba02719c9779e082b108ae74f9699fb0236c34
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/06/2021
ms.locfileid: "108644192"
---
# <a name="add-sslcert"></a><span data-ttu-id="c8a2f-104">add sslcert</span><span class="sxs-lookup"><span data-stu-id="c8a2f-104">add sslcert</span></span>

<span data-ttu-id="c8a2f-105">Fügt eine neue SECURE SOCKETS LAYER(SSL)-Serverzertifikatbindung und die entsprechenden Clientzertifikatrichtlinien für eine IP-Adresse und einen Port hinzu.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-105">Adds a new Secure Sockets Layer (SSL) server certificate binding and the corresponding client certificate policies for an IP address and port.</span></span>

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

## <a name="parameters"></a><span data-ttu-id="c8a2f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8a2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8a2f-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport=IP-Adresse:Port\]**</span><span class="sxs-lookup"><span data-stu-id="c8a2f-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport=IP Address:port\]**</span></span>
</dt> <dd>

<span data-ttu-id="c8a2f-108">Gibt die IP-Adresse und den Port für die Bindung an.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-108">Specifies the IP address and port for the binding.</span></span>

</dd> <dt>

<span data-ttu-id="c8a2f-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash=string\]**</span><span class="sxs-lookup"><span data-stu-id="c8a2f-109"><span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="c8a2f-110">Gibt den SHA-Hash des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-110">Specifies the SHA hash of the certificate.</span></span> <span data-ttu-id="c8a2f-111">Dieser Hash ist 20 Byte lang und wird als hexadezimale Zeichenfolge angegeben.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-111">This hash is 20 bytes long and specified as a hexadecimal string.</span></span>

</dd> <dt>

<span data-ttu-id="c8a2f-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[appid=GUID\]**</span><span class="sxs-lookup"><span data-stu-id="c8a2f-112"><span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[appid=GUID\]**</span></span>
</dt> <dd>

<span data-ttu-id="c8a2f-113">Gibt die GUID zum Identifizieren der besitzenden Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-113">Specifies the GUID to identify the owning application.</span></span>

</dd> <dt>

<span data-ttu-id="c8a2f-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename=string\]**</span><span class="sxs-lookup"><span data-stu-id="c8a2f-114"><span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="c8a2f-115">Gibt den Speichernamen für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-115">Specifies the store name for the certificate.</span></span> <span data-ttu-id="c8a2f-116">Die Standardeinstellung ist MY.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-116">Defaults to MY.</span></span> <span data-ttu-id="c8a2f-117">Das Zertifikat muss im Kontext des lokalen Computers gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-117">Certificate must be stored in the local computer context.</span></span>

</dd> <dt>

<span data-ttu-id="c8a2f-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation={enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="c8a2f-118"><span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="c8a2f-119">Aktiviert oder deaktiviert die Überprüfung der Sperrung von Clientzertifikaten.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-119">Turns on or turnsoff verification of revocation of client certificates.</span></span>

</dd> <dt>

<span data-ttu-id="c8a2f-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly={enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="c8a2f-120"><span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="c8a2f-121">Aktiviert oder deaktiviert die Ausschließliche Verwendung des zwischengespeicherten Clientzertifikats für die Sperrüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-121">Turns on or turns off usage of only cached client certificate for revocation checking.</span></span>

</dd> <dt>

<span data-ttu-id="c8a2f-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck={enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="c8a2f-122"><span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="c8a2f-123">Aktiviert oder deaktiviert die Nutzungsprüfung.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-123">Turns on or turns off usage check.</span></span> <span data-ttu-id="c8a2f-124">Die Standardeinstellung ist „Aktiviert“.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-124">Default is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="c8a2f-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[revocationfreshnesstime=u-int\]**</span><span class="sxs-lookup"><span data-stu-id="c8a2f-125"><span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[revocationfreshnesstime=u-int\]**</span></span>
</dt> <dd>

<span data-ttu-id="c8a2f-126">Gibt das Zeitintervall für die Überprüfung auf eine aktualisierte Zertifikatsperrliste (Certificate Revocation List, CRL) an.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-126">Specifies the time interval to check for an updated certificate revocation list (CRL).</span></span> <span data-ttu-id="c8a2f-127">Wenn dieser Wert 0 ist, wird die neue Zertifikatsperrliste nur aktualisiert, wenn die vorherige abläuft (in Sekunden).</span><span class="sxs-lookup"><span data-stu-id="c8a2f-127">If this value is 0, then the new CRL is updated only if the previous one expires (in seconds).</span></span>

</dd> <dt>

<span data-ttu-id="c8a2f-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[urlretrievaltimeout=u-int\]**</span><span class="sxs-lookup"><span data-stu-id="c8a2f-128"><span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[urlretrievaltimeout=u-int\]**</span></span>
</dt> <dd>

<span data-ttu-id="c8a2f-129">Gibt das Timeoutintervall für Versuche an, die Zertifikatsperrliste für die Remote-URL abzurufen (in Millisekunden).</span><span class="sxs-lookup"><span data-stu-id="c8a2f-129">Specifies the timeout interval on attempts to retrieve the certificate revocation list for the remote URL (in milliseconds).</span></span>

</dd> <dt>

<span data-ttu-id="c8a2f-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[sslctlidentifier=string\]**</span><span class="sxs-lookup"><span data-stu-id="c8a2f-130"><span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[sslctlidentifier=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="c8a2f-131">Listet die Zertifikataussteller auf, die als vertrauenswürdig eingestuft werden können.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-131">Lists the certificate issuers that can be trusted.</span></span> <span data-ttu-id="c8a2f-132">Diese Liste kann eine Teilmenge der Zertifikatsaussteller sein, denen der Computer vertraut.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-132">This list can be a subset of the certificate issuers that are trusted by the computer.</span></span>

</dd> <dt>

<span data-ttu-id="c8a2f-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[sslctlstorename=string\]**</span><span class="sxs-lookup"><span data-stu-id="c8a2f-133"><span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[sslctlstorename=string\]**</span></span>
</dt> <dd>

<span data-ttu-id="c8a2f-134">Gibt den Speichernamen unter LOCAL \_ MACHINE an, auf dem SslCtlIdentifier gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-134">Specifies the store name under LOCAL\_MACHINE where SslCtlIdentifier is stored.</span></span>

</dd> <dt>

<span data-ttu-id="c8a2f-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage={enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="c8a2f-135"><span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="c8a2f-136">Aktiviert oder deaktiviert DS-Mapper.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-136">Turns on or turns off DS mappers.</span></span> <span data-ttu-id="c8a2f-137">Die Standardeinstellung ist „Deaktiviert“.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-137">Default is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="c8a2f-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation={enable \| disable}\]**</span><span class="sxs-lookup"><span data-stu-id="c8a2f-138"><span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation={enable\|disable}\]**</span></span>
</dt> <dd>

<span data-ttu-id="c8a2f-139">Aktiviert oder deaktiviert die Aushandlung des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-139">Turns on or turns off negotiation of certificate.</span></span> <span data-ttu-id="c8a2f-140">Die Standardeinstellung ist „Deaktiviert“.</span><span class="sxs-lookup"><span data-stu-id="c8a2f-140">Default is disabled.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="c8a2f-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8a2f-141">Examples</span></span>

<span data-ttu-id="c8a2f-142">**add sslcert ipport=1.1.1.1:443**</span><span class="sxs-lookup"><span data-stu-id="c8a2f-142">**add sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="c8a2f-143">**certhash=0102030405060708090A0B0C0D0E0F1011121314**</span><span class="sxs-lookup"><span data-stu-id="c8a2f-143">**certhash=0102030405060708090A0B0C0D0E0F1011121314**</span></span>

<span data-ttu-id="c8a2f-144">**appid={00112233-4455-6677-8899-AABBCCDDEEFF}**</span><span class="sxs-lookup"><span data-stu-id="c8a2f-144">**appid={00112233-4455-6677-8899-AABBCCDDEEFF}**</span></span>

 

 




