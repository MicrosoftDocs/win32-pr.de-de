---
description: Eine SNMP-Auflistung wird einer CIM-Klasse zugeordnet, und die Elemente einer Auflistung werden den Eigenschaften einer CIM-Klasse zugeordnet. Alle generierten CIM-Klassendefinitionen müssen von der snmpobjecttype-Klasse abgeleitet werden.
ms.assetid: e6f82fd6-e3d8-48c5-8c7b-a30a2d502f41
ms.tgt_platform: multiple
title: SNMP-Sammlungen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a85473a394ce715ff9759e974a47824e5621509f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347318"
---
# <a name="snmp-collections"></a>SNMP-Sammlungen

Eine SNMP-Auflistung wird einer CIM-Klasse zugeordnet, und die Elemente einer Auflistung werden den Eigenschaften einer CIM-Klasse zugeordnet. Alle generierten CIM-Klassendefinitionen müssen von der **snmpobjecttype** -Klasse abgeleitet werden.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

Die folgenden Klassendefinitionen übergeordnet alle generierten Klassendefinitionen:

``` syntax
[abstract]
class SnmpMacro
{
};

[abstract]
class SnmpObjectType:SnmpMacro
{
};
```

## <a name="remarks"></a>Bemerkungen

Die folgenden Regeln gelten für die Zuordnung von SNMP-Auflistungen zu CIM-Klassen. Sofern nicht anders angegeben, gelten diese Regeln sowohl für skalare als auch für Tabellen Auflistungen:

-   Der Zustellungs Prozess generiert CIM-Klassennamen durch Verkettung von "SNMP \_ ", des MIB-Modul Identitäts namens, " \_ " und des Objekt Deskriptors der Auflistung.

    Beispiel: das **System** wird in das **SNMP- \_ RFC1213 \_ MIB- \_ System** übersetzt, während **iftable** in **SNMP \_ RFC1213 \_ MIB \_ iftable** übersetzt.

-   In allen Fällen werden Bindestriche (-) in SNMP-MIB-Bezeichnerzeichen unterstrichen ( \_ ) in CIM-Klassennamen zugeordnet.
-   Namenskonflikte können auftreten, wenn die Groß-/Kleinschreibung des CIM-namens nicht beachtet wird Wenn ein Benennungs Konflikt auftritt, wählt der Anbieter eine der in Konflikt stehenden Gruppendefinitionen aus und ignoriert die restlichen Definitionen.
-   Der Identitäts Name des MIB-Moduls, das die Auflistung enthält, wird dem klassenqualifizierermodulnamen des CIM-Klasse zugeordnet. **\_**
-   Der Objekt Bezeichner der fabricollection wird der CIM-Klassen- **qualifizierergruppe \_ objectID** zugeordnet.
-   Die Importliste des MIB-Moduls (aus der Definition des **Modul-Identity-** Makros abgerufen) wird den **\_ Importen** des CIM-klassenqualifizierungsmoduls zugeordnet. Dieser Qualifizierer enthält eine durch Trennzeichen getrennte Liste von Modulnamen.

 

 



