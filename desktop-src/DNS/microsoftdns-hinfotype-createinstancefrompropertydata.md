---
title: CreateInstanceFromPropertyData-Methode der MicrosoftDNS_HINFOType-Klasse
description: Die CreateInstanceFromPropertyData-Methode instanziiert einen HINFO-Ressourceneintrag (Host Information).
ms.assetid: dfc11ae8-5013-4b48-a1e9-78566dc32297
keywords:
- CreateInstanceFromPropertyData-Methode DNS
- CreateInstanceFromPropertyData-Methode DNS, MicrosoftDNS_HINFOType-Klasse
- MicrosoftDNS_HINFOType-Klasse DNS, CreateInstanceFromPropertyData-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e47c2f5795b1099e1e3dfafbfa27fdfe833ae6e2fae0608be173b59dce7120
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433050"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_hinfotype-class"></a>CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ HINFOType-Klasse

Die **CreateInstanceFromPropertyData-Methode** instanziiert einen HINFO-Ressourceneintrag (Host Information).

## <a name="syntax"></a>Syntax


```mof
void CreateInstanceFromPropertyData(
  [in]           string                 DnsServerName,
  [in]           string                 ContainerName,
  [in]           string                 OwnerName,
  [in, optional] uint32                 RecordClass = 1,
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
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

Der Name des Containers für die Zone-, Cache- oder RootHints-Instanz, die diese RR enthält.

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

*CPU* \[ in, optional\]
</dt> <dd>

CPU-Typ des Datensatzbesitzers.

</dd> <dt>

*Betriebssystem* \[ in, optional\]
</dt> <dd>

Betriebssystem des Datensatzbesitzers.

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



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**MicrosoftDNS \_ HINFOType**](microsoftdns-hinfotype.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ HINFOType-Klasse**](microsoftdns-hinfotype-modify.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





