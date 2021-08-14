---
description: Mit einem ACE (Conditional Access Control Entry) kann eine Zugriffsbedingung ausgewertet werden, wenn eine Zugriffsüberprüfung durchgeführt wird. Die Sicherheitsdeskriptordefinitionssprache (Security Descriptor Definition Language, SDDL) stellt Syntax zum Definieren von bedingten ACEs in einem Zeichenfolgenformat bereit.
ms.assetid: cdc3629d-c4d8-4910-8838-3bdb601f7064
title: Sicherheitsbeschreibungsdefinitionssprache für bedingte ACEs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0a746460c7582d95e0c95e2a2c179aac2eb29456418234cb52e842c8c56738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780525"
---
# <a name="security-descriptor-definition-language-for-conditional-aces"></a>Sicherheitsbeschreibungsdefinitionssprache für bedingte ACEs

Mit einem ACE (Conditional [*Access Control Entry)*](/windows/desktop/SecGloss/a-gly) kann eine Zugriffsbedingung ausgewertet werden, wenn eine Zugriffsüberprüfung durchgeführt wird. Die Sicherheitsdeskriptordefinitionssprache (Security Descriptor Definition Language, SDDL) stellt Syntax zum Definieren von bedingten ACEs in einem Zeichenfolgenformat bereit.

Die SDDL für einen bedingten ACE ist identisch mit jedem ACE, wobei die Syntax für die bedingte Anweisung an das Ende der ACE-Zeichenfolge angefügt ist. Informationen zu SDDL finden Sie unter [Security Descriptor Definition Language](security-descriptor-definition-language.md).

Das \# Zeichen "" ist synonym mit "0" in Ressourcenattributen. Beispiel: D:AI(XA;OICI;FA;;; WD;(OctetStringType== \# 1 \# 2 \# 3 \# \# )) entspricht und wird als D:AI(XA;OICI;FA;;; interpretiert. WD;(OctetStringType== \# 01020300)).

