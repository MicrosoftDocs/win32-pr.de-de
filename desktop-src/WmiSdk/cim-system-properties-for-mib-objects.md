---
description: WMI definiert eine Reihe von Systemeigenschaften, die neben klassenspezifischen Eigenschaften allen Klassen und Instanzen von Klassen zugeordnet sind.
ms.assetid: ea8ca4e4-9969-48fc-9b9f-5a5c8442006d
ms.tgt_platform: multiple
title: CIM-System Eigenschaften für MIB-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0425afecc399c3cd1399e8bf565908b1c7c5d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362279"
---
# <a name="cim-system-properties-for-mib-objects"></a>CIM-System Eigenschaften für MIB-Objekte

WMI definiert eine Reihe von Systemeigenschaften, die neben klassenspezifischen Eigenschaften allen Klassen und Instanzen von Klassen zugeordnet sind.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

Der SNMP-Anbieter verwendet die folgenden CIM-Systemeigenschaften bei der Zuordnung von MIB-Objekt Definitionen zu CIM-Klassendefinitionen. Erforderliche Eigenschaften müssen vorhanden sein, damit der SNMP-Anbieter ein Gruppen Objekt vollständig auflösen muss. Wenn Sie eine obligatorische Eigenschaft nicht definieren, wird ein Fehler zurückgegeben.



<table>
<thead>
<tr class="header">
<th>Eigenschaft</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>__CLASS</strong></td>
<td><strong>Zeichenfolge</strong> Verpflich<br/> Für-Instanzen die Klasse, zu der das Objekt gehört. Bei Klassen ist dies der Klassenname.<br/></td>
</tr>
<tr class="even">
<td><strong>__DYNASTY</strong></td>
<td><strong>Zeichenfolge</strong> Optionale<br/> Der Name der Klasse, bei der es sich um die ultimative Basisklasse für das aktuelle Objekt handelt (nicht um seine unmittelbare übergeordnete Klasse).<br/></td>
</tr>
<tr class="odd">
<td><strong>__GENUS</strong></td>
<td><strong>UInt32</strong> Verpflich<br/> Typ des Objekts. Gültige Werte:<br/> <dl> 1 = Klasse<br />
2 = Instanz<br />
</dl></td>
</tr>
<tr class="even">
<td><strong>__NAMESPACE</strong></td>
<td><strong>Zeichenfolge</strong> Verpflich<br/> Der Namespace, in dem sich das Objekt befindet.<br/></td>
</tr>
<tr class="odd">
<td><strong>__PATH</strong></td>
<td><strong>Zeichenfolge</strong> Verpflich<br/> Absoluter Pfad zum Objekt.<br/></td>
</tr>
<tr class="even">
<td><strong>__PROPERTYCOUNT</strong></td>
<td><strong>UInt32</strong> Verpflich<br/> Anzahl der nicht-Systemeigenschaften, die für das Objekt definiert sind.<br/></td>
</tr>
<tr class="odd">
<td><strong>__RELPATH</strong></td>
<td><strong>Zeichenfolge</strong> Verpflich<br/> Relativer Pfad zum Objekt.<br/></td>
</tr>
<tr class="even">
<td><strong>__SERVER</strong></td>
<td><strong>Zeichenfolge</strong> Verpflich<br/> Server, der das Objekt bereitstellt.<br/></td>
</tr>
<tr class="odd">
<td><strong>__SUPERCLASS</strong></td>
<td><strong>Zeichenfolge</strong> Optionale<br/> Unmittelbar übergeordnete Klasse des Objekts.<br/></td>
</tr>
</tbody>
</table>



 

 

 




