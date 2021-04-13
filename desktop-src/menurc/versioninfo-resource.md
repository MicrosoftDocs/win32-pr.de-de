---
title: VERSIONINFO-Ressource
description: Definiert eine Versions Informations Ressource. Die Ressource enthält Informationen über die Datei als Versionsnummer, das beabsichtigte Betriebssystem und den ursprünglichen Dateinamen. Die Ressource ist für die Verwendung mit den Versions Informationsfunktionen vorgesehen.
ms.assetid: be4fbf3d-ca30-4de1-b17a-691a316edfad
keywords:
- VERSIONINFO-Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9248abe18d07820ebefaa6d939f36f617f6cd07f
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/16/2020
ms.locfileid: "104316718"
---
# <a name="versioninfo-resource"></a>VERSIONINFO-Ressource

Definiert eine Versions Informations Ressource. Die Ressource enthält Informationen über die Datei als Versionsnummer, das beabsichtigte Betriebssystem und den ursprünglichen Dateinamen. Die Ressource ist für die Verwendung mit den [Versions Informations](./version-information.md) Funktionen vorgesehen.

Es gibt zwei Möglichkeiten, eine **VERSIONINFO** -Anweisung zu formatieren:

``` syntax
versionID VERSIONINFO fixed-info  { block-statement . . . }
```

\- oder -

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

Der Versions Informationsressourcen Bezeichner. Dieser Wert muss 1 sein.

</dd> <dt>

<span id="fixed-info"></span><span id="FIXED-INFO"></span>*Fixed-Info*
</dt> <dd>

Versionsinformationen, wie z. b. die Dateiversion und das beabsichtigte Betriebssystem. Dieser Parameter besteht aus den folgenden Anweisungen.



| -Anweisung.                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **File Version** - *Version*         | Binäre Versionsnummer für die Datei. Die *Version* besteht aus 2 32-Bit-Ganzzahlen, die durch ganze Zahlen mit 4 16 Bit definiert werden. Beispielsweise wird "fileversion 3, 10, 0, 61" in zwei Double Words übersetzt: 0x0003000a und 0x0000003d in dieser Reihenfolge. Wenn die *Version* durch die **DWORD** -Werte *DW1* und *DW2* definiert ist, müssen Sie daher wie folgt in der **fileversion** -Anweisung angezeigt werden: `HIWORD(dw1)` , `LOWORD(dw1)` , `HIWORD(dw2)` , `LOWORD(dw2)` . |
| **ProductVersion** - *Version*      | Binäre Versionsnummer für das Produkt, mit dem die Datei verteilt wird. Der *Versions* Parameter ist 2 32-Bit-Ganzzahlen, die durch ganze Zahlen mit 4 16 Bit definiert werden. Weitere Informationen zur- *Version* finden Sie in der Beschreibung der **Dateiversion** .                                                                                                                                                                                                           |
| **Fileflagsmask** *fileflagsmask* | Gibt an, welche Bits in der **FILEFLAGS** -Anweisung gültig sind. Bei 16-Bit-Fenstern ist dieser Wert 0x3F.                                                                                                                                                                                                                                                                                                                                          |
| **FILEFLAGS** - *FILEFLAGS*         | Attribute der Datei.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **FILEOS** - *Datei* Betriebssysteme               | Das Betriebssystem, für das diese Datei entworfen wurde. Der *FILEOS* -Parameter kann einer der Betriebssystem Werte sein, die im Abschnitt "Hinweise" angegeben sind.                                                                                                                                                                                                                                                                                               |
| **FILETYPE** - *Dateityp*           | Allgemeiner Dateityp. Der *filetype* -Parameter kann einer der Dateityp Werte sein, die im Abschnitt "Hinweise" aufgeführt sind.                                                                                                                                                                                                                                                                                                                                |
| **Filesubtype** - *Untertyp*         | Funktion der Datei. Der *Untertyp* -Parameter ist 0 (null), es sei denn, der *filetype* -Parameter in der **filetype** -Anweisung ist VFT \_ drv, VFT- \_ Schriftart oder VFT \_ . Eine Liste der Werte für den Datei Untertyp finden Sie im Abschnitt "Hinweise".                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*Block-Anweisung*
</dt> <dd>

