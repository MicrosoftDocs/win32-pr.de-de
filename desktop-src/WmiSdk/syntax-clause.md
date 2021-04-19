---
description: Enthält eine Syntax Klausel, die die Daten und den Typ für das MIB-Objekt definiert.
ms.assetid: 24c483c8-db50-492f-9c2e-72620395331a
ms.tgt_platform: multiple
title: Syntax Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d0bf25156ddda4bf71a7f40a8de1fede2a82d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359571"
---
# <a name="syntax-clause"></a>Syntax Klausel

Das [Object-Type-](object-type-macro.md) Makro enthält eine Syntax Klausel, die die Daten und den Typ für das MIB-Objekt definiert. Während der SNMP-Anbieter allgemeine Regeln für Mapping-Syntax Klauseln beachtet, befolgt der Anbieter auch Regeln, die für verschiedene Datentypen spezifisch sind.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

Die folgenden Zuordnungsregeln gelten für alle Datentypen, die in der folgenden Tabelle beschrieben werden:

-   Die Textdarstellung der Syntax Klausel wird der **Text \_ Konvention** für den CIM-Eigenschaften Qualifizierer zugeordnet.
-   Die benannte Typdefinition in der Syntax Klausel ist der CIM-Eigenschaft **qualifiziererobjektsyntax \_** zugeordnet. Diese Zuordnung unterscheidet sich je nach Datentyp. Weitere Informationen finden Sie in den Mapping-Beschreibungen.
-   Der beim Codieren von SNMPv1-und SNMPv2C-Protokoll Rahmen verwendete SNMP-Typ wird der CIM-Eigenschaft qualifizierercodierung zugeordnet.
-   Der CIM-Eigenschaften **Qualifizierer CimType** enthält die Textdarstellung, die den zugrunde liegenden CIM-Protokoll Wert formatiert.

In der folgenden Tabelle sind die Datentypen aufgelistet, die bestimmte Regeln aufweisen, die das Verhalten der Anbieter Zuordnung steuern.



