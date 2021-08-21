---
title: CreateInstanceFromPropertyData-Methode der MicrosoftDNS_WINSRType-Klasse
description: Die CreateInstanceFromPropertyData-Methode instanziiert einen WINS Reverse Lookup(WINSR)-Ressourceneintrag.
ms.assetid: e14e81be-fc5c-4a6f-b6d1-cb3ce5005e00
keywords:
- CreateInstanceFromPropertyData-Methode DNS
- CreateInstanceFromPropertyData-Methode DNS , MicrosoftDNS_WINSRType-Klasse
- MicrosoftDNS_WINSRType-Klasse DNS, CreateInstanceFromPropertyData-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8bc5103c9a7034b79500496cc7a066c1fbc65aa32d20dd29ea3160dfbaf0ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162941"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_winsrtype-class"></a>CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ WINSRType-Klasse

Die **CreateInstanceFromPropertyData-Methode** instanziiert einen WINS Reverse Lookup(WINSR)-Ressourceneintrag.

## <a name="syntax"></a>Syntax


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in]           uint32                 MappingFlag,
  [in]           uint32                 LookupTimeout,
  [in]           uint32                 CacheTimeout,
  [in]           string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
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

WINSR-Zuordnungsflag, das angibt, ob der Datensatz in die Zonenreplikation eingeschlossen werden muss. Sie kann nur zwei Werte aufweisen: 0x80000000 und 0x00010000 entsprechend den Replikationsflags bzw. Flags ohne Replikation (lokaler Datensatz).

</dd> <dt>

*LookupTimeout* \[ In\]
</dt> <dd>

Time out in Sekunden für einen DNS-Server mit WINS Reverse Look up.

</dd> <dt>

*CacheTimeout* \[ In\]
</dt> <dd>

Die Zeit in Sekunden, die ein DNS-Server mit WINS-Suche verwendet, kann die Antwort des WINS-Servers zwischenspeichern.

</dd> <dt>

*ResultDomain* \[ In\]
</dt> <dd>

Domänenname, der an zurückgegebene NetBIOS-Namen angefügt werden soll.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Verweis auf das neue Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\Stamm-MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ WINSRType-Klasse**](microsoftdns-winsrtype-modify.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





