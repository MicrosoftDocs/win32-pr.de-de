---
description: Die Listen und Tabellen in diesem Abschnitt zeigen die Ausgabe des generischen Formatierers. Beachten Sie, dass der generische Formatierer die Member DataType und dataqualifier der PropertyInfo-Struktur verwendet, um zu bestimmen, wie die angezeigten Daten formatiert werden sollen.
ms.assetid: cf3dc6cd-7b24-464a-9d2b-5e35c4e8825e
title: Generische formatiererausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf4b334dd717c7ff332c3b730afb57d4be611ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344660"
---
# <a name="generic-formatter-output"></a>Generische formatiererausgabe

Die Listen und Tabellen in diesem Abschnitt zeigen die Ausgabe des [*generischen Formatierers*](g.md). Beachten Sie, dass der generische Formatierer die Member **DataType** und **dataqualifier** der [**PropertyInfo**](propertyinfo.md) -Struktur verwendet, um zu bestimmen, wie die angezeigten Daten formatiert werden sollen.

Weitere Informationen und ein Beispiel für die Ausgabe eines bestimmten Eigenschafts Datentyps finden Sie unter:

-   [Prop- \_ Typ \_ void](/windows)
-   [Prop \_ - \_ typzusammenfassung](/windows)
-   [Prop \_ - \_ typbyte](/windows)
-   [Prop \_ - \_ typwort](/windows)
-   [Prop- \_ Typ \_ DWORD](/windows)
-   Der prop- \_ Typ \_ largeint (generischer Formatierer unterstützt nicht)
-   Prop \_ Type \_ addr (generischer Formatierer unterstützt nicht)
-   [Prop \_ - \_ typzeit](/windows)
-   [Prop \_ - \_ Zeichenfolge](/windows)
-   [\_ \_ IP-Adresse des prop-Typs \_](/windows)
-   Der prop- \_ Typ \_ byteswlapp \_ Word (veraltet). Weitere Informationen finden Sie unter [Prop \_ - \_ typwort](/windows).)
-   Der prop- \_ Typ \_ byteswlapp \_ DWORD (veraltet). Weitere Informationen finden Sie unter [Prop \_ Type \_ DWORD](/windows).
-   \_ \_ Typisierte Zeichenfolge des prop-Typs \_ (veraltet)
-   [Rohdaten des prop- \_ Typs \_ \_](/windows)
-   [Prop \_ - \_ typkommentar](/windows)
-   Der prop- \_ Typ \_ srcfriendlyname (generischer Formatierer unterstützt nicht)
-   Prop \_ Type \_ dstfriendlyname (generischer Formatierer unterstützt nicht)
-   "Prop \_ Type \_ TokenRing \_ Address" (generischer Formatierer unterstützt nicht)
-   Prop- \_ Typ- \_ f- \_ Adresse (generischer Formatierer unterstützt nicht)
-   "Prop \_ Type \_ Ethernet Address" \_ (generischer Formatierer unterstützt nicht)
-   \_Objekt Bezeichner des prop-Typs \_ \_ (generischer Formatierer unterstützt nicht)
-   \_ \_ \_ IP-Adresse der prop-Typ-Reben \_ (generischer Formatierer unterstützt nicht)
-   Prop \_ Type \_ var \_ len \_ Small \_ int (generischer Formatierer unterstützt nicht)

## <a name="prop_type_void-and-prop_type_comment"></a>"Prop \_ Type \_ void" und "prop \_ Type \_ comment"

In der folgenden Tabelle wird die generische Format Ausgabe für die Datentyp Eigenschaften " **Prop \_ Type \_ void** " und " **Prop \_ Type \_ comment** " aufgelistet.

In der Ausgabe Spalte Formatierer lautet der Wert der Daten in der Erfassung XYZ.



| Eigenschaftsqualifizierer            | Formatierer-Ausgabe                                      |
|-------------------------------|-------------------------------------------------------|
| Prop \_ Qual \_ None              | XYZ                                                   |
| Bereich für die Stütz \_ Qual \_             | XYZ                                                   |
| Prop \_ - \_ Bitfeld          | Veraltet                                              |
| Bezeichnung für "prop \_ Qual" \_ \_      | XYZ                                                   |
| Prop \_ Qual mit \_ Bezeichnung als \_ Bitfeld | Veraltet. Weitere Informationen finden Sie unter Prop- \_ Qual- \_ Flags. |
| Prop \_ Qual \_ konstant             | XYZ                                                   |
| Prop- \_ Qual- \_ Flags             | XYZ                                                   |
| Prop- \_ Qual- \_ Array             | XYZ                                                   |



 

## <a name="prop_type_summary"></a>Prop \_ - \_ typzusammenfassung

