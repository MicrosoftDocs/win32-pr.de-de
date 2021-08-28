---
description: Jede MIB-Objektdefinition enthält entweder eine ACCESS-Klausel (SNMPv1) oder eine MAX-ACCESS-Klausel (SNMPv2C), die die Zugriffsrechte für das Objekt definiert.
ms.assetid: c3b8d65b-c1ca-4131-baf4-1aab54451180
ms.tgt_platform: multiple
title: ACCESS- und MAX-ACCESS-Klauseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 985b4bfe968841436cedd352a01a609aac6ba2d725887b6a638ffcd95656935d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120940"
---
# <a name="access-and-max-access-clauses"></a>ACCESS- und MAX-ACCESS-Klauseln

Jede MIB-Objektdefinition enthält entweder eine ACCESS-Klausel (SNMPv1) oder eine MAX-ACCESS-Klausel (SNMPv2C), die die Zugriffsrechte für das Objekt definiert.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

 

In der folgenden Tabelle ist die Zuordnung der SNMPv1 ACCESS-Klausel aufgeführt.



| MIB ACCESS-Klausel | CIM-Qualifizierer       |
|-------------------|---------------------|
| schreibgeschützt         | **Lesen**            |
| Lese-/Schreibzugriff        | **Lesen,** **Schreiben** |
| Lesegeschützte        | **Schreiben**           |
| Nicht zugänglich    | **Nicht \_ zugänglich** |



 

Die folgende Tabelle enthält die Zuordnung der SNMPv2C MAX-ACCESS-Klausel.



| MIB-ACCESS-Klausel     | CIM-Qualifizierer       |
|-----------------------|---------------------|
| schreibgeschützt             | **Lesen**            |
| Lese-/Schreibzugriff            | **Lesen,** **Schreiben** |
| read-create           | **Lesen**            |
| accessible-for-notify | **Nicht \_ zugänglich** |
| Nicht zugänglich        | **Nicht \_ zugänglich** |



 

Wenn ein MIB-Objekt nicht zugänglich zugeordnet wird und keine schlüsselbasierte Eigenschaft der -Klasse ist, gibt es keine Zuordnung des MIB-Objekts selbst.

 

 