Gibt mindestens einen Versions Informationsblock an. Ein-Block kann Zeichen folgen Informationen oder Variablen Informationen enthalten. Weitere Informationen finden Sie unter [**stringfileinfo-Block**](stringfileinfo-block.md) oder [**varfileinfo-Block**](varfileinfo-block.md).

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie die mit der **VERSIONINFO** -Anweisung angegebenen Konstanten verwenden möchten, müssen Sie die Header Datei "winver. h" oder "Windows. h" in die Ressourcen Definitionsdatei einschließen.

In der folgenden Liste werden die Parameter beschrieben, die in der **VERSIONINFO** -Anweisung verwendet werden:

<dl> <dt>

<span id="fileflags"></span><span id="FILEFLAGS"></span>*FILEFLAGS*
</dt> <dd>

Eine Kombination der folgenden Werte.



| Wert                      | BESCHREIBUNG                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VS \_ FF- \_ Debug**          | Die Datei enthält Debuginformationen oder wird mit aktivierten Debuggingfunktionen kompiliert.                                                                                                                                                                                         |
| **VS \_ FF \_ gepatcht**        | Die Datei wurde geändert und ist nicht identisch mit der ursprünglichen Versand Datei derselben Versionsnummer.                                                                                                                                                                       |
| **VS \_ FF- \_ Vorabversion**     | Die Datei ist eine Entwicklungsversion und kein kommerziell veröffentlichtes Produkt.                                                                                                                                                                                                         |
| **VS \_ FF \_ PrivateBuild**   | Die Datei wurde nicht mit standardmäßigen releaseprozeduren erstellt. Wenn dieser Wert angegeben wird, muss der [**stringfilinput FO-Block**](stringfileinfo-block.md) eine **PrivateBuild** -Zeichenfolge enthalten.                                                                                              |
| **VS \_ FF \_ SpecialBuild**   | Die Datei wurde vom ursprünglichen Unternehmen mithilfe von standardmäßigen releaseprozeduren erstellt, ist jedoch eine Variation der Standarddatei derselben Versionsnummer. Wenn dieser Wert angegeben wird, muss der [ **stringfilinput FO** -Block](stringfileinfo-block.md) Block eine **SpecialBuild** -Zeichenfolge enthalten. |
| **VS \_ FFI \_ fileflagsmask** | Eine Kombination aus allen vorangehenden Werten.                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="fileos"></span><span id="FILEOS"></span>*FILEOS*
</dt> <dd>

Einer der folgenden Werte.



| Wert                   | BESCHREIBUNG                                                      |
|-------------------------|------------------------------------------------------------------|
| **Vos \_ Unknown**        | Das Betriebssystem, für das die Datei entworfen wurde, ist unbekannt. |
| **Vos \_ DOS**            | Die Datei wurde für MS-DOS konzipiert.                                    |
| **Vos \_ NT**             | Die Datei wurde für 32-Bit-Windows entwickelt.                            |
| **Vos \_ \_ WINDOWS16**    | Die Datei wurde für 16-Bit-Windows entwickelt.                            |
| **Vos \_ \_ WINDOWS32**    | Die Datei wurde für 32-Bit-Windows entwickelt.                            |
| **Vos \_ DOS \_ WINDOWS16** | Die Datei wurde für 16-Bit-Windows entwickelt, die mit MS-DOS ausgeführt werden.        |
| **Vos \_ DOS \_ WINDOWS32** | Die Datei wurde für 32-Bit-Windows entwickelt, die mit MS-DOS ausgeführt werden.        |
| **Vos \_ NT \_ WINDOWS32**  | Die Datei wurde für 32-Bit-Windows entwickelt.                            |



 

Die Werte 0x00002l, 0x00003l, 0x20000l und 0x30000l sind reserviert.

</dd> <dt>

<span id="filetype"></span><span id="FILETYPE"></span>*filetype*
</dt> <dd>

Einer der folgenden Werte.



