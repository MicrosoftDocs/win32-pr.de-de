---
title: VERSIONINFO-Ressource
description: Definiert eine Versionsinformationsressource. Die Ressource enthält solche Informationen über die Datei wie die Versionsnummer, das beabsichtigte Betriebssystem und den ursprünglichen Dateinamen. Die Ressource ist für die Verwendung mit den Versionsinformationsfunktionen vorgesehen.
ms.assetid: be4fbf3d-ca30-4de1-b17a-691a316edfad
keywords:
- VERSIONSINFO-Ressourcenmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6708b4fefc564685a9989140e5f07dd20714e8bbcb60c53710f43cbfee4aa7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971869"
---
# <a name="versioninfo-resource"></a>VERSIONINFO-Ressource

Definiert eine Versionsinformationsressource. Die Ressource enthält solche Informationen über die Datei wie die Versionsnummer, das beabsichtigte Betriebssystem und den ursprünglichen Dateinamen. Die Ressource ist für die Verwendung mit den [Versionsinformationsfunktionen](./version-information.md) vorgesehen.

Es gibt zwei Möglichkeiten, eine **VERSIONINFO-Anweisung** zu formatieren:

``` syntax
versionID VERSIONINFO fixed-info  { block-statement . . . }
```

\- oder –

``` syntax
versionID VERSIONINFO 
fixed-info
BEGIN
block-statement
. . .
END
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*
</dt> <dd>

Ressourcenbezeichner für Versionsinformationen. Dieser Wert muss 1 sein.

</dd> <dt>

<span id="fixed-info"></span><span id="FIXED-INFO"></span>*Fixed-Info*
</dt> <dd>

Versionsinformationen, z. B. die Dateiversion und das gewünschte Betriebssystem. Dieser Parameter besteht aus den folgenden Anweisungen.



| -Anweisung.                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FILEVERSION-Version**          | Binäre Versionsnummer für die Datei. Die *Version* besteht aus zwei 32-Bit-Ganzzahlen, die durch vier 16-Bit-Ganzzahlen definiert werden. Beispielsweise wird "FILEVERSION 3,10,0,61" in zwei Doppelwörter übersetzt: 0x0003000a und 0x0000003d in dieser Reihenfolge. Wenn daher *version* durch die **DWORD-Werte** *dw1* und *dw2* definiert wird, müssen sie in der **FILEVERSION-Anweisung** wie folgt angezeigt werden: `HIWORD(dw1)` , , , `LOWORD(dw1)` `HIWORD(dw2)` `LOWORD(dw2)` . |
| **PRODUCTVERSION-Version**       | Binäre Versionsnummer für das Produkt, mit dem die Datei verteilt wird. Der *Versionsparameter* ist zwei 32-Bit-Ganzzahlen, die durch vier 16-Bit-Ganzzahlen definiert werden. Weitere Informationen zur *Version* finden Sie in der **Beschreibung von FILEVERSION.**                                                                                                                                                                                                           |
| **FILEFLAGSMASK** *fileflagsmask* | Gibt an, welche Bits in der **FILEFLAGS-Anweisung** gültig sind. Bei 16-Bit-Windows ist dieser Wert 0x3f.                                                                                                                                                                                                                                                                                                                                          |
|  *FILEFLAGS-Dateiflags*         | Attribute der Datei.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **FILEOS fileos**                | Betriebssystem, für das diese Datei entworfen wurde. Der *fileos-Parameter* kann einer der Im Abschnitt Hinweise angegebenen Betriebssystemwerte sein.                                                                                                                                                                                                                                                                                               |
| **FILETYPE filetype**            | Allgemeiner Dateityp. Der *filetype-Parameter* kann einer der Dateitypwerte sein, die im Abschnitt Hinweise aufgeführt sind.                                                                                                                                                                                                                                                                                                                                |
| **FILESUBTYPE-Untertyp**          | Funktion der Datei. Der *Untertypparameter* ist 0 (null), es sei denn, der *Filetype-Parameter* in der **FILETYPE-Anweisung** ist VFT \_ DRV, VFT \_ FONT oder VFT \_ VXD. Eine Liste der Dateiuntertypwerte finden Sie im Abschnitt Hinweise.                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*block-statement*
</dt> <dd>

Gibt mindestens einen Versionsinformationsblock an. Ein -Block kann Zeichenfolgeninformationen oder Variableninformationen enthalten. Weitere Informationen finden Sie unter [**StringFileInfo-Block**](stringfileinfo-block.md) oder [**VarFileInfo-Block.**](varfileinfo-block.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um die mit der **VERSIONINFO-Anweisung** angegebenen Konstanten zu verwenden, müssen Sie die Headerdatei Winver.h oder Windows.h in die Ressourcendefinitionsdatei einschließen.

In der folgenden Liste werden die parameter beschrieben, die in der **VERSIONINFO-Anweisung** verwendet werden:

<dl> <dt>

<span id="fileflags"></span><span id="FILEFLAGS"></span>*fileflags*
</dt> <dd>

Eine Kombination der folgenden Werte.



| Wert                      | BESCHREIBUNG                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VS \_ FF \_ DEBUG**          | Die Datei enthält Debuginformationen oder wird mit aktivierten Debugfunktionen kompiliert.                                                                                                                                                                                         |
| **VS \_ FF \_ PATCHED**        | Die Datei wurde geändert und ist nicht identisch mit der ursprünglichen Versanddatei mit derselben Versionsnummer.                                                                                                                                                                       |
| **VS \_ FF \_ PRERELEASE**     | Bei der Datei handelt es sich um eine Entwicklungsversion, nicht um ein kommerziell veröffentlichtes Produkt.                                                                                                                                                                                                         |
| **VS \_ FF \_ PRIVATEBUILD**   | Die Datei wurde nicht mithilfe von Standardversionsverfahren erstellt. Wenn dieser Wert angegeben wird, muss der [**StringFileInfo-Block**](stringfileinfo-block.md) eine **PrivateBuild-Zeichenfolge** enthalten.                                                                                              |
| **VS \_ FF \_ SPECIALBUILD**   | Die Datei wurde vom ursprünglichen Unternehmen mithilfe von Standardversionsverfahren erstellt, ist jedoch eine Variante der Standarddatei mit derselben Versionsnummer. Wenn dieser Wert angegeben wird, muss der [ **StringFileInfo-Block**](stringfileinfo-block.md) eine **SpecialBuild-Zeichenfolge** enthalten. |
| **VS \_ FFI \_ FILEFLAGSMASK** | Eine Kombination aller vorangehenden Werte.                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="fileos"></span><span id="FILEOS"></span>*fileos*
</dt> <dd>

Einer der folgenden Werte.



| Wert                   | BESCHREIBUNG                                                      |
|-------------------------|------------------------------------------------------------------|
| **VOS \_ UNKNOWN**        | Das Betriebssystem, für das die Datei entworfen wurde, ist unbekannt. |
| **VOS \_ DOS**            | Die Datei wurde für MS-DOS entwickelt.                                    |
| **VOS \_ NT**             | Die Datei wurde für 32-Bit-Windows entwickelt.                            |
| **VOS \_ \_ WINDOWS16**    | Die Datei wurde für 16-Bit-Windows entwickelt.                            |
| **VOS \_ \_ WINDOWS32**    | Die Datei wurde für 32-Bit-Windows entwickelt.                            |
| **VOS \_ DOS \_ WINDOWS16** | Die Datei wurde für 16-Bit-Windows entwickelt, die mit MS-DOS ausgeführt werden.        |
| **VOS \_ DOS \_ WINDOWS32** | Die Datei wurde für 32-Bit-Windows entwickelt, die mit MS-DOS ausgeführt werden.        |
| **VOS \_ NT \_ WINDOWS32**  | Die Datei wurde für 32-Bit-Windows entwickelt.                            |



 

Die Werte 0x00002L, 0x00003L, 0x20000L und 0x30000L sind reserviert.

</dd> <dt>

<span id="filetype"></span><span id="FILETYPE"></span>*Filetype*
</dt> <dd>

Einer der folgenden Werte.



| Wert                | BESCHREIBUNG                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **VFT \_ UNKNOWN**     | Der Dateityp ist unbekannt.                                                                                                       |
| **\_VFT-APP**         | Die Datei enthält eine Anwendung.                                                                                               |
| **\_VFT-DLL**         | Die Datei enthält eine Dynamic Link Library (DLL).                                                                                 |
| **VFT \_ DRV**         | Die Datei enthält einen Gerätetreiber. Wenn *filetype* **VFT \_ DRV** ist, enthält *der Untertyp* eine spezifischere Beschreibung des Treibers. |
| **\_VFT-SCHRIFTART**        | Die Datei enthält eine Schriftart. Wenn *filetype* VFT \_ FONT ist, enthält der *Untertyp* eine spezifischere Beschreibung der Schriftart.               |
| **\_VFT-VXD**         | Die Datei enthält ein virtuelles Gerät.                                                                                             |
| **VFT \_ STATIC \_ LIB** | Die Datei enthält eine statische Linkbibliothek.                                                                                        |



 

Alle anderen Werte sind für die Verwendung durch Microsoft reserviert.

</dd> <dt>

<span id="subtype"></span><span id="SUBTYPE"></span>*Untertyp*
</dt> <dd>

Zusätzliche Informationen zum Dateityp.

Wenn *filetype* **VFT \_ DRV** angibt, kann dieser Parameter einer der folgenden Werte sein.



| Wert                             | BESCHREIBUNG                               |
|-----------------------------------|-------------------------------------------|
| **VFT2 \_ UNKNOWN**                 | Der Treibertyp ist unbekannt.                   |
| **VFT2 \_ DRV \_ COMM**               | Die Datei enthält einen Kommunikationstreiber.    |
| **VFT2 \_ DRV \_ PRINTER**            | Die Datei enthält einen Druckertreiber.           |
| **\_VFT2-DRV-TASTATUR \_**           | Die Datei enthält einen Tastaturtreiber.          |
| **\_VFT2-DRV-SPRACHE \_**           | Die Datei enthält einen Sprachtreiber.          |
| **\_VFT2-DRV-ANZEIGE \_**            | Die Datei enthält einen Anzeigetreiber.           |
| **VFT2 \_ DRV \_ MOUSE**              | Die Datei enthält einen Maustreiber.             |
| **VFT2 \_ DRV \_ NETWORK**            | Die Datei enthält einen Netzwerktreiber.           |
| **VFT2 \_ DRV \_ SYSTEM**             | Die Datei enthält einen Systemtreiber.            |
| **VFT2 \_ DRV \_ INSTALLABLE**        | Die Datei enthält einen installierbaren Treiber.      |
| **VFT2 \_ DRV \_ SOUND**              | Die Datei enthält einen Soundtreiber.             |
| **\_ \_ VFT2 DRV-DRUCKER MIT VERSIONSBEZEICHNER \_** | Die Datei enthält einen Druckertreiber mit Versionsfreigabe. |



 

Wenn *filetype* **VFT \_ FONT** angibt, kann dieser Parameter einer der folgenden Werte sein.



| Wert                    | BESCHREIBUNG                    |
|--------------------------|--------------------------------|
| **VFT2 \_ UNKNOWN**        | Der Schriftarttyp ist unbekannt.          |
| **VFT2 \_ FONT \_ RASTER**   | Die Datei enthält eine Rasterschriftart.   |
| **\_VFT2-SCHRIFTARTVEKTOR \_**   | Die Datei enthält eine Vektorschriftart.   |
| **VFT2 \_ FONT \_ TRUETYPE** | Die Datei enthält eine TrueType-Schriftart. |



 

Wenn *filetype* VFT \_ VXD angibt, muss dieser Parameter der bezeichner des virtuellen Geräts sein, der im Steuerungsblock für virtuelle Geräte enthalten ist.

Alle hier nicht aufgeführten *Untertypwerte* sind für die Verwendung durch Microsoft reserviert.

</dd> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*Langid*
</dt> <dd>

Einer der folgenden Sprachcodes.



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
| 0x040A | Spanisch (Castilienisch)   | 0x041E | Thailändisch                      |
| 0x040B | Finnisch             | 0x041F | Türkisch                   |
| 0x040C | Französisch              | 0x0420 | Urdu                      |
| 0x040D | Hebräisch              | 0x0421 | Bahasa                    |
| 0x040E | Ungarisch           | 0x0804 | Chinesisch (vereinfacht)        |
| 0x040F | Isländisch           | 0x0807 | Deutsch (Deutsch)              |
| 0x0410 | Italienisch             | 0x0809 | Vereinigtes Königreich: Englisch              |
| 0x0411 | Japanisch            | 0x080A | Spanisch (Mexiko)          |
| 0x0412 | Koreanisch              | 0x080C | Französisch (Französisch)            |
| 0x0413 | Niederländisch               | 0x0C0C | Französisch (Kanada)           |
| 0x0414 | Norwegisch? Bokmal  | 0x100C | Französisch (Französisch)              |
| 0x0810 | Italienisch       | 0x0816 | Portugiesisch (Portugal)     |
| 0x0813 | Niederländisch (Niederländisch)       | 0x081A | Serbo-Croatian (Kyrillisch) |
| 0x0814 | Norwegisch? Nynorsk |        |                           |



 

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*
</dt> <dd>

Einer der folgenden Zeichensatzbezeichner.



| Decimal | Hexadezimal | Zeichensatz              |
|---------|-------------|----------------------------|
| 0       | 0000        | 7-Bit-ASCII                |
| 932     | 03A4        | Japan (Umschalten? JIS X-0208) |
| 949     | 03B5        | Korea (Umschalten? KSC 5601)   |
| 950     | 03B6        | Taiwan (Big5)              |
| 1200    | 04B0        | Unicode                    |
| 1250    | 04E2        | Latin-2 (Osteerisch) |
| 1251    | 04E3        | Kyrillisch                   |
| 1252    | 04E4        | Mehrsprachige               |
| 1253    | 04E5        | Griechisch                      |
| 1254    | 04E6        | Türkisch                    |
| 1255    | 04E7        | Hebräisch                     |
| 1256    | 04E8        | Arabisch                     |



 

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*string-name*
</dt> <dd>

Einer der folgenden vordefinierten Namen.



| Name                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kommentare**         | Zusätzliche Informationen, die zu Diagnosezwecken angezeigt werden sollen.                                                                                                                                                                                                                                    |
| **CompanyName**      | Unternehmen, das die Datei erstellt hat, z.B. "Microsoft Corporation" oder "Standard Microsystems Corporation, Inc." Diese Zeichenfolge ist erforderlich.                                                                                                                                                                   |
| **FileDescription**  | Dateibeschreibung, die Benutzern angezeigt werden soll. Diese Zeichenfolge kann in einem Listenfeld angezeigt werden, wenn der Benutzer Zu installierende Dateien auswählt, z.B. "Tastaturtreiber für AT-Style Tastaturen". Diese Zeichenfolge ist erforderlich.                                                                                            |
| **FileVersion**      | Versionsnummer der Datei?, z.B. "3.10" oder "5.00.RC2". Diese Zeichenfolge ist erforderlich.                                                                                                                                                                                                                      |
| **InternalName**     | Interner Name der Datei, falls vorhanden? z. B. ein Modulname, wenn es sich bei der Datei um eine Dynamic Link Library handelt. Wenn die Datei keinen internen Namen hat, sollte diese Zeichenfolge der ursprüngliche Dateiname ohne Erweiterung sein. Diese Zeichenfolge ist erforderlich.                                                                       |
| **LegalCopyright**   | Urheberrechtshinweise, die für die Datei gelten. Dies sollte den vollständigen Text aller Hinweise, rechtlichen Symbole, Copyrightdaten usw. enthalten. Diese Zeichenfolge ist optional.                                                                                                                                             |
| **LegalTrademarks**  | Marken und registrierte Marken, die für die Datei gelten. Dies sollte den vollständigen Text aller Hinweise, rechtliche Symbole, Markennummern usw. umfassen. Diese Zeichenfolge ist optional.                                                                                                                        |
| **OriginalFilename** | Ursprünglicher Name der Datei ohne Pfad. Anhand dieser Informationen kann eine Anwendung bestimmen, ob eine Datei von einem Benutzer umbenannt wurde. Das Format des Namens hängt vom Dateisystem ab, für das die Datei erstellt wurde. Diese Zeichenfolge ist erforderlich.                                                 |
| **PrivateBuild**     | Informationen zu einer privaten Version der Datei, z.B. "Built by TESTER1 on \\ TESTBED". Diese Zeichenfolge sollte nur vorhanden sein, wenn **VS \_ FF \_ PRIVATEBUILD** im *fileflags-Parameter* des Stammblocks angegeben ist.                                                                                   |
| **ProductName**      | Name des Produkts, mit dem die Datei verteilt wird. Diese Zeichenfolge ist erforderlich.                                                                                                                                                                                                                            |
| **ProductVersion**   | Version des Produkts, mit dem die Datei verteilt wird, z.B. "3.10" oder "5.00.RC2". Diese Zeichenfolge ist erforderlich.                                                                                                                                                                                       |
| **SpecialBuild**     | Text, der angibt, wie sich diese Version der Datei von der Standardversion unterscheidet, z.B. "Privater Build für TESTER1 zum Lösen von Mausproblemen auf M250- und M250E-Computern". Diese Zeichenfolge sollte nur vorhanden sein, wenn **VS \_ FF \_ SPECIALBUILD** im *fileflags-Parameter* des Stammblocks angegeben ist. |



 

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [Allgemeine Ressourcenattribute.](common-resource-attributes.md)

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine **VERSIONINFO-Ressource** definiert:

``` syntax
#define VER_FILEVERSION             3,10,349,0
#define VER_FILEVERSION_STR         "3.10.349.0\0"

