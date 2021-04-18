---
description: SNMP-Textkonventionen werden CIM-definierten Typen zugeordnet.
ms.assetid: 73bb6c22-0a68-4a4b-8de2-8326ec67a059
ms.tgt_platform: multiple
title: Text Konvention-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329508ce3d124c0b3954675b3142aeb33c402923
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343787"
---
# <a name="textual-convention-macro"></a>Text Konvention-Makro

SNMP-Textkonventionen werden CIM-definierten Typen zugeordnet.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

Die folgenden Zuordnungsregeln gelten für die SNMP-Textkonventionen:

-   Die benannte Typdefinition in der Syntax Klausel ordnet der CIM-Eigenschaften **qualifiziererobjektsyntax \_** wörtlich zu.
-   Verwenden Sie die folgende Tabelle, um Textkonventionen zuzuordnen, wenn sich die Syntax Klausel explizit auf eine Text Konvention eines SNMPv2C-Text Konvention-Makros bezieht, oder auf eine implizite Text Konvention verweist. Der Standardwert ist immer **null**.



| Text Konvention | CIM-Variant-Typ | CIM Qualifizierer                                                                                                                                                        |
|--------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DateAndTime        | **VT \_ BSTR**     | **Text \_ Konvention**: DateAndTime<br/> **Codierung**: octetstring<br/> **Objekt \_ Syntax**: DateAndTime<br/> **CimType**: Zeichenfolge<br/>       |
| Display String      | **VT \_ BSTR**     | **Text \_ Konvention**: Display String<br/> **Codierung**: octetstring<br/> **Objekt \_ Syntax**: Display String<br/> **CimType**: Zeichenfolge<br/>   |
| MacAddress         | **VT \_ BSTR**     | **Text \_ Konvention**: MACAddress<br/> **Codierung**: octetstring<br/> **Objekt \_ Syntax**: MACAddress<br/> **CimType**: Zeichenfolge<br/>         |
| Physaddress        | **VT \_ BSTR**     | **Text \_ Konvention**: physaddress<br/> **Codierung**: octetstring<br/> **Objekt \_ Syntax**: physaddress<br/> **CimType**: Zeichenfolge<br/>       |
| Snmpudpaddress     | **VT \_ BSTR**     | **Text \_ Konvention**: snmpudpaddress<br/> **Codierung**: octetstring<br/> **Objekt \_ Syntax**: snmpudpaddress<br/> **CimType**: Zeichenfolge<br/> |
| Snmposiaddress     | **VT \_ BSTR**     | **Text \_ Konvention**: snmposiaddress<br/> **Codierung**: octetstring<br/> **Objekt \_ Syntax**: snmposiaddress<br/> **CimType**: Zeichenfolge<br/> |
| Snmpipxaddress     | **VT \_ BSTR**     | **Text \_ Konvention**: snmpipxaddress<br/> **Codierung**: octetstring<br/> **Objekt \_ Syntax**: snmpipxaddress<br/> **CimType**: Zeichenfolge<br/> |



 

-   Der CIM-definierte Variant-Typ und die CIM-Eigenschafts Qualifizierer **Text \_ Konvention**, **Codierung**, **Objekt \_ Syntax** und **CimType** -Zuordnung unter Verwendung des zugrunde liegenden primitiven Typs.
-   Die Display-Hint-Klausel des SNMPv2C-Text Konvention-Makros wird dem CIM-Eigenschaften qualifiziereranzeige- **\_ Hinweis** wörtlich zugeordnet. Dieser Qualifizierer wird nicht generiert, wenn kein Textkonventionen-Makro vorhanden ist oder das Makro keine Display-Hint-Klausel enthält.

## <a name="example-code"></a>Beispielcode

Im folgenden Beispiel wird eine SNMPv1-Text Konvention beschrieben.

``` syntax
myNamedType ::= DISPLAYSTRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myNamedType
ACCESS read-only
STATUS MANDATORY
DESCRIPTION ""
```

Dieses Beispiel generiert die folgenden CIM-Qualifizierer.

``` syntax
object_syntax("myNamedType"),
textual_convention("DISPLAYSTRING"),
encoding("OCTETSTRING"),
variable_length("0..127")
```

Im folgenden Beispiel wird eine SNMPv2-Text Konvention beschrieben.

``` syntax
myDisplaystring ::= TEXTUAL-CONVENTION
DISPLAY-HINT "255a"
STATUS current
DESCRIPTION "" 
SYNTAX OCTET STRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myDisplaystring
MAX-ACCESS read-only
STATUS current
DESCRIPTION ""
```

Dieses Beispiel generiert die folgenden CIM-Qualifizierer.

``` syntax
object_syntax("myDisplaystring"),
textual_convention("OCTETSTRING"),
encoding("OCTETSTRING"),
display_hint("255a"),
variable_length("0..127")
```

 

 