In der folgenden Tabelle wird die generische Format Ausgabe für die Datentyp Eigenschaften der **Prop- \_ \_ typzusammenfassung** aufgelistet.

In der Beispielausgabe Spalte lautet der Wert der Daten in der Erfassung XYZ.



| Eigenschaftsqualifizierer            | Beispielausgabe                                        |
|-------------------------------|-------------------------------------------------------|
| Prop \_ Qual \_ None              | XYZ                                                   |
| Bereich für die Stütz \_ Qual \_             | XYZ                                                   |
| Prop \_ - \_ Bitfeld          | Veraltet                                              |
| Bezeichnung für "prop \_ Qual" \_ \_      | XYZ                                                   |
| Prop \_ Qual mit \_ Bezeichnung als \_ Bitfeld | Veraltet. Weitere Informationen finden Sie unter Prop- \_ Qual- \_ Flags. |
| Prop \_ Qual \_ konstant             | XYZ                                                   |
| Prop- \_ Qual- \_ Flags             | XYZ                                                   |
| Prop- \_ Qual- \_ Array             | XYZ                                                   |



 

## <a name="prop_type_byte"></a>Prop \_ - \_ typbyte

In der folgenden Tabelle wird die generische Format Ausgabe für die Datentyp Eigenschaften des **Datentyps Prop \_ Type \_** aufgelistet.

In der Beispielausgabe Spalte lautet der Wert der Daten in der Erfassung 10.



| Eigenschaftsqualifizierer            | Beispielausgabe                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------|
| Prop \_ Qual \_ None              | 10 (0xa) "                                                                                                     |
| Bereich für die Stütz \_ Qual \_             | 10 (0xa)-Bereich:(1 (0x1)-20 (0x14))                                                                          |
| Prop- \_ Qual- \_ Satz               | 10 (0xa) entspricht dem festgelegten Wert oder<br/> 10 (0xa) unbekannter festgelegtem Wert<br/>                                |
| Prop \_ - \_ Bitfeld          | Veraltet.                                                                                                     |
| Bezeichnung für "prop \_ Qual" \_ \_      | Entsprechende Bezeichnung in einem Bezeichnungs Satz oder einer Zahl.                                                                 |
| Prop \_ Qual mit \_ Bezeichnung als \_ Bitfeld | Veraltet. Weitere Informationen finden Sie unter Prop- \_ Qual- \_ Flags.                                                        |
| Prop \_ Qual \_ konstant             | Keine Ausgabe. Im Detailbereich werden keine Daten angezeigt.                                                           |
| Prop- \_ Qual- \_ Flags             | ....... 0 = Bezeichnung aus Zeichenfolge...... 1. = Bezeichnung in Zeichenfolge.... 0.. = Bezeichnung aus Zeichenfolge.... 1... = Bezeichnung für Zeichenfolge |
| Prop- \_ Qual- \_ Array             | 0a ff...                                                                                                     |



 

## <a name="prop_type_word"></a>Prop \_ - \_ typwort

In der folgenden Tabelle ist die generische Format Ausgabe für eine Eigenschaft vom Typ " **Prop \_ Type \_ Word** Data Type" aufgeführt.

> [!Note]  
> Bei nicht-Intel-DWORD-Eigenschaften, die im Byte ausgetauscht wurden, müssen Sie die Daten in ein Intel-Format ändern. Um das Format zu ändern, legen Sie den *IFlags* - **Parameter der** anfügenschafteninstanzfunktion fest, die \_ beim Zuordnen der Eigenschafts Instanz zu einem Speicherort ausgetauscht wurde.

 

In der Beispielausgabe Spalte lautet der Wert der Daten in der Erfassung 10.



| Eigenschaftsqualifizierer            | Beispielausgabe                                                                                                                                                                                                                |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prop \_ Qual \_ None              | 10 (0xa)                                                                                                                                                                                                                      |
| Bereich für die Stütz \_ Qual \_             | 10 (0xa)-Bereich:(1 (0x1)-20 (0x14))                                                                                                                                                                                          |
| Prop- \_ Qual- \_ Satz               | 10 (0xa) entspricht dem festgelegten Wert oder<br/> 10 (0xa) unbekannter festgelegtem Wert<br/>                                                                                                                                                |
| Prop \_ - \_ Bitfeld          | Veraltet.                                                                                                                                                                                                                     |
| Bezeichnung für "prop \_ Qual" \_ \_      | Entsprechende Bezeichnung im Bezeichnungs Satz oder der Bezeichnung.                                                                                                                                                                               |
| Prop \_ Qual mit \_ Bezeichnung als \_ Bitfeld | Veraltet. Weitere Informationen finden Sie unter Prop- \_ Qual- \_ Flags.                                                                                                                                                                        |
| Prop \_ Qual \_ konstant             | Keine Ausgabe. Im Detailbereich werden keine Daten angezeigt.                                                                                                                                                                           |
| Prop- \_ Qual- \_ Flags             | ....... 0 = Bezeichnung aus Zeichenfolge...... 1,0. = Bezeichnung aus Zeichenfolge.... 0.. = Bezeichnung aus Zeichenfolge.... 0... = Bezeichnung aus Zeichenfolge... 0.... = Bezeichnung aus Zeichenfolge... 1.... = Bezeichnung für String. 0...... = Bezeichnung aus Zeichenfolge 1....... = Bezeichnung in Zeichenfolge |
| Prop- \_ Qual- \_ Array             | 000A FFFF...                                                                                                                                                                                                                 |



 

