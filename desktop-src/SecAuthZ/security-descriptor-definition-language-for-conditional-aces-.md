---
description: Mit einem bedingten Zugriffs Steuerungs Eintrag (ACE) kann eine Zugriffs Bedingung ausgewertet werden, wenn eine Zugriffs Überprüfung durchgeführt wird. Die Security Deskriptor Definition Language (SDDL) stellt eine Syntax zum Definieren von bedingten ACEs in einem Zeichen folgen Format bereit.
ms.assetid: cdc3629d-c4d8-4910-8838-3bdb601f7064
title: Sicherheits Deskriptor-Definitions Sprache für bedingte ACEs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cb6ae0588ae197c84d3b13362721cc3e98b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527014"
---
# <a name="security-descriptor-definition-language-for-conditional-aces"></a>Sicherheits Deskriptor-Definitions Sprache für bedingte ACEs

Mit einem bedingten [*Zugriffs Steuerungs Eintrag*](/windows/desktop/SecGloss/a-gly) (ACE) kann eine Zugriffs Bedingung ausgewertet werden, wenn eine Zugriffs Überprüfung durchgeführt wird. Die Security Deskriptor Definition Language (SDDL) stellt eine Syntax zum Definieren von bedingten ACEs in einem Zeichen folgen Format bereit.

Die SDDL für einen bedingten ACE ist das gleiche wie bei jedem ACE, wobei die Syntax für die bedingte Anweisung an das Ende der ACE-Zeichenfolge angefügt wird. Weitere Informationen zu SDDL finden Sie unter [Security Descriptor Definition Language](security-descriptor-definition-language.md).

Das \# Zeichen "" ist in Ressourcen Attributen mit "0" Synonym. Beispiel: d:Ai (XA; oici; FA;;; WD; (octetstringtype = = \# 1 \# 2 \# 3 \# \# )) entspricht und wird als d:Ai (XA; oici; FA;;;) interpretiert. WD; (octetstringtype = = \# 01020300)).

