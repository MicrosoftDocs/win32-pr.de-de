---
title: MicrosoftDNS_SRVType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen Dienst (SRV)-Datensatz darstellt.
ms.assetid: 4b36246d-4466-46d9-9267-180e43547ae6
keywords:
- DNS-MicrosoftDNS_SRVType Klasse
- DNS-MicrosoftDNS_SRVType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_SRVType
- MicrosoftDNS_SRVType.CreateInstanceFromPropertyData
- MicrosoftDNS_SRVType.Modify
- MicrosoftDNS_SRVType.Priority
- MicrosoftDNS_SRVType.Weight
- MicrosoftDNS_SRVType.Port
- MicrosoftDNS_SRVType.SRVDomainName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea955cad281e9361b4fa1ca5b033a4ca0d39719
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477265"
---
# <a name="microsoftdns_srvtype-class"></a>MicrosoftDNS- \_ srvtype-Klasse

Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen Dienst (SRV)-Datensatz darstellt.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_SRVType : MicrosoftDNS_ResourceRecord
{
  uint16 Priority;
  uint16 Weight;
  uint16 Port;
  string SRVDomainName;
};
```

## <a name="members"></a>Member

Die Klasse " **\_ srvtype" der MicrosoftDNS** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die Klasse " **\_ srvtype" der MicrosoftDNS** verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                      |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **"Kreateinzustancefrompropertydata"** | Instanziiert einen SRV-Typ von RR auf der Grundlage der Daten in den Eingabe Parametern der Methode: der DNS-Server Name des Datensatzes, der Container Name, der Besitzer/Zielname, die Klasse (Standard = in), der Wert für die Gültigkeitsdauer und die Priorität, die Gewichtung, der Port und der Domänen Name des Zielhosts. Es wird ein Verweis auf das neue-Objekt als Output-Parameter zurückgegeben. <br/> Qualifizierer: implementiert, statisch<br/> |
| **Modify**                         | Aktualisiert die TTL, Priorität, Gewichtung, den Port und den Domänen Namen auf die Werte, die als Eingabeparameter dieser Methode angegeben sind. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück. <br/> Qualifizierer: Implementiert<br/>                  |



 

### <a name="properties"></a>Eigenschaften

Die Klasse **MicrosoftDNS \_ srvtype** verfügt über diese Eigenschaften.

<dl> <dt>

**Port**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Port, der auf dem Zielhost eines Protokoll Diensts verwendet wird.

</dd> <dt>

**Priority**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Priorität des im Besitzer Namen angegebenen Zielhosts. Niedrigere Zahlen implizieren höhere Prioritäten.

</dd> <dt>

**Srvdomainname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der voll qualifizierte Namen des Zielhosts. Ein Ziel von \\ . \\ bedeutet, dass der Dienst in dieser Domäne nicht verfügbar ist.

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gewichtung des Zielhosts. Dies ist hilfreich bei der Auswahl zwischen Hosts mit der gleichen Priorität. Die Wahrscheinlichkeit, diesen Host zu verwenden, sollte proportional zu seiner Gewichtung sein.

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

[**Die Methode "kreateinstancefrompropertydata" der Klasse "srvtype" von MicrosoftDNS \_**](microsoftdns-srvtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ srvtype-Klasse**](microsoftdns-srvtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





