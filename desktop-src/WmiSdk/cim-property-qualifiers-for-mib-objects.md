---
description: Der SNMP-Anbieter verwendet beim Zuordnen von MIB-Objektdefinitionen zu CIM-Klassendefinitionen die folgenden CIM-Eigenschaftsqualifizierer.
ms.assetid: 6e858e7e-5c46-4350-9696-c5efa1252c00
ms.tgt_platform: multiple
title: CIM-Eigenschaftsqualifizierer für MIB-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2fd45f250b603fcea97040a35faf43f6343311094e97a52ca06823e99bfcac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131712"
---
# <a name="cim-property-qualifiers-for-mib-objects"></a>CIM-Eigenschaftsqualifizierer für MIB-Objekte

Der SNMP-Anbieter verwendet beim Zuordnen von MIB-Objektdefinitionen zu CIM-Klassendefinitionen die folgenden CIM-Eigenschaftsqualifizierer. Ein obligatorischer Qualifizierer muss vorhanden sein, damit der SNMP-Anbieter ein MIB-Objekt vollständig auflösen kann. Fehler beim Definieren eines obligatorischen Qualifizierers gibt einen Fehler zurück. Wenn Sie einen ungültigen Qualifiziererwert angeben, wird auch ein Fehler zurückgegeben.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

 



| Qualifizierer                          | Beschreibung                                                                                                                                                                                            |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bits**                           | **Zeichenfolge** Obligatorisch, wenn der **Textkonventionenqualifizierer \_** nicht bits entspricht.<br/> Enumerationswerte für die Untertypdefinition eines Bits.<br/>                                        |
| **Cimtype**                        | **Zeichenfolge** Obligatorisch<br/> CIM-Textdarstellung, die einen zugrunde liegenden CIM-Protokollwert formatiert.<br/>                                                                                    |
| **Defval**                         | **Zeichenfolge** Optional<br/> Der Standardwert des Objekts.<br/>                                                                                                                                       |
| **Beschreibung**                    | **Zeichenfolge** Optional<br/> Eine Beschreibung des Objekts.<br/>                                                                                                                                    |
| **\_Anzeigehinweis**                  | **Zeichenfolge** Optional<br/> Art und Weise, in der die Daten des Objekts einem Benutzer angezeigt werden sollen.<br/>                                                                                                    |
| **Codieren**                       | **Zeichenfolge** Optional<br/> SNMP-Typ, der beim Codieren von SNMPv1- und SNMPv2C-Protokollframes verwendet wird.<br/>                                                                                              |
| **Enumeration**                    | **Zeichenfolge** Obligatorisch, wenn der **Textual \_ Convention-Qualifizierer** nicht gleich ENUMERATEDINTEGER ist.<br/> Aufzählte Werte für eine aufzählte Ganzzahl-Untertypdefinition.<br/>                  |
| **Feste \_ Länge**                  | **uint32** Optional<br/> Wert fester Länge.<br/>                                                                                                                                           |
| [**Key**](standard-qualifiers.md) | **Bool** Optional<br/> Schlüsseleigenschaft einer Klassendefinition.<br/>                                                                                                                             |
| **\_Schlüsselreihenfolge**                     | **uint32** Optional, es sei denn, [**Key**](standard-qualifiers.md) ist angegeben.<br/> Reihenfolge der Schlüsseleigenschaft in der Klassendefinition.<br/>                                                   |
| **Name**                           | **Zeichenfolge** Obligatorisch<br/> Impliziter Name der Eigenschaft. Beachten Sie, dass dieser Qualifizierer nicht explizit definiert ist.<br/>                                                                           |
| **\_Objektbezeichner**             | **Zeichenfolge** Obligatorisch<br/> Der MIB-Objektbezeichner des Objekts.<br/>                                                                                                                              |
| **\_Objektsyntax**                 | **Zeichenfolge** Optional<br/> Die definition des benannten Typs des Objekts.<br/>                                                                                                                               |
| **Lesen**                           | **Bool** Optional (mindestens ein **Lese-** oder **Schreibvorgang** muss angegeben werden)<br/> Gewährt Lesezugriff auf das Objekt.<br/>                                                                     |
| **Referenz**                      | **Zeichenfolge** Optional<br/> Bezieht sich auf ein anderes Dokument, das weitere Informationen zum -Objekt enthält.<br/>                                                                                   |
| **Status**                         | **Zeichenfolge** Optional<br/> Gibt an, ob das -Objekt unterstützt werden muss.<br/>                                                                                                               |
| **Textkonvention \_**            | **Zeichenfolge** Obligatorisch<br/> Textdarstellung der SYNTAX-Klausel des MIB [OBJECT-TYPE-Makros.](object-type-macro.md)<br/>                                                           |
| **Einheiten**                          | **Zeichenfolge** Optional<br/> Genaue Definition, was das -Objekt darstellt.<br/>                                                                                                             |
| **Variable \_ Länge**               | **Zeichenfolge** Optional<br/> Minimale, maximale und feste Werte, die der Typdefinition des Objekts zugeordnet sind.<br/>                                                                       |
| **\_Variablenwert**                | **Zeichenfolge** Optional<br/> Bereichs- und feste Werte, die der Typdefinition des Objekts zugeordnet sind.<br/>                                                                                         |
| **Virtueller \_ Schlüssel**                   | **Bool** Optional<br/> Gibt an, dass der Wert der Eigenschaft auf der Obermenge der Instanzinformationen basieren soll, die allen barrierefreien MIB-Objekten in der Klassendefinition zugeordnet sind.<br/> |
| **Schreiben**                          | **Bool** Optional (mindestens ein **Lese-** oder **Schreibvorgang** muss angegeben werden)<br/> Gewährt Schreibzugriff auf das Objekt.<br/>                                                                    |



 

 

 




