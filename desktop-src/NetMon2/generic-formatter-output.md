---
description: Die Listen und Tabellen in diesem Abschnitt zeigen die Ausgabe des generischen Formatierungsformatierers. Beachten Sie, dass das generische Formatierer die Member DataType und DataQualifier der PROPERTYINFO-Struktur verwendet, um zu bestimmen, wie die angezeigten Daten formatiert werden sollen.
ms.assetid: cf3dc6cd-7b24-464a-9d2b-5e35c4e8825e
title: Generische Formatierungsausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d76a67fadbed3bde5eb3e5534c8f104e918ac870df27c767b98575058a0a188
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743970"
---
# <a name="generic-formatter-output"></a>Generische Formatierungsausgabe

Die Listen und Tabellen in diesem Abschnitt zeigen die Ausgabe des [*generischen Formatierungs-.*](g.md) Beachten Sie, dass das generische Formatierer die **Member DataType** und **DataQualifier** der [**PROPERTYINFO-Struktur**](propertyinfo.md) verwendet, um zu bestimmen, wie die angezeigten Daten formatiert werden sollen.

Weitere Informationen und ein Beispiel für die Ausgabe für einen bestimmten Eigenschaftsdatentyp finden Sie unter:

-   [PROP \_ TYPE \_ VOID](/windows)
-   [\_ZUSAMMENFASSUNG DES PROP-TYPS \_](/windows)
-   [PROP \_ TYPE \_ BYTE](/windows)
-   [PROP \_ TYPE \_ WORD](/windows)
-   [PROP \_ TYPE \_ DWORD](/windows)
-   PROP \_ TYPE \_ LARGEINT (generisches Formatierungsformatierer wird nicht unterstützt)
-   PROP \_ TYPE \_ ADDR (generisches Formatierungsformatierer wird nicht unterstützt)
-   [PROP \_ TYPE \_ TIME](/windows)
-   [PROP \_ TYPE \_ STRING](/windows)
-   [\_PROP TYPE IP ADDRESS \_ (IP-ADRESSE DES PROP-TYPS) \_](/windows)
-   PROP \_ TYPE \_ BYTESWAPPED \_ WORD (Obsolete. Weitere Informationen finden Sie unter [PROP \_ TYPE \_ WORD](/windows))
-   PROP \_ TYPE \_ BYTESWAPPED \_ DWORD (Obsolete. Weitere Informationen finden Sie unter [PROP \_ TYPE \_ DWORD](/windows))
-   TYPISIERTE ZEICHENFOLGE VOM TYP PROP \_ \_ \_ (veraltet)
-   [PROP \_ TYPE \_ RAW \_ DATA](/windows)
-   [PROP \_ TYPE \_ COMMENT](/windows)
-   PROP \_ TYPE \_ SRCFRIENDLYNAME (generisches Formatierungsformatierer wird nicht unterstützt)
-   PROP \_ TYPE \_ DSTFRIENDLYNAME (generisches Formatierungsformatierer wird nicht unterstützt)
-   PROP \_ TYPE \_ TOKENRING ADDRESS \_ (generisches Formatierungsformatierer wird nicht unterstützt)
-   PROP \_ TYPE \_ FDDI \_ ADDRESS (generisches Formatierungsformatierer wird nicht unterstützt)
-   PROP \_ TYPE ETHERNET ADDRESS \_ \_ (generisches Formatierungsformatierer wird nicht unterstützt)
-   PROP \_ TYPE OBJECT IDENTIFIER \_ \_ (generisches Formatierungsformatierer wird nicht unterstützt)
-   PROP \_ TYPE \_ VINES IP ADDRESS \_ \_ (generisches Formatierungsformatierer wird nicht unterstützt)
-   PROP \_ TYPE \_ VAR \_ LEN SMALL \_ \_ INT (generisches Formatierungsformatierer wird nicht unterstützt)

## <a name="prop_type_void-and-prop_type_comment"></a>PROP \_ TYPE VOID und PROP TYPE \_ \_ \_ COMMENT

In der folgenden Tabelle ist die generische Formatausgabe für die Eigenschaften **PROP \_ TYPE \_ VOID** und **PROP TYPE \_ \_ COMMENT** aufgeführt.

In der Ausgabespalte des Formatierungsformatierers lautet der Wert der Daten in der Erfassung XYZ.