| SNMP-Datentyp                                     | BESCHREIBUNG                                                                                                                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Primitiver Typ](#primitive-type)                  | Einer der grundlegenden Datentypen, die in der Struktur von Verwaltungsinformationen (SMI) definiert sind, dokumentiert RFC 1213 und RFC 1903.                                                                                                                            |
| [Text Konvention](textual-convention-macro.md) | Typdefinition, die durch die explizite Verwendung des SNMPv2C **-Text Konvention-** Makros generiert oder durch die Verwendung eines benannten Typs generiert wurde. Eine Text Konvention weist einem vorhandenen Datentyp einen Namen und in einigen Fällen einen Wertebereich zu. |
| [Benannter Typ](#named-type)                          | Benannter Verweis auf einen primitiven Typ, eine Text Konvention oder einen eingeschränkten Typ.                                                                                                                                                                    |
| [Eingeschränkter Typ](#constrained-type)              | Primitiver Typ, benannter Typ oder Text Konvention, der durch einen unter Typisierungs Mechanismus eingeschränkt wurde, der in den SMI-Dokumenten RFC 1213 und RFC 1903 definiert ist.                                                                                      |



 

## <a name="primitive-type"></a>Primitiver Typ

Der primitive Typ ist einer der grundlegenden Datentypen, die in der Struktur der Verwaltungsinformationen (SMI)-Dokumente RFC 1213 und RFC 1903 definiert sind. Primitive SNMP-Typen werden CIM-definierten Typen zugeordnet. In der folgenden Tabelle wird die Zuordnung aufgelistet, die auftritt, wenn sich die Syntax Klausel explizit auf einen primitiven Typ für SNMPv1 bezieht. Die Qualifizierer für **Text \_ Konventionen**, **Codierung** und **Objekt \_ Syntax** sind immer identisch mit dem MIB-Typ, und der Standardwert ist immer **null**.



| MIB-Typ         | CIM-Variant-Typ | CimType-Wert |
|------------------|------------------|---------------|
| INTEGER          | VT \_ I4           | **sint32**    |
| Octetstring      | VT \_ BSTR         | **string**    |
| OBJECTIDENTIFIER | VT \_ BSTR         | **string**    |
| NULL             | VT \_ null         | Nicht unterstützt |
| IpAddress        | VT \_ BSTR         | **string**    |
| Zähler          | VT \_ I4           | **uint32**    |
| Maßstab            | VT \_ I4           | **uint32**    |
| TimeTicks        | VT \_ I4           | **uint32**    |
| Nicht transparent           | VT \_ BSTR         | **string**    |
| NetworkAddress   | VT \_ BSTR         | **string**    |



 

Der Anbieter ignoriert das objekttypmakro, wenn die Syntax Klausel auf **null** verweist, entweder explizit oder durch eine benannte Typzuweisung. In der folgenden Tabelle wird die Zuordnung aufgelistet, die auftritt, wenn sich die Syntax Klausel explizit auf einen primitiven Typ für SNMPv2 bezieht. Die Qualifizierer für **Text \_ Konventionen**, **Codierung** und **Objekt \_ Syntax** sind immer identisch mit dem MIB-Typ, und der Standardwert ist immer **null**.



| MIB-Typ          | CIM-Variant-Typ | CimType-Wert |
|-------------------|------------------|---------------|
| INTEGER           | VT \_ I4           | **sint32**    |
| Oktett-Zeichenfolge      | VT \_ BSTR         | **string**    |
| Objekt Bezeichner | VT \_ BSTR         | **string**    |
| IpAddress         | VT \_ BSTR         | **string**    |
| Counter32         | VT \_ I4           | **uint32**    |
| Gauge32           | VT \_ I4           | **uint32**    |
| Unsigned32        | VT \_ I4           | **uint32**    |
| Integer32         | VT \_ I4           | **sint32**    |
| Counter64         | VT \_ BSTR         | **uint64**    |
| TimeTicks         | VT \_ I4           | **uint32**    |
| Nicht transparent            | VT \_ BSTR         | **string**    |



 

## <a name="named-type"></a>Benannter Typ

Benannte SNMP-Typen werden CIM-definierten Typen zugeordnet. Wenn sich die Syntax Klausel auf einen [primitiven Typ](#primitive-type), eine [Text Konvention](textual-convention-macro.md)oder einen [eingeschränkten Typ](#constrained-type) durch eine typzuweisungs Ableitung bezieht, verwenden Sie die diese Typen, um zu bestimmen, welche Zuordnungs Prozeduren angewendet werden.

-   Wenn bei der Ableitung der typzuweisungs Regeln eine beschränkte Typdefinition auftritt:

    -   Wenn Sie durch weitere Ableitung eine der im [Textkonventionen-Makro](textual-convention-macro.md)aufgeführten Textkonventionen sehen, wenden Sie dann die Zuordnungsregeln für eingeschränkte Typen und Textkonventionen an.
    -   Wenn Sie einen der primitiven Typen sehen, die in der Tabelle primitiver Typen aufgeführt sind, wenden Sie andernfalls die Zuordnungsregeln für primitive Typen und eingeschränkte Typen an.

-   Wenn eine der im [Text \_ Konvention-Makro](textual-convention-macro.md)aufgeführten Textkonventionen vorliegt, wenden Sie die Zuordnungsregeln für Textkonventionen an.
-   Wenn Sie einen der primitiven Typen sehen, die in der Tabelle primitiver Typen aufgeführt sind, wenden Sie die Zuordnungsregeln für primitive Typen an.

> [!Note]  
> Klassen, die Eigenschafts Typen enthalten, die nicht mit der oben beschriebenen Zuordnung übereinstimmen, sind ungültig. In diesem Fall gibt der Anbieter einen Fehler zurück, wenn der Anbieter den Abruf einer Klassendefinition beim Ausführen einer Instanzabruf Funktion anfordert.

 

## <a name="constrained-type"></a>Eingeschränkter Typ

Ein eingeschränkter Typ ist ein primitiver Typ, benannter Typ oder eine Text Konvention, der durch einen unter Typisierungs Mechanismus eingeschränkt wurde, der in den SMI-Dokumenten RFC 1213 und RFC 1903 definiert ist. Wenn die unter Typisierung erfolgt, sind zusätzliche CIM-Qualifizierer erforderlich, um die Untertyp Werte anzugeben. Die benannte Typdefinition in der Syntax Klausel ordnet die **\_ Syntax** des CIM-Eigenschafts qualifiziererobjekts bis zu, ohne die Einschränkungen des unter Typs.

Untertypen können einem der folgenden Formate folgen:

-   Enumerierte Ganzzahl

    Die CIM-Eigenschaft **qualifiziererenumeration** gibt die Enumerationswerte an. Dieser Qualifizierer wird als Zeichenfolge dargestellt, die eine durch Trennzeichen getrennte Liste von ganzzahligen 32-Bit-Werten enthält. In der folgenden Tabelle sind die-Mapping-Typen aufgeführt. Der Standardwert ist immer **null**.



| Eingeschränkter MIB-Typ | CIM-Variant-Typ | CIM Qualifizierer                                                                                                        |
|----------------------|------------------|-----------------------------------------------------------------------------------------------------------------------|
| Enumerierte Ganzzahl   | VT \_ BSTR         | **Text \_ Konvention**: enumeratedinteger<br/> **Codierung**: ganze Zahl<br/> **CimType**: Zeichenfolge<br/> |



 

-   BITS

    Der CIM-Eigenschaften Qualifizierer **Bits** gibt die Enumerationswerte an. Dieser Qualifizierer wird als Zeichenfolge dargestellt, die eine durch Trennzeichen getrennte Liste von ganzzahligen 32-Bit-Werten enthält. In der folgenden Tabelle sind die-Mapping-Typen aufgeführt. Der Standardwert ist immer **null**.



| Eingeschränkter MIB-Typ | CIM-Variant-Typ      | CIM Qualifizierer                                                                                               |
|----------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| BITS                 | VT \_ array \| VT \_ BSTR | **Text \_ Konvention**: Bits<br/> **Codierung**: octetstring<br/> **CimType**: Zeichenfolge<br/> |



 

-   Variable Länge

    Wenn sich die Syntax Klausel auf einen primitiven Typ, einen benannten Typ oder eine Text Konvention bezieht, die als Oktett-Zeichenfolge mit variabler Länge oder als nicht transparent typisiert ist, gibt die **\_ Länge der Länge** des CIM-Eigenschaften Qualifizierers den minimalen, maximalen und den Wert mit fester Länge an, der der Typdefinition zugeordnet ist. Dieser Qualifizierer wird als Zeichenfolge im folgenden Format implementiert, in dem die Werte variabler Länge als Vorzeichen lose ganze Zahlen mit Vorzeichen (32 Bit) dargestellt werden.

    ``` syntax
    (((0.9) .. (0.9)) | (0.9))(, (((0.9) .. (0.9)) | (0.9)))*
    ```

-   Feste Länge

    Wenn sich die Syntax Klausel auf einen primitiven Typ, einen benannten Typ oder eine Text Konvention bezieht, die als Oktett-Zeichenfolge mit fester Länge oder als nicht transparent typisiert ist, gibt die **festgelegte \_ Länge** des CIM-Eigenschaften Qualifizierers den Wert mit fester Länge an. Dieser Qualifizierer wird als ganzzahliger Wert ohne Vorzeichen (32 Bit) dargestellt.

-   Range

    Wenn sich die Syntax Klausel auf einen primitiven Typ, einen benannten Typ oder eine Text Konvention bezieht, die als eine ganze Zahl oder eine ganze Zahl mit fester Wert oder einem Messgerät subtypisiert ist, gibt der **\_ Wert** des CIM-Eigenschafts Qualifizierers den mit der Typdefinition verknüpften Bereich und die Werte an Dieser Qualifizierer wird als Zeichenfolge im folgenden Format implementiert, wobei der Bereich und die Werte mit fester Länge als Vorzeichen lose ganze Zahlen mit Vorzeichen (32 Bit) dargestellt werden.

    ``` syntax
    (((0.9)..(0.9))|(0.9))(,(((0.9)..(0.9))|(0.9)))*
    ```

## <a name="example-code"></a>Beispielcode

Im folgenden Beispiel wird ein enumerierter ganzzahliger Untertyp beschrieben.

``` syntax
Status := INTEGER {
up(1),
down(2),
testing(3)
}
```

In diesem Beispiel wird Folgendes dargestellt:

``` syntax
enumeration("up(1),down(2),testing(3)")
```

Im folgenden Codebeispiel wird ein Bits-Untertyp beschrieben.

``` syntax
Status := BITS {
up(1),
down(2), 
testing(3)
}
```

Im folgenden Codebeispiel wird Folgendes veranschaulicht:

``` syntax
bits("up(1),down(2),testing(3)")
```

Im folgenden Codebeispiel wird ein Untertyp variabler Länge beschrieben.

``` syntax
MySnmpOSIAddress ::=  TEXTUAL-CONVENTION

    DISPLAY-HINT    "*1x:/1x:"
    STATUS        current
    DESCRIPTION
            "Represents an OSI transport-address:

            octets    contents         encoding
              1        length of NSAP   'n' as an unsigned-integer
                                        (either 0 or from 3 to 20)
              2..(n+1)  NSAP          concrete binary representation
              (n+2)..m  TSEL             string of (up to 64) octets
            "
    SYNTAX         OCTET STRING (SIZE (1|4..85))
```

In diesem Beispiel wird Folgendes dargestellt:

``` syntax
display_hint("*1x:/1x:"),
encoding("OCTETSTRING"),
textual_convention("OCTETSTRING"),
variable_length ("1,4..85")
```

Im folgenden Beispiel wird ein Untertyp mit fester Länge beschrieben.

``` syntax
IPXADDRESS := OCTET STRING (SIZE (6))
```

In diesem Beispiel wird Folgendes dargestellt:

``` syntax
fixed_length(6)
```

Im folgenden Beispiel wird ein Bereichs Untertyp beschrieben.

``` syntax
Status := INTEGER (10..20|8)
```

In diesem Beispiel wird Folgendes dargestellt:

``` syntax
variable_value("10..20,8")
```

 

 




