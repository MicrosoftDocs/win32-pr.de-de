---
title: CreateInstanceFromPropertyData-Methode der MicrosoftDNS_ATMAType-Klasse
description: Die CreateInstanceFromPropertyData-Methode instanziiert einen ATMA-Ressourcendatensatz (ATM Address to Name).
ms.assetid: 0f3270fe-40d0-43f7-b4fc-95d96f9dd9f9
keywords:
- CreateInstanceFromPropertyData-Methode DNS
- CreateInstanceFromPropertyData-Methode DNS , MicrosoftDNS_ATMAType-Klasse
- MicrosoftDNS_ATMAType DNS-Klasse, CreateInstanceFromPropertyData-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44edf3428087da73f5ba89c32232af0ae589bc0d865642ec04953c62e16404e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539320"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atmatype-class"></a>CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ ATMAType-Klasse

Die **CreateInstanceFromPropertyData-Methode** instanziiert einen ATMA-Ressourcendatensatz (ATM Address to Name).

## <a name="syntax"></a>Syntax


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint16                Format,
  [in]           string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
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

*Formatieren* \[ In\]
</dt> <dd>

ATM-Adressformat. Zwei mögliche Werte für FORMAT sind: 0 , das das Format der ATM-Endsystemadresse (ATM End System Address, AESA) angibt, und 1 das E.164-Format.

</dd> <dt>

*ATMAddress* \[ In\]
</dt> <dd>

Zeichenfolge variabler Länge von Oktetten, die die ATM-Adresse des Knotens/Besitzers enthalten, auf den sich diese RR bezieht. Die ersten vier Bytes des Arrays werden verwendet, um die Größe der Oktettzeichenfolge zu speichern. Das wichtigste Byte wird in Byte 0 gespeichert.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS \_ ATMAType**](microsoftdns-atmatype.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ ATMAType-Klasse**](microsoftdns-atmatype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





