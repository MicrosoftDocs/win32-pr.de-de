---
title: MicrosoftDNS_ATMAType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die den Atma-Datensatz (ATM Address to Name) darstellt.
ms.assetid: 3e9e4032-08a0-4a2e-bcff-f461b69a44d4
keywords:
- DNS-MicrosoftDNS_ATMAType Klasse
- DNS-MicrosoftDNS_ATMAType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
- MicrosoftDNS_ATMAType.Modify
- MicrosoftDNS_ATMAType.Format
- MicrosoftDNS_ATMAType.ATMAddress
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 237dc4ecb657e79e835abcfdacf90844fb05c5b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956474"
---
# <a name="microsoftdns_atmatype-class"></a>MicrosoftDNS \_ atmatype-Klasse

Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die den Atma-Datensatz (ATM Address to Name) darstellt.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_ATMAType : MicrosoftDNS_ResourceRecord
{
  uint16 Format;
  string ATMAddress;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ atmatype** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ atmatype** -Klasse verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                        |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **"Kreateinzustancefrompropertydata"** | Instanziiert einen Atma-Ressourcen Eintrag auf der Grundlage der Daten in den Eingabe Parametern der Methode: dem DNS-Server Namen des Datensatzes, dem Container Namen, dem Besitzer/Knoten Namen, der Klasse (Standard = in), dem Wert für die Gültigkeitsdauer und dem ATM-Format und der Adresse. Gibt einen Verweis auf das neue-Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: implementiert, statisch<br/> |
| **Modify**                         | Aktualisiert die TTL, das Format und die Atma-Adresse auf die Werte, die als Eingabeparameter dieser Methode angegeben sind. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück. <br/> Qualifizierer: Implementiert<br/>         |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ atmatype** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Atmaddress**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Zeichenfolge mit variabler Länge von Oktetten, die die ATM-Adresse des Knotens bzw. Besitzers enthält, auf den sich diese RR bezieht. Die ersten 4 Bytes des Arrays werden verwendet, um die Größe der Oktett-Zeichenfolge zu speichern. Das signifikanteste Byte wird in Byte 0 gespeichert.

</dd> <dt>

**Format**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

ATM-Adressformat. Gültige Werte sind: 0, was das AESA-Format (ATM End System Address) angibt, und 1 gibt das E. 164-Format an.

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

[**Methode "kreateinzustancefrompropertydata" der MicrosoftDNS \_ atmatype-Klasse**](microsoftdns-atmatype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ atmatype-Klasse**](microsoftdns-atmatype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





