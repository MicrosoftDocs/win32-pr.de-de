---
title: MicrosoftDNS_AFSDBType-Klasse
description: Unterklasse von MicrosoftDNS \_ ResourceRecord, die einen AFSDB-Datensatz (Andrew File System Database Server) darstellt.
ms.assetid: 536f4df7-bd01-458b-b8f1-36f066e9ca04
keywords:
- dns-Klasse MicrosoftDNS_AFSDBType
- MicrosoftDNS_AFSDBType Dns-Klasse beschrieben
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
ms.openlocfilehash: 74c7887d51e58b8c34374ed5ca96d0206472155872ba573b7b9f8879329910f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815700"
---
# <a name="microsoftdns_afsdbtype-class"></a>MicrosoftDNS \_ AFSDBType-Klasse

Unterklasse von [**MicrosoftDNS \_ ResourceRecord,**](microsoftdns-resourcerecord.md) die einen AFSDB-Datensatz (Andrew File System Database Server) darstellt.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_AFSDBType : MicrosoftDNS_ResourceRecord
{
  uint16 Subtype;
  string ServerName;
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ AFSDBType-Klasse** verfügt über folgende Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ AFSDBType-Klasse** verfügt über diese Methoden.



| Methode                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Instanziiert einen AFSDB-Ressourceneintrag basierend auf den Daten in den Eingabeparametern der Methode: DNS-Servername des Eintrags, Containername, Besitzer-/Zellenname, Klasse (Standard = IN), Wert für Lebzeit und Untertyp und Name des Host-AFS-Servers. Gibt einen Verweis auf das neue Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: Implementiert, statisch<br/> |
| **Änderung**                         | Diese Methode aktualisiert TTL, Untertyp und Servername auf die Werte, die als Eingabeparameter dieser Methode angegeben sind. Wenn kein neuer Wert für einen Parameter angegeben wird, wird der aktuelle Wert für den Parameter nicht geändert. Die -Methode gibt einen Verweis auf das geänderte Objekt als Ausgabeparameter zurück. <br/> Qualifizierer: Implementiert<br/>   |



 

### <a name="properties"></a>Eigenschaften

Die **MicrosoftDNS \_ AFSDBType-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

FQDN, der einen Host angibt, der über einen Server für die im Besitzernamen angegebene AFS-Zelle verfügt.

</dd> <dt>

**Untertyp**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Untertyp des Host-AFS-Servers. Für den Untertyp 1 (wert=1) verfügt der Host über einen AFS-Volumespeicherortserver der Version 3.0 für die benannte AFS-Zelle. Im Fall von Untertyp 2 (wert=2) verfügt der Host über einen authentifizierten Namenserver, der den Zellenstammverzeichnisknoten für die benannte DCE/NCA-Zelle enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\Stamm-MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ AFSDBType-Klasse**](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ AFSDBType-Klasse**](microsoftdns-afsdbtype-modify.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