-   [Format der bedingten ACE-Zeichenfolge](#conditional-ace-string-format)
-   [Bedingte Ausdrücke](#conditional-expressions)
-   [Attribute](#attributes)
-   [Operatoren](#operators)
-   [Operatorrangfolge](#operator-precedence)
-   [Unbekannte Werte](#unknown-values)
-   [Auswertung bedingter ACE](#conditional-ace-evaluation)
-   [Beispiele](#examples)
-   [Zugehörige Themen](#related-topics)

## <a name="conditional-ace-string-format"></a>Format der bedingten ACE-Zeichenfolge

Jeder ACE in einer [*sicherheitsbeschreibungerzeichenfolge*](/windows/desktop/SecGloss/s-gly) wird in Klammern eingeschlossen. Die Felder des ACE liegen in der folgenden Reihenfolge vor und sind durch Semikolons (;) getrennt.

*AceType ***;** _AceFlags_* _;_ *_Rechte_*_;_ *_ObjectGUID_*_;_ *_Erertobjectguid_*_;_ *_AccountSid_*_;(_*_ConditionalExpression_*_)_*

Die Felder werden wie in [ACE](ace-strings.md)-Zeichen folgen beschrieben mit den folgenden Ausnahmen beschrieben.

-   Das Feld " *AceType* " kann eine der folgenden Zeichen folgen sein.

    | ACE-Zeichenfolge | Konstante in SDDL. h                         | AceType-Wert                                   |
    |-----------------|--------------------------------------------|-------------------------------------------------|
    | Geleitet<br/> | SDDL- \_ Rückruf \_ Zugriff \_ zulässig<br/> | Zugriffs zulässiger \_ \_ Rückruf-ACE- \_ \_ Typ<br/> |
    | XD<br/> | SDDL- \_ Rückruf \_ Zugriff \_ verweigert<br/>  | \_Rückruf- \_ ACE \_ - \_ Typ für Zugriff verweigert<br/>  |

    

     

-   Die ACE-Zeichenfolge enthält einen oder mehrere bedingte Ausdrücke, die in Klammern am Ende der Zeichenfolge eingeschlossen werden.

## <a name="conditional-expressions"></a>Bedingte Ausdrücke

Ein bedingter Ausdruck kann eines der folgenden Elemente enthalten.



| Ausdruckselement                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *AttributeName*<br/>                                        | Testet, ob das angegebene Attribut einen Wert ungleich 0 (null) aufweist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|  *attributeName* ist vorhanden<br/>                             | Testet, ob das angegebene Attribut im Client Kontext vorhanden ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| *AttributeName* - *Operator* *Wert*<br/>                     | Gibt das Ergebnis des angegebenen Vorgangs zurück.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| * ConditionalExpression * **\|\|** _ConditionalExpression_<br/> | Testet, ob einer der angegebenen bedingten Ausdrücke True ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *ConditionalExpression* **&&** *ConditionalExpression*<br/> | Testet, ob beide angegebenen bedingten Ausdrücke True sind.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **! (**_ConditionalExpression_*_)_*<br/>                     | Die Umkehrung eines bedingten Ausdrucks.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Member \_ von {**_sidarray_*_}_*<br/>                         | Testet, ob das [**sid \_ -und \_ Attribute-**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) Array des Client Kontexts alle [Sicherheits](security-identifiers.md) -IDs (SIDs) in der durch Trennzeichen getrennten Liste enthält, die von *sidarray* angegeben wird.<br/> Für ACEs zulassen muss für eine Client Kontext-sid festgelegt sein, dass das Attribut der **SE- \_ Gruppe \_** als eine Entsprechung betrachtet wird.<br/> Bei deny-ACEs muss für eine Client Kontext-sid entweder die **SE- \_ Gruppe \_ aktiviert** sein, oder die Gruppe "SE", die für das Attribut " **\_ \_ \_ \_ \_ nur ablehnen" verwendet** werden soll.<br/> Das *sidarray* -Array kann entweder sid-Zeichen folgen (z. b. "S-1-5-6") oder sid-Aliase (z. b. "BA") enthalten.<br/> |



 

## <a name="attributes"></a>Attribute

Ein Attribut stellt ein Element im Informations Array der [**Authz- \_ Sicherheits \_ Attribute \_**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) im Client Kontext dar. Ein Attribut Name kann alle alphanumerischen Zeichen und jedes der Zeichen ":", "/", "." und " \_ " enthalten.

Bei einem Attribut Wert kann es sich um einen der folgenden Typen handeln:



| Werttyp         | BESCHREIBUNG                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Integer<br/> | Eine 64-Bit-Ganzzahl in Dezimal-oder hexadezimal Schreibweise.<br/>                                                                                                                              |
| String<br/>  | Ein durch Anführungszeichen getrennter Zeichen folgen Wert.<br/>                                                                                                                                                      |
| SID<br/>     | Sid (S-1-1-0) oder sid (BA). Muss Mitglied der RHS des Members \_ oder des Geräte \_ Mitglieds von sein \_ .<br/>                                                                                                           |
| BLOB<br/>    | \# gefolgt von hexadezimal Zahlen. Wenn die Länge der Zahlen ungerade ist, wird der in 0 (null) \# übersetzt, um dies zu tun. Außerdem \# wird ein, das an anderer Stelle im Wert angezeigt wird, in 0 übersetzt.<br/> |



 

## <a name="operators"></a>Operatoren

Die folgenden Operatoren sind für die Verwendung in bedingten Ausdrücken definiert, um die Werte von Attributen zu testen. Alle diese Operatoren sind binäre Operatoren und werden in der Form *attributeName* *Operator* *value* verwendet.



| Operator            | BESCHREIBUNG                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| ==<br/>       | Konventionelle Definition.<br/>                                                                                      |
| !=<br/>       | Konventionelle Definition.<br/>                                                                                      |
| <<br/>     | Konventionelle Definition.<br/>                                                                                      |
| <=<br/>    | Konventionelle Definition.<br/>                                                                                      |
| ><br/>     | Konventionelle Definition.<br/>                                                                                      |
| >=<br/>    | Konventionelle Definition.<br/>                                                                                      |
| Enthält<br/> | **True** , wenn der Wert des angegebenen Attributs eine übergeordnete Menge des angegebenen Werts ist. andernfalls **false**.<br/>  |
| Beliebige \_ von<br/>  | **True** , wenn der angegebene Wert eine supermenge des Werts des angegebenen Attributs ist. andernfalls **false**. <br/> |



 

Außerdem sind die unären Operatoren vorhanden, Member \_ von und Negation (!) werden wie in der Tabelle bedingte Ausdrücke beschrieben definiert.

Dem "enthält"-Operator muss ein Leerraum vorangestellt und gefolgt werden, und dem "Any \_ of"-Operator muss ein Leerzeichen vorangestellt werden.

## <a name="operator-precedence"></a>Operatorrangfolge

Die Operatoren werden in der folgenden Rangfolge ausgewertet, wobei Vorgänge mit gleicher Rangfolge von links nach rechts ausgewertet werden.

1.  Vorhanden, Mitglied \_ von
2.  Enthält, beliebige \_ von
3.  = =,! =, <, <=, >, >=
4.  !
5.  &&
6.  \|\|

Außerdem kann jeder Teil eines bedingten Ausdrucks in Klammern eingeschlossen werden. Ausdrücke in Klammern werden zuerst ausgewertet.

## <a name="unknown-values"></a>Unbekannte Werte

Die Ergebnisse der bedingten Ausdrücke geben mitunter den Wert **Unknown** zurück. Beispielsweise geben alle relationalen Vorgänge " **Unknown** " zurück, wenn das angegebene Attribut nicht vorhanden ist.

In der folgenden Tabelle werden die Ergebnisse für eine logische **and-** Operation zwischen zwei bedingten Ausdrücken, *ConditionalExpression1* und *ConditionalExpression2*, beschrieben.



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



 

In der folgenden Tabelle werden die Ergebnisse für eine logische **or** -Operation zwischen zwei bedingten Ausdrücken, *ConditionalExpression1* und *ConditionalExpression2*, beschrieben.



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



 

Die Negation eines bedingten Ausdrucks mit dem Wert " **Unknown** " ist ebenfalls **unbekannt**.

## <a name="conditional-ace-evaluation"></a>Auswertung bedingter ACE

In der folgenden Tabelle wird das Ergebnis der Zugriffs Überprüfung eines bedingten ACE in Abhängigkeit von der abschließenden Auswertung des bedingten Ausdrucks beschrieben.

| ACE-Typ         | TRUE             | false                 | UNKNOWN               |
|------------------|------------------|-----------------------|-----------------------|
| Zulassen<br/> | Zulassen<br/> | ACE ignorieren<br/> | ACE ignorieren<br/> |
| Verweigern<br/>  | Verweigern<br/>  | ACE ignorieren<br/> | Verweigern<br/>       |



 

## <a name="examples"></a>Beispiele

In den folgenden Beispielen wird veranschaulicht, wie die angegebenen Zugriffsrichtlinien durch einen bedingten ACE dargestellt werden, der mithilfe von SDDL definiert wurde.

<dl> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy
</dt> <dd>

Execute für alle zulassen, wenn die beiden folgenden Bedingungen erfüllt sind:

-   Titel = pm
-   Division = Finanzen oder Division = Verkäufe

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D: (XA;; FX;;; S-1-1-0; ( @User.Title = = "PM"  &&  ( @User.Division = = "Finance" \| \| @User.Division = = "Sales")))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy
</dt> <dd>

Execute Execute, wenn eines der Benutzer-Projekte mit den Datei-Projekten Intersect.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D: (XA;; FX;;; S-1-1-0; ( @User.Project Any \_ von @Resource.Project ))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Policy
</dt> <dd>

Lesezugriff zulassen, wenn der Benutzer sich mit einer Smartcard angemeldet hat, ein Sicherungs Operator ist und eine Verbindung von einem Computer mit aktiviertem BitLocker herstellt.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D: (XA;; Fr;;; S-1-1-0; (Mitglied \_ von {sid (Smartcard- \_ SID), sid (BO)}  && @Device.Bitlocker ))

</dd> <dt>

 
</dt> <dd>

 

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[\[MS-DYP \] : Beschreibung der Sicherheits Beschreibungssprache](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

