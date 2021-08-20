---
description: SNMP-Textkonventionen werden CIM-definierten Typen zugeordnet.
ms.assetid: 73bb6c22-0a68-4a4b-8de2-8326ec67a059
ms.tgt_platform: multiple
title: TEXTUAL-CONVENTION-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 316463282549180b7c0781ea19d36818e1636bb9f061b78c51420694cfc4890c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107604"
---
# <a name="textual-convention-macro"></a>TEXTUAL-CONVENTION-Makro

SNMP-Textkonventionen werden CIM-definierten Typen zugeordnet.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

 

Die folgenden Zuordnungsregeln gelten für SNMP-Textkonventionen:

-   Die Definition des benannten Typs in der SYNTAX-Klausel ordnet der **CIM-Eigenschaftenqualifiziererobjektsyntax \_** ausführlich zu.
-   Verwenden Sie die folgende Tabelle, um Textkonventionen zuzuordnen, wenn die SYNTAX-Klausel explizit auf eine Textkonvention eines SNMPv2C TEXTUAL-CONVENTION-Makros oder auf eine implizite Textkonvention verweist. Der Standardwert ist immer **NULL.**



| Textkonvention | CIM-Variantentyp | CIM-Qualifizierer                                                                                                                                                        |
|--------------------|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DateAndTime        | **VT \_ BSTR**     | **textual \_ convention**: DateAndTime<br/> **encoding**: OCTETSTRING<br/> **\_ Objektsyntax:** DateAndTime<br/> **cimtype:** string<br/>       |
| Displaystring      | **VT \_ BSTR**     | **textual \_ convention**: Displaystring<br/> **encoding**: OCTETSTRING<br/> **\_ Objektsyntax:** Displaystring<br/> **cimtype:** string<br/>   |
| MacAddress         | **VT \_ BSTR**     | **\_ Textkonvention:** MacAddress<br/> **encoding**: OCTETSTRING<br/> **\_ Objektsyntax:** MacAddress<br/> **cimtype:** string<br/>         |
| PhysAddress        | **VT \_ BSTR**     | **textual \_ convention**: PhysAddress<br/> **encoding**: OCTETSTRING<br/> **\_ Objektsyntax:** PhysAddress<br/> **cimtype:** string<br/>       |
| SnmpUDPAddress     | **VT \_ BSTR**     | **textual \_ convention**: SnmpUDPAddress<br/> **encoding**: OCTETSTRING<br/> **\_ Objektsyntax:** SnmpUDPAddress<br/> **cimtype:** string<br/> |
| SnmpOSIAddress     | **VT \_ BSTR**     | **textual \_ convention**: SnmpOSIAddress<br/> **encoding**: OCTETSTRING<br/> **\_ Objektsyntax:** SnmpOSIAddress<br/> **cimtype:** string<br/> |
| SnmpIPXAddress     | **VT \_ BSTR**     | **textual \_ convention**: SnmpIPXAddress<br/> **encoding**: OCTETSTRING<br/> **\_ Objektsyntax:** SnmpIPXAddress<br/> **cimtype:** string<br/> |



 

-   Der CIM-definierte Variantestyp und die CIM-Eigenschaftsqualifizierer **textual \_ convention**, **encoding**, **object \_ syntax** und **cimtype** map unter Verwendung des zugrunde liegenden primitiven Typs.
-   Die DISPLAY-HINT-Klausel des SNMPv2C TEXTUAL-CONVENTION-Makros wird dem **\_ ANZEIGEhinweis** des CIM-Eigenschaftsqualifizierers ausführlich zugeordnet. Dieser Qualifizierer wird nicht generiert, wenn kein TEXTUAL-CONVENTION-Makro vorhanden ist oder das Makro keine DISPLAY-HINT-Klausel enthält.

## <a name="example-code"></a>Beispielcode

Im folgenden Beispiel wird eine SNMPv1-Textkonvention beschrieben.

``` syntax
myNamedType ::= DISPLAYSTRING (SIZE (0..127))

myNamedProperty OBJECT-TYPE
SYNTAX  myNamedType
ACCESS read-only
STATUS MANDATORY
DESCRIPTION ""
```

In diesem Beispiel werden die folgenden CIM-Qualifizierer generiert.

``` syntax
object_syntax("myNamedType"),
textual_convention("DISPLAYSTRING"),
encoding("OCTETSTRING"),
variable_length("0..127")
```

Im folgenden Beispiel wird eine SNMPv2-Textkonvention beschrieben.

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

In diesem Beispiel werden die folgenden CIM-Qualifizierer generiert.

``` syntax
object_syntax("myDisplaystring"),
textual_convention("OCTETSTRING"),
encoding("OCTETSTRING"),
display_hint("255a"),
variable_length("0..127")
```

 

 




