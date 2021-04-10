---
title: MicrosoftDNS_AFSDBType-Klasse
description: Die Unterklasse von MicrosoftDNS \_ resourcerecord, die einen AFSDB-Datensatz (Andrew File System Database Server) darstellt.
ms.assetid: 536f4df7-bd01-458b-b8f1-36f066e9ca04
keywords:
- DNS-MicrosoftDNS_AFSDBType Klasse
- DNS-MicrosoftDNS_AFSDBType Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType.CreateInstanceFromPropertyData
- MicrosoftDNS_AFSDBType.Modify
- MicrosoftDNS_AFSDBType.Subtype
- MicrosoftDNS_AFSDBType.ServerName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 836de50f4da9e613fb3e940b90971f38a634c804
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040624"
---
# <a name="microsoftdns_afsdbtype-class"></a>MicrosoftDNS \_ afsdbtype-Klasse

Die Unterklasse von [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) , die einen AFSDB-Datensatz (Andrew File System Database Server) darstellt.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_AFSDBType : MicrosoftDNS_ResourceRecord
{
  uint16 Subtype;
  string ServerName;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ afsdbtype** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ afsdbtype** -Klasse verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **"Kreateinzustancefrompropertydata"** | Instanziiert einen AFSDB-Ressourcen Eintrag auf der Grundlage der Daten in den Eingabe Parametern der Methode: DNS-Servername des Datensatzes, Container Name, Besitzer/Zellen Name, Klasse (Standard = in), Time-to-Live-Wert und Host-AFS-Server Untertyp und-Name. Gibt einen Verweis auf das neue-Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: implementiert, statisch<br/> |
| **Modify**                         | Diese Methode aktualisiert die TTL-, Untertyp-und Server Namen auf die Werte, die als Eingabeparameter dieser Methode angegeben werden. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die-Methode gibt einen Verweis auf das geänderte-Objekt als Output-Parameter zurück. <br/> Qualifizierer: Implementiert<br/>   |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ afsdbtype** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein voll qualifizierter Host, der einen Host mit einem Server für die im Besitzer Namen angegebene AFS-Zelle angibt.

</dd> <dt>

**Untertyp**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Untertyp des Host-AFS-Servers. Für den Untertyp 1 (Wert = 1) verfügt der Host über einen mespeicherort-Server der Version 3,0 für die benannte AFS-Zelle. Im Fall von Untertyp 2 (Wert = 2) verfügt der Host über einen authentifizierten Namen Server, der den Zellen Stammverzeichnis-Knoten für die benannte DCE/NCA-Zelle enthält.

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

[**Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ afsdbtype-Klasse**](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ afsdbtype-Klasse**](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