| Eigenschaftsqualifizierer            | Formatierungsausgabe                                      |
|-------------------------------|-------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | XYZ                                                   |
| PROP \_ QUAL \_ RANGE             | XYZ                                                   |
| PROP \_ QUAL \_ BITFIELD          | Veraltet                                              |
| PROP \_ QUAL \_ LABELED \_ SET      | XYZ                                                   |
| PROP \_ QUAL \_ BEZEICHNETES \_ BITFIELD | Veraltet. Weitere Informationen finden Sie unter PROP \_ QUAL \_ FLAGS. |
| PROP \_ QUAL \_ CONST             | XYZ                                                   |
| \_ \_ PROP-QUAL-FLAGS             | XYZ                                                   |
| PROP \_ QUAL \_ ARRAY             | XYZ                                                   |



 

## <a name="prop_type_summary"></a>\_ZUSAMMENFASSUNG DES PROP-TYPS \_

In der folgenden Tabelle ist die generische Formatausgabe für eigenschaften des **PROP \_ TYPE \_ SUMMARY-Datentyps** aufgeführt.

In der Beispielausgabespalte lautet der Wert der Daten in der Erfassung XYZ.



| Eigenschaftsqualifizierer            | Beispielausgabe                                        |
|-------------------------------|-------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | XYZ                                                   |
| PROP \_ QUAL \_ RANGE             | XYZ                                                   |
| PROP \_ QUAL \_ BITFIELD          | Veraltet                                              |
| PROP \_ QUAL \_ LABELED \_ SET      | XYZ                                                   |
| PROP \_ QUAL \_ BEZEICHNETES \_ BITFIELD | Veraltet. Weitere Informationen finden Sie unter PROP \_ QUAL \_ FLAGS. |
| PROP \_ QUAL \_ CONST             | XYZ                                                   |
| \_ \_ PROP-QUAL-FLAGS             | XYZ                                                   |
| PROP \_ QUAL \_ ARRAY             | XYZ                                                   |



 

## <a name="prop_type_byte"></a>PROP \_ TYPE \_ BYTE

In der folgenden Tabelle ist die generische Formatausgabe für EIGENSCHAFTEN des **PROP \_ TYPE \_ BYTE-Datentyps** aufgeführt.

In der Beispielausgabespalte ist der Wert der Daten in der Erfassung 10.



| Eigenschaftsqualifizierer            | Beispielausgabe                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | 10 (0xa)"                                                                                                     |
| PROP \_ QUAL \_ RANGE             | 10 (0xa) Bereich: (1 (0x1) - 20 (0x14))                                                                          |
| PROP \_ QUAL \_ SET               | 10 (0xa) entspricht dem festgelegten Wert oder<br/> 10 (0xa) Unbekannter Set-Wert<br/>                                |
| PROP \_ QUAL \_ BITFIELD          | Veraltet.                                                                                                     |
| PROP \_ QUAL \_ LABELED \_ SET      | Entsprechende Bezeichnung in einem Bezeichnungssatz oder einer Bezeichnungsnummer.                                                                 |
| PROP \_ QUAL \_ BEZEICHNETES \_ BITFIELD | Veraltet. Weitere Informationen finden Sie unter PROP \_ QUAL \_ FLAGS.                                                        |
| PROP \_ QUAL \_ CONST             | Keine Ausgabe. Im Detailbereich werden keine Daten angezeigt.                                                           |
| \_ \_ PROP-QUAL-FLAGS             | ....... 0 = Label Off String ...... 1. = Label On String ..... 0.. = Label Off String .... 1... = Bezeichnung für Zeichenfolge |
| PROP \_ QUAL \_ ARRAY             | 0a ff ...                                                                                                     |



 

## <a name="prop_type_word"></a>PROP \_ TYPE \_ WORD

In der folgenden Tabelle ist die generische Formatausgabe für eine **\_ PROP TYPE \_ WORD-Datentypeigenschaft** aufgeführt.

> [!Note]  
> Bei DWORD-Eigenschaften ohne Intel-Bytetausch müssen Sie die Daten in ein Intel-Format ändern. Um das Format zu ändern, legen Sie den *IFlags-Parameter* der Attach-Eigenschaftsinstanzfunktion IFLAG  \_ SWAPPED fest, wenn Sie die Eigenschafteninstanz einem Speicherort zuordnen.

 

In der Beispielausgabespalte ist der Wert der Daten in der Erfassung 10.



