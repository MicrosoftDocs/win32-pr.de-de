---
title: NAP-Typkonstanten (NapTypes.h)
description: Die folgenden NAP-Konstanten werden definiert.
ms.assetid: 2727487c-8c6a-4cd9-b6d8-253191a7d7f6
topic_type:
- apiref
api_name:
- maxSoHAttributeCount
- maxSoHAttributeSize
- minNetworkSoHSize
- maxNetworkSoHSize
- maxDwordCountPerSoHAttribute
- maxIpv4CountPerSoHAttribute
- maxIpv6CountPerSoHAttribute
- maxStringLength
- maxStringLengthInBytes
- maxSystemHealthEntityCount
- SystemHealthEntityCount
- maxEnforcerCount
- EnforcementEntityCount
- maxPrivateDataSize
- maxConnectionCountPerEnforcer
- maxCachedSoHCount
- freshSoHRequest
- shaFixup
- failureCategoryCount
- ComponentTypeEnforcementClientSoH
- ComponentTypeEnforcementClientRp
- defaultProtocolMaxSize
- maxProtocolMaxSize
- minProtocolMaxSize
- ProtocolMaxSize
api_location:
- NapTypes.h
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f0201f29d19969de6050ce3eeebf29a7bee73792dcc6b61b2359e5660db12d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685920"
---
# <a name="nap-type-constants"></a>NAP-Typkonstanten

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die folgenden NAP-Konstanten werden definiert.

Die folgenden NAP-Konstanten sind in NapTypes.h definiert:

<dl> <dt>

<span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxSoHAttributeCount**
</dt> <dd> <dl> <dt>

0x64
</dt> <dt>



Die maximale Anzahl von [**SoHAttribute-TLV-Objekten**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) (Type-Length-Value), die einem [**SoH-Paket**](/windows/win32/api/naptypes/ns-naptypes-soh) zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxSoHAttributeSize**
</dt> <dd> <dl> <dt>

0xFA0
</dt> <dt>



Die maximale Größe eines [**SoHAttribute-Objekts**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) in Bytes, das einem Integritätshinweispaket [**(SoH)**](/windows/win32/api/naptypes/ns-naptypes-soh)zugeordnet ist.


</dt> </dl> </dd> <dt>

<span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minNetworkSoHSize**
</dt> <dd> <dl> <dt>

0xC
</dt> <dt>



Die Mindestgröße eines [**SoH-Pakets**](/windows/win32/api/naptypes/ns-naptypes-soh) in Bytes.


</dt> </dl> </dd> <dt>

<span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxNetworkSoHSize**
</dt> <dd> <dl> <dt>

0xFA0
</dt> <dt>



Die maximale Größe eines [**SoH-Pakets**](/windows/win32/api/naptypes/ns-naptypes-soh) in Bytes.


</dt> </dl> </dd> <dt>

<span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxDwordCountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/sizeof(DWORD)
</dt> <dt>



