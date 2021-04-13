---
title: Stringfilanfo-Block Anweisung
description: Beschreibt die Form des Zeichen folgen Informations Blocks.
ms.assetid: d5edf638-b70a-44d0-a43a-89d4d21e679f
keywords:
- Stringfilanfo-Block Anweisungs Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- StringFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb0a1c5e7a2fd5e3d2f096c882ca928ce1febf92
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389185"
---
# <a name="stringfileinfo-block-statement"></a>Stringfilanfo-Block Anweisung

Definiert einen Zeichen folgen-Informationsblock.

``` syntax
BLOCK "StringFileInfo" { BLOCK "lang-charset" {VALUE "string-name", "value" . . . }}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lang-charset"></span><span id="LANG-CHARSET"></span>*lang-charset*
</dt> <dd>

Sprach-und Zeichensatz-Bezeichnerpaar. Dabei handelt es sich um eine hexadezimale Zeichenfolge, die aus der Verkettung der Sprach-und Zeichensatz Bezeichner besteht, die im Abschnitt "Hinweise" angegeben sind.

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*Zeichen folgen Name*
</dt> <dd>

Der Name eines Werts im Block und kann einer der vordefinierten Namen sein, die im Abschnitt "Hinweise" angegeben sind.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Wert*
</dt> <dd>

Zeichenfolge, die den Wert des entsprechenden Zeichen folgen namens angibt. Es können mehr als eine **value** -Anweisung angegeben werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der *lang-charset-* Parameter gibt einen der folgenden Sprachcodes an.



| Code   | Sprache            | Code   | Sprache                  |
|--------|---------------------|--------|---------------------------|
| 0x0401 | Arabisch              | 0x0415 | Polnisch                    |
| 0x0402 | Bulgarisch           | 0x0416 | Portugiesisch (Brasilien)       |
| 0x0403 | Katalanisch             | 0x0417 | Rhaeto-Romanic            |
| 0x0404 | Chinesisch (traditionell) | 0x0418 | Rumänisch                  |
| 0x0405 | Tschechisch               | 0x0419 | Russisch                   |
| 0x0406 | Dänisch              | 0x041a | Croato-Serbian (lateinisch)    |
| 0x0407 | Deutsch              | 0x041b | Slowakisch                    |
| 0x0408 | Griechisch               | 0x041c | Albanisch                  |
| 0x0409 | US-Englisch        | 0x041d | Schwedisch                   |
| 0x040A | Castilisch Spanisch   | 0x041E | Thailändisch                      |
| 0x040b | Finnisch             | 0x041f | Türkisch                   |
| 0x040c | Französisch              | 0x0420 | Urdu                      |
| 0x040d | Hebräisch              | 0x0421 | Bahasa                    |
| 0x040e | Ungarisch           | 0x0804 | Chinesisch (vereinfacht)        |
| 0x040f | Isländisch           | 0x0807 | Deutsch (Schweiz)              |
| 0x0410 | Italienisch             | 0x0809 | Vereinigtes Königreich: Englisch              |
| 0x0411 | Japanisch            | 0x080a | Spanisch (Mexiko)          |
| 0x0412 | Koreanisch              | 0x080c | Französisch (Belgien)            |
| 0x0413 | Niederländisch               | 0x0c0c | Französisch (Kanada)           |
| 0x0414 | Norwegisch – Bokmal  | 0x100c | Schweiz Französisch              |
| 0x0810 | Schweizer Italienisch       | 0x0816 | Portugiesisch (Portugal)     |
| 0x0813 | Belgisch Niederländisch       | 0x081a | Serbo-Croatian (Kyrillisch) |
| 0x0814 | Norwegisch – Nynorsk | ?      | ?                         |



 

Der *lang-charset-* Parameter gibt auch einen der folgenden Zeichensatz Bezeichner an.



| Bezeichner | Zeichensatz              |
|------------|----------------------------|
| 0          | 7-Bit-ASCII                |
| 932        | Japan (Shift – JIS X-0208) |
| 949        | Korea (Shift – KSC 5601)   |
| 950        | Taiwan (Big5)              |
| 1200       | Unicode                    |
| 1250       | Lateinisch-2 (Osteuropäisch) |
| 1251       | Kyrillisch                   |
| 1252       | Mehrsprachige               |
| 1253       | Griechisch                      |
| 1254       | Türkisch                    |
| 1255       | Hebräisch                     |
| 1256       | Arabisch                     |



 

Der *String-Name-* Parameter gibt einen der folgenden vordefinierten Namen an.



| Name                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kommentare**         | Zusätzliche Informationen, die zu Diagnose Zwecken angezeigt werden sollten.                                                                                                                                                                                                                                    |
| **CompanyName**      | Das Unternehmen, das die Datei erstellt hat – z. b. "Microsoft Corporation" oder "Standard Microsystems Corporation, Inc." Diese Zeichenfolge ist erforderlich.                                                                                                                                                                   |
| **FileDescription**  | Die Dateibeschreibung, die Benutzern angezeigt werden soll. Diese Zeichenfolge wird möglicherweise in einem Listenfeld angezeigt, wenn der Benutzer die zu installierenden Dateien auswählt – z. b. "Tastaturtreiber für AT-Style-Tastaturen". Diese Zeichenfolge ist erforderlich.                                                                                            |
| **FileVersion**      | Versionsnummer der Datei – z. b. "3,10" oder "5.00. RC2". Diese Zeichenfolge ist erforderlich.                                                                                                                                                                                                                      |
| **InternalName**     | Interner Name der Datei (sofern vorhanden) – z. b. ein Modulname, wenn es sich bei der Datei um eine Dynamic Link Library handelt. Wenn die Datei keinen internen Namen hat, sollte diese Zeichenfolge der ursprüngliche Dateiname ohne Erweiterung sein. Diese Zeichenfolge ist erforderlich.                                                                       |
| **LegalCopyright**   | Copyright Hinweise, die für die Datei gelten. Dies sollte den vollständigen Text aller Hinweise, rechtliche Symbole, Copyright Daten usw. enthalten. Diese Zeichenfolge ist optional.                                                                                                                                             |
| **LegalTrademarks**  | Marken und eingetragene Marken, die auf die Datei angewendet werden. Dies sollte den vollständigen Text aller Hinweise, rechtliche Symbole, Markennummern usw. umfassen. Diese Zeichenfolge ist optional.                                                                                                                        |
| **OriginalFilename** | Ursprünglicher Name der Datei ohne Pfad. Mithilfe dieser Informationen kann eine Anwendung ermitteln, ob eine Datei von einem Benutzer umbenannt wurde. Das Format des Namens hängt vom Dateisystem ab, für das die Datei erstellt wurde. Diese Zeichenfolge ist erforderlich.                                                 |
| **PrivateBuild**     | Informationen über eine private Version der Datei – z. b. "von TESTER1 auf \\ Testbett erstellt". Diese Zeichenfolge sollte nur vorhanden sein, wenn **vs \_ FF \_ PrivateBuild** im *FILEFLAGS* -Parameter des root-Blocks angegeben wird.                                                                                   |
| **ProductName**      | Der Name des Produkts, mit dem die Datei verteilt wird. Diese Zeichenfolge ist erforderlich.                                                                                                                                                                                                                            |
| **ProductVersion**   | Die Version des Produkts, mit dem die Datei verteilt wird – z. b. "3,10" oder "5.00. RC2". Diese Zeichenfolge ist erforderlich.                                                                                                                                                                                       |
| **SpecialBuild**     | Text, der angibt, wie sich diese Version der Datei von der Standardversion unterscheidet – beispielsweise "privater Build für TESTER1 lösen von Maus Problemen auf M250-und M250E-Computern". Diese Zeichenfolge sollte nur vorhanden sein, wenn **vs \_ FF \_ SpecialBuild** im *FILEFLAGS* -Parameter des root-Blocks angegeben wird. |



 

 

 




