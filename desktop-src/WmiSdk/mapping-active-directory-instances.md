---
description: Im Allgemeinen wird jedes Active Directory Objekt genau einer WMI-Instanz zugeordnet.
ms.assetid: c6c7f3c3-7174-4278-bf40-d99ed8bd0c8d
ms.tgt_platform: multiple
title: Zuordnung von Active Directory Instanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51eaec7b2c6ef121d0f65df375e1bb0fce32cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042590"
---
# <a name="mapping-active-directory-instances"></a>Zuordnung von Active Directory Instanzen

Im Allgemeinen wird jedes Active Directory Objekt genau einer WMI-Instanz zugeordnet. Die WMI-Klasse, die der WMI-Instanz entspricht, ist identisch mit der-Klasse, die vom-Klassen Anbieter aus der entsprechenden Active Directory-Klasse bereitgestellt wird. Die Schlüsseleigenschaft **adsipath** der einzelnen Instanzen wird mit dem ADSI-Pfad des Objekts ausgefüllt.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Mapping von Namespaces](#mapping-namespaces)
-   [Zuordnen von Attributwerten](#mapping-attribute-values)
-   [Zuordnungs Instanzen Zuordnungen](#mapping-instance-associations)

> [!Note]  
> Weitere Informationen zur Unterstützung und Installation dieser Komponente auf einem bestimmten Betriebssystem finden Sie unter [Betriebssystem Verfügbarkeit von WMI-Komponenten](operating-system-availability-of-wmi-components.md).

 

## <a name="mapping-namespaces"></a>Mapping von Namespaces

Jeder der Namespaces in ADSI ordnet eins-zu-eins-Namespaces im Namespace des WMI-Stamm \\ \\ Verzeichnisses zu. Der Name des WMI-Namespace ist mit dem **ProgID** -Wert des Verzeichnisdienst Anbieters identisch, der den Namespace bereitstellt. Insbesondere Active Directory dem \\ LDAP-Namespace im Stammverzeichnis- \\ \\ Namespace zugeordnet. WMI erstellt den \\ LDAP-Namespace als Teil des Klassen Anbieter-Registrierungsprozesses.

## <a name="mapping-attribute-values"></a>Zuordnen von Attributwerten

In der folgenden Tabelle wird die Zuordnung zwischen den einzelnen Attributen eines Active Directory Objekts und der WMI-Eigenschaft aufgelistet.



| Active Directory-Syntax | WMI-Datentyp                                 | WMI-Eigenschafts Wert                                                        |
|-------------------------|-----------------------------------------------|---------------------------------------------------------------------------|
| Access-Point            | **CIM- \_ Zeichenfolge**                               | Wird vom Wert der Zeichenfolge zugeordnet.                                      |
| Boolean                 | **CIM- \_ boolescher Wert**                              | Wird direkt dem entsprechenden booleschen Wert zugeordnet.                         |
| Groß-/Kleinschreibung | **CIM- \_ Zeichenfolge**                               | Wird vom Wert der Zeichenfolge zugeordnet.                                      |
| Groß-/Kleinschreibung   | **CIM- \_ Zeichenfolge**                               | Wird vom Wert der Zeichenfolge zugeordnet.                                      |
| Definierter Name      | **CIM- \_ Zeichenfolge**                               | Wird vom Wert der Zeichenfolge zugeordnet.                                      |
| DN-Binary               | Eingebettetes Objekt der Klasse **DN \_ mit \_ Binär** | Wird Instanzen des **DN mit der \_ \_ String** -Klasse zugeordnet.                    |
| DN-String               | Eingebettetes Objekt der Klasse **DN \_ mit \_ Zeichenfolge** | Wird Instanzen des **DN mit der \_ \_ String** -Klasse zugeordnet.                    |
| Enumeration             | **CIM \_ SINT32**                               | Wird direkt dem ganzzahligen Wert zugeordnet.                                     |
| IA5-String              | **CIM- \_ Zeichenfolge**                               | Wird vom Wert der Zeichenfolge zugeordnet.                                      |
| Integer                 | **CIM \_ SINT32**                               | Wird direkt dem ganzzahligen Wert zugeordnet.                                     |
| NT-Sicherheits Beschreibung  | Eingebettetes Objekt der Klasse **Uint8Array**       | Wird Instanzen der **Uint8Array** -Klasse zugeordnet.                          |
| Numerische Zeichenfolge          | **CIM- \_ Zeichenfolge**                               | Wird vom Wert der Zeichenfolge zugeordnet.                                      |
| Objekt-ID               | **CIM- \_ Zeichenfolge**                               | Wird von der Zeichen folgen Darstellung der OID zugeordnet. Beispiel: "1.3.3.4". |
| Oktett-Zeichenfolge            | Eingebettetes Objekt der Klasse **Uint8Array**       | Wird Instanzen der **Uint8Array** -Klasse zugeordnet.                          |
| Oder Name                 | **CIM- \_ Zeichenfolge**                               | Wird vom Wert der Zeichenfolge zugeordnet.                                      |
| Presentation-Address    | **CIM- \_ Zeichenfolge**                               | Wird vom Wert der Zeichenfolge zugeordnet.                                      |
| Print Case-Zeichenfolge       | **CIM- \_ Zeichenfolge**                               | Wird vom Wert der Zeichenfolge zugeordnet.                                      |
| Replikat Link            | Eingebettetes Objekt der Klasse **Uint8Array**       | Wird Instanzen der **Uint8Array** -Klasse zugeordnet.                          |
| SID                     | Eingebettetes Objekt der Klasse **Uint8Array**       | Wird Instanzen der **Uint8Array** -Klasse zugeordnet.                          |
| Time                    | **CIM- \_ DateTime**                             | Wird in die CIM \_ -DateTime-Darstellung konvertiert und zugeordnet.                 |
| Nicht definiert               | –                                           | –                                                                       |
| Unicode-Zeichenfolge          | **CIM- \_ Zeichenfolge**                               | Wird vom Wert der Zeichenfolge zugeordnet.                                      |
| UTC-codierte Zeit          | **CIM- \_ DateTime**                             | Wird in die CIM \_ -DateTime-Darstellung konvertiert und zugeordnet.                 |



 

Weitere Informationen zu **Uint8Array** und **DN \_ mit \_ Binary** finden Sie unter [Mapping-Attribute](mapping-active-directory-classes.md).

## <a name="mapping-instance-associations"></a>Zuordnungs Instanzen Zuordnungen

Der Verzeichnisdienst Anbieter ordnet die unterschiedlichen Container Beziehungen in Active Directory mithilfe von Instanzen der Klassen-Containment-Klasse der [**DS- \_ LDAP- \_ Instanz \_**](/previous-versions/windows/desktop/dsprov/ds-ldap-instance-containment) zu.

 

 
