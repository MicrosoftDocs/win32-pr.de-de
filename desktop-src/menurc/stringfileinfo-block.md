---
title: StringFileInfo BLOCK-Anweisung
description: Beschreibt die Form des Zeichenfolgeninformationsblocks.
ms.assetid: d5edf638-b70a-44d0-a43a-89d4d21e679f
keywords:
- StringFileInfo BLOCK-Anweisungsmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- StringFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468257d0b8b8b53f3168e8e11e2f649b8354d50a76d3c2a010b98d245472aad0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886765"
---
# <a name="stringfileinfo-block-statement"></a>StringFileInfo BLOCK-Anweisung

Definiert einen Zeichenfolgeninformationsblock.

``` syntax
BLOCK "StringFileInfo" { BLOCK "lang-charset" {VALUE "string-name", "value" . . . }}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lang-charset"></span><span id="LANG-CHARSET"></span>*lang-charset*
</dt> <dd>

Sprachen- und Zeichensatz-Bezeichnerpaar. Es handelt sich um eine hexadezimale Zeichenfolge, die aus der Verkettung der Sprache und zeichensatzbezeichnern besteht, die im Abschnitt "Hinweise" angegeben sind.

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*string-name*
</dt> <dd>

Der Name eines Werts im -Block und kann einer der vordefinierten Namen sein, die im Abschnitt "Hinweise" angegeben sind.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Wert*
</dt> <dd>

Zeichenfolge, die den Wert des entsprechenden Zeichenfolgennamens angibt. Es können mehrere **VALUE-Anweisungen** angegeben werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der *parameter lang-charset* gibt einen der folgenden Sprachcodes an.



| Code   | Sprache            | Code   | Sprache                  |
|--------|---------------------|--------|---------------------------|
| 0x0401 | Arabisch              | 0x0415 | Polnisch                    |
| 0x0402 | Bulgarisch           | 0x0416 | Portugiesisch (Brasilien)       |
| 0x0403 | Katalanisch             | 0x0417 | Rhaeto-Romanic            |
| 0x0404 | Chinesisch (traditionell) | 0x0418 | Rumänisch                  |
| 0x0405 | Tschechisch               | 0x0419 | Russisch                   |
| 0x0406 | Dänisch              | 0x041A | Croato-Serbian (Lateinisch)    |
| 0x0407 | Deutsch              | 0x041B | Slowakisch                    |
| 0x0408 | Griechisch               | 0x041C | Albanisch                  |
| 0x0409 | Englisch (USA)        | 0x041D | Schwedisch                   |
| 0x040A | Caststilnisch (Spanisch)   | 0x041E | Thailändisch                      |
| 0x040B | Finnisch             | 0x041F | Türkisch                   |
| 0x040C | Französisch              | 0x0420 | Urdu                      |
| 0x040D | Hebräisch              | 0x0421 | Bahasa                    |
| 0x040E | Ungarisch           | 0x0804 | Chinesisch (vereinfacht)        |
| 0x040F | Isländisch           | 0x0807 | Deutsch (Deutsch)              |
| 0x0410 | Italienisch             | 0x0809 | Vereinigtes Königreich: Englisch              |
| 0x0411 | Japanisch            | 0x080A | Spanisch (Mexiko)          |
| 0x0412 | Koreanisch              | 0x080C | Französisch (Französisch)            |
| 0x0413 | Niederländisch               | 0x0C0C | Französisch (Kanada)           |
| 0x0414 | Norwegisch – Bokmal  | 0x100C | Französisch (Französisch)              |
| 0x0810 | Italienisch       | 0x0816 | Portugiesisch (Portugal)     |
| 0x0813 | Niederländisch (Niederländisch)       | 0x081A | Serbo-Croatian (Kyrillisch) |
| 0x0814 | Norwegisch – Nynorsk | ?      | ?                         |



 

Der *lang-charset-Parameter* gibt auch einen der folgenden Zeichensatzbezeichner an.



| Bezeichner | Zeichensatz              |
|------------|----------------------------|
| 0          | 7-Bit-ASCII                |
| 932        | Japan (Shift – JIS X-0208) |
| 949        | Korea (Umschalten – KSC 5601)   |
| 950        | Taiwan (Big5)              |
| 1200       | Unicode                    |
| 1250       | Latin-2 (Osteerisch) |
| 1251       | Kyrillisch                   |
| 1252       | Mehrsprachige               |
| 1253       | Griechisch                      |
| 1254       | Türkisch                    |
| 1255       | Hebräisch                     |
| 1256       | Arabisch                     |



 

Der *string-name-Parameter* gibt einen der folgenden vordefinierten Namen an.



| Name                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kommentare**         | Zusätzliche Informationen, die zu Diagnosezwecken angezeigt werden sollen.                                                                                                                                                                                                                                    |
| **CompanyName**      | Unternehmen, das die Datei erstellt hat, z. B. "Microsoft Corporation" oder "Standard Microsystems Corporation, Inc." Diese Zeichenfolge ist erforderlich.                                                                                                                                                                   |
| **FileDescription**  | Dateibeschreibung, die Benutzern angezeigt werden soll. Diese Zeichenfolge wird möglicherweise in einem Listenfeld angezeigt, wenn der Benutzer zu installierende Dateien auswählt, z. B. "Tastaturtreiber für AT-Style Tastaturen". Diese Zeichenfolge ist erforderlich.                                                                                            |
| **FileVersion**      | Versionsnummer der Datei, z.B. "3.10" oder "5.00.RC2". Diese Zeichenfolge ist erforderlich.                                                                                                                                                                                                                      |
| **InternalName**     | Interner Name der Datei, sofern vorhanden, z. B. ein Modulname, wenn es sich bei der Datei um eine Dynamic Link Library handelt. Wenn die Datei keinen internen Namen hat, sollte diese Zeichenfolge der ursprüngliche Dateiname ohne Erweiterung sein. Diese Zeichenfolge ist erforderlich.                                                                       |
| **LegalCopyright**   | Copyrighthinweise, die für die Datei gelten. Dies sollte den vollständigen Text aller Hinweise, rechtlichen Symbole, Copyrightdaten und so weiter enthalten. Diese Zeichenfolge ist optional.                                                                                                                                             |
| **LegalTrademarks**  | Marken und registrierte Marken, die für die Datei gelten. Dies sollte den vollständigen Text aller Hinweise, rechtliche Symbole, Markennummern usw. umfassen. Diese Zeichenfolge ist optional.                                                                                                                        |
| **OriginalFilename** | Ursprünglicher Name der Datei ohne Pfad. Mit diesen Informationen kann eine Anwendung bestimmen, ob eine Datei von einem Benutzer umbenannt wurde. Das Format des Namens hängt vom Dateisystem ab, für das die Datei erstellt wurde. Diese Zeichenfolge ist erforderlich.                                                 |
| **PrivateBuild**     | Informationen zu einer privaten Version der Datei, z.B. "Built by TESTER1 on \\ TESTBED". Diese Zeichenfolge sollte nur vorhanden sein, **wenn VS \_ FF \_ PRIVATEBUILD** im *fileflags-Parameter* des Stammblocks angegeben ist.                                                                                   |
| **ProductName**      | Name des Produkts, mit dem die Datei verteilt wird. Diese Zeichenfolge ist erforderlich.                                                                                                                                                                                                                            |
| **ProductVersion**   | Version des Produkts, mit dem die Datei verteilt wird, z.B. "3.10" oder "5.00.RC2". Diese Zeichenfolge ist erforderlich.                                                                                                                                                                                       |
| **SpecialBuild**     | Text, der angibt, wie sich diese Version der Datei von der Standardversion unterscheidet, z.B. "Privater Build für TESTER1 zum Lösen von Mausproblemen auf M250- und M250E-Computern". Diese Zeichenfolge sollte nur vorhanden sein, **wenn VS \_ FF \_ SPECIALBUILD** im *fileflags-Parameter* des Stammblocks angegeben ist. |



 

 

 




