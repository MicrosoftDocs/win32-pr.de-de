---
description: Jede MIB-Objektdefinition enthält entweder eine Access (SNMPv1)-oder eine Max-Access (SNMPv2C)-Klausel, die die Zugriffsrechte für das Objekt definiert.
ms.assetid: c3b8d65b-c1ca-4131-baf4-1aab54451180
ms.tgt_platform: multiple
title: Access-und Max-Access-Klauseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37084a25a48c874866774b990a70e1332e730103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363248"
---
# <a name="access-and-max-access-clauses"></a>Access-und Max-Access-Klauseln

Jede MIB-Objektdefinition enthält entweder eine Access (SNMPv1)-oder eine Max-Access (SNMPv2C)-Klausel, die die Zugriffsrechte für das Objekt definiert.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

In der folgenden Tabelle ist die Zuordnung der SNMPv1 Access-Klausel aufgeführt.



| MIB-Zugriffs Klausel | CIM Qualifizierer       |
|-------------------|---------------------|
| schreibgeschützt         | **Lesen**            |
| Lesen/Schreiben        | **Lesen**, **Schreiben** |
| Lesegeschützte        | **Schreiben**           |
| nicht zugänglich    | **Nicht \_ zugänglich** |



 

In der folgenden Tabelle ist die Zuordnung der SNMPv2C Max-Access-Klausel aufgeführt.



| MIB-Access-Klausel     | CIM Qualifizierer       |
|-----------------------|---------------------|
| schreibgeschützt             | **Lesen**            |
| Lesen/Schreiben            | **Lesen**, **Schreiben** |
| Lesen/Erstellen           | **Lesen**            |
| Zugriff für Benachrichtigungen | **Nicht \_ zugänglich** |
| nicht zugänglich        | **Nicht \_ zugänglich** |



 

Wenn ein MIB-Objekt nicht zugreifbar zugeordnet ist und keine Schlüssel gebundene Eigenschaft der Klasse ist, gibt es keine Zuordnung des MIB-Objekts selbst.

 

 



