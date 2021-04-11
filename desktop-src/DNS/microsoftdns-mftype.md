---
title: MicrosoftDNS_MFType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen e-Mail-Weiterleitungs-Agent für einen Domänen Eintrag (MF) darstellt.
ms.assetid: 0ba0fddd-c316-4a5b-ad65-6344dbe949c1
keywords:
- DNS-MicrosoftDNS_MFType Klasse
- DNS-MicrosoftDNS_MFType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType
- MicrosoftDNS_MFType.CreateInstanceFromPropertyData
- MicrosoftDNS_MFType.Modify
- MicrosoftDNS_MFType.MFHost
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e030f695e95ee736b1c53a345201e0bd1addfe3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104739"
---
# <a name="microsoftdns_mftype-class"></a>MicrosoftDNS- \_ mftype-Klasse

Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen e-Mail-Weiterleitungs-Agent für einen Domänen Eintrag (MF) darstellt.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_MFType : MicrosoftDNS_ResourceRecord
{
  string MFHost;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS- \_ mftype** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS- \_ mftype** -Klasse verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                            |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **"Kreateinzustancefrompropertydata"** | Diese Methode instanziiert den MF-Typ RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer Namen der Domäne, der Klasse (Standard = in), dem Gültigkeitsdauer Wert und dem Host des Mail-Agents. Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben. <br/> Qualifizierer: implementiert, statisch<br/> |
| **Modify**                         | Diese Methode aktualisiert den TTL-und den MF-Host auf die Werte, die als Eingabeparameter dieser Methode angegeben werden. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück. <br/> Qualifizierer: Implementiert<br/>                         |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS- \_ mftype** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**MF-Host**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

FQDN, der einen Host mit einem e-Mail-Agent angibt, der e-Mail für die Weiterleitung an die angegebene Domäne akzeptiert.

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

[**Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ Klasse "mftype"**](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ mftype-Klasse**](microsoftdns-mftype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





