---
title: MicrosoftDNS_MINFOType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen e-Mail-Informations Eintrag (MINFO) darstellt.
ms.assetid: 9c4b70b8-f9cf-4dea-8d2d-43e0de002d52
keywords:
- DNS-MicrosoftDNS_MINFOType Klasse
- DNS-MicrosoftDNS_MINFOType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType
- MicrosoftDNS_MINFOType.CreateInstanceFromPropertyData
- MicrosoftDNS_MINFOType.Modify
- MicrosoftDNS_MINFOType.ResponsibleMailbox
- MicrosoftDNS_MINFOType.ErrorMailbox
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a7d230db9da32ce47cd4cfaf99c4978c4e63385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105938"
---
# <a name="microsoftdns_minfotype-class"></a>MicrosoftDNS- \_ minfotype-Klasse

Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen e-Mail-Informations Eintrag (MINFO) darstellt.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_MINFOType : MicrosoftDNS_ResourceRecord
{
  string ResponsibleMailbox;
  string ErrorMailbox;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS- \_ minfotype** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS- \_ minfotype** -Klasse verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **"Kreateinzustancefrompropertydata"** | Instanziiert einen MINFO-Typ von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: der DNS-Server Name des Datensatzes, der Container Name, der Besitzer Name des e-Mail-Listen/-Felds, die Klasse (Standard = in), der Wert für die Gültigkeitsdauer und die entsprechenden Postfächer. Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben. <br/> Qualifizierer: implementiert, statisch<br/> |
| **Modify**                         | Diese Methode aktualisiert die TTL, das verantwortliche Postfach und das Fehler Postfach auf die Werte, die als Eingabeparameter dieser Methode angegeben werden. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück. <br/> Qualifizierer: Implementiert<br/>    |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS- \_ minfotype** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Errormailbox**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

FQDN, der ein Postfach für den Empfang von Fehlermeldungen in Bezug auf die Mailingliste oder das Postfach angibt, das durch den Besitzer Namen des MINFO-Datensatzes angegeben wird.

</dd> <dt>

**"Verantworblemailbox"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der voll qualifizierte Name ist ein Postfach, das für die Mailingliste oder das Postfach zuständig ist, die im Besitzer Namen des Datensatzes angegeben sind.

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

[**Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ minfotype-Klasse**](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS- \_ minfotype-Klasse**](microsoftdns-minfotype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