-   [Bedingtes ACE-Zeichenfolgenformat](#conditional-ace-string-format)
-   [Bedingte Ausdrücke](#conditional-expressions)
-   [Attribute](#attributes)
-   [Operatoren](#operators)
-   [Operatorrangfolge](#operator-precedence)
-   [Unbekannte Werte](#unknown-values)
-   [Bedingte ACE-Auswertung](#conditional-ace-evaluation)
-   [Beispiele](#examples)
-   [Zugehörige Themen](#related-topics)

## <a name="conditional-ace-string-format"></a>Bedingtes ACE-Zeichenfolgenformat

Jeder ACE in einer [*Sicherheitsbeschreibungszeichenfolge*](/windows/desktop/SecGloss/s-gly) ist in Klammern eingeschlossen. Die Felder des ACE befinden sich in der folgenden Reihenfolge und werden durch Semikolons (;).

*AceType***;** _AceFlags_* _;_ *_Rechte_*_;_ *_ObjectGuid_*_;_ *_InheritObjectGuid_*_;_ *_AccountSid_*_;(_*_ConditionalExpression_*_)_*

Die Felder sind wie in [ACE-Zeichenfolgen](ace-strings.md)beschrieben, mit den folgenden Ausnahmen.

-   Das *AceType-Feld* kann eine der folgenden Zeichenfolgen sein.

    | ACE-Typzeichenfolge | Konstante in "Sddl.h"                         | AceType-Wert                                   |
    |-----------------|--------------------------------------------|-------------------------------------------------|
    | "XA"<br/> | SDDL \_ CALLBACK \_ ACCESS \_ ALLOWED<br/> | \_ZUGRIFF ZULÄSSIGER \_ \_ RÜCKRUF-ACE-TYP \_<br/> |
    | "XD"<br/> | ZUGRIFF DES \_ SDDL-RÜCKRUFS \_ \_ VERWEIGERT<br/>  | ACCESS \_ DENIED \_ CALLBACK \_ ACE \_ TYPE<br/>  |

    

     

-   Die ACE-Zeichenfolge enthält einen oder mehrere bedingte Ausdrücke, die in Klammern am Ende der Zeichenfolge eingeschlossen sind.

## <a name="conditional-expressions"></a>Bedingte Ausdrücke

Ein bedingter Ausdruck kann eines der folgenden Elemente enthalten.



| Ausdruckselement                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *AttributeName*<br/>                                        | Testet, ob das angegebene Attribut über einen Wert ungleich 0 (null) verfügt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **exists** *AttributeName*<br/>                             | Testet, ob das angegebene Attribut im Clientkontext vorhanden ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| *AttributeName-Operatorwert*  <br/>                     | Gibt das Ergebnis des angegebenen Vorgangs zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| *ConditionalExpression* **\|\|** _ConditionalExpression_<br/> | Testet, ob einer der angegebenen bedingten Ausdrücke true ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *ConditionalExpression* **&&** *ConditionalExpression*<br/> | Testet, ob beide der angegebenen bedingten Ausdrücke wahr sind.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **! (**_ConditionalExpression_*_)_*<br/>                     | Die Umkehrung eines bedingten Ausdrucks.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Member \_ von{**_SidArray_*_}_*<br/>                         | Testet, ob das [**SID \_ AND \_ ATTRIBUTES-Array**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) des Clientkontexts alle [Sicherheitsbezeichner](security-identifiers.md) (SIDs) in der durch Trennzeichen getrennten Liste enthält, die von *SidArray* angegeben wird.<br/> Für ACEs zulassen muss für eine Clientkontext-SID das **SE \_ GROUP \_ ENABLED-Attribut** festgelegt sein, um als Übereinstimmung angesehen zu werden.<br/> Für ACEs verweigern muss für eine Clientkontext-SID entweder das **SE \_ GROUP \_ ENABLED** oder das **SE GROUP USE FOR \_ \_ \_ \_ DENY \_ ONLY-Attribut** festgelegt sein, um als Übereinstimmung angesehen zu werden.<br/> Das *SidArray-Array* kann entweder SID-Zeichenfolgen (z.B. "S-1-5-6") oder SID-Aliase (z.B. "BA") enthalten.<br/> |



 

## <a name="attributes"></a>Attribute

Ein Attribut stellt ein Element im [**ARRAY DER SECURITY ATTRIBUTES \_ \_ \_ INFORMATION**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) von AUTHZ im Clientkontext dar. Ein Attributname kann alle alphanumerischen Zeichen und die Zeichen ":", "/", "." und "" \_ enthalten.

Ein Attributwert kann einer der folgenden Typen sein.



| Werttyp         | BESCHREIBUNG                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Integer<br/> | Eine 64-Bit-Ganzzahl in Dezimal- oder Hexadezimalschreibweise.<br/>                                                                                                                              |
| String<br/>  | Ein Zeichenfolgenwert, der durch Anführungszeichen getrennt ist.<br/>                                                                                                                                                      |
| SID<br/>     | SID(S-1-1-0) oder SID(BA). Muss sich auf DEM RHS von Member \_ von oder Device Member von \_ \_ befingen.<br/>                                                                                                           |
| BLOB<br/>    | \# gefolgt von Hexadezimalzahlen. Wenn die Länge der Zahlen ungerade ist, wird in \# eine 0 übersetzt, um sie gleichmäßig zu machen. Auch eine \# , die an anderer Stelle im Wert angezeigt wird, wird in eine 0 übersetzt.<br/> |



 

## <a name="operators"></a>Operatoren

Die folgenden Operatoren werden für die Verwendung in bedingten Ausdrücken definiert, um die Werte von Attributen zu testen. Alle diese Operatoren sind binäre Operatoren und werden im Format *AttributeName-Operatorwert* verwendet. 



| Operator            | BESCHREIBUNG                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| ==<br/>       | Konventionelle Definition.<br/>                                                                                      |
| !=<br/>       | Konventionelle Definition.<br/>                                                                                      |
| <<br/>     | Konventionelle Definition.<br/>                                                                                      |
| <=<br/>    | Konventionelle Definition.<br/>                                                                                      |
| ><br/>     | Konventionelle Definition.<br/>                                                                                      |
| >=<br/>    | Konventionelle Definition.<br/>                                                                                      |
| Enthält<br/> | **TRUE,** wenn der Wert des angegebenen Attributs eine Obermenge des angegebenen Werts ist; Andernfalls **FALSE**.<br/>  |
| Eine \_ der<br/>  | **TRUE,** wenn der angegebene Wert eine Obermenge des Werts des angegebenen Attributs ist; Andernfalls **FALSE**. <br/> |



 

Darüber hinaus werden die unären Operatoren Exists, Member \_ of und negation (!) wie in der Tabelle Bedingte Ausdrücke beschrieben definiert.

Dem Operator "Contains" muss Leerzeichen vorangestellt werden, gefolgt von Leerzeichen, und dem Operator "Any \_ of" muss Leerraum vorangestellt werden.

## <a name="operator-precedence"></a>Operatorrangfolge

Die Operatoren werden in der folgenden Rangfolge ausgewertet, wobei Vorgänge gleicher Rangfolge von links nach rechts ausgewertet werden.

1.  Exists, Member \_ von
2.  Contains, Any \_ of
3.  ==, !=, <, <=, >, >=
4.  !
5.  &&
6.  \|\|

Darüber hinaus kann jeder Teil eines bedingten Ausdrucks in Klammern eingeschlossen werden. Ausdrücke in Klammern werden zuerst ausgewertet.

## <a name="unknown-values"></a>Unbekannte Werte

Die Ergebnisse von bedingten Ausdrücken geben manchmal den Wert **Unknown** zurück. Beispielsweise gibt jeder der relationalen Vorgänge Unknown **zurück,** wenn das angegebene Attribut nicht vorhanden ist.

In der folgenden Tabelle werden die Ergebnisse für einen logischen **AND-Vorgang** zwischen zwei bedingten Ausdrücken beschrieben: *ConditionalExpression1* und *ConditionalExpression2.*



| *ConditionalExpression1* | *ConditionalExpression2* | *ConditionalExpression1* **&&** *ConditionalExpression2* |
|--------------------------|--------------------------|----------------------------------------------------------|
| **TRUE**<br/>      | **TRUE**<br/>      | **TRUE**<br/>                                      |
| **TRUE**<br/>      | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **TRUE**<br/>      | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                   |
| **FALSE**<br/>     | **TRUE**<br/>      | **FALSE**<br/>                                     |
| **FALSE**<br/>     | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **FALSE**<br/>     | **UNKNOWN**<br/>   | **FALSE**<br/>                                     |
| **UNKNOWN**<br/>   | **TRUE**<br/>      | **UNKNOWN**<br/>                                   |
| **UNKNOWN**<br/>   | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **UNKNOWN**<br/>   | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                   |



 

In der folgenden Tabelle werden die Ergebnisse für einen logischen **OR-Vorgang** zwischen zwei bedingten Ausdrücken beschrieben: *ConditionalExpression1* und *ConditionalExpression2.*



| *ConditionalExpression1* | *ConditionalExpression2* | *ConditionalExpression1* **\|\|** *ConditionalExpression2* |
|--------------------------|--------------------------|------------------------------------------------------------|
| **TRUE**<br/>      | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **TRUE**<br/>      | **FALSE**<br/>     | **TRUE**<br/>                                        |
| **TRUE**<br/>      | **UNKNOWN**<br/>   | **TRUE**<br/>                                        |
| **FALSE**<br/>     | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **FALSE**<br/>     | **FALSE**<br/>     | **FALSE**<br/>                                       |
| **FALSE**<br/>     | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                     |
| **UNKNOWN**<br/>   | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **UNKNOWN**<br/>   | **FALSE**<br/>     | **UNKNOWN**<br/>                                     |
| **UNKNOWN**<br/>   | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                     |



 

Die Negation eines bedingten Ausdrucks mit dem Wert **UNKNOWN** ist ebenfalls **UNKNOWN.**

## <a name="conditional-ace-evaluation"></a>Bedingte ACE-Auswertung

In der folgenden Tabelle wird das Ergebnis der Zugriffsüberprüfung eines bedingten ACE in Abhängigkeit von der endgültigen Auswertung des bedingten Ausdrucks beschrieben.

| ACE-Typ         | TRUE             | FALSE                 | UNKNOWN               |
|------------------|------------------|-----------------------|-----------------------|
| Zulassen<br/> | Zulassen<br/> | ACE ignorieren<br/> | ACE ignorieren<br/> |
| Verweigern<br/>  | Verweigern<br/>  | ACE ignorieren<br/> | Verweigern<br/>       |



 

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird gezeigt, wie die angegebenen Zugriffsrichtlinien durch einen bedingten ACE dargestellt werden, der mithilfe von SDDL definiert wird.

<dl> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Politik
</dt> <dd>

Lassen Sie Die Ausführung an alle zu, wenn beide der folgenden Bedingungen erfüllt sind:

-   Title = PM
-   Division = Finance oder Division = Sales

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>Sddl
</dt> <dd>

D:(XA; ; FX;;; S-1-1-0; ( @User.Title =="PM" && ( @User.Division =="Finance" \| \| @User.Division ==" Sales")))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Politik
</dt> <dd>

Ausführung zulassen, wenn sich eines der Projekte des Benutzers mit den Projekten der Datei überschneidet.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>Sddl
</dt> <dd>

D:(XA; ; FX;;; S-1-1-0; ( @User.Project Any \_ of @Resource.Project ))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Politik
</dt> <dd>

Lesezugriff zulassen, wenn sich der Benutzer mit einer Smartcard angemeldet hat, ein Sicherungsoperator ist und von einem Computer aus eine Verbindung mit aktivierter BitLocker-Funktion herstellen kann.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>Sddl
</dt> <dd>

D:(XA; ;FR;;; S-1-1-0; (Member \_ von {SID(Smartcard \_ SID), SID(BO)} && @Device.Bitlocker ))

</dd> <dt>

 
</dt> <dd>

 

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[\[MS-DTYP: \] Beschreibungssprache für Sicherheitsbeschreibungen](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