#define VER_PRODUCTVERSION          3,10,0,0
#define VER_PRODUCTVERSION_STR      "3.10\0"

#ifndef DEBUG
#define VER_DEBUG                   0
#else
#define VER_DEBUG                   VS_FF_DEBUG
#endif

VS_VERSION_INFO VERSIONINFO
FILEVERSION     VER_FILEVERSION
PRODUCTVERSION  VER_PRODUCTVERSION
FILEFLAGSMASK   VS_FFI_FILEFLAGSMASK
FILEFLAGS       (VER_PRIVATEBUILD|VER_PRERELEASE|VER_DEBUG)
FILEOS          VOS__WINDOWS32
FILETYPE        VFT_DLL
FILESUBTYPE     VFT2_UNKNOWN
BEGIN
    BLOCK "StringFileInfo"
    BEGIN
        BLOCK "040904E4"
        BEGIN
            VALUE "CompanyName",      VER_COMPANYNAME_STR
            VALUE "FileDescription",  VER_FILEDESCRIPTION_STR
            VALUE "FileVersion",      VER_FILEVERSION_STR
            VALUE "InternalName",     VER_INTERNALNAME_STR
            VALUE "LegalCopyright",   VER_LEGALCOPYRIGHT_STR
            VALUE "LegalTrademarks1", VER_LEGALTRADEMARKS1_STR
            VALUE "LegalTrademarks2", VER_LEGALTRADEMARKS2_STR
            VALUE "OriginalFilename", VER_ORIGINALFILENAME_STR
            VALUE "ProductName",      VER_PRODUCTNAME_STR
            VALUE "ProductVersion",   VER_PRODUCTVERSION_STR
        END
    END

    BLOCK "VarFileInfo"
    BEGIN
        /* The following line should only be modified for localized versions.     */
        /* It consists of any number of WORD,WORD pairs, with each pair           */
        /* describing a language,codepage combination supported by the file.      */
        /*                                                                        */
        /* For example, a file might have values "0x409,1252" indicating that it  */
        /* supports English language (0x409) in the Windows ANSI codepage (1252). */

        VALUE "Translation", 0x409, 1252

    END
END
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Verwenden von Versionsinformationen](./using-version-information.md)
</dt> <dt>

[Versionsinformationen](./version-information.md)
</dt> </dl>

 

 