| Eigenschaftsqualifizierer            | Beispielausgabe                                                                                                                                                                                                                |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | 10 (0xa)                                                                                                                                                                                                                      |
| PROP \_ QUAL \_ RANGE             | 10 (0xa) Bereich: (1 (0x1) - 20 (0x14))                                                                                                                                                                                          |
| PROP \_ QUAL \_ SET               | 10 (0xa) entspricht dem festgelegten Wert oder<br/> 10 (0xa) Unbekannter Set-Wert<br/>                                                                                                                                                |
| PROP \_ QUAL \_ BITFIELD          | Veraltet.                                                                                                                                                                                                                     |
| PROP \_ QUAL \_ LABELED \_ SET      | Entsprechende Bezeichnung im Bezeichnungssatz oder in der Bezeichnungsnummer.                                                                                                                                                                               |
| PROP \_ QUAL \_ BEZEICHNETES \_ BITFIELD | Veraltet. Weitere Informationen finden Sie unter PROP \_ QUAL \_ FLAGS.                                                                                                                                                                        |
| PROP \_ QUAL \_ CONST             | Keine Ausgabe. Im Detailbereich werden keine Daten angezeigt.                                                                                                                                                                           |
| \_ \_ PROP-QUAL-FLAGS             | ....... 0 = Label Off String ...... 0. = Label Off String ..... 0.. = Label Off String .... 0... = Label Off String ... 0.... = Label Off String .. 1..... = Bezeichnung für Zeichenfolge .0...... = Label Off String 1....... = Bezeichnung für Zeichenfolge |
| PROP \_ QUAL \_ ARRAY             | 000a ffff ...                                                                                                                                                                                                                 |



 

## <a name="prop_type_dword"></a>PROP \_ TYPE \_ DWORD

In der folgenden Tabelle ist die generische Formatausgabe für EIGENSCHAFTEN des **PROP \_ \_ TYPE-DWORD-Datentyps** aufgeführt.

> [!Note]  
> Bei DWORD-Eigenschaften ohne Intel-Bytetausch müssen Sie die Daten in ein Intel-Format ändern. Um das Format zu ändern, legen Sie den *IFlags-Parameter* der Attach-Eigenschaftsinstanzfunktion IFLAG  \_ SWAPPED fest, wenn Sie die Eigenschafteninstanz einem Speicherort zuordnen.

 

In der Beispielausgabespalte ist der Wert der Daten in der Erfassung 10.



| Eigenschaftsqualifizierer            | Beispielausgabe                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | 10 (0xa)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| PROP \_ QUAL \_ RANGE             | 10 (0xa) Bereich: (1 (0x1) - 20 (0x14))                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| PROP \_ QUAL \_ SET               | 10 (0xa) entspricht dem festgelegten Wert oder<br/> 10 (0xa) Unbekannter Set-Wert<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| PROP \_ QUAL \_ BITFIELD          | Veraltet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| PROP \_ QUAL \_ LABELED \_ SET      | Entsprechende Bezeichnung in Bezeichnungssatz oder Zahl.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROP \_ QUAL \_ BEZEICHNETES \_ BITFIELD | Veraltet. Weitere Informationen finden Sie unter PROP \_ QUAL \_ FLAGS.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| PROP \_ QUAL \_ CONST             | Keine Ausgabe. Im Detailbereich werden keine Daten angezeigt.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_ \_ PROP-QUAL-FLAGS             | ............... 0 = Label Off String .............. 0. = Label Off String ............. 0.. = Label Off String ............ 0... = Label Off String ........... 0.... = Label Off String .......... 0..... = Label Off String ......... 0...... = Label Off String ........ 0....... = Label Off String ....... 0........ = Label Off String ...... 0......... = Label Off String ..... 0.......... = Label Off String .... 0........... = Label Off String ... 0............ = Label Off String .. 1............. = Bezeichnung für Zeichenfolge .0.............. = Label Off String 1............... = Bezeichnung für Zeichenfolge |
| PROP \_ QUAL \_ ARRAY             | 0000000a ffffffff ...                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="prop_type_raw_data"></a>PROP \_ TYPE \_ RAW \_ DATA

In der folgenden Tabelle ist die generische Formatausgabe für eine **PROP \_ TYPE RAW \_ \_ DATA-Datentypeigenschaft** aufgeführt. Beachten Sie, dass die Formatierungsausgabe nicht die Rohdaten anzeigt, sondern die Eigenschaftenbezeichnung.



| Eigenschaftsqualifizierer            | Formatierungsausgabe |
|-------------------------------|------------------|
| PROP \_ QUAL \_ NONE              | Eigenschaftenbezeichnung.  |
| PROP \_ QUAL \_ RANGE             | Eigenschaftenbezeichnung.  |
| PROP \_ QUAL \_ BITFIELD          | Eigenschaftenbezeichnung.  |
| PROP \_ QUAL \_ LABELED \_ SET      | Eigenschaftenbezeichnung.  |
| PROP \_ QUAL \_ BEZEICHNETES \_ BITFIELD | Eigenschaftenbezeichnung.  |
| PROP \_ QUAL \_ CONST             | Eigenschaftenbezeichnung.  |
| \_ \_ PROP-QUAL-FLAGS             | Eigenschaftenbezeichnung.  |
| PROP \_ QUAL \_ ARRAY             | Eigenschaftenbezeichnung.  |



 

