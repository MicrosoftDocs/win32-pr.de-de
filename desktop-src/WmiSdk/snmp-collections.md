---
description: Eine SNMP-Auflistung wird einer CIM-Klasse und die Elemente einer Auflistung den Eigenschaften einer CIM-Klasse zugeordnet. Alle generierten CIM-Klassendefinitionen müssen von der SnmpObjectType-Klasse abgeleitet werden.
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
ms.openlocfilehash: df4926ab89a6bb9a936fe5bdb27f921699bbe90a528842d81de96d8049412940
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315304"
---
# <a name="snmp-collections"></a>SNMP-Sammlungen

Eine SNMP-Auflistung wird einer CIM-Klasse und die Elemente einer Auflistung den Eigenschaften einer CIM-Klasse zugeordnet. Alle generierten CIM-Klassendefinitionen müssen von der **SnmpObjectType-Klasse** abgeleitet werden.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

 

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

## <a name="remarks"></a>Hinweise

Die folgenden Regeln gelten beim Zuordnen von SNMP-Sammlungen zu CIM-Klassen. Sofern nicht anders angegeben, gelten diese Regeln sowohl für skalare als auch für Tabellensammlungen:

-   Der Zuordnungsprozess generiert CIM-Klassennamen, indem "SNMP", \_ der Identitätsname des MIB-Moduls " " und der Objektdeskriptor der Sammlung verkettet \_ werden.

    Beispiel: **System** wird in **SNMP \_ RFC1213 \_ \_ MIB-System** übersetzt, während **ifTable** in **SNMP \_ RFC1213 \_ MIB \_ ifTable** übersetzt.

-   In allen Fällen werden Bindestriche (-) in SNMP-MIB-Bezeichnern Unterstrichen ( \_ ) in CIM-Klassennamen zugeordnet.
-   Benennungskonflikte können aufgrund der Nichtberücksichtigung der Groß-/Kleinschreibung von CIM-Namen auftreten. Wenn ein Namenskonflikt auftritt, wählt der Anbieter eine der in Konflikt geratenen Gruppendefinitionen aus und ignoriert die verbleibenden Definitionen.
-   Der Identitätsname des MIB-Moduls, das die Auflistung enthält, wird dem CIM-Klassenqualifizierer **\_ Modulname** zugeordnet.
-   Der Objektbezeichner der -Auflistung wird dem CIM-Klassenqualifizierer **Group \_ Objectid** zugeordnet.
-   Die Importliste des MIB-Moduls (aus der **MODULE-IDENTITY-Makrodefinition** abgerufen) wird dem CIM-Klassenqualifizierermodul **\_ imports** zugeordnet. Dieser Qualifizierer enthält eine durch Trennzeichen getrennte Liste von Modulnamen.

 

 



