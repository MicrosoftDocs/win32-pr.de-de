---
title: MicrosoftDNS_RootHints-Klasse
description: Die MicrosoftDNS- \_ Klasse roothints beschreibt die in einer Cache Datei auf einem DNS-Server gespeicherten roothints. Diese Klasse vereinfacht die Visualisierung der Kapselung von DNS-Objekten, anstatt ein reales Objekt darzustellen.
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- DNS-MicrosoftDNS_RootHints Klasse
- DNS-MicrosoftDNS_RootHints Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints.WriteBackRootHintDatafile
- MicrosoftDNS_RootHints.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d69b737efaeb18058151b3e785270775d8af0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104157"
---
# <a name="microsoftdns_roothints-class"></a>MicrosoftDNS- \_ Klasse "roothints"

Die **MicrosoftDNS-Klasse \_ roothints** beschreibt die in einer Cache Datei auf einem DNS-Server gespeicherten roothints. Diese Klasse vereinfacht die Visualisierung der Kapselung von DNS-Objekten, anstatt ein reales Objekt darzustellen.

**MicrosoftDNS \_ Roothints** ist ein Container für die Ressourcen Datensätze, die vom DNS-Server in einer Cache Datei gespeichert werden. Jede Instanz der **MicrosoftDNS-Klasse \_ roothints** muss genau einem DNS-Server zugewiesen werden. Sie ist möglicherweise mehreren Instanzen der [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) -Klasse zugeordnet.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS-Klasse \_ roothints** verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS-Klasse \_ roothints** verfügt über diese Methoden.



| Methode                        | BESCHREIBUNG                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| **Getchilshedname**      | Ruft den Distinguished Name für die Zone ab. <br/> Qualifizierer: Implementiert<br/>   |
| **"Schreibbackroothintdatafile"** | Schreibt die roothints zurück in die DNS-Cache Datei. <br/> Qualifizierer: Implementiert<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS- \_ Domäne**](microsoftdns-domain.md)
</dt> <dt>

[**"Write-backroothintdatafile"-Methode der MicrosoftDNS- \_ Klasse "roothints"**](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Klasse "roothints"**](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





