---
title: MicrosoftDNS_AAAAType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen IPv6-Adresseintrag (AAAA) darstellt. Der AAAA-Datensatz hat häufig den Wert \ 0034; Quad-a Record \ 0034;.
ms.assetid: e16a7a69-18df-43dc-add9-700a702724ce
keywords:
- DNS-MicrosoftDNS_AAAAType Klasse
- DNS-MicrosoftDNS_AAAAType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType
- MicrosoftDNS_AAAAType.CreateInstanceFromPropertyData
- MicrosoftDNS_AAAAType.Modify
- MicrosoftDNS_AAAAType.IPv6Address
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0131177c342730c08868946c29356554cbfb9cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339969"
---
# <a name="microsoftdns_aaaatype-class"></a>MicrosoftDNS \_ aaaatype-Klasse

Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen IPv6-Adresseintrag (AAAA) darstellt. Der AAAA-Datensatz ist im Allgemeinen als "Quad-a-Datensatz" bezeichnet.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_AAAAType : MicrosoftDNS_ResourceRecord
{
  string IPv6Address;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ aaaatype** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ aaaatype** -Klasse verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **"Kreateinzustancefrompropertydata"** | Instanziiert einen "AAAA"-Typ von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer/Hostnamen, der Klasse (Standard = in), dem Gültigkeitsdauer Wert und der IPv6-Adresse. Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben. <br/> Qualifizierer: implementiert, statisch<br/> |
| **Modify**                         | Aktualisiert die TTL-und IPv6-Adresse auf die Werte, die als Eingabeparameter dieser Methode angegeben werden. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück. <br/> Qualifizierer: Implementiert<br/>      |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ aaaatype** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**IPv6Address**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

IPv6-Adresse für den Host.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Methode "kreateinzustancefrompropertydata" der Klasse "MicrosoftDNS \_ aaaatype"**](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ aaaatype-Klasse**](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





