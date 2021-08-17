---
description: Im Allgemeinen wird jedes Active Directory-Objekt genau einer WMI-Instanz zugeordnet.
ms.assetid: c6c7f3c3-7174-4278-bf40-d99ed8bd0c8d
ms.tgt_platform: multiple
title: Zuordnen von Active Directory-Instanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a3e40a6f4a85ebb1bb3d7e1e5a5de7bc43c754ff7672f694aff05b62853dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317637"
---
# <a name="mapping-active-directory-instances"></a>Zuordnen von Active Directory-Instanzen

Im Allgemeinen wird jedes Active Directory-Objekt genau einer WMI-Instanz zugeordnet. Die WMI-Klasse, die der WMI-Instanz entspricht, entspricht der Klasse, die vom Klassenanbieter aus der entsprechenden Active Directory-Klasse bereitgestellt wird. Die Schlüsseleigenschaft **ADSIPath** jeder Instanz wird mit dem ADSI-Pfad des Objekts ausgefüllt.

Die folgenden Abschnitte werden in diesem Thema erläutert:

-   [Zuordnungsnamespaces](#mapping-namespaces)
-   [Zuordnen von Attributwerten](#mapping-attribute-values)
-   [Zuordnungsinstanzzuordnungen](#mapping-instance-associations)

> [!Note]  
> Weitere Informationen zur Unterstützung und Installation dieser Komponente unter einem bestimmten Betriebssystem finden Sie unter [Betriebssystemverfügbarkeit von WMI-Komponenten.](operating-system-availability-of-wmi-components.md)

 

## <a name="mapping-namespaces"></a>Zuordnungsnamespaces

Jeder der Namespaces in ADSI ordnen Namespaces im WMI-Stammverzeichnisnamespace 1:1 \\ \\ zu. Der Name des WMI-Namespaces entspricht dem **ProgId-Wert** des Directory Services-Anbieters, der den Namespace bereitstellt. Insbesondere wird Active Directory dem \\ LDAP-Namespace im \\ \\ Stammverzeichnisnamespace zugeordnet. WMI erstellt den \\ LDAP-Namespace als Teil des Registrierungsprozesses des Klassenanbieters.

## <a name="mapping-attribute-values"></a>Zuordnen von Attributwerten

In der folgenden Tabelle ist die Zuordnung zwischen den einzelnen Attributen eines Active Directory-Objekts und einer WMI-Eigenschaft aufgeführt.



| Active Directory-Syntax | WMI-Datentyp                                 | WMI-Eigenschaftswert                                                        |
|-------------------------|-----------------------------------------------|---------------------------------------------------------------------------|
| Access-Point            | **CIM \_ STRING**                               | Zugeordnet aus dem Wert der Zeichenfolge.                                      |
| Boolean                 | **CIM \_ BOOLEAN**                              | Direkt dem entsprechenden booleschen Wert zugeordnet.                         |
| Zeichenfolge ohne Empfindlichkeit der Groß-/Kleinschreibung | **CIM \_ STRING**                               | Zugeordnet aus dem Wert der Zeichenfolge.                                      |
| Zeichenfolge mit Empfindlichkeit der Groß-/Kleinschreibung   | **CIM \_ STRING**                               | Zugeordnet aus dem Wert der Zeichenfolge.                                      |
| Definierter Name      | **CIM \_ STRING**                               | Zugeordnet aus dem Wert der Zeichenfolge.                                      |
| DN-Binary               | Eingebettetes Objekt der **DN-Klasse \_ mit \_ Binärdatei** | Zugeordnet zu Instanzen der **DN \_ With \_ String-Klasse.**                    |
| DN-String               | Eingebettetes Objekt der **DN-Klasse \_ mit \_ Zeichenfolge** | Zugeordnet zu Instanzen der **DN \_ With \_ String-Klasse.**                    |
| Enumeration             | **CIM \_ SINT32**                               | Direkt dem ganzzahligen Wert zugeordnet.                                     |
| IA5-String              | **CIM \_ STRING**                               | Zugeordnet aus dem Wert der Zeichenfolge.                                      |
| Integer                 | **CIM \_ SINT32**                               | Direkt dem ganzzahligen Wert zugeordnet.                                     |
| NT-Sicherheitsbeschreibung  | Eingebettetes Objekt der **Klasse Uint8Array**       | Zugeordnet zu Instanzen der **Uint8Array-Klasse.**                          |
| Numerische Zeichenfolge          | **CIM \_ STRING**                               | Zugeordnet aus dem Wert der Zeichenfolge.                                      |
| Objekt-ID               | **CIM \_ STRING**                               | Zugeordnet aus der Zeichenfolgendarstellung der OID; Beispiel: "1.3.3.4". |
| Oktettzeichenfolge            | Eingebettetes Objekt der **Klasse Uint8Array**       | Zugeordnet zu Instanzen der **Uint8Array-Klasse.**                          |
| OR-Name                 | **CIM \_ STRING**                               | Zugeordnet aus dem Wert der Zeichenfolge.                                      |
| Presentation-Address    | **CIM \_ STRING**                               | Zugeordnet aus dem Wert der Zeichenfolge.                                      |
| Druckbuchstabenzeichenfolge       | **CIM \_ STRING**                               | Zugeordnet aus dem Wert der Zeichenfolge.                                      |
| Replikatlink            | Eingebettetes Objekt der **Klasse Uint8Array**       | Zugeordnet zu Instanzen der **Uint8Array-Klasse.**                          |
| SID                     | Eingebettetes Objekt der **Klasse Uint8Array**       | Zugeordnet zu Instanzen der **Uint8Array-Klasse.**                          |
| Time                    | **CIM \_ DATETIME**                             | Konvertiert in die \_ CIM DATETIME-Darstellung und zugeordnet.                 |
| Nicht definiert               | Nicht zutreffend                                           | Nicht zutreffend                                                                       |
| Unicode-Zeichenfolge          | **CIM \_ STRING**                               | Zugeordnet aus dem Wert der Zeichenfolge.                                      |
| Codierte UTC-Zeit          | **CIM \_ DATETIME**                             | Konvertiert in die \_ CIM DATETIME-Darstellung und zugeordnet.                 |



 

Weitere Informationen zu **Uint8Array** und **DN \_ mit \_ binären** finden Sie unter [Zuordnungsattribute.](mapping-active-directory-classes.md)

## <a name="mapping-instance-associations"></a>Zuordnungsinstanzzuordnungen

Der Directory Services-Anbieter ordnet die verschiedenen Containerbeziehungen in Active Directory mithilfe von Instanzen der [**DS \_ \_ \_ LDAP-Instanzeinschlussklasse**](/previous-versions/windows/desktop/dsprov/ds-ldap-instance-containment) zu.

 

 
