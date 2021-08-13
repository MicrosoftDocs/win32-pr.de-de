---
title: CreateInstanceFromPropertyData-Methode der MicrosoftDNS_SRVType Klasse
description: Die CreateInstanceFromPropertyData-Methode instanziiert einen Dienstressourcendatensatz (SRV).
ms.assetid: ef55faa8-1109-4c96-98ac-2b01b940fa5c
keywords:
- CreateInstanceFromPropertyData-Methode DNS
- CreateInstanceFromPropertyData-Methode DNS , MicrosoftDNS_SRVType-Klasse
- MicrosoftDNS_SRVType DNS-Klasse, CreateInstanceFromPropertyData-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92519a3dcd383fca9297323c5217cfdefa997752ede62435b8002af5e151114f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669088"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_srvtype-class"></a>CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ SRVType-Klasse

Die **CreateInstanceFromPropertyData-Methode** instanziiert einen Dienstressourcendatensatz (SRV).

## <a name="syntax"></a>Syntax


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Priority,
  [in]           uint16               Weight,
  [in]           uint16               Port,
  [in]           string               SRVDomainName,
  [out, ref]     MicrosoftDNS_SRVType &RR
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

Name des Containers für die Zone-, Cache- oder RootHints-Instanz, die diese RR enthält.

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

*TTL* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, die die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Priorität* \[ In\]
</dt> <dd>

Die Priorität des Zielhosts, der im Besitzernamen angegeben ist. Niedrigere Zahlen setzen höhere Prioritäten voraus.

</dd> <dt>

*Gewichtung* \[ In\]
</dt> <dd>

Gewichtung des Zielhosts. Dies ist nützlich, wenn Sie hosts mit der gleichen Priorität auswählen. Die Wahrscheinlichkeit, dass dieser Host verwendet wird, sollte proportional zu seiner Gewichtung sein.

</dd> <dt>

*Port* \[ In\]
</dt> <dd>

Auf dem Zielhost eines Protokolldiensts verwendeter Port.

</dd> <dt>

*SRVDomainName* \[ In\]
</dt> <dd>

FQDN des Zielhosts. Ein Ziel von bedeutet, dass der Dienst in dieser \\ Domäne definitiv nicht verfügbar \\ ist.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Verweis auf das neue -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MicrosoftDNS \_ SRVType**](microsoftdns-srvtype.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ SRVType-Klasse**](microsoftdns-srvtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





