---
title: MicrosoftDNS_HINFOType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen hinfo-Datensatz darstellt.
ms.assetid: c6591010-0fe6-45b2-9032-9f847237ecf6
keywords:
- DNS-MicrosoftDNS_HINFOType Klasse
- DNS-MicrosoftDNS_HINFOType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType
- MicrosoftDNS_HINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_HINFOType.Modify
- MicrosoftDNS_HINFOType.CPU
- MicrosoftDNS_HINFOType.OS
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3298e5a7f90dbaee24e5014b1a3aab76ad6997
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339351"
---
# <a name="microsoftdns_hinfotype-class"></a>MicrosoftDNS- \_ hinfotype-Klasse

Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen hinfo-Datensatz darstellt.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_HINFOType : MicrosoftDNS_ResourceRecord
{
  string CPU;
  string OS;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS- \_ hinfotype** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS- \_ hinfotype** -Klasse verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **"Kreateinzustancefrompropertydata"** | Instanziiert eine hinfo von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: der DNS-Server Name des Datensatzes, der Container Name, der Besitzer Name, die Klasse (Standard = in), der Gültigkeitsdauer Wert und die CPU-und Betriebssystem Typen des Hosts. Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben. <br/> Qualifizierer: implementiert, statisch<br/> |
| **Modify**                         | Aktualisiert die Gültigkeitsdauer, CPU und das Betriebssystem auf die Werte, die als Eingabeparameter dieser Methode angegeben sind. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück. <br/> Qualifizierer: Implementiert<br/>          |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS- \_ hinfotype** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**CPU**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der CPU-Typ des Daten Satz Besitzers.

</dd> <dt>

**Betriebssystem**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das Betriebssystem des Daten Satz Besitzers.

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

[**Methode "kreateinstancefrompropertydata" der "hinfotype"-Klasse von MicrosoftDNS \_**](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS- \_ hinfotype-Klasse**](microsoftdns-hinfotype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