## <a name="prop_type_time"></a>PROP \_ TYPE \_ TIME

In der folgenden Tabelle ist die generische Formatausgabe für eine **PROP \_ TYPE \_ TIME-Datentypeigenschaft** aufgeführt. Beachten Sie, dass die formatierte Ausgabe abhängig vom Datenqualifizierer der Eigenschaft variieren kann.

Der generische Formatierer ruft [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) auf, um eine Zeit abzurufen, die auf der Systemuhr des lokalen Computers basiert.



| Eigenschaftsqualifizierer            | Formatierungsausgabe                                            |
|-------------------------------|-------------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | Zeigt die Systemzeit basierend auf der Uhr des lokalen Computers an. |
| PROP \_ QUAL \_ RANGE             | Zeigt die Systemzeit basierend auf der Uhr des lokalen Computers an. |
| PROP \_ QUAL \_ BITFIELD          | Veraltet.                                                   |
| PROP \_ QUAL \_ LABELED \_ SET      | Zeigt die Systemzeit basierend auf der Uhr des lokalen Computers an. |
| PROP \_ QUAL \_ BEZEICHNETES \_ BITFIELD | Veraltet. Weitere Informationen finden Sie unter PROP \_ QUAL \_ FLAGS.      |
| PROP \_ QUAL \_ CONST             | Zeigt die Systemzeit basierend auf der Uhr des lokalen Computers an. |
| \_ \_ PROP-QUAL-FLAGS             | Zeigt die Systemzeit basierend auf der Uhr des lokalen Computers an. |
| PROP \_ QUAL \_ ARRAY             | Zeigt die Systemzeit basierend auf der Uhr des lokalen Computers an. |



 

## <a name="prop_type_string"></a>PROP \_ TYPE \_ STRING

In der folgenden Tabelle ist die generische Formatausgabe für EIGENSCHAFTEN des **PROP \_ TYPE \_ STRING-Datentyps** aufgeführt. Beachten Sie, dass die Formatierungsausgabe abhängig vom Datenqualifizierer der Eigenschaft variieren kann.



| Eigenschaftsqualifizierer            | Formatierungsausgabe                                       |
|-------------------------------|--------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | Angefügte Zeichenfolge.                                       |
| PROP \_ QUAL \_ RANGE             | Angefügte Zeichenfolge.                                       |
| PROP \_ QUAL \_ BITFIELD          | Veraltet.                                              |
| PROP \_ QUAL \_ LABELED \_ SET      | Angefügte Zeichenfolge.                                       |
| PROP \_ QUAL \_ BEZEICHNETES \_ BITFIELD | Veraltet. Weitere Informationen finden Sie unter PROP \_ QUAL \_ FLAGS. |
| PROP \_ QUAL \_ CONST             | Angefügte Zeichenfolge.                                       |
| \_ \_ PROP-QUAL-FLAGS             | Angefügte Zeichenfolge.                                       |
| PROP \_ QUAL \_ ARRAY             | Angefügte Zeichenfolge.                                       |



 

## <a name="prop_type_ip_address"></a>\_PROP TYPE IP ADDRESS \_ (IP-ADRESSE DES PROP-TYPS) \_

In der folgenden Tabelle ist die generische Formatausgabe für EIGENSCHAFTEN des **PROP \_ TYPE IP \_ \_ ADDRESS-Datentyps** aufgeführt. Beachten Sie, dass die formatierte Ausgabe abhängig vom Eigenschaftsdatenqualifizierer der Eigenschaft variieren kann.

In der Beispielausgabespalte lautet der Wert der Daten in der Erfassung "129.65.100.2".



| Eigenschaftsqualifizierer            | Beispielausgabe                                         |
|-------------------------------|--------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | 129.65.100.2                                           |
| PROP \_ QUAL \_ RANGE             | 129.65.100.2                                           |
| PROP \_ QUAL \_ BITFIELD          | Veraltet.                                              |
| PROP \_ QUAL \_ LABELED \_ SET      | 129.65.100.2                                           |
| PROP \_ QUAL \_ BEZEICHNETES \_ BITFIELD | Veraltet. Weitere Informationen finden Sie unter PROP \_ QUAL \_ FLAGS. |
| PROP \_ QUAL \_ CONST             | 129.65.100.2                                           |
| \_ \_ PROP-QUAL-FLAGS             | 129.65.100.2                                           |
| PROP \_ QUAL \_ ARRAY             | 129.65.100.2                                           |



 

 