| Wert                | BESCHREIBUNG                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **VFT \_ unbekannt**     | Der Dateityp ist unbekannt.                                                                                                       |
| **VFT- \_ App**         | Die Datei enthält eine Anwendung.                                                                                               |
| **VFT- \_ dll**         | Die Datei enthält eine Dynamic Link Library (dll).                                                                                 |
| **VFT \_ drv**         | Die Datei enthält einen Gerätetreiber. Wenn *filetype* der **VFT \_ drv** ist, enthält der *Untertyp* eine spezifischere Beschreibung des Treibers. |
| **VFT- \_ Schriftart**        | Die Datei enthält eine Schriftart. Wenn *filetype* die VFT- \_ Schriftart ist, enthält der *Untertyp* eine spezifischere Beschreibung der Schriftart.               |
| **VFT \_ VxD**         | Die Datei enthält ein virtuelles Gerät.                                                                                             |
| **statische VFT- \_ \_ lib** | Die Datei enthält eine Bibliothek mit statischem Link.                                                                                        |



 

Alle anderen Werte sind für die Verwendung durch Microsoft reserviert.

</dd> <dt>

<span id="subtype"></span><span id="SUBTYPE"></span>*Untertyp*
</dt> <dd>

Weitere Informationen zum Dateityp.

Wenn *filetype* den **VFT- \_ drv** angibt, kann dieser Parameter einen der folgenden Werte aufweisen.



| Wert                             | BESCHREIBUNG                               |
|-----------------------------------|-------------------------------------------|
| **VFT2 \_ unbekannt**                 | Der Treibertyp ist unbekannt.                   |
| **VFT2 \_ drv- \_ comm**               | Die Datei enthält einen Kommunikationstreiber.    |
| **VFT2 \_ drv- \_ Drucker**            | Die Datei enthält einen Druckertreiber.           |
| **VFT2 \_ drv- \_ Tastatur**           | Die Datei enthält einen Tastaturtreiber.          |
| **VFT2 \_ drv- \_ Sprache**           | Die Datei enthält einen Sprachtreiber.          |
| **VFT2 \_ drv \_ anzeigen**            | Die Datei enthält einen Anzeigetreiber.           |
| **VFT2 \_ drv- \_ Maus**              | Die Datei enthält einen Maustreiber.             |
| **VFT2 \_ drv- \_ Netzwerk**            | Die Datei enthält einen Netzwerktreiber.           |
| **VFT2 \_ drv- \_ System**             | Die Datei enthält einen System Treiber.            |
| **VFT2 \_ drv \_ installier Bar**        | Die Datei enthält einen installierbaren Treiber.      |
| **VFT2 \_ drv- \_ Sound**              | Die Datei enthält einen Soundtreiber.             |
| **VFT2 mit \_ drv \_ versionierter \_ Drucker** | Die Datei enthält einen Druckertreiber mit Versions Angabe. |



 

Wenn *filetype* die **VFT- \_ Schriftart** angibt, kann dieser Parameter einen der folgenden Werte aufweisen.



| Wert                    | BESCHREIBUNG                    |
|--------------------------|--------------------------------|
| **VFT2 \_ unbekannt**        | Der Schriftart ist unbekannt.          |
| **VFT2 \_ Schriftart \_ Raster**   | Die Datei enthält eine Raster Schriftart.   |
| **VFT2- \_ Schriftart \_ Vektor**   | Die Datei enthält eine Vektor Schriftart.   |
| **VFT2 \_ Schriftart \_ TrueType** | Die Datei enthält eine TrueType-Schriftart. |



 

Wenn *filetype* VFT \_ VxD angibt, muss dieser Parameter der im Virtual Device-Kontroll Block enthaltene Bezeichner für virtuelle Geräte sein.

Alle *unter Typwerte* , die hier nicht aufgelistet sind, sind für die Verwendung durch Microsoft reserviert.

</dd> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

Einer der folgenden Sprachcodes.



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
| 0x0414 | Norwegisch? Bokmal  | 0x100c | Schweiz Französisch              |
| 0x0810 | Schweizer Italienisch       | 0x0816 | Portugiesisch (Portugal)     |
| 0x0813 | Belgisch Niederländisch       | 0x081a | Serbo-Croatian (Kyrillisch) |
| 0x0814 | Norwegisch? Nynorsk |        |                           |



 

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charder TID*
</dt> <dd>

Einer der folgenden Zeichensatz Bezeichner.