## <a name="prop_type_dword"></a>Prop- \_ Typ \_ DWORD

In der folgenden Tabelle wird die generische Format Ausgabe für die Eigenschaften des **\_ \_ DWORD** -Datentyps Prop Type aufgelistet.

> [!Note]  
> Bei nicht-Intel-DWORD-Eigenschaften, die im Byte ausgetauscht wurden, müssen Sie die Daten in ein Intel-Format ändern. Um das Format zu ändern, legen Sie den *IFlags* - **Parameter der** anfügenschafteninstanzfunktion fest, die \_ beim Zuordnen der Eigenschafts Instanz zu einem Speicherort ausgetauscht wurde.

 

In der Beispielausgabe Spalte lautet der Wert der Daten in der Erfassung 10.



| Eigenschaftsqualifizierer            | Beispielausgabe                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Prop \_ Qual \_ None              | 10 (0xa)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Bereich für die Stütz \_ Qual \_             | 10 (0xa)-Bereich:(1 (0x1)-20 (0x14))                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Prop- \_ Qual- \_ Satz               | 10 (0xa) entspricht dem festgelegten Wert oder<br/> 10 (0xa) unbekannter festgelegtem Wert<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Prop \_ - \_ Bitfeld          | Veraltet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Bezeichnung für "prop \_ Qual" \_ \_      | Entsprechende Bezeichnung in der Bezeichnungs Gruppe oder-Nummer.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Prop \_ Qual mit \_ Bezeichnung als \_ Bitfeld | Veraltet. Weitere Informationen finden Sie unter Prop- \_ Qual- \_ Flags.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Prop \_ Qual \_ konstant             | Keine Ausgabe. Im Detailbereich werden keine Daten angezeigt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Prop- \_ Qual- \_ Flags             | ............... 0 = Bezeichnung aus Zeichenfolge................... 1,0. = Bezeichnung aus Zeichenfolge............. 0.. = Bezeichnung aus Zeichenfolge................ 0... = Bezeichnung aus Zeichenfolge................ 0.... = Bezeichnung aus Zeichenfolge.......... 0.... = Bezeichnung aus Zeichenfolge......... 0...... = Bezeichnung aus Zeichenfolge....... 0....... = Bezeichnung aus Zeichenfolge....... 0....... = Bezeichnung aus Zeichenfolge...... 0......... = Bezeichnung aus Zeichenfolge.... 0.......... = Bezeichnung aus Zeichenfolge.... 0................ = Bezeichnung aus Zeichenfolge... 0............ = Bezeichnung aus Zeichenfolge... 1.......................................... = Bezeichnung aus Zeichenfolge 1.................... = Bezeichnung in Zeichenfolge |
| Prop- \_ Qual- \_ Array             | 0000000A FFFFFFFF...                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="prop_type_raw_data"></a>Rohdaten des prop- \_ Typs \_ \_

In der folgenden Tabelle sind die generischen Format Ausgaben für eine Eigenschaft des Datentyps für den **Prop- \_ \_ \_ typrohdaten** Beachten Sie, dass die formatiererausgabe nicht die Rohdaten anzeigt, sondern die Eigenschaften Bezeichnung anzeigt.



| Eigenschaftsqualifizierer            | Formatierer-Ausgabe |
|-------------------------------|------------------|
| Prop \_ Qual \_ None              | Eigenschaften Bezeichnung.  |
| Bereich für die Stütz \_ Qual \_             | Eigenschaften Bezeichnung.  |
| Prop \_ - \_ Bitfeld          | Eigenschaften Bezeichnung.  |
| Bezeichnung für "prop \_ Qual" \_ \_      | Eigenschaften Bezeichnung.  |
| Prop \_ Qual mit \_ Bezeichnung als \_ Bitfeld | Eigenschaften Bezeichnung.  |
| Prop \_ Qual \_ konstant             | Eigenschaften Bezeichnung.  |
| Prop- \_ Qual- \_ Flags             | Eigenschaften Bezeichnung.  |
| Prop- \_ Qual- \_ Array             | Eigenschaften Bezeichnung.  |



 

