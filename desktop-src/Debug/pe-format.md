---
description: Diese Spezifikation beschreibt die Struktur von ausführbaren Dateien (Imagedateien) und Objektdateien unter der Windows Betriebssystemfamilie. Diese Dateien werden als portable ausführbare Dateien (Portable Executable, PE) bzw. COFF-Dateien (Common Object File Format) bezeichnet.
ms.assetid: 3dbfbf7f-6662-45a4-99f1-e0e24c370dee
title: PE-Format
ms.topic: article
ms.date: 03/31/2021
ms.custom: contperf-fy21q1
ms.openlocfilehash: f20431f7f56c64d5d430c9992da72ea4331cbf21
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812196"
---
# <a name="pe-format"></a>PE-Format

Diese Spezifikation beschreibt die Struktur von ausführbaren Dateien (Imagedateien) und Objektdateien unter der Windows Betriebssystemfamilie. Diese Dateien werden als portable ausführbare Dateien (Portable Executable, PE) bzw. COFF-Dateien (Common Object File Format) bezeichnet.

> [!Note]  
> Dieses Dokument wird bereitgestellt, um die Entwicklung von Tools und Anwendungen für Windows zu unterstützen, es ist jedoch nicht garantiert, dass es sich in jeder Hinsicht um eine vollständige Spezifikation handelt. Microsoft behält sich das Recht vor, dieses Dokument ohne vorherige Ankündigung zu ändern.

Diese Revision der Microsoft Portable Executable- und Common Object File Format Specification ersetzt alle vorherigen Revisionen dieser Spezifikation.

## <a name="general-concepts"></a>Allgemeine Konzepte

Dieses Dokument gibt die Struktur von ausführbaren Dateien (Imagedateien) und Objektdateien unter der Microsoft Windows-Betriebssystemfamilie an. Diese Dateien werden als portable ausführbare Dateien (Portable Executable, PE) bzw. COFF-Dateien (Common Object File Format) bezeichnet. Der Name "Portable Executable" bezieht sich auf die Tatsache, dass das Format nicht architekturspezifisch ist.

Bestimmte Konzepte, die in dieser Spezifikation angezeigt werden, werden in der folgenden Tabelle beschrieben:

