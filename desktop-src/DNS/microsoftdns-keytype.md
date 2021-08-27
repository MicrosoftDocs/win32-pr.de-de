---
title: MicrosoftDNS_KEYType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ ResourceRecord, die einen KEY-Ressourcendatensatz darstellt.
ms.assetid: d3fa1f35-fa0a-47ee-b2be-4464b9b21d80
keywords:
- MicrosoftDNS_KEYType DNS-Klasse
- MicrosoftDNS_KEYType DNS-Klasse , beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
- MicrosoftDNS_KEYType.Modify
- MicrosoftDNS_KEYType.Flags
- MicrosoftDNS_KEYType.Protocol
- MicrosoftDNS_KEYType.Algorithm
- MicrosoftDNS_KEYType.PublicKey
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 279044856e695c7e287809a3cbe89a6fffbbc1c0352c0cb68ae45350aa17fc16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109130"
---
# <a name="microsoftdns_keytype-class"></a>MicrosoftDNS \_ KEYType-Klasse

Die Unterklasse von [**MicrosoftDNS \_ ResourceRecord,**](microsoftdns-resourcerecord.md) die einen KEY-Ressourcendatensatz darstellt.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_KEYType : MicrosoftDNS_ResourceRecord
{
  uint16 Flags;
  uint16 Protocol;
  uint16 Algorithm;
  string PublicKey;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ KEYType-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ KEYType-Klasse** verfügt über diese Methoden.



| Methode                             | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instanziiert einen KEY-Ressourceneintrag basierend auf den Daten in den Eingabeparametern der Methode: DNS-Servername des Eintrags, Containername, Besitzername, Klasse (Standard = IN), Time-to-Live-Wert und WINS-Zuordnungsflag, Time out für reverse look-up, WINS-Cache-Time out und Domänenname, der angefügt werden soll. Sie gibt einen Verweis auf das neue Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: Implementiert, statisch<br/> |
| **Änderung**                         | Aktualisiert die TTL, das Zuordnungsflag, das Time out für die Suche, das Cache-Time out und die Ergebnisdomäne auf die Werte, die als Eingabeparameter dieser Methode angegeben sind. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die -Methode gibt einen Verweis auf das geänderte Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: Implementiert<br/>                          |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ KEYType-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Algorithmus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Algorithmus, der mit dem im Ressourcendatensatz angegebenen Schlüssel verwendet wird. Die zugewiesenen Werte sind in der folgenden Tabelle aufgeführt.



| Wert                                                                                                | Bedeutung                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Kryptografie mit elliptischen Kurven<br/> |



 

</dd> <dt>

**Flags**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Flags, die zum Angeben der Zuordnung verwendet werden, wie in IETF RFC 2535 beschrieben.

</dd> <dt>

**Protokoll**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Protokoll, für das der im Ressourcendatensatz angegebene Schlüssel verwendet werden kann. Die zugewiesenen Werte sind in der folgenden Tabelle aufgeführt.



| Wert                                                                                                    | Bedeutung                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>     | TLS<br/>           |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>     | E-Mail<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>     | DNSSEC<br/>        |
| <span id="4"></span><dl> <dt>**4**</dt> </dl>     | IPsec<br/>         |
| <span id="255"></span><dl> <dt>**255**</dt> </dl> | Alle Protokolle<br/> |



 

</dd> <dt>

**PublicKey**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Öffentlicher Schlüssel, dargestellt in Base64, wie in Anhang A von RFC 2535 beschrieben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ KEYType-Klasse**](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ KEYType-Klasse**](microsoftdns-keytype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





