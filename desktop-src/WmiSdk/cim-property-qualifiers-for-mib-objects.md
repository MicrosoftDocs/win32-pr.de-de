---
description: Der SNMP-Anbieter verwendet bei der Zuordnung von MIB-Objekt Definitionen zu CIM-Klassendefinitionen die folgenden CIM-Eigenschaften Qualifizierer.
ms.assetid: 6e858e7e-5c46-4350-9696-c5efa1252c00
ms.tgt_platform: multiple
title: CIM-Eigenschaften Qualifizierer für MIB-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f2a25edf9c15930202d3c8cf79d3d62b0d1dd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217743"
---
# <a name="cim-property-qualifiers-for-mib-objects"></a>CIM-Eigenschaften Qualifizierer für MIB-Objekte

Der SNMP-Anbieter verwendet bei der Zuordnung von MIB-Objekt Definitionen zu CIM-Klassendefinitionen die folgenden CIM-Eigenschaften Qualifizierer. Ein obligatorischer Qualifizierer muss vorhanden sein, damit der SNMP-Anbieter ein MIB-Objekt vollständig auflösen muss. Wenn Sie keinen obligatorischen Qualifizierer definieren, wird ein Fehler zurückgegeben. Wenn Sie einen ungültigen qualifiziererwert angeben, wird auch ein Fehler

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 



| Qualifizierer                          | BESCHREIBUNG                                                                                                                                                                                            |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bits**                           | **Zeichenfolge** Obligatorisch, wenn der **Text \_ Konventionen** -Qualifizierer nicht gleich Bits ist.<br/> Enumerationswerte für die Untertyp Definition eines Bits.<br/>                                        |
| **CimType**                        | **Zeichenfolge** Verpflich<br/> CIM-Textdarstellung, die einen zugrunde liegenden CIM-Protokoll Wert formatiert.<br/>                                                                                    |
| **Defval**                         | **Zeichenfolge** Optionale<br/> Der Standardwert des Objekts.<br/>                                                                                                                                       |
| **Beschreibung**                    | **Zeichenfolge** Optionale<br/> Eine Beschreibung des Objekts.<br/>                                                                                                                                    |
| **Anzeige \_ Hinweis**                  | **Zeichenfolge** Optionale<br/> Die Art und Weise, in der die Daten des Objekts für einen Benutzer angezeigt werden sollen.<br/>                                                                                                    |
| **Codieren**                       | **Zeichenfolge** Optionale<br/> Der beim Codieren von SNMPv1-und SNMPv2C-Protokoll Rahmen verwendete SNMP-Typ.<br/>                                                                                              |
| **Enumeration**                    | **Zeichenfolge** Obligatorisch, wenn der **Text \_ Konventionen** -Qualifizierer nicht gleich enumeratedinteger ist.<br/> Enumerationswerte für eine enumerierte ganzzahlige unter Typdefinition.<br/>                  |
| **Länge mit fester \_ Länge**                  | **UInt32** Optionale<br/> Wert mit fester Länge.<br/>                                                                                                                                           |
| [**Wichtigen**](standard-qualifiers.md) | **Bool** Optionale<br/> Schlüsseleigenschaft einer Klassendefinition.<br/>                                                                                                                             |
| **Schlüssel \_ Reihenfolge**                     | **UInt32** Optional, es sei denn, [**Key**](standard-qualifiers.md) wird angegeben.<br/> Die Reihenfolge der Schlüsseleigenschaft in der Klassendefinition.<br/>                                                   |
| **Name**                           | **Zeichenfolge** Verpflich<br/> Impliziter Name der Eigenschaft. Beachten Sie, dass dieser Qualifizierer nicht explizit definiert ist.<br/>                                                                           |
| **Objekt \_ Bezeichner**             | **Zeichenfolge** Verpflich<br/> Der MIB-Objekt Bezeichner des Objekts.<br/>                                                                                                                              |
| **Objekt \_ Syntax**                 | **Zeichenfolge** Optionale<br/> Die benannte Typdefinition des Objekts.<br/>                                                                                                                               |
| **Lesen**                           | **Bool** Optional (mindestens ein **Lese** -oder **Schreibvorgang** muss angegeben werden)<br/> Gewährt Lesezugriff auf das-Objekt.<br/>                                                                     |
| **Verweis**                      | **Zeichenfolge** Optionale<br/> Verweist auf ein anderes Dokument, das weitere Informationen zum-Objekt enthält.<br/>                                                                                   |
| **Status**                         | **Zeichenfolge** Optionale<br/> Gibt an, ob das Objekt unterstützt werden muss.<br/>                                                                                                               |
| **Text \_ Konvention**            | **Zeichenfolge** Verpflich<br/> Textdarstellung der Syntax Klausel des MIB [-ObjektType-](object-type-macro.md) Makros.<br/>                                                           |
| **Einheiten**                          | **Zeichenfolge** Optionale<br/> Genaue Definition des Objekts, das das Objekt darstellt.<br/>                                                                                                             |
| **Variable \_ Länge**               | **Zeichenfolge** Optionale<br/> Minimale, maximale und Werte fester Länge, die der Typdefinition des Objekts zugeordnet sind.<br/>                                                                       |
| **Variablen \_ Wert**                | **Zeichenfolge** Optionale<br/> Bereichs-und Fixed-Werte, die der Typdefinition des Objekts zugeordnet sind.<br/>                                                                                         |
| **Virtueller \_ Schlüssel**                   | **Bool** Optionale<br/> Gibt an, dass der Wert der Eigenschaft auf der supermenge der Instanzinformationen basieren soll, die allen zugänglichen MIB-Objekten in der Klassendefinition zugeordnet sind.<br/> |
| **Schreiben**                          | **Bool** Optional (mindestens ein **Lese** -oder **Schreibvorgang** muss angegeben werden)<br/> Gewährt Schreibzugriff auf das-Objekt.<br/>                                                                    |



 

 

 




