---
title: MicrosoftDNS_Statistic-Klasse
description: Die MicrosoftDNS- \_ Statistik Klasse stellt eine einzelne DNS-Server Statistik dar.
ms.assetid: 49ee79d6-b93f-4a9b-8054-1ad290d092d6
keywords:
- DNS-MicrosoftDNS_Statistic Klasse
- DNS-MicrosoftDNS_Statistic Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_Statistic
- MicrosoftDNS_Statistic.DnsServerName
- MicrosoftDNS_Statistic.CollectionName
- MicrosoftDNS_Statistic.CollectionId
- MicrosoftDNS_Statistic.Name
- MicrosoftDNS_Statistic.Value
- MicrosoftDNS_Statistic.StringValue
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77e26f1738c046e446fa898c4fdff2f6e8855730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040884"
---
# <a name="microsoftdns_statistic-class"></a>MicrosoftDNS- \_ Statistik Klasse

Die **MicrosoftDNS- \_ Statistik** Klasse stellt eine einzelne DNS-Server Statistik dar.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_Statistic
{
  string DnsServerName;
  string CollectionName;
  uint32 CollectionId;
  string Name;
  uint32 Value;
  string StringValue;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS- \_ Statistik** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS- \_ Statistik** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Sammlungs**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Numerische Darstellung von **CollectionName**.

</dd> <dt>

**CollectionName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Sammlung, zu der die Statistik gehört.

</dd> <dt>

**Dnsservername**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den voll qualifizierten Namen oder die IP-Adresse des DNS-Servers an, der die Statistik enthält.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Statistik.

</dd> <dt>

**StringValue**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Zeichen folgen Wert der Statistik, der nur verwendet wird, wenn der Statistik Wert nicht als DWORD dargestellt wird.

</dd> <dt>

**Wert**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Numerischer Wert der Statistik, dargestellt als DWORD.

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

[MicrosoftDNS \_ statisticcollection](microsoftdns-statisticcollection.md)
</dt> </dl>

 

 





