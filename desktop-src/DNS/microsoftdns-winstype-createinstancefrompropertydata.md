---
title: CreateInstanceFromPropertyData-Methode der MicrosoftDNS_WINSType-Klasse
description: Die CreateInstanceFromPropertyData-Methode instanziiert einen Windows WINS-Ressourceneintrag (Internet Name Service).
ms.assetid: 0b41a6a5-0bb1-467b-9089-2c721d521887
keywords:
- CreateInstanceFromPropertyData-Methode DNS
- CreateInstanceFromPropertyData-Methode DNS, MicrosoftDNS_WINSType-Klasse
- MicrosoftDNS_WINSType-Klasse DNS, CreateInstanceFromPropertyData-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92f39b360c29ca859c0d0fd0188f0b065dec58293207c27e0a0267572472aabe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077050"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winstype-class"></a>CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ WINSType-Klasse

Die **CreateInstanceFromPropertyData-Methode** instanziiert einen Windows WINS-Ressourceneintrag (Internet Name Service).

## <a name="syntax"></a>Syntax


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint32                MappingFlag,
  [in]           uint32                LookupTimeout,
  [in]           uint32                CacheTimeout,
  [in]           string                WinsServers,
  [out, ref]     MicrosoftDNS_WINSType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DnsServerName* \[ In\]
</dt> <dd>

FQDN oder IP-Adresse des DNS-Servers, der diese RR enthält.

</dd> <dt>

*ContainerName* \[ In\]
</dt> <dd>

Name des Containers für die Zone, den Cache oder die RootHints-Instanz, die diese RR enthält.

</dd> <dt>

*OwnerName* \[ In\]
</dt> <dd>

Besitzername für die RR.

</dd> <dt>

*RecordClass* \[ in, optional\]
</dt> <dd>

Klasse der RR. Der Standardwert ist 1. Die folgenden Werte sind gültig.



| Wert                                                                                                | Bedeutung                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | IN (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CHAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

*Gültigkeitsdauer* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, in der die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*MappingFlag* \[ In\]
</dt> <dd>

WINS-Zuordnungsflag, das angibt, ob der Datensatz in die Zonenreplikation eingeschlossen werden muss. Sie kann nur zwei Werte aufweisen: 0x80000000 und 0x00010000 entsprechend den Replikationsflags bzw. Flags ohne Replikation (lokaler Datensatz). Die folgenden Werte sind gültig.



| Wert                                                                                                                                               | Bedeutung                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="0x80000000"></span><span id="0X80000000"></span><dl> <dt>**0x80000000**</dt> </dl> | Replikationsflag<br/>                   |
| <span id="0x00010000"></span><span id="0X00010000"></span><dl> <dt>**0x00010000**</dt> </dl> | Flag "No-Replication (local record)" (Keine Replikation (lokaler Datensatz))<br/> |



 

</dd> <dt>

*LookupTimeout* \[ In\]
</dt> <dd>

Zeit in Sekunden, in der ein DNS-Server versucht, die Auflösung mithilfe der WINS-Suche zu lösen.

</dd> <dt>

*CacheTimeout* \[ In\]
</dt> <dd>

Zeit in Sekunden, in der ein DNS-Server, der WINS Look up verwendet, die Antwort des WINS-Servers zwischenspeichern kann.

</dd> <dt>

*WinsServers* \[ In\]
</dt> <dd>

Liste der durch Kommas getrennten IP-Adressen von WINS-Servern, die in WINS-Suchläufen verwendet werden.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Verweis auf das neue Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\Stamm-MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS \_ WINSType**](microsoftdns-winstype.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ WINSType-Klasse**](microsoftdns-winstype-modify.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





