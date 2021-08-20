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
ms.openlocfilehash: 721931bfa05a96ca47fd69f643a02076201bb5f93eff003afa83714f2d14b519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950949"
---
# <a name="add-sslcert"></a>add sslcert

Fügt eine neue SECURE SOCKETS LAYER(SSL)-Serverzertifikatbindung und die entsprechenden Clientzertifikatrichtlinien für eine IP-Adresse und einen Port hinzu.

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

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport=IP-Adresse:Port\]**
</dt> <dd>

Gibt die IP-Adresse und den Port für die Bindung an.

</dd> <dt>

<span id="_certhash__string"></span><span id="_CERTHASH__STRING"></span>**\[certhash=string\]**
</dt> <dd>

Gibt den SHA-Hash des Zertifikats an. Dieser Hash ist 20 Byte lang und wird als hexadezimale Zeichenfolge angegeben.

</dd> <dt>

<span id="_appid__GUID"></span><span id="_appid__guid"></span><span id="_APPID__GUID"></span>**\[appid=GUID\]**
</dt> <dd>

Gibt die GUID zum Identifizieren der besitzenden Anwendung an.

</dd> <dt>

<span id="_certstorename__string"></span><span id="_CERTSTORENAME__STRING"></span>**\[certstorename=string\]**
</dt> <dd>

Gibt den Speichernamen für das Zertifikat an. Die Standardeinstellung ist MY. Das Zertifikat muss im Kontext des lokalen Computers gespeichert werden.

</dd> <dt>

<span id="_verifyclientcertrevocation__enable_disable__"></span><span id="_VERIFYCLIENTCERTREVOCATION__ENABLE_DISABLE__"></span>**\[verifyclientcertrevocation={enable \| disable}\]**
</dt> <dd>

Aktiviert oder deaktiviert die Überprüfung der Sperrung von Clientzertifikaten.

</dd> <dt>

<span id="_verifyrevocationwithcachedclientcertonly__enable_disable__"></span><span id="_VERIFYREVOCATIONWITHCACHEDCLIENTCERTONLY__ENABLE_DISABLE__"></span>**\[verifyrevocationwithcachedclientcertonly={enable \| disable}\]**
</dt> <dd>

Aktiviert oder deaktiviert die Ausschließliche Verwendung des zwischengespeicherten Clientzertifikats für die Sperrüberprüfung.

</dd> <dt>

<span id="_usagecheck__enable_disable__"></span><span id="_USAGECHECK__ENABLE_DISABLE__"></span>**\[usagecheck={enable \| disable}\]**
</dt> <dd>

Aktiviert oder deaktiviert die Nutzungsprüfung. Die Standardeinstellung ist „Aktiviert“.

</dd> <dt>

<span id="_revocationfreshnesstime__u-int"></span><span id="_REVOCATIONFRESHNESSTIME__U-INT"></span>**\[revocationfreshnesstime=u-int\]**
</dt> <dd>

Gibt das Zeitintervall für die Überprüfung auf eine aktualisierte Zertifikatsperrliste (Certificate Revocation List, CRL) an. Wenn dieser Wert 0 ist, wird die neue Zertifikatsperrliste nur aktualisiert, wenn die vorherige abläuft (in Sekunden).

</dd> <dt>

<span id="_urlretrievaltimeout__u-int"></span><span id="_URLRETRIEVALTIMEOUT__U-INT"></span>**\[urlretrievaltimeout=u-int\]**
</dt> <dd>

Gibt das Timeoutintervall für Versuche an, die Zertifikatsperrliste für die Remote-URL abzurufen (in Millisekunden).

</dd> <dt>

<span id="_sslctlidentifier__string"></span><span id="_SSLCTLIDENTIFIER__STRING"></span>**\[sslctlidentifier=string\]**
</dt> <dd>

Listet die Zertifikataussteller auf, die als vertrauenswürdig eingestuft werden können. Diese Liste kann eine Teilmenge der Zertifikatsaussteller sein, denen der Computer vertraut.

</dd> <dt>

<span id="_sslctlstorename__string"></span><span id="_SSLCTLSTORENAME__STRING"></span>**\[sslctlstorename=string\]**
</dt> <dd>

Gibt den Speichernamen unter LOCAL MACHINE an, in dem \_ SslCtlIdentifier gespeichert ist.

</dd> <dt>

<span id="_dsmapperusage__enable_disable__"></span><span id="_DSMAPPERUSAGE__ENABLE_DISABLE__"></span>**\[dsmapperusage={enable \| disable}\]**
</dt> <dd>

Aktiviert oder deaktiviert DS-Mapper. Die Standardeinstellung ist „Deaktiviert“.

</dd> <dt>

<span id="_clientcertnegotiation__enable_disable__"></span><span id="_CLIENTCERTNEGOTIATION__ENABLE_DISABLE__"></span>**\[clientcertnegotiation={enable \| disable}\]**
</dt> <dd>

Aktiviert oder deaktiviert die Aushandlung des Zertifikats. Die Standardeinstellung ist „Deaktiviert“.

</dd> </dl>

## <a name="examples"></a>Beispiele

**add sslcert ipport=1.1.1.1:443**

**certhash=0102030405060708090A0B0C0D0E0F1011121314**

**appid={00112233-4455-6677-8899-AABBCCDDEEFF}**

 

 




