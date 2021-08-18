---
title: MicrosoftDNS_AAAAType-Klasse
description: Unterklasse von MicrosoftDNS \_ ResourceRecord, die einen AAAA-Eintrag (IPv6 Address) darstellt. Der AAAA-Eintrag wird häufig als \0034;quad-a record \ 0034; ausgesprochen.
ms.assetid: e16a7a69-18df-43dc-add9-700a702724ce
keywords:
- MicrosoftDNS_AAAAType DNS-Klasse
- MicrosoftDNS_AAAAType DNS-Klasse , beschrieben
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
ms.openlocfilehash: 90628ba4ceedffe9628aca0b96b624377ae7a8ab2351cfe6ae6b43ba8a381235
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587570"
---
# <a name="microsoftdns_aaaatype-class"></a>MicrosoftDNS \_ AAAAType-Klasse

Unterklasse von [**MicrosoftDNS \_ ResourceRecord,**](microsoftdns-resourcerecord.md) die einen AAAA-Eintrag (IPv6 Address) darstellt. Der AAAA-Eintrag wird häufig als "Quad-a-Record" ausgesprochen.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_AAAAType : MicrosoftDNS_ResourceRecord
{
  string IPv6Address;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ AAAAType-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ AAAAType-Klasse** verfügt über diese Methoden.



| Methode                             | Beschreibung                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instanziiert einen "AAAA"-Typ von RR basierend auf den Daten in den Eingabeparametern der Methode: DNS-Servername des Eintrags, Containername, Besitzer-/Hostname, Klasse (Standard = IN), Wert für Live-Datenübertragung und IPv6-Adresse. Sie gibt einen Verweis auf das neue Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: Implementiert, statisch<br/> |
| **Änderung**                         | Aktualisiert die TTL- und IPv6-Adresse auf die Werte, die als Eingabeparameter dieser Methode angegeben sind. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die -Methode gibt einen Verweis auf das geänderte Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: Implementiert<br/>      |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ AAAAType-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**IPv6Address**
</dt> <dd> <dl> <dt>

Datentyp: **string**
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
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ AAAAType-Klasse**](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ AAAAType-Klasse**](microsoftdns-aaaatype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





