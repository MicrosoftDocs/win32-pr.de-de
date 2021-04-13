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
# <a name="add-sslcert"></a>add sslcert

Fügt eine neue SSL-Serverzertifikat Bindung (Secure Sockets Layer) und die entsprechenden Client Zertifikat Richtlinien für eine IP-Adresse und einen Port hinzu.

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

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[IPPort = \] * * * IP-Adresse: Port*
</dt> <dd>

Gibt die IP-Adresse und den Port für die Bindung an.

</dd> <dt>

<span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[CertHash = \] * * * Zeichenfolge*
</dt> <dd>

Gibt den SHA-Hash des Zertifikats an. Dieser Hash ist 20 Bytes lang und wird als hexadezimale Zeichenfolge angegeben.

</dd> <dt>

<span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[AppID = \] * * * GUID*
</dt> <dd>

Gibt die GUID zum Identifizieren der besitzenden Anwendung an.

</dd> <dt>

<span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename = \] * * * Zeichenfolge*
</dt> <dd>

Gibt den Speichernamen für das Zertifikat an. Die Standardeinstellung ist MY. Das Zertifikat muss im Kontext des lokalen Computers gespeichert werden.

</dd> <dt>

<span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation = {enable enable \| }\]**
</dt> <dd>

Schaltet die Überprüfung des Sperrens von Client Zertifikaten ein oder die Überprüfung wird durchgeführt.

</dd> <dt>

<span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly = {enable \| Deaktivieren}\]**
</dt> <dd>

Schaltet die Verwendung des zwischengespeicherten Client Zertifikats für die Sperr Überprüfung ein oder aus.

</dd> <dt>

<span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck = {enable \| Deaktivieren}\]**
</dt> <dd>

Schaltet die Nutzungs Überprüfung ein oder aus. Die Standardeinstellung ist „Aktiviert“.

</dd> <dt>

<span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[RevocationFreshnessTime = \] * * * u-int*
</dt> <dd>

Gibt das Zeitintervall an, nach dem eine aktualisierte Zertifikat Sperr Liste (CRL) überprüft werden soll. Wenn dieser Wert 0 ist, wird die neue Zertifikat Sperr Liste nur aktualisiert, wenn der vorherige Wert (in Sekunden) abläuft.

</dd> <dt>

<span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[UrlRetrievalTimeout = \] * * * u-int*
</dt> <dd>

Gibt das Timeout Intervall für das Abrufen der Zertifikats Sperr Liste für die Remote-URL (in Millisekunden) an.

</dd> <dt>

<span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[sslctlidentifier = \] * * * Zeichenfolge*
</dt> <dd>

Listet die Zertifikat Aussteller auf, denen vertraut werden kann. Diese Liste kann eine Teilmenge der Zertifikatsaussteller sein, denen der Computer vertraut.

</dd> <dt>

<span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[SslCtlStoreName = \] * * * Zeichenfolge*
</dt> <dd>

Gibt den Speicher Namen unter dem lokalen Computer an, auf \_ dem sslctlidentifier gespeichert ist.

</dd> <dt>

<span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage = {enable \| Deaktivieren}\]**
</dt> <dd>

Schaltet DS-Mapper ein oder aus. Die Standardeinstellung ist „Deaktiviert“.

</dd> <dt>

<span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertaushandlung = {enable \| Deaktivieren}\]**
</dt> <dd>

Schaltet die Aushandlung des Zertifikats ein oder aus. Die Standardeinstellung ist „Deaktiviert“.

</dd> </dl>

## <a name="examples"></a>Beispiele

**Hinzufügen von sslcert IPPort = 1.1.1.1:443**

**CertHash = 0102030405060708090a0b0c0d0e0f 1011121314**

**AppID = {00112233-4455-6677-8899-aabbccddeeff}**

 

 