## <a name="prop_type_time"></a>Prop \_ - \_ typzeit

In der folgenden Tabelle wird die generische Format Ausgabe für eine Eigenschaft vom Datentyp " **Prop \_ Type \_ time** " aufgelistet. Beachten Sie, dass die formatierte Ausgabe abhängig vom Daten Qualifizierer der Eigenschaft variieren kann.

Der generische Formatierer ruft [**getDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) auf, um eine Zeit zu erhalten, die auf der Systemuhr des lokalen Computers basiert.



| Eigenschaftsqualifizierer            | Formatierer-Ausgabe                                            |
|-------------------------------|-------------------------------------------------------------|
| Prop \_ Qual \_ None              | Zeigt die Systemzeit auf der Grundlage der lokalen Computeruhr an. |
| Bereich für die Stütz \_ Qual \_             | Zeigt die Systemzeit auf der Grundlage der lokalen Computeruhr an. |
| Prop \_ - \_ Bitfeld          | Veraltet.                                                   |
| Bezeichnung für "prop \_ Qual" \_ \_      | Zeigt die Systemzeit auf der Grundlage der lokalen Computeruhr an. |
| Prop \_ Qual mit \_ Bezeichnung als \_ Bitfeld | Veraltet. Weitere Informationen finden Sie unter Prop- \_ Qual- \_ Flags.      |
| Prop \_ Qual \_ konstant             | Zeigt die Systemzeit auf der Grundlage der lokalen Computeruhr an. |
| Prop- \_ Qual- \_ Flags             | Zeigt die Systemzeit auf der Grundlage der lokalen Computeruhr an. |
| Prop- \_ Qual- \_ Array             | Zeigt die Systemzeit auf der Grundlage der lokalen Computeruhr an. |



 

## <a name="prop_type_string"></a>Prop \_ - \_ Zeichenfolge

In der folgenden Tabelle wird die generische Format Ausgabe für die Datentyp Eigenschaften des **Prop- \_ Typs \_ String** aufgelistet. Beachten Sie, dass die formatiererausgabe je nach Daten Qualifizierer der Eigenschaft variieren kann.



| Eigenschaftsqualifizierer            | Formatierer-Ausgabe                                       |
|-------------------------------|--------------------------------------------------------|
| Prop \_ Qual \_ None              | Angefügte Zeichenfolge.                                       |
| Bereich für die Stütz \_ Qual \_             | Angefügte Zeichenfolge.                                       |
| Prop \_ - \_ Bitfeld          | Veraltet.                                              |
| Bezeichnung für "prop \_ Qual" \_ \_      | Angefügte Zeichenfolge.                                       |
| Prop \_ Qual mit \_ Bezeichnung als \_ Bitfeld | Veraltet. Weitere Informationen finden Sie unter Prop- \_ Qual- \_ Flags. |
| Prop \_ Qual \_ konstant             | Angefügte Zeichenfolge.                                       |
| Prop- \_ Qual- \_ Flags             | Angefügte Zeichenfolge.                                       |
| Prop- \_ Qual- \_ Array             | Angefügte Zeichenfolge.                                       |



 

## <a name="prop_type_ip_address"></a>\_ \_ IP-Adresse des prop-Typs \_

In der folgenden Tabelle sind die generischen Format Ausgaben für die Eigenschaften des Typs **\_ \_ IP- \_ Adresse des prop-Typs** aufgelistet. Beachten Sie, dass die formatierte Ausgabe je nach dem Qualifizierer der Eigenschaften Daten der Eigenschaft variieren kann.

In der Beispielausgabe Spalte lautet der Wert der Daten in der Erfassung "129.65.100.2".



| Eigenschaftsqualifizierer            | Beispielausgabe                                         |
|-------------------------------|--------------------------------------------------------|
| Prop \_ Qual \_ None              | 129.65.100.2                                           |
| Bereich für die Stütz \_ Qual \_             | 129.65.100.2                                           |
| Prop \_ - \_ Bitfeld          | Veraltet.                                              |
| Bezeichnung für "prop \_ Qual" \_ \_      | 129.65.100.2                                           |
| Prop \_ Qual mit \_ Bezeichnung als \_ Bitfeld | Veraltet. Weitere Informationen finden Sie unter Prop- \_ Qual- \_ Flags. |
| Prop \_ Qual \_ konstant             | 129.65.100.2                                           |
| Prop- \_ Qual- \_ Flags             | 129.65.100.2                                           |
| Prop- \_ Qual- \_ Array             | 129.65.100.2                                           |



 

 

