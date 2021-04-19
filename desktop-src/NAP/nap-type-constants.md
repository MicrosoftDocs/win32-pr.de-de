---
title: NAP-Typkonstanten (naptypes. h)
description: Die folgenden NAP-Konstanten sind definiert.
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
ms.openlocfilehash: 85692a7ccc9cbb602a34da714a5eeb488ea5c4a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346522"
---
# <a name="nap-type-constants"></a>NAP-Typkonstanten

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die folgenden NAP-Konstanten sind definiert.

Die folgenden NAP-Konstanten werden in "naptypes. h" definiert:

<dl> <dt>

<span id="maxSoHAttributeCount"></span><span id="maxsohattributecount"></span><span id="MAXSOHATTRIBUTECOUNT"></span>**maxsohattributecount**
</dt> <dd> <dl> <dt>

0x64
</dt> <dt>



Die maximale Anzahl von [**sohattribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) -TLV-Objekten (Type-Length-Value), die einem [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="maxSoHAttributeSize"></span><span id="maxsohattributesize"></span><span id="MAXSOHATTRIBUTESIZE"></span>**maxsohattributesize**
</dt> <dd> <dl> <dt>

0xfa0
</dt> <dt>



Die maximale Größe (in Bytes) eines [**sohattribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) -Objekts, das einem [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)-Paket (Statement of Health) zugeordnet ist.


</dt> </dl> </dd> <dt>

<span id="minNetworkSoHSize"></span><span id="minnetworksohsize"></span><span id="MINNETWORKSOHSIZE"></span>**minnetworksohsize**
</dt> <dd> <dl> <dt>

0xc
</dt> <dt>



Die minimale Größe eines [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Pakets in Byte.


</dt> </dl> </dd> <dt>

<span id="maxNetworkSoHSize"></span><span id="maxnetworksohsize"></span><span id="MAXNETWORKSOHSIZE"></span>**maxnetworksohsize**
</dt> <dd> <dl> <dt>

0xfa0
</dt> <dt>



Die maximale Größe eines [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Pakets in Byte.


</dt> </dl> </dd> <dt>

<span id="maxDwordCountPerSoHAttribute"></span><span id="maxdwordcountpersohattribute"></span><span id="MAXDWORDCOUNTPERSOHATTRIBUTE"></span>**maxdwordzählpersohattribute**
</dt> <dd> <dl> <dt>

maxsohattributesize/sizeof (DWORD)
</dt> <dt>



Die maximale Anzahl von DWORD-Werten, die einem [**sohattribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="maxIpv4CountPerSoHAttribute"></span><span id="maxipv4countpersohattribute"></span><span id="MAXIPV4COUNTPERSOHATTRIBUTE"></span>**maxIpv4CountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxsohattributesize/0x4
</dt> <dt>



Die maximale Anzahl von IPv4-Adressen, die einem [**sohattribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="maxIpv6CountPerSoHAttribute"></span><span id="maxipv6countpersohattribute"></span><span id="MAXIPV6COUNTPERSOHATTRIBUTE"></span>**maxIpv6CountPerSoHAttribute**
</dt> <dd> <dl> <dt>

maxsohattributesize/0x10
</dt> <dt>



Die maximale Anzahl von IPv6-Adressen, die einem [**sohattribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="maxStringLength"></span><span id="maxstringlength"></span><span id="MAXSTRINGLENGTH"></span>**maxstringlength**
</dt> <dd> <dl> <dt>

0x400
</dt> <dt>



Die maximale Länge einer Zeichenfolge, die von der [**countedstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur angegeben wird.


</dt> </dl> </dd> <dt>

<span id="maxStringLengthInBytes"></span><span id="maxstringlengthinbytes"></span><span id="MAXSTRINGLENGTHINBYTES"></span>**maxstringlengthinbytes**
</dt> <dd> <dl> <dt>

(maxstringlength + 1) \* sizeof (WChar)
</dt> <dt>



Die maximale Länge einer Zeichenfolge in Bytes, die von der [**countedstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur angegeben wird.


</dt> </dl> </dd> <dt>

<span id="maxSystemHealthEntityCount"></span><span id="maxsystemhealthentitycount"></span><span id="MAXSYSTEMHEALTHENTITYCOUNT"></span>**maxsystemhealthentitycount**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Die maximale Anzahl von Systemintegritäts-Entitäten, z. b. SHVs und SHAs.


</dt> </dl> </dd> <dt>

<span id="SystemHealthEntityCount"></span><span id="systemhealthentitycount"></span><span id="SYSTEMHEALTHENTITYCOUNT"></span>**Systemhealthentitycount**
</dt> <dd> <dl> <dt>

\[Bereich (0, maxsystemhealthentitycount)\] 
</dt> <dt>



Der Bereich möglicher Werte für die Anzahl der Systemintegritäts-Entitäten.


</dt> </dl> </dd> <dt>

<span id="maxEnforcerCount"></span><span id="maxenforcercount"></span><span id="MAXENFORCERCOUNT"></span>**maxenforcercount**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Die maximale Anzahl von Erzwingungs Entitäten, z. b. qecs.


</dt> </dl> </dd> <dt>

<span id="EnforcementEntityCount"></span><span id="enforcemententitycount"></span><span id="ENFORCEMENTENTITYCOUNT"></span>**Enforcemententitycount**
</dt> <dd> <dl> <dt>

\[Bereich (0, maxenforcercount)\]
</dt> <dt>



Der Bereich möglicher Werte für die Anzahl von Erzwingungs Entitäten.


</dt> </dl> </dd> <dt>

<span id="maxPrivateDataSize"></span><span id="maxprivatedatasize"></span><span id="MAXPRIVATEDATASIZE"></span>**maxprivatedatasize**
</dt> <dd> <dl> <dt>

0xc8
</dt> <dt>



Die maximale Größe einer [**PRIVATEDATA**](/windows/win32/api/naptypes/ns-naptypes-privatedata) -Struktur in Bytes.


</dt> </dl> </dd> <dt>

<span id="maxConnectionCountPerEnforcer"></span><span id="maxconnectioncountperenforcer"></span><span id="MAXCONNECTIONCOUNTPERENFORCER"></span>**maxconnectioncountrytperenforcer**
</dt> <dd> <dl> <dt>

0x14
</dt> <dt>



Die maximale Anzahl von [**inapenforcementclientconnection**](inapenforcementclientconnection.md) -Objekten, die einer Erzwingungs Entität zugeordnet sind.


</dt> </dl> </dd> <dt>

<span id="maxCachedSoHCount"></span><span id="maxcachedsohcount"></span><span id="MAXCACHEDSOHCOUNT"></span>**maxcachedsohcount**
</dt> <dd> <dl> <dt>

maxsystemhealthentitycount \* maxenforcercount \* maxconnectiongräfin-perenforcer
</dt> <dt>



Die maximale Anzahl von zwischengespeicherten SoH-Verbindungen für alle Systemintegritäts-und Erzwingungs Entitäten.


</dt> </dl> </dd> <dt>

<span id="freshSoHRequest"></span><span id="freshsohrequest"></span><span id="FRESHSOHREQUEST"></span>**freshsohrequest**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Gibt an, dass ein [**sohresponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh)-Wert auf eine neue Anforderung und nicht auf eine zwischengespeicherte Anforderung zurückzuführen ist. Dieses Flag wird vom NAP-Agent auf einem [**inapenforcementclientconnection**](inapenforcementclientconnection.md) -Objekt verwendet.


</dt> </dl> </dd> <dt>

<span id="shaFixup"></span><span id="shafixup"></span><span id="SHAFIXUP"></span>**shafixup**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Gibt an, dass ein Problem behoben werden muss. Dieses Flag wird von einem SHA verwendet.


</dt> </dl> </dd> <dt>

<span id="failureCategoryCount"></span><span id="failurecategorycount"></span><span id="FAILURECATEGORYCOUNT"></span>**failurecategorycount**
</dt> <dd> <dl> <dt>

0x5
</dt> <dt>



Die Anzahl der Fehlerkategorien, die in einer [**failurecategorymapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) -Struktur enthalten sind.


</dt> </dl> </dd> <dt>

<span id="ComponentTypeEnforcementClientSoH"></span><span id="componenttypeenforcementclientsoh"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTSOH"></span>**Componenttypeenforcementclientsoh**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Bei der Komponente handelt es sich um einen Quarantäne Erzwingungs Client (QEC), der während der Verbindungs Authentifizierung ein [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket in-Band sendet.

> [!Note]  
> Dieser Wert wird von SHAs und SHVs nicht verwendet.

 


</dt> </dl> </dd> <dt>

<span id="ComponentTypeEnforcementClientRp"></span><span id="componenttypeenforcementclientrp"></span><span id="COMPONENTTYPEENFORCEMENTCLIENTRP"></span>**Componenttypeenforcementclientrp**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



Die Komponente ist ein QEC, das [**inapcertrelyingparty**](inapcertrelyingparty.md) implementiert und mit dem Integritäts Zertifikat Server (HCS) interagieren muss, damit ein Integritäts Zertifikat abgerufen werden kann.

> [!Note]  
> Dieser Wert wird von SHAs und SHVs nicht verwendet.

 


</dt> </dl> </dd> </dl>

Die folgenden NAP-Konstanten werden in "napforcementclient. h" definiert.

<dl> <dt>

<span id="defaultProtocolMaxSize"></span><span id="defaultprotocolmaxsize"></span><span id="DEFAULTPROTOCOLMAXSIZE"></span>**defaultprotocolmaxsize**
</dt> <dd> <dl> <dt>

0x0fa0
</dt> <dt>



Die maximale Standardgröße eines SoH-Pakets in Byte.


</dt> </dl> </dd> <dt>

<span id="maxProtocolMaxSize"></span><span id="maxprotocolmaxsize"></span><span id="MAXPROTOCOLMAXSIZE"></span>**maxprotocolmaxsize**
</dt> <dd> <dl> <dt>

0xFFFF
</dt> <dt>



Die maximal mögliche Größe eines SoH-Pakets in Bytes.


</dt> </dl> </dd> <dt>

<span id="minProtocolMaxSize"></span><span id="minprotocolmaxsize"></span><span id="MINPROTOCOLMAXSIZE"></span>**minprotocolmaxsize**
</dt> <dd> <dl> <dt>

0x012c
</dt> <dt>



Die kleinste mögliche maximale Größe eines SoH-Pakets in Byte. Die tatsächliche Größe des SoH-Pakets kann kleiner als **minprotocolmaxsize** sein.


</dt> </dl> </dd> <dt>

<span id="ProtocolMaxSize"></span><span id="protocolmaxsize"></span><span id="PROTOCOLMAXSIZE"></span>**Protocolmaxsize**
</dt> <dd> <dl> <dt>

Bereich (minprotocolmaxsize, maxprotocolmaxsize)
</dt> <dt>



Der Bereich möglicher Werte für die maximale Größe eines SoH-Pakets.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                                                                |
| Header<br/>                   | <dl> <dt>Naptypes. h; </dt> <dt>Napforcementclient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**NAP-Konstanten**](nap-constants.md)
</dt> </dl>

 

 