Die maximale Anzahl von DWORD-Werten, die einem [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/0x4
</dt> <dt>



Die maximale Anzahl von IPv4-Adressen, die einem [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxSoHAttributeSize/0x10
</dt> <dt>



Die maximale Anzahl von IPv6-Adressen, die einem [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxStringLength**
</dt> <dd> <dl> <dt>

0x400
</dt> <dt>



Die maximale Länge einer Zeichenfolge, die von der [**CountedString-Struktur**](/windows/win32/api/naptypes/ns-naptypes-countedstring) angegeben wird.


</dt> </dl> </dd> <dt>

<span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxStringLengthInBytes**
</dt> <dd> <dl> <dt>

(maxStringLength + 1) \* sizeof(WCHAR)
</dt> <dt>



Die maximale Länge einer von der [**CountedString-Struktur**](/windows/win32/api/naptypes/ns-naptypes-countedstring) angegebenen Zeichenfolge in Bytes.


</dt> </dl> </dd> <dt>

<span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxSystemHealthEntityCount**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Die maximale Anzahl von Systemzustandsentitäten, z. B. SHVs und SHAs.


</dt> </dl> </dd> <dt>

<span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**SystemHealthEntityCount**
</dt> <dd> <dl> <dt>

\[range(0, maxSystemHealthEntityCount)\] 
</dt> <dt>



Der Bereich der möglichen Werte für die Anzahl der Systemzustandsentitäten.


</dt> </dl> </dd> <dt>

<span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxEnforcerCount**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Die maximale Anzahl von Erzwingungsentitäten, z. B. QECs.


</dt> </dl> </dd> <dt>

<span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**EnforcementEntityCount**
</dt> <dd> <dl> <dt>

\[range(0, maxEnforcerCount)\]
</dt> <dt>



Der Bereich der möglichen Werte für die Anzahl der Erzwingungsentitäten.


</dt> </dl> </dd> <dt>

<span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxPrivateDataSize**
</dt> <dd> <dl> <dt>

0xC8
</dt> <dt>



Die maximale Größe einer [**PrivateData-Struktur**](/windows/win32/api/naptypes/ns-naptypes-privatedata) in Bytes.


</dt> </dl> </dd> <dt>

<span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxConnectionCountPerEnforcer**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Die maximale Anzahl von [**INapEnforcementClientConnection-Objekten,**](inapenforcementclientconnection.md) die einer Erzwingungsentität zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxCachedSoHCount**
</dt> <dd> <dl> <dt>

maxSystemHealthEntityCount \* maxEnforcerCount \* maxConnectionCountPerEnforcer
</dt> <dt>



Die maximale Anzahl zwischengespeicherter SoH-Verbindungen für alle Systemzustands- und Erzwingungsentitäten.


</dt> </dl> </dd> <dt>

<span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshSoHRequest**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Gibt an, dass eine [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)auf eine neue Anforderung und nicht auf eine zwischengespeicherte Anforderung zurückzuführen ist. Dieses Flag wird vom NAP-Agent für ein [**INapEnforcementClientConnection-Objekt**](inapenforcementclientconnection.md) verwendet.


</dt> </dl> </dd> <dt>

<span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shaFixup**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Gibt an, dass eine Korrektur erforderlich ist. Dieses Flag wird von einem SHA verwendet.


</dt> </dl> </dd> <dt>

<span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failureCategoryCount**
</dt> <dd> <dl> <dt>

0x5
</dt> <dt>



Die Anzahl der Fehlerkategorien, die in einer [**FailureCategoryMapping-Struktur**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) enthalten sind.


</dt> </dl> </dd> <dt>

<span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**ComponentTypeEnforcementClientSoH**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Die Komponente ist ein Quarantäneerzwingungsclient (Quarantine Enforcement Client, QEC), der während der Verbindungsauthentifizierung ein [**SoH-Paket**](/windows/win32/api/naptypes/ns-naptypes-soh) in Band sendet.

> [!Note]  
> Dieser Wert wird nicht von SHAs und SHVs verwendet.

 


</dt> </dl> </dd> <dt>

<span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**ComponentTypeEnforcementClientRp**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



Die Komponente ist eine QEC, die [**INapCertRelyingParty**](inapcertrelyingparty.md) implementiert und mit dem Integritätszertifikatserver (HCS) interagieren muss, um ein Integritätszertifikat zu erhalten.

> [!Note]  
> Dieser Wert wird nicht von SHAs und SHVs verwendet.

 


</dt> </dl> </dd> </dl>

Die folgenden NAP-Konstanten sind in NapEnforcementClient.h definiert.

<dl> <dt>

<span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultProtocolMaxSize**
</dt> <dd> <dl> <dt>

0x0FA0
</dt> <dt>



Die maximale Standardgröße eines SoH-Pakets in Bytes.


</dt> </dl> </dd> <dt>

<span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxProtocolMaxSize**
</dt> <dd> <dl> <dt>

0xFFFF
</dt> <dt>



Die maximal mögliche Größe eines SoH-Pakets in Bytes.


</dt> </dl> </dd> <dt>

<span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minProtocolMaxSize**
</dt> <dd> <dl> <dt>

0x012C
</dt> <dt>



Die kleinstmögliche maximale Größe eines SoH-Pakets in Bytes. Die tatsächliche Größe des SoH-Pakets kann kleiner als **minProtocolMaxSize** sein.


</dt> </dl> </dd> <dt>

<span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**ProtocolMaxSize**
</dt> <dd> <dl> <dt>

range(minProtocolMaxSize, maxProtocolMaxSize)
</dt> <dt>



Der Bereich der möglichen Werte für die maximale Größe eines SoH-Pakets.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                                |
| Header<br/>                   | <dl> <dt>NapTypes.h; </dt> <dt>NapEnforcementClient.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**NAP-Konstanten**](nap-constants.md)
</dt> </dl>

 

 





