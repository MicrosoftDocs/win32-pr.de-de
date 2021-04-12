---
description: Der SNMP-Anbieter verwendet bei der Zuordnung von MIB-Objekt Definitionen zu CIM-Klassendefinitionen die folgenden CIM-Klassen Qualifizierer.
ms.assetid: 458167dc-562e-47b8-8760-797ae13f9459
ms.tgt_platform: multiple
title: CIM-Klassen Qualifizierer für MIB-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60fe97debc7fd81b48a6daf0f5a955374546458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217747"
---
# <a name="cim-class-qualifiers-for-mib-objects"></a>CIM-Klassen Qualifizierer für MIB-Objekte

Der SNMP-Anbieter verwendet bei der Zuordnung von MIB-Objekt Definitionen zu CIM-Klassendefinitionen die folgenden CIM-Klassen Qualifizierer. Ein obligatorischer Qualifizierer muss vorhanden sein, damit der SNMP-Anbieter ein Gruppen Objekt vollständig auflösen muss. Wenn Sie keinen obligatorischen Qualifizierer definieren, wird ein Fehler zurückgegeben. Wenn Sie einen ungültigen qualifiziererwert angeben, wird auch ein Fehler

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 



| Qualifizierer           | BESCHREIBUNG                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Beschreibung**     | **Zeichenfolge** Optionale<br/> Die Beschreibung der Klasse.<br/>                                                                      |
| **Group \_ objectID** | **Zeichenfolge** Obligatorisch, wenn die Klasse für den SNMP-Klassen Anbieter vorgesehen ist.<br/> Der Objekt Bezeichner der fabricollection.<br/> |
| **Modul \_ Importe** | **Zeichenfolge** Optionale<br/> Durch Trennzeichen getrennte Liste von MIB-Modulnamen, die zum Auflösen von Importen verwendet werden.<br/>                              |
| **\_Modulname**    | **Zeichenfolge** Optionale<br/> Der Identitäts Name eines MIB-Moduls.<br/>                                                                 |
| **Verweis**       | **Zeichenfolge** Optionale<br/> Verweist auf ein anderes Dokument, das weitere Informationen zur-Klasse enthält.<br/>                     |
| **Singleton**       | **Bool** Obligatorisch für Klassen, die aus skalaren Auflistungen zugeordnet sind.<br/> Gibt eine Klasse an, die nur eine Instanz aufweisen kann.<br/>  |



 

 

 