| Decimal | Hexadezimal | Zeichensatz              |
|---------|-------------|----------------------------|
| 0       | 0000        | 7-Bit-ASCII                |
| 932     | 03a4        | Japan (Schicht? JIS X-0208) |
| 949     | 03b5        | Korea (Schicht? KSC 5601)   |
| 950     | 03b6        | Taiwan (Big5)              |
| 1200    | 04b0        | Unicode                    |
| 1250    | 04e2        | Lateinisch-2 (Osteuropäisch) |
| 1251    | 04e3        | Kyrillisch                   |
| 1252    | 04e4        | Mehrsprachige               |
| 1253    | 04e5        | Griechisch                      |
| 1254    | 04e6        | Türkisch                    |
| 1255    | 04e7        | Hebräisch                     |
| 1256    | 04e8        | Arabisch                     |



 

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*Zeichen folgen Name*
</dt> <dd>

Einer der folgenden vordefinierten Namen.



| Name                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kommentare**         | Zusätzliche Informationen, die zu Diagnose Zwecken angezeigt werden sollten.                                                                                                                                                                                                                                    |
| **CompanyName**      | Das Unternehmen, das die Datei erstellt hat, z. b. "Microsoft Corporation" oder "Standard Microsystems Corporation, Inc." Diese Zeichenfolge ist erforderlich.                                                                                                                                                                   |
| **FileDescription**  | Die Dateibeschreibung, die Benutzern angezeigt werden soll. Diese Zeichenfolge wird möglicherweise in einem Listenfeld angezeigt, wenn der Benutzer die zu installierenden Dateien auswählt, z. b. "Tastaturtreiber für AT-Style-Tastaturen". Diese Zeichenfolge ist erforderlich.                                                                                            |
| **FileVersion**      | Versionsnummer der Datei, z. b. "3,10" oder "5.00. RC2". Diese Zeichenfolge ist erforderlich.                                                                                                                                                                                                                      |
| **InternalName**     | Interner Name der Datei (sofern vorhanden), z. b. ein Modulname, wenn es sich bei der Datei um eine Dynamic Link Library handelt. Wenn die Datei keinen internen Namen hat, sollte diese Zeichenfolge der ursprüngliche Dateiname ohne Erweiterung sein. Diese Zeichenfolge ist erforderlich.                                                                       |
| **LegalCopyright**   | Copyright Hinweise, die für die Datei gelten. Dies sollte den vollständigen Text aller Hinweise, rechtliche Symbole, Copyright Daten usw. enthalten. Diese Zeichenfolge ist optional.                                                                                                                                             |
| **LegalTrademarks**  | Marken und eingetragene Marken, die auf die Datei angewendet werden. Dies sollte den vollständigen Text aller Hinweise, rechtliche Symbole, Markennummern usw. umfassen. Diese Zeichenfolge ist optional.                                                                                                                        |
| **OriginalFilename** | Ursprünglicher Name der Datei ohne Pfad. Mithilfe dieser Informationen kann eine Anwendung ermitteln, ob eine Datei von einem Benutzer umbenannt wurde. Das Format des Namens hängt vom Dateisystem ab, für das die Datei erstellt wurde. Diese Zeichenfolge ist erforderlich.                                                 |
| **PrivateBuild**     | Informationen über eine private Version der Datei, z. b. "erstellt von TESTER1 auf \\ Testbed". Diese Zeichenfolge sollte nur vorhanden sein, wenn **vs \_ FF \_ PrivateBuild** im *FILEFLAGS* -Parameter des root-Blocks angegeben wird.                                                                                   |
| **ProductName**      | Der Name des Produkts, mit dem die Datei verteilt wird. Diese Zeichenfolge ist erforderlich.                                                                                                                                                                                                                            |
| **ProductVersion**   | Version des Produkts, mit dem die Datei verteilt wird, z. b. "3,10" oder "5.00. RC2". Diese Zeichenfolge ist erforderlich.                                                                                                                                                                                       |
| **SpecialBuild**     | Text, der angibt, wie diese Version der Datei von der Standardversion abweicht, z. b. "privater Build für TESTER1 lösen von Maus Problemen auf M250-und M250E-Computern". Diese Zeichenfolge sollte nur vorhanden sein, wenn **vs \_ FF \_ SpecialBuild** im *FILEFLAGS* -Parameter des root-Blocks angegeben wird. |



 

</dd> </dl>

Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt. Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird eine **VERSIONINFO** -Ressource definiert:

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

 

 