| Name                              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Attributzertifikat <br/> | Ein Zertifikat, das zum Zuordnen überprüfbarer Anweisungen zu einem Image verwendet wird. Einer Datei können verschiedene überprüfbare Anweisungen zugeordnet werden. Einer der nützlichsten ist eine Anweisung eines Softwareherstellers, die angibt, welcher Nachrichtenhest des Images erwartet wird. Ein Nachrichtenhest ähnelt einer Prüfsumme, mit der Ausnahme, dass es äußerst schwierig ist, ihn zu forten. Daher ist es sehr schwierig, eine Datei so zu ändern, dass sie den gleichen Nachrichtenhest wie die ursprüngliche Datei hat. Die Anweisung kann mithilfe von Kryptografieschemas mit öffentlichem oder privatem Schlüssel als vom Hersteller vorgenommen überprüft werden. In diesem Dokument werden Details zu Attributzertifikaten beschrieben, die nicht das Einfügen in Bilddateien ermöglichen. <br/> |
| Datums-/Zeitstempel <br/>       | Ein Stempel, der für verschiedene Zwecke an mehreren Stellen in einer PE- oder COFF-Datei verwendet wird. In den meisten Fällen ist das Format jedes Stempels mit dem Format identisch, das von den Zeitfunktionen in der C-Laufzeitbibliothek verwendet wird. Ausnahmen finden Sie im Deskript für IMAGE \_ DEBUG \_ TYPE \_ REPRO im [Debugtyp](#debug-type). Wenn der Stempelwert 0 oder 0xFFFFFFFF ist, stellt er keinen echten oder aussagekräftigen Datums-/Uhrzeitstempel dar. <br/>                                                                                                                                                                                                                                                                                                                                            |
| Dateizeiger <br/>          | Der Speicherort eines Elements innerhalb der Datei selbst, bevor er vom Linker (bei Objektdateien) oder vom Ladeprogramm (bei Bilddateien) verarbeitet wird. Anders ausgedrückt: Dies ist eine Position innerhalb der Datei, die auf dem Datenträger gespeichert ist. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Linker <br/>                | Ein Verweis auf den Linker, der mit Microsoft Visual Studio bereitgestellt wird. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Objektdatei <br/>           | Eine Datei, die als Eingabe für den Linker angegeben wird. Der Linker erzeugt eine Bilddatei, die wiederum vom Ladeprogramm als Eingabe verwendet wird. Der Begriff "Objektdatei" impliziert nicht notwendigerweise eine Verbindung mit der objektorientierten Programmierung. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| reserviert, muss 0 sein. <br/>   | Eine Beschreibung eines Felds, das angibt, dass der Wert des Felds für Generatoren 0 (null) sein muss und Consumer das Feld ignorieren müssen. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Relative virtuelle Adresse (RVA) <br/>                   | In einer Bilddatei ist dies die Adresse eines Elements, nachdem es in den Arbeitsspeicher geladen wurde, wobei die Basisadresse der Bilddatei davon subtrahiert wird. Das RVA eines Elements unterscheidet sich fast immer von seiner Position innerhalb der Datei auf dem Datenträger (Dateizeiger). <br/> In einer Objektdatei ist ein RVA weniger aussagekräftig, da keine Speicherorte zugewiesen sind. In diesem Fall wäre ein RVA eine Adresse innerhalb eines Abschnitts (weiter unten in dieser Tabelle beschrieben), auf den später während der Verknüpfung eine Verschiebung angewendet wird. Der Einfachheit halber sollte ein Compiler einfach das erste RVA in jedem Abschnitt auf 0 (null) festlegen. <br/>                                                                                                                                         |
| section <br/>               | Die grundlegende Einheit von Code oder Daten in einer PE- oder COFF-Datei. Beispielsweise kann der gesamte Code in einer Objektdatei innerhalb eines einzelnen Abschnitts kombiniert werden, oder (je nach Compilerverhalten) kann jede Funktion einen eigenen Abschnitt belegen. Mit mehr Abschnitten ist der Dateimoverhead größer, aber der Linker kann im Code selektiver verknüpfen. Ein Abschnitt ähnelt einem Segment in der Intel 8086-Architektur. Alle Rohdaten in einem Abschnitt müssen zusammenhängend geladen werden. Darüber hinaus kann eine Bilddatei eine Reihe von Abschnitten enthalten, z. B. TLS oder .reloc, die besondere Zwecke haben. <br/>                                                                                                                                                                      |
| Virtuelle Adresse (VA) <br/>                    | Identisch mit RVA, außer dass die Basisadresse der Imagedatei nicht subtrahiert wird. Die Adresse wird als VA bezeichnet, da Windows einen eindeutigen VA-Bereich für jeden Prozess erstellt, unabhängig vom physischen Speicher. Für fast alle Zwecke sollte eine Va nur als Adresse betrachtet werden. Eine Va ist nicht so vorhersagbar wie ein RVA, da das Ladeprogramm das Image möglicherweise nicht an seinem bevorzugten Speicherort lädt. <br/>                                                                                                                                                                                                                                                                                                                                        |

## <a name="overview"></a>Übersicht

In der folgenden Liste wird das ausführbare Format von Microsoft PE mit der Basis des Imageheaders oben beschrieben. Der Abschnitt vom MS-DOS 2.0 Compatible EXE Header bis zum nicht verwendeten Abschnitt direkt vor dem PE-Header ist der MS-DOS 2.0-Abschnitt und wird nur für die MS-DOS-Kompatibilität verwendet.

-   MS-DOS 2.0-kompatibler EXE-Header
-   unused
-   OEM-Bezeichner

    Informationen zum Gerätehersteller

    Offset zu PE-Header

-   MS-DOS 2.0-Stubprogramm und -Verschiebungstabelle

-   unused

-   PE-Header (an 8-Byte-Grenze ausgerichtet)

-   Abschnittsheader
-   Bildseiten:

    Importinformationen

    Exportieren von Informationen

    Basisverlagerungen

    Ressourceninfo

In der folgenden Liste wird das Microsoft COFF-Objektmodulformat beschrieben:

-   Microsoft COFF-Header
-   Abschnittsheader
-   Rohdaten:

    code

    data

    Debuginformationen

    Standortverlagerungen

## <a name="file-headers"></a>Dateiheader

- [MS-DOS-Stub (nur Bild)](#ms-dos-stub-image-only)
- [Signatur (nur Bild)](#signature-image-only)
- [COFF-Dateiheader (Objekt und Bild)](#coff-file-header-object-and-image)
  - [Computertypen](#machine-types)
  - [Characteristics](#characteristics)
- [Optionaler Header (nur Bild)](#optional-header-image-only)
  - [Optionale Standardfelder für Header (nur Bild)](#optional-header-standard-fields-image-only)
  - [Optionale Header-Windows-Specific-Felder (nur Bild)](#optional-header-windows-specific-fields-image-only)
  - [Optionale Headerdatenverzeichnisse (nur Bild)](#optional-header-data-directories-image-only)

Der PE-Dateiheader besteht aus einem Microsoft MS-DOS-Stub, der PE-Signatur, dem COFF-Dateiheader und einem optionalen Header. Ein COFF-Objektdateiheader besteht aus einem COFF-Dateiheader und einem optionalen Header. In beiden Fällen folgen auf die Dateiheader unmittelbar Abschnittsheader.

### <a name="ms-dos-stub-image-only"></a>MS-DOS-Stub (nur Bild)

Der MS-DOS-Stub ist eine gültige Anwendung, die unter MS-DOS ausgeführt wird. Sie wird am Anfang des EXE-Images platziert. Der Linker platziert hier einen Standardstub, der die Meldung "Dieses Programm kann nicht im DOS-Modus ausgeführt werden" ausgibt, wenn das Image in MS-DOS ausgeführt wird. Der Benutzer kann mithilfe der /STUB-Linkeroption einen anderen Stub angeben.

An der 0x3c hat der Stub den Dateioffset zur PE-Signatur. Diese Informationen ermöglichen es Windows, die Imagedatei ordnungsgemäß auszuführen, obwohl sie über einen MS-DOS-Stub verfügt. Dieser Dateioffset wird während der Verknüpfung 0x3c Speicherort platziert.

### <a name="signature-image-only"></a>Signatur (nur Image)

Nach dem MS-DOS-Stub ist am Dateioffset, der bei offset 0x3c angegeben ist, eine 4-Byte-Signatur, die die Datei als Bilddatei im PE-Format identifiziert. Diese Signatur ist "PE \\ 0 \\ 0" (die Buchstaben "P" und "E" gefolgt von zwei NULL-Bytes).

### <a name="coff-file-header-object-and-image"></a>COFF-Dateiheader (Objekt und Bild)

Am Anfang einer Objektdatei oder unmittelbar nach der Signatur einer Bilddatei ist ein COFF-Standarddateiheader im folgenden Format. Beachten Sie, dass Windows-Lader die Anzahl der Abschnitte auf 96 beschränkt.

| Offset         | Size          | Feld                            | Beschreibung                                                                                                                                                                                                                                                          |
|----------------|---------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/> | Machine <br/>              | Die Zahl, die den Typ des Zielcomputers identifiziert. Weitere Informationen finden Sie unter [Computertypen](#machine-types). <br/>                                                                                                                                        |
| 2 <br/>  | 2 <br/> | NumberOfSections <br/>     | Die Anzahl der Abschnitte. Dies gibt die Größe der Abschnittstabelle an, die unmittelbar auf die Header folgt. <br/>                                                                                                                                             |
| 4 <br/>  | 4 <br/> | TimeDateStamp <br/>        | Die niedrigen 32 Bits der Anzahl von Sekunden seit dem 1. Januar 1970 00:00 (ein C-Laufzeitwert t), der angibt, wann die Datei erstellt \_ wurde. <br/>                                                                                                             |
| 8 <br/>  | 4 <br/> | PointerToSymbolTable <br/> | Der Dateioffset der COFF-Symboltabelle oder 0 (null), wenn keine COFF-Symboltabelle vorhanden ist. Dieser Wert sollte für ein Image 0 (null) sein, da COFF-Debuginformationen veraltet sind. <br/>                                                                           |
| 12 <br/> | 4 <br/> | NumberOfSymbols <br/>      | Die Anzahl der Einträge in der Symboltabelle. Diese Daten können verwendet werden, um die Zeichenfolgentabelle zu suchen, die unmittelbar auf die Symboltabelle folgt. Dieser Wert sollte für ein Image 0 (null) sein, da COFF-Debuginformationen veraltet sind. <br/>                        |
| 16 <br/> | 2 <br/> | SizeOfOptionalHeader <br/> | Die Größe des optionalen Headers, der für ausführbare Dateien, aber nicht für Objektdateien erforderlich ist. Dieser Wert sollte für eine Objektdatei NULL sein. Eine Beschreibung des Headerformats finden Sie unter [Optionaler Header (nur Bild).](#optional-header-image-only) <br/> |
| 18 <br/> | 2 <br/> | Merkmale <br/>      | Die Flags, die die Attribute der Datei angeben. Informationen zu bestimmten Flagwerten finden Sie unter [Merkmale.](#characteristics) <br/>                                                                                                                               |

#### <a name="machine-types"></a>Computertypen

Das Feld Computer verfügt über einen der folgenden Werte, die den CPU-Typ angeben. Eine Imagedatei kann nur auf dem angegebenen Computer oder auf einem System ausgeführt werden, das den angegebenen Computer emuliert.

| Konstante                                    | Wert              | Beschreibung                                                                             |
|---------------------------------------------|--------------------|-----------------------------------------------------------------------------------------|
| \_ \_ IMAGEDATEICOMPUTER \_ UNBEKANNT <br/>   | 0x0 <br/>    | Es wird davon ausgegangen, dass der Inhalt dieses Felds auf jeden Computertyp anwendbar ist. <br/> |
| \_ \_ IMAGEDATEICOMPUTER \_ AM33 <br/>      | 0x1d3 <br/>  | Matsushita AM33 <br/>                                                             |
| \_ \_ IMAGEDATEICOMPUTER \_ AMD64 <br/>     | 0x8664 <br/> | x64 <br/>                                                                         |
| IMAGE \_ FILE \_ MACHINE \_ ARM <br/>       | 0x1c0 <br/>  | ARM Little Endian <br/>                                                           |
| \_ \_ IMAGEDATEICOMPUTER \_ ARM64 <br/>     | 0xaa64 <br/> | ARM64 Little-Endian <br/>                                                         |
| \_ \_ IMAGEDATEICOMPUTER \_ ARMNT <br/>     | 0x1c4 <br/>  | ARM Thumb-2 Little Endian <br/>                                                   |
| \_ \_ BILDDATEICOMPUTER \_ EBC <br/>       | 0xebc <br/>  | EFI-Bytecode <br/>                                                               |
| \_ \_ IMAGEDATEICOMPUTER \_ I386 <br/>      | 0x14c <br/>  | Intel 386- oder höher-Prozessoren und kompatible Prozessoren <br/>                     |
| \_ \_ IMAGEDATEICOMPUTER \_ IA64 <br/>      | 0x200 <br/>  | Intel Itanium-Prozessorfamilie <br/>                                              |
| \_ \_ IMAGEDATEICOMPUTER \_ M32R <br/>      | 0x9041 <br/> | Little-Endian M32R <br/>                                               |
| \_ \_ IMAGEDATEICOMPUTER \_ MIPS16 <br/>    | 0x266 <br/>  | MIPS16 <br/>                                                                      |
| \_ \_ IMAGEDATEICOMPUTER \_ MIPSFPU <br/>   | 0x366 <br/>  | MIPS mit FPU <br/>                                                               |
| \_ \_ IMAGEDATEICOMPUTER \_ MIPSFPU16 <br/> | 0x466 <br/>  | MIPS16 mit FPU <br/>                                                             |
| \_ \_ IMAGEDATEICOMPUTER \_ POWERPC <br/>   | 0x1f0 <br/>  | Power PC Little-Endian <br/>                                                      |
| \_ \_ IMAGEDATEICOMPUTER \_ POWERPCFP <br/> | 0x1f1 <br/>  | Power PC mit Gleitkommaunterstützung <br/>                                        |
| \_ \_ IMAGEDATEICOMPUTER \_ R4000 <br/>     | 0x166 <br/>  | MIPS little endian <br/>                                                          |
| \_ \_ IMAGEDATEICOMPUTER \_ RISCV32 <br/>   | 0x5032 <br/> | RISC-V 32-Bit-Adressraum <br/>                                                 |
| \_ \_ IMAGEDATEICOMPUTER \_ RISCV64 <br/>   | 0x5064 <br/> | RISC-V 64-Bit-Adressraum <br/>                                                 |
| \_ \_ IMAGEDATEICOMPUTER \_ RISCV128 <br/>  | 0x5128 <br/> | RISC-V 128-Bit-Adressraum <br/>                                                |
| IMAGE \_ FILE \_ MACHINE \_ SH3 <br/>       | 0x1a2 <br/>  | Hitachi SH3 <br/>                                                                 |
| IMAGE \_ FILE \_ MACHINE \_ SH3DSP <br/>    | 0x1a3 <br/>  | Sh3-DSP <br/>                                                             |
| IMAGE \_ FILE \_ MACHINE \_ SH4 <br/>       | 0x1a6 <br/>  | Hitachi SH4 <br/>                                                                 |
| \_ \_ IMAGEDATEICOMPUTER \_ SH5 <br/>       | 0x1a8 <br/>  | Hitachi SH5 <br/>                                                                 |
| \_ \_ \_ BILDDATEICOMPUTERFINGER <br/>     | 0x1c2 <br/>  | Ziehpunkt <br/>                                                                       |
| \_ \_ IMAGEDATEICOMPUTER \_ WCEMIPSV2 <br/> | 0x169 <br/>  | MIPS Little-Endian WCE v2 <br/>                                                   |

#### <a name="characteristics"></a>Merkmale

Das Feld Merkmale enthält Flags, die Attribute des Objekts oder der Bilddatei angeben. Die folgenden Flags sind derzeit definiert:

| Flag                                                 | Wert              | Beschreibung                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ FILE \_ RELOCS \_ STRIPPED <br/>            | 0x0001 <br/> | Nur Image, Windows CE und Microsoft Windows NT und höher. Dies gibt an, dass die Datei keine Basisverlagerungen enthält und daher an der bevorzugten Basisadresse geladen werden muss. Wenn die Basisadresse nicht verfügbar ist, meldet das Ladeprogramm einen Fehler. Das Standardverhalten des Linkers besteht darin, Basisverlagerungen aus ausführbaren Dateien (EXE) zu löschen. <br/> |
| AUSFÜHRBARES IMAGE DER \_ BILDDATEI \_ \_ <br/>           | 0x0002 <br/> | Nur Bild. Dies gibt an, dass die Imagedatei gültig ist und ausgeführt werden kann. Wenn dieses Flag nicht festgelegt ist, wird ein Linkerfehler angezeigt. <br/>                                                                                                                                                                                                                          |
| \_ \_ \_ BILDDATEIZEILEN-NUMS \_ ENTFERNT <br/>        | 0x0004 <br/> | COFF-Zeilennummern wurden entfernt. Dieses Flag ist veraltet und sollte 0 (null) sein. <br/>                                                                                                                                                                                                                                                                       |
| LOKALE SYMS DER \_ BILDDATEI \_ \_ \_ ENTFERNT <br/>       | 0x0008 <br/> | Coff-Symboltabelleneinträge für lokale Symbole wurden entfernt. Dieses Flag ist veraltet und sollte 0 (null) sein. <br/>                                                                                                                                                                                                                                             |
| BILDDATEI \_ \_ AGGRESSIVE \_ WS \_ TRIM <br/>        | 0x0010 <br/> | Veraltet. Arbeitssatz aggressiv kürzen. Dieses Flag ist für Windows 2000 und höher veraltet und muss 0 (null) sein. <br/>                                                                                                                                                                                                                                          |
| BILDDATEI \_ \_ MIT GROßER \_ ADRESSE \_ <br/>      | 0x0020 <br/> | Die Anwendung kann > 2-GB-Adressen verarbeiten. <br/>                                                                                                                                                                                                                                                                                                            |
|                                                      | 0x0040 <br/> | Dieses Flag ist für die zukünftige Verwendung reserviert. <br/>                                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ FILE \_ BYTES \_ REVERSED \_ LO <br/>         | 0x0080 <br/> | Little-Endian: Das am wenigsten signifikante Bit (LSB) ist dem wichtigsten Bit (MSB) im Arbeitsspeicher voraus. Dieses Flag ist veraltet und sollte 0 (null) sein. <br/>                                                                                                                                                                                                          |
| \_ \_ IMAGEDATEI 32-BIT-COMPUTER \_ <br/>              | 0x0100 <br/> | Der Computer basiert auf einer 32-Bit-Wortarchitektur. <br/>                                                                                                                                                                                                                                                                                                        |
| DEBUGGEN \_ DER BILDDATEI \_ \_ ENTFERNT <br/>             | 0x0200 <br/> | Debuginformationen werden aus der Imagedatei entfernt. <br/>                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ FILE \_ REMOVABLE \_ RUN \_ FROM \_ SWAP <br/> | 0x0400 <br/> | Wenn sich das Image auf Wechselmedien befindet, laden Sie es vollständig, und kopieren Sie es in die Auslagerungsdatei. <br/>                                                                                                                                                                                                                                                                        |
| IMAGE \_ FILE \_ NET \_ RUN \_ FROM \_ SWAP <br/>        | 0x0800 <br/> | Wenn sich das Image auf Netzwerkmedien befindet, laden Sie es vollständig, und kopieren Sie es in die Auslagerungsdatei. <br/>                                                                                                                                                                                                                                                                          |
| IMAGE \_ FILE \_ SYSTEM <br/>                      | 0x1000 <br/> | Die Imagedatei ist eine Systemdatei, kein Benutzerprogramm. <br/>                                                                                                                                                                                                                                                                                                   |
| \_ \_ IMAGEDATEI-DLL <br/>                         | 0x2000 <br/> | Die Bilddatei ist eine Dynamic Link Library (DLL). Solche Dateien werden für fast alle Zwecke als ausführbare Dateien betrachtet, obwohl sie nicht direkt ausgeführt werden können. <br/>                                                                                                                                                                                              |
| IMAGE \_ FILE \_ UP \_ SYSTEM \_ ONLY <br/>            | 0x4000 <br/> | Die Datei sollte nur auf einem Uniprozessorcomputer ausgeführt werden. <br/>                                                                                                                                                                                                                                                                                                 |
| BILDDATEI \_ \_ BYTES \_ REVERSED \_ HI <br/>         | 0x8000 <br/> | Big-Endian: Der MSB geht dem LSB im Arbeitsspeicher voraus. Dieses Flag ist veraltet und sollte 0 (null) sein. <br/>                                                                                                                                                                                                                                                            |

### <a name="optional-header-image-only"></a>Optionaler Header (nur Bild)

Jede Imagedatei verfügt über einen optionalen Header, der Dem Ladeprogramm Informationen bereitstellt. Dieser Header ist optional, da einige Dateien (insbesondere Objektdateien) nicht über ihn verfügen. Für Bilddateien ist dieser Header erforderlich. Eine Objektdatei kann einen optionalen Header aufweisen, aber im Allgemeinen hat dieser Header keine Funktion in einer Objektdatei, außer um die Größe zu erhöhen.

Beachten Sie, dass die Größe des optionalen Headers nicht festgelegt ist. Das **Feld SizeOfOptionalHeader** im COFF-Header muss verwendet werden, um zu überprüfen, ob ein Test in der Datei für ein bestimmtes Datenverzeichnis nicht über **SizeOfOptionalHeader hinaus geht.** Weitere Informationen finden Sie unter [COFF-Dateiheader (Objekt und Bild).](#coff-file-header-object-and-image)

Das **NumberOfRvaAndSizes-Feld** des optionalen Headers sollte auch verwendet werden, um sicherzustellen, dass kein Test für einen bestimmten Datenverzeichniseintrag über den optionalen Header hinausgeht. Darüber hinaus ist es wichtig, die optionale Magic-Zahl für Header auf Formatkompatibilität zu überprüfen.

Die optionale Header-Magic-Zahl bestimmt, ob es sich bei einem Image um eine ausführbare PE32- oder PE32+-Datei handelt.

| Magische Zahl      | PE-Format         |
|-------------------|-------------------|
| 0x10b <br/> | PE32 <br/>  |
| 0x20b <br/> | PE32+ <br/> |

PE32+-Images ermöglichen einen 64-Bit-Adressraum und beschränken die Bildgröße auf 2 Gigabyte. Andere PE32+-Änderungen werden in den entsprechenden Abschnitten behandelt.

Der optionale Header selbst besteht aus drei Hauptteilen.

| Offset (PE32/PE32+) | Größe (PE32/PE32+)    | Headerteil                         | Beschreibung                                                                                                                                                                   |
|---------------------|----------------------|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>       | 28/24 <br/>    | Standardfelder <br/>         | Felder, die für alle Implementierungen von COFF definiert sind, einschließlich UNIX. <br/>                                                                                          |
| 28/24 <br/>   | 68/88 <br/>    | Windows-spezifische Felder <br/> | Zusätzliche Felder zur Unterstützung bestimmter Features von Windows (z. B. Subsysteme). <br/>                                                                              |
| 96/112 <br/>  | Variable <br/> | Datenverzeichnisse <br/>        | Adress-/Größenpaare für spezielle Tabellen, die sich in der Imagedatei befinden und vom Betriebssystem verwendet werden (z. B. die Importtabelle und die Exporttabelle). <br/> |

#### <a name="optional-header-standard-fields-image-only"></a>Optionale Standardfelder für Header (nur Bild)

Die ersten acht Felder des optionalen Headers sind Standardfelder, die für jede Implementierung von COFF definiert sind. Diese Felder enthalten allgemeine Informationen, die zum Laden und Ausführen einer ausführbaren Datei nützlich sind. Sie sind für das PE32+-Format unverändert.

| Offset         | Size          | Feld                               | Beschreibung                                                                                                                                                                                                                                                                                                                                   |
|----------------|---------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/> | Magic <br/>                   | Die ganze Zahl ohne Vorzeichen, die den Status der Bilddatei identifiziert. Die häufigste Zahl ist 0x10B, die sie als normale ausführbare Datei identifiziert. 0x107 identifiziert es als ROM-Image und 0x20B als ausführbare PE32+-Datei. <br/>                                                                                            |
| 2 <br/>  | 1 <br/> | MajorLinkerVersion <br/>      | Die Hauptversionsnummer des Linker. <br/>                                                                                                                                                                                                                                                                                                  |
| 3 <br/>  | 1 <br/> | MinorLinkerVersion <br/>      | Die Nebenversionsnummer des Linker. <br/>                                                                                                                                                                                                                                                                                                  |
| 4 <br/>  | 4 <br/> | SizeOfCode <br/>              | Die Größe des Codeabschnitts (Text) oder die Summe aller Codeabschnitte, wenn mehrere Abschnitte enthalten sind. <br/>                                                                                                                                                                                                                              |
| 8 <br/>  | 4 <br/> | SizeOfInitializedData <br/>   | Die Größe des initialisierten Datenabschnitts oder die Summe aller dieser Abschnitte, wenn mehrere Datenabschnitte sind. <br/>                                                                                                                                                                                                                    |
| 12 <br/> | 4 <br/> | SizeOfUninitializedData <br/> | Die Größe des Abschnitts für nicht initialisierte Daten (BSS) oder die Summe aller dieser Abschnitte, wenn mehrere BSS-Abschnitte verfügbar sind. <br/>                                                                                                                                                                                                             |
| 16 <br/> | 4 <br/> | AddressOfEntryPoint <br/>     | Die Adresse des Einstiegspunkts relativ zur Imagebasis, wenn die ausführbare Datei in den Arbeitsspeicher geladen wird. Bei Programmbildern ist dies die Startadresse. Bei Gerätetreibern ist dies die Adresse der Initialisierungsfunktion. Ein Einstiegspunkt ist für DLLs optional. Wenn kein Einstiegspunkt vorhanden ist, muss dieses Feld 0 (null) sein. <br/> |
| 20 <br/> | 4 <br/> | BaseOfCode <br/>              | Die Adresse, die relativ zur Imagebasis des Codeanfangsabschnitts ist, wenn er in den Arbeitsspeicher geladen wird. <br/>                                                                                                                                                                                                                    |

PE32 enthält dieses zusätzliche Feld, das in PE32+ nicht vorhanden ist, und folgt BaseOfCode.

| Offset         | Size          | Feld                  | Beschreibung                                                                                                                |
|----------------|---------------|------------------------|----------------------------------------------------------------------------------------------------------------------------|
| 24 <br/> | 4 <br/> | BaseOfData <br/> | Die Adresse, die relativ zur Imagebasis des Datenanfangsabschnitts ist, wenn er in den Arbeitsspeicher geladen wird. <br/> |

#### <a name="optional-header-windows-specific-fields-image-only"></a>Optionale Header Windows-Specific Felder (nur Bild)

Die nächsten 21 Felder sind eine Erweiterung des optionalen COFF-Headerformats. Sie enthalten zusätzliche Informationen, die vom Linker und Lader in der Windows.

| Offset (PE32/ PE32+) | Größe (PE32/ PE32+) | Feld                                   | Beschreibung                                                                                                                                                                                                                                                                                                            |
|----------------------|--------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 28/24 <br/>    | 4/8 <br/>    | Imagebase <br/>                   | Die bevorzugte Adresse des ersten Byte des Bilds beim Laden in den Arbeitsspeicher; muss ein Vielfaches von 64.000 sein. Der Standardwert für DLLs ist 0x10000000. Der Standardwert für Windows CE-EXEs ist 0x00010000. Der Standardwert für Windows NT, Windows 2000, Windows XP, Windows 95, Windows 98 und Windows Me ist 0x00400000. <br/>       |
| 32/32 <br/>    | 4 <br/>      | SectionAlignment <br/>            | Die Ausrichtung (in Bytes) von Abschnitten beim Laden in den Arbeitsspeicher. Er muss größer oder gleich FileAlignment sein. Der Standard für die Architektur ist die Seitengröße. <br/>                                                                                                                               |
| 36/36 <br/>    | 4 <br/>      | FileAlignment <br/>               | Der Ausrichtungsfaktor (in Byte), der verwendet wird, um die Rohdaten von Abschnitten in der Imagedatei auszurichten. Der Wert sollte eine Leistung von 2 zwischen 512 und 64.000 (einschließlich) haben. Der Standardwert liegt bei 512. Wenn sectionAlignment kleiner als die Seitengröße der Architektur ist, muss FileAlignment mit SectionAlignment übereinstimmen. <br/> |
| 40/40 <br/>    | 2 <br/>      | MajorOperatingSystemVersion <br/> | Die Hauptversionsnummer des erforderlichen Betriebssystems. <br/>                                                                                                                                                                                                                                                 |
| 42/42 <br/>    | 2 <br/>      | MinorOperatingSystemVersion <br/> | Die Nebenversionsnummer des erforderlichen Betriebssystems. <br/>                                                                                                                                                                                                                                                 |
| 44/44 <br/>    | 2 <br/>      | MajorImageVersion <br/>           | Die Hauptversionsnummer des Images. <br/>                                                                                                                                                                                                                                                                     |
| 46/46 <br/>    | 2 <br/>      | MinorImageVersion <br/>           | Die Nebenversionsnummer des Images. <br/>                                                                                                                                                                                                                                                                     |
| 48/48 <br/>    | 2 <br/>      | MajorSubsystemVersion <br/>       | Die Hauptversionsnummer des Subsystems. <br/>                                                                                                                                                                                                                                                                 |
| 50/50 <br/>    | 2 <br/>      | MinorSubsystemVersion <br/>       | Die Nebenversionsnummer des Subsystems. <br/>                                                                                                                                                                                                                                                                 |
| 52/52 <br/>    | 4 <br/>      | Win32VersionValue <br/>           | Reserviert, muss 0 (null) sein. <br/>                                                                                                                                                                                                                                                                                    |
| 56/56 <br/>    | 4 <br/>      | SizeOfImage <br/>                 | Die Größe (in Bytes) des Bilds, einschließlich aller Header, während das Bild in den Arbeitsspeicher geladen wird. Es muss ein Vielfaches von SectionAlignment sein. <br/>                                                                                                                                                                      |
| 60/60 <br/>    | 4 <br/>      | SizeOfHeaders <br/>               | Die kombinierte Größe eines MS-DOS-Stubs, eines PE-Headers und von Abschnittsheadern, die auf ein Vielfaches von FileAlignment aufgerundet sind. <br/>                                                                                                                                                                                             |
| 64/64 <br/>    | 4 <br/>      | Prüfsumme <br/>                    | Die Prüfsumme der Bilddatei. Der Algorithmus zum Berechnen der Prüfsumme wird in die IMAGHELP.DLL. Folgendes wird zur Ladezeit auf Überprüfung überprüft: alle Treiber, alle dll-Dateien, die beim Start geladen werden, und alle DLLs, die in einen kritischen Windows werden. <br/>                                          |
| 68/68 <br/>    | 2 <br/>      | Subsystem <br/>                   | Das Subsystem, das zum Ausführen dieses Images erforderlich ist. Weitere Informationen finden Sie unter [Windows Subsystem](#windows-subsystem). <br/>                                                                                                                                                                                       |
| 70/70 <br/>    | 2 <br/>      | DllCharacteristics <br/>          | Weitere Informationen finden Sie weiter unten in dieser Spezifikation unter [DLL-Merkmale.](#dll-characteristics) <br/>                                                                                                                                                                                                         |
| 72/72 <br/>    | 4/8 <br/>    | SizeOfStackReserve <br/>          | Die Größe des Stapels, der reserviert werden soll. Nur Für SizeOfStackCommit wird ein Committed ausführen. Der Rest wird seite für Seite zur Verfügung gestellt, bis die Reservegröße erreicht ist. <br/>                                                                                                                                                    |
| 76/80 <br/>    | 4/8 <br/>    | SizeOfStackCommit <br/>           | Dier Größe des Stapels, für den ein Commit ausgeführt wird. <br/>                                                                                                                                                                                                                                                                           |
| 80/88 <br/>    | 4/8 <br/>    | SizeOfHeapReserve <br/>           | Die Größe des Speicherplatzes für den lokalen Heap, der reserviert werden soll. Es wird nur ein Committed für SizeOfHeapCommit verwendet. Der Rest wird seite für Seite zur Verfügung gestellt, bis die Reservegröße erreicht ist. <br/>                                                                                                                                          |
| 84/96 <br/>    | 4/8 <br/>    | SizeOfHeapCommit <br/>            | Die Größe des Speicherplatzes für den lokalen Heap, für den ein Commit ausgeführt werden soll. <br/>                                                                                                                                                                                                                                                                |
| 88/104 <br/>   | 4 <br/>      | LoaderFlags <br/>                 | Reserviert, muss 0 (null) sein. <br/>                                                                                                                                                                                                                                                                                    |
| 92/108 <br/>   | 4 <br/>      | NumberOfRvaAndSizes <br/>         | Die Anzahl der Datenverzeichniseinträge im Rest des optionalen Headers. Jeder beschreibt einen Speicherort und eine Größe. <br/>                                                                                                                                                                                          |

##### <a name="windows-subsystem"></a>Windows Subsystem

Die folgenden Werte, die für das Feld Subsystem des optionalen Headers definiert sind, bestimmen, Windows Subsystem (sofern vorhanden) zum Ausführen des Images erforderlich ist.

| Konstante                                                  | Wert          | Beschreibung                                                      |
|-----------------------------------------------------------|----------------|------------------------------------------------------------------|
| \_IMAGESUBSYSTEM \_ UNBEKANNT <br/>                     | 0 <br/>  | Ein unbekanntes Subsystem <br/>                                 |
| \_SYSTEMEIGENES \_ IMAGESUBSYSTEM <br/>                      | 1 <br/>  | Gerätetreiber und native Windows Prozesse <br/>          |
| \_WINDOWS-GUI DES \_ IMAGE-SUBSYSTEMS \_ <br/>                | 2 <br/>  | Das Windows GUI-Subsystem (Grafische Benutzeroberfläche) <br/> |
| IMAGE \_ SUBSYSTEM \_ WINDOWS \_ CUI <br/>                | 3 <br/>  | Das Windows Zeichensubsystem <br/>                      |
| \_IMAGE-SUBSYSTEM \_ OS2 \_ CUI <br/>                    | 5 <br/>  | Das Os/2-Zeichensubsystem <br/>                         |
| IMAGE \_ SUBSYSTEM \_ POSIX \_ CUI <br/>                  | 7 <br/>  | Das Posix-Zeichensubsystem <br/>                        |
| \_SYSTEMEIGENES \_ IMAGESUBSYSTEM \_ UNTER WINDOWS <br/>             | 8 <br/>  | Nativer Win9x-Treiber <br/>                                  |
| IMAGE \_ SUBSYSTEM \_ WINDOWS \_ CE \_ GUI <br/>            | 9 <br/>  | Windows CE <br/>                                           |
| \_ \_ IMAGE-SUBSYSTEM-EFI-ANWENDUNG \_ <br/>            | 10 <br/> | Eine Extensible Firmware Interface -Anwendung (EFI) <br/>   |
| \_ \_ \_ IMAGE-SUBSYSTEM-EFI-STARTDIENSTTREIBER \_ \_ <br/> | 11 <br/> | Ein EFI-Treiber mit Startdiensten <br/>                     |
| IMAGE \_ SUBSYSTEM \_ EFI \_ RUNTIME \_ DRIVER <br/>       | 12 <br/> | Ein EFI-Treiber mit Laufzeitdiensten <br/>                 |
| IMAGE \_ SUBSYSTEM \_ EFI \_ ROM <br/>                    | 13 <br/> | Ein EFI-ROM-Image <br/>                                     |
| \_BILDSUBSYSTEM \_ XBOX <br/>                        | 14 <br/> | XBOX <br/>                                                 |
| \_WINDOWS-STARTANWENDUNG FÜR DAS \_ \_ IMAGESUBSYSTEM \_ <br/>  | 16 <br/> | Windows Startanwendung. <br/>                            |

##### <a name="dll-characteristics"></a>DLL-Merkmale

Die folgenden Werte werden für das DllCharacteristics-Feld des optionalen Headers definiert.

| Konstante                                                             | Wert              | Beschreibung                                                                                             |
|----------------------------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------|
|                                                                      | 0x0001 <br/> | Reserviert, muss 0 (null) sein. <br/>                                                                     |
|                                                                      | 0x0002 <br/> | Reserviert, muss 0 (null) sein. <br/>                                                                     |
|                                                                      | 0x0004 <br/> | Reserviert, muss 0 (null) sein. <br/>                                                                     |
|                                                                      | 0x0008 <br/> | Reserviert, muss 0 (null) sein. <br/>                                                                     |
| IMAGE \_ DLLCHARACTERISTICS \_ HIGH \_ ENTROPY \_ VA <br/>             | 0x0020 <br/> | Das Image kann einen virtuellen 64-Bit-Adressraum mit hoher Entropie verarbeiten. <br/>                               |
| \_IMAGE-DLLCHARACTERISTICS\_ <br/> DYNAMIC \_ BASE <br/>    | 0x0040 <br/> | DIE DLL kann zur Ladezeit verschoben werden. <br/>                                                          |
| \_IMAGE-DLLCHARACTERISTICS\_ <br/> ERZWINGEN \_ DER INTEGRITÄT <br/> | 0x0080 <br/> | Codeintegritätsprüfungen werden erzwungen. <br/>                                                         |
| \_IMAGE-DLLCHARACTERISTICS\_ <br/> \_NX-KOMPATIBILITÄT <br/>       | 0x0100 <br/> | Das Image ist NX-kompatibel. <br/>                                                                     |
| IMAGE \_ DLLCHARACTERISTICS \_ NO \_ ISOLATION <br/>                | 0x0200 <br/> | Isolationsbewusst, aber isolieren Sie das Image nicht. <br/>                                              |
| IMAGE \_ DLLCHARACTERISTICS \_ NO \_ SEH <br/>                      | 0x0400 <br/> | Verwendet keine strukturierte Ausnahmebehandlung (SE Ausnahme). In diesem SE kann kein Handler aufgerufen werden. <br/> |
| IMAGE \_ DLLCHARACTERISTICS \_ NO \_ BIND <br/>                     | 0x0800 <br/> | Binden Sie das Image nicht. <br/>                                                                      |
| IMAGE \_ DLLCHARACTERISTICS \_ APPCONTAINER <br/>                  | 0x1000 <br/> | Das Image muss in einem AppContainer ausgeführt werden. <br/>                                                      |
| \_ \_ IMAGE-DLLCHARACTERISTICS-WDM-TREIBER \_ <br/>                  | 0x2000 <br/> | Ein WDM-Treiber. <br/>                                                                               |
| IMAGE \_ DLLCHARACTERISTICS \_ GUARD \_ CF <br/>                     | 0x4000 <br/> | Image unterstützt Control Flow Guard. <br/>                                                          |
| IMAGE \_ DLLCHARACTERISTICS \_ TERMINAL \_ SERVER \_ AWARE <br/>      | 0x8000 <br/> | Terminalserver-aware. <br/>                                                                      |

#### <a name="optional-header-data-directories-image-only"></a>Optionale Headerdatenverzeichnisse (nur Bild)

Jedes Datenverzeichnis gibt die Adresse und Größe einer Tabelle oder Zeichenfolge an, die Windows verwendet. Diese Datenverzeichniseinträge werden alle in den Arbeitsspeicher geladen, damit sie vom System zur Laufzeit verwendet werden können. Ein Datenverzeichnis ist ein 8-Byte-Feld mit der folgenden Deklaration:

```cpp
typedef struct _IMAGE_DATA_DIRECTORY {
    DWORD   VirtualAddress;
    DWORD   Size;
} IMAGE_DATA_DIRECTORY, *PIMAGE_DATA_DIRECTORY;
```

Das erste Feld, VirtualAddress, ist tatsächlich das RVA der Tabelle. Das RVA ist die Adresse der Tabelle relativ zur Basisadresse des Images, wenn die Tabelle geladen wird. Das zweite Feld gibt die Größe in Bytes an. Die Datenverzeichnisse, die den letzten Teil des optionalen Headers bilden, sind in der folgenden Tabelle aufgeführt.

Beachten Sie, dass die Anzahl der Verzeichnisse nicht festgelegt ist. Bevor Sie nach einem bestimmten Verzeichnis suchen, überprüfen Sie das Feld NumberOfRvaAndSizes im optionalen Header.

Gehen Sie außerdem nicht davon aus, dass die RVAs in dieser Tabelle auf den Anfang eines Abschnitts zeigen oder dass die Abschnitte, die bestimmte Tabellen enthalten, bestimmte Namen haben.

| Offset (PE/PE32+)   | Size          | Feld                               | Beschreibung                                                                                                                                                                          |
|---------------------|---------------|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 96/112 <br/>  | 8 <br/> | Tabelle exportieren <br/>            | Die Adresse und Größe der Exporttabelle. Weitere Informationen finden Sie im [Abschnitt .edata (Nur Bild).](#the-edata-section-image-only) <br/>                                                |
| 104/120 <br/> | 8 <br/> | Tabelle importieren <br/>            | Die Adresse und Größe der Importtabelle. Weitere Informationen finden Sie im [Abschnitt .idata.](#the-idata-section)<br/>                                                                    |
| 112/128 <br/> | 8 <br/> | Ressourcentabelle <br/>          | Die Adresse und Größe der Ressourcentabelle. Weitere Informationen finden Sie im [Rsrc-Abschnitt](#the-rsrc-section).<br/>                                                                    |
| 120/136 <br/> | 8 <br/> | Ausnahmetabelle <br/>         | Adresse und Größe der Ausnahmetabelle. Weitere Informationen finden Sie im [Abschnitt .pdata.](#the-pdata-section) <br/>                                                                |
| 128/144 <br/> | 8 <br/> | Zertifikattabelle <br/>       | Die Adresse und Größe der Attributzertifikattabelle. Weitere Informationen finden Sie unter [Die Attributzertifikattabelle (nur Bild).](#the-attribute-certificate-table-image-only) <br/> |
| 136/152 <br/> | 8 <br/> | Basisverlagerungstabelle <br/>   | Die Adresse und Größe der Basisverlagerungstabelle. Weitere Informationen finden Sie im [Abschnitt .reloc (nur Bild).](#the-reloc-section-image-only)<br/>                                   |
| 144/160 <br/> | 8 <br/> | Debug <br/>                   | Die Startadresse und -größe der Debugdaten. Weitere Informationen finden Sie im [Abschnitt .debug.](#the-debug-section)<br/>                                                             |
| 152/168 <br/> | 8 <br/> | Aufbau <br/>            | Reserviert, muss 0 sein <br/>                                                                                                                                                      |
| 160/176 <br/> | 8 <br/> | Global Ptr <br/>              | Die RVA des Werts, der im globalen Zeigerregister gespeichert werden soll. Der Größenmember dieser Struktur muss auf 0 (null) festgelegt werden. <br/>                                                 |
| 168/184 <br/> | 8 <br/> | TLS-Tabelle <br/>               | Die Adresse und Größe der TLS-Tabelle (Thread Local Storage). Weitere Informationen finden Sie im [Abschnitt .tls.](#the-tls-section)<br/>                                                        |
| 176/192 <br/> | 8 <br/> | Laden der Konfigurationstabelle <br/>       | Adresse und Größe der Ladekonfigurationstabelle. Weitere Informationen finden Sie unter [The Load Configuration Structure (Image Only) (The Load Configuration Structure (Nur Image)).](#the-load-configuration-structure-image-only)<br/>       |
| 184/200 <br/> | 8 <br/> | Gebundener Import <br/>            | Die Adresse und Größe der gebundenen Importtabelle. <br/>                                                                                                                                 |
| 192/208 <br/> | 8 <br/> | Iat <br/>                     | Die Adresse und Größe der Importadresstabelle. Weitere Informationen finden Sie unter [Import Address Table](#import-address-table).<br/>                                                 |
| 200/216 <br/> | 8 <br/> | Verzögerter Importdeskriptor <br/> | Die Adresse und Größe des Verzögertimportdeskriptors. Weitere Informationen finden Sie unter [Verzögertes Laden von Importtabellen (nur Bild).](#delay-load-import-tables-image-only)<br/>                    |
| 208/224 <br/> | 8 <br/> | CLR-Runtimeheader <br/>      | Die Adresse und Größe des CLR-Runtimeheaders. Weitere Informationen finden Sie im [Abschnitt .cormeta (nur Objekt).](#the-cormeta-section-object-only)<br/>                                |
| 216/232 <br/> | 8 <br/> | Reserviert, muss 0 (null) sein <br/>  |                                                                                                                                                                                      |

Der Eintrag Zertifikattabelle verweist auf eine Tabelle mit Attributzertifikaten. Diese Zertifikate werden nicht als Teil des Images in den Arbeitsspeicher geladen. Daher ist das erste Feld dieses Eintrags, das normalerweise ein RVA ist, stattdessen ein Dateizeiger.

## <a name="section-table-section-headers"></a>Abschnittstabelle (Abschnittsheader)

- [Abschnittsflags](#section-flags)
- [Gruppierte Abschnitte (nur Objekt)](#grouped-sections-object-only)

Jede Zeile der Abschnittstabelle ist tatsächlich ein Abschnittsheader. Diese Tabelle folgt, falls vorhanden, unmittelbar auf den optionalen Header. Diese Positionierung ist erforderlich, da der Dateiheader keinen direkten Zeiger auf die Abschnittstabelle enthält. Stattdessen wird die Position der Abschnittstabelle durch Berechnen der Position des ersten Byte nach den Headern bestimmt. Stellen Sie sicher, dass Sie die Größe des optionalen Headers wie im Dateiheader angegeben verwenden.

Die Anzahl der Einträge in der Abschnittstabelle wird durch das Feld NumberOfSections im Dateiheader angegeben. Einträge in der Abschnittstabelle werden beginnend mit 1 nummeriert (1). Die Code- und Datenspeicherabschnittseinträge befinden sich in der vom Linker ausgewählten Reihenfolge.

In einer Bilddatei müssen die VAs für Abschnitte vom Linker zugewiesen werden, damit sie sich in aufsteigender Reihenfolge und nebeneinander befinden, und sie müssen ein Vielfaches des SectionAlignment-Werts im optionalen Header sein.

Jeder Abschnittsheader (Abschnittstabelleneintrag) hat das folgende Format für insgesamt 40 Bytes pro Eintrag.



| Offset         | Size          | Feld                            | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------|---------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 8 <br/> | Name <br/>                 | Eine 8-Byte-UTF-8-codierte Zeichenfolge mit NULL-Padd. Wenn die Zeichenfolge genau 8 Zeichen lang ist, gibt es keinen endenden NULL-Wert. Bei längeren Namen enthält dieses Feld einen Schrägstrich (/), auf den eine ASCII-Darstellung einer Dezimalzahl folgt, die ein Offset in der Zeichenfolgentabelle ist. Ausführbare Images verwenden keine Zeichenfolgentabelle und unterstützen keine Abschnittsnamen, die länger als 8 Zeichen sind. Lange Namen in Objektdateien werden abgeschnitten, wenn sie in eine ausführbare Datei ausgegeben werden. <br/>                                         |
| 8 <br/>  | 4 <br/> | VirtualSize <br/>          | Die Gesamtgröße des Abschnitts beim Laden in den Arbeitsspeicher. Wenn dieser Wert größer als SizeOfRawData ist, wird der Abschnitt mit 0 (null) aufschlossen. Dieses Feld ist nur für ausführbare Bilder gültig und sollte für Objektdateien auf 0 festgelegt werden. <br/>                                                                                                                                                                                                                                                                                           |
| 12 <br/> | 4 <br/> | VirtualAddress <br/>       | Bei ausführbaren Images die Adresse des ersten Byte des Abschnitts relativ zur Imagebasis, wenn der Abschnitt in den Arbeitsspeicher geladen wird. Bei Objektdateien ist dieses Feld die Adresse des ersten Byte, bevor die Verschiebung angewendet wird. Der Einfachheit halber sollten Compiler dies auf 0 (null) festlegen. Andernfalls ist es ein beliebiger Wert, der während der Verschiebung von Offsets subtrahiert wird. <br/>                                                                                                                                         |
| 16 <br/> | 4 <br/> | SizeOfRawData <br/>        | Die Größe des Abschnitts (für Objektdateien) oder die Größe der initialisierten Daten auf dem Datenträger (für Bilddateien). Bei ausführbaren Images muss dies ein Vielfaches von FileAlignment aus dem optionalen Header sein. Wenn dies kleiner als VirtualSize ist, wird der Rest des Abschnitts mit 0 (null) gefüllt. Da das Feld SizeOfRawData gerundet wird, das VirtualSize-Feld jedoch nicht, ist es möglich, dass SizeOfRawData auch größer als VirtualSize ist. Wenn ein Abschnitt nur nicht initialisierte Daten enthält, sollte dieses Feld 0 (null) sein. <br/> |
| 20 <br/> | 4 <br/> | PointerToRawData <br/>     | Der Dateizeiger auf die erste Seite des Abschnitts in der COFF-Datei. Bei ausführbaren Images muss dies ein Vielfaches von FileAlignment aus dem optionalen Header sein. Für Objektdateien sollte der Wert an einer 4-Byte-Grenze ausgerichtet werden, um eine optimale Leistung zu erzielen. Wenn ein Abschnitt nur nicht initialisierte Daten enthält, sollte dieses Feld 0 (null) sein. <br/>                                                                                                                                                                               |
| 24 <br/> | 4 <br/> | PointerToRelocations <br/> | Der Dateizeiger auf den Anfang der Verschiebungseinträge für den Abschnitt. Dies ist für ausführbare Images oder , wenn keine Verschiebungen ausgeführt werden, auf 0 (null) festgelegt. <br/>                                                                                                                                                                                                                                                                                                                                                                   |
| 28 <br/> | 4 <br/> | PointerToLinenumbers <br/> | Der Dateizeiger auf den Anfang der Zeilennummereinträge für den Abschnitt. Dieser Wert wird auf 0 (null) festgelegt, wenn keine COFF-Zeilennummern enthalten sind. Dieser Wert sollte für ein Image 0 (null) sein, da COFF-Debuginformationen veraltet sind. <br/>                                                                                                                                                                                                                                                                                            |
| 32 <br/> | 2 <br/> | NumberOfRelocations <br/>  | Die Anzahl der Verschiebungseinträge für den Abschnitt. Dies ist für ausführbare Images auf 0 (null) festgelegt. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 34 <br/> | 2 <br/> | NumberOfLinenumbers <br/>  | Die Anzahl der Zeilennummereinträge für den Abschnitt. Dieser Wert sollte für ein Image 0 (null) sein, da COFF-Debuginformationen veraltet sind. <br/>                                                                                                                                                                                                                                                                                                                                                                          |
| 36 <br/> | 4 <br/> | Merkmale <br/>      | Die Flags, die die Merkmale des Abschnitts beschreiben. Weitere Informationen finden Sie unter [Abschnittsflags](#section-flags).<br/>                                                                                                                                                                                                                                                                                                                                                                                                |



 

### <a name="section-flags"></a>Abschnittsflags

Die Abschnittsflags im Feld Merkmale des Abschnittsheaders geben Merkmale des Abschnitts an.



| Flag                                              | Wert                  | Beschreibung                                                                                                                                                                 |
|---------------------------------------------------|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                                   | 0x00000000 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
|                                                   | 0x00000001 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
|                                                   | 0x00000002 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
|                                                   | 0x00000004 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ TYPE \_ NO \_ PAD <br/>             | 0x00000008 <br/> | Der Abschnitt sollte nicht bis zur nächsten Grenze aufschlossen werden. Dieses Flag ist veraltet und wird durch IMAGE \_ SCN \_ ALIGN \_ 1BYTES ersetzt. Dies ist nur für Objektdateien gültig. <br/> |
|                                                   | 0x00000010 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
| IMAGE \_ \_ SCN-CNT-CODE \_ <br/>                 | 0x00000020 <br/> | Der Abschnitt enthält ausführbaren Code. <br/>                                                                                                                           |
| IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA <br/>    | 0x00000040 <br/> | Der Abschnitt enthält initialisierte Daten. <br/>                                                                                                                          |
| IMAGE \_ SCN \_ CNT \_ UNINITIALIZED \_ DATA <br/> | 0x00000080 <br/> | Der Abschnitt enthält nicht initialisierte Daten. <br/>                                                                                                                        |
| IMAGE \_ SCN \_ LNK \_ OTHER <br/>                | 0x00000100 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ LNK \_ INFO <br/>                 | 0x00000200 <br/> | Der Abschnitt enthält Kommentare oder andere Informationen. Der Abschnitt .dre wies diesen Typ auf. Dies gilt nur für Objektdateien. <br/>                                    |
|                                                   | 0x00000400 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ LNK \_ REMOVE <br/>               | 0x00000800 <br/> | Der Abschnitt wird nicht Teil des Images. Dies ist nur für Objektdateien gültig. <br/>                                                                             |
| IMAGE \_ SCN \_ LNK \_ COMDAT <br/>               | 0x00001000 <br/> | Der Abschnitt enthält COMDAT-Daten. Weitere Informationen finden Sie unter [COMDAT-Abschnitte (nur Objekt).](#comdat-sections-object-only) Dies ist nur für Objektdateien gültig. <br/> |
| IMAGE \_ SCN \_ GPREL <br/>                     | 0x00008000 <br/> | Der Abschnitt enthält Daten, auf die über den globalen Zeiger (GP) verwiesen wird. <br/>                                                                                           |
| IMAGE \_ SCN \_ MEM \_ PURGEABLE <br/>            | 0x00020000 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ MEM \_ 16BIT <br/>                | 0x00020000 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ MEM \_ LOCKED <br/>               | 0x00040000 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ MEM \_ PRELOAD <br/>              | 0x00080000 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ ALIGN \_ 1BYTES <br/>             | 0x00100000 <br/> | Ausrichten von Daten an einer 1-Byte-Grenze. Nur für Objektdateien gültig. <br/>                                                                                                   |
| IMAGE \_ SCN \_ ALIGN \_ 2BYTES <br/>             | 0x00200000 <br/> | Ausrichten von Daten an einer 2-Byte-Grenze. Nur für Objektdateien gültig. <br/>                                                                                                   |
| IMAGE \_ SCN \_ ALIGN \_ 4BYTES <br/>             | 0x00300000 <br/> | Ausrichten von Daten an einer 4-Byte-Grenze. Nur für Objektdateien gültig. <br/>                                                                                                   |
| IMAGE \_ SCN \_ ALIGN \_ 8BYTES <br/>             | 0x00400000 <br/> | Ausrichten von Daten an einer 8-Byte-Grenze. Nur für Objektdateien gültig. <br/>                                                                                                  |
| IMAGE \_ SCN \_ ALIGN \_ 16BYTES <br/>            | 0x00500000 <br/> | Ausrichten von Daten an einer 16-Byte-Grenze. Nur für Objektdateien gültig. <br/>                                                                                                  |
| IMAGE \_ SCN \_ ALIGN \_ 32BYTES <br/>            | 0x00600000 <br/> | Ausrichten von Daten an einer 32-Byte-Grenze. Nur für Objektdateien gültig. <br/>                                                                                                  |
| IMAGE \_ SCN \_ ALIGN \_ 64BYTES <br/>            | 0x00700000 <br/> | Ausrichten von Daten an einer 64-Byte-Grenze. Nur für Objektdateien gültig. <br/>                                                                                                  |
| IMAGE \_ SCN \_ ALIGN \_ 128BYTES <br/>           | 0x00800000 <br/> | Ausrichten von Daten an einer 128-Byte-Grenze. Nur für Objektdateien gültig. <br/>                                                                                                 |
| IMAGE \_ SCN \_ ALIGN \_ 256BYTES <br/>           | 0x00900000 <br/> | Ausrichten von Daten an einer 256-Byte-Grenze. Nur für Objektdateien gültig. <br/>                                                                                                 |
| IMAGE \_ SCN \_ ALIGN \_ 512BYTES <br/>           | 0x00A00000 <br/> | Ausrichten von Daten an einer 512-Byte-Grenze. Nur für Objektdateien gültig. <br/>                                                                                                 |
| IMAGE \_ SCN \_ ALIGN \_ 1024BYTES <br/>          | 0x00B00000 <br/> | Ausrichten von Daten an einer 1024-Byte-Grenze. Nur für Objektdateien gültig. <br/>                                                                                                |
| IMAGE \_ SCN \_ ALIGN \_ 2048BYTES <br/>          | 0x00C00000 <br/> | Ausrichten von Daten an einer 2048-Byte-Grenze. Nur für Objektdateien gültig. <br/>                                                                                                |
| IMAGE \_ SCN \_ ALIGN \_ 4096BYTES <br/>          | 0x00D00000 <br/> | Ausrichten von Daten an einer 4096-Byte-Grenze. Nur für Objektdateien gültig. <br/>                                                                                                |
| IMAGE \_ SCN \_ ALIGN \_ 8192BYTES <br/>          | 0x00E00000 <br/> | Ausrichten von Daten an einer 8192-Byte-Grenze. Nur für Objektdateien gültig. <br/>                                                                                               |
| IMAGE \_ SCN \_ LNK \_ NRELOC \_ OVFL <br/>         | 0x01000000 <br/> | Der Abschnitt enthält erweiterte Verschiebungen. <br/>                                                                                                                      |
| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>          | 0x02000000 <br/> | Der Abschnitt kann nach Bedarf verworfen werden. <br/>                                                                                                                         |
| IMAGE \_ SCN \_ MEM \_ NOT \_ CACHED <br/>          | 0x04000000 <br/> | Der Abschnitt kann nicht zwischengespeichert werden. <br/>                                                                                                                                   |
| IMAGE \_ SCN \_ MEM \_ NOT \_ PAGED <br/>           | 0x08000000 <br/> | Der Abschnitt kann nicht auslagerungsfähig sein. <br/>                                                                                                                                    |
| IMAGE \_ SCN \_ MEM \_ SHARED <br/>               | 0x10000000 <br/> | Der Abschnitt kann im Arbeitsspeicher freigegeben werden. <br/>                                                                                                                            |
| IMAGE \_ SCN \_ MEM \_ EXECUTE <br/>              | 0x20000000 <br/> | Der Abschnitt kann als Code ausgeführt werden. <br/>                                                                                                                            |
| IMAGE \_ SCN \_ MEM \_ READ <br/>                 | 0x40000000 <br/> | Der Abschnitt kann gelesen werden. <br/>                                                                                                                                        |
| IMAGE \_ SCN \_ MEM \_ WRITE <br/>                | 0x80000000 <br/> | In den Abschnitt kann geschrieben werden. <br/>                                                                                                                                  |



 

IMAGE \_ SCN \_ LNK \_ NRELOC OVFL gibt an, dass die Anzahl der Verschiebungen für den Abschnitt die 16 Bits überschreitet, die für ihn \_ im Abschnittsheader reserviert sind. Wenn das Bit festgelegt ist und das Feld NumberOfRelocations im Abschnittsheader 0xffff ist, wird die tatsächliche Anzahl der Verschiebungen im 32-Bit-Feld VirtualAddress der ersten Verschiebung gespeichert. Es ist ein Fehler, wenn IMAGE \_ SCN \_ LNK \_ NRELOC OVFL festgelegt ist und weniger als 0xffff im Abschnitt \_ angezeigt werden.

### <a name="grouped-sections-object-only"></a>Grouped Sections (Object Only)

Das "$"? -Zeichen (Dollarzeichen) hat eine besondere Interpretation in Abschnittsnamen in Objektdateien.

Wenn der Bildabschnitt bestimmt wird, der den Inhalt eines Objektabschnitts enthält, verwirft der Linker das "$"? und alle zeichen, die darauf folgen. Daher ein Objektabschnitt mit dem Namen . **text$X** trägt tatsächlich zum **Textabschnitt** im Bild bei.

Die Zeichen, die auf "$" folgen? bestimmt die Reihenfolge der Beiträge zum Bildabschnitt. Alle Beiträge mit demselben Objektabschnittsnamen werden zusammenhängend im Bild zugeordnet, und die Beiträge werden in lexikalischer Reihenfolge nach Objektabschnittsnamen sortiert. Aus diesem Grund werden alle Objekte in Objektdateien mit dem Abschnittsnamen **.text$X** nach den **.text$W-Beiträgen** und vor den **.text$Y-Beiträgen** zusammenkommen.

Der Abschnittsname in einer Bilddatei enthält nie "$"? befinden.

## <a name="other-contents-of-the-file"></a>Anderer Inhalt der Datei

- [Abschnittsdaten](#section-data)
- [COFF-Verschiebungen (nur Objekt)](#coff-relocations-object-only)
  - [Typindikatoren](#type-indicators)
- [COFF-Zeilennummern (veraltet)](#coff-line-numbers-deprecated)
- [COFF-Symboltabelle](#coff-symbol-table)
  - [Symbolnamendarstellung](#symbol-name-representation)
  - [Abschnittsnummerwerte](#section-number-values)
  - [Typdarstellung](#type-representation)
  - [Storage Klasse](#storage-class)
- [Hilfssymboldatensätze](#auxiliary-symbol-records)
  - [Hilfsformat 1: Funktionsdefinitionen](#auxiliary-format-1-function-definitions)
  - [Hilfsformat 2: Bf- und EF-Symbole](#auxiliary-format-2-bf-and-ef-symbols)
  - [Hilfsformat 3: Schwache externe Daten](#auxiliary-format-3-weak-externals)
  - [Hilfsformat 4: Dateien](#auxiliary-format-4-files)
  - [Hilfsformat 5: Abschnittsdefinitionen](#auxiliary-format-5-section-definitions)
  - [COMDAT-Abschnitte (nur Objekt)](#comdat-sections-object-only)
  - [CLR-Tokendefinition (nur Objekt)](#clr-token-definition-object-only)
- [COFF-Zeichenfolgentabelle](#coff-string-table)
- [Attributzertifikattabelle (nur Bild)](#the-attribute-certificate-table-image-only)
  - [Zertifikatdaten](#certificate-data)
- [Verzögertes Laden von Importtabellen (nur Image)](#delay-load-import-tables-image-only)
  - [Die Delay-Load Directory-Tabelle](#the-delay-load-directory-table)
  - [Attribute](#attributes)
  - [Name](#name)
  - [Modulhand handle](#module-handle)
  - [Verzögerte Importadressentabelle](#delay-import-address-table)
  - [Tabelle "Verzögerter Importname"](#delay-import-name-table)
  - [Verzögerte gebundene Importadressentabelle und Zeitstempel](#delay-bound-import-address-table-and-time-stamp)
  - [Tabelle zum Verzögerten Entladen von Importadressen](#delay-unload-import-address-table)

Die bisher beschriebenen Datenstrukturen bis einschließlich des optionalen Headers befinden sich alle an einem festen Offset vom Anfang der Datei (oder vom PE-Header, wenn die Datei ein Bild ist, das einen MS-DOS-Stub enthält).

Der Rest eines COFF-Objekts oder einer Bilddatei enthält Datenblöcke, die nicht notwendigerweise an einem bestimmten Dateioffset liegen. Stattdessen werden die Speicherorte durch Zeiger im optionalen Header oder einem Abschnittsheader definiert.

Eine Ausnahme sind Bilder mit einem SectionAlignment-Wert, der kleiner als die Seitengröße der Architektur ist (4 K für Intel x86 und für MIPS und 8 K für Itanium). Eine Beschreibung von SectionAlignment finden Sie unter [OptionalEr Header (nur Bild)](#optional-header-image-only). In diesem Fall gelten Einschränkungen für den Dateioffset der Abschnittsdaten, wie in Abschnitt 5.1, "Abschnittsdaten" beschrieben. Eine weitere Ausnahme ist, dass Attributzertifikat- und Debuginformationen ganz am Ende einer Imagedatei platziert werden müssen, während die Attributzertifikattabelle unmittelbar vor dem Debugabschnitt steht, da das Lademodul diese nicht dem Arbeitsspeicher zuteilt. Die Regel über Attributzertifikat- und Debuginformationen gilt jedoch nicht für Objektdateien.

### <a name="section-data"></a>Abschnittsdaten

Initialisierte Daten für einen Abschnitt bestehen aus einfachen Byteblöcken. Für Abschnitte, die alle Nullen enthalten, müssen die Abschnittsdaten jedoch nicht eingeschlossen werden.

Die Daten für jeden Abschnitt befinden sich am Dateioffset, der durch das Feld PointerToRawData im Abschnittsheader angegeben wurde. Die Größe dieser Daten in der Datei wird durch das Feld SizeOfRawData angegeben. Wenn SizeOfRawData kleiner als VirtualSize ist, wird der Rest mit Nullen aufschlossen.

In einer Bilddatei müssen die Abschnittsdaten an einer Grenze ausgerichtet werden, wie im Feld FileAlignment im optionalen Header angegeben. Abschnittsdaten müssen in der Reihenfolge der RVA-Werte für die entsprechenden Abschnitte angezeigt werden (wie die einzelnen Abschnittsheader in der Abschnittstabelle).

Es gibt zusätzliche Einschränkungen für Bilddateien, wenn der SectionAlignment-Wert im optionalen Header kleiner als die Seitengröße der Architektur ist. Für solche Dateien muss der Speicherort der Abschnittsdaten in der Datei mit dem Speicherort im Arbeitsspeicher übereinstimmen, wenn das Bild geladen wird, sodass der physische Offset für Abschnittsdaten mit dem RVA identisch ist.

### <a name="coff-relocations-object-only"></a>COFF-Verschiebungen (nur Objekt)

Objektdateien enthalten COFF-Verschiebungen, die angeben, wie die Abschnittsdaten geändert werden sollen, wenn sie in der Bilddatei platziert und anschließend in den Arbeitsspeicher geladen werden.

Bilddateien enthalten keine COFF-Verschiebungen, da allen Referenzsymbolen bereits Adressen in einem flachen Adressraum zugewiesen wurden. Ein Image enthält Verschiebungsinformationen in Form von Basisverlagerungen im Abschnitt .reloc (es sei denn, das Image verfügt über das ATTRIBUT IMAGE \_ FILE \_ RELOCS \_ STRIPPED). Weitere Informationen finden Sie im [Abschnitt .reloc (nur Image).](#the-reloc-section-image-only)

Für jeden Abschnitt in einer Objektdatei enthält ein Array von Datensätzen fester Länge die COFF-Verschiebungen des Abschnitts. Die Position und Länge des Arrays werden im Abschnittsheader angegeben. Jedes Element des Arrays hat das folgende Format.



| Offset        | Size          | Feld                        | Beschreibung                                                                                                                                                                                                                                                                                                                                                     |
|---------------|---------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | VirtualAddress <br/>   | Die Adresse des Elements, auf das die Verschiebung angewendet wird. Dies ist der Offset vom Anfang des Abschnitts plus dem Wert des RVA/Offset-Felds des Abschnitts. Siehe [Abschnittstabelle (Abschnittsheader)](#section-table-section-headers). Wenn das erste Byte des Abschnitts beispielsweise die Adresse 0x10, hat das dritte Byte die Adresse 0x12. <br/> |
| 4 <br/> | 4 <br/> | SymbolTableIndex <br/> | Ein nullbasierter Index in der Symboltabelle. Dieses Symbol gibt die Adresse an, die für die Verschiebung verwendet werden soll. Wenn das angegebene Symbol über eine Abschnittsspeicherklasse verfügt, ist die Adresse des Symbols die Adresse mit dem ersten Abschnitt desselben Namens. <br/>                                                                                                 |
| 8 <br/> | 2 <br/> | Typ <br/>             | Ein -Wert, der die Art der Verschiebung angibt, die ausgeführt werden soll. Gültige Verschiebungstypen hängen vom Computertyp ab. Weitere Informationen [finden Sie unter Typindikatoren](#type-indicators). <br/>                                                                                                                                                                                     |



 

Wenn das Symbol, auf das durch das Feld SymbolTableIndex verwiesen wird, über die Speicherklasse IMAGE SYM CLASS SECTION verfügt, ist die Adresse des Symbols der \_ \_ Anfang des \_ Abschnitts. Der Abschnitt befindet sich in der Regel in derselben Datei, außer wenn die Objektdatei Teil eines Archivs (Bibliothek) ist. In diesem Fall ist der Abschnitt in jeder anderen Objektdatei im Archiv zu finden, die über denselben Archivmitgliedsnamen wie die aktuelle Objektdatei verfügt. (Die Beziehung mit dem Namen des Archivmitglieds wird beim Verknüpfen von Importtabellen verwendet, d.h. im Abschnitt .idata.)

#### <a name="type-indicators"></a>Typindikatoren

Das Feld Typ des Verschiebungsdatensatz gibt an, welche Art von Verschiebung durchgeführt werden soll. Für jeden Computertyp werden unterschiedliche Verschiebungstypen definiert.

##### <a name="x64-processors"></a>x64-Prozessoren

Die folgenden Verschiebungstypindikatoren werden für x64- und kompatible Prozessoren definiert.



| Konstante                                | Wert              | Beschreibung                                                                                                                                                   |
|-----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ AMD64 \_ ABSOLUTE <br/> | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                        |
| IMAGE \_ REL \_ AMD64 \_ ADDR64 <br/>   | 0x0001 <br/> | Die 64-Bit-Va des Verschiebungsziels. <br/>                                                                                                           |
| IMAGE \_ REL \_ AMD64 \_ ADDR32 <br/>   | 0x0002 <br/> | Die 32-Bit-Va des Verschiebungsziels. <br/>                                                                                                           |
| IMAGE \_ REL \_ AMD64 \_ ADDR32NB <br/> | 0x0003 <br/> | Die 32-Bit-Adresse ohne Imagebasis (RVA). <br/>                                                                                                   |
| IMAGE \_ REL \_ AMD64 \_ REL32 <br/>    | 0x0004 <br/> | Die relative 32-Bit-Adresse aus dem Byte nach der Verschiebung. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 1 <br/> | 0x0005 <br/> | Die 32-Bit-Adresse relativ zum Byteabstand 1 von der Verschiebung. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 2 <br/> | 0x0006 <br/> | Die 32-Bit-Adresse relativ zum Byteabstand 2 von der Verschiebung. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 3 <br/> | 0x0007 <br/> | Die 32-Bit-Adresse relativ zum Byteabstand 3 von der Verschiebung. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 4 <br/> | 0x0008 <br/> | Die 32-Bit-Adresse relativ zum Byteabstand 4 von der Verschiebung. <br/>                                                                               |
| IMAGE \_ REL \_ AMD64 \_ REL32 \_ 5 <br/> | 0x0009 <br/> | Die 32-Bit-Adresse relativ zum Byteabstand 5 von der Verschiebung. <br/>                                                                               |
| ABSCHNITT "IMAGE \_ REL \_ AMD64" \_ <br/>  | 0x000A <br/> | Der 16-Bit-Abschnittsindex des Abschnitts, der das Ziel enthält. Dies wird verwendet, um Debuginformationen zu unterstützen. <br/>                                  |
| IMAGE \_ REL \_ AMD64 \_ SECREL <br/>   | 0x000B <br/> | Der 32-Bit-Offset des Ziels vom Anfang des Abschnitts. Dies wird verwendet, um Debuginformationen und statischen lokalen Threadspeicher zu unterstützen. <br/> |
| IMAGE \_ REL \_ AMD64 \_ SECREL7 <br/>  | 0x000C <br/> | Ein 7-Bit-Offset ohne Vorzeichen von der Basis des Abschnitts, der das Ziel enthält. <br/>                                                                    |
| IMAGE \_ REL \_ AMD64 \_ TOKEN <br/>    | 0x000D <br/> | CLR-Token. <br/>                                                                                                                                       |
| IMAGE \_ REL \_ AMD64 \_ SREL32 <br/>   | 0x000E <br/> | Ein 32-Bit-Wert, der von einer Spanne signiert ist und in das -Objekt ausgegeben wird. <br/>                                                                                     |
| IMAGE \_ REL \_ AMD64-PAAR \_ <br/>     | 0x000F <br/> | Ein Paar, das unmittelbar auf jeden span-abhängigen Wert folgen muss. <br/>                                                                                   |
| IMAGE \_ REL \_ AMD64 \_ SSPAN32 <br/>  | 0x0010 <br/> | Ein 32-Bit-Wert, der von einer Spanne signiert ist und zur Linkzeit angewendet wird. <br/>                                                                                |



 

##### <a name="arm-processors"></a>ARM-Prozessoren

Die folgenden Indikatoren für den Verschiebungstyp werden für ARM-Prozessoren definiert.



| Konstante                                | Wert              | Beschreibung                                                                                                                                                                                                                                                            |
|-----------------------------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ ARM \_ ABSOLUTE <br/>   | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ ARM \_ ADDR32 <br/>     | 0x0001 <br/> | Die 32-Bit-Va des Ziels. <br/>                                                                                                                                                                                                                               |
| IMAGE \_ REL \_ ARM \_ ADDR32NB <br/>   | 0x0002 <br/> | Die 32-Bit-RVA des Ziels. <br/>                                                                                                                                                                                                                              |
| IMAGE \_ REL \_ ARM \_ BRANCH24 <br/>   | 0x0003 <br/> | Die relative 24-Bit-Verschiebung zum Ziel. <br/>                                                                                                                                                                                                            |
| IMAGE \_ REL \_ ARM \_ BRANCH11 <br/>   | 0x0004 <br/> | Der Verweis auf einen Unterroutinenaufruf. Der Verweis besteht aus zwei 16-Bit-Anweisungen mit 11-Bit-Offsets. <br/>                                                                                                                                                 |
| IMAGE \_ REL \_ ARM \_ REL32 <br/>      | 0x000A <br/> | Die relative 32-Bit-Adresse aus dem Byte nach der Verschiebung. <br/>                                                                                                                                                                                        |
| \_ARM-ABSCHNITT "IMAGE \_ REL" \_ <br/>    | 0x000E <br/> | Der 16-Bit-Abschnittsindex des Abschnitts, der das Ziel enthält. Dies wird verwendet, um Debuginformationen zu unterstützen. <br/>                                                                                                                                           |
| IMAGE \_ REL \_ ARM \_ SECREL <br/>     | 0x000F <br/> | Der 32-Bit-Offset des Ziels vom Anfang des Abschnitts. Dies wird verwendet, um Debuginformationen und statischen lokalen Threadspeicher zu unterstützen. <br/>                                                                                                          |
| IMAGE \_ REL \_ ARM \_ MOV32 <br/>      | 0x0010 <br/> | Die 32-Bit-Va des Ziels. Diese Verschiebung wird mithilfe einer MOVW-Anweisung für die niedrigen 16 Bits angewendet, gefolgt von einem MOVT für die hohen 16 Bits. <br/>                                                                                                              |
| \_BILDREL \_ THUMB \_ MOV32 <br/>    | 0x0011 <br/> | Die 32-Bit-VA des Ziels. Diese Verschiebung wird mithilfe einer MOVW-Anweisung für die niedrigen 16 Bits angewendet, gefolgt von einem MOVT für die hohen 16 Bits. <br/>                                                                                                              |
| IMAGE \_ REL \_ THUMB \_ BRANCH20 <br/> | 0x0012 <br/> | Die Anweisung wird mit der relativen Verschiebung von 21 Bit zum 2-Byte-ausgerichteten Ziel korrigiert. Das am wenigsten signifikante Teil der Verschiebung ist immer 0 (null) und wird nicht gespeichert. Diese Verschiebung entspricht einer bedingte 32-Bit-Thumb-2-B-Anweisung. <br/> |
| Nicht verwendet <br/>                      | 0x0013 <br/> |                                                                                                                                                                                                                                                                        |
| IMAGE \_ REL \_ THUMB \_ BRANCH24 <br/> | 0x0014 <br/> | Die Anweisung wird mit der relativen Verschiebung von 25 Bit zum 2-Byte-ausgerichteten Ziel korrigiert. Das am wenigsten signifikante Teil der Verschiebung ist 0 (null) und wird nicht gespeichert. Diese Verschiebung entspricht einer Thumb-2 B-Anweisung. <br/>                            |
| IMAGE \_ REL \_ THUMB \_ BLX23 <br/>    | 0x0015 <br/> | Die Anweisung wird mit der relativen Verschiebung von 25 Bit zum 4-Byte-ausgerichteten Ziel korrigiert. Die niedrigen 2 Bits der Verschiebung sind 0 (null) und werden nicht gespeichert. <br/> Diese Verschiebung entspricht einer Thumb-2 BLX-Anweisung. <br/>                      |
| \_ARM-PAAR "IMAGE \_ REL" \_ <br/>       | 0x0016 <br/> | Die Verschiebung ist nur gültig, wenn sie unmittelbar auf eine ARM \_ REFHI oder THUMB \_ REFHI folgt. SymbolTableIndex enthält eine Verschiebung und keinen Index in der Symboltabelle. <br/>                                                                                |



 

##### <a name="arm64-processors"></a>ARM64-Prozessoren

Die folgenden Verlagerungstypindikatoren sind für ARM64-Prozessoren definiert.



| Konstante                                       | Wert              | Beschreibung                                                                                                                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ ARM64 \_ ABSOLUTE <br/>        | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                        |
| IMAGE \_ REL \_ ARM64 \_ ADDR32 <br/>          | 0x0001 <br/> | Die 32-Bit-VA des Ziels. <br/>                                                                                                                      |
| IMAGE \_ REL \_ ARM64 \_ ADDR32NB <br/>        | 0x0002 <br/> | Das 32-Bit-RVA des Ziels. <br/>                                                                                                                     |
| IMAGE \_ REL \_ ARM64 \_ BRANCH26 <br/>        | 0x0003 <br/> | Die relative Verschiebung von 26 Bit zum Ziel für B- und BL-Anweisungen. <br/>                                                                        |
| IMAGE \_ REL \_ ARM64 \_ PAGEBASE \_ REL21 <br/> | 0x0004 <br/> | Die Seitenbasis des Ziels für die ADRP-Anweisung. <br/>                                                                                                |
| IMAGE \_ REL \_ ARM64 \_ REL21 <br/>           | 0x0005 <br/> | Die relative Verschiebung von 12 Bit zum Ziel für die Anweisung ADR <br/>                                                                               |
| IMAGE \_ REL \_ ARM64 \_ PAGEOFFSET \_ 12A <br/> | 0x0006 <br/> | Der 12-Bit-Seitenoffset des Ziels, für Anweisungen ADD/ADDS (direkt) mit null Verschiebung. <br/>                                                      |
| IMAGE \_ REL \_ ARM64 \_ PAGEOFFSET \_ 12L <br/> | 0x0007 <br/> | Der 12-Bit-Seitenoffset des Ziels für die Anweisung LDR (indexed, unsigned immediate). <br/>                                                          |
| IMAGE \_ REL \_ ARM64 \_ SECREL <br/>          | 0x0008 <br/> | Der 32-Bit-Offset des Ziels vom Anfang des Abschnitts. Dies wird verwendet, um Debuginformationen und statischen lokalen Threadspeicher zu unterstützen. <br/> |
| IMAGE \_ REL \_ ARM64 \_ SECREL \_ LOW12A <br/>  | 0x0009 <br/> | Bit 0:11 des Abschnittsoffsets des Ziels, für Anweisungen ADD/ADDS (direkt) mit Nullverschiebung. <br/>                                                  |
| IMAGE \_ REL \_ ARM64 \_ SECREL \_ HIGH12A <br/> | 0x000A <br/> | Bit 12:23 des Abschnittsoffsets des Ziels, für Anweisungen ADD/ADDS (direkt) mit Nullverschiebung. <br/>                                                 |
| IMAGE \_ REL \_ ARM64 \_ SECREL \_ LOW12L <br/>  | 0x000B <br/> | Bit 0:11 des Abschnittsoffsets des Ziels für die Anweisung LDR (indexed, unsigned immediate). <br/>                                                      |
| IMAGE \_ REL \_ ARM64 \_ TOKEN <br/>           | 0x000C <br/> | CLR-Token. <br/>                                                                                                                                        |
| IMAGE \_ REL \_ ARM64 \_ SECTION <br/>         | 0x000D <br/> | Der 16-Bit-Abschnittsindex des Abschnitts, der das Ziel enthält. Dies wird verwendet, um Debuginformationen zu unterstützen. <br/>                                  |
| IMAGE \_ REL \_ ARM64 \_ ADDR64 <br/>          | 0x000E <br/> | Die 64-Bit-VA des Verschiebungsziels. <br/>                                                                                                           |
| IMAGE \_ REL \_ ARM64 \_ BRANCH19 <br/>        | 0x000F <br/> | Der 19-Bit-Offset zum Verschiebungsziel für die bedingte B-Anweisung. <br/>                                                                        |
| IMAGE \_ REL \_ ARM64 \_ BRANCH14 <br/>        | 0x0010 <br/> | Der 14-Bit-Offset zum Verschiebungsziel für die Anweisungen TBZ und TBNZ. <br/>                                                                        |
| IMAGE \_ REL \_ ARM64 \_ REL32 <br/>           | 0x0011 <br/> | Die relative 32-Bit-Adresse aus dem Byte nach der Verschiebung. <br/>                                                                               |

##### <a name="hitachi-superh-processors"></a>SuperH-Prozessoren

Die folgenden Verlagerungstypindikatoren sind für SH3- und SH4-Prozessoren definiert. SH5-spezifische Verlagerungen werden als SHM (SH Media) bezeichnet.



| Konstante                                      | Wert              | Beschreibung                                                                                                                                                                                                                |
|-----------------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ SH3 \_ ABSOLUTE <br/>         | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                                                                                     |
| IMAGE \_ REL \_ SH3 \_ DIRECT16 <br/>         | 0x0001 <br/> | Ein Verweis auf die 16-Bit-Position, die die Va des Zielsymbols enthält. <br/>                                                                                                                                  |
| IMAGE \_ REL \_ SH3 \_ DIRECT32 <br/>         | 0x0002 <br/> | Die 32-Bit-VA des Zielsymbols. <br/>                                                                                                                                                                            |
| IMAGE \_ REL \_ SH3 \_ DIRECT8 <br/>          | 0x0003 <br/> | Ein Verweis auf die 8-Bit-Position, die die Va des Zielsymbols enthält. <br/>                                                                                                                                   |
| IMAGE \_ REL \_ SH3 \_ DIRECT8 \_ WORD <br/>    | 0x0004 <br/> | Ein Verweis auf die 8-Bit-Anweisung, die die effektive 16-Bit-Va des Zielsymbols enthält. <br/>                                                                                                               |
| IMAGE \_ REL \_ SH3 \_ DIRECT8 \_ LONG <br/>    | 0x0005 <br/> | Ein Verweis auf die 8-Bit-Anweisung, die die effektive 32-Bit-Va des Zielsymbols enthält. <br/>                                                                                                               |
| IMAGE \_ REL \_ SH3 \_ DIRECT4 <br/>          | 0x0006 <br/> | Ein Verweis auf die 8-Bit-Position, deren niedrige 4 Bits die VA des Zielsymbols enthalten. <br/>                                                                                                                        |
| IMAGE \_ REL \_ SH3 \_ DIRECT4 \_ WORD <br/>    | 0x0007 <br/> | Ein Verweis auf die 8-Bit-Anweisung, deren niedrige 4 Bits die effektive 16-Bit-VA des Zielsymbols enthalten. <br/>                                                                                                    |
| IMAGE \_ REL \_ SH3 \_ DIRECT4 \_ LONG <br/>    | 0x0008 <br/> | Ein Verweis auf die 8-Bit-Anweisung, deren niedrige 4 Bits die effektive 32-Bit-Va des Zielsymbols enthalten. <br/>                                                                                                    |
| IMAGE \_ REL \_ SH3 \_ PCREL8 \_ WORD <br/>     | 0x0009 <br/> | Ein Verweis auf die 8-Bit-Anweisung, die den effektiven relativen 16-Bit-Offset des Zielsymbols enthält. <br/>                                                                                                  |
| IMAGE \_ REL \_ SH3 \_ PCREL8 \_ LONG <br/>     | 0x000A <br/> | Ein Verweis auf die 8-Bit-Anweisung, die den effektiven relativen 32-Bit-Offset des Zielsymbols enthält. <br/>                                                                                                  |
| IMAGE \_ REL \_ SH3 \_ PCREL12 \_ WORD <br/>    | 0x000B <br/> | Ein Verweis auf die 16-Bit-Anweisung, deren niedrige 12 Bits den effektiven relativen 16-Bit-Offset des Zielsymbols enthalten. <br/>                                                                                     |
| IMAGE \_ REL \_ SH3 \_ STARTOF \_ SECTION <br/> | 0x000C <br/> | Ein Verweis auf eine 32-Bit-Position, bei der es sich um die Va des Abschnitts handelt, der das Zielsymbol enthält. <br/>                                                                                                                |
| IMAGE \_ REL \_ SH3 \_ SIZEOF \_ SECTION <br/>  | 0x000D <br/> | Ein Verweis auf die 32-Bit-Position, die der Größe des Abschnitts entspricht, der das Zielsymbol enthält. <br/>                                                                                                            |
| ABSCHNITT "IMAGE \_ REL \_ \_ SH3" <br/>          | 0x000E <br/> | Der 16-Bit-Abschnittsindex des Abschnitts, der das Ziel enthält. Dies wird verwendet, um Debuginformationen zu unterstützen. <br/>                                                                                               |
| IMAGE \_ REL \_ SH3 \_ SECREL <br/>           | 0x000F <br/> | Der 32-Bit-Offset des Ziels vom Anfang des Abschnitts. Dies wird verwendet, um Debuginformationen und statischen lokalen Threadspeicher zu unterstützen. <br/>                                                              |
| IMAGE \_ REL \_ SH3 \_ DIRECT32 \_ NB <br/>     | 0x0010 <br/> | Die 32-Bit-RVA des Zielsymbols. <br/>                                                                                                                                                                           |
| IMAGE \_ REL \_ SH3 \_ GPREL4 \_ LONG <br/>     | 0x0011 <br/> | GP relativ. <br/>                                                                                                                                                                                                   |
| IMAGE \_ REL \_ SH3 \_ TOKEN <br/>            | 0x0012 <br/> | CLR-Token. <br/>                                                                                                                                                                                                     |
| IMAGE \_ REL \_ SHM \_ PCRELPT <br/>          | 0x0013 <br/> | Der Offset der aktuellen Anweisung in Longwords. Wenn das NOMODE-Bit nicht festgelegt ist, fügen Sie die Umkehrung des niedrigen Bits bei Bit 32 ein, um PTA oder PTB auszuwählen. <br/>                                                          |
| IMAGE \_ REL \_ SHM \_ REFLO <br/>            | 0x0014 <br/> | Die niedrigen 16 Bits der 32-Bit-Adresse. <br/>                                                                                                                                                                         |
| IMAGE \_ REL \_ SHM \_ REFHALF <br/>          | 0x0015 <br/> | Die hohen 16 Bits der 32-Bit-Adresse. <br/>                                                                                                                                                                        |
| IMAGE \_ REL \_ SHM \_ REUK <br/>            | 0x0016 <br/> | Die niedrigen 16 Bits der relativen Adresse. <br/>                                                                                                                                                                       |
| IMAGE \_ REL \_ SHM \_ RELHALF <br/>          | 0x0017 <br/> | Die hohen 16 Bits der relativen Adresse. <br/>                                                                                                                                                                      |
| IMAGE \_ REL \_ SHM \_ PAIR <br/>             | 0x0018 <br/> | Die Verschiebung ist nur gültig, wenn sie unmittelbar auf eine REFHALF-, RELHALF- oder REHAL-Verschiebung folgt. Das Feld SymbolTableIndex der Verschiebung enthält eine Verschiebung und keinen Index in der Symboltabelle. <br/> |
| IMAGE \_ REL \_ SHM \_ NOMODE <br/>           | 0x8000 <br/> | Bei der Verschiebung wird der Abschnittsmodus ignoriert. <br/>                                                                                                                                                                           |



 

##### <a name="ibm-powerpc-processors"></a>IBM PowerPC-Prozessoren

Die folgenden Verlagerungstypindikatoren werden für PowerPC Prozessoren definiert.



| Konstante                              | Wert              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ PPC \_ ABSOLUTE <br/> | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                                                                                                                                                                                                                                              |
| IMAGE \_ REL \_ PPC \_ ADDR64 <br/>   | 0x0001 <br/> | Die 64-Bit-Va des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                            |
| IMAGE \_ REL \_ PPC \_ ADDR32 <br/>   | 0x0002 <br/> | Die 32-Bit-VA des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                            |
| IMAGE \_ REL \_ PPC \_ ADDR24 <br/>   | 0x0003 <br/> | Die niedrigen 24 Bits der VA des Ziels. Dies ist nur gültig, wenn das Zielsymbol absolut ist und auf seinen ursprünglichen Wert erweitert werden kann. <br/>                                                                                                                                                                                                                          |
| IMAGE \_ REL \_ PPC \_ ADDR16 <br/>   | 0x0004 <br/> | Die niedrigen 16 Bits der Va des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ REL \_ PPC \_ ADDR14 <br/>   | 0x0005 <br/> | Die niedrigen 14 Bits der Va des Ziels. Dies ist nur gültig, wenn das Zielsymbol absolut ist und auf seinen ursprünglichen Wert erweitert werden kann. <br/>                                                                                                                                                                                                                               |
| IMAGE \_ REL \_ PPC \_ REL24 <br/>    | 0x0006 <br/> | Ein 24-Bit-PC-relativer Offset zum Speicherort des Symbols. <br/>                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ PPC \_ REL14 <br/>    | 0x0007 <br/> | Ein 14-Bit-PC-relativer Offset zur Position des Symbols. <br/>                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ PPC \_ ADDR32NB <br/> | 0x000A <br/> | Die 32-Bit-RVA des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                           |
| IMAGE \_ REL \_ PPC \_ SECREL <br/>   | 0x000B <br/> | Der 32-Bit-Offset des Ziels vom Anfang des Abschnitts. Dies wird verwendet, um Debuginformationen und statischen lokalen Threadspeicher zu unterstützen. <br/>                                                                                                                                                                                                                       |
| ABSCHNITT "IMAGE \_ REL \_ \_ PPC" <br/>  | 0x000C <br/> | Der 16-Bit-Abschnittsindex des Abschnitts, der das Ziel enthält. Dies wird verwendet, um Debuginformationen zu unterstützen. <br/>                                                                                                                                                                                                                                                        |
| IMAGE \_ REL \_ PPC \_ SECREL16 <br/> | 0x000F <br/> | Der 16-Bit-Offset des Ziels vom Anfang des Abschnitts. Dies wird verwendet, um Debuginformationen und statischen lokalen Threadspeicher zu unterstützen. <br/>                                                                                                                                                                                                                       |
| IMAGE \_ REL \_ PPC \_ REFHI <br/>    | 0x0010 <br/> | Die hohen 16 Bits der 32-Bit-Va des Ziels. Dies wird für die erste Anweisung in einer Sequenz mit zwei Anweisungen verwendet, die eine vollständige Adresse lädt. Auf diese Verschiebung muss sofort eine PAIR-Verschiebung folgen, deren SymbolTableIndex eine signierte 16-Bit-Verschiebung enthält, die den oberen 16 Bits hinzugefügt wird, die von der Position übernommen wurden, die verschoben wird. <br/> |
| IMAGE \_ REL \_ PPC \_ REFLO <br/>    | 0x0011 <br/> | Die niedrigen 16 Bits der Va des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                     |
| \_BILDREL \_ \_ PPC-PAAR <br/>     | 0x0012 <br/> | Eine Verschiebung, die nur gültig ist, wenn sie unmittelbar auf eine REFHI- oder SECRELHI-Verschiebung folgt. Der SymbolTableIndex enthält eine Verschiebung und keinen Index in der Symboltabelle. <br/>                                                                                                                                                                                        |
| IMAGE \_ REL \_ PPC \_ SECRELLO <br/> | 0x0013 <br/> | Die niedrigen 16 Bits des 32-Bit-Offsets des Ziels vom Anfang des Abschnitts. <br/>                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ PPC \_ GPREL <br/>    | 0x0015 <br/> | Die 16-Bit-Verschiebung des Ziels mit Vor signed relativ zum GP-Register. <br/>                                                                                                                                                                                                                                                                                               |
| IMAGE \_ REL \_ PPC \_ TOKEN <br/>    | 0x0016 <br/> | Das CLR-Token. <br/>                                                                                                                                                                                                                                                                                                                                                          |



 

##### <a name="intel-386-processors"></a>Intel 386-Prozessoren

Für Intel 386 und kompatible Prozessoren sind die folgenden Indikatoren für den Verschiebungstyp definiert.



| Konstante                               | Wert              | Beschreibung                                                                                                                                                   |
|----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ I386 \_ ABSOLUTE <br/> | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                        |
| IMAGE \_ REL \_ I386 \_ DIR16 <br/>    | 0x0001 <br/> | Wird nicht unterstützt. <br/>                                                                                                                                    |
| IMAGE \_ REL \_ I386 \_ REL16 <br/>    | 0x0002 <br/> | Wird nicht unterstützt. <br/>                                                                                                                                    |
| IMAGE \_ REL \_ I386 \_ DIR32 <br/>    | 0x0006 <br/> | Die 32-Bit-Va des Ziels. <br/>                                                                                                                           |
| IMAGE \_ REL \_ I386 \_ DIR32NB <br/>  | 0x0007 <br/> | Die 32-Bit-RVA des Ziels. <br/>                                                                                                                          |
| IMAGE \_ REL \_ I386 \_ SEG12 <br/>    | 0x0009 <br/> | Wird nicht unterstützt. <br/>                                                                                                                                    |
| ABSCHNITT \_ "IMAGE REL \_ I386" \_ <br/>  | 0x000A <br/> | Der 16-Bit-Abschnittsindex des Abschnitts, der das Ziel enthält. Dies wird verwendet, um Debuginformationen zu unterstützen. <br/>                                  |
| IMAGE \_ REL \_ I386 \_ SECREL <br/>   | 0x000B <br/> | Der 32-Bit-Offset des Ziels vom Anfang des Abschnitts. Dies wird verwendet, um Debuginformationen und statischen lokalen Threadspeicher zu unterstützen. <br/> |
| IMAGE \_ REL \_ I386 \_ TOKEN <br/>    | 0x000C <br/> | Das CLR-Token. <br/>                                                                                                                                    |
| IMAGE \_ REL \_ I386 \_ SECREL7 <br/>  | 0x000D <br/> | Ein 7-Bit-Offset von der Basis des Abschnitts, der das Ziel enthält. <br/>                                                                             |
| IMAGE \_ REL \_ I386 \_ REL32 <br/>    | 0x0014 <br/> | Die relative 32-Bit-Verschiebung zum Ziel. Dies unterstützt den relativen x86-Branch und Aufrufanweisungen. <br/>                                      |



 

##### <a name="intel-itanium-processor-family-ipf"></a>Intel Itanium-Prozessorfamilie (IPF)

Die folgenden Verschiebungstypindikatoren werden für die Intel Itanium-Prozessorfamilie und kompatible Prozessoren definiert. Beachten Sie, dass verschiebungen bei Anweisungen die Offset- und Slotnummer des Bündels für den Verschiebungsoffset verwenden.



| Konstante                                 | Wert              | Beschreibung                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ IA64 \_ ABSOLUTE <br/>   | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                                                                                                                                                                                                          |
| IMAGE \_ REL \_ IA64 \_ IMM14 <br/>      | 0x0001 <br/> | Auf die Anweisungsverlagerung kann eine ADDEND-Verschiebung folgen, deren Wert der Zieladresse hinzugefügt wird, bevor sie in den angegebenen Slot im IMM14-Paket eingefügt wird. Das Verschiebungsziel muss absolut sein, oder das Image muss korrigiert werden. <br/>                                                                                 |
| IMAGE \_ REL \_ IA64 \_ IMM22 <br/>      | 0x0002 <br/> | Auf die Anweisungsverlagerung kann eine ADDEND-Verschiebung folgen, deren Wert der Zieladresse hinzugefügt wird, bevor sie in den angegebenen Slot im IMM22-Paket eingefügt wird. Das Verschiebungsziel muss absolut sein, oder das Image muss korrigiert werden. <br/>                                                                                 |
| IMAGE \_ REL \_ IA64 \_ IMM64 <br/>      | 0x0003 <br/> | Die Slotnummer dieser Verschiebung muss eins (1) sein. Auf die Verschiebung kann eine ADDEND-Verschiebung folgen, deren Wert der Zieladresse hinzugefügt wird, bevor sie in allen drei Slots des IMM64-Pakets gespeichert wird. <br/>                                                                                                                   |
| IMAGE \_ REL \_ IA64 \_ DIR32 <br/>      | 0x0004 <br/> | Die 32-Bit-VA des Ziels. Dies wird nur für /LARGEADDRESSAWARE:NO-Images unterstützt. <br/>                                                                                                                                                                                                                                                    |
| IMAGE \_ REL \_ IA64 \_ DIR64 <br/>      | 0x0005 <br/> | Die 64-Bit-VA des Ziels. <br/>                                                                                                                                                                                                                                                                                                             |
| IMAGE \_ REL \_ IA64 \_ PCREL21B <br/>   | 0x0006 <br/> | Die Anweisung wird mit der relativen Verschiebung von 25 Bit zum 16-Bit-ausgerichteten Ziel korrigiert. Die niedrigen 4 Bits der Verschiebung sind 0 (null) und werden nicht gespeichert. <br/>                                                                                                                                                                     |
| IMAGE \_ REL \_ IA64 \_ PCREL21M <br/>   | 0x0007 <br/> | Die Anweisung wird mit der relativen Verschiebung von 25 Bit zum 16-Bit-ausgerichteten Ziel korrigiert. Die niedrigen 4 Bits der Verschiebung, die null sind, werden nicht gespeichert. <br/>                                                                                                                                                                 |
| IMAGE \_ REL \_ IA64 \_ PCREL21F <br/>   | 0x0008 <br/> | Die LSBs des Offsets dieser Verschiebung müssen die Slotnummer enthalten, während der Rest die Paketadresse ist. Das Paket wird mit der relativen Verschiebung von 25 Bit zum 16-Bit-ausgerichteten Ziel fixiert. Die niedrigen 4 Bits der Verschiebung sind 0 (null) und werden nicht gespeichert. <br/>                                                                |
| IMAGE \_ REL \_ IA64 \_ GPREL22 <br/>    | 0x0009 <br/> | Auf die Anweisungsverschiebung kann eine ADDEND-Verschiebung folgen, deren Wert der Zieladresse hinzugefügt wird, und dann ein 22-Bit-GP-relativer Offset, der berechnet und auf das GPREL22-Paket angewendet wird. <br/>                                                                                                                            |
| IMAGE \_ REL \_ IA64 \_ LTOFF22 <br/>    | 0x000A <br/> | Die Anweisung wird mit dem 22-Bit-GP-relativen Offset zum Literaltabelleneintrag des Zielsymbols korrigiert. Der Linker erstellt diesen Literaltabelleneintrag basierend auf dieser Verschiebung und der möglicherweise folgenden ADDEND-Verschiebung. <br/>                                                                                                        |
| ABSCHNITT \_ "IMAGE REL \_ IA64" \_ <br/>    | 0x000B <br/> | Der 16-Bit-Abschnittsindex des Abschnitts enthält das Ziel. Dies wird verwendet, um Debuginformationen zu unterstützen. <br/>                                                                                                                                                                                                                         |
| IMAGE \_ REL \_ IA64 \_ SECREL22 <br/>   | 0x000C <br/> | Die Anweisung wird mit dem 22-Bit-Offset des Ziels vom Anfang des Abschnitts korrigiert. Auf diese Verschiebung kann sofort eine ADDEND-Verschiebung folgen, deren Wertfeld den 32-Bit-Offset ohne Vorzeichen des Ziels vom Anfang des Abschnitts enthält. <br/>                                                     |
| ABBILDUNG \_ REL \_ IA64 \_ SECREL64I <br/>  | 0x000D <br/> | Die Slotnummer für diese Verschiebung muss eins (1) sein. Die Anweisung wird mit dem 64-Bit-Offset des Ziels vom Anfang des Abschnitts korrigiert. Auf diese Verschiebung kann sofort eine ADDEND-Verschiebung folgen, deren Wertfeld den 32-Bit-Offset ohne Vorzeichen des Ziels vom Anfang des Abschnitts enthält. <br/> |
| IMAGE \_ REL \_ IA64 \_ SECREL32 <br/>   | 0x000E <br/> | Die Adresse der Daten, die mit dem 32-Bit-Offset des Ziels vom Anfang des Abschnitts korrigiert werden sollen. <br/>                                                                                                                                                                                                                          |
| IMAGE \_ REL \_ IA64 \_ DIR32NB <br/>    | 0x0010 <br/> | Das 32-Bit-RVA des Ziels. <br/>                                                                                                                                                                                                                                                                                                            |
| IMAGE \_ REL \_ IA64 \_ SREL14 <br/>     | 0x0011 <br/> | Dies wird auf ein 14-Bit-Direktzeichen angewendet, das den Unterschied zwischen zwei wiederholbaren Zielen enthält. Dies ist ein deklaratives Feld für den Linker, das angibt, dass der Compiler diesen Wert bereits ausgegeben hat. <br/>                                                                                                              |
| IMAGE \_ REL \_ IA64 \_ SREL22 <br/>     | 0x0012 <br/> | Dies wird auf ein 22-Bit-Direktzeichen mit Vorzeichen angewendet, das den Unterschied zwischen zwei wiederholbaren Zielen enthält. Dies ist ein deklaratives Feld für den Linker, das angibt, dass der Compiler diesen Wert bereits ausgegeben hat. <br/>                                                                                                              |
| IMAGE \_ REL \_ IA64 \_ SREL32 <br/>     | 0x0013 <br/> | Dies wird auf ein 32-Bit-Direktzeichen mit Vorzeichen angewendet, das den Unterschied zwischen zwei wiederholbaren Werten enthält. Dies ist ein deklaratives Feld für den Linker, das angibt, dass der Compiler diesen Wert bereits ausgegeben hat. <br/>                                                                                                               |
| IMAGE \_ REL \_ IA64 \_ UREL32 <br/>     | 0x0014 <br/> | Dies wird auf ein 32-Bit-Direkt ohne Vorzeichen angewendet, das den Unterschied zwischen zwei wiederholbaren Werten enthält. Dies ist ein deklaratives Feld für den Linker, das angibt, dass der Compiler diesen Wert bereits ausgegeben hat. <br/>                                                                                                            |
| IMAGE \_ REL \_ IA64 \_ PCREL60X <br/>   | 0x0015 <br/> | Eine 60-Bit-PC-relative Fixup, die immer als BRL-Anweisung eines MLX-Bündels verbleibt. <br/>                                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ IA64 \_ PCREL60B <br/>   | 0x0016 <br/> | Eine 60-Bit-PC-relative Korrektur. Wenn die Zielverschiebung in ein 25-Bit-Feld mit Vorzeichen passt, konvertieren Sie das gesamte Paket in ein MBB-Bündel mit NOP. B in Slot 1 und eine 25-Bit-BR-Anweisung (mit den vier niedrigsten Bits alle null und verworfen) in Slot 2. <br/>                                                                                          |
| IMAGE \_ REL \_ IA64 \_ PCREL60F <br/>   | 0x0017 <br/> | Eine 60-Bit-PC-relative Korrektur. Wenn die Zielverschiebung in ein 25-Bit-Feld mit Vorzeichen passt, konvertieren Sie das gesamte Bündel in ein MFB-Bündel mit NOP. F in Slot 1 und eine 25-Bit-BR-Anweisung (4 niedrigste Bits alle null und verworfen) in Slot 2. <br/>                                                                                                   |
| IMAGE \_ REL \_ IA64 \_ PCREL60I <br/>   | 0x0018 <br/> | Eine 60-Bit-PC-relative Korrektur. Wenn die Zielverschiebung in ein 25-Bit-Feld mit Vorzeichen passt, konvertieren Sie das gesamte Bündel in ein MIB-Bündel mit NOP. Ich in Slot 1 und eine 25-Bit-BR-Anweisung (4 niedrigste Bits alle null und verworfen) in Slot 2. <br/>                                                                                                   |
| IMAGE \_ REL \_ IA64 \_ PCREL60M <br/>   | 0x0019 <br/> | Eine 60-Bit-PC-relative Korrektur. Wenn die Zielverschiebung in ein 25-Bit-Feld mit Vorzeichen passt, konvertieren Sie das gesamte Bündel in ein MMB-Bündel mit NOP. M in Slot 1 und eine 25-Bit-BR-Anweisung (4 niedrigste Bits alle null und verworfen) in Slot 2. <br/>                                                                                                   |
| IMAGE \_ REL \_ IA64 \_ IMMGPREL64 <br/> | 0x001a <br/> | Eine 64-Bit-GP-relative Korrektur. <br/>                                                                                                                                                                                                                                                                                                         |
| IMAGE \_ REL \_ IA64 \_ TOKEN <br/>      | 0x001b <br/> | Ein CLR-Token. <br/>                                                                                                                                                                                                                                                                                                                        |
| IMAGE \_ REL \_ IA64 \_ GPREL32 <br/>    | 0x001c <br/> | Ein 32-Bit-GP-relativer Fixup. <br/>                                                                                                                                                                                                                                                                                                         |
| IMAGE \_ REL \_ IA64 \_ ADDEND <br/>     | 0x001F <br/> | Die Verschiebung ist nur gültig, wenn sie unmittelbar auf eine der folgenden Verschiebungen folgt: IMM14, IMM22, IMM64, GPREL22, LTOFF22, LTOFF64, SECREL22, SECREL64I oder SECREL32. Der Wert enthält das Add-In, das auf Anweisungen in einem Bündel angewendet werden soll, nicht auf Daten. <br/>                                                                  |



 

##### <a name="mips-processors"></a>MIPS-Prozessoren

Die folgenden Verlagerungstypindikatoren werden für MIPS-Prozessoren definiert.



| Konstante                                | Wert              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ MIPS \_ ABSOLUTE <br/>  | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                                                                                                                                                                                                                                              |
| IMAGE \_ REL \_ MIPS \_ REFHALF <br/>   | 0x0001 <br/> | Die hohen 16 Bits der 32-Bit-Va des Ziels. <br/>                                                                                                                                                                                                                                                                                                                             |
| IMAGE \_ REL \_ MIPS \_ REFWORD <br/>   | 0x0002 <br/> | Die 32-Bit-Va des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ MIPS \_ JMPADDR <br/>   | 0x0003 <br/> | Die unteren 26 Bits der Va des Ziels. Dies unterstützt die MIPS J- und JAL-Anweisungen. <br/>                                                                                                                                                                                                                                                                                      |
| IMAGE \_ REL \_ MIPS \_ REFHI <br/>     | 0x0004 <br/> | Die hohen 16 Bits der 32-Bit-Va des Ziels. Dies wird für die erste Anweisung in einer Sequenz mit zwei Anweisungen verwendet, die eine vollständige Adresse lädt. Auf diese Verschiebung muss sofort eine PAIR-Verschiebung folgen, deren SymbolTableIndex eine signierte 16-Bit-Verschiebung enthält, die den oberen 16 Bits hinzugefügt wird, die von der Position übernommen werden, die verschoben wird. <br/> |
| IMAGE \_ REL \_ MIPS \_ REFLO <br/>     | 0x0005 <br/> | Die niedrigen 16 Bits der Va des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ REL \_ MIPS \_ GPREL <br/>     | 0x0006 <br/> | Eine 16-Bit-Verschiebung des Ziels mit Vor signed relativ zum GP-Register. <br/>                                                                                                                                                                                                                                                                                                 |
| \_IMAGEREL \_ MIPS \_ LITERAL <br/>   | 0x0007 <br/> | Identisch mit IMAGE \_ REL \_ MIPS \_ GPREL. <br/>                                                                                                                                                                                                                                                                                                                                    |
| \_BILDREL \_ MIPS-ABSCHNITT \_ <br/>   | 0x000A <br/> | Der 16-Bit-Abschnittsindex des Abschnitts enthält das Ziel. Dies wird verwendet, um Debuginformationen zu unterstützen. <br/>                                                                                                                                                                                                                                                             |
| IMAGE \_ REL \_ MIPS \_ SECREL <br/>    | 0x000B <br/> | Der 32-Bit-Offset des Ziels vom Anfang des Abschnitts. Dies wird verwendet, um Debuginformationen und statischen lokalen Threadspeicher zu unterstützen. <br/>                                                                                                                                                                                                                       |
| IMAGE \_ REL \_ MIPS \_ SECRELLO <br/>  | 0x000C <br/> | Die niedrigen 16 Bits des 32-Bit-Offsets des Ziels vom Anfang des Abschnitts. <br/>                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ MIPS \_ SECRELHI <br/>  | 0x000D <br/> | Die hohen 16 Bits des 32-Bit-Offsets des Ziels vom Anfang des Abschnitts. Eine IMAGE \_ REL \_ MIPS \_ PAIR-Verschiebung muss unmittelbar darauf folgen. Der SymbolTableIndex der PAIR-Verschiebung enthält eine signierte 16-Bit-Verschiebung, die den oberen 16 Bits hinzugefügt wird, die von der Position übernommen werden, die verschoben wird. <br/>                            |
| IMAGE \_ REL \_ MIPS \_ JMPADDR16 <br/> | 0x0010 <br/> | Die unteren 26 Bits der Va des Ziels. Dies unterstützt die MIPS16-JAL-Anweisung. <br/>                                                                                                                                                                                                                                                                                           |
| IMAGE \_ REL \_ MIPS \_ REFWORDNB <br/> | 0x0022 <br/> | Die 32-Bit-RVA des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                                |
| \_ \_ BILDREL-MIPS-PAAR \_ <br/>      | 0x0025 <br/> | Die Verschiebung ist nur gültig, wenn sie unmittelbar auf eine REFHI- oder SECRELHI-Verschiebung folgt. Der SymbolTableIndex enthält eine Verschiebung und keinen Index in der Symboltabelle. <br/>                                                                                                                                                                                           |



 

##### <a name="mitsubishi-m32r"></a>Über M32R

Die folgenden Indikatoren für den Verschiebungstyp werden für dieProzessoren Vom Typ "Sprogramm M32R" definiert.



| Konstante                               | Wert              | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ M32R \_ ABSOLUTE <br/> | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| IMAGE \_ REL \_ M32R \_ ADDR32 <br/>   | 0x0001 <br/> | Die 32-Bit-Va des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                                                           |
| IMAGE \_ REL \_ M32R \_ ADDR32NB <br/> | 0x0002 <br/> | Die 32-Bit-RVA des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                                                          |
| IMAGE \_ REL \_ M32R \_ ADDR24 <br/>   | 0x0003 <br/> | Die 24-Bit-Va des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                                                           |
| IMAGE \_ REL \_ M32R \_ GPREL16 <br/>  | 0x0004 <br/> | Der 16-Bit-Offset des Ziels vom GP-Register. <br/>                                                                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ REL \_ M32R \_ PCREL24 <br/>  | 0x0005 <br/> | Der 24-Bit-Offset des Ziels vom Programmzähler (PC), um 2 Bits nach links verschoben und erweitert <br/>                                                                                                                                                                                                                                                                                                |
| IMAGE \_ REL \_ M32R \_ PCREL16 <br/>  | 0x0006 <br/> | Der 16-Bit-Offset des Ziels vom PC, um 2 Bits nach links verschoben und erweitert <br/>                                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ REL \_ M32R \_ PCREL8 <br/>   | 0x0007 <br/> | Der 8-Bit-Offset des Ziels vom PC, um 2 Bits nach links verschoben und erweitert <br/>                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ REL \_ M32R \_ REFHALF <br/>  | 0x0008 <br/> | Die 16 MSBs der Ziel-VA. <br/>                                                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ REL \_ M32R \_ REFHI <br/>    | 0x0009 <br/> | Die 16 MSBs der Ziel-VA, angepasst an die LSB-Signiererweiterung. Dies wird für die erste Anweisung in einer Zweianweisungssequenz verwendet, die eine vollständige 32-Bit-Adresse lädt. Auf diese Verschiebung muss sofort eine PAIR-Verschiebung folgen, deren SymbolTableIndex eine signierte 16-Bit-Verschiebung enthält, die den oberen 16 Bits hinzugefügt wird, die von der Position übernommen werden, die verschoben wird. <br/> |
| IMAGE \_ REL \_ M32R \_ REFLO <br/>    | 0x000A <br/> | Die 16 LSBs der Ziel-VA. <br/>                                                                                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ REL \_ M32R \_ PAIR <br/>     | 0x000B <br/> | Die Verschiebung muss der REFHI-Verschiebung folgen. Der SymbolTableIndex enthält eine Verschiebung und keinen Index in der Symboltabelle. <br/>                                                                                                                                                                                                                                                             |
| ABSCHNITT \_ "IMAGE REL \_ M32R" \_ <br/>  | 0x000C <br/> | Der 16-Bit-Abschnittsindex des Abschnitts, der das Ziel enthält. Dies wird verwendet, um Debuginformationen zu unterstützen. <br/>                                                                                                                                                                                                                                                                                  |
| IMAGE \_ REL \_ M32R \_ SECREL <br/>   | 0x000D <br/> | Der 32-Bit-Offset des Ziels vom Anfang des Abschnitts. Dies wird verwendet, um Debuginformationen und statischen lokalen Threadspeicher zu unterstützen. <br/>                                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ M32R \_ TOKEN <br/>    | 0x000E <br/> | Das CLR-Token. <br/>                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="coff-line-numbers-deprecated"></a>COFF-Zeilennummern (veraltet)

COFF-Zeilennummern werden nicht mehr erstellt und in Zukunft nicht mehr verwendet.

COFF-Zeilennummern geben die Beziehung zwischen Code und Zeilennummern in Quelldateien an. Das Microsoft-Format für COFF-Zeilennummern ähnelt dem COFF-Standardformat, wurde jedoch erweitert, um zu ermöglichen, dass ein einzelner Abschnitt mit Zeilennummern in mehreren Quelldateien in Beziehung steht.

COFF-Zeilennummern bestehen aus einem Array von Datensätzen fester Länge. Der Speicherort (Dateioffset) und die Größe des Arrays werden im Abschnittsheader angegeben. Jeder Zeilennummerdatensatz hat das folgende Format.



| Offset        | Size          | Feld                  | Beschreibung                                                                                                                                                 |
|---------------|---------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Typ ( \* ) <br/>  | Dies ist eine Vereinigung aus zwei Feldern: SymbolTableIndex und VirtualAddress. Ob SymbolTableIndex oder RVA verwendet wird, hängt vom Wert von Linenumber ab. <br/> |
| 4 <br/> | 2 <br/> | Linenumber <br/> | Bei einem Wert ungleich 0 (null) gibt dieses Feld eine einsbasierte Zeilennummer an. Bei 0 (null) wird das Feld Type als Symboltabellenindex für eine Funktion interpretiert. <br/>    |



 

Das Feld Type ist eine Vereinigung aus zwei 4-Byte-Feldern: SymbolTableIndex und VirtualAddress.



| Offset        | Size          | Feld                        | Beschreibung                                                                                                                                                                             |
|---------------|---------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | SymbolTableIndex <br/> | Wird verwendet, wenn Linenumber 0 (null) ist: Index zum Symboltabelleneintrag für eine Funktion. Dieses Format wird verwendet, um die Funktion anzugeben, auf die eine Gruppe von Zeilennummerdatensätzen verweist. <br/>      |
| 0 <br/> | 4 <br/> | VirtualAddress <br/>   | Wird verwendet, wenn Linenumber nicht 0 (null) ist: das RVA des ausführbaren Codes, der der angegebenen Quellzeile entspricht. In einer Objektdatei enthält dies die Va innerhalb des Abschnitts. <br/> |



 

Ein Zeilennummerneintrag kann entweder das Feld Linenumber auf 0 (null) festlegen und auf eine Funktionsdefinition in der Symboltabelle zeigen, oder er kann als Standardeintrag für Zeilennummern verwendet werden, indem eine positive ganze Zahl (Zeilennummer) und die entsprechende Adresse im Objektcode angegeben werden.

Eine Gruppe von Zeilennummereinträgen beginnt immer mit dem ersten Format: dem Index eines Funktionssymbols. Wenn dies der erste Zeilennummerdatensatz im Abschnitt ist, ist dies auch der COMDAT-Symbolname für die Funktion, wenn das COMDAT-Flag des Abschnitts festgelegt ist. Weitere Informationen [finden Sie unter COMDAT-Abschnitte (nur Objekt).](#comdat-sections-object-only) Der Hilfsdatensatz der Funktion in der Symboltabelle verfügt über einen Zeiger auf das Feld Linenumber, das auf denselben Zeilennummerndatensatz zeigt.

Auf einen Datensatz, der eine Funktion identifiziert, folgt eine beliebige Anzahl von Zeilennummerneinträgen, die tatsächliche Zeilennummerninformationen enthalten (d. h. Einträge mit Zeilennummer größer als 0 (null). Diese Einträge sind einsbasierte Einträge relativ zum Anfang der Funktion und stellen jede Quellzeile in der Funktion dar, mit Ausnahme der ersten Zeile.

Beispielsweise würde der erste Zeilennummerndatensatz für das folgende Beispiel die ReverseSign-Funktion angeben (SymbolTableIndex von ReverseSign und Linenumber auf 0 festgelegt). Anschließend folgen Datensätze mit den Linenumber-Werten 1, 2 und 3, die den Quellzeilen wie gezeigt entspricht:


```C++
// some code precedes ReverseSign function
int ReverseSign(int i)
1: {
2:  return -1 * i;
3: }
```



### <a name="coff-symbol-table"></a>COFF-Symboltabelle

Die Symboltabelle in diesem Abschnitt wird vom herkömmlichen COFF-Format geerbt. Sie unterscheiden sich von Microsoft Visual C++ Debuginformationen. Eine Datei kann sowohl eine COFF-Symboltabelle als auch Visual C++ Debuginformationen enthalten, und die beiden werden getrennt gehalten. Einige Microsoft-Tools verwenden die Symboltabelle für eingeschränkte, aber wichtige Zwecke, z. B. die Kommunikation von COMDAT-Informationen mit dem Linker. Abschnitts- und Dateinamen sowie Code- und Datensymbole sind in der Symboltabelle aufgeführt.

Die Position der Symboltabelle wird im COFF-Header angegeben.

Die Symboltabelle ist ein Array von Datensätzen, die jeweils 18 Bytes lang sind. Jeder Datensatz ist entweder ein Standarddatensatz oder ein Hilfsdatensatz für Symboltabellen. Ein Standarddatensatz definiert ein Symbol oder einen Namen und hat das folgende Format.



| Offset         | Size          | Feld                          | Beschreibung                                                                                                                                                                                                                                 |
|----------------|---------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 8 <br/> | Name ( \* ) <br/>          | Der Name des Symbols, dargestellt durch eine Vereinigung von drei -Strukturen. Ein Array von 8 Bytes wird verwendet, wenn der Name nicht mehr als 8 Bytes lang ist. Weitere Informationen finden Sie unter [Symbolnamendarstellung.](https://www.bing.com/search?q=Symbol+Name+Representation) <br/> |
| 8 <br/>  | 4 <br/> | Wert <br/>              | Der Wert, der dem Symbol zugeordnet ist. Die Interpretation dieses Felds hängt von SectionNumber und StorageClass ab. Eine typische Bedeutung ist die umsetzbare Adresse. <br/>                                                         |
| 12 <br/> | 2 <br/> | SectionNumber <br/>      | Die ganze Zahl mit Vorzeichen, die den Abschnitt mit einem 1-basierten Index in der Abschnittstabelle identifiziert. Einige Werte haben eine besondere Bedeutung, wie in Abschnitt 5.4.2, "Section Number Values", definiert. <br/>                                         |
| 14 <br/> | 2 <br/> | Typ <br/>               | Eine Zahl, die den Typ darstellt. Microsoft-Tools legen dieses Feld auf 0x20 (Funktion) oder 0x0 (keine Funktion) fest. Weitere Informationen finden Sie unter [Typdarstellung.](#type-representation) <br/>                                                |
| 16 <br/> | 1 <br/> | StorageClass <br/>       | Ein aufzählter Wert, der die Speicherklasse darstellt. Weitere Informationen finden Sie unter [Storage-Klasse.](#storage-class) <br/>                                                                                                                   |
| 17 <br/> | 1 <br/> | NumberOfAuxSymbols <br/> | Die Anzahl der zusätzlichen Symboltabelleneinträge, die diesem Datensatz folgen. <br/>                                                                                                                                                           |



 

Null oder mehr zusätzliche Symboltabelleneinträge folgen unmittelbar auf jeden Standard-Symboltabellen-Datensatz. In der Regel folgt jedoch nicht mehr als ein zusätzlicher Symboltabelleneintrag einem Standardmäßigen Symboltabellendatensatz (mit Ausnahme von DATEI-Datensätzen mit langen Dateinamen). Jeder zusätzliche Datensatz hat die gleiche Größe wie ein Standard-Symboltabellendatensatz (18 Bytes), aber anstatt ein neues Symbol zu definieren, liefert der Zusätzliche Datensatz zusätzliche Informationen zum letzten definierten Symbol. Die Auswahl, welches von mehreren Formaten verwendet werden soll, hängt vom Feld StorageClass ab. Derzeit definierte Formate für Zusätzliche Symboltabellendatensätze werden in Abschnitt 5.5, "Zusätzliche Symboldatensätze" angezeigt.

Tools, die COFF-Symboltabellen lesen, müssen zusätzliche Symboldatensätze ignorieren, deren Interpretation unbekannt ist. Dadurch kann das Symboltabellenformat erweitert werden, um neue zusätzliche Datensätze hinzuzufügen, ohne vorhandene Tools zu unterbrechen.

#### <a name="symbol-name-representation"></a>Symbolnamendarstellung

Das Feld ShortName in einer Symboltabelle besteht aus 8 Bytes, die den Namen selbst enthalten, wenn er nicht mehr als 8 Bytes lang ist, oder das Feld ShortName gibt einen Offset in die Zeichenfolgentabelle ein. Um zu bestimmen, ob der Name selbst oder ein Offset angegeben ist, testen Sie die ersten 4 Bytes auf Gleichheit bis 0 (null).

Gemäß der Konvention werden die Namen als mit 0 (null) endende UTF-8-codierte Zeichenfolgen behandelt.



| Offset        | Size          | Feld                 | Beschreibung                                                                                                          |
|---------------|---------------|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 8 <br/> | ShortName <br/> | Ein Array von 8 Bytes. Dieses Array wird rechts mit NULL-Zeichen aufgefüllt, wenn der Name kleiner als 8 Bytes ist. <br/> |
| 0 <br/> | 4 <br/> | Nullen <br/>    | Ein Feld, das auf alle Nullen festgelegt ist, wenn der Name länger als 8 Bytes ist. <br/>                                     |
| 4 <br/> | 4 <br/> | Offset <br/>    | Ein Offset in die Zeichenfolgentabelle. <br/>                                                                         |



 

#### <a name="section-number-values"></a>Werte für Abschnittsnummer

Normalerweise ist das Feld Abschnittswert in einem Symboltabelleneintrag ein einsbasierter Index in der Abschnittstabelle. Dieses Feld ist jedoch eine ganze Zahl mit Vorzeichen und kann negative Werte annehmen. Die folgenden Werte( kleiner als 1) haben eine besondere Bedeutung.



| Konstante                          | Wert          | Beschreibung                                                                                                                                                                                                                            |
|-----------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ SYM \_ UNDEFINED <br/> | 0 <br/>  | Dem Symboldatensatz ist noch kein Abschnitt zugewiesen. Der Wert 0 gibt an, dass ein Verweis auf ein externes Symbol an anderer Stelle definiert ist. Ein Wert ungleich 0 (null) ist ein allgemeines Symbol mit einer Größe, die durch den -Wert angegeben wird. <br/> |
| BILD \_ SYM \_ ABSOLUTE <br/>  | –1 <br/> | Das Symbol verfügt über einen absoluten (nicht wiederholbaren) Wert und ist keine Adresse. <br/>                                                                                                                                                  |
| IMAGE \_ SYM \_ DEBUG <br/>     | –2 <br/> | Das Symbol stellt allgemeine Typ- oder Debuginformationen bereit, entspricht jedoch keinem Abschnitt. Microsoft-Tools verwenden diese Einstellung zusammen mit FILE-Datensätzen (Speicherklasse FILE). <br/>                                            |



 

#### <a name="type-representation"></a>Typdarstellung

Das Feld Typ eines Symboltabelleneintrags enthält 2 Bytes, wobei jedes Byte Typinformationen darstellt. Der LSB stellt den einfachen Datentyp (Basisdatentyp) dar, und der MSB stellt ggf. den komplexen Typ dar:



| Msb                                                       | Lsb                                                        |
|-----------------------------------------------------------|------------------------------------------------------------|
| Komplexer Typ: none, pointer, function, array. <br/> | Basistyp: ganze Zahl, Gleitkomma usw. <br/> |



 

Die folgenden Werte werden für den Basistyp definiert, obwohl Microsoft-Tools dieses Feld im Allgemeinen nicht verwenden und LSB auf 0 festlegen. Stattdessen werden Visual C++ Debuginformationen verwendet, um Typen anzugeben. Die möglichen COFF-Werte sind jedoch aus Gründen der Vollständigkeit hier aufgeführt.



| Konstante                             | Wert          | Beschreibung                                                                            |
|--------------------------------------|----------------|----------------------------------------------------------------------------------------|
| BILD \_ SYM \_ TYPE \_ NULL <br/>   | 0 <br/>  | Keine Typinformationen oder unbekannter Basistyp. Microsoft-Tools verwenden diese Einstellung. <br/> |
| IMAGE \_ SYM \_ TYPE \_ VOID <br/>   | 1 <br/>  | Kein gültiger Typ; wird mit void-Zeigern und -Funktionen verwendet <br/>                       |
| IMAGE \_ SYM \_ TYPE \_ CHAR <br/>   | 2 <br/>  | Ein Zeichen (Byte mit Vorzeichen) <br/>                                                  |
| IMAGE \_ SYM \_ TYPE \_ SHORT <br/>  | 3 <br/>  | Eine 2-Byte-Ganzzahl mit Vorzeichen <br/>                                                    |
| IMAGE \_ SYM \_ TYPE \_ INT <br/>    | 4 <br/>  | Ein natürlicher ganzzahliger Typ (normalerweise 4 Bytes in Windows) <br/>                       |
| IMAGE \_ SYM \_ TYPE \_ LONG <br/>   | 5 <br/>  | Eine 4-Byte-Ganzzahl mit Vorzeichen <br/>                                                    |
| IMAGE \_ SYM \_ TYPE \_ FLOAT <br/>  | 6 <br/>  | Eine 4-Byte-Gleitkommazahl <br/>                                             |
| IMAGE \_ SYM \_ TYPE \_ DOUBLE <br/> | 7 <br/>  | Eine 8-Byte-Gleitkommazahl <br/>                                            |
| IMAGE \_ SYM \_ TYPE \_ STRUCT <br/> | 8 <br/>  | Eine -Struktur <br/>                                                                |
| BILD: \_ SYM \_ TYPE \_ UNION <br/>  | 9 <br/>  | Eine Union <br/>                                                                    |
| IMAGE \_ SYM \_ TYPE \_ ENUM <br/>   | 10 <br/> | Ein enumerationsierter Typ <br/>                                                         |
| IMAGE \_ SYM \_ TYPE \_ MOE <br/>    | 11 <br/> | Ein Member der Enumeration (ein bestimmter Wert) <br/>                                 |
| IMAGE \_ SYM \_ TYPE \_ BYTE <br/>   | 12 <br/> | Ein Byte; 1-Byte-Ganzzahl ohne Vorzeichen <br/>                                            |
| \_ \_ BILD: WORT VOM TYP "SYM" \_ <br/>   | 13 <br/> | Ein Wort; 2-Byte-Ganzzahl ohne Vorzeichen <br/>                                            |
| IMAGE \_ SYM \_ TYPE \_ UINT <br/>   | 14 <br/> | Eine ganze Zahl ohne Vorzeichen mit natürlicher Größe (normalerweise 4 Bytes) <br/>                    |
| IMAGE \_ SYM \_ TYPE \_ DWORD <br/>  | 15 <br/> | Eine 4-Byte-Ganzzahl ohne Vorzeichen <br/>                                                 |



 

Das wichtigste Byte gibt an, ob das Symbol ein Zeiger auf, eine Funktion, die zurückgibt, oder ein Array des Basistyps ist, der im LSB angegeben ist. Microsoft-Tools verwenden dieses Feld nur, um anzugeben, ob das Symbol eine Funktion ist, sodass die einzigen beiden resultierenden Werte 0x0 und für das Feld Typ 0x20 werden. Andere Tools können dieses Feld jedoch verwenden, um weitere Informationen zu kommunizieren.

Es ist sehr wichtig, das Funktionsattribut richtig anzugeben. Diese Informationen sind erforderlich, damit inkrementelle Verknüpfungen ordnungsgemäß funktionieren. Bei einigen Architekturen sind die Informationen möglicherweise für andere Zwecke erforderlich.



| Konstante                                | Wert         | Beschreibung                                                          |
|-----------------------------------------|---------------|----------------------------------------------------------------------|
| BILD \_ SYM \_ DTYPE \_ NULL <br/>     | 0 <br/> | Kein abgeleiteter Typ; Das Symbol ist eine einfache Skalarvariable. <br/> |
| \_BILD: \_ SYMBOLISCHER \_ DTYPE-ZEIGER <br/>  | 1 <br/> | Das Symbol ist ein Zeiger auf den Basistyp. <br/>                    |
| IMAGE \_ SYM \_ \_ DTYPE-FUNKTION <br/> | 2 <br/> | Das Symbol ist eine Funktion, die einen Basistyp zurückgibt. <br/>       |
| IMAGE \_ SYM \_ DTYPE \_ ARRAY <br/>    | 3 <br/> | Das Symbol ist ein Array des Basistyps. <br/>                     |



 

#### <a name="storage-class"></a>Speicherklasse

Das Feld StorageClass der Symboltabelle gibt an, welche Art von Definition ein Symbol darstellt. In der folgenden Tabelle sind mögliche Werte aufgeführt. Beachten Sie, dass das Feld StorageClass eine 1-Byte-Ganzzahl ohne Vorzeichen ist. Der Sonderwert -1 sollte daher als entsprechung ohne Vorzeichen 0xFF werden.

Obwohl das herkömmliche COFF-Format viele Speicherklassenwerte verwendet, basieren Microsoft-Tools für die meisten symbolischen Informationen auf Visual C++ Debugformat und verwenden im Allgemeinen nur vier Speicherklassenwerte: EXTERNAL (2), STATIC (3), FUNCTION (101) und FILE (103). Mit Ausnahme der zweiten Spaltenüberschrift unten sollte "Value" als Wertfeld des Symboldatensatzes verwendet werden (dessen Interpretation von der Als Speicherklasse gefundenen Zahl abhängt).



| Konstante                                          | Wert                 | Beschreibung/Interpretation des Felds Wert                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ SYM \_ CLASS \_ END \_ OF \_ FUNCTION <br/>  | -1 (0xFF) <br/> | Ein spezielles Symbol, das das Ende der Funktion zu Debugzwecken darstellt. <br/>                                                                                                                                                                                                                                                  |
| BILD \_ SYM \_ CLASS \_ NULL <br/>               | 0 <br/>         | Keine zugewiesene Speicherklasse. <br/>                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ SYM \_ CLASS \_ AUTOMATIC <br/>          | 1 <br/>         | Die automatische Variable (Stapelvariable). Das Feld Wert gibt den Stapelrahmenoffset an. <br/>                                                                                                                                                                                                                                              |
| IMAGE \_ SYM \_ CLASS \_ EXTERNAL <br/>           | 2 <br/>         | Ein -Wert, den Microsoft-Tools für externe Symbole verwenden. Das Feld Wert gibt die Größe an, wenn die Abschnittsnummer IMAGE \_ SYM \_ UNDEFINED (0) lautet. Wenn die Abschnittsnummer nicht 0 (null) ist, gibt das Feld Wert den Offset innerhalb des Abschnitts an. <br/>                                                                                 |
| IMAGE \_ SYM \_ CLASS \_ STATIC <br/>             | 3 <br/>         | Der Offset des Symbols innerhalb des Abschnitts. Wenn das Feld Wert 0 (null) ist, stellt das Symbol einen Abschnittsnamen dar. <br/>                                                                                                                                                                                                            |
| IMAGE \_ SYM \_ CLASS \_ REGISTER <br/>           | 4 <br/>         | Eine Registervariable. Das Feld Wert gibt die Registernummer an. <br/>                                                                                                                                                                                                                                                            |
| IMAGE \_ SYM \_ CLASS \_ EXTERNAL \_ DEF <br/>      | 5 <br/>         | Ein extern definiertes Symbol. <br/>                                                                                                                                                                                                                                                                                           |
| IMAGE \_ SYM \_ CLASS \_ LABEL <br/>              | 6 <br/>         | Eine Codebezeichnung, die innerhalb des Moduls definiert ist. Das Feld Wert gibt den Offset des Symbols innerhalb des Abschnitts an. <br/>                                                                                                                                                                                                         |
| IMAGE \_ SYM \_ CLASS \_ UNDEFINED \_ LABEL <br/>   | 7 <br/>         | Ein Verweis auf eine Codebezeichnung, die nicht definiert ist. <br/>                                                                                                                                                                                                                                                                               |
| IMAGE \_ SYM \_ CLASS \_ MEMBER \_ OF \_ STRUCT <br/> | 8 <br/>         | Der Strukturmember. Das Feld Wert gibt das n-th-Element an. <br/>                                                                                                                                                                                                                                                               |
| IMAGE \_ SYM \_ CLASS \_ ARGUMENT <br/>           | 9 <br/>         | Ein formales Argument (Parameter) einer Funktion. Das Feld Wert gibt das n-ten Argument an. <br/>                                                                                                                                                                                                                                      |
| IMAGE \_ SYM \_ CLASS \_ STRUCT \_ TAG <br/>        | 10 <br/>        | Der Tagnameneintrag der Struktur. <br/>                                                                                                                                                                                                                                                                                                  |
| IMAGE \_ SYM \_ CLASS \_ MEMBER \_ OF \_ UNION <br/>  | 11 <br/>        | Ein Union-Member. Das Feld Wert gibt das n-th-Element an. <br/>                                                                                                                                                                                                                                                                     |
| IMAGE \_ SYM \_ CLASS \_ UNION \_ TAG <br/>         | 12 <br/>        | Der Union-Tagname-Eintrag. <br/>                                                                                                                                                                                                                                                                                                      |
| TYPDEFINITION \_ \_ DER BILD-SYM-KLASSE \_ \_ <br/>   | 13 <br/>        | Ein Typedef-Eintrag. <br/>                                                                                                                                                                                                                                                                                                               |
| IMAGE \_ SYM \_ CLASS \_ UNDEFINED \_ STATIC <br/>  | 14 <br/>        | Eine statische Datendeklaration. <br/>                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ SYM \_ CLASS \_ ENUM \_ TAG <br/>          | 15 <br/>        | Ein Aufzählungstyp-Tagname-Eintrag. <br/>                                                                                                                                                                                                                                                                                              |
| IMAGE \_ SYM \_ CLASS \_ MEMBER \_ OF \_ ENUM <br/>   | 16 <br/>        | Ein Member einer Enumeration. Das Feld Wert gibt das n-te Element an. <br/>                                                                                                                                                                                                                                                         |
| IMAGE \_ SYM \_ CLASS \_ REGISTER \_ PARAM <br/>    | 17 <br/>        | Ein Registerparameter. <br/>                                                                                                                                                                                                                                                                                                          |
| IMAGE \_ SYM \_ CLASS \_ BIT \_ FIELD <br/>         | 18 <br/>        | Ein Bitfeldverweis. Das Feld Wert gibt das n-te Bit im Bitfeld an. <br/>                                                                                                                                                                                                                                                |
| IMAGE \_ SYM \_ CLASS \_ BLOCK <br/>              | 100 <br/>       | Ein BB-Datensatz (Anfang des Blocks) oder eb (Ende des Blocks). Das Feld Wert ist die umsetzbare Adresse des Codespeicherorts. <br/>                                                                                                                                                                                                      |
| IMAGE \_ \_ SYM-KLASSENFUNKTION \_ <br/>           | 101 <br/>       | Ein Wert, der von Microsoft-Tools für Symboldatensätze verwendet wird, die den Umfang einer Funktion definieren: begin function (.bf), end function ( .ef ) und Zeilen in function ( .lf ). Für LF-Datensätze gibt das Feld Wert die Anzahl der Quellzeilen in der Funktion an. Für EF-Datensätze gibt das Feld Wert die Größe des Funktionscodes an. <br/> |
| IMAGE \_ SYM \_ CLASS \_ END \_ OF \_ STRUCT <br/>    | 102 <br/>       | Ein End-of-Structure-Eintrag. <br/>                                                                                                                                                                                                                                                                                                     |
| IMAGE \_ \_ SYM-KLASSENDATEI \_ <br/>               | 103 <br/>       | Ein Wert, den Microsoft-Tools sowie das herkömmliche COFF-Format für den Quelldatei-Symboldatensatz verwenden. Auf das Symbol folgen zusätzliche Datensätze, die die Datei benennen. <br/>                                                                                                                                                       |
| ABSCHNITT ZUR \_ IMAGE \_ \_ SYM-KLASSE <br/>            | 104 <br/>       | Eine Definition eines Abschnitts (Microsoft-Tools verwenden stattdessen die STATIC-Speicherklasse). <br/>                                                                                                                                                                                                                                                  |
| IMAGE \_ \_ SYM-KLASSE \_ WEAK \_ EXTERNAL <br/>     | 105 <br/>       | Ein schwaches externes . Weitere Informationen finden Sie unter [Auxiliary Format 3: Weak Externals](#auxiliary-format-3-weak-externals). <br/>                                                                                                                                                                                                           |
| IMAGE \_ SYM \_ CLASS \_ CLR \_ TOKEN <br/>         | 107 <br/>       | Ein CLR-Tokensymbol. Der Name ist eine ASCII-Zeichenfolge, die aus dem Hexadezimalwert des Tokens besteht. Weitere Informationen finden Sie unter [CLR-Tokendefinition (nur Objekt).](#clr-token-definition-object-only) <br/>                                                                                                                        |



 

### <a name="auxiliary-symbol-records"></a>Hilfssymboldatensätze

Hilfssymboltabellen-Datensätze folgen immer einigen Standard-Symboltabellen-Datensätzen und gelten für diese. Ein Hilfsdatensatz kann ein beliebiges Format haben, das die Tools erkennen können, aber 18 Bytes müssen für sie zugeordnet werden, damit die Symboltabelle als Array regulärer Größe beibehalten wird. Derzeit erkennen Microsoft-Tools Hilfsformate für die folgenden Arten von Datensätzen: Funktionsdefinitionen, Funktions- und Endsymbole (BF und EF), schwache externe Daten, Dateinamen und Abschnittsdefinitionen.

Der herkömmliche COFF-Entwurf umfasst auch Hilfsdatensatzformate für Arrays und Strukturen. Microsoft-Tools verwenden diese nicht, sondern platzieren diese symbolischen Informationen in Visual C++ Debugformat in den Debugabschnitten.

#### <a name="auxiliary-format-1-function-definitions"></a>Hilfsformat 1: Funktionsdefinitionen

Ein Symboltabellendatensatz markiert den Anfang einer Funktionsdefinition, wenn er über folgende Werte verfügt: eine Speicherklasse von EXTERNAL (2), einen Type-Wert, der angibt, dass es sich um eine Funktion (0x20) handelt, und eine Abschnittsnummer, die größer als 0 (null) ist. Beachten Sie, dass ein Symboltabellendatensatz, der über eine Abschnittsnummer von UNDEFINED (0) verfügt, die Funktion nicht definiert und keinen zusätzlichen Datensatz besitzt. Auf Funktionsdefinitionssymbol-Datensätze folgt ein Hilfsdatensatz im unten beschriebenen Format:



| Offset         | Size          | Feld                             | Beschreibung                                                                                                                                                                                                                   |
|----------------|---------------|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | TagIndex <br/>              | Der Symboltabellenindex des entsprechenden BF-Symboldatensatz (begin function). <br/>                                                                                                                                   |
| 4 <br/>  | 4 <br/> | TotalSize <br/>             | Die Größe des ausführbaren Codes für die Funktion selbst. Wenn sich die Funktion in einem eigenen Abschnitt befindet, ist sizeOfRawData im Abschnittsheader größer oder gleich diesem Feld, je nach Ausrichtungsüberlegungen. <br/> |
| 8 <br/>  | 4 <br/> | PointerToLinenumber <br/>   | Der Dateioffset des ersten COFF-Zeilennummereintrags für die Funktion oder 0 (null), wenn kein Eintrag vorhanden ist. Weitere Informationen finden Sie unter [COFF-Zeilennummern (veraltet).](#coff-line-numbers-deprecated) <br/>                          |
| 12 <br/> | 4 <br/> | PointerToNextFunction <br/> | Der Symboltabellenindex des Datensatzes für die nächste Funktion. Wenn die Funktion die letzte in der Symboltabelle ist, wird dieses Feld auf 0 (null) festgelegt. <br/>                                                                           |
| 16 <br/> | 2 <br/> | Nicht verwendet <br/>                |                                                                                                                                                                                                                               |



 

#### <a name="auxiliary-format-2-bf-and-ef-symbols"></a>Hilfsformat 2: Bf- und EF-Symbole

Für jede Funktionsdefinition in der Symboltabelle beschreiben drei Elemente den Anfang, das Ende und die Anzahl der Zeilen. Jedes dieser Symbole verfügt über die Speicherklasse FUNCTION (101):

Ein Symboldatensatz mit dem Namen .bf (begin-Funktion). Das Feld Wert wird nicht verwendet.

Ein Symboldatensatz mit dem Namen .lf (Zeilen in funktion). Das Feld Wert gibt die Anzahl der Zeilen in der Funktion an.

Ein Symboldatensatz mit dem Namen .ef (Ende der Funktion). Das Feld Wert hat die gleiche Zahl wie das Feld Gesamtgröße im Funktionsdefinitionssymbol-Datensatz.

Auf die Bf- und EF-Symboldatensätze (jedoch nicht auf LF-Datensätze) folgt ein Hilfsdatensatz im folgenden Format:



| Offset         | Size          | Feld                                         | Beschreibung                                                                                                                                                                   |
|----------------|---------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Nicht verwendet <br/>                            |                                                                                                                                                                               |
| 4 <br/>  | 2 <br/> | Linenumber <br/>                        | Die tatsächliche Ordinalzeilennummer (1, 2, 3 und so weiter) in der Quelldatei, die dem BF- oder EF-Datensatz entspricht. <br/>                                               |
| 6 <br/>  | 6 <br/> | Nicht verwendet <br/>                            |                                                                                                                                                                               |
| 12 <br/> | 4 <br/> | PointerToNextFunction (nur BF) <br/> | Der Symboltabellenindex des nächsten BF-Symboldatensatzes. Wenn die Funktion die letzte in der Symboltabelle ist, wird dieses Feld auf 0 (null) festgelegt. Sie wird nicht für EF-Datensätze verwendet. <br/> |
| 16 <br/> | 2 <br/> | Nicht verwendet <br/>                            |                                                                                                                                                                               |



 

#### <a name="auxiliary-format-3-weak-externals"></a>Hilfsformat 3: Schwache externe Daten

"Schwache externe Objekte" sind ein Mechanismus für Objektdateien, der Flexibilität zur Linkzeit ermöglicht. Ein Modul kann ein nicht aufgelöstes externes Symbol (sym1) enthalten, aber es kann auch einen zusätzlichen Datensatz enthalten, der angibt, dass, wenn sym1 zur Linkzeit nicht vorhanden ist, stattdessen ein anderes externes Symbol (sym2) verwendet wird, um Verweise aufzulösen.

Wenn eine Definition von sym1 verknüpft ist, wird ein externer Verweis auf das Symbol normal aufgelöst. Wenn eine Definition von sym1 nicht verknüpft ist, verweisen alle Verweise auf das schwache externe für sym1 stattdessen auf sym2. Das externe Symbol sym2 muss immer verknüpft sein. In der Regel wird sie im Modul definiert, das den schwachen Verweis auf sym1 enthält.

Schwache externe Werte werden durch einen Symboltabellendatensatz mit EXTERNAL-Speicherklasse, UNDEF-Abschnittsnummer und einem Wert von 0 dargestellt. Auf den schwach-externen Symboldatensatz folgt ein Hilfsdatensatz im folgenden Format:



| Offset        | Size           | Feld                       | Beschreibung                                                                                                                                                                                                                                                                                                                                                |
|---------------|----------------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/>  | TagIndex <br/>        | Der Symboltabellenindex von sym2. Das Symbol, das verknüpft werden soll, wenn sym1 nicht gefunden wird. <br/>                                                                                                                                                                                                                                                                  |
| 4 <br/> | 4 <br/>  | Merkmale <br/> | Der Wert IMAGE WEAK EXTERN SEARCH NOLIBRARY gibt an, dass \_ \_ keine \_ \_ Bibliothekssuche nach sym1 durchgeführt werden soll. <br/> Der Wert IMAGE \_ WEAK EXTERN SEARCH LIBRARY gibt \_ \_ \_ an, dass eine Bibliothekssuche nach sym1 durchgeführt werden soll. <br/> Der Wert IMAGE \_ WEAK EXTERN SEARCH ALIAS gibt \_ \_ \_ an, dass sym1 ein Alias für sym2 ist. <br/> |
| 8 <br/> | 10 <br/> | Nicht verwendet <br/>          |                                                                                                                                                                                                                                                                                                                                                            |



 

Beachten Sie, dass das Feld Merkmale nicht in WINNT definiert ist. H; Stattdessen wird das Feld Gesamtgröße verwendet.

#### <a name="auxiliary-format-4-files"></a>Hilfsformat 4: Dateien

Dieses Format folgt einem Symboltabellen-Datensatz mit der Speicherklasse FILE (103). Der Symbolname selbst sollte .file lauten, und der darauf folgende zusätzliche Datensatz gibt den Namen einer Quellcodedatei an.



| Offset        | Size           | Feld                 | Beschreibung                                                                                                                         |
|---------------|----------------|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 18 <br/> | Dateiname <br/> | Eine ANSI-Zeichenfolge, die den Namen der Quelldatei angibt. Dieser wird mit NULL-Werten aufschlossen, wenn er kleiner als die maximale Länge ist. <br/> |



 

#### <a name="auxiliary-format-5-section-definitions"></a>Hilfsformat 5: Abschnittsdefinitionen

Dieses Format folgt einem Symboltabellen-Datensatz, der einen Abschnitt definiert. Ein solcher Datensatz verfügt über einen Symbolnamen, der dem Namen eines Abschnitts (z. B. .text oder .dre analog) und der Speicherklasse STATIC (3) ist. Der Hilfsdatensatz enthält Informationen zu dem Abschnitt, auf den er verweist. Daher werden einige der Informationen im Abschnittsheader dupliziert.



| Offset         | Size          | Feld                           | Beschreibung                                                                                                                                                                                                             |
|----------------|---------------|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Länge <br/>              | Die Größe der Abschnittsdaten; identisch mit SizeOfRawData im Abschnittsheader. <br/>                                                                                                                                  |
| 4 <br/>  | 2 <br/> | NumberOfRelocations <br/> | Die Anzahl der Verschiebungseinträge für den Abschnitt. <br/>                                                                                                                                                           |
| 6 <br/>  | 2 <br/> | NumberOfLinenumbers <br/> | Die Anzahl der Zeilennummereinträge für den Abschnitt. <br/>                                                                                                                                                          |
| 8 <br/>  | 4 <br/> | Prüfsumme <br/>            | Die Prüfsumme für personenbezogene Daten. Dies ist anwendbar, wenn das \_ COMDAT-Flag IMAGE SCN \_ LNK \_ im Abschnittsheader festgelegt ist. Weitere Informationen finden Sie unter [COMDAT-Abschnitte (nur Objekt).](#comdat-sections-object-only) <br/> |
| 12 <br/> | 2 <br/> | Number <br/>              | Ein-basierter Index in der Abschnittstabelle für den zugeordneten Abschnitt. Dies wird verwendet, wenn die COMDAT-Auswahleinstellung 5 ist. <br/>                                                                                     |
| 14 <br/> | 1 <br/> | Auswahl <br/>           | Die COMDAT-Auswahlnummer. Dies gilt, wenn der Abschnitt ein COMDAT-Abschnitt ist. <br/>                                                                                                                         |
| 15 <br/> | 3 <br/> | Nicht verwendet <br/>              |                                                                                                                                                                                                                         |



 

#### <a name="comdat-sections-object-only"></a>COMDAT-Abschnitte (nur Objekt)

Das Feld Auswahl des Zusätzlichen Format der Abschnittsdefinition ist anwendbar, wenn der Abschnitt ein COMDAT-Abschnitt ist. Ein COMDAT-Abschnitt ist ein Abschnitt, der von mehr als einer Objektdatei definiert werden kann. (Das Flag IMAGE \_ SCN \_ LNK \_ COMDAT wird im Abschnittsflagsfeld des Abschnittsheaders festgelegt.) Das Feld Auswahl bestimmt, wie der Linker die verschiedenen Definitionen von COMDAT-Abschnitten auflöset.

Das erste Symbol mit dem Abschnittswert des COMDAT-Abschnitts muss das Abschnittssymbol sein. Dieses Symbol hat den Namen des Abschnitts, das Feld Wert gleich 0 (null), die Abschnittsnummer des zu verwendenden COMDAT-Abschnitts, das Feld Typ gleich IMAGE SYM TYPE NULL, das Feld Klasse gleich IMAGE SYM CLASS STATIC und einen Zusätzlichen \_ \_ \_ \_ \_ \_ Datensatz. Das zweite Symbol wird als "COMDAT-Symbol" bezeichnet und vom Linker in Verbindung mit dem Feld Auswahl verwendet.

Die Werte für das Feld Auswahl sind unten dargestellt.



| Konstante                                        | Wert         | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BILD \_ COMDAT \_ SELECT \_ NODUPLICATES <br/> | 1 <br/> | Wenn dieses Symbol bereits definiert ist, gibt der Linker den Fehler "Multiplizieren definierter Symbole" aus. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| IMAGE \_ COMDAT \_ SELECT \_ ANY <br/>          | 2 <br/> | Jeder Abschnitt, der dasselbe COMDAT-Symbol definiert, kann verknüpft werden. Der Rest wird entfernt. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| IMAGE \_ COMDAT \_ SELECT \_ SAME \_ SIZE <br/>   | 3 <br/> | Der Linker wählt einen beliebigen Abschnitt unter den Definitionen für dieses Symbol aus. Wenn alle Definitionen nicht die gleiche Größe haben, wird ein Fehler mit einem "multiplizieren definierten Symbol" ausgegeben. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| BILD \_ COMDAT \_ SELECT EXACT \_ \_ MATCH <br/> | 4 <br/> | Der Linker wählt einen beliebigen Abschnitt unter den Definitionen für dieses Symbol aus. Wenn alle Definitionen nicht genau übereinstimmen, wird ein Multiplikationsfehler für definierte Symbole ausgegeben. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| BILD \_ COMDAT \_ SELECT \_ ASSOCIATIVE <br/>  | 5 <br/> | Der Abschnitt ist verknüpft, wenn ein bestimmter anderer COMDAT-Abschnitt verknüpft ist. Dieser andere Abschnitt wird durch das Feld Zahl des Hilfssymboldatensatzes für die Abschnittsdefinition angegeben. Diese Einstellung ist nützlich für Definitionen, die Komponenten in mehreren Abschnitten enthalten (z. B. Code in einem und Daten in einem anderen), wobei jedoch alle als Gruppe verknüpft oder verworfen werden müssen. Der andere Abschnitt, dem dieser Abschnitt zugeordnet ist, muss ein COMDAT-Abschnitt sein, der ein weiterer assoziativer COMDAT-Abschnitt sein kann. Die Abschnittsassoziationskette eines assoziativen COMDAT-Abschnitts kann keine Schleife bilden. Die Abschnittsassoziationskette muss schließlich zu einem COMDAT-Abschnitt gelangen, für den IMAGE \_ COMDAT \_ SELECT \_ ASSOCIATIVE nicht festgelegt ist. <br/> |
| IMAGE \_ COMDAT \_ SELECT \_ LARGEST <br/>      | 6 <br/> | Der Linker wählt die größte Definition aus allen Definitionen für dieses Symbol aus. Wenn mehrere Definitionen diese Größe haben, ist die Wahl zwischen ihnen willkürlich. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                |



 

#### <a name="clr-token-definition-object-only"></a>CLR-Tokendefinition (nur Objekt)

Dieses Hilfssymbol folgt in der Regel dem IMAGE \_ SYM \_ CLASS \_ CLR \_ TOKEN. Es wird verwendet, um dem Namespace der COFF-Symboltabelle ein Token zu zuordnen.



| Offset        | Size           | Feld                        | Beschreibung                                                                                |
|---------------|----------------|------------------------------|--------------------------------------------------------------------------------------------|
| 0 <br/> | 1 <br/>  | bAuxType <br/>         | Muss IMAGE \_ AUX \_ SYMBOL TYPE TOKEN DEF \_ \_ \_ (1) sein. <br/>                              |
| 1 <br/> | 1 <br/>  | bReserved <br/>        | Reserviert, muss 0 (null) sein. <br/>                                                        |
| 2 <br/> | 4 <br/>  | SymbolTableIndex <br/> | Der Symbolindex des COFF-Symbols, auf das diese CLR-Tokendefinition verweist. <br/> |
| 6 <br/> | 12 <br/> |                              | Reserviert, muss 0 (null) sein. <br/>                                                        |



 

### <a name="coff-string-table"></a>COFF-Zeichenfolgentabelle

Unmittelbar nach der COFF-Symboltabelle befindet sich die COFF-Zeichenfolgentabelle. Die Position dieser Tabelle wird gefunden, indem die Symboltabellenadresse im COFF-Header verwendet und die Anzahl der Symbole multipliziert mit der Größe eines Symbols hinzugefügt wird.

Am Anfang der COFF-Zeichenfolgentabelle befinden sich 4 Bytes, die die Gesamtgröße (in Bytes) des Rests der Zeichenfolgentabelle enthalten. Diese Größe schließt das Größenfeld selbst ein, sodass der Wert an dieser Position 4 wäre, wenn keine Zeichenfolgen vorhanden wären.

Im Anschluss an die Größe folgen null-terminige Zeichenfolgen, auf die symbole in der COFF-Symboltabelle zeigen.

### <a name="the-attribute-certificate-table-image-only"></a>Attributzertifikattabelle (nur Bild)

Attributzertifikate können einem Image zugeordnet werden, indem eine Attributzertifikattabelle hinzugefügt wird. Die Attributzertifikattabelle besteht aus einem Satz zusammenhängender, quadword-ausgerichteter Attributzertifikateinträge. Zwischen dem ursprünglichen Ende der Datei und dem Anfang der Attributzertifikattabelle wird 0 Auf padding eingefügt, um diese Ausrichtung zu erreichen. Jeder Attributzertifikateintrag enthält die folgenden Felder.



| Offset       | Size                         | Feld                       | Beschreibung                                                                                                |
|--------------|------------------------------|-----------------------------|------------------------------------------------------------------------------------------------------------|
| 0<br/> | 4<br/>                 | dwLength<br/>         | Gibt die Länge des Attributzertifikateintrags an. <br/>                                       |
| 4<br/> | 2<br/>                 | wRevision<br/>        | Enthält die Zertifikatversionsnummer. Weitere Informationen finden Sie im folgenden Text.<br/>                   |
| 6<br/> | 2<br/>                 | wCertificateType<br/> | Gibt den Inhaltstyp in bCertificate an. Weitere Informationen finden Sie im folgenden Text.<br/>             |
| 8<br/> | Finden Sie hier<br/> | bCertificate<br/>     | Enthält ein Zertifikat, z. B. eine Authenticode-Signatur. Weitere Informationen finden Sie im folgenden Text.<br/> |



 

Der virtuelle Adresswert aus dem Eintrag Zertifikattabelle im Optional Header Data Directory ist ein Dateioffset zum ersten Attributzertifikateintrag. Auf nachfolgende Einträge wird zugegriffen, indem die dwLength-Bytes dieses Eintrags, die auf ein 8-Byte-Vielfaches aufgerundet werden, ab dem Anfang des aktuellen Attributzertifikateintrags erhöht werden. Dies wird so lange fortgesetzt, bis die Summe der gerundeten dwLength-Werte dem Size-Wert aus dem Eintrag Certificates Table im Optional Header Data Directory entspricht. Wenn die Summe der gerundeten dwLength-Werte nicht dem Wert Size entspricht, ist entweder die Attributzertifikattabelle oder das Feld Size beschädigt.

Beispiel: Der Zertifikattabelleneintrag des optionalen Headerdatenverzeichnisses enthält Folgendes:


```C++
virtual address = 0x5000
size = 0x1000
```



Das erste Zertifikat beginnt am Offset 0x5000 dem Anfang der Datei auf dem Datenträger. So führen Sie alle Attributzertifikateinträge aus:

1.  Fügen Sie dem Startoffset den dwLength-Wert des ersten Attributzertifikats hinzu.
2.  Rundet den Wert von Schritt 1 auf das nächste 8-Byte-Vielfache, um den Offset des zweiten Attributzertifikateintrags zu finden.
3.  Fügen Sie den Offsetwert aus Schritt 2 dem dwLength-Wert des zweiten Attributzertifikateintrags hinzu, und runden Sie auf das nächste 8-Byte-Vielfache auf, um den Offset des dritten Attributzertifikateintrags zu bestimmen.
4.  Wiederholen Sie Schritt 3 für jedes aufeinander folgende Zertifikat, bis der berechnete Offset 0x6000 (0x5000 Start + 0x1000 Gesamtgröße) entspricht. Dies bedeutet, dass Sie die gesamte Tabelle durchschritten haben.

Alternativ können Sie die Zertifikateinträge aufzählen, indem Sie die **Win32-Funktion ImageEnumerateCertificates** in einer Schleife aufrufen. Einen Link zur Referenzseite der Funktion finden Sie unter [Verweise auf](#references).

Attributzertifikattabelleneinträge können jeden Zertifikattyp enthalten, solange der Eintrag über den richtigen dwLength-Wert, einen eindeutigen wRevision-Wert und einen eindeutigen wCertificateType-Wert verfügt. Der häufigste Typ des Zertifikattabelleneintrags ist eine WIN CERTIFICATE-Struktur, die in Wintrust.h dokumentiert und im weiteren \_ Verlauf dieses Abschnitts erläutert wird.

Die Optionen für das WIN \_ CERTIFICATE **wRevision-Mitglied** umfassen Folgendes (aber nicht beschränkt auf).



| Wert             | Name                                 | Notizen                                                                                                                                                 |
|-------------------|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0100<br/> | WIN \_ CERT \_ REVISION \_ 1 \_ 0<br/> | Version 1, Legacyversion der Win \_ Certificate-Struktur. Es wird nur zum Überprüfen von älteren Authenticode-Signaturen unterstützt.<br/> |
| 0x0200<br/> | WIN \_ CERT \_ REVISION \_ 2 \_ 0<br/> | Version 2 ist die aktuelle Version der Win \_ Certificate-Struktur. <br/>                                                                       |



 

Die Optionen für das WIN \_ CERTIFICATE **wCertificateType-Member** umfassen (aber nicht beschränkt auf) die Elemente in der folgenden Tabelle. Beachten Sie, dass einige Werte derzeit nicht unterstützt werden.



| Wert             | Name                                           | Notizen                                                                                   |
|-------------------|------------------------------------------------|-----------------------------------------------------------------------------------------|
| 0x0001<br/> | WIN \_ \_ CERT-TYP \_ X509 <br/>              | bCertificate enthält ein X.509-Zertifikat <br/> Nicht unterstützt<br/>         |
| 0x0002<br/> | WIN \_ \_ CERT-TYP \_ \_ PKCS-SIGNIERTE \_ DATEN<br/> | bCertificate enthält eine PKCS \# 7 SignedData-Struktur.<br/>                         |
| 0x0003<br/> | WIN \_ \_ CERT-TYP \_ RESERVIERT \_ 1<br/>        | Reserviert <br/>                                                                    |
| 0x0004<br/> | WIN \_ CERT \_ TYPE \_ TS \_ STACK \_ SIGNED<br/>  | Zertifikatsignatur für Terminalserverprotokollstapel <br/> Nicht unterstützt<br/> |



 

Der bCertificate-Member der WIN CERTIFICATE-Struktur enthält ein Bytearray variabler Länge mit dem durch \_ **wCertificateType angegebenen Inhaltstyp.**  Der von Authenticode unterstützte Typ ist WIN \_ CERT \_ TYPE \_ PKCS \_ SIGNED \_ DATA, eine PKCS \# 7 **SignedData-Struktur.** Weitere Informationen zum Format der digitalen Authenticode-Signatur finden Sie unter Windows [Authenticode Portable Executable Signature Format](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/Authenticode_PE.docx).

Wenn **der bCertificate-Inhalt** nicht an einer Quadwordgrenze endet, wird der Attributzertifikateintrag vom Ende von **bCertificate** bis zur nächsten Quadwordgrenze mit Nullen aufschlossen.

Der **dwLength-Wert** ist die Länge der finalisierten WIN \_ CERTIFICATE-Struktur und wird wie die folgenden berechnet:

`dwLength = offsetof(WIN_CERTIFICATE, bCertificate) + (size of the variable-length binary array contained within bCertificate)`

Diese Länge sollte die Größe aller Beläge enthalten, die verwendet werden, um die Anforderung zu erfüllen, dass jede WIN \_ CERTIFICATE-Struktur quadword-ausgerichtet ist:

` dwLength += (8 - (dwLength & 7)) & 7;`

Die **Größe der Zertifikattabelle,** die im Eintrag **Zertifikattabelle** unter [Optional Header Data Directories (Image Only) (Optionale Headerdatenverzeichnisse (nur Bild)) angegeben ist,](#optional-header-data-directories-image-only)enthält die Auf padding.)

Weitere Informationen zur Verwendung der ImageHlp-API zum Aufzählen, Hinzufügen und Entfernen von Zertifikaten aus PE-Dateien finden Sie unter [ImageHlp Functions ( ImageHlp-Funktionen](imagehlp-functions.md)).

#### <a name="certificate-data"></a>Zertifikatdaten

Wie im vorherigen Abschnitt erwähnt, können die Zertifikate in der Attributzertifikattabelle einen beliebigen Zertifikattyp enthalten. Zertifikate, die die Integrität einer PE-Datei sicherstellen, können einen PE-Imagehash enthalten.

Ein PE-Imagehash (oder Dateihash) ähnelt einer Dateiüberprüfungssumme, da der Hashalgorithmus einen Nachrichtenhash erzeugt, der mit der Integrität einer Datei verknüpft ist. Eine Prüfsumme wird jedoch von einem einfachen Algorithmus erstellt und hauptsächlich verwendet, um zu erkennen, ob ein Speicherblock auf dem Datenträger fehlerhaft geworden ist und die dort gespeicherten Werte beschädigt wurden. Ein Dateihash ähnelt einer Prüfsumme, da er auch Dateibeschädigungen erkennt. Im Gegensatz zu den meisten Prüfsummenalgorithmen ist es jedoch sehr schwierig, eine Datei zu ändern, ohne den Dateihash von ihrem ursprünglichen unveränderten Wert zu ändern. Ein Dateihash kann daher verwendet werden, um absichtliche und sogar kleine Änderungen an einer Datei zu erkennen, z. B. solche, die von Viren, Hackern oder programmgesteuerten Antivirusprogrammen eingeführt werden.

Wenn der Image-Digest in einem Zertifikat enthalten ist, muss er bestimmte Felder im PE-Image ausschließen, z. B. den Eintrag Prüfsumme und Zertifikattabelle in Optionale Headerdatenverzeichnisse. Dies liegt daran, dass das Hinzufügen eines Zertifikats diese Felder ändert und dazu führen würde, dass ein anderer Hashwert berechnet wird.

Die Win32 **ImageGetDigestStream-Funktion** stellt einen Datenstrom aus einer PE-Zieldatei für Hashfunktionen zur Verfügung. Dieser Datenstrom bleibt konsistent, wenn Einer PE-Datei Zertifikate hinzugefügt oder daraus entfernt werden. Basierend auf den Parametern, die an **ImageGetDigestStream** übergeben werden, können andere Daten aus dem PE-Image bei der Hashberechnung weggelassen werden. Einen Link zur Referenzseite der Funktion finden Sie unter [Verweise auf](#references).

### <a name="delay-load-import-tables-image-only"></a>Delay-Load Tabellen importieren (nur Image)

Diese Tabellen wurden dem Image hinzugefügt, um einen einheitlichen Mechanismus zu unterstützen, mit dem Anwendungen das Laden einer DLL bis zum ersten Aufruf dieser DLL verzögern können. Das Layout der Tabellen entspricht dem der herkömmlichen Importtabellen, die in Abschnitt 6.4, [The .idata Section , beschrieben werden.](#the-idata-section) Hier werden nur einige Details erläutert.

#### <a name="the-delay-load-directory-table"></a>Die Delay-Load Directory-Tabelle

Die Verzeichnistabelle delay-load ist das Gegenstück zur Importverzeichnistabelle. Sie kann über den Eintrag Deskriptor für verzögerten Import in der Liste optionaler Headerdatenverzeichnisse (Offset 200) abgerufen werden. Die Tabelle ist wie folgt angeordnet:



| Offset         | Size          | Feld                                  | Beschreibung                                                                                                                                                                                                                                                                                                                  |
|----------------|---------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Attribute <br/>                 | Muss Null sein. <br/>                                                                                                                                                                                                                                                                                                    |
| 4 <br/>  | 4 <br/> | Name <br/>                       | Die RVA des Namens der zu ladenden DLL. Der Name befindet sich im schreibgeschützten Datenabschnitt des Images. <br/>                                                                                                                                                                                                        |
| 8 <br/>  | 4 <br/> | Modulhand handle <br/>              | Die RVA des Modulhandls (im Datenabschnitt des Images) der DLL, die verzögert geladen werden soll. Er wird für die Speicherung durch die Routine verwendet, die bereitgestellt wird, um das verzögerte Laden zu verwalten. <br/>                                                                                                                                   |
| 12 <br/> | 4 <br/> | Verzögerte Importadressentabelle <br/> | Das RVA der Importadressentabelle mit verzögerungsbasiertem Ladevorgang. Weitere Informationen finden Sie unter [Delay Import Address Table (IAT)](#delay-import-address-table). <br/>                                                                                                                                                                       |
| 16 <br/> | 4 <br/> | Tabelle "Verzögerter Importname" <br/>    | Die RVA der Namenstabelle für verzögertes Laden, die die Namen der Importe enthält, die möglicherweise geladen werden müssen. Dies entspricht dem Layout der Importnamentabelle. Weitere Informationen finden Sie unter [Hinweis-/Namenstabelle.](#hintname-table)<br/>                                                                                       |
| 20 <br/> | 4 <br/> | Importtabelle mit gebundener Verzögerung <br/>   | Das RVA der gebundenen Adresstabelle für verzögertes Laden, sofern vorhanden. <br/>                                                                                                                                                                                                                                                     |
| 24 <br/> | 4 <br/> | Importtabelle mit Verzögerung beim Entladen <br/>  | Die RVA der Entladungsverzögerungs-Adresstabelle, sofern vorhanden. Dies ist eine genaue Kopie der Tabelle mit den Verzögertimportadressen. Wenn der Aufrufer die DLL entlädt, sollte diese Tabelle über die Verzögerte Importadressentabelle zurückkopiert werden, damit nachfolgende Aufrufe der DLL weiterhin ordnungsgemäß den Länkmechanismus verwenden. <br/> |
| 28 <br/> | 4 <br/> | Zeitstempel <br/>                 | Der Zeitstempel der DLL, an die dieses Image gebunden wurde. <br/>                                                                                                                                                                                                                                                     |



 

Die Tabellen, auf die in dieser Datenstruktur verwiesen wird, sind wie ihre Entsprechungen für herkömmliche Importe organisiert und sortiert. Weitere Informationen finden Sie im [Abschnitt .idata](#the-idata-section).

#### <a name="attributes"></a>Attribute

Es sind noch keine Attributflags definiert. Der Linker legt dieses Feld auf 0 (null) im Bild fest. Dieses Feld kann verwendet werden, um den Datensatz zu erweitern, indem das Vorhandensein neuer Felder angegeben wird, oder es kann verwendet werden, um Verhalten für die Hilfsfunktionen zum Verzögern oder Entladen anzugeben.

#### <a name="name"></a>Name

Der Name der DLL, die verzögert geladen werden soll, befindet sich im Abschnitt mit schreibgeschützten Daten des Images. Auf sie wird über das Feld szName verwiesen.

#### <a name="module-handle"></a>Modulhandle

Das Handle der DLL, die verzögert geladen werden soll, befindet sich im Datenabschnitt des Images. Das Phmod-Feld zeigt auf das Handle. Das angegebene Hilfprogramm für verzögertes Laden verwendet diesen Speicherort, um das Handle in der geladenen DLL zu speichern.

#### <a name="delay-import-address-table"></a>Verzögerte Importadresstabelle

Auf die IAT (Delay Import Address Table) wird vom Deskriptor für den verzögerten Import über das Feld pIAT verwiesen. Das Hilfprogramm für verzögertes Laden aktualisiert diese Zeiger mit den tatsächlichen Einstiegspunkten, sodass sich die Thunks nicht mehr in der aufrufenden Schleife befinden. Auf die Funktionszeiger wird mithilfe des Ausdrucks `pINT->u1.Function` zugegriffen.

#### <a name="delay-import-name-table"></a>Tabelle "Importname verzögern"

Die Tabelle mit verzögerten Importnamen (Delay Import Name Table, INT) enthält die Namen der Importe, die möglicherweise geladen werden müssen. Sie werden auf die gleiche Weise wie die Funktionszeiger im IAT sortiert. Sie bestehen aus den gleichen Strukturen wie der Standard-INT und werden mithilfe des Ausdrucks `pINT->u1.AddressOfData->Name[0]` aufgerufen.

#### <a name="delay-bound-import-address-table-and-time-stamp"></a>Verzögerte gebundene Importadresstabelle und Zeitstempel

Die Verzögerte gebundene Importadresstabelle (DELAY Bound Import Address Table, BIAT) ist eine optionale Tabelle mit IMAGE \_ THUNK \_ DATA-Elementen, die zusammen mit dem Zeitstempelfeld der Verzeichnistabelle für verzögertes Laden durch eine Postprozessbindungsphase verwendet wird.

#### <a name="delay-unload-import-address-table"></a>Verzögertes Entladen der Importadresstabelle

Die UiAT (Delay Unload Import Address Table) ist eine optionale Tabelle mit IMAGE \_ THUNK \_ DATA-Elementen, die der Entladecode verwendet, um eine explizite Entladeanforderung zu verarbeiten. Sie besteht aus initialisierten Daten im schreibgeschützten Abschnitt, bei denen es sich um eine exakte Kopie des ursprünglichen IAT handelt, der den Code auf die Thunks mit verzögerten Ladevorgang verweist. Bei der Entladeanforderung kann die Bibliothek freigegeben, der \* Phmod gelöscht und die UIAT über den IAT geschrieben werden, um den Zustand des Vorabladens wiederherzustellen.

## <a name="special-sections"></a>Spezielle Abschnitte

- [Abschnitt ".debug"](#the-debug-section)
  - [Debugverzeichnis (nur Bild)](#debug-directory-image-only)
  - [Debugtyp](#debug-type)
  - [.debug$F (nur Objekt)](#debugf-object-only)
  - [.debug$S (nur Objekt)](#debugs-object-only)
  - [.debug$P (nur Objekt)](#debugp-object-only)
  - [.debug$T (nur Objekt)](#debugt-object-only)
  - [Linkerunterstützung für Microsoft-Debuginformationen](#linker-support-for-microsoft-debug-information)
- [.drectve-Abschnitt (nur Objekt)](#the-drectve-section-object-only)
- [Abschnitt ".edata" (nur Bild)](#the-edata-section-image-only)
  - [Exportieren einer Verzeichnistabelle](#export-directory-table)
  - [Adresstabelle exportieren](#export-address-table)
  - [Exportieren der Name-Zeigertabelle](#export-name-pointer-table)
  - [Exportieren der Ordnungstabelle](#export-ordinal-table)
  - [Exportieren der Namenstabelle](#export-name-table)
- [Der .idata-Abschnitt](#the-idata-section)
  - [Verzeichnistabelle importieren](#import-directory-table)
  - [Import Lookup Table](#import-lookup-table)
  - [Hinweis-/Namenstabelle](#hintname-table)
  - [Adresstabelle importieren](#delay-import-address-table)
- [Der PDATA-Abschnitt](#the-pdata-section)
- [Der Abschnitt .reloc (nur Bild)](#the-reloc-section-image-only)
  - [Basisverlagerungsblock](#base-relocation-block)
  - [Basisverlagerungstypen](#base-relocation-types)
- [Abschnitt ".tls"](#the-tls-section)
  - [Das TLS-Verzeichnis](#the-tls-directory)
  - [TLS-Rückruffunktionen](#tls-callback-functions)
- [Die Struktur der Auslastungskonfiguration (nur Image)](#the-load-configuration-structure-image-only)
  - [Laden des Konfigurationsverzeichnisses](#load-configuration-directory)
  - [Laden des Konfigurationslayouts](#load-configuration-layout)
- [Abschnitt ".rsrc"](#the-rsrc-section)
  - [Ressourcenverzeichnistabelle](#resource-directory-table)
  - [Ressourcenverzeichniseinträge](#resource-directory-entries)
  - [Ressourcenverzeichniszeichenfolge](#resource-directory-string)
  - [Ressourcendateneintrag](#resource-data-entry)
- [.cormeta-Abschnitt (nur Objekt)](#the-cormeta-section-object-only)
- [Der SXDATA-Abschnitt](#the-sxdata-section)

Typische COFF-Abschnitte enthalten Code oder Daten, die Linker und Microsoft Win32-Ladeprogramm ohne besondere Kenntnisse des Abschnittsinhalts verarbeiten. Der Inhalt ist nur für die Anwendung relevant, die verknüpft oder ausgeführt wird.

Einige COFF-Abschnitte haben jedoch besondere Bedeutungen, wenn sie in Objekt- oder Bilddateien gefunden werden. Tools und Ladeprogramme erkennen diese Abschnitte, da sie spezielle Flags im Abschnittsheader festgelegt haben, weil spezielle Positionen im optionalen Header des Bilds auf sie zeigen oder weil der Abschnittsname selbst eine spezielle Funktion des Abschnitts angibt. (Auch wenn der Abschnittsname selbst keine spezielle Funktion des Abschnitts angibt, wird der Abschnittsname gemäß Konvention vorgegeben, sodass die Autoren dieser Spezifikation in allen Fällen auf einen Abschnittsnamen verweisen können.)

Die reservierten Abschnitte und ihre Attribute werden in der folgenden Tabelle beschrieben, gefolgt von detaillierten Beschreibungen für die Abschnittstypen, die in ausführbaren Dateien beibehalten werden, und die Abschnittstypen, die Metadaten für Erweiterungen enthalten.



| Abschnittsname          | Inhalt                                                                                                                                                                  | Merkmale                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .bss <br/>      | Nicht initialisierte Daten (kostenloses Format) <br/>                                                                                                                             | IMAGE \_ SCN \_ CNT \_ UNINITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ WRITE <br/>                                                                                                                                                                                                                                                                                               |
| .cormeta <br/>  | CLR-Metadaten, die angeben, dass die Objektdatei verwalteten Code enthält <br/>                                                                                       | IMAGE \_ SCN \_ LNK \_ INFO <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| .data <br/>     | Initialisierte Daten (kostenloses Format) <br/>                                                                                                                               | IMAGE \_ SCN \_ CNT \_ \_ INITIALISIERTES \| DATENIMAGE \_ SCN MEM READ IMAGE \_ \_ \| \_ SCN MEM \_ \_ WRITE <br/>                                                                                                                                                                                                                                                                                                 |
| .debug$F <br/>  | Generierte FPO-Debuginformationen (nur Objekt, nur x86-Architektur und jetzt veraltet) <br/>                                                                       | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>                                                                                                                                                                                                                                                                                           |
| .debug$P <br/>  | Vorkompilierte Debugtypen (nur Objekt) <br/>                                                                                                                        | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>                                                                                                                                                                                                                                                                                           |
| .debug$S <br/>  | Debugsymbole (nur Objekt) <br/>                                                                                                                                  | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>                                                                                                                                                                                                                                                                                           |
| .debug$T <br/>  | Debugtypen (nur Objekt) <br/>                                                                                                                                    | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>                                                                                                                                                                                                                                                                                           |
| .drective <br/> | Linkeroptionen <br/>                                                                                                                                               | IMAGE \_ SCN \_ LNK \_ INFO <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| .edata <br/>    | Exportieren von Tabellen <br/>                                                                                                                                                | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                                           |
| .idata <br/>    | Importieren von Tabellen <br/>                                                                                                                                                | IMAGE \_ SCN \_ CNT \_ \_ INITIALISIERTES \| DATENIMAGE \_ SCN MEM READ IMAGE \_ \_ \| \_ SCN MEM \_ \_ WRITE <br/>                                                                                                                                                                                                                                                                                                 |
| .idlsym <br/>   | Schließt registrierte SEH (nur Bild) zur Unterstützung von IDL-Attributen ein. Weitere Informationen finden Sie unter "IDL-Attribute" unter [Verweise](#references) am Ende dieses Themas. <br/> | IMAGE \_ SCN \_ LNK \_ INFO <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| .pdata <br/>    | Ausnahmeinformationen <br/>                                                                                                                                        | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                                           |
| .rdata <br/>    | Schreibgeschützte initialisierte Daten <br/>                                                                                                                                   | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                                           |
| .reloc <br/>    | Bildverlagerungen <br/>                                                                                                                                            | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ \| IMAGE \_ SCN \_ MEM \_ DISCARDABLE <br/>                                                                                                                                                                                                                                                                                           |
| .rsrc <br/>     | Ressourcenverzeichnis <br/>                                                                                                                                           | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                                           |
| SBSS <br/>     | GP-relative nicht initialisierte Daten (freies Format) <br/>                                                                                                                 | IMAGE \_ SCN \_ CNT \_ UNINITIALIZED \_ DATA IMAGE \| \_ SCN MEM READ IMAGE \_ \_ \| \_ SCN MEM WRITE IMAGE \_ \_ \| \_ SCN \_ GPREL Das IMAGE \_ SCN \_ GPREL-Flag sollte nur für IA64-Architekturen festgelegt werden. Dieses Flag ist für andere Architekturen nicht gültig. Das IMAGE \_ \_ SCN-GPREL-Flag gilt nur für Objektdateien. Wenn dieser Abschnittstyp in einer Bilddatei angezeigt wird, darf das IMAGE \_ SCN \_ GPREL-Flag nicht festgelegt werden. <br/> |
| .sdata <br/>    | GP-relative initialisierte Daten (kostenloses Format) <br/>                                                                                                                   | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA IMAGE \| \_ SCN MEM READ \_ IMAGE \_ \| \_ SCN MEM WRITE IMAGE \_ \_ \| \_ SCN \_ GPREL Das IMAGE \_ SCN \_ GPREL-Flag sollte nur für IA64-Architekturen festgelegt werden. Dieses Flag ist für andere Architekturen ungültig. Das IMAGE \_ \_ SCN-GPREL-Flag gilt nur für Objektdateien. Wenn dieser Abschnittstyp in einer Bilddatei angezeigt wird, darf das IMAGE \_ SCN \_ GPREL-Flag nicht festgelegt werden. <br/>   |
| .srdata <br/>   | GP-relative schreibgeschützte Daten (kostenloses Format) <br/>                                                                                                                     | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA IMAGE \| \_ SCN MEM READ \_ IMAGE \_ \| \_ SCN \_ GPREL Das IMAGE \_ SCN \_ GPREL-Flag sollte nur für IA64-Architekturen festgelegt werden. Dieses Flag ist für andere Architekturen nicht gültig. Das IMAGE \_ \_ SCN-GPREL-Flag gilt nur für Objektdateien. Wenn dieser Abschnittstyp in einer Bilddatei angezeigt wird, darf das IMAGE \_ SCN \_ GPREL-Flag nicht festgelegt werden. <br/>                             |
| .sxdata <br/>   | Registrierte Ausnahmehandlerdaten (freies Format und nur x86/Objekt) <br/>                                                                                          | IMAGE \_ SCN \_ LNK \_ INFO Enthält den Symbolindex der einzelnen Ausnahmehandler, auf die der Code in dieser Objektdatei verweist. Das Symbol kann für ein UNDEF-Symbol oder ein Symbol sein, das in diesem Modul definiert ist. <br/>                                                                                                                                                                     |
| .text <br/>     | Ausführbarer Code (kostenloses Format) <br/>                                                                                                                                | IMAGE \_ SCN \_ CNT \_ CODE \| IMAGE \_ SCN \_ MEM \_ EXECUTE \| IIMAGE \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                           |
| TLS <br/>      | Threadlokaler Speicher (nur Objekt) <br/>                                                                                                                           | IMAGE \_ SCN \_ CNT \_ \_ INITIALISIERTES \| DATENIMAGE \_ SCN MEM READ IMAGE \_ \_ \| \_ SCN MEM \_ \_ WRITE <br/>                                                                                                                                                                                                                                                                                                 |
| .tls$ <br/>     | Threadlokaler Speicher (nur Objekt) <br/>                                                                                                                           | IMAGE \_ SCN \_ CNT \_ \_ INITIALISIERTES \| DATENIMAGE \_ SCN MEM READ IMAGE \_ \_ \| \_ SCN MEM \_ \_ WRITE <br/>                                                                                                                                                                                                                                                                                                 |
| .vsdata <br/>   | GP-relative initialisierte Daten (kostenloses Format und nur für ARM-, SH4- und Thumb-Architekturen) <br/>                                                                    | IMAGE \_ SCN \_ CNT \_ \_ INITIALISIERTES \| DATENIMAGE \_ SCN MEM READ IMAGE \_ \_ \| \_ SCN MEM \_ \_ WRITE <br/>                                                                                                                                                                                                                                                                                                 |
| .xdata <br/>    | Ausnahmeinformationen (kostenloses Format) <br/>                                                                                                                          | IMAGE \_ SCN \_ CNT \_ INITIALIZED \_ DATA \| IMAGE \_ SCN \_ MEM \_ READ <br/>                                                                                                                                                                                                                                                                                                                           |



 

Einige der hier aufgeführten Abschnitte sind als "Nur Objekt" oder "Nur Bild" gekennzeichnet, um anzugeben, dass ihre spezielle Semantik nur für Objektdateien bzw. Bilddateien relevant ist. Ein Abschnitt, der als "Nur Bild" markiert ist, wird möglicherweise weiterhin in einer Objektdatei angezeigt, um in die Bilddatei zu gelangen, aber der Abschnitt hat keine besondere Bedeutung für den Linker, sondern nur für das Bilddateiladeprogramm.

### <a name="the-debug-section"></a>Abschnitt ".debug"

Der Abschnitt .debug wird in Objektdateien verwendet, um vom Compiler generierte Debuginformationen zu enthalten, und in Imagedateien, die alle generierten Debuginformationen enthalten. In diesem Abschnitt wird die Paketierung von Debuginformationen in Objekt- und Imagedateien beschrieben.

Im nächsten Abschnitt wird das Format des Debugverzeichnisses beschrieben, das sich an einer beliebigen Stelle im Image befinden kann. In den nachfolgenden Abschnitten werden die "Gruppen" in Objektdateien beschrieben, die Debuginformationen enthalten.

Der Standardwert für den Linker ist, dass Debuginformationen nicht dem Adressraum des Bilds zugeordnet werden. Ein DEBUG-Abschnitt ist nur vorhanden, wenn Debuginformationen im Adressraum zugeordnet werden.

#### <a name="debug-directory-image-only"></a>Debugverzeichnis (nur Bild)

Bilddateien enthalten ein optionales Debugverzeichnis, das angibt, welche Form von Debuginformationen vorhanden ist und wo sie sich befinden. Dieses Verzeichnis besteht aus einem Array von Debugverzeichniseinträgen, deren Speicherort und Größe im optionalen Imageheader angegeben sind.

Das Debugverzeichnis kann sich in einem verwerfbaren DEBUG-Abschnitt befinden (sofern vorhanden), oder es kann in einem anderen Abschnitt in der Imagedatei enthalten sein oder überhaupt nicht in einem Abschnitt enthalten sein.

Jeder Debugverzeichniseintrag identifiziert den Speicherort und die Größe eines Blocks mit Debuginformationen. Die angegebene RVA kann 0 (null) sein, wenn die Debuginformationen nicht durch einen Abschnittsheader abgedeckt werden (d. b. sie befinden sich in der Imagedatei und werden nicht dem Laufzeitadressraum zugeordnet). Wenn es zugeordnet ist, ist das RVA seine Adresse.

Ein Debugverzeichniseintrag hat das folgende Format:



| Offset         | Size          | Feld                        | Beschreibung                                                                                                                                            |
|----------------|---------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Merkmale <br/>  | Reserviert, muss 0 (null) sein. <br/>                                                                                                                    |
| 4 <br/>  | 4 <br/> | TimeDateStamp <br/>    | Die Uhrzeit und das Datum, an dem die Debugdaten erstellt wurden. <br/>                                                                                         |
| 8 <br/>  | 2 <br/> | MajorVersion <br/>     | Die Hauptversionsnummer des Debugdatenformats. <br/>                                                                                         |
| 10 <br/> | 2 <br/> | MinorVersion <br/>     | Die Nebenversionsnummer des Debugdatenformats. <br/>                                                                                         |
| 12 <br/> | 4 <br/> | Typ <br/>             | Das Format der Debuginformationen. Dieses Feld ermöglicht die Unterstützung mehrerer Debugger. Weitere Informationen finden Sie unter [Debugtyp](#debug-type).<br/> |
| 16 <br/> | 4 <br/> | SizeOfData <br/>       | Die Größe der Debugdaten (ohne das Debugverzeichnis selbst). <br/>                                                                     |
| 20 <br/> | 4 <br/> | AddressOfRawData <br/> | Die Adresse der Debugdaten beim Laden relativ zur Imagebasis. <br/>                                                                     |
| 24 <br/> | 4 <br/> | PointerToRawData <br/> | Der Dateizeiger auf die Debugdaten. <br/>                                                                                                        |



 

#### <a name="debug-type"></a>Debugtyp

Die folgenden Werte werden für das Feld Typ des Debugverzeichniseintrags definiert:



| Konstante                                        | Wert          | Beschreibung                                                                                                                                                                                                      |
|-------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ DEBUG \_ TYPE \_ UNKNOWN <br/>         | 0 <br/>  | Ein unbekannter Wert, der von allen Tools ignoriert wird. <br/>                                                                                                                                                       |
| IMAGE \_ DEBUG \_ TYPE \_ COFF <br/>            | 1 <br/>  | Die COFF-Debuginformationen (Zeilennummern, Symboltabelle und Zeichenfolgentabelle). Auf diese Art von Debuginformationen wird auch von Feldern in Dateiheadern verwiesen. <br/>                                          |
| IMAGE \_ DEBUG \_ TYPE \_ CODEVIEW <br/>        | 2 <br/>  | Die Visual C++ Debuginformationen. <br/>                                                                                                                                                                    |
| IMAGE \_ DEBUG \_ TYPE \_ FPO <br/>             | 3 <br/>  | Die Framezeigerauslassungsinformationen (FPO). Diese Informationen informieren den Debugger darüber, wie nicht standardmäßige Stapelrahmen interpretiert werden, die das EBP-Register für einen anderen Zweck als als einen Framezeiger verwenden. <br/> |
| IMAGE \_ DEBUG \_ TYPE \_ MISC <br/>            | 4 <br/>  | Der Speicherort der DBG-Datei. <br/>                                                                                                                                                                            |
| AUSNAHME \_ DES IMAGEDEBUGGINGTYPS \_ \_ <br/>       | 5 <br/>  | Eine Kopie des PDATA-Abschnitts. <br/>                                                                                                                                                                            |
| IMAGE \_ DEBUG \_ TYPE \_ FIXUP <br/>           | 6 <br/>  | Reserviert. <br/>                                                                                                                                                                                            |
| IMAGE \_ DEBUG \_ TYPE \_ OMAP \_ TO \_ SRC <br/>   | 7 <br/>  | Die Zuordnung von einem RVA im Image zu einem RVA im Quellimage. <br/>                                                                                                                                          |
| IMAGE \_ DEBUG \_ TYPE \_ OMAP \_ FROM \_ SRC <br/> | 8 <br/>  | Die Zuordnung von einem RVA im Quellimage zu einem RVA im Image. <br/>                                                                                                                                          |
| IMAGE \_ DEBUG \_ TYPE \_ BORLAND <br/>         | 9 <br/>  | Reserviert für Borland. <br/>                                                                                                                                                                                |
| IMAGE \_ DEBUG \_ TYPE \_ RESERVED10 <br/>      | 10 <br/> | Reserviert. <br/>                                                                                                                                                                                            |
| IMAGE \_ DEBUG \_ TYPE \_ CLSID <br/>           | 11 <br/> | Reserviert. <br/>                                                                                                                                                                                            |
| IMAGE \_ DEBUG \_ TYPE \_ REPRO <br/>           | 16 <br/> | PE-Determinismus oder Reproduzierbarkeit. <br/>                                                                                                                                                                   |
| IMAGE \_ DEBUG \_ TYPE \_ EX \_ DLLCHARACTERISTICS | 20 | Erweiterte DLL-Eigenschaftenbits. |



 

Wenn das Feld Typ auf IMAGE DEBUG TYPE FPO festgelegt ist, handelt es sich bei \_ \_ den \_ Debugrohdaten um ein Array, in dem jeder Member den Stapelrahmen einer Funktion beschreibt. Nicht für jede Funktion in der Imagedatei müssen FPO-Informationen definiert sein, auch wenn der Debugtyp FPO ist. Bei Funktionen ohne FPO-Informationen wird davon ausgegangen, dass sie normale Stapelrahmen aufweisen. Das Format für FPO-Informationen lautet wie folgt:


```C++
#define FRAME_FPO   0               
#define FRAME_TRAP  1
#define FRAME_TSS   2
               
typedef struct _FPO_DATA {
    DWORD       ulOffStart;            // offset 1st byte of function code
    DWORD       cbProcSize;            // # bytes in function
    DWORD       cdwLocals;             // # bytes in locals/4
    WORD        cdwParams;             // # bytes in params/4
    WORD        cbProlog : 8;          // # bytes in prolog
    WORD        cbRegs   : 3;          // # regs saved
    WORD        fHasSEH  : 1;          // TRUE if SEH in func
    WORD        fUseBP   : 1;          // TRUE if EBP has been allocated
    WORD        reserved : 1;          // reserved for future use
    WORD        cbFrame  : 2;          // frame type
} FPO_DATA;
```



Das Vorhandensein eines Eintrags vom Typ IMAGE \_ DEBUG \_ TYPE \_ REPRO gibt an, dass die PE-Datei auf eine Weise erstellt wurde, um Determinismus oder Reproduzierbarkeit zu erreichen. Wenn sich die Eingabe nicht ändert, ist die PE-Ausgabedatei garantiert bit-for-bit-identisch, unabhängig davon, wann oder wo der PE erzeugt wird. Verschiedene Datums-/Zeitstempelfelder in der PE-Datei werden mit teilen oder allen Bits aus einem berechneten Hashwert gefüllt, der PE-Dateiinhalt als Eingabe verwendet und daher nicht mehr das tatsächliche Datum und die tatsächliche Uhrzeit darstellt, zu der eine PE-Datei oder zugehörige spezifische Daten innerhalb des PE erstellt werden. Die Rohdaten dieses Debugeintrags können leer sein oder einen berechneten Hashwert enthalten, dem ein 4-Byte-Wert vorangestellt ist, der die Hashwertlänge darstellt.

Wenn das Feld Typ auf IMAGE \_ DEBUG \_ TYPE EX \_ \_ DLLCHARACTERISTICS festgelegt ist, enthalten die Debugrohdaten erweiterte DLL-Eigenschaftenbits zusätzlich zu den Bits, die im optionalen Header des Images festgelegt werden können. Weitere Informationen finden Sie unter [DLL-Merkmale](#dll-characteristics) im Abschnitt [Optionale Header Windows-Specific Felder (nur Bild).](#optional-header-windows-specific-fields-image-only)

##### <a name="extended-dll-characteristics"></a>Erweiterte DLL-Merkmale

Die folgenden Werte werden für die erweiterten DLL-Eigenschaftenbits definiert.

| Konstante | Wert | Beschreibung |
|-|-|-|
| IMAGE \_ DLLCHARACTERISTICS \_ EX \_ CET \_ COMPAT | 0x0001 | Image ist MIT DEM BILD kompatibel. |

#### <a name="debugf-object-only"></a>.debug$F (nur Objekt)

Die Daten in diesem Abschnitt wurden in Visual C++ Version 7.0 und höher durch einen umfangreicheren Satz von Daten ersetzt, die in einen Unterabschnitt **.debug$S** ausgegeben werden.

Objektdateien können .debug$F-Abschnitte enthalten, deren Inhalt einem oder mehreren FPO \_ DATA-Datensätzen (Framezeigerauslassungsinformationen) entsprechen. Weitere Informationen finden Sie unter "IMAGE \_ DEBUG \_ TYPE FPO" (IMAGE DEBUG TYPE \_ FPO) im [Debugtyp](#debug-type).

Der Linker erkennt diese **.debug$F-Datensätze.** Wenn Debuginformationen generiert werden, sortiert der Linker die \_ FPO-DATENdatensätze nach RVA-Prozedur und generiert einen Debugverzeichniseintrag für sie.

Der Compiler sollte keine FPO-Einträge für Prozeduren mit einem Standardframeformat generieren.

#### <a name="debugs-object-only"></a>.debug$S (nur Objekt)

Dieser Abschnitt enthält Visual C++ Debuginformationen (symbolische Informationen).

#### <a name="debugp-object-only"></a>.debug$P (nur Objekt)

Dieser Abschnitt enthält Visual C++ Debuginformationen (vorkompilierte Informationen). Dies sind gemeinsame Typen für alle Objekte, die mithilfe des vorkompilierten Headers kompiliert wurden, der mit diesem -Objekt generiert wurde.

#### <a name="debugt-object-only"></a>.debug$T (nur Objekt)

Dieser Abschnitt enthält Visual C++ Debuginformationen (Typinformationen).

#### <a name="linker-support-for-microsoft-debug-information"></a>Linkerunterstützung für Microsoft-Debuginformationen

Um Debuginformationen zu unterstützen, hat der Linker Folgendes:

-   Erfasst alle relevanten Debugdaten aus den Abschnitten **.debug$F,** **debug$S,** **.debug$P** und **.debug$T.**

-   Verarbeitet diese Daten zusammen mit den vom Linker generierten Debuginformationen in der PDB-Datei und erstellt einen Debugverzeichniseintrag, um darauf zu verweisen.

### <a name="the-drectve-section-object-only"></a>.drectve-Abschnitt (nur Objekt)

Ein Abschnitt ist ein Direktivenabschnitt, wenn \_ \_ im Abschnittsheader das IMAGE SCN LNK \_ INFO-Flag festgelegt ist und der Name des **DRECTVE-Abschnitts** vorhanden ist. Der Linker entfernt nach der Verarbeitung der Informationen einen **DRECTVE-Abschnitt,** sodass der Abschnitt nicht in der Imagedatei angezeigt wird, die verknüpft wird.

Ein **DRECTVE-Abschnitt** besteht aus einer Textzeichenfolge, die als ANSI oder UTF-8 codiert werden kann. Wenn der UTF-8-Bytereihenfolgemarker (BOM, ein Drei-Byte-Präfix, das aus 0xEF, 0xBB und 0xBF besteht) nicht vorhanden ist, wird die Anweisungszeichenfolge als ANSI interpretiert. Die Direktivenzeichenfolge ist eine Reihe von Linkeroptionen, die durch Leerzeichen getrennt sind. Jede Option enthält einen Bindestrich, den Optionsnamen und ein beliebiges entsprechendes Attribut. Wenn eine Option Leerzeichen enthält, muss die Option in Anführungszeichen eingeschlossen werden. Der **Abschnitt .drectve** darf keine Verschiebungen oder Zeilennummern aufweisen.

### <a name="the-edata-section-image-only"></a>Abschnitt ".edata" (nur Bild)

Der Abschnitt zum Exportieren von Daten mit dem Namen .edata enthält Informationen zu Symbolen, auf die andere Bilder über dynamisches Verknüpfen zugreifen können. Exportierte Symbole befinden sich in der Regel in DLLs, aber DLLs können auch Symbole importieren.

Eine Übersicht über die allgemeine Struktur des Exportabschnitts wird unten beschrieben. Die beschriebenen Tabellen sind in der Datei in der Regel in der angegebenen Reihenfolge zusammenhängend (dies ist jedoch nicht erforderlich). Nur die Exportverzeichnistabelle und die Exportadressentabelle sind erforderlich, um Symbole als Ordinalzahlen zu exportieren. (Eine Ordnungszahl ist ein Export, auf den direkt über den Index der Exportadressentabelle zugegriffen wird.) Die Namenszeigertabelle, die Ordinaltabelle und die Exportnamentabelle sind vorhanden, um die Verwendung von Exportnamen zu unterstützen.



| Tabellenname                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verzeichnistabelle exportieren <br/> | Eine Tabelle mit nur einer Zeile (im Gegensatz zum Debugverzeichnis). Diese Tabelle gibt die Speicherorte und Größen der anderen Exporttabellen an. <br/>                                                                                                                                                                                                               |
| Adresstabelle exportieren <br/>   | Ein Array von RVAs exportierter Symbole. Dies sind die tatsächlichen Adressen der exportierten Funktionen und Daten innerhalb des ausführbaren Codes und der Datenabschnitte. Andere Bilddateien können ein Symbol importieren, indem sie einen Index in diese Tabelle (eine Ordnungszahl) oder optional den öffentlichen Namen verwenden, der der Ordnungszahl entspricht, wenn ein öffentlicher Name definiert ist. <br/> |
| Namenszeigertabelle <br/>     | Ein Array von Zeigern auf die öffentlichen Exportnamen, sortiert in aufsteigender Reihenfolge. <br/>                                                                                                                                                                                                                                                                    |
| Ordinaltabelle <br/>          | Ein Array der Ordinalzahlen, die Membern der Namenszeigertabelle entsprechen. Die Entsprechung ist nach Position; Daher müssen die Namenszeigertabelle und die Ordinaltabelle die gleiche Anzahl von Membern haben. Jede Ordnungszahl ist ein Index in der Exportadressentabelle. <br/>                                                                        |
| Exportieren der Namenstabelle <br/>      | Eine Reihe von ASCII-Zeichenfolgen mit NULL-Terminierung. Elemente der Namenszeigertabelle zeigen auf diesen Bereich. Diese Namen sind die öffentlichen Namen, über die die Symbole importiert und exportiert werden. Sie sind nicht notwendigerweise identisch mit den privaten Namen, die in der Imagedatei verwendet werden. <br/>                                                           |



 

Wenn eine andere Bilddatei ein Symbol nach Namen importiert, durchsucht das Win32-Lader die Namenszeigertabelle nach einer übereinstimmenden Zeichenfolge. Wenn eine übereinstimmende Zeichenfolge gefunden wird, wird die zugeordnete Ordnungszahl identifiziert, indem das entsprechende Member in der Ordnungszahltabelle gesucht wird (d. h. das Member der Ordnungstabelle mit dem gleichen Index wie der Zeichenfolgenzeiger in der Namenszeigertabelle). Die resultierende Ordnungszahl ist ein Index in der Exportadressentabelle, der den tatsächlichen Speicherort des gewünschten Symbols angibt. Auf jedes Exportsymbol kann über eine Ordnungszahl zugegriffen werden.

Wenn eine andere Bilddatei ein Symbol nach Ordnungszahl importiert, ist es nicht erforderlich, in der Namenszeigertabelle nach einer übereinstimmenden Zeichenfolge zu suchen. Die direkte Verwendung einer Ordnungszahl ist daher effizienter. Ein Exportname ist jedoch leichter zu merken und erfordert nicht, dass der Benutzer den Tabellenindex für das Symbol kennt.

#### <a name="export-directory-table"></a>Verzeichnistabelle exportieren

Die Exportsymbolinformationen beginnen mit der Exportverzeichnistabelle, die den Rest der Exportsymbolinformationen beschreibt. Die Exportverzeichnistabelle enthält Adressinformationen, die zum Auflösen von Importen in die Einstiegspunkte in diesem Image verwendet werden.



| Offset         | Size          | Feld                                | Beschreibung                                                                                                                                                               |
|----------------|---------------|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Exportieren von Flags <br/>             | Reserviert, muss 0 sein. <br/>                                                                                                                                          |
| 4 <br/>  | 4 <br/> | Zeit-/Datumsstempel <br/>          | Die Uhrzeit und das Datum, zu denen die Exportdaten erstellt wurden. <br/>                                                                                                           |
| 8 <br/>  | 2 <br/> | Hauptversion <br/>            | Die Hauptversionsnummer. Die Haupt- und Nebenversionsnummern können vom Benutzer festgelegt werden. <br/>                                                                         |
| 10 <br/> | 2 <br/> | Nebenversion <br/>            | Die Nebenversionsnummer. <br/>                                                                                                                                     |
| 12 <br/> | 4 <br/> | Name RVA <br/>                 | Die Adresse der ASCII-Zeichenfolge, die den Namen der DLL enthält. Diese Adresse ist relativ zur Imagebasis. <br/>                                                |
| 16 <br/> | 4 <br/> | Ordinalbasis <br/>             | Die Start ordinalzahl für Exporte in diesem Image. Dieses Feld gibt die Start ordinalzahl für die Exportadressentabelle an. Sie ist in der Regel auf 1 festgelegt. <br/> |
| 20 <br/> | 4 <br/> | Adresstabelleneinträge <br/>    | Die Anzahl der Einträge in der Exportadressentabelle. <br/>                                                                                                            |
| 24 <br/> | 4 <br/> | Anzahl von Namensze0ern <br/>  | Die Anzahl der Einträge in der Namenszeigertabelle. Dies ist auch die Anzahl der Einträge in der Ordnungstabelle. <br/>                                                     |
| 28 <br/> | 4 <br/> | RVA für Die Adresstabelle exportieren <br/> | Die Adresse der Exportadressentabelle relativ zur Imagebasis. <br/>                                                                                          |
| 32 <br/> | 4 <br/> | Namenszeiger-RVA <br/>         | Die Adresse der Exportnamenzeigertabelle relativ zur Imagebasis. Die Tabellengröße wird durch das Feld Number of Name Pointers angegeben. <br/>                       |
| 36 <br/> | 4 <br/> | Ordinaltabellen-RVA <br/>        | Die Adresse der Ordnungszahltabelle relativ zur Imagebasis. <br/>                                                                                                 |



 

#### <a name="export-address-table"></a>Adresstabelle exportieren

Die Exportadressentabelle enthält die Adresse der exportierten Einstiegspunkte und exportierten Daten sowie absolute Werte. Eine Ordnungszahl wird als Index in der Exportadressentabelle verwendet.

Jeder Eintrag in der Exportadressentabelle ist ein Feld, das eines von zwei Formaten in der folgenden Tabelle verwendet. Wenn sich die angegebene Adresse nicht innerhalb des Exportabschnitts befindet (wie durch die Adresse und Länge definiert, die im optionalen Header angegeben sind), ist das Feld ein Export-RVA, bei dem es sich um eine tatsächliche Adresse im Code oder in den Daten handelt. Andernfalls handelt es sich bei dem Feld um eine RVA für die Vorwärtsweiterweiterung, die ein Symbol in einer anderen DLL benennt.



| Offset        | Size          | Feld                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------|---------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Exportieren von RVA <br/>    | Die Adresse des exportierten Symbols, wenn es in den Arbeitsspeicher geladen wird, relativ zur Imagebasis. Beispielsweise die Adresse einer exportierten Funktion. <br/>                                                                                                                                                                                                                                                                                                       |
| 0 <br/> | 4 <br/> | Forwarder RVA <br/> | Der Zeiger auf eine auf NULL beendete ASCII-Zeichenfolge im Exportabschnitt. Diese Zeichenfolge muss innerhalb des Bereichs liegen, der durch den Exporttabellen-Datenverzeichniseintrag angegeben wird. Weitere Informationen [finden Sie unter Optional Header Data Directories (Image Only) (Optionale Headerdatenverzeichnisse (nur Image)).](#optional-header-data-directories-image-only) Diese Zeichenfolge gibt den DLL-Namen und den Namen des Exports (z. B. "MYDLL.expfunc") oder den DLL-Namen und die Ordnungszahl des Exports (z. B. "MYDLL. \# 27"). <br/> |



 

Eine RVA-Forwarder exportiert eine Definition aus einem anderen Image, wodurch sie so ausgesehen wird, als würde sie vom aktuellen Image exportiert. Daher wird das Symbol gleichzeitig importiert und exportiert.

Beispielsweise wird in Kernel32.dll in Windows XP der Export mit dem Namen "HeapAlloc" an die Zeichenfolge "NTDLL. RtlAllocateHeap." Dadurch können Anwendungen die Windows XP-spezifischen Ntdll.dll verwenden, ohne tatsächlich Importverweise darauf zu enthalten. Die Importtabelle der Anwendung bezieht sich nur auf Kernel32.dll. Daher ist die Anwendung nicht spezifisch für Windows XP und kann auf jedem Win32-System ausgeführt werden.

#### <a name="export-name-pointer-table"></a>Exportieren der Namenszeigertabelle

Die Exportnamenzeigertabelle ist ein Array von Adressen (RVAs) in der Exportnamentabelle. Die Zeiger sind jeweils 32 Bits und relativ zur Imagebasis. Die Zeiger werden lexikalisch sortiert, um binäre Suchvorgänge zu ermöglichen.

Ein Exportname wird nur definiert, wenn die Exportnamenzeigertabelle einen Zeiger darauf enthält.

#### <a name="export-ordinal-table"></a>Exportieren der Ordinaltabelle

Die Export ordinal-Tabelle ist ein Array von 16-Bit-Indizes ohne Berücksichtigung der Exportadressentabelle. Ordnungszahlen werden durch das Ordinalbasisfeld der Exportverzeichnistabelle voreingenommen. Anders ausgedrückt: Die Ordnungsbasis muss von den Ordnungszahlen subtrahiert werden, um echte Indizes in die Exportadressentabelle zu erhalten.

Die Exportnamenzeigertabelle und die Export ordinaltabelle bilden zwei parallele Arrays, die getrennt sind, um eine natürliche Feldausrichtung zu ermöglichen. Diese beiden Tabellen werden als eine Tabelle verwendet, in der die Spalte Export Name Pointer auf einen öffentlichen (exportierten) Namen verweist und die Spalte Ordinal exportieren die entsprechende Ordnungszahl für diesen öffentlichen Namen angibt. Ein Member der Exportnamenzeigertabelle und ein Member der Export ordinaltabelle werden zugeordnet, indem in ihren jeweiligen Arrays die gleiche Position (Index) verwendet wird.

Wenn also die Exportnamenzeigertabelle durchsucht wird und eine übereinstimmende Zeichenfolge an Position i gefunden wird, ist der Algorithmus zum Suchen der RVA und der verzerrten Ordnungszahl des Symbols:

```C++
i = Search_ExportNamePointerTable (name);
ordinal = ExportOrdinalTable [i];

rva = ExportAddressTable [ordinal];
biased_ordinal = ordinal + OrdinalBase;
```

Bei der Suche nach einem Symbol nach (verzerrter) Ordnungszahl ist der Algorithmus zum Suchen der RVA und des Namens des Symbols:

```C++
ordinal = biased_ordinal - OrdinalBase;
i = Search_ExportOrdinalTable (ordinal);

rva = ExportAddressTable [ordinal];
name = ExportNameTable [i];
```

#### <a name="export-name-table"></a>Tabelle "Name exportieren"

Die Exportnamentabelle enthält die tatsächlichen Zeichenfolgendaten, auf die von der Exportnamenzeigertabelle verwiesen wurde. Die Zeichenfolgen in dieser Tabelle sind öffentliche Namen, die andere Bilder zum Importieren der Symbole verwenden können. Diese öffentlichen Exportnamen sind nicht unbedingt identisch mit den privaten Symbolnamen, die die Symbole in ihrer eigenen Bilddatei und im Quellcode haben, obwohl dies möglich ist.

Jedes exportierte Symbol verfügt über einen Ordinalwert, bei dem es sich nur um den Index in der Exportadressentabelle handelt. Die Verwendung von Exportnamen ist jedoch optional. Einige, alle oder keine der exportierten Symbole können Exportnamen haben. Bei exportierten Symbolen mit Exportnamen werden die entsprechenden Einträge in der Exportnamenzeigertabelle und der Export ordinaltabelle zusammen verwendet, um jeden Namen einer Ordnungszahl zu zuordnen.

Die Struktur der Exportnamentabelle besteht aus einer Reihe von ASCII-Zeichenfolgen mit NULL-Terminierung variabler Länge.

### <a name="the-idata-section"></a>Der Abschnitt ".idata"

Alle Bilddateien, die Symbole importieren, einschließlich praktisch aller ausführbaren Dateien (EXE), verfügen über einen IDATA-Abschnitt. Es folgt ein typisches Dateilayout für die Importinformationen:

-   Verzeichnistabelle

    NULL-Verzeichniseintrag

-   DLL1 Import Lookup Table

    Null

-   DLL2 Import Lookup Table

    Null

-   DLL3 Import Lookup Table

    Null

-   Hint-Name Tabelle

#### <a name="import-directory-table"></a>Verzeichnistabelle importieren

Die Importinformationen beginnen mit der Importverzeichnistabelle, die den Rest der Importinformationen beschreibt. Die Importverzeichnistabelle enthält Adressinformationen, die verwendet werden, um Fixupverweise auf die Einstiegspunkte in einem DLL-Image aufzulösen. Die Importverzeichnistabelle besteht aus einem Array von Importverzeichniseinträgen, einem Eintrag für jede DLL, auf die das Image verweist. Der letzte Verzeichniseintrag ist leer (mit NULL-Werten gefüllt), was das Ende der Verzeichnistabelle angibt.

Jeder Importverzeichniseintrag hat das folgende Format:



| Offset         | Size          | Feld                                                 | Beschreibung                                                                                                                                                                                 |
|----------------|---------------|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Import Lookup Table RVA (Merkmale) <br/> | Die RVA der Import-Lookuptabelle. Diese Tabelle enthält einen Namen oder eine Ordnungszahl für jeden Import. (Der Name "Characteristics" wird in Winnt.h verwendet, beschreibt dieses Feld jedoch nicht mehr.) <br/> |
| 4 <br/>  | 4 <br/> | Zeit-/Datumsstempel <br/>                           | Der Stempel, der auf 0 (null) festgelegt ist, bis das Bild gebunden ist. Nachdem das Image gebunden wurde, wird dieses Feld auf den Zeit-/Datenstempel der DLL festgelegt. <br/>                                          |
| 8 <br/>  | 4 <br/> | Forwarder Chain <br/>                           | Der Index des ersten Forwarderverweises. <br/>                                                                                                                                     |
| 12 <br/> | 4 <br/> | Name RVA <br/>                                  | Die Adresse einer ASCII-Zeichenfolge, die den Namen der DLL enthält. Diese Adresse ist relativ zur Imagebasis. <br/>                                                                   |
| 16 <br/> | 4 <br/> | RVA für Die Adresstabelle importieren (Thunk-Tabelle) <br/>    | Das RVA der Importadrentabelle. Der Inhalt dieser Tabelle ist mit dem Inhalt der Importsuchetabelle identisch, bis das Bild gebunden ist. <br/>                              |



 

#### <a name="import-lookup-table"></a>Importieren der Nachschlagetabelle

Eine Importsuchetabelle ist ein Array von 32-Bit-Zahlen für PE32 oder ein Array von 64-Bit-Zahlen für PE32+. Jeder Eintrag verwendet das in der folgenden Tabelle beschriebene Bitfeldformat. In diesem Format ist Bit 31 das wichtigste Bit für PE32, und Bit 63 ist das wichtigste Bit für PE32+. Die Auflistung dieser Einträge beschreibt alle Importe aus einer bestimmten DLL. Der letzte Eintrag wird auf null (NULL) festgelegt, um das Ende der Tabelle anzugeben.



| Bit(s)            | Size           | Bitfeld                       | Beschreibung                                                                                                                                                               |
|-------------------|----------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31/63 <br/> | 1 <br/>  | Ordinal-/Namensflag <br/>   | Wenn dieses Bit festgelegt ist, importieren Sie nach Ordnungszahl. Andernfalls importieren Sie nach Namen. Bit wird als 0x80000000 für PE32 maskiert, 0x8000000000000000 für PE32+. <br/>                         |
| 15-0 <br/>  | 16 <br/> | Ordinalzahl <br/>      | Eine 16-Bit-Ordnungszahl. Dieses Feld wird nur verwendet, wenn das Bitfeld Ordinal/Name Flag 1 ist (Import nach Ordnungszahl). Die Bits 30-15 oder 62-15 müssen 0 sein. <br/>                  |
| 30-0 <br/>  | 31 <br/> | RVA für Hinweis-/Namenstabelle <br/> | Ein 31-Bit-RVA eines Hinweis-/Namenstabelleneintrags. Dieses Feld wird nur verwendet, wenn das Bitfeld Ordinal/Name Flag 0 (Import nach Name) ist. Für PE32+-Bits muss 62-31 0 (null) sein. <br/> |



 

#### <a name="hintname-table"></a>Hinweis-/Namenstabelle

Eine Hinweis-/Namenstabelle reicht für den gesamten Importabschnitt aus. Jeder Eintrag in der Hinweis-/Namenstabelle weist das folgende Format auf:



| Offset         | Size                 | Feld            | Beschreibung                                                                                                                                                                                       |
|----------------|----------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/>        | Hinweis <br/> | Ein Index in der Exportnamenzeigertabelle. Zuerst wird eine Übereinstimmung mit diesem Wert versucht. Wenn ein Fehler auftritt, wird eine binäre Suche für die Exportnamenzeigertabelle der DLL ausgeführt. <br/>            |
| 2 <br/>  | -Variable <br/> | Name <br/> | Eine ASCII-Zeichenfolge, die den namen enthält, der importiert werden soll. Dies ist die Zeichenfolge, die mit dem öffentlichen Namen in der DLL abgegleichen werden muss. Bei dieser Zeichenfolge wird die Groß-/Kleinschreibung beachtet und durch ein NULL-Byte beendet. <br/> |
| \* <br/> | 0 oder 1 <br/>   | Pad <br/>  | Ein nachfolgendes Nullpad-Byte, das nach dem nachfolgenden NULL-Byte angezeigt wird, um ggf. den nächsten Eintrag an einer geraden Grenze auszurichten. <br/>                                                        |



 

#### <a name="import-address-table"></a>Adresstabelle importieren

Die Struktur und der Inhalt der Importadresstabelle sind mit denen der Importsuchetabelle identisch, bis die Datei gebunden ist. Während der Bindung werden die Einträge in der Importadresstabelle mit den 32-Bit- (für PE32) oder 64-Bit-Adressen (für PE32+ ) der importierten Symbole überschrieben. Diese Adressen sind die tatsächlichen Speicheradressen der Symbole, obwohl sie technisch gesehen immer noch als "virtuelle Adressen" bezeichnet werden. Das Ladeprogramm verarbeitet in der Regel die Bindung.

### <a name="the-pdata-section"></a>Der PDATA-Abschnitt

Der Abschnitt .pdata enthält ein Array von Funktionstabelleneinträgen, die für die Ausnahmebehandlung verwendet werden. Darauf zeigt der Ausnahmetabelleneintrag im Bilddatenverzeichnis. Die Einträge müssen nach den Funktionsadressen (dem ersten Feld in jeder Struktur) sortiert werden, bevor sie in das endgültige Bild ausgegeben werden. Die Zielplattform bestimmt, welche der drei unten beschriebenen Variationen des Funktionstabelleneintragsformats verwendet wird.

Für 32-Bit-MIPS-Bilder weisen Funktionstabelleneinträge das folgende Format auf:



| Offset         | Size          | Feld                          | Beschreibung                                                                    |
|----------------|---------------|--------------------------------|--------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Startadresse <br/>      | Die VA der entsprechenden Funktion. <br/>                              |
| 4 <br/>  | 4 <br/> | Endadresse <br/>        | Die VA des Endes der Funktion. <br/>                                 |
| 8 <br/>  | 4 <br/> | Ausnahmehandler <br/>  | Der Zeiger auf den Ausnahmehandler, der ausgeführt werden soll. <br/>               |
| 12 <br/> | 4 <br/> | Handlerdaten <br/>       | Der Zeiger auf zusätzliche Informationen, die an den Handler übergeben werden sollen. <br/> |
| 16 <br/> | 4 <br/> | Prolog-Endadresse <br/> | Die VA am Ende des Prologs der Funktion. <br/>                        |



 

Für die Plattformen ARM, PowerPC, SH3 und SH4 Windows CE weisen Funktionstabelleneinträge das folgende Format auf:



| Offset        | Size                | Feld                       | Beschreibung                                                                                                               |
|---------------|---------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/>       | Startadresse <br/>   | Die VA der entsprechenden Funktion. <br/>                                                                         |
| 4 <br/> | 8 Bit <br/>  | Prologlänge <br/>   | Die Anzahl der Anweisungen im Prolog der Funktion. <br/>                                                          |
| 4 <br/> | 22 Bits <br/> | Funktionslänge <br/> | Die Anzahl der Anweisungen in der Funktion. <br/>                                                                   |
| 4 <br/> | 1 Bit <br/>   | 32-Bit-Flag <br/>     | Wenn diese Einstellung festgelegt ist, besteht die Funktion aus 32-Bit-Anweisungen. Wenn dies klar ist, besteht die Funktion aus 16-Bit-Anweisungen. <br/> |
| 4 <br/> | 1 Bit <br/>   | Ausnahmeflag <br/>  | Wenn diese Einstellung festgelegt ist, ist ein Ausnahmehandler für die Funktion vorhanden. Andernfalls ist kein Ausnahmehandler vorhanden. <br/>                 |



 

Für x64- und Itanium-Plattformen weisen Funktionstabelleneinträge das folgende Format auf:



| Offset        | Size          | Feld                          | Beschreibung                                        |
|---------------|---------------|--------------------------------|----------------------------------------------------|
| 0 <br/> | 4 <br/> | Begin Address <br/>      | Das RVA der entsprechenden Funktion. <br/> |
| 4 <br/> | 4 <br/> | Endadresse <br/>        | Das RVA am Ende der Funktion. <br/>    |
| 8 <br/> | 4 <br/> | Entladungsinformationen <br/> | Das RVA der Entladungsinformationen. <br/>     |



 

### <a name="the-reloc-section-image-only"></a>Abschnitt ".reloc" (nur Bild)

Die Basisverlagerungstabelle enthält Einträge für alle Basisverlagerungen im Image. Das Feld Basisverlagerungstabelle in den optionalen Headerdatenverzeichnissen gibt die Anzahl von Bytes in der Basisverlagerungstabelle an. Weitere Informationen finden Sie unter [Optionale Headerdatenverzeichnisse (nur Image).](#optional-header-data-directories-image-only) Die Basisverlagerungstabelle ist in Blöcke unterteilt. Jeder Block stellt die Basisverlagerungen für eine 4K-Seite dar. Jeder Block muss an einer 32-Bit-Grenze beginnen.

Das Lader ist nicht erforderlich, um Basisverlagerungen zu verarbeiten, die vom Linker aufgelöst werden, es sei denn, das Ladeimage kann nicht auf der Imagebasis geladen werden, die im PE-Header angegeben ist.

#### <a name="base-relocation-block"></a>Basisverlagerungsblock

Jeder Basisverlagerungsblock beginnt mit der folgenden Struktur:



| Offset        | Size          | Feld                  | Beschreibung                                                                                                                                              |
|---------------|---------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Seiten-RVA <br/>   | Die Imagebasis plus die Seiten-RVA wird jedem Offset hinzugefügt, um die Va zu erstellen, auf die die Basisverlagerung angewendet werden muss. <br/>                         |
| 4 <br/> | 4 <br/> | Blockgröße <br/> | Die Gesamtzahl der Bytes im Basisverlagerungsblock, einschließlich der Felder Seiten-RVA und Blockgröße und der folgenden Felder vom Typ/Offset. <br/> |



 

Auf das Feld Blockgröße folgt dann eine beliebige Anzahl von Typ- oder Offsetfeldeinträgen. Jeder Eintrag ist ein WORD -Eintrag (2 Bytes) und hat die folgende Struktur:



| Offset        | Size                | Feld              | Beschreibung                                                                                                                                                                                                            |
|---------------|---------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 Bits <br/>  | Typ <br/>   | Wird in den hohen 4 Bits des WORD gespeichert, ein Wert, der den Typ der zu verwendenden Basisverlagerung angibt. Weitere Informationen finden Sie unter [Basisverlagerungstypen.](#base-relocation-types)<br/>                         |
| 0 <br/> | 12 Bits <br/> | Offset <br/> | Wird in den verbleibenden 12 Bits von WORD gespeichert, ein Offset von der Startadresse, die im Feld Seiten-RVA für den Block angegeben wurde. Dieser Offset gibt an, wo die Basisverlagerung angewendet werden soll. <br/> |



 

Um eine Basisverlagerung anzuwenden, wird die Differenz zwischen der bevorzugten Basisadresse und der Basis berechnet, in der das Image tatsächlich geladen wird. Wenn das Image an seiner bevorzugten Basis geladen wird, beträgt die Differenz 0 (null), und daher müssen die Basisverlagerungen nicht angewendet werden.

#### <a name="base-relocation-types"></a>Basisverlagerungstypen



| Konstante                                       | Wert          | Beschreibung                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IMAGE \_ REL \_ BASED \_ ABSOLUTE <br/>        | 0 <br/>  | Die Basisverlagerung wird übersprungen. Dieser Typ kann verwendet werden, um einen Block zu aufpaddnen. <br/>                                                                                                                                                                                                                                                 |
| IMAGE \_ REL \_ BASED \_ HIGH <br/>            | 1 <br/>  | Die Basisverlagerung fügt dem 16-Bit-Feld am Offset die hohen 16 Bits der Differenz hinzu. Das 16-Bit-Feld stellt den hohen Wert eines 32-Bit-Worts dar. <br/>                                                                                                                                                               |
| IMAGE \_ REL \_ BASED \_ LOW <br/>             | 2 <br/>  | Die Basisverlagerung fügt dem 16-Bit-Feld am Offset die unteren 16 Bits der Differenz hinzu. Das 16-Bit-Feld stellt die untere Hälfte eines 32-Bit-Worts dar. <br/>                                                                                                                                                                  |
| IMAGE \_ \_ REL-BASIERTES \_ HIGHLOW <br/>         | 3 <br/>  | Die Basisverlagerung wendet alle 32 Bits der Differenz auf das 32-Bit-Feld am Offset an. <br/>                                                                                                                                                                                                                              |
| IMAGE \_ \_ REL-BASIERTES \_ HIGHADJ <br/>         | 4 <br/>  | Die Basisverlagerung fügt dem 16-Bit-Feld am Offset die hohen 16 Bits der Differenz hinzu. Das 16-Bit-Feld stellt den hohen Wert eines 32-Bit-Worts dar. Die unteren 16 Bits des 32-Bit-Werts werden im 16-Bit-Wort gespeichert, das dieser Basisverlagerung folgt. Dies bedeutet, dass diese Basisverlagerung zwei Slots belegt. <br/> |
| IMAGE \_ \_ REL-BASIERTE \_ MIPS \_ JMPADDR <br/>   | 5 <br/>  | Die Interpretation der Verschiebung hängt vom Computertyp ab. <br/> Wenn der Computertyp MIPS ist, gilt die Basisverlagerung für eine MIPS-Sprunganweisung. <br/>                                                                                                                                                    |
| IMAGE \_ \_ REL-BASIERTES \_ ARM \_ MOV32 <br/>      | 5 <br/>  | Diese Verschiebung ist nur sinnvoll, wenn der Computertyp ARM oder Thumb ist. Die Basisverlagerung wendet die 32-Bit-Adresse eines Symbols auf ein aufeinander folgendes MOVW/MOVT-Anweisungspaar an. <br/>                                                                                                                                 |
| IMAGE \_ \_ REL-BASIERTES \_ RISCV \_ HIGH20 <br/>   | 5 <br/>  | Diese Verschiebung ist nur sinnvoll, wenn der Computertyp RISC-V ist. Die Basisverlagerung gilt für die hohen 20 Bits einer absoluten 32-Bit-Adresse. <br/>                                                                                                                                                                     |
|                                                | 6 <br/>  | Reserviert, muss 0 (null) sein. <br/>                                                                                                                                                                                                                                                                                               |
| IMAGE \_ \_ REL-BASIERTER \_ THUMB \_ MOV32 <br/>    | 7 <br/>  | Diese Verschiebung ist nur sinnvoll, wenn der Computertyp Thumb ist. Die Basisverlagerung wendet die 32-Bit-Adresse eines Symbols auf ein aufeinander folgendes MOVW/MOVT-Anweisungspaar an. <br/>                                                                                                                                            |
| IMAGE \_ \_ REL-BASIERTER \_ RISCV \_ LOW12I <br/>   | 7 <br/>  | Diese Verschiebung ist nur sinnvoll, wenn der Computertyp RISC-V ist. Die Basisverlagerung gilt für die unteren 12 Bits einer absoluten 32-Bit-Adresse, die im RISC-V-I-Typanweisungsformat gebildet wird. <br/>                                                                                                                           |
| IMAGE \_ \_ REL-BASIERTER \_ RISCV \_ LOW12S <br/>   | 8 <br/>  | Diese Verschiebung ist nur sinnvoll, wenn der Computertyp RISC-V ist. Die Basisverlagerung gilt für die niedrigen 12 Bits einer absoluten 32-Bit-Adresse, die im RISC-V-S-Typanweisungsformat formatiert ist. <br/>                                                                                                                           |
| \_ \_ IMAGEREL-BASIERTE \_ MIPS \_ JMPADDR16 <br/> | 9 <br/>  | Die Verschiebung ist nur sinnvoll, wenn der Computertyp MIPS ist. Die Basisverlagerung gilt für eine MIPS16-Sprunganweisung. <br/>                                                                                                                                                                                            |
| IMAGE \_ REL \_ BASED \_ DIR64 <br/>           | 10 <br/> | Die Basisverschiebung wendet die Differenz auf das 64-Bit-Feld beim Offset an. <br/>                                                                                                                                                                                                                                             |



 

### <a name="the-tls-section"></a>Abschnitt ".tls"

Der Abschnitt .tls bietet direkte PE- und COFF-Unterstützung für statischen lokalen Threadspeicher (TLS). TLS ist eine spezielle Speicherklasse, die Windows unterstützt, bei der ein Datenobjekt keine automatische (Stapel-)Variable ist, aber lokal für jeden einzelnen Thread ist, der den Code ausführt. Daher kann jeder Thread einen anderen Wert für eine Variable beibehalten, die mit TLS deklariert wird.

Beachten Sie, dass jede Menge an TLS-Daten unterstützt werden kann, indem die API TlsAlloc, TlsFree, TlsSetValue und TlsGetValue aufruft. Die PE- oder COFF-Implementierung ist ein alternativer Ansatz zur Verwendung der API und hat den Vorteil, dass sie aus Sicht des Programmierers auf hoher Ebene einfacher ist. Diese Implementierung ermöglicht es, TLS-Daten ähnlich wie gewöhnliche statische Variablen in einem Programm zu definieren und zu initialisieren. Beispielsweise kann in Visual C++ eine statische TLS-Variable wie folgt definiert werden, ohne die Windows-API zu verwenden:

`__declspec (thread) int tlsFlag = 1;`

Zur Unterstützung dieses Programmierkonstrukts gibt der Abschnitt PE und COFF .tls die folgenden Informationen an: Initialisierungsdaten, Rückrufroutinen für die Threadinitialisierung und -beendigung und den TLS-Index, die in der folgenden Erläuterung erläutert werden.

> [!Note]
>
> Statisch deklarierte TLS-Datenobjekte können nur in statisch geladenen Bilddateien verwendet werden. Dies macht es unzuverlässig, statische TLS-Daten in einer DLL zu verwenden, es sei denn, Sie wissen, dass die DLL oder statisch verknüpfte Daten nie dynamisch mit der LoadLibrary-API-Funktion geladen werden.

 

Ausführbarer Code greift mithilfe der folgenden Schritte auf ein statisches TLS-Datenobjekt zu:

1.  Zur Linkzeit legt der Linker das Feld Adresse des Indexes des TLS-Verzeichnisses fest. Dieses Feld verweist auf einen Speicherort, an dem das Programm erwartet, dass der TLS-Index empfangen wird.

    Die Microsoft-Laufzeitbibliothek erleichtert diesen Prozess, indem sie ein Speicherimage des TLS-Verzeichnisses definiert und ihm den speziellen Namen \_ \_ "tls \_ used" (Intel x86-Plattformen) oder \_ "tls \_ used" (andere Plattformen) gibt. Der Linker sucht nach diesem Speicherimage und verwendet die Daten dort, um das TLS-Verzeichnis zu erstellen. Andere Compiler, die TLS unterstützen und mit dem Microsoft-Linker arbeiten, müssen das gleiche Verfahren verwenden.

2.  Wenn ein Thread erstellt wird, kommuniziert das Ladeprogramm die Adresse des TLS-Arrays des Threads, indem die Adresse des Threadumgebungsblocks (TEB) im FS-Register platziert wird. Ein Zeiger auf das TLS-Array befindet sich am Offset 0x2C vom Anfang von TEB. Dieses Verhalten ist Intel x86-spezifisch.

3.  Das Ladeprogramm weist den Wert des TLS-Indexes der Stelle zu, die im Feld Adresse des Indexes angegeben wurde.

4.  Der ausführbare Code ruft den TLS-Index und auch den Speicherort des TLS-Arrays ab.

5.  Der Code verwendet den TLS-Index und die TLS-Arrayposition (Multiplizieren des Indexes mit 4 und Verwenden dieses Indexes als Offset zum Array), um die Adresse des TLS-Datenbereichs für das angegebene Programm und Modul abzurufen. Jeder Thread verfügt über einen eigenen TLS-Datenbereich, aber dies ist für das Programm transparent, das nicht wissen muss, wie Daten einzelnen Threads zugeordnet werden.

6.  Auf ein einzelnes TLS-Datenobjekt wird als fester Offset im TLS-Datenbereich zugegriffen.

Das TLS-Array ist ein Array von Adressen, das das System für jeden Thread verwaltet. Jede Adresse in diesem Array gibt den Speicherort der TLS-Daten für ein bestimmtes Modul (EXE oder DLL) innerhalb des Programms an. Der TLS-Index gibt an, welcher Member des Arrays verwendet werden soll. Der Index ist eine Zahl (nur für das System aussagekräftig), die das Modul identifiziert.

#### <a name="the-tls-directory"></a>Das TLS-Verzeichnis

Das TLS-Verzeichnis hat das folgende Format:



| Offset (PE32/PE32+) | Größe (PE32/PE32+) | Feld                            | Beschreibung                                                                                                                                                                                                                                                                                                                                         |
|----------------------|--------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>        | 4/8 <br/>    | Rohdatenstart-VA <br/>    | Die Startadresse der TLS-Vorlage. Die Vorlage ist ein Datenblock, der zum Initialisieren von TLS-Daten verwendet wird. Das System kopiert alle diese Daten jedes Mal, wenn ein Thread erstellt wird, sodass sie nicht beschädigt werden dürfen. Beachten Sie, dass diese Adresse kein RVA ist. Es handelt sich um eine Adresse, für die im Abschnitt .reloc eine Basisverlagerung erfolgen soll. <br/> |
| 4/8 <br/>      | 4/8 <br/>    | Rohdaten–End-VA <br/>      | Die Adresse des letzten Byte des TLS, mit Ausnahme der 0(null) Füllung. Wie beim Feld Raw Data Start VA ist dies eine VA, keine RVA. <br/>                                                                                                                                                                                                       |
| 8/16 <br/>     | 4/8 <br/>    | Adresse des Indexes <br/>     | Der Speicherort, an den der TLS-Index empfangen werden soll, den das Ladeprogramm zuweist. Dieser Speicherort befindet sich in einem normalen Datenabschnitt, sodass ihm ein symbolischer Name gegeben werden kann, auf den das Programm zugreifen kann. <br/>                                                                                                                                                    |
| 12/24 <br/>    | 4/8 <br/>    | Adresse von Rückrufen <br/> | Der Zeiger auf ein Array von TLS-Rückruffunktionen. Das Array ist NULL-terminiert. Wenn also keine Rückruffunktion unterstützt wird, zeigt dieses Feld auf 4 Bytes, die auf 0 festgelegt sind. Informationen zum Prototyp für diese Funktionen finden Sie unter [TLS-Rückruffunktionen.](#tls-callback-functions)<br/>                                                      |
| 16/32 <br/>    | 4 <br/>      | Größe von 0 (null) Füllung <br/>    | Die Größe der Vorlage in Bytes, die über die initialisierten Daten hinausgeht, die durch die Felder Rohdatenstart-VA und Rohdaten-End-VA getrennt sind. Die Gesamtgröße der Vorlage sollte mit der Gesamtgröße der TLS-Daten in der Imagedatei übereinstimmen. Die 0 (null) Füllung ist die Datenmenge, die nach den initialisierten Daten ungleich 0 (null) eingeht. <br/>                            |
| 20/36 <br/>    | 4 <br/>      | Merkmale <br/>      | Die vier Bits \[ 23:20 \] beschreiben Ausrichtungsinformationen. Mögliche Werte sind die als IMAGE SCN ALIGN definierten \_ \_ \_ \* Werte, die auch verwendet werden, um die Ausrichtung des Abschnitts in Objektdateien zu beschreiben. Die anderen 28 Bits sind für die zukünftige Verwendung reserviert. <br/>                                                                                                       |



 

#### <a name="tls-callback-functions"></a>TLS-Rückruffunktionen

Das Programm kann eine oder mehrere TLS-Rückruffunktionen bereitstellen, um zusätzliche Initialisierung und Beendigung für TLS-Datenobjekte zu unterstützen. Eine typische Verwendung für eine solche Rückruffunktion wäre das Aufrufen von Konstruktoren und Destruktoren für Objekte.

Obwohl in der Regel nicht mehr als eine Rückruffunktion vorhanden ist, wird ein Rückruf als Array implementiert, damit bei Bedarf zusätzliche Rückruffunktionen hinzugefügt werden können. Wenn mehrere Rückruffunktionen vorhanden sind, wird jede Funktion in der Reihenfolge aufgerufen, in der ihre Adresse im Array angezeigt wird. Ein NULL-Zeiger beendet das Array. Es ist durchaus gültig, eine leere Liste zu verwenden (kein Rückruf wird unterstützt). In diesem Fall weist das Rückrufarray genau einen Member auf– einen NULL-Zeiger.

Der Prototyp für eine Rückruffunktion (auf die ein Zeiger vom Typ PIMAGE \_ TLS \_ CALLBACK zeigt) verfügt über die gleichen Parameter wie eine DLL-Einstiegspunktfunktion:


```C++
typedef VOID
(NTAPI *PIMAGE_TLS_CALLBACK) (
    PVOID DllHandle,
    DWORD Reason,
    PVOID Reserved
    );
```



Der Reserved-Parameter sollte auf 0 (null) festgelegt werden. Der Reason-Parameter kann die folgenden Werte annehmen:



| Einstellung                          | Wert         | Beschreibung                                                                                          |
|----------------------------------|---------------|------------------------------------------------------------------------------------------------------|
| DLL \_ PROCESS \_ ATTACH <br/> | 1 <br/> | Ein neuer Prozess wurde gestartet, einschließlich des ersten Threads. <br/>                                   |
| DLL \_ THREAD \_ ATTACH <br/>  | 2 <br/> | Ein neuer Thread wurde erstellt. Diese Benachrichtigung wurde für alle bis auf den ersten Thread gesendet. <br/>      |
| DLL \_ THREAD \_ DETACH <br/>  | 3 <br/> | Ein Thread wird gerade beendet. Diese Benachrichtigung wurde für alle bis auf den ersten Thread gesendet. <br/> |
| \_ \_ DLL-PROZESSTRENNUNG <br/> | 0 <br/> | Ein Prozess wird beendet, einschließlich des ursprünglichen Threads. <br/>                          |



 

### <a name="the-load-configuration-structure-image-only"></a>Die Struktur der Auslastungskonfiguration (nur Image)

Die Auslastungskonfigurationsstruktur (IMAGE \_ LOAD \_ CONFIG \_ DIRECTORY) wurde früher in sehr begrenzten Fällen im Windows NT-Betriebssystem selbst verwendet, um verschiedene Features zu schwierig oder zu groß zu beschreiben, um sie im Dateiheader oder optionalen Header des Images zu beschreiben. Aktuelle Versionen des Microsoft-Linkers und Windows XP und neuere Versionen von Windows eine neue Version dieser Struktur für x86-basierte 32-Bit-Systeme verwenden, die reservierte SEH-Technologie enthalten. Dies stellt eine Liste der sicheren strukturierten Ausnahmehandler bereit, die das Betriebssystem während der Ausnahmeverteilung verwendet. Wenn sich die Handleradresse im VA-Bereich eines Bilds befindet und als reserviert seh-aware markiert ist (d. h., IMAGE \_ DLLCHARACTERISTICS \_ NO SEH ist im Feld \_ DllCharacteristics des optionalen Headers wie zuvor beschrieben klar), muss sich der Handler in der Liste der bekannten sicheren Handler für dieses Image befinden. Andernfalls beendet das Betriebssystem die Anwendung. Dies hilft, den Exploit "x86 exception handler hijacking" zu verhindern, der in der Vergangenheit verwendet wurde, um die Kontrolle über das Betriebssystem zu übernehmen.

Der Microsoft-Linker stellt automatisch eine Standardstruktur für die Auslastungskonfiguration bereit, um die reservierten SEH-Daten einzubeziehen. Wenn der Benutzercode bereits eine Auslastungskonfigurationsstruktur bereitstellt, muss er die neuen reservierten SEH-Felder enthalten. Andernfalls kann der Linker die reservierten SEH-Daten nicht einschließen, und das Bild ist nicht als enthaltende reservierte SEH gekennzeichnet.

#### <a name="load-configuration-directory"></a>Laden des Konfigurationsverzeichnisses

Der Datenverzeichniseintrag für eine vorab reservierte SEH-Ladekonfigurationsstruktur muss eine bestimmte Größe der Ladekonfigurationsstruktur angeben, da das Betriebssystemladeprogramm immer erwartet, dass es sich um einen bestimmten Wert handeln soll. In diesem Zusammenhang ist die Größe eigentlich nur eine Versionsprüfung. Für die Kompatibilität mit Windows XP und früheren Versionen von Windows muss die Größe für x86-Images 64 sein.

#### <a name="load-configuration-layout"></a>Laden des Konfigurationslayouts

Die Struktur der Ladekonfiguration weist das folgende Layout für 32-Bit- und 64-Bit-PE-Dateien auf:



| Offset              | Size            | Feld                                      | Beschreibung                                                                                                                                                                                                                                                                                 |
|---------------------|-----------------|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>       | 4 <br/>   | Merkmale <br/>                | Flags, die Attribute der Datei angeben, die derzeit nicht verwendet werden. <br/>                                                                                                                                                                                                                   |
| 4 <br/>       | 4 <br/>   | TimeDateStamp <br/>                  | Datums- und Zeitstempelwert. Der Wert wird in der Anzahl der Sekunden dargestellt, die seit Mitternacht (00:00:00), 1. Januar 1970, koordinierte Weltzeit, gemäß der Systemuhr verstrichen sind. Der Zeitstempel kann mithilfe der Zeitfunktion der C-Laufzeit (CRT) ausgegeben werden. <br/> |
| 8 <br/>       | 2 <br/>   | MajorVersion <br/>                   | Hauptversionsnummer. <br/>                                                                                                                                                                                                                                                           |
| 10 <br/>      | 2 <br/>   | MinorVersion <br/>                   | Nebenversionsnummer. <br/>                                                                                                                                                                                                                                                           |
| 12 <br/>      | 4 <br/>   | GlobalFlagsClear <br/>               | Die globalen Ladeprogrammflags, die für diesen Prozess gelöscht werden sollen, wenn das Ladeprogramm den Prozess startet. <br/>                                                                                                                                                                                             |
| 16 <br/>      | 4 <br/>   | GlobalFlagsSet <br/>                 | Die globalen Ladeprogrammflags, die für diesen Prozess festgelegt werden sollen, wenn das Ladeprogramm den Prozess startet. <br/>                                                                                                                                                                                               |
| 20 <br/>      | 4 <br/>   | CriticalSectionDefaultTimeout <br/>  | Der Standardtimeoutwert, der für die kritischen Abschnitte dieses Prozesses verwendet werden soll, die abgebrochen werden. <br/>                                                                                                                                                                                       |
| 24 <br/>      | 4/8 <br/> | DeCommitFreeBlockThreshold <br/>     | Arbeitsspeicher, der freigegeben werden muss, bevor er in Bytes an das System zurückgegeben wird. <br/>                                                                                                                                                                                                        |
| 28/32 <br/>   | 4/8 <br/> | DeCommitTotalFreeThreshold <br/>     | Gesamtmenge des freien Arbeitsspeichers in Bytes. <br/>                                                                                                                                                                                                                                          |
| 32/40 <br/>   | 4/8 <br/> | LockPrefixTable <br/>                | \[x86 nur \] Die VA einer Liste von Adressen, in der das LOCK-Präfix verwendet wird, sodass sie durch NOP auf Einzelprozessorcomputern ersetzt werden können. <br/>                                                                                                                                    |
| 36/48 <br/>   | 4/8 <br/> | MaximumAllocationSize <br/>          | Maximale Zuordnungsgröße in Bytes. <br/>                                                                                                                                                                                                                                              |
| 40/56 <br/>   | 4/8 <br/> | VirtualMemoryThreshold <br/>         | Maximale Größe des virtuellen Arbeitsspeichers in Bytes. <br/>                                                                                                                                                                                                                                          |
| 44/64 <br/>   | 4/8 <br/> | ProcessAffinityMask <br/>            | Das Festlegen dieses Felds auf einen Wert ungleich 0 (null) entspricht dem Aufruf von SetProcessAffinityMask mit diesem Wert während des Prozessstarts (nur .exe). <br/>                                                                                                                                       |
| 48/72 <br/>   | 4 <br/>   | ProcessHeapFlags <br/>               | Verarbeiten Sie Heapflags, die dem ersten Argument der HeapCreate-Funktion entsprechen. Diese Flags gelten für den Prozessheap, der während des Prozessstarts erstellt wird. <br/>                                                                                                              |
| 52/76 <br/>   | 2 <br/>   | CSDVersion <br/>                     | Der Service Pack-Versionsbezeichner. <br/>                                                                                                                                                                                                                                            |
| 54/78 <br/>   | 2 <br/>   | Reserviert <br/>                       | Muss Null sein. <br/>                                                                                                                                                                                                                                                                   |
| 56/80 <br/>   | 4/8 <br/> | EditList <br/>                       | Für die Verwendung durch das System reserviert. <br/>                                                                                                                                                                                                                                                 |
| 60/88 <br/>   | 4/8 <br/> | SecurityCookie <br/>                 | Ein Zeiger auf ein Cookie, das von Visual C++ oder GS-Implementierung verwendet wird. <br/>                                                                                                                                                                                                          |
| 64/96 <br/>   | 4/8 <br/> | SEHandlerTable <br/>                 | \[x86 nur \] Die VA der sortierten Tabelle der RVAs jedes gültigen, eindeutigen SE Handlers im Bild. <br/>                                                                                                                                                                                  |
| 68/104 <br/>  | 4/8 <br/> | SEHandlerCount <br/>                 | \[Nur x86 \] Die Anzahl der eindeutigen Handler in der Tabelle. <br/>                                                                                                                                                                                                                         |
| 72/112 <br/>  | 4/8 <br/> | GuardCFCheckFunctionPointer <br/>    | Die VA, in der der Check-Function-Zeiger Control Flow Guard gespeichert wird. <br/>                                                                                                                                                                                                               |
| 76/120 <br/>  | 4/8 <br/> | GuardCFDispatchFunctionPointer <br/> | Die VA, in der der Dispatchfunktionszeiger Control Flow Guard gespeichert wird. <br/>                                                                                                                                                                                                            |
| 80/128 <br/>  | 4/8 <br/> | GuardCFFunctionTable <br/>           | Die VA der sortierten Tabelle der RVAs jeder Control Flow Guard-Funktion im Bild. <br/>                                                                                                                                                                                            |
| 84/136 <br/>  | 4/8 <br/> | GuardCFFunctionCount <br/>           | Die Anzahl der eindeutigen RVAs in der obigen Tabelle. <br/>                                                                                                                                                                                                                                    |
| 88/144 <br/>  | 4 <br/>   | GuardFlags <br/>                     | Steuern sie Flow Guard-bezogene Flags. <br/>                                                                                                                                                                                                                                               |
| 92/148 <br/>  | 12 <br/>  | CodeIntegrity <br/>                  | Codeintegritätsinformationen. <br/>                                                                                                                                                                                                                                                     |
| 104/160 <br/> | 4/8 <br/> | GuardAddressTakenIatEntryTable <br/> | Die VA, in der die IAT-Tabelle Control Flow Guard-Adresse gespeichert wird. <br/>                                                                                                                                                                                                              |
| 108/168 <br/> | 4/8 <br/> | GuardAddressTakenIatEntryCount <br/> | Die Anzahl der eindeutigen RVAs in der obigen Tabelle. <br/>                                                                                                                                                                                                                                    |
| 112/176 <br/> | 4/8 <br/> | GuardLongJumpTargetTable <br/>       | Die VA, in der die Tabelle control Flow Guard long jump target gespeichert wird. <br/>                                                                                                                                                                                                               |
| 116/184 <br/> | 4/8 <br/> | GuardLongJumpTargetCount <br/>       | Die Anzahl der eindeutigen RVAs in der obigen Tabelle. <br/>                                                                                                                                                                                                                                    |



 

Das Feld GuardFlags enthält eine Kombination aus mindestens einem der folgenden Flags und Unterfelder:

-   Das Modul führt Überprüfungen der Ablaufsteuerungsintegrität mithilfe der vom System bereitgestellten Unterstützung durch.

    ` #define IMAGE_GUARD_CF_INSTRUMENTED  0x00000100`

-   Das Modul führt Ablaufsteuerungs- und Schreibintegritätsprüfungen durch.

    ` #define IMAGE_GUARD_CFW_INSTRUMENTED  0x00000200`

-   Das Modul enthält gültige Ablaufsteuerungszielmetadaten.

    `#define IMAGE_GUARD_CF_FUNCTION_TABLE_PRESENT  0x00000400`

-   Das Modul verwendet nicht das /GS-Sicherheitscookie.

    ` #define IMAGE_GUARD_SECURITY_COOKIE_UNUSED  0x00000800`

-   Das Modul unterstützt IAT für schreibgeschütztes verzögertes Laden.

    `#define IMAGE_GUARD_PROTECT_DELAYLOAD_IAT  0x00001000`

-   Verzögertes Laden der Importtabelle im eigenen DIDAT-Abschnitt (ohne weitere Informationen), der frei erneut geschützt werden kann.

    ` #define IMAGE_GUARD_DELAYLOAD_IAT_IN_ITS_OWN_SECTION  0x00002000`

-   Das Modul enthält unterdrückte Exportinformationen. Dies leitet auch ab, dass die IAT-Adresstabelle auch in der Ladekonfiguration vorhanden ist.

    `#define  IMAGE_GUARD_CF_EXPORT_SUPPRESSION_INFO_PRESENT  0x00004000`

-   Das Modul ermöglicht die Unterdrückung von Exporten.

    `#define IMAGE_GUARD_CF_ENABLE_EXPORT_SUPPRESSION  0x00008000`

-   Das Modul enthält Longjmp-Zielinformationen.

    ` #define IMAGE_GUARD_CF_LONGJUMP_TABLE_PRESENT  0x00010000`

-   Maskieren Sie für das Unterfeld, das den Schritt der Einträge in der Control Flow Guard-Funktionstabelle enthält (d. b. die zusätzliche Anzahl von Bytes pro Tabelleneintrag).

    ` #define IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_MASK  0xF0000000`

Darüber hinaus definiert der Windows SDK-Header winnt.h dieses Makro für die Menge der Bits, um den GuardFlags-Wert nach rechts zu verschieben, um die Steuerung Flow Guard-Funktionstabelle zu rechtfertigen:

` #define IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_SHIFT  28`

### <a name="the-rsrc-section"></a>Abschnitt ".rsrc"

Ressourcen werden durch eine binär sortierte Struktur mit mehreren Ebenen indiziert. Der allgemeine Entwurf kann 2 \* \* 31 Ebenen umfassen. Laut Konvention verwendet Windows jedoch drei Ebenen:

<dl> type  
Name  
Sprache  
</dl>

Eine Reihe von Ressourcenverzeichnistabellen verknüpft alle Ebenen wie folgt: Auf jede Verzeichnistabelle folgt eine Reihe von Verzeichniseinträgen, die den Namen oder Bezeichner (ID) für diese Ebene (Typ, Name oder Sprachebene) und eine Adresse einer Datenbeschreibung oder einer anderen Verzeichnistabelle enthalten. Wenn die Adresse auf eine Datenbeschreibung verweist, handelt es sich bei den Daten um ein Blatt in der Struktur. Wenn die Adresse auf eine andere Verzeichnistabelle verweist, listet diese Tabelle Verzeichniseinträge auf der nächsten Ebene nach unten auf.

Typ-, Namens- und Sprach-IDs eines Blatts werden durch den Pfad bestimmt, der durch Verzeichnistabellen geleitet wird, um das Blatt zu erreichen. Die erste Tabelle bestimmt die Typ-ID, die zweite Tabelle (auf die durch den Verzeichniseintrag in der ersten Tabelle verwiesen wird) bestimmt die Namens-ID, und die dritte Tabelle bestimmt die Sprach-ID.

Die allgemeine Struktur des Abschnitts .rsrc lautet:



| Daten                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ressourcenverzeichnistabellen (und Ressourcenverzeichniseinträge) <br/> | Eine Reihe von Tabellen, eine für jede Gruppe von Knoten in der Struktur. Alle Knoten der obersten Ebene (Typ) werden in der ersten Tabelle aufgeführt. Einträge in dieser Tabelle zeigen auf Tabellen der zweiten Ebene. Jede Struktur der zweiten Ebene hat die gleiche Typ-ID, aber unterschiedliche Namens-IDs. Strukturen auf dritter Ebene haben die gleichen Typ- und Namens-IDs, aber unterschiedliche Sprach-IDs. <br/> Auf jede einzelne Tabelle folgen unmittelbar Verzeichniseinträge, in denen jeder Eintrag einen Namen oder numerischen Bezeichner und einen Zeiger auf eine Datenbeschreibung oder eine Tabelle auf der nächstunteren Ebene hat. <br/> |
| Ressourcenverzeichniszeichenfolgen <br/>                                 | Zwei-Byte-ausgerichtete Unicode-Zeichenfolgen, die als Zeichenfolgendaten dienen, auf die verzeichniseinträge verweisen. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Beschreibung der Ressourcendaten <br/>                                  | Ein Array von Datensätzen, auf die von Tabellen verwiesen wird, die die tatsächliche Größe und den Tatsächlichen Speicherort der Ressourcendaten beschreiben. Diese Datensätze sind die Blätter in der Ressourcenbeschreibungsstruktur. <br/>                                                                                                                                                                                                                                                                                                                                                                |
| Ressourcendaten <br/>                                              | Rohdaten des Ressourcenabschnitts. Die Größen- und Standortinformationen im Feld Ressourcendatenbeschreibungen begrenzen die einzelnen Regionen der Ressourcendaten. <br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

#### <a name="resource-directory-table"></a>Ressourcenverzeichnistabelle

Jede Ressourcenverzeichnistabelle hat das folgende Format. Diese Datenstruktur sollte als Überschrift einer Tabelle betrachtet werden, da die Tabelle tatsächlich aus Verzeichniseinträgen (beschrieben in Abschnitt 6.9.2, "Ressourcenverzeichniseinträge") und dieser Struktur besteht:



| Offset         | Size          | Feld                              | Beschreibung                                                                                                                                                                     |
|----------------|---------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Merkmale <br/>        | Ressourcenflags. Dieses Feld ist für eine spätere Verwendung vorgesehen. Sie ist derzeit auf 0 (null) festgelegt. <br/>                                                                                 |
| 4 <br/>  | 4 <br/> | Uhrzeit/Datumsstempel <br/>        | Der Zeitpunkt, zu dem die Ressourcendaten vom Ressourcencompiler erstellt wurden. <br/>                                                                                               |
| 8 <br/>  | 2 <br/> | Hauptversion <br/>          | Die Vom Benutzer festgelegte Hauptversionsnummer. <br/>                                                                                                                          |
| 10 <br/> | 2 <br/> | Nebenversion <br/>          | Die vom Benutzer festgelegte Nebenversionsnummer. <br/>                                                                                                                          |
| 12 <br/> | 2 <br/> | Anzahl von Namenseinträgen <br/> | Die Anzahl der Verzeichniseinträge unmittelbar nach der Tabelle, die Zeichenfolgen verwenden, um Einträge vom Typ, Namen oder der Sprache zu identifizieren (abhängig von der Ebene der Tabelle). <br/> |
| 14 <br/> | 2 <br/> | Anzahl von ID-Einträgen <br/>   | Die Anzahl der Verzeichniseinträge unmittelbar nach den Namenseinträgen, die numerische IDs für Type-, Name- oder Language-Einträge verwenden. <br/>                                    |



 

#### <a name="resource-directory-entries"></a>Ressourcenverzeichniseinträge

Die Verzeichniseinträge bilden die Zeilen einer Tabelle. Jeder Ressourcenverzeichniseintrag hat das folgende Format. Ob der Eintrag ein Name- oder ID-Eintrag ist, wird durch die Ressourcenverzeichnistabelle angegeben, die angibt, wie viele Name- und ID-Einträge darauf folgen (denken Sie daran, dass alle Namenseinträge allen ID-Einträgen für die Tabelle vorangestellt sind). Alle Einträge für die Tabelle werden in aufsteigender Reihenfolge sortiert: die Name-Einträge nach Zeichenfolge, bei der die Groß-/Kleinschreibung beachtet wird, und die ID-Einträge nach numerischem Wert. Offsets sind relativ zur Adresse im \_ IMAGE DIRECTORY ENTRY RESOURCE \_ \_ DataDirectory. Weitere Informationen finden Sie unter [Peering inside the PE: A Tour of the Win32 Portable Executable File Format (Peering innerhalb des PE: Überblick über das Win32 Portable Executable File Format).](/previous-versions/ms809762(v=msdn.10)#pe-file-resources)



| Offset        | Size          | Feld                           | Beschreibung                                                                                                          |
|---------------|---------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Namensoffset <br/>         | Der Offset einer Zeichenfolge, die abhängig von der Tabellenebene den Eintrag Typ, Name oder Sprach-ID angibt. <br/>     |
| 0 <br/> | 4 <br/> | Ganzzahlige ID <br/>          | Eine 32-Bit-Ganzzahl, die den Eintrag Typ, Name oder Sprach-ID identifiziert. <br/>                                   |
| 4 <br/> | 4 <br/> | Dateneingabeoffset <br/>   | High Bit 0. Adresse eines Ressourcendateneintrags (Blatt). <br/>                                                   |
| 4 <br/> | 4 <br/> | Unterverzeichnisoffset <br/> | High Bit 1. Die unteren 31 Bits sind die Adresse einer anderen Ressourcenverzeichnistabelle (die nächste Ebene nach unten). <br/> |



 

#### <a name="resource-directory-string"></a>Ressourcenverzeichniszeichenfolge

Der Zeichenfolgenbereich des Ressourcenverzeichnisses besteht aus Unicode-Zeichenfolgen, die wortbündig ausgerichtet sind. Diese Zeichenfolgen werden nach dem letzten Ressourcenverzeichniseintrag und vor dem ersten Ressourcendateneintrag zusammen gespeichert. Dadurch werden die Auswirkungen dieser Zeichenfolgen variabler Länge auf die Ausrichtung der Verzeichniseinträge fester Größe minimiert. Jede Ressourcenverzeichniszeichenfolge hat das folgende Format:



| Offset        | Size                 | Feld                      | Beschreibung                                                            |
|---------------|----------------------|----------------------------|------------------------------------------------------------------------|
| 0 <br/> | 2 <br/>        | Länge <br/>         | Die Größe der Zeichenfolge ohne Längenfeld selbst. <br/> |
| 2 <br/> | -Variable <br/> | Unicode-Zeichenfolge <br/> | Die Unicode-Zeichenfolgendaten variabler Länge, wortbündig ausgerichtet. <br/>     |



 

#### <a name="resource-data-entry"></a>Ressourcendateneintrag

Jeder Ressourcendateneintrag beschreibt eine tatsächliche Einheit von Rohdaten im Bereich Ressourcendaten. Ein Ressourcendateneintrag hat das folgende Format:



| Offset         | Size          | Feld                            | Beschreibung                                                                                                                                           |
|----------------|---------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Data RVA <br/>             | Die Adresse einer Einheit von Ressourcendaten im Bereich Ressourcendaten. <br/>                                                                         |
| 4 <br/>  | 4 <br/> | Size <br/>                 | Die Größe der Ressourcendaten in Bytes, auf die im Feld Data RVA verwiesen wird. <br/>                                                        |
| 8 <br/>  | 4 <br/> | codepage <br/>             | Die Codepage, die zum Decodieren von Codepunktwerten innerhalb der Ressourcendaten verwendet wird. In der Regel ist die Codepage die Unicode-Codepage. <br/> |
| 12 <br/> | 4 <br/> | Reserviert, muss 0 sein. <br/> |                                                                                                                                                       |



 

### <a name="the-cormeta-section-object-only"></a>.cormeta-Abschnitt (nur Objekt)

CLR-Metadaten werden in diesem Abschnitt gespeichert. Sie wird verwendet, um anzugeben, dass die Objektdatei verwalteten Code enthält. Das Format der Metadaten ist nicht dokumentiert, kann aber zur Behandlung von Metadaten an die CLR-Schnittstellen übergeben werden.

### <a name="the-sxdata-section"></a>Der SXDATA-Abschnitt

Die gültigen Ausnahmehandler eines Objekts werden im Abschnitt **.sxdata** dieses Objekts aufgeführt. Der Abschnitt ist als IMAGE \_ SCN \_ LNK \_ INFO gekennzeichnet. Sie enthält den COFF-Symbolindex jedes gültigen Handlers mit 4 Bytes pro Index.

Darüber hinaus markiert der Compiler ein COFF-Objekt als registriertes SEH, indem er das absolute Symbol " @feat.00 " " aussendet, wobei der LSB des Wertfelds auf 1 festgelegt ist. Ein COFF-Objekt ohne registrierte SEH-Handler hätte das Symbol " @feat.00 " , aber keinen **SXDATA-Abschnitt.**

## <a name="archive-library-file-format"></a>Archivdateiformat (Bibliothek)

- [Archivdateisignatur](#archive-file-signature)
- [Archivmemberheader](#archive-member-headers)
- [Erster Linkermember](#first-linker-member)
- [Zweiter Linkermember](#second-linker-member)
- [Longnames-Member](#longnames-member)

Das COFF-Archivformat bietet einen Standardmechanismus zum Speichern von Sammlungen von Objektdateien. Diese Sammlungen werden in der Programmierdokumentation häufig als Bibliotheken bezeichnet.

Die ersten 8 Bytes eines Archivs bestehen aus der Dateisignatur. Der Rest des Archivs besteht wie folgt aus einer Reihe von Archivmembern:

-   Der erste und der zweite Member sind "Linkermember". Jeder dieser Member verfügt über ein eigenes Format, wie im Abschnitt [Import Name Type (Importnametyp)](#import-name-type)beschrieben. In der Regel platziert ein Linker Informationen in diese Archivmember. Die Linkermember enthalten das Verzeichnis des Archivs.

-   Der dritte Member ist der Member "longnames". Dieser optionale Member besteht aus einer Reihe von MIT NULL endenden ASCII-Zeichenfolgen, in denen jede Zeichenfolge der Name eines anderen Archivmembers ist.

-   Der Rest des Archivs besteht aus Standardmembern (Objektdatei). Jeder dieser Member enthält den Inhalt einer Objektdatei in seiner Gesamtheit.

Jedem Element wird ein Archivmemberheader vorangestellt. Die folgende Liste zeigt die allgemeine Struktur eines Archivs:

-   Signatur :"! &lt; arch &gt; \\ n"
-   Header

    <dl> 1. Linkermitglied  
    </dl>

-   Header

    <dl> 2. Linkermember  
    </dl>

-   Header

    <dl> Longnames-Member  
    </dl>

-   Header

    <dl> Inhalt der OBJ-Datei 1  
    (COFF-Format)  
    </dl>

-   Header

    <dl> Inhalt der OBJ-Datei 2  
    (COFF-Format)  
    </dl>

### <a name="archive-file-signature"></a>Archivdateisignatur

Die Archivdateisignatur identifiziert den Dateityp. Jedes Hilfsprogramm (z. B. ein Linker), das eine Archivdatei als Eingabe annimmt, kann den Dateityp überprüfen, indem diese Signatur gelesen wird. Die Signatur besteht aus den folgenden ASCII-Zeichen, in denen jedes unten stehende Zeichen mit Ausnahme des Zeichens newline ( n) wörtlich dargestellt \\ wird:

`!<arch>\n`

### <a name="archive-member-headers"></a>Archivmemberheader

Jedem Member (Linker, Longnames oder Objektdateimember) wird ein Header vorangestellt. Ein Archivmemberheader hat das folgende Format, in dem jedes Feld eine ASCII-Textzeichenfolge ist, die mit Leerzeichen am Ende des Felds ausgerichtet und aufgefüllt wird. In einem dieser Felder ist kein abschließendes NULL-Zeichen vorhanden.

Jeder Memberheader beginnt mit der ersten geraden Adresse nach dem Ende des vorherigen Archivmembers.



| Offset         | Size           | Feld                     | Beschreibung                                                                                                                                                                                                 |
|----------------|----------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 16 <br/> | Name <br/>          | Der Name des Archivmembers, an den ein Schrägstrich (/) angefügt ist, um den Namen zu beenden. Wenn das erste Zeichen ein Schrägstrich ist, weist der Name eine besondere Interpretation auf, wie in der folgenden Tabelle beschrieben. <br/> |
| 16 <br/> | 12 <br/> | Date <br/>          | Datum und Uhrzeit der Erstellung des Archivmembers: Dies ist die ASCII-Dezimaldarstellung der Anzahl von Sekunden seit dem 1.1.1970 UCT. <br/>                                                    |
| 28 <br/> | 6 <br/>  | Benutzer-ID <br/>       | Eine ASCII-Dezimaldarstellung der Benutzer-ID. Dieses Feld enthält keinen aussagekräftigen Wert auf Windows Plattformen, da Microsoft-Tools alle Leerzeichen ausgeben. <br/>                                    |
| 34 <br/> | 6 <br/>  | Gruppen-ID <br/>      | Eine ASCII-Dezimaldarstellung der Gruppen-ID. Dieses Feld enthält keinen aussagekräftigen Wert auf Windows Plattformen, da Microsoft-Tools alle Leerzeichen ausgeben. <br/>                                   |
| 40 <br/> | 8 <br/>  | Mode <br/>          | Eine ASCII-oktale Darstellung des Dateimodus des Members. Dies ist der ST \_ MODE-Wert aus der C-Laufzeitfunktion \_ wstat. <br/>                                                                       |
| 48 <br/> | 10 <br/> | Size <br/>          | Eine ASCII-Dezimaldarstellung der Gesamtgröße des Archivmembers, ohne die Größe des Headers. <br/>                                                                                  |
| 58 <br/> | 2 <br/>  | Ende des Headers <br/> | Die beiden Bytes in der C-Zeichenfolge "bro \\ n" (0x60 0x0A). <br/>                                                                                                                                               |



 

Das Feld Name weist eines der in der folgenden Tabelle gezeigten Formate auf. Wie bereits erwähnt, wird jede dieser Zeichenfolgen ausgerichtet und mit nachgestellten Leerzeichen innerhalb eines Felds von 16 Bytes aufgefüllt:



| Inhalt des Felds "Name" | Beschreibung                                                                                                                                                                                                                                                                                          |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name/ <br/>      | Der Name des Archivmembers. <br/>                                                                                                                                                                                                                                                          |
| / <br/>          | Der Archivmember ist einer der beiden Linkermember. Beide Linkermember haben diesen Namen. <br/>                                                                                                                                                                                          |
| // <br/>         | Das Archivmember ist der Longnames-Member, der aus einer Reihe von AUF NULL endende ASCII-Zeichenfolgen besteht. Der Longnames-Member ist der dritte Archivmember und optional. <br/>                                                                     |
| /n <br/>         | Der Name des Archivmembers befindet sich bei Offset n innerhalb des Longnames-Members. Die Zahl n ist die Dezimaldarstellung des Offsets. Beispiel: "/26" gibt an, dass der Name des Archivmembers 26 Bytes hinter dem Anfang des Longnames-Elementinhalts liegt. <br/> |



 

### <a name="first-linker-member"></a>Erster Linkermember

Der Name des ersten Linkermembers lautet "/". Der erste Linkermember ist aus Gründen der Abwärtskompatibilität enthalten. Sie wird nicht von aktuellen Linkern verwendet, aber ihr Format muss korrekt sein. Dieser Linkermember stellt ein Verzeichnis mit Symbolnamen bereit, ebenso wie das zweite Linkermember. Für jedes Symbol geben die Informationen an, wo das Archivmember zu finden ist, das das Symbol enthält.

Der erste Linkermember hat das folgende Format. Diese Informationen werden nach dem Header angezeigt:



| Offset         | Size               | Feld                         | Beschreibung                                                                                                                                                                                                                                                                                                                                                        |
|----------------|--------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/>      | Anzahl von Symbolen <br/> | Unsigned long, das die Anzahl der indizierten Symbole enthält. Diese Zahl wird im Big-Endian-Format gespeichert. Jedes Objektdateimember definiert in der Regel ein oder mehrere externe Symbole. <br/>                                                                                                                                                                         |
| 4 <br/>  | 4 \* n <br/> | Offsets <br/>           | Ein Array von Dateioffsets zu Archivmemberheadern, wobei n gleich dem Feld Number of Symbols (Anzahl von Symbolen) ist. Jede Zahl im Array ist eine lange Zahl ohne Vorzeichen, die im Big-Endian-Format gespeichert ist. Für jedes Symbol, das in der Zeichenfolgentabelle benannt ist, gibt das entsprechende Element im Offsetarray die Position des Archivelements an, das das Symbol enthält. <br/> |
| \* <br/> | \* <br/>     | Zeichenfolgentabelle <br/>      | Eine Reihe von auf NULL endenden Zeichenfolgen, die alle Symbole im Verzeichnis benennen. Jede Zeichenfolge beginnt unmittelbar nach dem NULL-Zeichen in der vorherigen Zeichenfolge. Die Anzahl der Zeichenfolgen muss gleich dem Wert des Felds Anzahl von Symbolen sein. <br/>                                                                                                       |



 

Die Elemente im Offsetarray müssen in aufsteigender Reihenfolge angeordnet werden. Dies bedeutet, dass die Symbole in der Zeichenfolgentabelle entsprechend der Reihenfolge der Archivmember angeordnet werden müssen. Beispielsweise müssten alle Symbole im ersten Objektdateimember vor den Symbolen in der zweiten Objektdatei aufgelistet werden.

### <a name="second-linker-member"></a>Zweiter Linkermember

Der zweite Linkermember hat den Namen "/" wie der erste Linkermember. Obwohl beide Linkermember ein Verzeichnis von Symbolen und Archivmembern bereitstellen, die sie enthalten, wird das zweite Linkermember von allen aktuellen Linkern bevorzugt verwendet. Der zweite Linkermember enthält Symbolnamen in lexikalischer Reihenfolge, was eine schnellere Suche nach Namen ermöglicht.

Das zweite Element hat das folgende Format. Diese Informationen werden nach dem Header angezeigt:



| Offset         | Size               | Feld                         | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|--------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/>      | Anzahl von Membern <br/> | Eine Länge ohne Vorzeichen, die die Anzahl der Archivmember enthält. <br/>                                                                                                                                                                                                                                                                                                                                |
| 4 <br/>  | 4 \* m <br/> | Offsets <br/>           | Ein Array von Dateioffsets zu Archivmemberheadern, die in aufsteigender Reihenfolge angeordnet sind. Jeder Offset ist ein unsigned long . Die Zahl m entspricht dem Wert des Felds Anzahl von Mitgliedern. <br/>                                                                                                                                                                                                        |
| \* <br/> | 4 <br/>      | Anzahl von Symbolen <br/> | Ein long-Wert ohne Vorzeichen, der die Anzahl der indizierten Symbole enthält. Jedes Objektdateimember definiert in der Regel ein oder mehrere externe Symbole. <br/>                                                                                                                                                                                                                                                        |
| \* <br/> | 2 \* n <br/> | Indizes <br/>           | Ein Array von 1-basierten Indizes (kurz ohne Vorzeichen), die Symbolnamen zu Archivmemberoffsets zuordnen. Die Zahl n entspricht dem Feld Anzahl von Symbolen. Für jedes Symbol, das in der Zeichenfolgentabelle benannt ist, gibt das entsprechende Element im Indexarray einen Index in das Offsets-Array. Das Offsetarray gibt wiederum die Position des Archivmembers an, der das Symbol enthält. <br/> |
| \* <br/> | \* <br/>     | Zeichenfolgentabelle <br/>      | Eine Reihe von auf NULL endenden Zeichenfolgen, die alle Symbole im Verzeichnis benennen. Jede Zeichenfolge beginnt unmittelbar nach dem NULL-Byte in der vorherigen Zeichenfolge. Die Anzahl der Zeichenfolgen muss gleich dem Wert des Felds Anzahl von Symbolen sein. In dieser Tabelle werden alle Symbolnamen in aufsteigender lexikalischer Reihenfolge aufgelistet. <br/>                                                                             |



 

### <a name="longnames-member"></a>Longnames-Member

Der Name des Longnames-Members lautet "/". Der longnames-Member ist eine Reihe von Zeichenfolgen mit Archivmembernamen. Ein Name wird hier nur angezeigt, wenn nicht genügend Platz im Feld Name (16 Bytes) vorhanden ist. Der Longnames-Member ist optional. Es kann leer sein, wenn nur ein Header vorhanden ist, oder er kann ohne header vollständig fehlen.

Die Zeichenfolgen sind NULL-terminiert. Jede Zeichenfolge beginnt unmittelbar nach dem NULL-Byte in der vorherigen Zeichenfolge.

## <a name="import-library-format"></a>Importieren des Bibliotheksformats

- [Importheader](#import-header)
- [Importtyp](#import-type)

Herkömmliche Importbibliotheken, d. h. Bibliotheken, die die Exporte aus einem Bild zur Verwendung durch ein anderes beschreiben, folgen in der Regel dem in Abschnitt 7, [Archivdateiformat (Bibliothek)](#archive-library-file-format)beschriebenen Layout. Der Hauptunterschied besteht darin, dass Importbibliotheksmember Pseudoobjektdateien anstelle realer Dateien enthalten, in denen jedes Element die Abschnittsbeiträge enthält, die erforderlich sind, um die Importtabellen zu erstellen, die in Abschnitt 6.4, [The .idata Section,](#the-idata-section) beschrieben sind. Der Linker generiert dieses Archiv beim Erstellen der exportierenden Anwendung.

Die Abschnittsbeiträge für einen Import können aus einem kleinen Satz von Informationen abgeleitet werden. Der Linker kann entweder die vollständigen, ausführlichen Informationen für jedes Mitglied zum Zeitpunkt der Erstellung der Bibliothek in die Importbibliothek generieren oder nur die kanonischen Informationen in die Bibliothek schreiben und die Anwendung, die sie später verwendet, die erforderlichen Daten im Ruhevorgang generieren lassen.

In einer Importbibliothek mit dem langen Format enthält ein einzelner Member die folgenden Informationen:

<dl> Archivmemberheader  
Dateiheader  
Abschnittsheader  
Daten, die den einzelnen Abschnittsheadern entsprechen  
COFF-Symboltabelle  
Zeichenfolgen  
  
</dl>

Im Gegensatz dazu wird eine kurze Importbibliothek wie folgt geschrieben:

<dl> Archivmemberheader  
Importheader  
Auf NULL endende Importnamenzeichenfolge  
AUF NULL endende DLL-Namenszeichenfolge  
</dl>

Dies sind ausreichende Informationen, um den gesamten Inhalt des Members zum Zeitpunkt seiner Verwendung genau zu rekonstruieren.

### <a name="import-header"></a>Importheader

Der Importheader enthält die folgenden Felder und Offsets:



| Offset         | Size                | Feld                       | Beschreibung                                                                                                                  |
|----------------|---------------------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/>       | Sig1 <br/>            | Muss IMAGE \_ FILE MACHINE UNKNOWN \_ \_ sein. Weitere Informationen finden Sie unter [Computertypen.](#machine-types) <br/>                |
| 2 <br/>  | 2 <br/>       | Sig2 <br/>            | Muss 0xFFFF sein. <br/>                                                                                                  |
| 4 <br/>  | 2 <br/>       | Version <br/>         | Die Strukturversion. <br/>                                                                                           |
| 6 <br/>  | 2 <br/>       | Machine <br/>         | Die Zahl, die den Typ des Zielcomputers identifiziert. Weitere Informationen finden Sie unter [Computertypen.](#machine-types)<br/> |
| 8 <br/>  | 4 <br/>       | Time-Date Stamp <br/> | Die Uhrzeit und das Datum, an dem die Datei erstellt wurde. <br/>                                                                     |
| 12 <br/> | 4 <br/>       | Größe der Daten <br/>    | Die Größe der Zeichenfolgen, die dem Header folgen. <br/>                                                                  |
| 16 <br/> | 2 <br/>       | Ordnungszahl/Hinweis <br/>    | Entweder die Ordnungszahl oder der Hinweis für den Import, bestimmt durch den Wert im Feld Namenstyp. <br/>                   |
| 18 <br/> | 2 Bits <br/>  | Typ <br/>            | Der Importtyp. Spezifische Werte und Beschreibungen finden Sie unter [Importtyp.](#import-type)<br/>                           |
|                | 3 Bits <br/>  | Name-Typ <br/>       | Der Importnamenstyp. Weitere Informationen finden Sie unter [Import Name Type](#import-name-type). <br/>                           |
|                | 11 Bit <br/> | Reserviert <br/>        | Reserviert, muss 0 sein. <br/>                                                                                             |



 

Auf diese Struktur folgen zwei auf NULL endende Zeichenfolgen, die den Namen des importierten Symbols und die DLL beschreiben, aus der es stammt.

### <a name="import-type"></a>Importtyp

Die folgenden Werte werden für das Feld Type im Importheader definiert:

| Konstante                  | Wert         | Beschreibung                                      |
|---------------------------|---------------|--------------------------------------------------|
| IMPORTIEREN VON \_ CODE <br/>  | 0 <br/> | Ausführbarer Code. <br/>                     |
| IMPORTIEREN VON \_ DATEN <br/>  | 1 <br/> | Daten. <br/>                                |
| IMPORT \_ CONST <br/> | 2 <br/> | Wird in der DEF-Datei als CONST angegeben. <br/> |

Diese Werte werden verwendet, um zu bestimmen, welche Abschnittsbeiträge von dem Tool generiert werden müssen, das die Bibliothek verwendet, wenn sie auf diese Daten zugreifen muss.

### <a name="import-name-type"></a>Typ des Importnamens

Der auf NULL endende Importsymbolname folgt unmittelbar auf den zugeordneten Importheader. Die folgenden Werte werden für das Feld Namenstyp im Importheader definiert. Sie geben an, wie der Name verwendet werden soll, um die richtigen Symbole zu generieren, die den Import darstellen:

| Konstante | Wert | Beschreibung |
| - | - | - |
| IMPORT \_ ORDINAL | 0 | Der Import erfolgt nach Ordnungszahl. Dies gibt an, dass der Wert im Feld Ordinal/Hint des Importheaders die Ordnungszahl des Imports ist. Wenn diese Konstante nicht angegeben wird, sollte das Feld Ordinal/Hint immer als Hinweis des Imports interpretiert werden. |
| \_IMPORTNAME | 1 | Der Importname ist identisch mit dem Namen des öffentlichen Symbols. |
| IMPORTNAME \_ \_ NOPREFIX | 2 | Der Importname ist der öffentliche Symbolname, überspringt jedoch die führenden Zeichen ?, @oder optional \_ . |
| IMPORTNAME \_ \_ UNDECORATE | 3 | Der Importname ist der öffentliche Symbolname, überspringt jedoch die führenden Zeichen ?, @oder optional \_ , und schneidet bei der ersten @ ab. |

## <a name="appendix-a-calculating-authenticode-pe-image-hash"></a>Anhang A: Berechnen des Authenticode PE-Imagehashs

- [Was ist ein Authenticode PE-Imagehash?](#what-is-an-authenticode-pe-image-hash)
- [Was wird in einem Authenticode PE-Imagehash abgedeckt?](#what-is-covered-in-an-authenticode-pe-image-hash)

Es wird erwartet, dass mehrere Attributzertifikate verwendet werden, um die Integrität der Images zu überprüfen. Die gängigste ist jedoch die Authenticode-Signatur. Eine Authenticode-Signatur kann verwendet werden, um zu überprüfen, ob die relevanten Abschnitte einer PE-Imagedatei in keiner Weise vom ursprünglichen Format der Datei geändert wurden. Für diese Aufgabe enthalten Authenticode-Signaturen etwas, das als PE-Imagehash bezeichnet wird.

### <a name="what-is-an-authenticode-pe-image-hash"></a>Was ist ein Authenticode PE-Imagehash?

Der Authenticode PE-Imagehash oder kurz Der Dateihash ähnelt einer Dateiprüfsumme, da er einen kleinen Wert erzeugt, der sich auf die Integrität einer Datei bezieht. Eine Prüfsumme wird von einem einfachen Algorithmus erzeugt und hauptsächlich verwendet, um Speicherfehler zu erkennen. Das heißt, es wird verwendet, um zu erkennen, ob ein Speicherblock auf dem Datenträger fehlerhaft geworden ist und die dort gespeicherten Werte beschädigt wurden. Ein Dateihash ähnelt einer Prüfsumme, da er auch Dateibeschädigungen erkennt. Im Gegensatz zu den meisten Prüfsummenalgorithmen ist es jedoch sehr schwierig, eine Datei so zu ändern, dass sie den gleichen Dateihash wie ihr ursprüngliches (unverändertes) Format hat. Das heißt, eine Prüfsumme dient dazu, einfache Speicherfehler zu erkennen, die zu Beschädigungen führen, aber ein Dateihash kann verwendet werden, um absichtliche und sogar geringfügige Änderungen an einer Datei zu erkennen, z. B. solche, die durch Viren, Hacker oder Trojanerprogramme eingeführt wurden.

Bei einer Authenticode-Signatur wird der Dateihash digital signiert, indem ein privater Schlüssel verwendet wird, der nur dem Signaturgeber der Datei bekannt ist. Ein Softwareverbraucher kann die Integrität der Datei überprüfen, indem er den Hashwert der Datei berechnet und mit dem Wert des signierten Hashs vergleicht, der in der digitalen Authenticode-Signatur enthalten ist. Wenn die Dateihashes nicht übereinstimmen, wurde ein Teil der Vom PE-Imagehash abgedeckten Datei geändert.

### <a name="what-is-covered-in-an-authenticode-pe-image-hash"></a>Was wird in einem Authenticode PE-Imagehash abgedeckt?

Es ist nicht möglich oder wünschenswert, alle Bilddateidaten in die Berechnung des PE-Imagehashs einzuschließen. Manchmal stellt sie einfach unerwünschte Merkmale dar (z. B. können Debuginformationen nicht aus öffentlich veröffentlichten Dateien entfernt werden). manchmal ist es einfach unmöglich. Beispielsweise ist es nicht möglich, alle Informationen in einer Bilddatei in eine Authenticode-Signatur einzuschließen, dann die Authenticode-Signatur, die diesen PE-Imagehash enthält, in das PE-Image einzufügen und später einen identischen PE-Imagehash generieren zu können, indem alle Bilddateidaten erneut in die Berechnung einbezogen werden, da die Datei jetzt die Authenticode-Signatur enthält, die ursprünglich nicht vorhanden war.

#### <a name="process-for-generating-the-authenticode-pe-image-hash"></a>Prozess zum Generieren des Authenticode PE-Imagehashs

In diesem Abschnitt wird beschrieben, wie ein PE-Imagehash berechnet wird und welche Teile des PE-Images geändert werden können, ohne dass die Authenticode-Signatur ungültig wird.

> [!NOTE]
> Der PE-Imagehash für eine bestimmte Datei kann in einer separaten Katalogdatei enthalten sein, ohne ein Attributzertifikat in die Hashdatei aufzunehmen. Dies ist relevant, da es möglich ist, den PE-Imagehash in einer Authenticode-signierten Katalogdatei ungültig zu machen, indem ein PE-Image geändert wird, das eigentlich keine Authenticode-Signatur enthält.

Alle Daten in Abschnitten des PE-Images, die in der Abschnittstabelle angegeben sind, werden mit Ausnahme der folgenden Ausschlussbereiche vollständig gehasht:

- **Das CheckSum-Feld der Datei der Windows spezifischen Felder des optionalen Headers.** Diese Prüfsumme enthält die gesamte Datei (einschließlich aller Attributzertifikate in der Datei). Die Prüfsumme unterscheidet sich aller Wahrscheinlichkeit nach dem Einfügen der Authenticode-Signatur vom ursprünglichen Wert.

- **Informationen im Zusammenhang mit Attributzertifikaten.** Die Bereiche des PE-Images, die sich auf die Authenticode-Signatur beziehen, sind nicht in der Berechnung des PE-Imagehashs enthalten, da Authenticode-Signaturen einem Image hinzugefügt oder daraus entfernt werden können, ohne die Allgemeine Integrität des Images zu beeinträchtigen. Dies ist kein Problem, da es Benutzerszenarien gibt, die davon abhängen, PE-Images erneut zu signieren oder einen Zeitstempel hinzuzufügen. Authenticode schließt die folgenden Informationen aus der Hashberechnung aus:

  - Das Feld Zertifikattabelle der optionalen Headerdatenverzeichnisse.

  - Die Zertifikattabelle und die entsprechenden Zertifikate, auf die das feld Zertifikattabelle zeigt, das direkt oben aufgeführt ist.

  Um den PE-Imagehash zu berechnen, sortiert Authenticode die in der Abschnittstabelle angegebenen Abschnitte nach Adressbereich und hasht dann die resultierende Bytesequenz und übergibt die Ausschlussbereiche.

- **Informationen nach dem Ende des letzten Abschnitts.** Der Bereich hinter dem letzten Abschnitt (definiert durch den höchsten Offset) wird nicht per Hashwert versehen. Dieser Bereich enthält häufig Debuginformationen. Debuginformationen können im Allgemeinen als Empfehlung für Debugger betrachtet werden. sie wirkt sich nicht auf die tatsächliche Integrität des ausführbaren Programms aus. Es ist durchaus möglich, Debuginformationen aus einem Image zu entfernen, nachdem ein Produkt geliefert wurde, ohne die Funktionalität des Programms zu beeinträchtigen. In der Tat wird dies manchmal als Datenträgersparmaßnahme durchgeführt. Beachten Sie, dass Debuginformationen, die in den angegebenen Abschnitten des PE-Images enthalten sind, nicht entfernt werden können, ohne dass die Authenticode-Signatur ungültig wird.

Sie können die im Windows Platform SDK bereitgestellten Tools makecert und signtool verwenden, um mit dem Erstellen und Überprüfen von Authenticode-Signaturen zu experimentieren. Weitere Informationen finden Sie weiter unten in der Referenz.

## <a name="references"></a>Referenzen

[Downloads und Tools für Windows (einschließlich des Windows SDK)](https://developer.microsoft.com/windows/downloads)

[Erstellen, Anzeigen und Verwalten von Zertifikaten](/windows/desktop/SecCrypto/creating-viewing-and-managing-certificates)

[Exemplarische Vorgehensweise zur Codesignierung im Kernelmodus (.doc)](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/KMCS_Walkthrough.doc)

[SignTool](/windows/desktop/SecCrypto/signtool)

[Windows Authenticode Portable Executable Signature Format (.docx)](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/Authenticode_PE.docx)

[ImageHlp-Funktionen](/windows/desktop/Debug/imagehlp-functions)
