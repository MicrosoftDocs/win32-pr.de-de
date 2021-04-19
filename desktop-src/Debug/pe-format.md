---
description: Diese Spezifikation beschreibt die Struktur von ausführbaren Dateien (Bilddateien) und Objektdateien unter der Windows-Betriebssystem Familie. Diese Dateien werden als portable ausführbare Dateien (PE) bzw. COFF-Dateien (Common Object File Format) bezeichnet.
ms.assetid: 3dbfbf7f-6662-45a4-99f1-e0e24c370dee
title: PE-Format
ms.topic: article
ms.date: 03/31/2021
ms.custom: contperf-fy21q1
ms.openlocfilehash: 3cc6fd777bca831ca4424baaa81c5525a24556ec
ms.sourcegitcommit: 3b9424e1dcd951b2a73e47de3c7f4d734de4263b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "106374063"
---
# <a name="pe-format"></a>PE-Format

Diese Spezifikation beschreibt die Struktur von ausführbaren Dateien (Bilddateien) und Objektdateien unter der Windows-Betriebssystem Familie. Diese Dateien werden als portable ausführbare Dateien (PE) bzw. COFF-Dateien (Common Object File Format) bezeichnet.

> [!Note]  
> Dieses Dokument wird bereitgestellt, um die Entwicklung von Tools und Anwendungen für Windows zu unterstützen. es ist jedoch nicht garantiert, dass es eine vollständige Spezifikation ist. Microsoft behält sich das Recht vor, dieses Dokument ohne vorherige Ankündigung zu ändern.

Diese Revision der von Microsoft Portable ausführbaren Datei und der allgemeinen Objektdatei Format Spezifikation ersetzt alle vorherigen Revisionen dieser Spezifikation.

## <a name="general-concepts"></a>Allgemeine Konzepte

In diesem Dokument wird die Struktur der ausführbaren Dateien (Bilddateien) und der Objektdateien unter der Microsoft Windows-Betriebssystem Familie angegeben. Diese Dateien werden als portable ausführbare Dateien (PE) bzw. COFF-Dateien (Common Object File Format) bezeichnet. Der Name "portable ausführbare Datei" bezieht sich auf die Tatsache, dass das Format nicht architekturspezifisch ist.

Bestimmte Konzepte, die in dieser Spezifikation angezeigt werden, werden in der folgenden Tabelle beschrieben:

| Name                              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Attribut Zertifikat <br/> | Ein Zertifikat, das verwendet wird, um überprüfbare Anweisungen einem Bild zuzuordnen. Eine Reihe von unterschiedlichen überprüfbaren Anweisungen kann einer Datei zugeordnet werden. eine der nützlichsten ist eine-Anweisung von einem Softwarehersteller, die angibt, wie der Nachrichten Digest des Abbilds erwartet wird. Ein Nachrichten Digest ähnelt einer Prüfsumme, mit dem Unterschied, dass es äußerst schwierig ist, Sie zu schmieden. Daher ist es sehr schwierig, eine Datei so zu ändern, dass Sie denselben Nachrichten Digest wie die ursprüngliche Datei hat. Die Anweisung kann überprüft werden, wenn Sie vom Hersteller mithilfe von kryptografieschemas für öffentliche oder private Schlüssel erstellt wird. In diesem Dokument werden Details zu Attribut Zertifikaten beschrieben, die für das Einfügen in Bilddateien nicht zulässig sind. <br/> |
| Datums-/Zeitstempel <br/>       | Ein Stempel, der für verschiedene Zwecke an mehreren Stellen in einer PE-oder COFF-Datei verwendet wird. In den meisten Fällen ist das Format jedes Stempels identisch mit dem, das von den Zeitfunktionen in der C-Lauf Zeit Bibliothek verwendet wird. Informationen zu Ausnahmen finden Sie unter deskripton von Image \_ Debug \_ Type \_ Repro in [Debug Type](#debug-type). Wenn der Stempel Wert 0 oder 0xFFFFFFFF ist, stellt er keinen echten oder sinnvollen Datums-/Uhrzeitstempel dar. <br/>                                                                                                                                                                                                                                                                                                                                            |
| Dateizeiger <br/>          | Der Speicherort eines Elements in der Datei selbst, bevor die Verarbeitung durch den Linker erfolgt (im Fall von Objektdateien) oder das Lade Tool (im Fall von Bilddateien). Dies bedeutet, dass es sich hierbei um eine Position innerhalb der Datei handelt, die auf dem Datenträger gespeichert ist. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Linker <br/>                | Ein Verweis auf den Linker, der mit Microsoft Visual Studio bereitgestellt wird. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Objektdatei <br/>           | Eine Datei, die als Eingabe für den Linker angegeben wird. Der Linker erstellt eine Bilddatei, die wiederum vom Lade Tool als Eingabe verwendet wird. Der Begriff "Objektdatei" impliziert nicht notwendigerweise eine Verbindung mit der objektorientierten Programmierung. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| reserviert, muss 0 sein. <br/>   | Eine Beschreibung eines Felds, das angibt, dass der Wert des Felds für Generatoren NULL sein muss, und Consumer müssen das Feld ignorieren. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Relative virtuelle Adresse (RVA) <br/>                   | In einer Bilddatei ist dies die Adresse eines Elements, nachdem es in den Arbeitsspeicher geladen wurde, wobei die Basisadresse der Abbild Datei von ihm subtrahiert wurde. Die RVA eines Elements unterscheidet sich fast immer von der Position in der Datei auf dem Datenträger (Dateizeiger). <br/> In einer Objektdatei ist eine RVA weniger sinnvoll, da keine Speicherorte zugewiesen werden. In diesem Fall handelt es sich bei einer RVA um eine Adresse in einem Abschnitt (weiter unten in dieser Tabelle beschrieben), auf den später während der Verknüpfung eine Verlagerung angewendet wird. Der Einfachheit halber sollte ein Compiler einfach die erste RVA in jedem Abschnitt auf NULL festlegen. <br/>                                                                                                                                         |
| section <br/>               | Die grundlegende Einheit von Code oder Daten in einer PE-oder COFF-Datei. Beispielsweise kann der gesamte Code in einer Objektdatei in einem einzelnen Abschnitt oder (je nach Compilerverhalten) kombiniert werden. jede Funktion kann einen eigenen Abschnitt belegen. Bei mehr Abschnitten gibt es mehr Datei Mehraufwand, aber der Linker ist in der Lage, den Code selektiv zu verknüpfen. Ein Abschnitt ähnelt einem Segment in der Intel 8086-Architektur. Alle Rohdaten in einem Abschnitt müssen zusammenhängend geladen werden. Außerdem kann eine Bilddatei eine Reihe von Abschnitten enthalten, wie z. b.. TLS oder. reloc, die besondere Zwecke haben. <br/>                                                                                                                                                                      |
| Virtuelle Adresse (VA) <br/>                    | Identisch mit RVA, mit der Ausnahme, dass die Basisadresse der Bilddatei nicht subtrahiert wird. Die Adresse wird als "VA" bezeichnet, da Windows für jeden Prozess einen eindeutigen VA-Raum erstellt, unabhängig vom physischen Speicher. Für fast alle Zwecke sollte ein VA als nur eine Adresse betrachtet werden. Ein VA ist nicht so vorhersagbar wie eine RVA, weil das Lade Modul das Bild möglicherweise nicht am bevorzugten Speicherort lädt. <br/>                                                                                                                                                                                                                                                                                                                                        |

## <a name="overview"></a>Übersicht

In der folgenden Liste wird das ausführbare Format von Microsoft PE beschrieben, wobei die Basis des Bild Headers oben angezeigt wird. Der Abschnitt vom MS-DOS 2,0-kompatiblen exe-Header bis zum nicht verwendeten Abschnitt direkt vor dem PE-Header ist der MS-DOS 2,0-Abschnitt und wird nur für die MS-DOS-Kompatibilität verwendet.

-   MS-DOS 2,0 kompatibler exe-Header
-   unused
-   OEM-Bezeichner

    Informationen zum Gerätehersteller

    Offset in PE-Header

-   MS 2,0-Stub-Programm und Verschiebungs Tabelle

-   unused

-   PE-Header (an 8-Byte-Begrenzung ausgerichtet)

-   Abschnitts Header
-   Bildseiten:

    Informationen importieren

    Informationen exportieren

    Basis Umsetzungen

    Ressourceninfo

In der folgenden Liste wird das Microsoft COFF-Objekt Modulformat beschrieben:

-   Microsoft COFF-Header
-   Abschnitts Header
-   Rohdaten:

    code

    Daten

    Debuginformationen

    dient

## <a name="file-headers"></a>Dateiheader

- [MS-DOS-Stub (nur Bild)](#ms-dos-stub-image-only)
- [Signatur (nur Bild)](#signature-image-only)
- [COFF-Datei Header (Objekt und Bild)](#coff-file-header-object-and-image)
  - [Computertypen](#machine-types)
  - [Characteristics](#characteristics)
- [Optionaler Header (nur Bild)](#optional-header-image-only)
  - [Optionale Header Standard Felder (nur Bild)](#optional-header-standard-fields-image-only)
  - [Optionale Header Windows-Specific Felder (nur Bild)](#optional-header-windows-specific-fields-image-only)
  - [Optionale Header Datenverzeichnisse (nur Bild)](#optional-header-data-directories-image-only)

Der PE-Dateiheader besteht aus einem Microsoft-MS-DOS-Stub, der PE-Signatur, dem COFF-Dateiheader und einem optionalen Header. Ein COFF-Objektdatei Header besteht aus einem COFF-Dateiheader und einem optionalen Header. In beiden Fällen folgen den Datei Headern sofort Abschnitts Header.

### <a name="ms-dos-stub-image-only"></a>MS-DOS-Stub (nur Bild)

Der MS-DOS-Stub ist eine gültige Anwendung, die unter MS-DOS ausgeführt wird. Sie wird an der Vorderseite des exe-Bilds platziert. Der Linker platziert hier einen standardstub, der die Meldung "dieses Programm kann nicht im DOS-Modus ausgeführt werden" ausgibt, wenn das Image in MS-DOS ausgeführt wird. Der Benutzer kann mithilfe der Option/Stub Linker einen anderen Stub angeben.

An Speicherort 0x3C hat der Stub den Dateioffset für die PE-Signatur. Diese Informationen ermöglichen es Windows, die Bilddatei ordnungsgemäß auszuführen, auch wenn Sie über einen MS-DOS-Stub verfügt. Dieser Dateioffset wird bei der Verknüpfung an Speicherort 0x3C platziert.

### <a name="signature-image-only"></a>Signatur (nur Bild)

Nach dem MS-DOS-Stub ist die unter Offset 0x3C angegebene Dateioffset eine 4-Byte-Signatur, die die Datei als Bilddatei im PE-Format identifiziert. Diese Signatur ist "PE \\ 0 \\ 0" (Buchstaben "P" und "E", gefolgt von zwei NULL-Bytes).

### <a name="coff-file-header-object-and-image"></a>COFF-Datei Header (Objekt und Bild)

Am Anfang einer Objektdatei oder unmittelbar nach der Signatur einer Bilddatei ist ein standardmäßiger COFF-Dateiheader im folgenden Format. Beachten Sie, dass das Windows-Lade Modul die Anzahl von Abschnitten auf 96 beschränkt.

| Offset         | Size          | Feld                            | BESCHREIBUNG                                                                                                                                                                                                                                                          |
|----------------|---------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/> | Machine <br/>              | Die Zahl, die den Typ des Ziel Computers angibt. Weitere Informationen finden Sie unter [Computertypen](#machine-types). <br/>                                                                                                                                        |
| 2 <br/>  | 2 <br/> | Anzahl der Abschnitte <br/>     | Die Anzahl der Abschnitte. Dies gibt die Größe der Abschnittstabelle an, die unmittelbar auf die Header folgt. <br/>                                                                                                                                             |
| 4 <br/>  | 4 <br/> | TimeDateStamp <br/>        | Die unteren 32 Bits der Anzahl der Sekunden 00:00 seit dem 1. Januar 1970 (einem C-Lauf Zeit \_ Wert), der angibt, wann die Datei erstellt wurde. <br/>                                                                                                             |
| 8 <br/>  | 4 <br/> | Pointertopsymboltable <br/> | Der Dateioffset der COFF-Symboltabelle oder 0 (null), wenn keine COFF-Symboltabelle vorhanden ist. Dieser Wert sollte für ein Bild 0 (null) sein, da COFF-Debuginformationen veraltet sind. <br/>                                                                           |
| 12 <br/> | 4 <br/> | Anzahl von Symbolen <br/>      | Die Anzahl der Einträge in der Symboltabelle. Diese Daten können verwendet werden, um die Zeichenfolgentabelle zu suchen, die unmittelbar auf die Symboltabelle folgt. Dieser Wert sollte für ein Bild 0 (null) sein, da COFF-Debuginformationen veraltet sind. <br/>                        |
| 16 <br/> | 2 <br/> | Sizeofoptionalheader <br/> | Die Größe des optionalen Headers, der für ausführbare Dateien, jedoch nicht für Objektdateien erforderlich ist. Dieser Wert sollte für eine Objektdatei NULL sein. Eine Beschreibung des Header Formats finden Sie unter [optionaler Header (nur Bild)](#optional-header-image-only). <br/> |
| 18 <br/> | 2 <br/> | Merkmale <br/>      | Die Flags, die die Attribute der Datei angeben. Informationen zu bestimmten Flagwerten finden Sie unter [Merkmale](#characteristics). <br/>                                                                                                                               |

#### <a name="machine-types"></a>Computertypen

Das Feldcomputer hat einen der folgenden Werte, mit denen der CPU-Typ angegeben wird. Eine Bilddatei kann nur auf dem angegebenen Computer oder auf einem System ausgeführt werden, das den angegebenen Computer emuliert.

| Konstante                                    | Wert              | BESCHREIBUNG                                                                             |
|---------------------------------------------|--------------------|-----------------------------------------------------------------------------------------|
| Bild \_ Datei \_ Computer \_ unbekannt <br/>   | 0x0 <br/>    | Es wird davon ausgegangen, dass der Inhalt dieses Felds auf jeden Computertyp anwendbar ist. <br/> |
| Image \_ Datei \_ Computer \_ AM33 <br/>      | 0x1d3 <br/>  | Matsushita AM33 <br/>                                                             |
| Bild \_ Datei \_ Computer \_ amd64 <br/>     | 0x8664 <br/> | x64 <br/>                                                                         |
| Bild \_ Datei \_ Computer- \_ Arm <br/>       | 0x1c0 <br/>  | Arm-Little-Endian <br/>                                                           |
| Image \_ Datei \_ Computer \_ ARM64 <br/>     | 0xaa64 <br/> | ARM64 Little-umdian <br/>                                                         |
| Bilddatei- \_ \_ Computer \_ armnt <br/>     | 0x1c4 <br/>  | Arm Thumb-2 Little Endian <br/>                                                   |
| Image \_ Datei \_ Computer \_ EBC <br/>       | 0xebc <br/>  | EFI-Bytecode <br/>                                                               |
| Bild \_ Datei \_ Computer \_ i386 <br/>      | 0x14c <br/>  | Prozessoren mit Intel 386 oder höher und kompatible Prozessoren <br/>                     |
| Bild \_ Datei \_ Computer \_ ia64 <br/>      | 0x200 <br/>  | Intel Itanium-Prozessorfamilie <br/>                                              |
| Image \_ Datei \_ Computer \_ M32R <br/>      | 0x9041 <br/> | Mitsubishi M32R Little-in-Dian <br/>                                               |
| Image \_ Datei \_ Computer \_ MIPS16 <br/>    | 0x266 <br/>  | MIPS16 <br/>                                                                      |
| Bild \_ Datei \_ Computer \_ mipsfpu <br/>   | 0x366 <br/>  | MIPS mit "f" <br/>                                                               |
| Image \_ Datei \_ Computer \_ MIPSFPU16 <br/> | 0x466 <br/>  | MIPS16 mit "f" <br/>                                                             |
| Bild \_ Datei \_ Computer \_ powerpc <br/>   | 0x1F 0 <br/>  | Power PC Little-Endian <br/>                                                      |
| Image \_ Datei \_ Computer- \_ powerpcfp <br/> | 0x1F 1 <br/>  | Power PC mit Gleit Komma Unterstützung <br/>                                        |
| Image \_ Datei \_ Computer \_ R4000 <br/>     | 0x166 <br/>  | MIPS Little-umdian <br/>                                                          |
| Image \_ Datei \_ Computer \_ RISCV32 <br/>   | 0x5032 <br/> | RISC-V 32-Bit-Adressraum <br/>                                                 |
| Image \_ Datei \_ Computer \_ RISCV64 <br/>   | 0x5064 <br/> | RISC-V 64-Bit-Adressraum <br/>                                                 |
| Image \_ Datei \_ Computer \_ RISCV128 <br/>  | 0x5128 <br/> | RISC-V 128-Bit-Adressraum <br/>                                                |
| Image \_ Datei \_ Computer \_ SH3 <br/>       | 0x1a2 <br/>  | Hitachi SH3 <br/>                                                                 |
| Image \_ Datei \_ Computer \_ SH3DSP <br/>    | 0x1a3 <br/>  | Hitachi SH3 DSP <br/>                                                             |
| Image \_ Datei \_ Computer \_ SH4 <br/>       | 0x1a6 <br/>  | Hitachi SH4 <br/>                                                                 |
| Image \_ Datei \_ Computer \_ SH5 <br/>       | 0x1a8 <br/>  | Hitachi SH5 <br/>                                                                 |
| Ziehpunkt für Bild \_ Datei \_ Computer \_ <br/>     | 0x1c2 <br/>  | Ziehpunkt <br/>                                                                       |
| Image \_ Datei \_ Computer \_ WCEMIPSV2 <br/> | 0x169 <br/>  | MIPS Little-in WCE v2 <br/>                                                   |

#### <a name="characteristics"></a>Merkmale

Das Feld "Merkmale" enthält Flags, die auf Attribute der Objekt-oder Bilddatei hinweisen. Die folgenden Flags sind aktuell definiert:

| Flag                                                 | Wert              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abbild \_ Datei- \_ relocs entfernt \_ <br/>            | 0x0001 <br/> | Nur Image, Windows CE und Microsoft Windows NT und höher. Dies gibt an, dass die Datei keine Basis Umsetzungen enthält und daher an der bevorzugten Basisadresse geladen werden muss. Wenn die Basisadresse nicht verfügbar ist, meldet das Lade Modul einen Fehler. Das Standardverhalten des Linker besteht darin, Basis Umsetzungen aus ausführbaren Dateien (exe-Dateien) zu entfernen. <br/> |
| Image \_ Datei \_ ausführbares \_ Image <br/>           | 0x0002 <br/> | Nur Bild. Dies gibt an, dass die Bilddatei gültig ist und ausgeführt werden kann. Wenn dieses Flag nicht festgelegt ist, weist dies auf einen Linkerfehler hin. <br/>                                                                                                                                                                                                                          |
| Bilddatei- \_ \_ Zeilen- \_ nums entfernt \_ <br/>        | 0x0004 <br/> | COFF-Zeilennummern wurden entfernt. Dieses Flag ist veraltet und sollte NULL sein. <br/>                                                                                                                                                                                                                                                                       |
| \_ \_ lokale \_ Syms der Bilddatei wurden entfernt. \_ <br/>       | 0x0008 <br/> | COFF-Symboltabellen Einträge für lokale Symbole wurden entfernt. Dieses Flag ist veraltet und sollte NULL sein. <br/>                                                                                                                                                                                                                                             |
| \_Bilddatei \_ aggressive \_ WS- \_ Trim <br/>        | 0x0010 <br/> | Veraltet. Arbeits Satz aggressiv kürzen. Dieses Flag ist für Windows 2000 und höher veraltet und muss NULL sein. <br/>                                                                                                                                                                                                                                          |
| Bild \_ Datei mit \_ hoher \_ Adresse \_ <br/>      | 0x0020 <br/> | Die Anwendung kann > 2-GB-Adressen verarbeiten. <br/>                                                                                                                                                                                                                                                                                                            |
|                                                      | 0x0040 <br/> | Dieses Flag ist für die zukünftige Verwendung reserviert. <br/>                                                                                                                                                                                                                                                                                                                  |
| Bilddatei ( \_ \_ Bytes) \_ umgekehrt \_ <br/>         | 0x0080 <br/> | Little Endian: das am wenigsten bedeutende Bit (LSB) liegt vor dem signifikantesten Bit (MSB) im Arbeitsspeicher. Dieses Flag ist veraltet und sollte NULL sein. <br/>                                                                                                                                                                                                          |
| Bild \_ Datei- \_ 32-Bit- \_ Computer <br/>              | 0x0100 <br/> | Der computerbasiert auf einer 32-Bit-Word-Architektur. <br/>                                                                                                                                                                                                                                                                                                        |
| \_Bilddatei \_ Debuggen entfernt \_ <br/>             | 0x0200 <br/> | Debuginformationen werden aus der Bilddatei entfernt. <br/>                                                                                                                                                                                                                                                                                                  |
| \_Wechsel zum \_ Wechsel von Bilddatei \_ \_ aus \_ Swap <br/> | 0x0400 <br/> | Wenn sich das Bild auf einem Wechselmedium befindet, laden Sie es vollständig, und kopieren Sie es in die Auslagerungs Datei. <br/>                                                                                                                                                                                                                                                                        |
| \_Bilddatei \_ net \_ Run \_ from \_ Swap <br/>        | 0x0800 <br/> | Wenn sich das Image auf dem Netzwerk Medium befindet, laden Sie es vollständig, und kopieren Sie es in die Auslagerungs Datei. <br/>                                                                                                                                                                                                                                                                          |
| Bild \_ Datei \_ System <br/>                      | 0x1000 <br/> | Die Bilddatei ist eine Systemdatei, kein Benutzerprogramm. <br/>                                                                                                                                                                                                                                                                                                   |
| Bilddatei- \_ \_ dll <br/>                         | 0x2000 <br/> | Die Bilddatei ist eine Dynamic Link Library (dll). Solche Dateien werden für fast alle Zwecke als ausführbare Dateien betrachtet, Sie können jedoch nicht direkt ausgeführt werden. <br/>                                                                                                                                                                                              |
| \_nur Bild \_ Datei \_ System \_ <br/>            | 0x4000 <br/> | Die Datei sollte nur auf einem Uniprozessor-Computer ausgeführt werden. <br/>                                                                                                                                                                                                                                                                                                 |
| Bilddatei- \_ \_ Bytes \_ umgekehrt \_ <br/>         | 0x8000 <br/> | Big-erdian: der MSB geht vor dem LSB im Speicher. Dieses Flag ist veraltet und sollte NULL sein. <br/>                                                                                                                                                                                                                                                            |

### <a name="optional-header-image-only"></a>Optionaler Header (nur Bild)

Jede Bilddatei verfügt über einen optionalen Header, der Informationen für das Lade Modul bereitstellt. Dieser Header ist in dem Sinne, dass einige Dateien (insbesondere Objektdateien) nicht vorhanden sind, optional. Für Bilddateien ist dieser Header erforderlich. Eine Objektdatei kann über einen optionalen Header verfügen, aber in der Regel besitzt dieser Header keine Funktion in einer Objektdatei, außer um seine Größe zu erhöhen.

Beachten Sie, dass die Größe des optionalen-Headers nicht fest ist. Das **sizeofoptionalheader** -Feld im COFF-Header muss verwendet werden, um zu überprüfen, ob ein Test in die Datei für ein bestimmtes Datenverzeichnis nicht über **sizeofoptionalheader** hinausgeht. Weitere Informationen finden Sie unter [COFF-Datei Header (Objekt und Image)](#coff-file-header-object-and-image).

Das Feld " **numofrvaandsizes** " des optionalen Headers sollte auch verwendet werden, um sicherzustellen, dass kein Test für einen bestimmten Datenverzeichnis Eintrag den optionalen Header überschreitet. Außerdem ist es wichtig, die optionale Header-Magic-Nummer für die Format Kompatibilität zu überprüfen.

Die optionale Header-Magic Number bestimmt, ob ein Bild eine ausführbare Datei mit das Format PE32 oder das Format PE32 ist.

| Magische Zahl      | PE-Format         |
|-------------------|-------------------|
| 0x10b <br/> | Das Format PE32 <br/>  |
| 0x20b <br/> | Das Format PE32 + <br/> |

Das Format PE32 + Images ermöglichen einen 64-Bit-Adressraum, während die Bildgröße auf 2 Gigabyte beschränkt wird. Andere das Format PE32 +-Änderungen werden in den jeweiligen Abschnitten behandelt.

Der optionale Header selbst hat drei Hauptbestandteile.

| Offset (das Format PE32/das Format PE32 +) | Größe (das Format PE32/das Format PE32 +)    | Kopfteil                         | BESCHREIBUNG                                                                                                                                                                   |
|---------------------|----------------------|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>       | 28/24 <br/>    | Standardfelder <br/>         | Felder, die für alle Implementierungen von COFF definiert sind, einschließlich UNIX. <br/>                                                                                          |
| 28/24 <br/>   | 68/88 <br/>    | Windows-spezifische Felder <br/> | Zusätzliche Felder zur Unterstützung bestimmter Features von Windows (z. b. Subsysteme). <br/>                                                                              |
| 96/112 <br/>  | Variable <br/> | Datenverzeichnisse <br/>        | Adress-/größenpaare für spezielle Tabellen, die in der Bilddatei gefunden werden und vom Betriebssystem verwendet werden (z. b. die Import-und Export Tabelle). <br/> |

#### <a name="optional-header-standard-fields-image-only"></a>Optionale Header Standard Felder (nur Bild)

Die ersten acht Felder des optionalen Headers sind Standard Felder, die für jede Implementierung von COFF definiert werden. Diese Felder enthalten allgemeine Informationen, die beim Laden und Ausführen einer ausführbaren Datei nützlich sind. Sie sind für das das Format PE32 +-Format unverändert.

| Offset         | Size          | Feld                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                   |
|----------------|---------------|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/> | Magic <br/>                   | Die Ganzzahl ohne Vorzeichen, die den Status der Bilddatei identifiziert. Die häufigste Zahl ist 0x10b, die ihn als normale ausführbare Datei identifiziert. 0x107 identifiziert ihn als Rom-Bild, und 0x20b identifiziert ihn als eine ausführbare Datei mit das Format PE32 und höher. <br/>                                                                                            |
| 2 <br/>  | 1 <br/> | Majorlinkerversion <br/>      | Die Hauptversionsnummer des Linker. <br/>                                                                                                                                                                                                                                                                                                  |
| 3 <br/>  | 1 <br/> | Minorlinkerversion <br/>      | Die Nebenversionsnummer des Linker. <br/>                                                                                                                                                                                                                                                                                                  |
| 4 <br/>  | 4 <br/> | Sizeofcode <br/>              | Die Größe des Code Abschnitts (Text) oder die Summe aller Code Abschnitte, wenn mehrere Abschnitte vorhanden sind. <br/>                                                                                                                                                                                                                              |
| 8 <br/>  | 4 <br/> | Sizeofinitializeddata <br/>   | Die Größe des Abschnitts mit den initialisierten Daten oder die Summe aller dieser Abschnitte, wenn mehrere Datenabschnitte vorhanden sind. <br/>                                                                                                                                                                                                                    |
| 12 <br/> | 4 <br/> | Sizeofuninitializeddata <br/> | Die Größe des nicht initialisierten Daten Abschnitts (BSS) oder die Summe aller dieser Abschnitte, wenn mehrere BSS-Abschnitte vorhanden sind. <br/>                                                                                                                                                                                                             |
| 16 <br/> | 4 <br/> | Addressofentrypoint <br/>     | Die Adresse des Einstiegs Punkts, der relativ zur Bildbasis ist, wenn die ausführbare Datei in den Arbeitsspeicher geladen wird. Bei Programm Images ist dies die Startadresse. Für Gerätetreiber ist dies die Adresse der Initialisierungsfunktion. Ein Einstiegspunkt ist für DLLs optional. Wenn kein Einstiegspunkt vorhanden ist, muss dieses Feld NULL sein. <br/> |
| 20 <br/> | 4 <br/> | Baseof Code <br/>              | Die Adresse, die relativ zur bildintebene des Anfangs-von-Code-Abschnitts ist, wenn Sie in den Arbeitsspeicher geladen wird. <br/>                                                                                                                                                                                                                    |

Das Format PE32 enthält dieses zusätzliche Feld, das in das Format PE32 + fehlt, nach baseobcode.

| Offset         | Size          | Feld                  | BESCHREIBUNG                                                                                                                |
|----------------|---------------|------------------------|----------------------------------------------------------------------------------------------------------------------------|
| 24 <br/> | 4 <br/> | Baseof-Daten <br/> | Die-Adresse, die relativ zur bildintebene des Anfangsdaten Abschnitts ist, wenn Sie in den Arbeitsspeicher geladen wird. <br/> |

#### <a name="optional-header-windows-specific-fields-image-only"></a>Optionale Header Windows-Specific Felder (nur Bild)

Die nächsten 21 Felder sind eine Erweiterung des optionalen COFF-Header Formats. Sie enthalten zusätzliche Informationen, die für den Linker und das Lade Tool in Windows erforderlich sind.

| Offset (das Format PE32/das Format PE32 +) | Größe (das Format PE32/das Format PE32 +) | Feld                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                            |
|----------------------|--------------------|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 28/24 <br/>    | 4/8 <br/>    | ImageBase <br/>                   | Die bevorzugte Adresse des ersten Bytes des Bilds beim Laden in den Arbeitsspeicher. muss ein Vielfaches von 64 KB sein. Der Standardwert für DLLs ist 0x10000000. Der Standardwert für Windows CE-exe-Datei ist 0x00010000 bis. Der Standardwert für Windows NT, Windows 2000, Windows XP, Windows 95, Windows 98 und Windows Me ist 0x00400000. <br/>       |
| 32/32 <br/>    | 4 <br/>      | SectionAlignment <br/>            | Die Ausrichtung (in Bytes) von Abschnitten beim Laden in den Arbeitsspeicher. Der Wert muss größer als oder gleich "FileAlignment" sein. Der Standard für die Architektur ist die Seitengröße. <br/>                                                                                                                               |
| 36/36 <br/>    | 4 <br/>      | FileAlignment <br/>               | Der Ausrichtungsfaktor (in Byte), der verwendet wird, um die Rohdaten von Abschnitten in der Imagedatei auszurichten. Der Wert muss eine Potenz von 2 zwischen 512 und 64 K (einschließlich) sein. Der Standardwert liegt bei 512. Wenn ' sectionalignment ' kleiner ist als die Seitengröße der Architektur, muss ' FileAlignment ' mit ' sectionalignment ' übereinstimmen. <br/> |
| 40/40 <br/>    | 2 <br/>      | Majoroperatingsystemversion <br/> | Die Hauptversionsnummer des erforderlichen Betriebssystems. <br/>                                                                                                                                                                                                                                                 |
| 42/42 <br/>    | 2 <br/>      | Minoroperatingsystemversion <br/> | Die Nebenversionsnummer des erforderlichen Betriebssystems. <br/>                                                                                                                                                                                                                                                 |
| 44/44 <br/>    | 2 <br/>      | Majorimageversion <br/>           | Die Hauptversionsnummer des Images. <br/>                                                                                                                                                                                                                                                                     |
| 46/46 <br/>    | 2 <br/>      | Minorimageversion <br/>           | Die Nebenversionsnummer des Images. <br/>                                                                                                                                                                                                                                                                     |
| 48/48 <br/>    | 2 <br/>      | Majorsubsystemversion <br/>       | Die Hauptversionsnummer des Subsystems. <br/>                                                                                                                                                                                                                                                                 |
| 50/50 <br/>    | 2 <br/>      | Minorsubsystemversion <br/>       | Die Nebenversionsnummer des Subsystems. <br/>                                                                                                                                                                                                                                                                 |
| 52/52 <br/>    | 4 <br/>      | Win32VersionValue <br/>           | Reserviert, muss NULL sein. <br/>                                                                                                                                                                                                                                                                                    |
| 56/56 <br/>    | 4 <br/>      | Sizeofmage <br/>                 | Die Größe (in Bytes) des Bilds, einschließlich aller Header, während das Bild in den Arbeitsspeicher geladen wird. Es muss ein Vielfaches von "sectionalignment" sein. <br/>                                                                                                                                                                      |
| 60/60 <br/>    | 4 <br/>      | Sizeofheaders <br/>               | Die kombinierte Größe eines MS-DOS-Stubs, PE-Headers und von Abschnitts Headern, die auf ein Vielfaches von FileAlignment aufgerundet werden. <br/>                                                                                                                                                                                             |
| 64/64 <br/>    | 4 <br/>      | Prüfsumme <br/>                    | Die Prüfsumme der Bilddatei. Der Algorithmus zum Berechnen der Prüfsumme ist in IMAGHELP.DLL integriert. Folgendes wird zur Überprüfung zur Ladezeit überprüft: alle Treiber, alle zum Startzeitpunkt geladenen DLLs und alle dll-Informationen, die in einen kritischen Windows-Prozess geladen werden. <br/>                                          |
| 68/68 <br/>    | 2 <br/>      | Subsystem <br/>                   | Das Subsystem, das zum Ausführen dieses Images erforderlich ist. Weitere Informationen finden Sie unter [Windows-Subsystem](#windows-subsystem). <br/>                                                                                                                                                                                       |
| 70/70 <br/>    | 2 <br/>      | DllCharacteristics <br/>          | Weitere Informationen finden Sie unter [dll-Merkmale](#dll-characteristics) weiter unten in dieser Spezifikation. <br/>                                                                                                                                                                                                         |
| 72/72 <br/>    | 4/8 <br/>    | SizeOfStackReserve <br/>          | Die Größe des Stapels, der reserviert werden soll. Nur für sizeofstackcommit wird ein Commit ausgeführt. der Rest wird eine Seite zu einem Zeitpunkt verfügbar gemacht, bis die Reserve Größe erreicht ist. <br/>                                                                                                                                                    |
| 76/80 <br/>    | 4/8 <br/>    | Sizeofstackcommit <br/>           | Dier Größe des Stapels, für den ein Commit ausgeführt wird. <br/>                                                                                                                                                                                                                                                                           |
| 80/88 <br/>    | 4/8 <br/>    | Sizeofheapreserve <br/>           | Die Größe des Speicherplatzes für den lokalen Heap, der reserviert werden soll. Für "sizeofheapcommit" wird nur ein Commit ausgeführt. der Rest wird eine Seite zu einem Zeitpunkt verfügbar gemacht, bis die Reserve Größe erreicht ist. <br/>                                                                                                                                          |
| 84/96 <br/>    | 4/8 <br/>    | Sizeofheapcommit <br/>            | Die Größe des Speicherplatzes für den lokalen Heap, für den ein Commit ausgeführt werden soll. <br/>                                                                                                                                                                                                                                                                |
| 88/104 <br/>   | 4 <br/>      | Loaderflags <br/>                 | Reserviert, muss NULL sein. <br/>                                                                                                                                                                                                                                                                                    |
| 92/108 <br/>   | 4 <br/>      | Nummeriofrvaandsizes <br/>         | Die Anzahl der Datenverzeichnis Einträge im Rest des optionalen Headers. Jeder beschreibt einen Speicherort und eine Größe. <br/>                                                                                                                                                                                          |

##### <a name="windows-subsystem"></a>Windows-Subsystem

Die folgenden Werte, die für das Subsystem-Feld des optionalen-Headers definiert sind, legen fest, welches Windows-Subsystem (sofern vorhanden) zum Ausführen des Bilds erforderlich ist.

| Konstante                                                  | Wert          | BESCHREIBUNG                                                      |
|-----------------------------------------------------------|----------------|------------------------------------------------------------------|
| Image \_ Subsystem \_ Unknown <br/>                     | 0 <br/>  | Ein unbekanntes Subsystem <br/>                                 |
| Image \_ Subsystem \_ Native <br/>                      | 1 <br/>  | Gerätetreiber und systemeigene Windows-Prozesse <br/>          |
| Bild \_ Subsystem \_ Windows- \_ GUI <br/>                | 2 <br/>  | Das GUI-Subsystem (Graphical User Interface) von Windows <br/> |
| Bild \_ Subsystem \_ Windows \_ Cui <br/>                | 3 <br/>  | Das Windows-Zeichen Subsystem <br/>                      |
| Image \_ Subsystem \_ OS2 \_ Cui <br/>                    | 5 <br/>  | Das OS/2-Zeichen Subsystem <br/>                         |
| Image \_ Subsystem \_ POSIX \_ Cui <br/>                  | 7 <br/>  | Das POSIX-Zeichen Subsystem <br/>                        |
| \_ \_ native \_ Windows-Abbild Subsystem <br/>             | 8 <br/>  | Native Win9x-Treiber <br/>                                  |
| Bild \_ Subsystem \_ Windows \_ CE \_ GUI <br/>            | 9 <br/>  | Windows CE <br/>                                           |
| \_ \_ EFI-Anwendung des Image Subsystems \_ <br/>            | 10 <br/> | Eine Extensible Firmware Interface-Anwendung (EFI) <br/>   |
| Image- \_ Subsystem \_ EFI- \_ Start \_ Dienst \_ Treiber <br/> | 11 <br/> | Einen EFI-Treiber mit Start Diensten <br/>                     |
| \_ \_ EFI- \_ Lauf Zeit \_ Treiber für Image Subsystem <br/>       | 12 <br/> | Einen EFI-Treiber mit Lauf Zeit Diensten <br/>                 |
| Image \_ Subsystem \_ EFI \_ Rom <br/>                    | 13 <br/> | Ein EFI-ROM-Image <br/>                                     |
| Bild \_ Subsystem \_ Xbox <br/>                        | 14 <br/> | XBOX <br/>                                                 |
| Image- \_ Subsystem \_ Windows- \_ Start \_ Anwendung <br/>  | 16 <br/> | Windows-Start Anwendung. <br/>                            |

##### <a name="dll-characteristics"></a>DLL-Merkmale

Die folgenden Werte werden für das DllCharacteristics-Feld des optionalen-Headers definiert.

| Konstante                                                             | Wert              | BESCHREIBUNG                                                                                             |
|----------------------------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------|
|                                                                      | 0x0001 <br/> | Reserviert, muss NULL sein. <br/>                                                                     |
|                                                                      | 0x0002 <br/> | Reserviert, muss NULL sein. <br/>                                                                     |
|                                                                      | 0x0004 <br/> | Reserviert, muss NULL sein. <br/>                                                                     |
|                                                                      | 0x0008 <br/> | Reserviert, muss NULL sein. <br/>                                                                     |
| Image- \_ dllcharakteristika, \_ hohe \_ Entropie \_ VA <br/>             | 0x0020 <br/> | Image kann eine hoch Entropie 64-Bit-virtuellem Adressraum verarbeiten. <br/>                               |
| Image- \_ DllCharacteristics\_ <br/> dynamische \_ Basis <br/>    | 0x0040 <br/> | DLL kann zur Ladezeit verschoben werden. <br/>                                                          |
| Image- \_ DllCharacteristics\_ <br/> Erzwingen der \_ Integrität <br/> | 0x0080 <br/> | Code Integritätsprüfungen werden erzwungen. <br/>                                                         |
| Image- \_ DllCharacteristics\_ <br/> NX- \_ Kompatibilität <br/>       | 0x0100 <br/> | Das Image ist mit NX kompatibel. <br/>                                                                     |
| Image- \_ dllcharakteristika \_ keine \_ Isolation <br/>                | 0x0200 <br/> | Isolation wird unterstützt, aber das Bild wird nicht isoliert. <br/>                                              |
| Image- \_ dllcharakteristika \_ nicht \_ Seh <br/>                      | 0x0400 <br/> | Verwendet keine strukturierte Ausnahmebehandlung (SE). In diesem Bild kann kein SE-Handler aufgerufen werden. <br/> |
| Image- \_ dllcharakteristika \_ keine \_ Bindung <br/>                     | 0x0800 <br/> | Binden Sie das Bild nicht. <br/>                                                                      |
| Image- \_ dllcharakteristika \_ appcontainer <br/>                  | 0x1000 <br/> | Das Image muss in einem appcontainer ausgeführt werden. <br/>                                                      |
| Image- \_ DllCharacteristics- \_ WDM- \_ Treiber <br/>                  | 0x2000 <br/> | Ein WDM-Treiber. <br/>                                                                               |
| Abbildung \_ DllCharacteristics \_ Guard \_ CF <br/>                     | 0x4000 <br/> | Image unterstützt den Ablauf Steuerungs Schutz. <br/>                                                          |
| Image- \_ dllcharakteristika- \_ Terminal \_ Server \_ fähig <br/>      | 0x8000 <br/> | Terminal Server fähig. <br/>                                                                      |

#### <a name="optional-header-data-directories-image-only"></a>Optionale Header Datenverzeichnisse (nur Bild)

Jedes Datenverzeichnis gibt die Adresse und Größe einer Tabelle oder Zeichenfolge an, die von Windows verwendet wird. Diese Datenverzeichnis Einträge werden alle in den Arbeitsspeicher geladen, sodass Sie vom System zur Laufzeit verwendet werden können. Ein Datenverzeichnis ist ein 8-Byte-Feld mit der folgenden Deklaration:

```cpp
typedef struct _IMAGE_DATA_DIRECTORY {
    DWORD   VirtualAddress;
    DWORD   Size;
} IMAGE_DATA_DIRECTORY, *PIMAGE_DATA_DIRECTORY;
```

Das erste Feld, virtualAddress, ist tatsächlich die RVA der Tabelle. Bei der RVA handelt es sich um die Adresse der Tabelle relativ zur Basisadresse des Bilds, wenn die Tabelle geladen wird. Das zweite Feld gibt die Größe in Bytes an. Die Datenverzeichnisse, die den letzten Teil des optionalen Headers bilden, sind in der folgenden Tabelle aufgeführt.

Beachten Sie, dass die Anzahl der Verzeichnisse nicht korrigiert ist. Bevor Sie nach einem bestimmten Verzeichnis suchen, überprüfen Sie das Feld "numofrvaandsizes" im optionalen Header.

Nehmen Sie außerdem nicht an, dass die RVAs in dieser Tabelle auf den Anfang eines Abschnitts verweisen oder dass die Abschnitte, die bestimmte Tabellen enthalten, bestimmte Namen aufweisen.

| Offset (PE/das Format PE32 +)   | Size          | Feld                               | BESCHREIBUNG                                                                                                                                                                          |
|---------------------|---------------|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 96/112 <br/>  | 8 <br/> | Tabelle exportieren <br/>            | Die Adresse und Größe der Export Tabelle. Weitere Informationen finden Sie im [Abschnitt ". edata" (nur Bild)](#the-edata-section-image-only). <br/>                                                |
| 104/120 <br/> | 8 <br/> | Tabelle importieren <br/>            | Die Adresse und Größe der Import Tabelle. Weitere Informationen finden Sie [im Abschnitt. iData](#the-idata-section).<br/>                                                                    |
| 112/128 <br/> | 8 <br/> | Ressourcen Tabelle <br/>          | Die Adresse und Größe der Ressourcen Tabelle. Weitere Informationen finden Sie [im Abschnitt. rsrc](#the-rsrc-section).<br/>                                                                    |
| 120/136 <br/> | 8 <br/> | Ausnahme Tabelle <br/>         | Die Adresse und Größe der Ausnahme Tabelle. Weitere Informationen finden Sie [im Abschnitt. pdata](#the-pdata-section). <br/>                                                                |
| 128/144 <br/> | 8 <br/> | Zertifikat Tabelle <br/>       | Die Adresse und Größe der Attribut Zertifikat Tabelle. Weitere Informationen finden Sie in [der Attribut Zertifikat Tabelle (nur Image)](#the-attribute-certificate-table-image-only). <br/> |
| 136/152 <br/> | 8 <br/> | Basis Verschiebungs Tabelle <br/>   | Die Adresse und Größe der Basis Verschiebungs Tabelle. Weitere Informationen finden Sie [im Abschnitt ". reloc" (nur Image)](#the-reloc-section-image-only).<br/>                                   |
| 144/160 <br/> | 8 <br/> | Debug <br/>                   | Die Startadresse und-Größe der Debugdaten. Weitere Informationen finden Sie [im Abschnitt zum Debuggen](#the-debug-section).<br/>                                                             |
| 152/168 <br/> | 8 <br/> | Architektur <br/>            | Reserviert, muss 0 sein. <br/>                                                                                                                                                      |
| 160/176 <br/> | 8 <br/> | Globaler PTR <br/>              | Die RVA des Werts, der im globalen Zeiger Register gespeichert werden soll. Der Size-Member dieser-Struktur muss auf 0 (null) festgelegt werden. <br/>                                                 |
| 168/184 <br/> | 8 <br/> | TLS-Tabelle <br/>               | Die TLS-Tabellen Adresse (Thread Local Storage) und die Größe. Weitere Informationen finden Sie [im Abschnitt. TLS](#the-tls-section).<br/>                                                        |
| 176/192 <br/> | 8 <br/> | Konfigurations Tabelle laden <br/>       | Die Adresse und Größe der Lade Konfigurations Tabelle. Weitere Informationen finden Sie in [der Struktur der Lade Konfiguration (nur Bild)](#the-load-configuration-structure-image-only).<br/>       |
| 184/200 <br/> | 8 <br/> | Gebundener Import <br/>            | Die Adresse und Größe der gebundenen Import Tabelle. <br/>                                                                                                                                 |
| 192/208 <br/> | 8 <br/> | IAT <br/>                     | Die Adresse und Größe der Import Adress Tabelle. Weitere Informationen finden Sie unter [Import Address Table](#import-address-table).<br/>                                                 |
| 200/216 <br/> | 8 <br/> | Import Deskriptor verzögern <br/> | Die Adresse und Größe des verzögerten Import Deskriptors. Weitere Informationen finden Sie unter [Verzögertes Laden von Import Tabellen (nur Image)](#delay-load-import-tables-image-only).<br/>                    |
| 208/224 <br/> | 8 <br/> | CLR-Lauf Zeit Header <br/>      | Die CLR-Lauf Zeit Header Adresse und-Größe. Weitere Informationen finden Sie [im Abschnitt ". cormeta" (nur Objekt)](#the-cormeta-section-object-only).<br/>                                |
| 216/232 <br/> | 8 <br/> | Reserviert, muss NULL sein. <br/>  |                                                                                                                                                                                      |

Der Eintrag für die Zertifikat Tabelle verweist auf eine Tabelle mit Attribut Zertifikaten. Diese Zertifikate werden nicht als Teil des Abbilds in den Arbeitsspeicher geladen. Daher ist das erste Feld dieses Eintrags, bei dem es sich normalerweise um eine RVA handelt, stattdessen ein Dateizeiger.

## <a name="section-table-section-headers"></a>Abschnitts Tabelle (Abschnitts Header)

- [Abschnitts-Flags](#section-flags)
- [Gruppierte Abschnitte (nur Objekt)](#grouped-sections-object-only)

Jede Zeile der Abschnitts Tabelle ist tatsächlich ein Abschnitts Header. Diese Tabelle folgt unmittelbar auf den optionalen Header, falls vorhanden. Diese Positionierung ist erforderlich, da der Dateiheader keinen direkten Zeiger auf die Abschnitts Tabelle enthält. Stattdessen wird der Speicherort der Abschnitts Tabelle festgelegt, indem der Speicherort des ersten Bytes nach den Headern berechnet wird. Stellen Sie sicher, dass Sie die Größe des optionalen Headers verwenden, wie im Dateiheader angegeben.

Die Anzahl der Einträge in der Abschnitts Tabelle wird durch das Feld "nummeriofsection" in der Datei Kopfzeile angegeben. Einträge in der Abschnitts Tabelle sind beginnend mit eins (1) nummeriert. Die Einträge für den Code-und Datenspeicherbereich befinden sich in der vom Linker ausgewählten Reihenfolge.

In einer Bilddatei müssen die VAS für Abschnitte durch den Linker zugewiesen werden, damit Sie in aufsteigender Reihenfolge und nebeneinander angeordnet sind, und Sie müssen ein Vielfaches des sectionalignment-Werts in der optionalen Kopfzeile sein.

Jeder Abschnitts Header (Abschnitts Tabelleneintrag) weist das folgende Format auf: insgesamt 40 Byte pro Eintrag.



| Offset         | Size          | Feld                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------|---------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 8 <br/> | Name <br/>                 | Eine mit NULL gefüllte UTF-8-codierte Zeichenfolge mit 8 Bytes. Wenn die Zeichenfolge genau 8 Zeichen lang ist, wird kein abschließendes NULL-Zeichen angezeigt. Für längere Namen enthält dieses Feld einen Schrägstrich (/), dem eine ASCII-Darstellung einer Dezimalzahl folgt, bei der es sich um einen Offset in der Zeichen folgen Tabelle handelt. Ausführbare Images verwenden keine Zeichen folgen Tabelle und unterstützen keine Abschnittsnamen, die länger als 8 Zeichen sind. Lange Namen in Objektdateien werden abgeschnitten, wenn Sie an eine ausführbare Datei ausgegeben werden. <br/>                                         |
| 8 <br/>  | 4 <br/> | VirtualSize <br/>          | Die Gesamtgröße des Abschnitts beim Laden in den Arbeitsspeicher. Wenn dieser Wert größer als sizeofrawdata ist, wird der Abschnitt mit 0 (null) aufgefüllt. Dieses Feld ist nur für ausführbare Images gültig und sollte für Objektdateien auf 0 (null) festgelegt werden. <br/>                                                                                                                                                                                                                                                                                           |
| 12 <br/> | 4 <br/> | VirtualAddress <br/>       | Bei ausführbaren Images die Adresse des ersten Byte des Abschnitts relativ zur Bildbasis, wenn der Abschnitt in den Arbeitsspeicher geladen wird. Bei Objektdateien ist dieses Feld die Adresse des ersten Bytes vor dem Anwenden der Verschiebung. der Einfachheit halber sollten Compiler diesen Wert auf 0 festlegen. Andernfalls handelt es sich um einen beliebigen Wert, der während der Verlagerung von Offsets subtrahiert wird. <br/>                                                                                                                                         |
| 16 <br/> | 4 <br/> | Sizeofrawdata <br/>        | Die Größe des Abschnitts (für Objektdateien) oder die Größe der initialisierten Daten auf dem Datenträger (für Bilddateien). Bei ausführbaren Images muss es sich um ein Vielfaches von FileAlignment aus dem optionalen Header handeln. Wenn dieser Wert kleiner als VirtualSize ist, wird der Rest des Abschnitts mit 0 (null) aufgefüllt. Da das sizeofrawdata-Feld gerundet ist, das Feld "VirtualSize" jedoch nicht ist, kann "sizeofrawdata" auch größer als "VirtualSize" sein. Wenn ein Abschnitt nur nicht initialisierte Daten enthält, muss dieses Feld den Wert 0 (null) aufweisen. <br/> |
| 20 <br/> | 4 <br/> | Pointertor awdata <br/>     | Der Dateizeiger auf die erste Seite des Abschnitts in der COFF-Datei. Bei ausführbaren Images muss es sich um ein Vielfaches von FileAlignment aus dem optionalen Header handeln. Bei Objektdateien sollte der Wert an einer 4-Byte-Grenze ausgerichtet werden, um eine optimale Leistung zu erzielen. Wenn ein Abschnitt nur nicht initialisierte Daten enthält, muss dieses Feld den Wert 0 (null) aufweisen. <br/>                                                                                                                                                                               |
| 24 <br/> | 4 <br/> | Pointertorielocations <br/> | Der Dateizeiger auf den Anfang der Verschiebungs Einträge für den Abschnitt. Dies wird für ausführbare Images auf 0 (null) festgelegt, oder wenn keine Umsetzungen vorhanden sind. <br/>                                                                                                                                                                                                                                                                                                                                                                   |
| 28 <br/> | 4 <br/> | Pointertolinenumbers <br/> | Der Dateizeiger auf den Anfang der Zeilennummern Einträge für den Abschnitt. Dieser Wert wird auf NULL festgelegt, wenn keine COFF-Zeilennummern vorhanden sind. Dieser Wert sollte für ein Bild 0 (null) sein, da COFF-Debuginformationen veraltet sind. <br/>                                                                                                                                                                                                                                                                                            |
| 32 <br/> | 2 <br/> | Numofrelocations <br/>  | Die Anzahl der Verschiebungs Einträge für den Abschnitt. Dies wird für ausführbare Images auf 0 (null) festgelegt. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 34 <br/> | 2 <br/> | Nummerioflinenumber <br/>  | Die Anzahl der Zeilennummern Einträge für den Abschnitt. Dieser Wert sollte für ein Bild 0 (null) sein, da COFF-Debuginformationen veraltet sind. <br/>                                                                                                                                                                                                                                                                                                                                                                          |
| 36 <br/> | 4 <br/> | Merkmale <br/>      | Die Flags, die die Merkmale des Abschnitts beschreiben. Weitere Informationen finden Sie unter [Abschnitts-Flags](#section-flags).<br/>                                                                                                                                                                                                                                                                                                                                                                                                |



 

### <a name="section-flags"></a>Abschnitts-Flags

Die Abschnitts-Flags im Feld Merkmale der Abschnitts Kopfzeile geben Merkmale des Abschnitts an.



| Flag                                              | Wert                  | BESCHREIBUNG                                                                                                                                                                 |
|---------------------------------------------------|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                                   | 0x00000000 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
|                                                   | 0x00000001 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
|                                                   | 0x00000002 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
|                                                   | 0x00000004 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
| Bild \_ SCN \_ Type \_ No \_ Pad <br/>             | 0x00000008 <br/> | Der Abschnitt sollte nicht an der nächsten Grenze aufgefüllt werden. Dieses Flag ist veraltet und wird durch Bild- \_ SCN \_ aus \_ 1 Bytes ersetzt. Dies gilt nur für Objektdateien. <br/> |
|                                                   | 0x00000010 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
| Bild- \_ SCN- \_ CNT- \_ Code <br/>                 | 0x00000020 <br/> | Der-Abschnitt enthält ausführbaren Code. <br/>                                                                                                                           |
| Image \_ SCN \_ CNT- \_ initialisierte \_ Daten <br/>    | 0x00000040 <br/> | Der Abschnitt enthält initialisierte Daten. <br/>                                                                                                                          |
| Image \_ SCN- \_ CNT- \_ nicht initialisierte \_ Daten <br/> | 0x00000080 <br/> | Der Abschnitt enthält nicht initialisierte Daten. <br/>                                                                                                                        |
| Bild- \_ SCN \_ lnk \_ other <br/>                | 0x00000100 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
| Bild- \_ SCN \_ lnk \_ Info <br/>                 | 0x00000200 <br/> | Der Abschnitt enthält Kommentare oder andere Informationen. Der Abschnitt. drectve weist diesen Typ auf. Dies gilt nur für Objektdateien. <br/>                                    |
|                                                   | 0x00000400 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
| Bild- \_ SCN \_ lnk \_ Remove <br/>               | 0x00000800 <br/> | Der Abschnitt wird nicht Teil des Bilds. Dies gilt nur für Objektdateien. <br/>                                                                             |
| Bild- \_ SCN \_ lnk \_ COMDAT <br/>               | 0x00001000 <br/> | Der Abschnitt enthält COMDAT-Daten. Weitere Informationen finden Sie unter [COMDAT-Abschnitte (nur Objekt)](#comdat-sections-object-only). Dies gilt nur für Objektdateien. <br/> |
| Bild- \_ SCN- \_ gprel <br/>                     | 0x00008000 <br/> | Der-Abschnitt enthält Daten, auf die über den globalen Zeiger (GP) verwiesen wird. <br/>                                                                                           |
| Image-SCN-Speicher bereinigen \_ \_ \_ <br/>            | 0x00020000 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
| Bild SCN-Arbeitsspeicher ( \_ \_ \_ 16 Bit) <br/>                | 0x00020000 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
| Bild-SCN-Arbeitsspeicher \_ \_ \_ gesperrt <br/>               | 0x00040000 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
| vorab Laden von Image-SCN-Arbeitsspeicher \_ \_ \_ <br/>              | 0x00080000 <br/> | Für die zukünftige Verwendung reserviert. <br/>                                                                                                                                        |
| Bild- \_ SCN \_ Ausrichten von \_ 1 Bytes <br/>             | 0x00100000 <br/> | Richten Sie Daten an einer 1-Byte-Grenze aus. Nur für Objektdateien gültig. <br/>                                                                                                   |
| Bild- \_ SCN \_ Ausrichten von \_ 2 Bytes <br/>             | 0x00200000 <br/> | Richten Sie Daten an einer 2-Byte-Grenze aus. Nur für Objektdateien gültig. <br/>                                                                                                   |
| Bild- \_ SCN \_ Ausrichten von \_ 4 Bytes <br/>             | 0x00300000 <br/> | Richten Sie Daten an einer 4-Byte-Grenze aus. Nur für Objektdateien gültig. <br/>                                                                                                   |
| Bild- \_ SCN- \_ Ausrichtung \_ 8 Bytes <br/>             | 0x00400000 <br/> | Richten Sie Daten an einer 8-Byte-Grenze aus. Nur für Objektdateien gültig. <br/>                                                                                                  |
| Bild- \_ SCN \_ Ausrichten von \_ 16 Bytes <br/>            | 0x00500000 <br/> | Richten Sie Daten an einer 16-Byte-Grenze aus. Nur für Objektdateien gültig. <br/>                                                                                                  |
| Bild- \_ SCN \_ Ausrichten von \_ 32 Bytes <br/>            | 0x00600000 <br/> | Richten Sie Daten an einer Grenze von 32 Bytes aus. Nur für Objektdateien gültig. <br/>                                                                                                  |
| Bild- \_ SCN \_ Ausrichten von \_ 64bytes <br/>            | 0x00700000 <br/> | Richten Sie Daten an einer Grenze von 64 Bytes aus. Nur für Objektdateien gültig. <br/>                                                                                                  |
| Bild- \_ SCN mit \_ \_ 128 Bytes ausrichten <br/>           | 0x00800000 <br/> | Richten Sie Daten an einer Grenze von 128 Bytes aus. Nur für Objektdateien gültig. <br/>                                                                                                 |
| Bild- \_ SCN mit \_ \_ 256 Bytes ausrichten <br/>           | 0x00900000 <br/> | Richten Sie Daten an einer Grenze von 256 Bytes aus. Nur für Objektdateien gültig. <br/>                                                                                                 |
| Bild- \_ SCN- \_ Ausrichtung \_ 512 Bytes <br/>           | 0x00a00000 <br/> | Richten Sie Daten an einer Grenze von 512 Bytes aus. Nur für Objektdateien gültig. <br/>                                                                                                 |
| Bild- \_ SCN \_ Ausrichten von \_ 1024 Bytes <br/>          | 0x00b00000 <br/> | Richten Sie Daten an einer Grenze von 1024 Bytes aus. Nur für Objektdateien gültig. <br/>                                                                                                |
| Bild- \_ SCN \_ Ausrichten \_ 2048bytes <br/>          | 0x00c00000 <br/> | Richten Sie Daten an einer Grenze von 2048 Bytes aus. Nur für Objektdateien gültig. <br/>                                                                                                |
| Bild- \_ SCN \_ Ausrichten \_ 4096bytes <br/>          | 0x00d00000 <br/> | Richten Sie Daten an einer Grenze von 4096 Bytes aus. Nur für Objektdateien gültig. <br/>                                                                                                |
| Bild- \_ SCN \_ Ausrichten \_ 8192bytes <br/>          | 0x00e00000 <br/> | Richten Sie Daten an einer Grenze von 8192 Bytes aus. Nur für Objektdateien gültig. <br/>                                                                                               |
| Bild- \_ SCN \_ lnk \_ nreloc \_ ovfl <br/>         | 0x01000000 <br/> | Der Abschnitt enthält erweiterte Umsetzungen. <br/>                                                                                                                      |
| Image-SCN-Arbeitsspeicher \_ \_ \_ verwerfen <br/>          | 0x02000000 <br/> | Der Abschnitt kann bei Bedarf verworfen werden. <br/>                                                                                                                         |
| Bild-SCN-Arbeitsspeicher \_ \_ \_ nicht \_ zwischengespeichert <br/>          | 0x04000000 <br/> | Der Abschnitt kann nicht zwischengespeichert werden. <br/>                                                                                                                                   |
| Bild-SCN-Arbeitsspeicher \_ \_ \_ nicht \_ ausgelagert <br/>           | 0x08000000 <br/> | Der Abschnitt kann nicht eingefügt werden. <br/>                                                                                                                                    |
| Image-SCN-Speicher frei \_ \_ \_ gegeben <br/>               | 0x10000000 <br/> | Der Abschnitt kann im Arbeitsspeicher freigegeben werden. <br/>                                                                                                                            |
| Bild-SCN-Arbeitsspeicher \_ \_ \_ Ausführung <br/>              | 0x20000000 <br/> | Der Abschnitt kann als Code ausgeführt werden. <br/>                                                                                                                            |
| Bild-SCN-Arbeitsspeicher \_ \_ \_ Lesen <br/>                 | 0x40000000 <br/> | Der Abschnitt kann gelesen werden. <br/>                                                                                                                                        |
| Bild- \_ SCN- \_ \_ Schreibzugriff <br/>                | 0x80000000 <br/> | Der Abschnitt kann in geschrieben werden. <br/>                                                                                                                                  |



 

Image \_ SCN \_ lnk \_ nreloc \_ ovfl gibt an, dass die Anzahl der Umsetzungen für den Abschnitt die 16 Bits überschreitet, die für ihn in der Abschnitts Kopfzeile reserviert sind. Wenn das-Bit festgelegt ist und das Feld "numofrelocations" in der Abschnitts Kopfzeile "0xFFFF" ist, wird die tatsächliche Verschiebungs Anzahl im 32-Bit-virtualAddress-Feld der ersten Verschiebung gespeichert. Wenn Image \_ SCN \_ lnk \_ nreloc \_ ovfl festgelegt ist und im Abschnitt weniger als 0xFFFF-Umsetzungen vorhanden sind, ist ein Fehler aufgetreten.

### <a name="grouped-sections-object-only"></a>Gruppierte Abschnitte (nur Objekt)

"$"? das Zeichen (Dollarzeichen) weist eine besondere Interpretation in den Abschnittsnamen in Objektdateien auf.

Wenn Sie den Bild Abschnitt ermitteln, der den Inhalt eines Objekt Abschnitts enthält, verwirft der Linker das "$"? und alle darauf folgenden Zeichen. Daher wird ein Objekt Abschnitt mit dem Namen. der **Text $ X** trägt tatsächlich zum Abschnitt **. Text** des Bilds bei.

Die Zeichen, die auf "$" folgen? Legen Sie die Reihenfolge der Beiträge zum Bild Abschnitt fest. Alle Beiträge desselben Objekt Abschnitts namens werden im Bild zusammenhängend zugeordnet, und die Beitrags Blöcke werden in lexikalischer Reihenfolge nach Objekt Abschnitts Name sortiert. Daher endet alles in Objektdateien mit Abschnitts Name **. Text $ X** nach den Beiträgen **. Text $ W** und vor den Beiträgen. Text $ **Y** .

Der Abschnitts Name in einer Bilddatei enthält nie "$"? befinden.

## <a name="other-contents-of-the-file"></a>Anderer Inhalt der Datei

- [Abschnitts Daten](#section-data)
- [COFF-Umsetzungen (nur Objekt)](#coff-relocations-object-only)
  - [Typindikatoren](#type-indicators)
- [COFF-Zeilennummern (veraltet)](#coff-line-numbers-deprecated)
- [COFF-Symbol Tabelle](#coff-symbol-table)
  - [Symbol Namen Darstellung](#symbol-name-representation)
  - [Abschnitts Nummern Werte](#section-number-values)
  - [Typdarstellung](#type-representation)
  - [Speicherklasse](#storage-class)
- [Zusatz Symbol Datensätze](#auxiliary-symbol-records)
  - [Erweiterungs Format 1: Funktionsdefinitionen](#auxiliary-format-1-function-definitions)
  - [Erweiterungs Format 2:. BF-und EF-Symbole](#auxiliary-format-2-bf-and-ef-symbols)
  - [Zusatz Format 3: schwache externals](#auxiliary-format-3-weak-externals)
  - [Erweiterungs Format 4: Dateien](#auxiliary-format-4-files)
  - [Zusatz Format 5: Abschnitts Definitionen](#auxiliary-format-5-section-definitions)
  - [COMDAT-Abschnitte (nur Objekt)](#comdat-sections-object-only)
  - [CLR-tokendefinition (nur Objekt)](#clr-token-definition-object-only)
- [COFF-Zeichen folgen Tabelle](#coff-string-table)
- [Attribut Zertifikat Tabelle (nur Bild)](#the-attribute-certificate-table-image-only)
  - [Zertifikat Daten](#certificate-data)
- [Verzögertes Laden von Import Tabellen (nur Bild)](#delay-load-import-tables-image-only)
  - [Die Delay-Load Directory-Tabelle](#the-delay-load-directory-table)
  - [Attribute](#attributes)
  - [Name](#name)
  - [Modul handle](#module-handle)
  - [Verzögerten Import der Adress Tabelle](#delay-import-address-table)
  - [Import Name Tabelle verzögern](#delay-import-name-table)
  - [Verzögert gebundene Import Adress Tabelle und Zeitstempel](#delay-bound-import-address-table-and-time-stamp)
  - [Verzögertes Entladen der Import Adress Tabelle](#delay-unload-import-address-table)

Die bisher beschriebenen Datenstrukturen (bis zu und einschließlich des optionalen Headers) befinden sich alle an einem fixierten Offset am Anfang der Datei (oder im PE-Header, wenn es sich bei der Datei um ein Image handelt, das einen MS-DOS-Stub enthält).

Der Rest eines COFF-Objekts oder einer Bilddatei enthält Datenblöcke, die sich nicht notwendigerweise an einem bestimmten Dateioffset befinden. Stattdessen werden die Speicherorte durch Zeiger im optionalen Header oder über einen Abschnitts Header definiert.

Eine Ausnahme bilden Bilder mit einem sectionalignment-Wert, der kleiner ist als die Seitengröße der Architektur (4 KB für Intel x86 und für MIPS und 8 KB für Itanium). Eine Beschreibung von sectionalignment finden Sie unter [optionaler Header (nur Bild)](#optional-header-image-only). In diesem Fall gibt es Einschränkungen für den Dateioffset der Abschnitts Daten, wie im Abschnitt 5,1, "section Data" beschrieben. Eine weitere Ausnahme besteht darin, dass das Attribut Zertifikat und die Debuginformationen am Ende einer Bilddatei platziert werden müssen, wobei die Attribut Zertifikat Tabelle unmittelbar vor dem Debugabschnitt steht, weil das Lade Modul diese nicht in den Arbeitsspeicher zuordnet. Die Regel zu Attribut Zertifikat-und Debuginformationen gilt jedoch nicht für Objektdateien.

### <a name="section-data"></a>Abschnitts Daten

Initialisierte Daten für einen Abschnitt bestehen aus einfachen Byte Blöcken. Für Abschnitte, die alle Nullen enthalten, müssen die Abschnitts Daten jedoch nicht eingeschlossen werden.

Die Daten für die einzelnen Abschnitte befinden sich in der Datei Abweichung, die vom Feld "PointerToRawData" in der Abschnitts Kopfzeile angegeben wurde. Die Größe der Daten in der Datei wird durch das sizeofrawdata-Feld angegeben. Wenn sizeofrawdata kleiner als VirtualSize ist, wird der Rest mit Nullen aufgefüllt.

In einer Bilddatei müssen die Abschnitts Daten an einer Grenze ausgerichtet werden, die im Feld "FileAlignment" im optionalen Header angegeben ist. Abschnitts Daten müssen in der Reihenfolge der RVA-Werte für die entsprechenden Abschnitte angezeigt werden (wie die einzelnen Abschnitts Header in der Abschnitts Tabelle).

Es gibt zusätzliche Einschränkungen für Bilddateien, wenn der Wert der sectionalignment-Eigenschaft im optionalen Header kleiner ist als die Seitengröße der Architektur. Bei solchen Dateien muss der Speicherort der Abschnitts Daten in der Datei mit dem Speicherort im Arbeitsspeicher übereinstimmen, wenn das Image geladen wird, sodass der physische Offset für Abschnitts Daten mit der RVA identisch ist.

### <a name="coff-relocations-object-only"></a>COFF-Umsetzungen (nur Objekt)

Objektdateien enthalten COFF-Umsetzungen, die angeben, wie die Abschnitts Daten geändert werden sollen, wenn Sie in der Bilddatei abgelegt und anschließend in den Arbeitsspeicher geladen werden.

Bilddateien enthalten keine COFF-Umsetzungen, da allen referenzierten Symbolen bereits Adressen in einem flachen Adressraum zugewiesen wurden. Ein Bild enthält Verschiebungs Informationen in Form von Basis Umsetzungen im. reloc-Abschnitt (es sei denn, für das Image ist das Attribut "Image \_ file \_ relocs" entfernt \_ ). Weitere Informationen finden Sie [im Abschnitt ". reloc" (nur Image)](#the-reloc-section-image-only).

Für jeden Abschnitt in einer Objektdatei enthält ein Array mit Datensätzen fester Länge die COFF-Umsetzungen des Abschnitts. Die Position und Länge des Arrays werden in der Abschnitts Kopfzeile angegeben. Jedes Element des Arrays weist das folgende Format auf.



| Offset        | Size          | Feld                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                     |
|---------------|---------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | VirtualAddress <br/>   | Die Adresse des Elements, auf das die Verlagerung angewendet wird. Dies ist der Offset vom Anfang des Abschnitts plus dem Wert des Felds RVA/Offset des Abschnitts. Siehe [Abschnitts Tabelle (Abschnitts Header)](#section-table-section-headers). Wenn das erste Byte des Abschnitts z. b. die Adresse 0x10 hat, hat das dritte Byte die Adresse 0x12. <br/> |
| 4 <br/> | 4 <br/> | Symboltableindex <br/> | Ein NULL basierter Index in der Symboltabelle. Dieses Symbol gibt die Adresse an, die für die Verlagerung verwendet werden soll. Wenn das angegebene Symbol eine Abschnitts Speicher Klasse aufweist, ist die Symbol Adresse die Adresse mit dem ersten Abschnitt desselben Namens. <br/>                                                                                                 |
| 8 <br/> | 2 <br/> | type <br/>             | Ein-Wert, der die Art der Verschiebung angibt, die ausgeführt werden soll. Gültige Verschiebungs Typen sind vom Computertyp abhängig. Siehe [Typindikatoren](#type-indicators). <br/>                                                                                                                                                                                     |



 

Wenn das Symbol, auf das das symboltableindex-Feld verweist, den Abschnitt der SYM-Klasse der Speicher Klassen Image enthält \_ \_ \_ , ist die Adresse des Symbols der Anfang des Abschnitts. Der-Abschnitt befindet sich normalerweise in derselben Datei, es sei denn, die Objektdatei ist Teil einer Archive (Library). In diesem Fall befindet sich der Abschnitt in einer beliebigen anderen Objektdatei im Archiv, die denselben Archiv Elementnamen aufweist wie die aktuelle Objektdatei. (Die Beziehung zum Archivierungs Elementnamen wird beim Verknüpfen von Import Tabellen, d. h. im. iData-Abschnitt, verwendet.)

#### <a name="type-indicators"></a>Typindikatoren

Das typanfeld des Verschiebungs Datensatzes gibt an, welche Art der Verschiebung durchgeführt werden soll. Für jeden Computertyp werden unterschiedliche Verschiebungs Typen definiert.

##### <a name="x64-processors"></a>x64-Prozessoren

Die folgenden Verschiebungs Typen Indikatoren sind für x64-und kompatible Prozessoren definiert.



| Konstante                                | Wert              | BESCHREIBUNG                                                                                                                                                   |
|-----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Image \_ rel \_ amd64 \_ absolut <br/> | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                        |
| Bild \_ rel \_ amd64 \_ ADDR64 <br/>   | 0x0001 <br/> | Die 64-Bit-VA des Verschiebungs Ziels. <br/>                                                                                                           |
| Bild \_ rel \_ amd64 \_ ADDR32 <br/>   | 0x0002 <br/> | Die 32-Bit-VA des Verschiebungs Ziels. <br/>                                                                                                           |
| Bild \_ rel \_ amd64 \_ ADDR32NB <br/> | 0x0003 <br/> | Die 32-Bit-Adresse ohne Image Basis (RVA). <br/>                                                                                                   |
| Bild \_ rel \_ amd64 \_ REL32 <br/>    | 0x0004 <br/> | Die relative 32-Bit-Adresse aus dem Byte nach der Verschiebung. <br/>                                                                               |
| Bild \_ rel \_ amd64 \_ REL32 \_ 1 <br/> | 0x0005 <br/> | Die 32-Bit-Adresse relativ zum Byte-Abstand 1 aus der Verschiebung. <br/>                                                                               |
| Bild \_ rel \_ amd64 \_ REL32 \_ 2 <br/> | 0x0006 <br/> | Die 32-Bit-Adresse relativ zu Byte Distance 2 aus der Verschiebung. <br/>                                                                               |
| Bild \_ rel \_ amd64 \_ REL32 \_ 3 <br/> | 0x0007 <br/> | Die 32-Bit-Adresse relativ zu Byte Distance 3 aus der Verschiebung. <br/>                                                                               |
| Bild \_ rel \_ amd64 \_ REL32 \_ 4 <br/> | 0x0008 <br/> | Die 32-Bit-Adresse relativ zu Byte Distance 4 aus der Verschiebung. <br/>                                                                               |
| Bild \_ rel \_ amd64 \_ REL32 \_ 5 <br/> | 0x0009 <br/> | Die 32-Bit-Adresse relativ zu Byte Distance 5 aus der Verschiebung. <br/>                                                                               |
| Abschnitt "Image \_ rel \_ amd64" \_ <br/>  | 0x000A <br/> | Der 16-Bit-Abschnitts Index des Abschnitts, der das Ziel enthält. Hiermit werden Debuginformationen unterstützt. <br/>                                  |
| Bild \_ rel \_ amd64- \_ secrel <br/>   | 0x000B <br/> | Der 32-Bit-Offset des Ziels vom Anfang seines Abschnitts. Diese wird verwendet, um Debuginformationen und statischen lokalen Thread Speicher zu unterstützen. <br/> |
| Bild \_ rel \_ amd64 \_ SECREL7 <br/>  | 0x000C <br/> | Ein 7-Bit-Offset ohne Vorzeichen von der Basis des Abschnitts, der das Ziel enthält. <br/>                                                                    |
| Bild \_ rel \_ amd64- \_ Token <br/>    | 0x000D <br/> | CLR-Token. <br/>                                                                                                                                       |
| Bild \_ rel \_ amd64 \_ SREL32 <br/>   | 0x000e <br/> | Ein von 32 Bit signierter spannen abhängiger Wert, der in das-Objekt ausgegeben wird. <br/>                                                                                     |
| Bild \_ rel \_ amd64- \_ paar <br/>     | 0x000F <br/> | Ein paar, das unmittelbar auf alle Spannen abhängigen Werte folgen muss. <br/>                                                                                   |
| Bild \_ rel \_ amd64 \_ SSPAN32 <br/>  | 0x0010 <br/> | Ein von 32 Bit signierter spannen abhängiger Wert, der zur Linkzeit verwendet wird. <br/>                                                                                |



 

##### <a name="arm-processors"></a>ARM-Prozessoren

Die folgenden Verschiebungs Typen Indikatoren werden für ARM-Prozessoren definiert.



| Konstante                                | Wert              | BESCHREIBUNG                                                                                                                                                                                                                                                            |
|-----------------------------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Image \_ rel \_ Arm \_ absolut <br/>   | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                                                                                                                                 |
| Image \_ rel \_ Arm \_ ADDR32 <br/>     | 0x0001 <br/> | Die 32-Bit-VA des Ziels. <br/>                                                                                                                                                                                                                               |
| Image \_ rel \_ Arm \_ ADDR32NB <br/>   | 0x0002 <br/> | Die 32-Bit-RVA des Ziels. <br/>                                                                                                                                                                                                                              |
| Image \_ rel \_ Arm \_ BRANCH24 <br/>   | 0x0003 <br/> | Die relative 24-Bit-Verschiebung zum Ziel. <br/>                                                                                                                                                                                                            |
| Image \_ rel \_ Arm \_ BRANCH11 <br/>   | 0x0004 <br/> | Der Verweis auf einen Unterroutine-aufzurufenden. Der Verweis besteht aus 2 16-Bit-Anweisungen mit 11-Bit-Offsets. <br/>                                                                                                                                                 |
| Image \_ rel \_ Arm \_ REL32 <br/>      | 0x000A <br/> | Die relative 32-Bit-Adresse aus dem Byte nach der Verschiebung. <br/>                                                                                                                                                                                        |
| Abschnitt "Image \_ rel \_ Arm" \_ <br/>    | 0x000e <br/> | Der 16-Bit-Abschnitts Index des Abschnitts, der das Ziel enthält. Hiermit werden Debuginformationen unterstützt. <br/>                                                                                                                                           |
| Image \_ rel \_ Arm- \_ secrel <br/>     | 0x000F <br/> | Der 32-Bit-Offset des Ziels vom Anfang seines Abschnitts. Diese wird verwendet, um Debuginformationen und statischen lokalen Thread Speicher zu unterstützen. <br/>                                                                                                          |
| Image \_ rel \_ Arm \_ MOV32 <br/>      | 0x0010 <br/> | Die 32-Bit-VA des Ziels. Diese Verschiebung wird mithilfe einer muvw-Anweisung für die unteren 16 Bits gefolgt von einem muvt für die hohen 16 Bits angewendet. <br/>                                                                                                              |
| Image \_ rel \_ Thumb \_ MOV32 <br/>    | 0x0011 <br/> | Die 32-Bit-VA des Ziels. Diese Verschiebung wird mithilfe einer muvw-Anweisung für die unteren 16 Bits gefolgt von einem muvt für die hohen 16 Bits angewendet. <br/>                                                                                                              |
| Image \_ rel \_ Thumb \_ BRANCH20 <br/> | 0x0012 <br/> | Die-Anweisung wird mit der relativen Verschiebung von 21 Bit zum ausgerichteten 2-Byte-Ziel korrigiert. Das unwichtigste Bit der Verschiebung ist immer 0 (null) und wird nicht gespeichert. Diese Verschiebung entspricht einer bedingten Thumb-2 32-Bit-Anweisung. <br/> |
| Nicht verwendet <br/>                      | 0x0013 <br/> |                                                                                                                                                                                                                                                                        |
| Image \_ rel \_ Thumb \_ BRANCH24 <br/> | 0x0014 <br/> | Die-Anweisung wird mit der relativen Verschiebung von 25 Bit zum ausgerichteten 2-Byte-Ziel korrigiert. Das unwichtigste Bit der Verschiebung ist 0 (null) und wird nicht gespeichert. Diese Verschiebung entspricht einer Thumb-2 B-Anweisung. <br/>                            |
| Image \_ rel \_ Thumb \_ BLX23 <br/>    | 0x0015 <br/> | Die-Anweisung wird mit der relativen Verschiebung von 25 Bit zum ausgerichteten 4-Byte-Ziel korrigiert. Die unteren 2 Bits der Verschiebung sind 0 (null) und werden nicht gespeichert. <br/> Diese Verschiebung entspricht einer "Thumb-2 BLX"-Anweisung. <br/>                      |
| Image- \_ rel- \_ Arm- \_ paar <br/>       | 0x0016 <br/> | Die Verschiebung ist nur gültig, wenn Sie unmittelbar auf einen Arm- \_ refhi oder Thumb- \_ refhi folgt. Der symboltableindex-Wert enthält eine Verschiebung und keinen Index in der Symboltabelle. <br/>                                                                                |



 

##### <a name="arm64-processors"></a>ARM64-Prozessoren

Die folgenden Verschiebungs Typen Indikatoren sind für ARM64-Prozessoren definiert.



| Konstante                                       | Wert              | BESCHREIBUNG                                                                                                                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bild \_ rel \_ ARM64 \_ absolut <br/>        | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                        |
| Image \_ rel \_ ARM64 \_ ADDR32 <br/>          | 0x0001 <br/> | Die 32-Bit-VA des Ziels. <br/>                                                                                                                      |
| Image \_ rel \_ ARM64 \_ ADDR32NB <br/>        | 0x0002 <br/> | Die 32-Bit-RVA des Ziels. <br/>                                                                                                                     |
| Image \_ rel \_ ARM64 \_ BRANCH26 <br/>        | 0x0003 <br/> | Die relative Verschiebung von 26 Bit zum Ziel, für B-und BL-Anweisungen. <br/>                                                                        |
| Image \_ rel \_ ARM64 \_ pgebase \_ REL21 <br/> | 0x0004 <br/> | Die Seitenbasis des Ziels für die adrp-Anweisung. <br/>                                                                                                |
| Image \_ rel \_ ARM64 \_ REL21 <br/>           | 0x0005 <br/> | Die relative Verschiebung der 12-Bit-Version zum Ziel für die Anweisung AdR <br/>                                                                               |
| Bild \_ rel \_ ARM64 \_ pageoffset \_ 12a <br/> | 0x0006 <br/> | Der 12-Bit-Seiten Offset des Ziels, für Anweisungen Add/Adds (immediate) mit Zero Shift. <br/>                                                      |
| Bild \_ rel \_ ARM64 \_ pageoffset \_ 12L <br/> | 0x0007 <br/> | Der 12-Bit-Seiten Offset des Ziels für Anweisung LDR (indiziert, Ganzzahl ohne Vorzeichen immediate). <br/>                                                          |
| Image \_ rel \_ ARM64 \_ secrel <br/>          | 0x0008 <br/> | Der 32-Bit-Offset des Ziels vom Anfang seines Abschnitts. Diese wird verwendet, um Debuginformationen und statischen lokalen Thread Speicher zu unterstützen. <br/> |
| Image \_ rel \_ ARM64 \_ secrel \_ LOW12A <br/>  | 0x0009 <br/> | Bit 0:11 des Abschnitts Offsets des Ziels, für Anweisungen hinzufügen/hinzufügen (unmittelbar) mit 0 (null). <br/>                                                  |
| Image \_ rel \_ ARM64 \_ secrel \_ HIGH12A <br/> | 0x000A <br/> | Bit 12:23 des Abschnitts Offsets des Ziels, für Anweisungen hinzufügen/hinzufügen (unmittelbar) mit 0 (null). <br/>                                                 |
| Image \_ rel \_ ARM64 \_ secrel \_ LOW12L <br/>  | 0x000B <br/> | Bit 0:11 des Abschnitts Offsets des Ziels für Anweisung LDR (indiziert, Ganzzahl ohne Vorzeichen immediate). <br/>                                                      |
| Image \_ rel \_ ARM64 \_ Token <br/>           | 0x000C <br/> | CLR-Token. <br/>                                                                                                                                        |
| Abschnitt "Image \_ rel \_ ARM64" \_ <br/>         | 0x000D <br/> | Der 16-Bit-Abschnitts Index des Abschnitts, der das Ziel enthält. Hiermit werden Debuginformationen unterstützt. <br/>                                  |
| Image \_ rel \_ ARM64 \_ ADDR64 <br/>          | 0x000e <br/> | Die 64-Bit-VA des Verschiebungs Ziels. <br/>                                                                                                           |
| Image \_ rel \_ ARM64 \_ BRANCH19 <br/>        | 0x000F <br/> | Der 19-Bit-Offset zum Verschiebungs Ziel für die bedingte B-Anweisung. <br/>                                                                        |
| Image \_ rel \_ ARM64 \_ BRANCH14 <br/>        | 0x0010 <br/> | Der 14-Bit-Offset zum Verschiebungs Ziel für die Anweisungen TBZ und tbnz. <br/>                                                                        |
| Image \_ rel \_ ARM64 \_ REL32 <br/>           | 0x0011 <br/> | Die relative 32-Bit-Adresse aus dem Byte nach der Verschiebung. <br/>                                                                               |

##### <a name="hitachi-superh-processors"></a>Hitachi SuperH-Prozessoren

Die folgenden Verschiebungs Typen Indikatoren sind für SH3-und SH4-Prozessoren definiert. SH5-spezifische Umsetzungen werden als SHM (SH Media) notiert.



| Konstante                                      | Wert              | BESCHREIBUNG                                                                                                                                                                                                                |
|-----------------------------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bild \_ rel \_ SH3 \_ absolut <br/>         | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                                                                                     |
| Image \_ rel \_ SH3 \_ DIRECT16 <br/>         | 0x0001 <br/> | Ein Verweis auf den 16-Bit-Speicherort, der das VA des Ziel Symbols enthält. <br/>                                                                                                                                  |
| Image \_ rel \_ SH3 \_ DIRECT32 <br/>         | 0x0002 <br/> | Die 32-Bit-VA des Ziel Symbols. <br/>                                                                                                                                                                            |
| Image \_ rel \_ SH3 \_ DIRECT8 <br/>          | 0x0003 <br/> | Ein Verweis auf den 8-Bit-Speicherort, der das VA des Ziel Symbols enthält. <br/>                                                                                                                                   |
| Bild \_ rel \_ SH3 \_ DIRECT8 \_ Word <br/>    | 0x0004 <br/> | Ein Verweis auf die 8-Bit-Anweisung, die die effektive 16-Bit-VA des Ziel Symbols enthält. <br/>                                                                                                               |
| Image \_ rel \_ SH3 \_ DIRECT8 \_ Long <br/>    | 0x0005 <br/> | Ein Verweis auf die 8-Bit-Anweisung, die die effektive 32-Bit-VA des Ziel Symbols enthält. <br/>                                                                                                               |
| Image \_ rel \_ SH3 \_ DIRECT4 <br/>          | 0x0006 <br/> | Ein Verweis auf den 8-Bit-Speicherort, dessen niedrige 4 Bits das VA des Ziel Symbols enthalten. <br/>                                                                                                                        |
| Bild \_ rel \_ SH3 \_ DIRECT4 \_ Word <br/>    | 0x0007 <br/> | Ein Verweis auf die 8-Bit-Anweisung, deren niedrige 4 Bits die effektive 16-Bit-VA des Ziel Symbols enthalten. <br/>                                                                                                    |
| Image \_ rel \_ SH3 \_ DIRECT4 \_ Long <br/>    | 0x0008 <br/> | Ein Verweis auf die 8-Bit-Anweisung, deren niedrige 4 Bits die effektive 32-Bit-VA des Ziel Symbols enthalten. <br/>                                                                                                    |
| Bild \_ rel \_ SH3 \_ PCREL8 \_ Word <br/>     | 0x0009 <br/> | Ein Verweis auf die 8-Bit-Anweisung, die den effektiven 16-Bit-relativen Offset des Ziel Symbols enthält. <br/>                                                                                                  |
| Image \_ rel \_ SH3 \_ PCREL8 \_ Long <br/>     | 0x000A <br/> | Ein Verweis auf die 8-Bit-Anweisung, die den effektiven relativen 32-Bit-Offset des Ziel Symbols enthält. <br/>                                                                                                  |
| Bild \_ rel \_ SH3 \_ PCREL12 \_ Word <br/>    | 0x000B <br/> | Ein Verweis auf die 16-Bit-Anweisung, deren niedrige 12-Bit-Werte den effektiven 16-Bit-Offset des Ziel Symbols enthalten. <br/>                                                                                     |
| Image \_ rel \_ SH3 \_ StartOf- \_ Abschnitt <br/> | 0x000C <br/> | Ein Verweis auf einen 32-Bit-Speicherort, bei dem es sich um die VA des Abschnitts handelt, der das Ziel Symbol enthält. <br/>                                                                                                                |
| Image \_ rel \_ SH3 \_ sizeof- \_ Abschnitt <br/>  | 0x000D <br/> | Ein Verweis auf den 32-Bit-Speicherort, bei dem es sich um die Größe des Abschnitts handelt, der das Ziel Symbol enthält. <br/>                                                                                                            |
| Abschnitt "Image \_ rel \_ SH3" \_ <br/>          | 0x000e <br/> | Der 16-Bit-Abschnitts Index des Abschnitts, der das Ziel enthält. Hiermit werden Debuginformationen unterstützt. <br/>                                                                                               |
| Image \_ rel \_ SH3 \_ secrel <br/>           | 0x000F <br/> | Der 32-Bit-Offset des Ziels vom Anfang seines Abschnitts. Diese wird verwendet, um Debuginformationen und statischen lokalen Thread Speicher zu unterstützen. <br/>                                                              |
| Image \_ rel \_ SH3 \_ DIRECT32 \_ NB <br/>     | 0x0010 <br/> | Die 32-Bit-RVA des Ziel Symbols. <br/>                                                                                                                                                                           |
| Image \_ rel \_ SH3 \_ GPREL4 \_ Long <br/>     | 0x0011 <br/> | Relativer GP. <br/>                                                                                                                                                                                                   |
| Image \_ rel \_ SH3 \_ Token <br/>            | 0x0012 <br/> | CLR-Token. <br/>                                                                                                                                                                                                     |
| Image \_ rel \_ shm \_ pkrelpt <br/>          | 0x0013 <br/> | Der Offset der aktuellen Anweisung in longwords. Wenn das nomode-Bit nicht festgelegt ist, fügen Sie den umgekehrten Wert des unteren Bits in Bit 32 ein, um PTA oder PTB auszuwählen. <br/>                                                          |
| Image \_ rel \_ shm \_ Reflo <br/>            | 0x0014 <br/> | Die unteren 16 Bits der 32-Bit-Adresse. <br/>                                                                                                                                                                         |
| Image \_ rel \_ shm \_ refihalf <br/>          | 0x0015 <br/> | Die hohen 16 Bits der 32-Bit-Adresse. <br/>                                                                                                                                                                        |
| Image \_ rel \_ shm \_ rello <br/>            | 0x0016 <br/> | Die unteren 16 Bits der relativen Adresse. <br/>                                                                                                                                                                       |
| Bild \_ rel \_ shm \_ relhalf <br/>          | 0x0017 <br/> | Die hohen 16 Bits der relativen Adresse. <br/>                                                                                                                                                                      |
| Image \_ rel- \_ shm- \_ paar <br/>             | 0x0018 <br/> | Die Verschiebung ist nur gültig, wenn Sie unmittelbar auf eine refhalf-, relhalf-oder rello-Verschiebung folgt. Das symboltableindex-Feld der Verschiebung enthält eine Verschiebung und keinen Index in der Symboltabelle. <br/> |
| Image \_ rel \_ shm \_ nomode <br/>           | 0x8000 <br/> | Die Verschiebung ignoriert den Abschnitts Modus. <br/>                                                                                                                                                                           |



 

##### <a name="ibm-powerpc-processors"></a>IBM-PowerPC-Prozessoren

Die folgenden Verschiebungs Typen Indikatoren sind für PowerPC-Prozessoren definiert.



| Konstante                              | Wert              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Image \_ rel \_ PPC \_ absolut <br/> | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                                                                                                                                                                                                                                              |
| Image \_ rel \_ PPC \_ ADDR64 <br/>   | 0x0001 <br/> | Die 64-Bit-VA des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                            |
| Image \_ rel \_ PPC \_ ADDR32 <br/>   | 0x0002 <br/> | Die 32-Bit-VA des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                            |
| Image \_ rel \_ PPC \_ ADDR24 <br/>   | 0x0003 <br/> | Die unteren 24 Bits der VA des Ziels. Dies ist nur gültig, wenn das Ziel Symbol absolut ist und bis zum ursprünglichen Wert mit Vorzeichen erweitert werden kann. <br/>                                                                                                                                                                                                                          |
| Image \_ rel \_ PPC \_ ADDR16 <br/>   | 0x0004 <br/> | Die unteren 16 Bits der VA des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                     |
| Image \_ rel \_ PPC \_ ADDR14 <br/>   | 0x0005 <br/> | Die unteren 14 Bits der VA des Ziels. Dies ist nur gültig, wenn das Ziel Symbol absolut ist und bis zum ursprünglichen Wert mit Vorzeichen erweitert werden kann. <br/>                                                                                                                                                                                                                               |
| Image \_ rel \_ PPC \_ REL24 <br/>    | 0x0006 <br/> | Ein 24-Bit-PC-relativer Offset zum Speicherort des Symbols. <br/>                                                                                                                                                                                                                                                                                                                   |
| Image \_ rel \_ PPC \_ REL14 <br/>    | 0x0007 <br/> | Ein PC-relativer 14-Bit-Offset zum Speicherort des Symbols. <br/>                                                                                                                                                                                                                                                                                                                   |
| Image \_ rel \_ PPC \_ ADDR32NB <br/> | 0x000A <br/> | Die 32-Bit-RVA des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                           |
| Image \_ rel \_ PPC \_ secrel <br/>   | 0x000B <br/> | Der 32-Bit-Offset des Ziels vom Anfang seines Abschnitts. Diese wird verwendet, um Debuginformationen und statischen lokalen Thread Speicher zu unterstützen. <br/>                                                                                                                                                                                                                       |
| Abschnitt "Image \_ rel \_ PPC" \_ <br/>  | 0x000C <br/> | Der 16-Bit-Abschnitts Index des Abschnitts, der das Ziel enthält. Hiermit werden Debuginformationen unterstützt. <br/>                                                                                                                                                                                                                                                        |
| Image \_ rel \_ PPC \_ SECREL16 <br/> | 0x000F <br/> | Der 16-Bit-Offset des Ziels vom Anfang seines Abschnitts. Diese wird verwendet, um Debuginformationen und statischen lokalen Thread Speicher zu unterstützen. <br/>                                                                                                                                                                                                                       |
| Bild \_ rel \_ PPC \_ Ref <br/>    | 0x0010 <br/> | Die hohen 16 Bits der 32-Bit-VA des Ziels. Diese wird für die erste Anweisung in einer Sequenz mit zwei Anweisungen verwendet, die eine vollständige Adresse lädt. Auf diese Verschiebung muss unmittelbar eine paar Verlagerung folgen, deren symboltableindex eine 16-Bit-Verschiebung mit Vorzeichen enthält, die den oberen 16 Bits hinzugefügt wird, die von dem Speicherort, der verschoben wird, entnommen wurde. <br/> |
| Bild \_ rel, \_ PPC \_ Reflo <br/>    | 0x0011 <br/> | Die unteren 16 Bits der VA des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                     |
| Bild- \_ rel- \_ PPC- \_ paar <br/>     | 0x0012 <br/> | Eine Verschiebung, die nur gültig ist, wenn Sie unmittelbar auf eine refhi-oder secrelhi-Umsetzung folgt. Der symboltableindex-Wert enthält eine Verschiebung und keinen Index in der Symboltabelle. <br/>                                                                                                                                                                                        |
| Image \_ rel \_ PPC \_ secrello <br/> | 0x0013 <br/> | Die unteren 16 Bits des 32-Bit-Offsets des Ziels vom Anfang des Abschnitts. <br/>                                                                                                                                                                                                                                                                                   |
| Bild \_ rel \_ PPC \_ gprel <br/>    | 0x0015 <br/> | Die 16-Bit-Verschiebung des Ziels in Relation zum GP-Register. <br/>                                                                                                                                                                                                                                                                                               |
| Bild- \_ rel- \_ PPC- \_ Token <br/>    | 0x0016 <br/> | Das CLR-Token. <br/>                                                                                                                                                                                                                                                                                                                                                          |



 

##### <a name="intel-386-processors"></a>Intel 386-Prozessoren

Die folgenden Verschiebungs Typen Indikatoren sind für Intel 386 und kompatible Prozessoren definiert.



| Konstante                               | Wert              | BESCHREIBUNG                                                                                                                                                   |
|----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Image \_ rel \_ i386 \_ absolut <br/> | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                        |
| Image \_ rel \_ i386 \_ DIR16 <br/>    | 0x0001 <br/> | Wird nicht unterstützt. <br/>                                                                                                                                    |
| Image \_ rel \_ i386 \_ REL16 <br/>    | 0x0002 <br/> | Wird nicht unterstützt. <br/>                                                                                                                                    |
| Image \_ rel \_ i386 \_ DIR32 <br/>    | 0x0006 <br/> | Das 32-Bit-VA des Ziels. <br/>                                                                                                                           |
| Image \_ rel \_ i386 \_ DIR32NB <br/>  | 0x0007 <br/> | Die 32-Bit-RVA des Ziels. <br/>                                                                                                                          |
| Image \_ rel \_ i386 \_ SEG12 <br/>    | 0x0009 <br/> | Wird nicht unterstützt. <br/>                                                                                                                                    |
| Abschnitt "Image \_ rel \_ i386" \_ <br/>  | 0x000A <br/> | Der 16-Bit-Abschnitts Index des Abschnitts, der das Ziel enthält. Hiermit werden Debuginformationen unterstützt. <br/>                                  |
| Image \_ rel \_ i386 \_ secrel <br/>   | 0x000B <br/> | Der 32-Bit-Offset des Ziels vom Anfang seines Abschnitts. Diese wird verwendet, um Debuginformationen und statischen lokalen Thread Speicher zu unterstützen. <br/> |
| Image \_ rel \_ i386- \_ Token <br/>    | 0x000C <br/> | Das CLR-Token. <br/>                                                                                                                                    |
| Image \_ rel \_ i386 \_ SECREL7 <br/>  | 0x000D <br/> | Ein 7-Bit-Offset von der Basis des Abschnitts, der das Ziel enthält. <br/>                                                                             |
| Image \_ rel \_ i386 \_ REL32 <br/>    | 0x0014 <br/> | Die relative Verschiebung von 32 Bit zum Ziel. Dies unterstützt die x86-relative Verzweigung und die-Aufrufe. <br/>                                      |



 

##### <a name="intel-itanium-processor-family-ipf"></a>Intel Itanium-Prozessorfamilie (IPF)

Die folgenden Verschiebungs Typen Indikatoren werden für die Intel Itanium-Prozessorfamilie und kompatible Prozessoren definiert. Beachten Sie, dass bei Umsetzungen bei Anweisungen der Offset und die Slotnummer des Bündels für den Verschiebungs Offset verwendet



| Konstante                                 | Wert              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Image \_ rel \_ ia64 \_ absolut <br/>   | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                                                                                                                                                                                                          |
| Image \_ rel \_ ia64 \_ IMM14 <br/>      | 0x0001 <br/> | Der Anweisungs Verlagerung kann eine Addend-Verschiebung folgen, deren Wert der Zieladresse hinzugefügt wird, bevor Sie in den angegebenen Slot im IMM14 Bundle eingefügt wird. Das Verschiebungs Ziel muss absolut sein, oder das Image muss korrigiert werden. <br/>                                                                                 |
| Image \_ rel \_ ia64 \_ IMM22 <br/>      | 0x0002 <br/> | Der Anweisungs Verlagerung kann eine Addend-Verschiebung folgen, deren Wert der Zieladresse hinzugefügt wird, bevor Sie in den angegebenen Slot im IMM22 Bundle eingefügt wird. Das Verschiebungs Ziel muss absolut sein, oder das Image muss korrigiert werden. <br/>                                                                                 |
| Image \_ rel \_ ia64 \_ IMM64 <br/>      | 0x0003 <br/> | Die Slotnummer dieser Verschiebung muss eins (1) sein. Auf die Verschiebung kann eine Addend-Verschiebung folgen, deren Wert der Zieladresse hinzugefügt wird, bevor Sie in allen drei Slots des IMM64-Bundles gespeichert wird. <br/>                                                                                                                   |
| Image \_ rel \_ ia64 \_ DIR32 <br/>      | 0x0004 <br/> | Das 32-Bit-VA des Ziels. Dies wird nur für/LARGEADDRESSAWARE unterstützt: keine Bilder. <br/>                                                                                                                                                                                                                                                    |
| Image \_ rel \_ ia64 \_ DIR64 <br/>      | 0x0005 <br/> | Das 64-Bit-VA des Ziels. <br/>                                                                                                                                                                                                                                                                                                             |
| Image \_ rel \_ ia64 \_ PCREL21B <br/>   | 0x0006 <br/> | Die-Anweisung wird mit der relativen Verschiebung von 25 Bit zum Ziel mit 16-Bit-Ausrichtung korrigiert. Die unteren 4 Bits der Verschiebung sind 0 (null) und werden nicht gespeichert. <br/>                                                                                                                                                                     |
| Image \_ rel \_ ia64 \_ PCREL21M <br/>   | 0x0007 <br/> | Die-Anweisung wird mit der relativen Verschiebung von 25 Bit zum Ziel mit 16-Bit-Ausrichtung korrigiert. Die unteren 4 Bits der Verschiebung, die 0 (null) sind, werden nicht gespeichert. <br/>                                                                                                                                                                 |
| Image \_ rel \_ ia64 \_ PCREL21F <br/>   | 0x0008 <br/> | Die lssb dieses Verschiebungs Offsets müssen die Slotnummer enthalten, während der Rest die Bündel Adresse ist. Das Paket wird mit der relativen Verschiebung von 25 Bit zum Ziel mit 16-Bit-Ausrichtung korrigiert. Die unteren 4 Bits der Verschiebung sind 0 (null) und werden nicht gespeichert. <br/>                                                                |
| Image \_ rel \_ ia64 \_ GPREL22 <br/>    | 0x0009 <br/> | Der Anweisungs Verlagerung kann eine Addend-Verschiebung folgen, deren Wert der Zieladresse und dann ein 22-Bit-GP-relativer Offset, der berechnet und auf das GPREL22-Bündel angewendet wird, hinzugefügt wird. <br/>                                                                                                                            |
| Image \_ rel \_ ia64 \_ LTOFF22 <br/>    | 0x000A <br/> | Die Anweisung wird mit dem 22-Bit-GP-relativen Offset zum literaltabelleneintrag des Ziel Symbols korrigiert. Der Linker erstellt diesen literaltabelleneintrag auf der Grundlage dieser Verlagerung und der nachfolgenden nachfolgenden Umsetzung. <br/>                                                                                                        |
| Abschnitt "Image \_ rel \_ ia64" \_ <br/>    | 0x000B <br/> | Der 16-Bit-Abschnitts Index des Abschnitts enthält das Ziel. Hiermit werden Debuginformationen unterstützt. <br/>                                                                                                                                                                                                                         |
| Image \_ rel \_ ia64 \_ SECREL22 <br/>   | 0x000C <br/> | Die Anweisung wird mit dem 22-Bit-Offset des Ziels vom Anfang des Abschnitts korrigiert. Diese Verschiebung kann sofort durch eine Addend-Verschiebung befolgt werden, deren Wertfeld den 32-Bit-Offset ohne Vorzeichen des Ziels vom Anfang des Abschnitts enthält. <br/>                                                     |
| Image \_ rel \_ ia64 \_ SECREL64I <br/>  | 0x000D <br/> | Die Slotnummer für diese Verschiebung muss eins (1) sein. Die Anweisung wird mit dem 64-Bit-Offset des Ziels vom Anfang des Abschnitts korrigiert. Diese Verschiebung kann sofort durch eine Addend-Verschiebung befolgt werden, deren Wertfeld den 32-Bit-Offset ohne Vorzeichen des Ziels vom Anfang des Abschnitts enthält. <br/> |
| Image \_ rel \_ ia64 \_ SECREL32 <br/>   | 0x000e <br/> | Die Adresse der Daten, die mit dem 32-Bit-Offset des Ziels vom Anfang des Abschnitts korrigiert werden sollen. <br/>                                                                                                                                                                                                                          |
| Image \_ rel \_ ia64 \_ DIR32NB <br/>    | 0x0010 <br/> | Die 32-Bit-RVA des Ziels. <br/>                                                                                                                                                                                                                                                                                                            |
| Image \_ rel \_ ia64 \_ SREL14 <br/>     | 0x0011 <br/> | Dies wird auf eine sofortige 14-Bit-Version angewendet, die den Unterschied zwischen zwei wieder aufzurufbaren Zielen enthält. Dies ist ein deklaratives Feld für den Linker, das angibt, dass der Compiler diesen Wert bereits ausgegeben hat. <br/>                                                                                                              |
| Image \_ rel \_ ia64 \_ SREL22 <br/>     | 0x0012 <br/> | Dies wird auf eine sofortige 22-Bit-Version angewendet, die den Unterschied zwischen zwei wieder aufzurufbaren Zielen enthält. Dies ist ein deklaratives Feld für den Linker, das angibt, dass der Compiler diesen Wert bereits ausgegeben hat. <br/>                                                                                                              |
| Image \_ rel \_ ia64 \_ SREL32 <br/>     | 0x0013 <br/> | Dies wird auf eine signierte 32-Bit-Version angewendet, die den Unterschied zwischen zwei wieder aufzurufbaren Werten enthält. Dies ist ein deklaratives Feld für den Linker, das angibt, dass der Compiler diesen Wert bereits ausgegeben hat. <br/>                                                                                                               |
| Image \_ rel \_ ia64 \_ UREL32 <br/>     | 0x0014 <br/> | Dies wird auf eine nicht signierte 32-Bit-Version angewendet, die den Unterschied zwischen zwei wieder aufzurufbaren Werten enthält. Dies ist ein deklaratives Feld für den Linker, das angibt, dass der Compiler diesen Wert bereits ausgegeben hat. <br/>                                                                                                            |
| Image \_ rel \_ ia64 \_ PCREL60X <br/>   | 0x0015 <br/> | Ein 60-Bit-PC-relativer Fixup, das immer als BRL-Anweisung eines MLx-Pakets verbleibt. <br/>                                                                                                                                                                                                                                                 |
| Image \_ rel \_ ia64 \_ PCREL60B <br/>   | 0x0016 <br/> | Ein 60-Bit-PC-relativer Fixup. Wenn die Ziel Verschiebung in ein signiertes 25-Bit-Feld passt, konvertieren Sie das gesamte Paket in ein MBB-Bündel mit NOP. B in Slot 1 und eine 25-Bit-BR-Anweisung (mit den 4 niedrigsten Bits alle 0 (null) und "verworfen" in Slot 2. <br/>                                                                                          |
| Image \_ rel \_ ia64 \_ PCREL60F <br/>   | 0x0017 <br/> | Ein 60-Bit-PC-relativer Fixup. Wenn die Ziel Verschiebung in ein signiertes 25-Bit-Feld passt, konvertieren Sie das gesamte Paket in ein MFB-Bündel mit NOP. F in Slot 1 und 25-Bit (4 niedrigste Bits alle NULL und verworfen) BR-Anweisung in Slot 2. <br/>                                                                                                   |
| Image \_ rel \_ ia64 \_ PCREL60I <br/>   | 0x0018 <br/> | Ein 60-Bit-PC-relativer Fixup. Wenn die Ziel Verschiebung in ein signiertes 25-Bit-Feld passt, konvertieren Sie das gesamte Paket in ein MIB-Bündel mit NOP. I in Slot 1 und 25-Bit (4 niedrigste Bits alle NULL und gelöscht) BR-Anweisung in Slot 2. <br/>                                                                                                   |
| Image \_ rel \_ ia64 \_ PCREL60M <br/>   | 0x0019 <br/> | Ein 60-Bit-PC-relativer Fixup. Wenn die Ziel Verschiebung in ein signiertes 25-Bit-Feld passt, konvertieren Sie das gesamte Paket in ein MMB-Bündel mit NOP. M in Slot 1 und 25-Bit (4 niedrigste Bits alle NULL und gelöscht) BR-Anweisung in Slot 2. <br/>                                                                                                   |
| Image \_ rel \_ ia64 \_ IMMGPREL64 <br/> | 0x001a <br/> | Ein 64-Bit-GP-relativer Fixup. <br/>                                                                                                                                                                                                                                                                                                         |
| Image \_ rel \_ ia64- \_ Token <br/>      | 0x001b <br/> | Ein CLR-Token. <br/>                                                                                                                                                                                                                                                                                                                        |
| Image \_ rel \_ ia64 \_ GPREL32 <br/>    | 0x001c <br/> | Ein 32-Bit-GP-relativer Fixup. <br/>                                                                                                                                                                                                                                                                                                         |
| Image \_ rel \_ ia64 \_ Addend <br/>     | 0x001F <br/> | Die Verschiebung ist nur gültig, wenn Sie direkt einer der folgenden Umsetzungen folgt: IMM14, IMM22, IMM64, GPREL22, LTOFF22, LTOFF64, SECREL22, SECREL64I oder SECREL32. Der zugehörige Wert enthält den Addend, der auf Anweisungen in einem Bündel angewendet werden soll, nicht auf Daten. <br/>                                                                  |



 

##### <a name="mips-processors"></a>MIPS-Prozessoren

Die folgenden Verschiebungs Typen Indikatoren sind für MIPS-Prozessoren definiert.



| Konstante                                | Wert              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Image \_ rel \_ MIPS \_ absolut <br/>  | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                                                                                                                                                                                                                                              |
| Image \_ rel \_ MIPS \_ Ref. <br/>   | 0x0001 <br/> | Die hohen 16 Bits der 32-Bit-VA des Ziels. <br/>                                                                                                                                                                                                                                                                                                                             |
| Image \_ rel \_ MIPS \_ Ref <br/>   | 0x0002 <br/> | Das 32-Bit-VA des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                                 |
| Abbildung \_ rel \_ MIPS \_ jmpaddr <br/>   | 0x0003 <br/> | Die unteren 26 Bits der VA des Ziels. Dies unterstützt die Anweisungen MIPS J und JAL. <br/>                                                                                                                                                                                                                                                                                      |
| Bild \_ rel \_ MIPS \_ Ref <br/>     | 0x0004 <br/> | Die hohen 16 Bits der 32-Bit-VA des Ziels. Diese wird für die erste Anweisung in einer Sequenz mit zwei Anweisungen verwendet, die eine vollständige Adresse lädt. Auf diese Verschiebung muss unmittelbar eine paar Verlagerung folgen, deren symboltableindex eine 16-Bit-Verschiebung mit Vorzeichen enthält, die den oberen 16 Bits hinzugefügt wird, die von dem Speicherort, der verschoben wird, entnommen werden. <br/> |
| Bild \_ rel \_ MIPS \_ Reflo <br/>     | 0x0005 <br/> | Die unteren 16 Bits der VA des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                     |
| Bild \_ rel \_ MIPS- \_ gprel <br/>     | 0x0006 <br/> | Eine 16-Bit-Verschiebung des Ziels relativ zum GP-Register. <br/>                                                                                                                                                                                                                                                                                                 |
| Bild \_ rel \_ MIPS- \_ Literale <br/>   | 0x0007 <br/> | Identisch mit Image \_ rel \_ MIPS \_ gprel. <br/>                                                                                                                                                                                                                                                                                                                                    |
| Abschnitt "Abbildung \_ rel \_ MIPS" \_ <br/>   | 0x000A <br/> | Der 16-Bit-Abschnitts Index des Abschnitts enthält das Ziel. Hiermit werden Debuginformationen unterstützt. <br/>                                                                                                                                                                                                                                                             |
| Bild \_ rel \_ MIPS- \_ secrel <br/>    | 0x000B <br/> | Der 32-Bit-Offset des Ziels vom Anfang seines Abschnitts. Diese wird verwendet, um Debuginformationen und statischen lokalen Thread Speicher zu unterstützen. <br/>                                                                                                                                                                                                                       |
| Image \_ rel \_ MIPS \_ secrello <br/>  | 0x000C <br/> | Die unteren 16 Bits des 32-Bit-Offsets des Ziels vom Anfang des Abschnitts. <br/>                                                                                                                                                                                                                                                                                   |
| Image \_ rel \_ MIPS \_ secrelhi <br/>  | 0x000D <br/> | Die hohen 16 Bits des 32-Bit-Offsets des Ziels vom Anfang des Abschnitts. Die Verschiebung eines Bild- \_ rel- \_ MIPS- \_ Paars muss unmittelbar folgen. Der symboltableindex der paar Verschiebung enthält eine 16-Bit-Verschiebung mit Vorzeichen, die den oberen 16 Bits hinzugefügt wird, die von dem Speicherort entnommen werden, der verschoben wird. <br/>                            |
| Bild \_ rel \_ MIPS \_ JMPADDR16 <br/> | 0x0010 <br/> | Die unteren 26 Bits der VA des Ziels. Dadurch wird die MIPS16 JAL-Anweisung unterstützt. <br/>                                                                                                                                                                                                                                                                                           |
| Bild \_ rel \_ MIPS \_ rebwordnb <br/> | 0x0022 <br/> | Die 32-Bit-RVA des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                                |
| Bild \_ rel \_ MIPS- \_ paar <br/>      | 0x0,025 <br/> | Die Verschiebung ist nur gültig, wenn Sie unmittelbar auf eine refhi-oder secrelhi-Umsetzung folgt. Der symboltableindex-Wert enthält eine Verschiebung und keinen Index in der Symboltabelle. <br/>                                                                                                                                                                                           |



 

##### <a name="mitsubishi-m32r"></a>Mitsubishi M32R

Die folgenden Verschiebungs Typen Indikatoren sind für die Mitsubishi M32R-Prozessoren definiert.



| Konstante                               | Wert              | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bild \_ rel \_ M32R \_ absolut <br/> | 0x0000 <br/> | Die Verschiebung wird ignoriert. <br/>                                                                                                                                                                                                                                                                                                                                                                        |
| Image \_ rel \_ M32R \_ ADDR32 <br/>   | 0x0001 <br/> | Das 32-Bit-VA des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                                                           |
| Image \_ rel \_ M32R \_ ADDR32NB <br/> | 0x0002 <br/> | Die 32-Bit-RVA des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                                                          |
| Image \_ rel \_ M32R \_ ADDR24 <br/>   | 0x0003 <br/> | Die 24-Bit-VA des Ziels. <br/>                                                                                                                                                                                                                                                                                                                                                                           |
| Image \_ rel \_ M32R \_ GPREL16 <br/>  | 0x0004 <br/> | Der 16-Bit-Offset des Ziels aus dem GP-Register. <br/>                                                                                                                                                                                                                                                                                                                                                  |
| Image \_ rel \_ M32R \_ PCREL24 <br/>  | 0x0005 <br/> | Der 24-Bit-Offset des Ziels vom Programm Counter (PC), nach links um 2 Bits verschoben und mit Vorzeichen erweitert <br/>                                                                                                                                                                                                                                                                                                |
| Image \_ rel \_ M32R \_ PCREL16 <br/>  | 0x0006 <br/> | Der 16-Bit-Offset des Ziels vom PC, nach links um 2 Bits verschoben und mit Vorzeichen erweitert <br/>                                                                                                                                                                                                                                                                                                                  |
| Image \_ rel \_ M32R \_ PCREL8 <br/>   | 0x0007 <br/> | Der 8-Bit-Offset des Ziels vom PC, nach links um 2 Bits verschoben und mit Vorzeichen erweitert <br/>                                                                                                                                                                                                                                                                                                                   |
| Bild \_ rel \_ M32R \_ ref-Hälfte <br/>  | 0x0008 <br/> | Die 16 MSSB des Ziel-VA. <br/>                                                                                                                                                                                                                                                                                                                                                                     |
| Image \_ rel \_ M32R \_ Ref <br/>    | 0x0009 <br/> | Die 16 MSSB des Ziel-VA, angepasst an die lsb-Signierungs Erweiterung. Diese wird für die erste Anweisung in einer Sequenz mit zwei Anweisungen verwendet, die eine vollständige 32-Bit-Adresse lädt. Auf diese Verschiebung muss unmittelbar eine paar Verlagerung folgen, deren symboltableindex eine 16-Bit-Verschiebung mit Vorzeichen enthält, die den oberen 16 Bits hinzugefügt wird, die von dem Speicherort, der verschoben wird, entnommen werden. <br/> |
| Bild \_ rel \_ M32R \_ Reflo <br/>    | 0x000A <br/> | Die 16 lssb des Ziel-VA. <br/>                                                                                                                                                                                                                                                                                                                                                                     |
| Bild \_ rel \_ M32R \_ paar <br/>     | 0x000B <br/> | Die Verschiebung muss der Ref-Verschiebung folgen. Der symboltableindex-Wert enthält eine Verschiebung und keinen Index in der Symboltabelle. <br/>                                                                                                                                                                                                                                                             |
| Abschnitt "Image \_ rel \_ M32R" \_ <br/>  | 0x000C <br/> | Der 16-Bit-Abschnitts Index des Abschnitts, der das Ziel enthält. Hiermit werden Debuginformationen unterstützt. <br/>                                                                                                                                                                                                                                                                                  |
| Image \_ rel \_ M32R \_ secrel <br/>   | 0x000D <br/> | Der 32-Bit-Offset des Ziels vom Anfang seines Abschnitts. Diese wird verwendet, um Debuginformationen und statischen lokalen Thread Speicher zu unterstützen. <br/>                                                                                                                                                                                                                                                 |
| Image \_ rel \_ M32R \_ Token <br/>    | 0x000e <br/> | Das CLR-Token. <br/>                                                                                                                                                                                                                                                                                                                                                                                    |



 

### <a name="coff-line-numbers-deprecated"></a>COFF-Zeilennummern (veraltet)

COFF-Zeilennummern werden nicht mehr erstellt und werden in der Zukunft nicht mehr verbraucht.

COFF-Zeilennummern geben die Beziehung zwischen Code und Zeilennummern in den Quelldateien an. Das Microsoft-Format für COFF-Zeilennummern ähnelt dem Standard-COFF, aber es wurde so erweitert, dass ein einzelner Abschnitt mit Zeilennummern in mehreren Quelldateien verknüpft werden kann.

COFF-Zeilennummern bestehen aus einem Array von Datensätzen fester Länge. Der Speicherort (Dateioffset) und die Größe des Arrays werden in der Abschnitts Kopfzeile angegeben. Jeder Zeilennummern Satz weist das folgende Format auf.



| Offset        | Size          | Feld                  | BESCHREIBUNG                                                                                                                                                 |
|---------------|---------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Type ( \* ) <br/>  | Dies ist eine Kombination aus zwei Feldern: symboltableindex und virtualAddress. Ob symboltableindex oder RVA verwendet wird, hängt vom Wert von LineNumber ab. <br/> |
| 4 <br/> | 2 <br/> | LineNumber <br/> | Bei einem Wert ungleich 0 (null) gibt dieses Feld eine einzeilige Zeilennummer an. Wenn der Wert 0 (null) ist, wird das typanfeld als Symboltabellen Index für eine Funktion interpretiert. <br/>    |



 

Das typanfeld ist eine Union von 2 4-Byte-Feldern: symboltableindex und virtualAddress.



| Offset        | Size          | Feld                        | BESCHREIBUNG                                                                                                                                                                             |
|---------------|---------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Symboltableindex <br/> | Wird verwendet, wenn LineNumber NULL ist: Index-zu-Symbol-Tabelleneintrag für eine Funktion. Dieses Format wird verwendet, um die Funktion anzugeben, auf die sich eine Gruppe von Zeilennummern Datensätzen bezieht. <br/>      |
| 0 <br/> | 4 <br/> | VirtualAddress <br/>   | Wird verwendet, wenn LineNumber ungleich 0 (null) ist: die RVA des ausführbaren Codes, der der festgelegten Quellzeile entspricht. In einer Objektdatei enthält dies das VA innerhalb des Abschnitts. <br/> |



 

Ein Zeilennummern Daten Satz kann entweder das Feld "LineNumber" auf 0 (null) festlegen und auf eine Funktionsdefinition in der Symboltabelle zeigen, oder es kann als Standard-Zeilennummern Eintrag fungieren, indem eine positive Ganzzahl (Zeilennummer) und die entsprechende Adresse im Objektcode gegeben werden.

Eine Gruppe von Zeilennummern Einträgen beginnt immer mit dem ersten Format: dem Index eines Funktions Symbols. Wenn dies der erste Zeilennummern Daten Satz im-Abschnitt ist, dann ist es auch der Comdat-Symbol Name für die Funktion, wenn das Comdat-Flag des Abschnitts festgelegt ist. Siehe [COMDAT-Abschnitte (nur Objekt)](#comdat-sections-object-only). Der hilfdatensatz der Funktion in der Symboltabelle enthält einen Zeiger auf das Feld "LineNumber", das auf denselben Zeilennummern Daten Satz verweist.

Auf einen Datensatz, der eine Funktion identifiziert, folgt eine beliebige Anzahl von Zeilennummern Einträgen, die tatsächliche Zeilennummern Informationen (d. h. Einträge mit dem Wert "linenumber größer als Null") geben. Diese Einträge sind in Relation zum Anfang der Funktion 1-basiert und stellen jede Quellzeile in der Funktion außer der ersten Zeile dar.

Der erste Zeilennummern Eintrag für das folgende Beispiel würde beispielsweise die ReverseSign-Funktion angeben (symboltableindex von ReverseSign und LineNumber auf NULL festgelegt). Anschließend werden die Datensätze mit den LineNumber-Werten 1, 2 und 3 befolgt, die den folgenden Quellzeilen entsprechen:


```C++
// some code precedes ReverseSign function
int ReverseSign(int i)
1: {
2:  return -1 * i;
3: }
```



### <a name="coff-symbol-table"></a>COFF-Symbol Tabelle

Die Symboltabelle in diesem Abschnitt wird vom herkömmlichen COFF-Format geerbt. Sie unterscheidet sich von Microsoft Visual C++ Debuginformationen. Eine Datei kann sowohl eine COFF-Symboltabelle als auch Visual C++ Debuginformationen enthalten, und die beiden werden getrennt beibehalten. Einige Microsoft-Tools verwenden die Symboltabelle für begrenzte, aber wichtige Zwecke, z. b. die Kommunikation von COMDAT-Informationen an den Linker. Abschnittsnamen und Dateinamen sowie Code-und Daten Symbole werden in der Symboltabelle aufgeführt.

Der Speicherort der Symboltabelle wird im COFF-Header angegeben.

Die Symboltabelle ist ein Array von Datensätzen, die jeweils 18 Bytes lang sind. Jeder Datensatz ist entweder ein Standard-oder ein Zusatz Symboltabellen Daten Satz. Ein Standard-Datensatz definiert ein Symbol oder einen Namen und weist das folgende Format auf.



| Offset         | Size          | Feld                          | BESCHREIBUNG                                                                                                                                                                                                                                 |
|----------------|---------------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 8 <br/> | Name ( \* ) <br/>          | Der Name des Symbols, dargestellt durch eine Union von drei-Strukturen. Ein Array von 8 Bytes wird verwendet, wenn der Name nicht mehr als 8 Bytes lang ist. Weitere Informationen finden Sie unter [Symbol namens Darstellung](https://www.bing.com/search?q=Symbol+Name+Representation). <br/> |
| 8 <br/>  | 4 <br/> | Wert <br/>              | Der Wert, der dem Symbol zugeordnet ist. Die Interpretation dieses Felds hängt von "SectionNumber" und "storageclass" ab. Eine typische Bedeutung ist die wieder wiederholbare Adresse. <br/>                                                         |
| 12 <br/> | 2 <br/> | SectionNumber <br/>      | Die ganze Zahl mit Vorzeichen, die den Abschnitt mithilfe eines einbasierten Indexes in der Abschnitts Tabelle identifiziert. Einige Werte haben eine besondere Bedeutung, wie im Abschnitt "5.4.2", "section number values" definiert. <br/>                                         |
| 14 <br/> | 2 <br/> | type <br/>               | Eine Zahl, die den Typ darstellt. Microsoft-Tools legen dieses Feld auf 0x20 (Function) oder 0x0 (keine Funktion) fest. Weitere Informationen finden Sie unter [Typdarstellung](#type-representation). <br/>                                                |
| 16 <br/> | 1 <br/> | Storageclass <br/>       | Ein Enumerationswert, der die Speicher Klasse darstellt. Weitere Informationen finden Sie unter [Storage-Klasse](#storage-class). <br/>                                                                                                                   |
| 17 <br/> | 1 <br/> | "Numofauxsymbols" <br/> | Die Anzahl der Zusatz Symbol-Tabelleneinträge, die diesem Datensatz folgen. <br/>                                                                                                                                                           |



 

0 (null) oder mehrere hilfsmarttabellendaten Sätze folgen direkt den einzelnen standardmäßigen Symboltabellen Datensätzen. In der Regel wird jedoch nicht mehr als ein Zusatz Symboltabellen-Datensatz auf einen standardmäßigen Symbol Tabellendatensatz (mit Ausnahme von. File-Datensätzen mit langen Dateinamen) folgt. Jeder Erweiterungs Daten Satz hat dieselbe Größe wie ein standardmäßiger Symboltabellen Daten Satz (18 Bytes), aber anstelle eines neuen Symbols gibt der Erweiterungs Daten Satz zusätzliche Informationen über das letzte definierte Symbol aus. Welche der verschiedenen Formate verwendet werden soll, hängt vom Feld storageclass ab. Zurzeit definierte Formate für Zusatz Symboltabellen-Datensätze werden im Abschnitt 5,5, "hilfsymboldatensätze", angezeigt.

Tools, die COFF-Symboltabellen lesen, müssen zusätzliche Symbol Datensätze ignorieren, deren Interpretation unbekannt ist. Dadurch kann das Symboltabellen Format erweitert werden, um neue zusätzliche Datensätze hinzuzufügen, ohne vorhandene Tools zu unterbrechen.

#### <a name="symbol-name-representation"></a>Symbol Namen Darstellung

Das Feld "ShortName" in einer Symboltabelle besteht aus 8 Bytes, die den Namen selbst enthalten, wenn es nicht mehr als 8 Bytes lang ist, oder das Feld "ShortName" gibt einen Offset in der Zeichen folgen Tabelle an. Um zu ermitteln, ob der Name selbst oder ein Offset angegeben wird, testen Sie die ersten 4 Bytes auf Gleichheit mit 0 (null).

Gemäß der Konvention werden die Namen als mit 0 (null) beendete UTF-8-codierte Zeichen folgen behandelt.



| Offset        | Size          | Feld                 | BESCHREIBUNG                                                                                                          |
|---------------|---------------|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 8 <br/> | ShortName <br/> | Ein Array von 8 Bytes. Dieses Array wird mit NULL-Werten auf der rechten Seite aufgefüllt, wenn der Name weniger als 8 Bytes lang ist. <br/> |
| 0 <br/> | 4 <br/> | Nullen <br/>    | Ein Feld, das auf alle Nullen festgelegt wird, wenn der Name länger als 8 Bytes ist. <br/>                                     |
| 4 <br/> | 4 <br/> | Offset <br/>    | Ein Offset in der Zeichen folgen Tabelle. <br/>                                                                         |



 

#### <a name="section-number-values"></a>Abschnitts Nummern Werte

Normalerweise ist das Abschnitts Wert Feld in einem Symboltabellen Eintrag ein einbasierter Index in der Abschnitts Tabelle. Dieses Feld ist jedoch eine Ganzzahl mit Vorzeichen und kann negative Werte annehmen. Die folgenden Werte, die kleiner als 1 sind, haben eine besondere Bedeutung.



| Konstante                          | Wert          | BESCHREIBUNG                                                                                                                                                                                                                            |
|-----------------------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bild- \_ SYM nicht \_ definiert <br/> | 0 <br/>  | Dem Symbol Daten Satz wurde noch kein Abschnitt zugewiesen. Der Wert 0 (null) gibt an, dass ein Verweis auf ein externes Symbol an anderer Stelle definiert ist. Ein Wert ungleich 0 (null) ist ein gängiges Symbol mit einer Größe, die durch den-Wert angegeben wird. <br/> |
| Image- \_ SYM \_ absolut <br/>  | -1 <br/> | Das Symbol verfügt über einen absoluten (nicht wiederholbaren) Wert, und es handelt sich nicht um eine Adresse. <br/>                                                                                                                                                  |
| \_ \_ Debuggen von Images <br/>     | -2 <br/> | Das Symbol bietet allgemeine Informationen zum Typ oder Debuggen, entspricht jedoch keinem Abschnitt. Microsoft-Tools verwenden diese Einstellung zusammen mit. File-Datensätzen (Speicher Klassendatei). <br/>                                            |



 

#### <a name="type-representation"></a>Typdarstellung

Das typanfeld eines Symboltabellen Eintrags enthält 2 Bytes, wobei jedes Byte Typinformationen darstellt. Der LSB stellt den einfachen Datentyp (Base) dar, und der MSB stellt den komplexen Typ dar, falls vorhanden:



| MSB                                                       | LSB                                                        |
|-----------------------------------------------------------|------------------------------------------------------------|
| Komplexer Typ: None, Zeiger, Function, Array. <br/> | Basistyp: ganze Zahl, Gleit Komma, usw. <br/> |



 

Die folgenden Werte sind für den Basistyp definiert, obwohl Microsoft-Tools dieses Feld in der Regel nicht verwenden und der LSB nicht auf 0 festgelegt wird. Stattdessen werden Visual C++ Debuginformationen verwendet, um Typen anzugeben. Die möglichen COFF-Werte werden hier jedoch aus Gründen der Vollständigkeit aufgeführt.



| Konstante                             | Wert          | BESCHREIBUNG                                                                            |
|--------------------------------------|----------------|----------------------------------------------------------------------------------------|
| Bild- \_ SYM- \_ Typ \_ null <br/>   | 0 <br/>  | Es sind keine Typinformationen oder ein unbekannter Basistyp. Microsoft-Tools verwenden diese Einstellung. <br/> |
| Bild- \_ SYM- \_ Typ \_ void <br/>   | 1 <br/>  | Kein gültiger Typ; verwendet mit void-Zeigern und-Funktionen <br/>                       |
| Image- \_ SYM- \_ Typ \_ Char <br/>   | 2 <br/>  | Ein Zeichen (signiertes Byte) <br/>                                                  |
| Image- \_ SYM- \_ Typ \_ Short <br/>  | 3 <br/>  | Eine 2-Byte-Ganzzahl mit Vorzeichen <br/>                                                    |
| Image- \_ SYM- \_ Typ \_ int <br/>    | 4 <br/>  | Ein natürlicher ganzzahliger Typ (normalerweise 4 Bytes in Windows) <br/>                       |
| Bild- \_ SYM- \_ Typ \_ Long <br/>   | 5 <br/>  | Eine 4-Byte-Ganzzahl mit Vorzeichen <br/>                                                    |
| Bild- \_ SYM- \_ Typ \_ float <br/>  | 6 <br/>  | Eine 4-Byte-Gleit Komma Zahl <br/>                                             |
| Image- \_ SYM- \_ Typ \_ Double <br/> | 7 <br/>  | Eine 8-Byte-Gleit Komma Zahl <br/>                                            |
| Bild- \_ SYM- \_ \_ Typstruktur <br/> | 8 <br/>  | Eine-Struktur <br/>                                                                |
| Bild- \_ SYM- \_ Typ \_ Union <br/>  | 9 <br/>  | Eine Union <br/>                                                                    |
| Image- \_ SYM- \_ Typ-Aufzählung \_ <br/>   | 10 <br/> | Ein enumerierter Typ <br/>                                                         |
| Bild- \_ SYM- \_ Typ \_ <br/>    | 11 <br/> | Ein Member der-Enumeration (ein bestimmter Wert). <br/>                                 |
| Bild- \_ SYM- \_ Typ \_ Byte <br/>   | 12 <br/> | Ein Byte; nicht signierte 1-Byte-Ganzzahl <br/>                                            |
| Bild- \_ SYM- \_ Typ \_ Wort <br/>   | 13 <br/> | Ein Wort; ganze 2-Byte-Ganzzahl ohne Vorzeichen <br/>                                            |
| Bild- \_ SYM- \_ Typ \_ uint <br/>   | 14 <br/> | Eine Ganzzahl ohne Vorzeichen von natürlicher Größe (normalerweise 4 Bytes) <br/>                    |
| Image- \_ SYM- \_ Typ \_ DWORD <br/>  | 15 <br/> | Eine ganze 4-Byte-Ganzzahl ohne Vorzeichen <br/>                                                 |



 

Das signifikanteste Byte gibt an, ob das Symbol ein Zeiger auf, eine Funktions Rückgabe oder ein Array des Basistyps ist, das im lsb angegeben ist. Microsoft-Tools verwenden dieses Feld nur, um anzugeben, ob das Symbol eine Funktion ist, sodass nur zwei resultierende Werte für das typanfeld 0x0 und 0x20 sind. Allerdings können andere Tools dieses Feld verwenden, um weitere Informationen zu kommunizieren.

Es ist sehr wichtig, das Funktions Attribut ordnungsgemäß anzugeben. Diese Informationen sind erforderlich, damit die inkrementelle Verknüpfung ordnungsgemäß funktioniert. Für einige Architekturen sind die Informationen möglicherweise für andere Zwecke erforderlich.



| Konstante                                | Wert         | BESCHREIBUNG                                                          |
|-----------------------------------------|---------------|----------------------------------------------------------------------|
| Image- \_ SYM \_ dtype \_ null <br/>     | 0 <br/> | Kein abgeleiteter Typ; das Symbol ist eine einfache skalare Variable. <br/> |
| Image- \_ SYM- \_ dtype- \_ Zeiger <br/>  | 1 <br/> | Das Symbol ist ein Zeiger auf den Basistyp. <br/>                    |
| Image- \_ SYM- \_ dtype- \_ Funktion <br/> | 2 <br/> | Das Symbol ist eine Funktion, die einen Basistyp zurückgibt. <br/>       |
| Image- \_ SYM- \_ dtype- \_ Array <br/>    | 3 <br/> | Das Symbol ist ein Array des Basistyps. <br/>                     |



 

#### <a name="storage-class"></a>Speicherklasse

Das Feld storageclass der Symboltabelle gibt an, welche Art von Definition ein Symbol darstellt. In der folgenden Tabelle sind die möglichen Werte aufgeführt. Beachten Sie, dass das Feld storageclass eine ganze Zahl ohne Vorzeichen mit einer Länge von 1 Byte ist. Der spezielle Wert "-1" sollte daher mit dem unsignierten Äquivalent "0xFF" gemeint sein.

Obwohl das herkömmliche COFF-Format viele Speicher Klassen Werte verwendet, verwenden Microsoft-Tools für die meisten symbolischen Informationen Visual C++ debugformat und verwenden im Allgemeinen nur vier Werte für die Speicher Klasse: extern (2), static (3), Function (101) und File (103). Mit Ausnahme der zweiten Spaltenüberschrift sollte "Value" als Mittelwert für das Wertfeld des Symbol Datensatzes, dessen Interpretation von der als Speicher Klasse gefundenen Zahl abhängt, verwendet werden.



| Konstante                                          | Wert                 | Beschreibung/Interpretation des Wertfelds                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ Ende \_ der \_ Funktion der SYM-Image Klasse <br/>  | -1 (0xFF) <br/> | Ein spezielles Symbol, das das Ende der Funktion zu Debuggingzwecken darstellt. <br/>                                                                                                                                                                                                                                                  |
| Image- \_ SYM- \_ Klasse \_ null <br/>               | 0 <br/>         | Keine zugewiesene Speicher Klasse. <br/>                                                                                                                                                                                                                                                                                                     |
| Abbild- \_ SYM- \_ Klasse \_ automatisch <br/>          | 1 <br/>         | Die automatische (Stapel-) Variable. Das Wertfeld gibt den Stapel Rahmen Offset an. <br/>                                                                                                                                                                                                                                              |
| Image- \_ SYM- \_ Klasse \_ extern <br/>           | 2 <br/>         | Ein Wert, der von Microsoft-Tools für externe Symbole verwendet wird. Das Wertfeld gibt die Größe an, wenn die Abschnitts Nummer Bild- \_ SYM nicht \_ definiert (0) ist. Wenn die Abschnitts Nummer nicht 0 (null) ist, gibt das Wertfeld den Offset innerhalb des Abschnitts an. <br/>                                                                                 |
| Image- \_ SYM- \_ Klasse \_ statisch <br/>             | 3 <br/>         | Der Offset des Symbols innerhalb des Abschnitts. Wenn das Wertfeld NULL ist, stellt das Symbol einen Abschnittsnamen dar. <br/>                                                                                                                                                                                                            |
| Image- \_ SYM- \_ Klassen \_ Register <br/>           | 4 <br/>         | Eine Register Variable. Das Wertfeld gibt die Registernummer an. <br/>                                                                                                                                                                                                                                                            |
| Image- \_ SYM- \_ Klasse \_ extern \_ DEF <br/>      | 5 <br/>         | Ein Symbol, das extern definiert wird. <br/>                                                                                                                                                                                                                                                                                           |
| Bild- \_ SYM- \_ Klassen \_ Bezeichnung <br/>              | 6 <br/>         | Eine Code Bezeichnung, die im Modul definiert ist. Das Wertfeld gibt den Offset des Symbols innerhalb des Abschnitts an. <br/>                                                                                                                                                                                                         |
| Image- \_ SYM- \_ Klasse nicht \_ definierte \_ Bezeichnung <br/>   | 7 <br/>         | Ein Verweis auf eine Code Bezeichnung, die nicht definiert ist. <br/>                                                                                                                                                                                                                                                                               |
| \_Member-SYM- \_ \_ Klassenmember \_ der \_ Struktur <br/> | 8 <br/>         | Der Strukturmember. Das Wertfeld gibt das n-te Element an. <br/>                                                                                                                                                                                                                                                               |
| Image- \_ SYM- \_ Klassen \_ Argument <br/>           | 9 <br/>         | Ein formales Argument (-Parameter) einer Funktion. Das Feld Wert gibt das n-te Argument an. <br/>                                                                                                                                                                                                                                      |
| Strukturtag der \_ SYM-System \_ Klasse \_ \_ <br/>        | 10 <br/>        | Der Name des strukturtagnamens. <br/>                                                                                                                                                                                                                                                                                                  |
| Image- \_ SYM- \_ \_ Klassenmember \_ der \_ Union <br/>  | 11 <br/>        | Ein Union-Member. Das Wertfeld gibt das n-te Element an. <br/>                                                                                                                                                                                                                                                                     |
| Union-Tag der Bild- \_ SYM- \_ Klasse \_ \_ <br/>         | 12 <br/>        | Der Union-Tagnamens Eintrag. <br/>                                                                                                                                                                                                                                                                                                      |
| Typdefinition für Bild- \_ SYM- \_ Klasse \_ \_ <br/>   | 13 <br/>        | Ein TypeDef-Eintrag. <br/>                                                                                                                                                                                                                                                                                                               |
| Bild- \_ SYM- \_ Klasse nicht \_ definiert \_ statisch <br/>  | 14 <br/>        | Eine statische Daten Deklaration. <br/>                                                                                                                                                                                                                                                                                                     |
| Bild der \_ SYM- \_ Klasse enumerationstag \_ \_ <br/>          | 15 <br/>        | Ein Enumerationstyp Tagname-Eintrag. <br/>                                                                                                                                                                                                                                                                                              |
| \_Member-SYM- \_ \_ Klassenmember \_ von \_ enum <br/>   | 16 <br/>        | Ein Member einer Enumeration. Das Wertfeld gibt das n-te Element an. <br/>                                                                                                                                                                                                                                                         |
| Abbild- \_ SYM- \_ Klassen \_ Register \_ param <br/>    | 17 <br/>        | Ein Register-Parameter. <br/>                                                                                                                                                                                                                                                                                                          |
| Bitfeld für Bild- \_ SYM- \_ Klasse \_ \_ <br/>         | 18 <br/>        | Ein Bitfeld Verweis. Das Wertfeld gibt das n-te Bit im Bitfeld an. <br/>                                                                                                                                                                                                                                                |
| Image- \_ SYM- \_ Klassen \_ Block <br/>              | 100 <br/>       | Der Datensatz A. BB (Anfang des Blocks) oder. EB (Ende des Blocks). Das Wertfeld ist die wieder ersetz Bare Adresse des Code Speicher Orts. <br/>                                                                                                                                                                                                      |
| Image- \_ SYM- \_ Klassen \_ Funktion <br/>           | 101 <br/>       | Ein Wert, den Microsoft-Tools für Symbol Datensätze verwenden, die den Umfang einer Funktion definieren: begin Function (. BF), End Function (. EF) und Lines in Function (. LF). Für. LF-Einträge gibt das Wertfeld die Anzahl der Quellzeilen in der Funktion an. Für EF-Einträge gibt das Wertfeld die Größe des Funktions Codes an. <br/> |
| Bild \_ der SYM- \_ Klasse \_ Ende \_ der \_ Struktur <br/>    | 102 <br/>       | Ein End-of-Structure-Eintrag. <br/>                                                                                                                                                                                                                                                                                                     |
| Image- \_ SYM- \_ Klassen \_ Datei <br/>               | 103 <br/>       | Ein Wert, der von Microsoft-Tools und herkömmlichem COFF-Format für den Quelldatei-Symbol Daten Satz verwendet wird. Auf das Symbol folgen zusätzliche Datensätze, die die Datei benennen. <br/>                                                                                                                                                       |
| Bild- \_ SYM- \_ Klassen \_ Abschnitt <br/>            | 104 <br/>       | Eine Definition eines Abschnitts (Microsoft-Tools verwenden stattdessen eine statische Speicher Klasse). <br/>                                                                                                                                                                                                                                                  |
| Bild- \_ SYM- \_ Klasse \_ schwache \_ externe <br/>     | 105 <br/>       | Eine schwache externe. Weitere Informationen finden Sie unter [Zusatz Format 3: schwache externale](#auxiliary-format-3-weak-externals). <br/>                                                                                                                                                                                                           |
| Image- \_ SYM- \_ Klasse \_ CLR- \_ Token <br/>         | 107 <br/>       | Ein CLR-tokensymbol. Der Name ist eine ASCII-Zeichenfolge, die aus dem hexadezimalen Wert des Tokens besteht. Weitere Informationen finden Sie unter [CLR-tokendefinition (nur Objekt)](#clr-token-definition-object-only). <br/>                                                                                                                        |



 

### <a name="auxiliary-symbol-records"></a>Zusatz Symbol Datensätze

Erweiterungs Symboltabellen-Datensätze folgen immer und gelten für einige standardmäßige Symboltabellen Datensätze. Ein hilfssdatensatz kann ein beliebiges Format aufweisen, das von den Tools erkannt werden kann. es müssen jedoch 18 Bytes zugeordnet werden, damit die Symboltabelle als Array regulärer Größe beibehalten wird. Derzeit erkennen Microsoft-Tools zusätzliche Formate für die folgenden Arten von Datensätzen: Funktionsdefinitionen, Start-und Endsymbole von Funktionen (. BF und EF), schwache externale, Dateinamen und Abschnitts Definitionen.

Der herkömmliche COFF-Entwurf umfasst auch Erweiterungs Datensatzformate für Arrays und Strukturen. Microsoft-Tools verwenden diese nicht, sondern platzieren diese symbolischen Informationen in Visual C++ debugformat in den Debug-Abschnitten.

#### <a name="auxiliary-format-1-function-definitions"></a>Erweiterungs Format 1: Funktionsdefinitionen

Ein Symboltabellen Daten Satz markiert den Anfang einer Funktionsdefinition, wenn er Folgendes aufweist: eine Speicher Klasse von extern (2), ein Typwert, der angibt, dass es sich um eine Funktion (0x20) und eine Abschnitts Nummer handelt, die größer als 0 (null) ist. Beachten Sie, dass ein Symboltabellen Daten Satz mit der Abschnitts Nummer undefiniert (0) die Funktion nicht definiert und keinen zusätzlichen Datensatz enthält. Auf die Funktions Definitions Symbol-Einträge folgt ein hilfssdatensatz in dem unten beschriebenen Format:



| Offset         | Size          | Feld                             | BESCHREIBUNG                                                                                                                                                                                                                   |
|----------------|---------------|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Tagindex <br/>              | Der Symboltabellen Index des entsprechenden. BF (BEGIN Function)-Symbol Datensatzes. <br/>                                                                                                                                   |
| 4 <br/>  | 4 <br/> | TotalSize <br/>             | Die Größe des ausführbaren Codes für die Funktion selbst. Wenn sich die Funktion in einem eigenen Abschnitt befindet, ist sizeofrawdata im Abschnitts Header größer als oder gleich diesem Feld, abhängig von den Ausrichtungs Überlegungen. <br/> |
| 8 <br/>  | 4 <br/> | Pointertolinenumber <br/>   | Der Dateioffset des ersten COFF-Zeilennummern Eintrags für die Funktion, oder 0 (null), wenn keiner vorhanden ist. Weitere Informationen finden Sie unter [COFF-Zeilennummern (veraltet)](#coff-line-numbers-deprecated). <br/>                          |
| 12 <br/> | 4 <br/> | Pointertonextfunction <br/> | Der Symboltabellen Index des Datensatzes für die nächste Funktion. Wenn die Funktion der letzte in der Symboltabelle ist, wird dieses Feld auf 0 (null) festgelegt. <br/>                                                                           |
| 16 <br/> | 2 <br/> | Nicht verwendet <br/>                |                                                                                                                                                                                                                               |



 

#### <a name="auxiliary-format-2-bf-and-ef-symbols"></a>Erweiterungs Format 2:. BF-und EF-Symbole

Für jede Funktionsdefinition in der Symboltabelle beschreiben drei Elemente den Anfang, das Beenden und die Anzahl der Zeilen. Jedes dieser Symbole verfügt über eine Speicher Klassen Funktion (101):

Ein Symbol Daten Satz mit dem Namen. BF (BEGIN Function). Das Wertfeld wird nicht verwendet.

Ein Symbol Daten Satz mit dem Namen. LF (Zeilen in Function). Das Wertfeld gibt die Anzahl der Zeilen in der Funktion an.

Ein Symbol Daten Satz mit dem Namen. EF (Ende der Funktion). Das Feld Wert weist die gleiche Zahl wie das Feld Gesamtgröße im Funktions Definitions Symbol-Datensatz auf.

Auf die Symbol Datensätze ". BF" und ". EF" (aber keine ". LF"-Einträge) folgt ein hilfssdatensatz mit dem folgenden Format:



| Offset         | Size          | Feld                                         | BESCHREIBUNG                                                                                                                                                                   |
|----------------|---------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Nicht verwendet <br/>                            |                                                                                                                                                                               |
| 4 <br/>  | 2 <br/> | LineNumber <br/>                        | Die tatsächliche ordinalzeilennummer (1, 2, 3 usw.) in der Quelldatei, die dem. BF-oder. EF-Datensatz entspricht. <br/>                                               |
| 6 <br/>  | 6 <br/> | Nicht verwendet <br/>                            |                                                                                                                                                                               |
| 12 <br/> | 4 <br/> | Pointertonextfunction (nur. BF) <br/> | Der Symboltabellen Index des nächsten. BF-Symbol Datensatzes. Wenn die Funktion der letzte in der Symboltabelle ist, wird dieses Feld auf 0 (null) festgelegt. Er wird nicht für EF-Datensätze verwendet. <br/> |
| 16 <br/> | 2 <br/> | Nicht verwendet <br/>                            |                                                                                                                                                                               |



 

#### <a name="auxiliary-format-3-weak-externals"></a>Zusatz Format 3: schwache externals

"Schwache externale" sind ein Mechanismus für Objektdateien, der die Flexibilität zur Verknüpfungs Zeit ermöglicht. Ein Modul kann ein nicht aufgelöstes externes Symbol (SYM1) enthalten. es kann jedoch auch einen zusätzlichen Datensatz enthalten, der angibt, dass, wenn SYM1 nicht zur Verknüpfungs Zeit vorhanden ist, stattdessen ein anderes externes Symbol (SyM2) zum Auflösen von Verweisen verwendet wird.

Wenn eine Definition von SYM1 verknüpft ist, wird ein externer Verweis auf das Symbol normal aufgelöst. Wenn eine Definition von SYM1 nicht verknüpft ist, beziehen sich alle Verweise auf das schwache externe für SYM1 stattdessen auf SyM2. Das externe Symbol, SyM2, muss immer verknüpft werden. in der Regel wird Sie im Modul definiert, das den schwachen Verweis auf SYM1 enthält.

Schwache externale werden durch einen Symboltabellen Daten Satz mit externer Speicher Klasse, undef-Abschnitts Nummer und einem Wert von 0 (null) dargestellt. Auf den schwach externen Symbol Daten Satz folgt ein hilfssdatensatz mit dem folgenden Format:



| Offset        | Size           | Feld                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                |
|---------------|----------------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/>  | Tagindex <br/>        | Der Symboltabellen Index von SyM2, das Symbol, das verknüpft werden soll, wenn SYM1 nicht gefunden wird. <br/>                                                                                                                                                                                                                                                                  |
| 4 <br/> | 4 <br/>  | Merkmale <br/> | Der Wert Image \_ Weak \_ extern \_ Search \_ nolibrary gibt an, dass keine Bibliotheks Suche für SYM1 ausgeführt werden soll. <br/> Ein Wert der Bild \_ schwachen \_ externen \_ Such \_ Bibliothek gibt an, dass eine Bibliotheks Suche für SYM1 durchgeführt werden soll. <br/> Ein Wert von Image \_ Weak \_ extern \_ Search \_ Alias gibt an, dass SYM1 ein Alias für SyM2 ist. <br/> |
| 8 <br/> | 10 <br/> | Nicht verwendet <br/>          |                                                                                                                                                                                                                                                                                                                                                            |



 

Beachten Sie, dass das Feld "Merkmale" nicht in WinNT definiert ist. Micha Stattdessen wird das Feld Gesamtgröße verwendet.

#### <a name="auxiliary-format-4-files"></a>Erweiterungs Format 4: Dateien

Dieses Format folgt einem Symboltabellen Daten Satz mit der Speicher Klassendatei (103). Der Symbol Name selbst sollte. File lauten, und der darauf folgende hilfsdatensatz gibt den Namen einer Quell Code Datei an.



| Offset        | Size           | Feld                 | BESCHREIBUNG                                                                                                                         |
|---------------|----------------|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 18 <br/> | Dateiname <br/> | Eine ANSI-Zeichenfolge, die den Namen der Quelldatei enthält. Diese wird mit Nullen aufgefüllt, wenn Sie kleiner als die maximale Länge ist. <br/> |



 

#### <a name="auxiliary-format-5-section-definitions"></a>Zusatz Format 5: Abschnitts Definitionen

Dieses Format folgt einem Symboltabellen Daten Satz, der einen Abschnitt definiert. Ein solcher Datensatz hat einen Symbolnamen, bei dem es sich um den Namen eines Abschnitts handelt (z. b.. Text oder. drectve) und die Speicher Klasse static (3) aufweist. Der Zusatzdaten Satz enthält Informationen zu dem Abschnitt, auf den er verweist. Daher werden einige der Informationen in der Abschnitts Kopfzeile dupliziert.



| Offset         | Size          | Feld                           | BESCHREIBUNG                                                                                                                                                                                                             |
|----------------|---------------|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Länge <br/>              | Die Größe der Abschnitts Daten; identisch mit sizeofrawdata im Abschnitts Header. <br/>                                                                                                                                  |
| 4 <br/>  | 2 <br/> | Numofrelocations <br/> | Die Anzahl der Verschiebungs Einträge für den Abschnitt. <br/>                                                                                                                                                           |
| 6 <br/>  | 2 <br/> | Nummerioflinenumber <br/> | Die Anzahl der Zeilennummern Einträge für den Abschnitt. <br/>                                                                                                                                                          |
| 8 <br/>  | 4 <br/> | Prüfsumme <br/>            | Die Prüfsumme für die gemeinsamen Daten. Dies ist anwendbar, wenn das Image \_ SCN \_ lnk \_ COMDAT-Flag in der Abschnitts Kopfzeile festgelegt ist. Weitere Informationen finden Sie unter [COMDAT-Abschnitte (nur Objekt)](#comdat-sections-object-only). <br/> |
| 12 <br/> | 2 <br/> | Number <br/>              | Ein einbasierter Index in der Abschnitts Tabelle für den zugeordneten Abschnitt. Diese Option wird verwendet, wenn die COMDAT-Auswahl Einstellung 5 ist. <br/>                                                                                     |
| 14 <br/> | 1 <br/> | Auswahl <br/>           | Die COMDAT-Auswahl Nummer. Dies ist anwendbar, wenn der Abschnitt ein COMDAT-Abschnitt ist. <br/>                                                                                                                         |
| 15 <br/> | 3 <br/> | Nicht verwendet <br/>              |                                                                                                                                                                                                                         |



 

#### <a name="comdat-sections-object-only"></a>COMDAT-Abschnitte (nur Objekt)

Das Auswahlfeld des Abschnitts Definitions-Erweiterungs Formats ist anwendbar, wenn der Abschnitt ein COMDAT-Abschnitt ist. Ein COMDAT-Abschnitt ist ein Abschnitt, der durch mehr als eine Objektdatei definiert werden kann. (Das flagbild \_ SCN \_ lnk \_ COMDAT wird im Abschnitts Feld Flags des Abschnitts Headers festgelegt.) Das Auswahlfeld bestimmt die Art und Weise, in der der Linker die mehrfach Definitionen von COMDAT-Abschnitten auflöst.

Das erste Symbol, das den Abschnitts Wert des COMDAT-Abschnitts enthält, muss das Abschnitts Symbol sein. Dieses Symbol hat den Namen des Abschnitts, das Wertfeld gleich NULL, die Abschnitts Nummer des fraglichen COMDAT-Abschnitts, das typanfeld gleich dem Bild- \_ SYM \_ -Typ \_ NULL, das Klassenfeld gleich der Bild \_ \_ -SYM \_ -Klasse static und einen zusätzlichen Datensatz. Das zweite Symbol wird als "Comdat-Symbol" bezeichnet und wird vom Linker in Verbindung mit dem Auswahlfeld verwendet.

Die Werte für das Auswahlfeld sind unten dargestellt.



| Konstante                                        | Wert         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Image- \_ COMDAT \_ Select- \_ noduplicates <br/> | 1 <br/> | Wenn dieses Symbol bereits definiert ist, gibt der Linker einen Fehler vom Typ "mit dem multiplizieren definierter Symbol" aus. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Bild \_ COMDAT \_ Select \_ Any <br/>          | 2 <br/> | Jeder Abschnitt, der das gleiche Comdat-Symbol definiert, kann verknüpft werden. der Rest wird entfernt. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Bild \_ COMDAT \_ Wählen Sie \_ dieselbe \_ Größe aus. <br/>   | 3 <br/> | Der Linker wählt einen willkürlichen Abschnitt unter den Definitionen für dieses Symbol aus. Wenn alle Definitionen nicht die gleiche Größe haben, wird der Fehler "Fehler beim Multiplizieren von Symbolen" ausgegeben. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| \_bildcomdat \_ Select \_ Exact \_ Match <br/> | 4 <br/> | Der Linker wählt einen willkürlichen Abschnitt unter den Definitionen für dieses Symbol aus. Wenn alle Definitionen nicht exakt übereinstimmen, wird ein Fehler vom Typ "Symbol für mehrfach definierte Symbole" ausgegeben. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Bild \_ COMDAT \_ Select \_ associative <br/>  | 5 <br/> | Der Abschnitt ist verknüpft, wenn ein bestimmter anderer COMDAT-Abschnitt verknüpft ist. Dieser andere Abschnitt wird durch das Zahlenfeld des zusätzlichen Symbol Datensatzes für die Abschnitts Definition angegeben. Diese Einstellung ist nützlich für Definitionen, die über Komponenten in mehreren Abschnitten verfügen (z. b. Code in einem und Daten in einem anderen), wobei all als Satz verknüpft oder verworfen werden muss. Der andere Abschnitt, dem dieser Abschnitt zugeordnet ist, muss ein COMDAT-Abschnitt sein, bei dem es sich um einen weiteren assoziativen COMDAT-Abschnitt handeln kann. Die Abschnitts Zuordnungs Kette eines assoziativen COMDAT-Abschnitts kann keine Schleife bilden. Die Abschnitts Zuordnungs Kette muss schließlich zu einem COMDAT-Abschnitt kommen, der nicht über die Image \_ COMDAT \_ Select \_ associative Set verfügt. <br/> |
| Bild \_ COMDAT- \_ Auswahl am \_ größten <br/>      | 6 <br/> | Der Linker wählt die größte Definition aus allen Definitionen für dieses Symbol aus. Wenn mehrere Definitionen über diese Größe verfügen, ist die Wahl zwischen Ihnen willkürlich. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                |



 

#### <a name="clr-token-definition-object-only"></a>CLR-tokendefinition (nur Objekt)

Dieses hilfsymbol folgt in der Regel der Abbild- \_ SYM- \_ Klasse \_ CLR- \_ Token. Sie wird verwendet, um dem Namespace der COFF-Symboltabelle ein Token zuzuordnen.



| Offset        | Size           | Feld                        | BESCHREIBUNG                                                                                |
|---------------|----------------|------------------------------|--------------------------------------------------------------------------------------------|
| 0 <br/> | 1 <br/>  | bauxtype <br/>         | Muss das Image- \_ aux- \_ \_ Symboltyp \_ Token \_ DEF (1) sein. <br/>                              |
| 1 <br/> | 1 <br/>  | überarbeitete <br/>        | Reserviert, muss NULL sein. <br/>                                                        |
| 2 <br/> | 4 <br/>  | Symboltableindex <br/> | Der Symbol Index des COFF-Symbols, auf das diese CLR-tokendefinition verweist. <br/> |
| 6 <br/> | 12 <br/> |                              | Reserviert, muss NULL sein. <br/>                                                        |



 

### <a name="coff-string-table"></a>COFF-Zeichen folgen Tabelle

Unmittelbar nach der COFF-Symboltabelle ist die COFF-Zeichen folgen Tabelle. Die Position dieser Tabelle wird gefunden, indem die Symboltabellen Adresse im COFF-Header übernommen und die Anzahl der Symbole multipliziert mit der Größe eines Symbols hinzugefügt wird.

Am Anfang der COFF-Zeichen folgen Tabelle sind 4 Bytes, die die Gesamtgröße (in Bytes) der restlichen Zeichen folgen Tabelle enthalten. Diese Größe schließt das Größen Feld selbst ein, sodass der Wert an dieser Position 4 lauten würde, wenn keine Zeichen folgen vorhanden wären.

Nach der Größe handelt es sich um NULL-terminierte Zeichen folgen, auf die durch Symbole in der COFF-Symboltabelle gezeigt wird.

### <a name="the-attribute-certificate-table-image-only"></a>Attribut Zertifikat Tabelle (nur Bild)

Attribut Zertifikate können einem Image durch Hinzufügen einer Attribut Zertifikat Tabelle zugeordnet werden. Die Attribut Zertifikat Tabelle besteht aus einem Satz zusammenhängender Attribut Zertifikat Einträge mit Quadword-Ausrichtung. NULL-Auffüll Zeichen werden zwischen dem ursprünglichen Dateiende und dem Anfang der Attribut Zertifikat Tabelle eingefügt, um diese Ausrichtung zu erzielen. Jeder Attribut Zertifikat Eintrag enthält die folgenden Felder.



| Offset       | Size                         | Feld                       | BESCHREIBUNG                                                                                                |
|--------------|------------------------------|-----------------------------|------------------------------------------------------------------------------------------------------------|
| 0<br/> | 4<br/>                 | dwLength<br/>         | Gibt die Länge des Attribut Zertifikat Eintrags an. <br/>                                       |
| 4<br/> | 2<br/>                 | wrevision<br/>        | Enthält die Nummer der Zertifikat Version. Weitere Informationen finden Sie im folgenden Text.<br/>                   |
| 6<br/> | 2<br/>                 | wcertifialisietype<br/> | Gibt den Typ des Inhalts in bcertificate an. Weitere Informationen finden Sie im folgenden Text.<br/>             |
| 8<br/> | Finden Sie hier<br/> | bcertificate<br/>     | Enthält ein Zertifikat, z. b. eine Authenticode-Signatur. Weitere Informationen finden Sie im folgenden Text.<br/> |



 

Der Wert der virtuellen Adresse aus dem Zertifikat Tabelleneintrag im optionalen Header Datenverzeichnis ist ein Dateioffset zum ersten Attribut Zertifikat Eintrag. Der Zugriff auf nachfolgende Einträge erfolgt durch die Weiterentwicklung der dwLength-Bytes dieses Eintrags (aufgerundet auf ein 8-Byte-vielfache) vom Beginn des aktuellen Attribut Zertifikat Eintrags. Dies wird so lange fortgesetzt, bis die Summe der gerundeten dwLength-Werte dem Größen Wert aus dem Zertifikat Tabelleneintrag im optionalen Header Datenverzeichnis gleich ist. Wenn die Summe der gerundeten dwLength-Werte nicht gleich dem Größen Wert ist, ist entweder die Attribut Zertifikat Tabelle oder das Größen Feld beschädigt.

Wenn beispielsweise der Zertifikat Tabelleneintrag des optionalen Header Datenverzeichnisses Folgendes enthält:


```C++
virtual address = 0x5000
size = 0x1000
```



Das erste Zertifikat beginnt bei einem Offset von 0x5.000 vom Start der Datei auf dem Datenträger. So fahren Sie alle Attribut Zertifikat Einträge fort:

1.  Fügen Sie dem Start Offset den Wert dwLength des ersten Attribut Zertifikats hinzu.
2.  Runden Sie den Wert aus Schritt 1 bis zum nächsten 8-Byte-vielfachen ab, um den Offset des zweiten Attribut Zertifikat Eintrags zu ermitteln.
3.  Fügen Sie den Offset Wert aus Schritt 2 dem dwLength-Wert des zweiten Attribut Zertifikat Eintrags hinzu, und führen Sie eine Aufrundung auf das nächste 8-Byte-vielfache aus, um den Offset des dritten Attribut Zertifikats zu bestimmen.
4.  Wiederholen Sie Schritt 3 für jedes nachfolgende Zertifikat, bis der berechnete Offset 0x6000 (0x5.000 Start + 0x1000 Gesamtgröße) ist. Dies bedeutet, dass Sie die gesamte Tabelle durchlaufen haben.

Alternativ dazu können Sie die Zertifikat Einträge auflisten, indem Sie die Win32 **imageenumeratecertificates** -Funktion in einer-Schleife aufrufen. Einen Link zur Referenzseite der Funktion finden Sie unter [Verweise](#references).

Attribut Zertifikat-Tabelleneinträge können beliebige Zertifikat Typen enthalten, solange der Eintrag über den richtigen dwLength-Wert, einen eindeutigen wrevision-Wert und einen eindeutigen wcertifikatetype-Wert verfügt. Der häufigste Typ eines Zertifikats Tabellen Eintrags ist eine Win \_ -Zertifikat Struktur, die in wintrust. h dokumentiert und im restlichen Teil dieses Abschnitts erläutert wird.

Die Optionen für das Mitglied "Win \_ Certificate **wrevision** " umfassen Folgendes:



| Wert             | Name                                 | Notizen                                                                                                                                                 |
|-------------------|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0100<br/> | Win \_ CERT \_ Revision \_ 1 \_ 0<br/> | Version 1, ältere Version der Win- \_ Zertifikat Struktur. Sie wird nur zum Überprüfen von Legacy-Authenticode-Signaturen unterstützt.<br/> |
| 0x0200<br/> | Win \_ CERT \_ Revision \_ 2 \_ 0<br/> | Version 2 ist die aktuelle Version der Win- \_ Zertifikat Struktur. <br/>                                                                       |



 

Die Optionen für das Mitglied "Win \_ Certificate **wcertifikatetype** " umfassen die Elemente in der folgenden Tabelle (sind aber nicht darauf beschränkt). Beachten Sie, dass einige Werte derzeit nicht unterstützt werden.



| Wert             | Name                                           | Notizen                                                                                   |
|-------------------|------------------------------------------------|-----------------------------------------------------------------------------------------|
| 0x0001<br/> | Win \_ CERT \_ Type \_ X509 <br/>              | bcertificate enthält ein X. 509-Zertifikat. <br/> Nicht unterstützt<br/>         |
| 0x0002<br/> | Win \_ CERT \_ Type \_ PKCS \_ signierte \_ Daten<br/> | bcertificate enthält eine PKCS \# 7-SignedData-Struktur.<br/>                         |
| 0x0003<br/> | Win \_ CERT \_ Type \_ reserviert \_ 1<br/>        | Reserviert <br/>                                                                    |
| 0x0004<br/> | Windows- \_ Zertifikat \_ Typen- \_ \_ Stapel \_ signiert<br/>  | Signatur des Terminal Server Protokoll-Stapel Zertifikats <br/> Nicht unterstützt<br/> |



 

Der \_ **bcertificate** -Member der Win-Zertifikat Struktur enthält ein Bytearray variabler Länge mit dem durch **wcertifieretype** angegebenen Inhaltstyp. Der von Authenticode unterstützte Typ ist Win \_ CERT \_ Type \_ PKCS \_ Signed \_ Data, eine PKCS \# 7 **SignedData** -Struktur. Ausführliche Informationen zum Format der digitalen Signatur von Authenticode finden Sie unter [Signatur Format der portablen Windows Authenticode-ausführbaren Datei](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/Authenticode_PE.docx).

Wenn der **bcertificate** -Inhalt nicht an der Quadword-Grenze endet, wird der Attribut Zertifikat Eintrag mit Nullen aufgefüllt, vom Ende der **bcertificate** bis zur nächsten Quadword-Grenze.

Der **dwLength** -Wert ist die Länge der abgeschlossenen Win \_ -Zertifikat Struktur und wird wie folgt berechnet:

`dwLength = offsetof(WIN_CERTIFICATE, bCertificate) + (size of the variable-length binary array contained within bCertificate)`

Diese Länge sollte die Größe der Auffüll Zeichen enthalten, die verwendet wird, um die Anforderung zu erfüllen, dass jede Win- \_ Zertifikat Struktur in Quadword ausgerichtet ist:

` dwLength += (8 - (dwLength & 7)) & 7;`

Die **Größe der Zertifikat Tabelle**, die in den Zertifikat **Tabellen** Einträgen in den [optionalen Header Daten Verzeichnissen (nur Bild)](#optional-header-data-directories-image-only)angegeben ist, enthält die Auffüll Zeichen.

Weitere Informationen zur Verwendung der imagehlp-API zum Auflisten, hinzufügen und Entfernen von Zertifikaten aus PE-Dateien finden Sie unter [imagehlp Functions](imagehlp-functions.md).

#### <a name="certificate-data"></a>Zertifikat Daten

Wie im vorherigen Abschnitt erwähnt, können die Zertifikate in der Attribut Zertifikat Tabelle jeden beliebigen Zertifikattyp enthalten. Zertifikate, die sicherstellen, dass die Integrität einer PE-Datei einen PE-Abbild Hash enthält.

Ein PE-bildhash (oder Dateihash) ähnelt einer Datei Prüf Summe darin, dass der Hash Algorithmus einen Nachrichten Digest erzeugt, der sich auf die Integrität einer Datei bezieht. Eine Prüfsumme wird jedoch von einem einfachen Algorithmus erzeugt und wird hauptsächlich verwendet, um zu erkennen, ob ein Speicherblock auf dem Datenträger beschädigt war und die dort gespeicherten Werte beschädigt wurden. Ein Dateihash ähnelt einer Prüfsumme darin, dass auch Datei Beschädigungen erkannt werden. Anders als bei den meisten Prüfsummen Algorithmen ist es jedoch sehr schwierig, eine Datei zu ändern, ohne den Dateihash vom ursprünglichen nicht geänderten Wert zu ändern. Ein Dateihash kann daher verwendet werden, um absichtliche und sogar feine Änderungen an einer Datei zu erkennen, z. b. solche, die von Viren, Hacker oder Trojanerprogrammen eingeführt wurden.

Wenn Sie in einem Zertifikat enthalten ist, muss der Bild Digest bestimmte Felder im PE-Image ausschließen, wie z. b. die Prüfsummen-und Zertifikat Tabelleneinträge in optionalen Header Daten Verzeichnissen. Dies liegt daran, dass durch das Hinzufügen eines Zertifikats diese Felder geändert werden und ein anderer Hashwert berechnet wird.

Die Win32-Funktion **imagegetdigeststream** stellt einen Datenstrom aus einer Ziel-PE-Datei bereit, mit der Funktionen zu Hash Funktionen werden. Dieser Datenstrom bleibt konsistent, wenn Zertifikate zu einer PE-Datei hinzugefügt oder daraus entfernt werden. Basierend auf den Parametern, die an **imagegetdigeststream** übergeben werden, können andere Daten aus dem PE-Image aus der Hash Berechnung ausgelassen werden. Einen Link zur Referenzseite der Funktion finden Sie unter [Verweise](#references).

### <a name="delay-load-import-tables-image-only"></a>Delay-Load Importieren von Tabellen (nur Bild)

Diese Tabellen wurden dem Image hinzugefügt, um einen einheitlichen Mechanismus für Anwendungen zu unterstützen, mit dem das Laden einer DLL verzögert wird, bis der erste Aufrufe in diese DLL besteht. Das Layout der Tabellen stimmt mit dem der herkömmlichen Import Tabellen überein, die im Abschnitt 6,4, [dem. iData-Abschnitt](#the-idata-section)beschrieben werden. Hier werden nur einige Details erläutert.

#### <a name="the-delay-load-directory-table"></a>Die Delay-Load Directory-Tabelle

Die Verzeichnis Tabelle für verzögertes Laden ist das Gegenstück zur Import-Verzeichnis Tabelle. Sie kann über den Eintrag verzögerter Import Deskriptor in der Liste optionaler Header Datenverzeichnisse (Offset 200) abgerufen werden. Die Tabelle wird wie folgt angeordnet:



| Offset         | Size          | Feld                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                  |
|----------------|---------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Attribute <br/>                 | Muss Null sein. <br/>                                                                                                                                                                                                                                                                                                    |
| 4 <br/>  | 4 <br/> | Name <br/>                       | Die RVA des Namens der zu ladenden DLL. Der Name befindet sich im schreibgeschützten Daten Abschnitt des Bilds. <br/>                                                                                                                                                                                                        |
| 8 <br/>  | 4 <br/> | Modul handle <br/>              | Die RVA des Modul Handles (im Daten Abschnitt des Bilds) der dll, die verzögert geladen werden soll. Sie wird für die Speicherung durch die Routine verwendet, die zum Verwalten des verzögerten Ladens bereitgestellt wird. <br/>                                                                                                                                   |
| 12 <br/> | 4 <br/> | Verzögerten Import der Adress Tabelle <br/> | Die RVA der Import Adress Tabelle für verzögertes Laden. Weitere Informationen finden Sie unter [verzögertes Importieren der Adress Tabelle (IAT)](#delay-import-address-table). <br/>                                                                                                                                                                       |
| 16 <br/> | 4 <br/> | Import Name Tabelle verzögern <br/>    | Die RVA der Name-Tabelle mit verzögertem Ladevorgang, die die Namen der Importe enthält, die möglicherweise geladen werden müssen. Dies entspricht dem Layout der Import Name-Tabelle. Weitere Informationen finden Sie unter [Hint/Name Table](#hintname-table).<br/>                                                                                       |
| 20 <br/> | 4 <br/> | Import Tabelle für gebundene Verzögerung <br/>   | Die RVA der Adress Tabelle für das gebundene verzögerte Laden, sofern vorhanden. <br/>                                                                                                                                                                                                                                                     |
| 24 <br/> | 4 <br/> | Verzögerungs Import Tabelle entladen <br/>  | Die RVA der Adress Tabelle für den Entlade verzögerten Ladevorgang, falls vorhanden. Dies ist eine exakte Kopie der verzögerten Import Adress Tabelle. Wenn der Aufrufer die dll entlädt, sollte diese Tabelle wieder über die verzögerte Import Adress Tabelle kopiert werden, damit nachfolgende Aufrufe der DLL den Hash Mechanismus weiterhin ordnungsgemäß verwenden. <br/> |
| 28 <br/> | 4 <br/> | Zeitstempel <br/>                 | Der Zeitstempel der dll, an die dieses Bild gebunden wurde. <br/>                                                                                                                                                                                                                                                     |



 

Die Tabellen, auf die in dieser Datenstruktur verwiesen wird, werden so organisiert und sortiert, wie ihre Entsprechungen für herkömmliche Importe gelten. Weitere Informationen finden Sie [im Abschnitt. iData](#the-idata-section).

#### <a name="attributes"></a>Attribute

Es werden jedoch keine Attributflags definiert. Der Linker legt dieses Feld im Bild auf NULL fest. Dieses Feld kann verwendet werden, um den Datensatz zu erweitern, indem das vorhanden sein neuer Felder angegeben wird, oder es kann verwendet werden, um das Verhalten der Delay-oder Entlade Hilfsfunktionen anzugeben.

#### <a name="name"></a>Name

Der Name der dll, die verzögert geladen werden soll, befindet sich im schreibgeschützten Daten Abschnitt des Bilds. Der Verweis erfolgt über das Feld szName.

#### <a name="module-handle"></a>Modul handle

Das Handle der dll, das verzögert geladen werden soll, befindet sich im Daten Abschnitt des Bilds. Das phmod-Feld verweist auf das handle. Das bereitgestellte Hilfsprogramm für verzögertes Laden verwendet diesen Speicherort, um das Handle in der geladenen DLL zu speichern.

#### <a name="delay-import-address-table"></a>Verzögerten Import der Adress Tabelle

Auf die Verzögerungs Import-Adress Tabelle (IAT) wird durch den Verzögerungs Import Deskriptor über das Feld Piat verwiesen. Das Hilfsprogramm für verzögertes Laden aktualisiert diese Zeiger mit den tatsächlichen Einstiegspunkten, sodass die thunkte nicht mehr in der aufrufenden Schleife sind. Der Zugriff auf die Funktionszeiger erfolgt mithilfe des Ausdrucks `pINT->u1.Function` .

#### <a name="delay-import-name-table"></a>Import Name Tabelle verzögern

Die Name-Tabelle für verzögertes Importieren (int) enthält die Namen der Importe, die möglicherweise geladen werden müssen. Sie werden auf die gleiche Weise wie die Funktionszeiger in IAT angeordnet. Sie bestehen aus denselben Strukturen wie der Standard-int, und der Zugriff erfolgt über den-Ausdruck `pINT->u1.AddressOfData->Name[0]` .

#### <a name="delay-bound-import-address-table-and-time-stamp"></a>Verzögert gebundene Import Adress Tabelle und Zeitstempel

Die verzögert gebundene Import Adress Tabelle (BIAT) ist eine optionale Tabelle mit Image- \_ Thunk- \_ Datenelementen, die zusammen mit dem Zeitstempel-Feld der Verzeichnis Tabelle für verzögertes Laden durch eine nach Prozess Ende Bindungs Phase verwendet wird.

#### <a name="delay-unload-import-address-table"></a>Verzögertes Entladen der Import Adress Tabelle

Die verzögerte Entladungs Tabelle (UIAT) ist eine optionale Tabelle mit Image- \_ Thunk- \_ Datenelementen, die der Entlade Code verwendet, um eine explizite Entlade Anforderung zu verarbeiten. Er besteht aus initialisierten Daten im schreibgeschützten Abschnitt, bei dem es sich um eine exakte Kopie des ursprünglichen IAT handelt, das den Code auf die verzögerten Ladevorgänge verwiesen hat. Bei der Anforderung zum Entladen kann die Bibliothek freigegeben werden, der \* phmod wurde gelöscht, und der UIAT, der über die IAT-Umgebung geschrieben wurde, kann alle Elemente im Zustand "vorab laden" wiederherstellen.

## <a name="special-sections"></a>Besondere Abschnitte

- [Der. Debug-Abschnitt](#the-debug-section)
  - [Debugverzeichnis (nur Bild)](#debug-directory-image-only)
  - [Debugtyp](#debug-type)
  - [. Debug $ F (nur Objekt)](#debugf-object-only)
  - [. Debuggen von $ S (nur Objekt)](#debugs-object-only)
  - [. Debug $ P (nur Objekt)](#debugp-object-only)
  - [. Debug $ T (nur Objekt)](#debugt-object-only)
  - [Linker-Unterstützung für Microsoft-Debuginformationen](#linker-support-for-microsoft-debug-information)
- [Der Abschnitt ". drectve" (nur Objekt)](#the-drectve-section-object-only)
- [Der Abschnitt ". edata" (nur Bild)](#the-edata-section-image-only)
  - [Exportieren der Verzeichnis Tabelle](#export-directory-table)
  - [Adress Tabelle exportieren](#export-address-table)
  - [Namens Zeiger Tabelle exportieren](#export-name-pointer-table)
  - [Ordinaltabelle exportieren](#export-ordinal-table)
  - [Export Name Table](#export-name-table)
- [Der. iData-Abschnitt](#the-idata-section)
  - [Importieren der Verzeichnis Tabelle](#import-directory-table)
  - [Nachschlage Tabelle importieren](#import-lookup-table)
  - [Hint/Name-Tabelle](#hintname-table)
  - [Adress Tabelle importieren](#delay-import-address-table)
- [Der pdata-Abschnitt](#the-pdata-section)
- [Der. reloc-Abschnitt (nur Bild)](#the-reloc-section-image-only)
  - [Basis Verschiebungs Block](#base-relocation-block)
  - [Basis Verschiebungs Typen](#base-relocation-types)
- [Der. TLS-Abschnitt](#the-tls-section)
  - [Das TLS-Verzeichnis](#the-tls-directory)
  - [TLS-Rückruf Funktionen](#tls-callback-functions)
- [Struktur der Lade Konfiguration (nur Bild)](#the-load-configuration-structure-image-only)
  - [Konfigurationsverzeichnis laden](#load-configuration-directory)
  - [Konfigurations Layout laden](#load-configuration-layout)
- [Der Abschnitt ". rsrc"](#the-rsrc-section)
  - [Ressourcenverzeichnis Tabelle](#resource-directory-table)
  - [Ressourcenverzeichnis Einträge](#resource-directory-entries)
  - [Ressourcenverzeichnis Zeichenfolge](#resource-directory-string)
  - [Ressourcen Dateneintrag](#resource-data-entry)
- [Der. cormeta-Abschnitt (nur Objekt)](#the-cormeta-section-object-only)
- [Der sxdata-Abschnitt](#the-sxdata-section)

Typische COFF-Abschnitte enthalten Code oder Daten, die von linker und Microsoft Win32-Lade Programmen verarbeitet werden, ohne dass Sie besondere Kenntnisse über den Abschnitt Inhalt haben Der Inhalt ist nur für die Anwendung relevant, die verknüpft oder ausgeführt wird.

Einige COFF-Abschnitte haben jedoch eine besondere Bedeutung, wenn Sie in Objektdateien oder Bilddateien gefunden werden. Diese Abschnitte werden von Tools und lade Programmen erkannt, weil im Abschnitts Header besondere Flags festgelegt sind, da spezielle Positionen im optionalen Bild-Header auf Sie zeigen oder weil der Abschnitts Name selbst eine spezielle Funktion des Abschnitts angibt. (Selbst wenn der Abschnitts Name selbst keine besondere Funktion des Abschnitts angibt, wird der Abschnitts Name durch Konvention vorgegeben, sodass die Autoren dieser Spezifikation in allen Fällen auf einen Abschnittsnamen verweisen können.)

Die reservierten Abschnitte und deren Attribute werden in der folgenden Tabelle beschrieben, gefolgt von detaillierten Beschreibungen der Abschnitts Typen, die in ausführbaren Dateien persistent gespeichert werden, und der Abschnitts Typen, die Metadaten für Erweiterungen enthalten.



| Abschnitts Name          | Inhalt                                                                                                                                                                  | Merkmale                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BSS <br/>      | Nicht initialisierte Daten (freies Format) <br/>                                                                                                                             | Bild \_ SCN \_ CNT-Image für \_ nicht initialisierte \_ Daten \| \_ \_ \_ \| \_ \_ \_ <br/>                                                                                                                                                                                                                                                                                               |
| . cormeta <br/>  | CLR-Metadaten, die angeben, dass die Objektdatei verwalteten Code enthält <br/>                                                                                       | Bild- \_ SCN \_ lnk \_ Info <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| . Data <br/>     | Initialisierte Daten (freies Format) <br/>                                                                                                                               | Bild \_ SCN \_ CNT \_ initialisiertes \_ Daten \| Image \_ SCN Arbeitsspeicher \_ \_ Lese \| Image \_ SCN \_ \_ Arbeitsspeicher-Schreibvorgänge <br/>                                                                                                                                                                                                                                                                                                 |
| . Debuggen von $ F <br/>  | Fehler beim Generieren von Informationen zu "BPO" (nur Objekt, x86-Architektur und mittlerweile veraltet) <br/>                                                                       | Bild \_ SCN \_ CNT \_ initialisiertes \_ Daten \| Image \_ SCN Arbeitsspeicher \_ \_ \| Lesebild \_ SCN \_ \_ Arbeitsspeicher verwerfen <br/>                                                                                                                                                                                                                                                                                           |
| . Debuggen von $ P <br/>  | Vorkompilierte Debugtypen (nur Objekt) <br/>                                                                                                                        | Bild \_ SCN \_ CNT \_ initialisiertes \_ Daten \| Image \_ SCN Arbeitsspeicher \_ \_ \| Lesebild \_ SCN \_ \_ Arbeitsspeicher verwerfen <br/>                                                                                                                                                                                                                                                                                           |
| . Debuggen $ S <br/>  | Symbole Debuggen (nur Objekt) <br/>                                                                                                                                  | Bild \_ SCN \_ CNT \_ initialisiertes \_ Daten \| Image \_ SCN Arbeitsspeicher \_ \_ \| Lesebild \_ SCN \_ \_ Arbeitsspeicher verwerfen <br/>                                                                                                                                                                                                                                                                                           |
| . Debug $ T <br/>  | Debugtypen (nur Objekt) <br/>                                                                                                                                    | Bild \_ SCN \_ CNT \_ initialisiertes \_ Daten \| Image \_ SCN Arbeitsspeicher \_ \_ \| Lesebild \_ SCN \_ \_ Arbeitsspeicher verwerfen <br/>                                                                                                                                                                                                                                                                                           |
| . drective <br/> | Linkeroptionen <br/>                                                                                                                                               | Bild- \_ SCN \_ lnk \_ Info <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| . edata <br/>    | Exportieren von Tabellen <br/>                                                                                                                                                | Bild \_ SCN \_ CNT \_ initialisiertes \_ Daten \| Image \_ SCN \_ Arbeitsspeicher \_ Lesen <br/>                                                                                                                                                                                                                                                                                                                           |
| . iData <br/>    | Tabellen importieren <br/>                                                                                                                                                | Bild \_ SCN \_ CNT \_ initialisiertes \_ Daten \| Image \_ SCN Arbeitsspeicher \_ \_ Lese \| Image \_ SCN \_ \_ Arbeitsspeicher-Schreibvorgänge <br/>                                                                                                                                                                                                                                                                                                 |
| IDLSYM <br/>   | Schließt registrierte SEH ein (nur Bild), um IDL-Attribute zu unterstützen. Weitere Informationen finden Sie unter "IDL-Attribute" in den [verweisen](#references) am Ende dieses Themas. <br/> | Bild- \_ SCN \_ lnk \_ Info <br/>                                                                                                                                                                                                                                                                                                                                                                 |
| . pdata <br/>    | Ausnahmeinformationen <br/>                                                                                                                                        | Bild \_ SCN \_ CNT \_ initialisiertes \_ Daten \| Image \_ SCN \_ Arbeitsspeicher \_ Lesen <br/>                                                                                                                                                                                                                                                                                                                           |
| . rdata <br/>    | Schreibgeschützte initialisierte Daten <br/>                                                                                                                                   | Bild \_ SCN \_ CNT \_ initialisiertes \_ Daten \| Image \_ SCN \_ Arbeitsspeicher \_ Lesen <br/>                                                                                                                                                                                                                                                                                                                           |
| . reloc <br/>    | Bild Verschiebungen <br/>                                                                                                                                            | Bild \_ SCN \_ CNT \_ initialisiertes \_ Daten \| Image \_ SCN Arbeitsspeicher \_ \_ \| Lesebild \_ SCN \_ \_ Arbeitsspeicher verwerfen <br/>                                                                                                                                                                                                                                                                                           |
| . rsrc <br/>     | Ressourcenverzeichnis <br/>                                                                                                                                           | Bild \_ SCN \_ CNT \_ initialisiertes \_ Daten \| Image \_ SCN \_ Arbeitsspeicher \_ Lesen <br/>                                                                                                                                                                                                                                                                                                                           |
| SBSS <br/>     | GP-relative nicht initialisierte Daten (freies Format) <br/>                                                                                                                 | Bild \_ SCN \_ CNT \_ nicht initialisiertes \_ Daten \| Image \_ SCN Arbeitsspeicher- \_ \_ \| Lesebild SCN Arbeitsspeicher- \_ \_ \_ Schreib \| Image \_ SCN \_ gprel das Image \_ SCN- \_ gprel-Flag sollte nur für ia64-Architekturen festgelegt werden. dieses Flag ist für andere Architekturen ungültig. Das Abbild- \_ \_ gprel-Flag ist nur für Objektdateien vorgesehen. Wenn dieser Abschnitts Typ in einer Bilddatei angezeigt wird, darf das Image- \_ SCN- \_ gprel-Flag nicht festgelegt werden. <br/> |
| sdata <br/>    | GP-relative initialisierte Daten (freies Format) <br/>                                                                                                                   | Bild \_ SCN \_ CNT \_ initialisiertes \_ Daten \| Image \_ SCN Arbeitsspeicher- \_ \_ \| Lesebild SCN Arbeitsspeicher- \_ \_ \_ Schreib \| Image \_ SCN \_ gprel das Image \_ SCN- \_ gprel-Flag sollte nur für ia64-Architekturen festgelegt werden. dieses Flag ist für andere Architekturen ungültig. Das Abbild- \_ \_ gprel-Flag ist nur für Objektdateien vorgesehen. Wenn dieser Abschnitts Typ in einer Bilddatei angezeigt wird, darf das Image- \_ SCN- \_ gprel-Flag nicht festgelegt werden. <br/>   |
| srdata <br/>   | GP-relative schreibgeschützte Daten (freies Format) <br/>                                                                                                                     | Image \_ SCN \_ CNT \_ Initialized \_ Data \| Image \_ SCN \_ \_ standesleseimage \| \_ SCN \_ gprel das Image \_ SCN- \_ gprel-Flag sollte nur für ia64-Architekturen festgelegt werden. dieses Flag ist für andere Architekturen ungültig. Das Abbild- \_ \_ gprel-Flag ist nur für Objektdateien vorgesehen. Wenn dieser Abschnitts Typ in einer Bilddatei angezeigt wird, darf das Image- \_ SCN- \_ gprel-Flag nicht festgelegt werden. <br/>                             |
| sxdata <br/>   | Registrierte Ausnahmehandlerdaten (freies Format und x86/Objekt) <br/>                                                                                          | Image \_ SCN \_ lnk \_ Info enthält den Symbol Index jedes Ausnahmehandler, auf den der Code in dieser Objektdatei verweist. Das Symbol kann für ein undef-Symbol oder eines, das in diesem Modul definiert ist, sein. <br/>                                                                                                                                                                     |
| .text <br/>     | Ausführbarer Code (freies Format) <br/>                                                                                                                                | Bild \_ SCN \_ CNT \_ - \| Codebild \_ SCN Arbeitsspeicher \_ \_ Ausführen \| iImage \_ SCN \_ \_ Arbeitsspeicher lesen <br/>                                                                                                                                                                                                                                                                                                           |
| . TLS <br/>      | Lokaler Thread Speicher (nur Objekt) <br/>                                                                                                                           | Bild \_ SCN \_ CNT \_ initialisiertes \_ Daten \| Image \_ SCN Arbeitsspeicher \_ \_ Lese \| Image \_ SCN \_ \_ Arbeitsspeicher-Schreibvorgänge <br/>                                                                                                                                                                                                                                                                                                 |
| TLS $ <br/>     | Lokaler Thread Speicher (nur Objekt) <br/>                                                                                                                           | Bild \_ SCN \_ CNT \_ initialisiertes \_ Daten \| Image \_ SCN Arbeitsspeicher \_ \_ Lese \| Image \_ SCN \_ \_ Arbeitsspeicher-Schreibvorgänge <br/>                                                                                                                                                                                                                                                                                                 |
| vsdata <br/>   | GP-relative initialisierte Daten (freies Format und nur für Arm-, SH4-und Thumb-Architekturen) <br/>                                                                    | Bild \_ SCN \_ CNT \_ initialisiertes \_ Daten \| Image \_ SCN Arbeitsspeicher \_ \_ Lese \| Image \_ SCN \_ \_ Arbeitsspeicher-Schreibvorgänge <br/>                                                                                                                                                                                                                                                                                                 |
| . XData <br/>    | Ausnahme Informationen (freies Format) <br/>                                                                                                                          | Bild \_ SCN \_ CNT \_ initialisiertes \_ Daten \| Image \_ SCN \_ Arbeitsspeicher \_ Lesen <br/>                                                                                                                                                                                                                                                                                                                           |



 

Einige der hier aufgeführten Abschnitte sind als "nur Objekt" oder "nur Bild" gekennzeichnet, um anzugeben, dass ihre besondere Semantik nur für Objektdateien oder Bilddateien relevant ist. Ein Abschnitt, der als "nur Bild" gekennzeichnet ist, wird möglicherweise weiterhin in einer Objektdatei angezeigt, um in die Bilddatei zu gelangen, aber der Abschnitt hat keine besondere Bedeutung für den Linker, sondern nur für das Bild Datei Lade Programm.

### <a name="the-debug-section"></a>Der. Debug-Abschnitt

Der. Debug-Abschnitt wird in Objektdateien verwendet, um vom Compiler generierte Debuginformationen zu enthalten, und in Bilddateien, die alle generierten Debuginformationen enthalten. In diesem Abschnitt wird das Verpacken von Debuginformationen in Objekt-und Bilddateien beschrieben.

Im nächsten Abschnitt wird das Format des debugverzeichnisses beschrieben, das sich an einer beliebigen Stelle im Image befinden kann. In den nachfolgenden Abschnitten werden die "Gruppen" in Objektdateien beschrieben, die Debuginformationen enthalten.

Der Standardwert für den Linker ist, dass Debuginformationen nicht im Adressraum des Bilds zugeordnet werden. Ein. Debug-Abschnitt ist nur vorhanden, wenn Debuginformationen im Adressraum zugeordnet sind.

#### <a name="debug-directory-image-only"></a>Debugverzeichnis (nur Bild)

Bilddateien enthalten ein optionales Debugverzeichnis, das angibt, welche Art von Debuginformationen vorhanden ist und wo Sie sich befindet. Dieses Verzeichnis besteht aus einem Array von Debug-Verzeichnis Einträgen, deren Speicherort und Größe im optionalen Bild Header angezeigt werden.

Das Debugverzeichnis kann sich in einem verwerfbaren. Debug-Abschnitt (sofern vorhanden) befinden, oder er kann in einem beliebigen anderen Abschnitt in der Bilddatei enthalten sein oder darf sich nicht in einem Abschnitt befinden.

Jeder Debugverzeichniseintrag identifiziert den Speicherort und die Größe eines Blocks von Debuginformationen. Die angegebene RVA kann 0 (null) sein, wenn die Debuginformationen nicht von einem Abschnitts Header abgedeckt werden (d. h., Sie befindet sich in der Bilddatei und ist nicht im Lauf Zeit Adressraum zugeordnet). Wenn Sie zugeordnet ist, ist die RVA die Adresse.

Ein Debugverzeichniseintrag weist das folgende Format auf:



| Offset         | Size          | Feld                        | BESCHREIBUNG                                                                                                                                            |
|----------------|---------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Merkmale <br/>  | Reserviert, muss NULL sein. <br/>                                                                                                                    |
| 4 <br/>  | 4 <br/> | TimeDateStamp <br/>    | Das Datum und die Uhrzeit, zu der die Debugdaten erstellt wurden. <br/>                                                                                         |
| 8 <br/>  | 2 <br/> | MajorVersion <br/>     | Die Hauptversionsnummer des debugdatenformats. <br/>                                                                                         |
| 10 <br/> | 2 <br/> | MinorVersion <br/>     | Die neben Versionsnummer des debugdatenformats. <br/>                                                                                         |
| 12 <br/> | 4 <br/> | type <br/>             | Das Format der Debuginformationen. Dieses Feld ermöglicht die Unterstützung mehrerer debuggger. Weitere Informationen finden Sie unter [Debug Type](#debug-type).<br/> |
| 16 <br/> | 4 <br/> | Sizeofdata <br/>       | Die Größe der Debugdaten (ohne das Debugverzeichnis selbst). <br/>                                                                     |
| 20 <br/> | 4 <br/> | Addressofrawdata <br/> | Die Adresse der Debugdaten, wenn Sie in Relation zur Bildbasis geladen werden. <br/>                                                                     |
| 24 <br/> | 4 <br/> | Pointertor awdata <br/> | Der Dateizeiger auf die Debugdaten. <br/>                                                                                                        |



 

#### <a name="debug-type"></a>Debugtyp

Die folgenden Werte sind für das type-Feld des debugverzeichniseintrags definiert:



| Konstante                                        | Wert          | BESCHREIBUNG                                                                                                                                                                                                      |
|-------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ bilddebugtyp \_ unbekannt <br/>         | 0 <br/>  | Ein unbekannter Wert, der von allen Tools ignoriert wird. <br/>                                                                                                                                                       |
| Image \_ Debug \_ Type \_ COFF <br/>            | 1 <br/>  | Die COFF-Debuginformationen (Zeilennummern, Symboltabelle und Zeichenfolgentabelle). Auf diese Art von Debuginformationen wird auch von Feldern in Dateiheadern verwiesen. <br/>                                          |
| Bild \_ \_ Debugtyp \_ CodeView <br/>        | 2 <br/>  | Die Visual C++ Debuginformationen. <br/>                                                                                                                                                                    |
| Bild \_ Debugtyp-Fehlermeldung \_ \_ <br/>             | 3 <br/>  | Die Informationen zum Frame Zeiger ausgelassen (FPO). Diese Informationen informieren den Debugger darüber, wie nicht dem Standard entsprechende Stapel Rahmen interpretiert werden, die das EBP-Register für einen anderen Zweck als einen Frame Zeiger verwenden. <br/> |
| Bild \_ \_ Debugtyp \_ misc <br/>            | 4 <br/>  | Der Speicherort der dbg-Datei. <br/>                                                                                                                                                                            |
| Image- \_ Debug- \_ \_ typausnahme <br/>       | 5 <br/>  | Eine Kopie des pData-Abschnitts. <br/>                                                                                                                                                                            |
| Image \_ Debug \_ Type \_ Fixup <br/>           | 6 <br/>  | Reserviert. <br/>                                                                                                                                                                                            |
| Bild \_ Debuggen \_ Type \_ oMap \_ to \_ src <br/>   | 7 <br/>  | Die Zuordnung von einem RVA in Image zu einer RVA im Quell Image. <br/>                                                                                                                                          |
| Image \_ Debug \_ Type \_ oMap \_ from \_ src <br/> | 8 <br/>  | Die Zuordnung von einer RVA im Quell Image zu einer RVA in Image. <br/>                                                                                                                                          |
| Bild \_ \_ Debugtyp \_ Borland <br/>         | 9 <br/>  | Reserviert für Borland. <br/>                                                                                                                                                                                |
| Image \_ Debug \_ Type \_ RESERVED10 <br/>      | 10 <br/> | Reserviert. <br/>                                                                                                                                                                                            |
| Image \_ Debug \_ Type \_ CLSID <br/>           | 11 <br/> | Reserviert. <br/>                                                                                                                                                                                            |
| Image \_ Debug \_ Type \_ Repro <br/>           | 16 <br/> | PE-Determinismus oder Reproduzierbarkeit. <br/>                                                                                                                                                                   |
| Image \_ - \_ Debugtyp \_ Ex \_ DllCharacteristics | 20 | Erweiterte dll-Merkmale Bits. |



 

Wenn das type-Feld auf Image \_ Debug \_ Type FPO festgelegt ist \_ , ist das Debuggen von Rohdaten ein Array, in dem jedes Element den Stapel Rahmen einer Funktion beschreibt. Für nicht jede Funktion in der Bilddatei müssen die für die Datei festgelegten Informationen definiert sein, auch wenn der Debugtyp "f" ist. Bei den Funktionen, die keine FPO-Informationen aufweisen, wird angenommen, dass Sie über normale Stapel Rahmen verfügen. Das Format für die Informationen zu den folgenden Informationen lautet wie folgt:


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



Das vorhanden sein eines Eintrags vom Typ Image \_ Debug \_ Type \_ Repro gibt an, dass die PE-Datei auf eine Weise erstellt wurde, um Determinismus oder Reproduzierbarkeit zu erreichen. Wenn die Eingabe nicht geändert wird, ist die Ausgabe-PE-Datei für die Ausgabe der PE-Datei sicher, unabhängig davon, wann oder wo die PE erstellt wird. Verschiedene Datums-/Zeitstempelfelder in der PE-Datei werden mit einem Teil oder allen Bits aus einem berechneten Hashwert gefüllt, der PE-Dateiinhalte als Eingabe verwendet. Sie stellen daher nicht mehr das tatsächliche Datum und die Uhrzeit dar, zu denen eine PE-Datei oder zugehörige spezifische Daten innerhalb der PE erstellt werden. Die Rohdaten dieses debugtrags können leer sein oder einen berechneten Hashwert enthalten, dem ein 4-Byte-Wert vorangestellt ist, der die Länge des Hashwerts darstellt.

Wenn das type-Feld auf Image \_ Debug \_ Type \_ Ex DllCharacteristics festgelegt ist \_ , enthalten die debugrohdaten erweiterte dll-Merkmale, zusätzlich zu denen, die in der optionalen Kopfzeile von Image festgelegt werden könnten. Weitere Informationen finden Sie unter [dll-Eigenschaften](#dll-characteristics) im Abschnitt [optionale Header Windows-Specific Felder (nur Bild)](#optional-header-windows-specific-fields-image-only).

##### <a name="extended-dll-characteristics"></a>Erweiterte DLL-Eigenschaften

Die folgenden Werte sind für die erweiterten dll-Merkmale definiert.

| Konstante | Wert | BESCHREIBUNG |
|-|-|-|
| Image- \_ dllcharakteriken nach dem Betriebs- \_ \_ \_ kompatibler | 0x0001 | Das Image ist mit dem Wert "CET |

#### <a name="debugf-object-only"></a>. Debug $ F (nur Objekt)

Die Daten in diesem Abschnitt wurden in Visual C++ Version 7,0 und höher durch einen umfassenderen Satz von Daten ersetzt, die in einen **. Debug $ S** -unter Abschnitt ausgegeben werden.

Objektdateien können. Debug $ F-Abschnitte enthalten, deren Inhalt mindestens ein FPO-Daten Satz ist \_ (Informationen zum Weglassen von Frame Zeigern). Weitere Informationen finden Sie unter "Image \_ Debug \_ Type-Steuer Objekt \_ " unter [Debugtyp](#debug-type).

Der Linker erkennt diese **. Debug $ F** -Datensätze. Wenn Debuginformationen generiert werden, sortiert der Linker die \_ Datensätze für die Datensätze nach der Prozedur RVA und generiert einen Debugverzeichniseintrag.

Der Compiler sollte keine FPO-Datensätze für Prozeduren mit einem Standard Frame Format generieren.

#### <a name="debugs-object-only"></a>. Debuggen von $ S (nur Objekt)

Dieser Abschnitt enthält Visual C++ Debuginformationen (symbolische Informationen).

#### <a name="debugp-object-only"></a>. Debug $ P (nur Objekt)

Dieser Abschnitt enthält Visual C++ Debuginformationen (vorkompilierte Informationen). Dabei handelt es sich um freigegebene Typen für alle-Objekte, die mithilfe des vorkompilierten Headers kompiliert wurden, der mit diesem-Objekt generiert wurde.

#### <a name="debugt-object-only"></a>. Debug $ T (nur Objekt)

Dieser Abschnitt enthält Visual C++ Debuginformationen (Typinformationen).

#### <a name="linker-support-for-microsoft-debug-information"></a>Linker-Unterstützung für Microsoft-Debuginformationen

Um Debuginformationen zu unterstützen, wird der Linker:

-   Sammelt alle relevanten Debugdaten aus den Abschnitten " **. Debug $ F**", " **Debug $ S**", " **. Debug $ P**" und " **. Debug $ T** ".

-   Verarbeitet diese Daten zusammen mit den vom Linker generierten Debuginformationen in die PDB-Datei und erstellt einen Debugverzeichniseintrag, um darauf zu verweisen.

### <a name="the-drectve-section-object-only"></a>Der Abschnitt ". drectve" (nur Objekt)

Bei einem Abschnitt handelt es sich um einen direktivenabschnitt, wenn er das Image \_ SCN \_ lnk \_ Info-Flag im Abschnitts Header festgelegt hat und den **. drectve** -Abschnittsnamen aufweist. Der Linker entfernt einen **. drectve** -Abschnitt nach der Verarbeitung der Informationen, sodass der Abschnitt nicht in der Bilddatei angezeigt wird, die verknüpft wird.

Ein **. drectve** -Abschnitt besteht aus einer Text Zeichenfolge, die als ANSI oder UTF-8 codiert werden kann. Wenn die UTF-8-Byte Reihenfolge-Markierung (BOM, ein 3-Byte-Präfix, das aus 0xEF, 0xBB und 0xBF besteht) nicht vorhanden ist, wird die direktivenzeichenfolge als ANSI interpretiert. Die direktivenzeichenfolge ist eine Reihe von Linkeroptionen, die durch Leerzeichen getrennt sind. Jede Option enthält einen Bindestrich, den Optionsnamen und ein entsprechendes Attribut. Wenn eine Option Leerzeichen enthält, muss die Option in Anführungszeichen eingeschlossen werden. Der Abschnitt " **. drectve** " darf keine Umsetzungen oder Zeilennummern enthalten.

### <a name="the-edata-section-image-only"></a>Der Abschnitt ". edata" (nur Bild)

Der Abschnitt "Daten exportieren" mit dem Namen ". edata" enthält Informationen über Symbole, auf die andere Bilder durch dynamisches Verknüpfen zugreifen können. Exportierte Symbole werden im Allgemeinen in DLLs gefunden, DLLs können jedoch auch Symbole importieren.

Eine Übersicht über die allgemeine Struktur des Abschnitts exportieren wird unten beschrieben. Die beschriebenen Tabellen sind normalerweise in der angegebenen Reihenfolge in der Datei zusammenhängend (obwohl dies nicht erforderlich ist). Zum Exportieren von Symbolen als ordinale sind nur die Export Verzeichnis Tabelle und die Export Adress Tabelle erforderlich. (Eine Ordinalzahl ist ein Export, auf den direkt über den Export Adresstabellen-Index zugegriffen wird.) Die Name-Zeiger Tabelle, ordinaltabelle und Export namens Tabelle sind vorhanden, um die Verwendung von Export Namen zu unterstützen.



| Tabellenname                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exportieren der Verzeichnis Tabelle <br/> | Eine Tabelle mit nur einer Zeile (im Gegensatz zum Debugverzeichnis). Diese Tabelle zeigt die Speicherorte und Größen der anderen Export Tabellen an. <br/>                                                                                                                                                                                                               |
| Adress Tabelle exportieren <br/>   | Ein Array von RVAs exportierter Symbole. Dies sind die tatsächlichen Adressen der exportierten Funktionen und Daten innerhalb des Abschnitts "ausführbarer Code" und "Daten". Andere Bilddateien können ein Symbol mit einem Index für diese Tabelle (Ordnungszahl) oder optional mithilfe des öffentlichen namens importieren, der der Ordinalzahl entspricht, wenn ein öffentlicher Name definiert ist. <br/> |
| Namens Zeiger Tabelle <br/>     | Ein Array von Zeigern auf die öffentlichen Export Namen, sortiert in aufsteigender Reihenfolge. <br/>                                                                                                                                                                                                                                                                    |
| Ordinaltabelle <br/>          | Ein Array von ordinalen, die Membern der Name-Zeiger Tabelle entsprechen. Die Entsprechung ist nach Position. Daher müssen die Name-Zeiger Tabelle und die ordinaltabelle dieselbe Anzahl von Elementen aufweisen. Jede Ordinalzahl ist ein Index in der Export Adress Tabelle. <br/>                                                                        |
| Export Name Table <br/>      | Eine Reihe von null-terminierten ASCII-Zeichen folgen. Member des Name-Zeiger Tabellen Punkts in diesen Bereich. Diese Namen sind die öffentlichen Namen, über die die Symbole importiert und exportiert werden. Sie sind nicht notwendigerweise mit den privaten Namen identisch, die in der Bilddatei verwendet werden. <br/>                                                           |



 

Wenn eine andere Bilddatei ein Symbol nach Name importiert, durchsucht das Win32-Lade Modul die Name-Zeiger Tabelle nach einer übereinstimmenden Zeichenfolge. Wenn eine übereinstimmende Zeichenfolge gefunden wird, wird die zugehörige Ordinalzahl identifiziert, indem der entsprechende Member in der ordinaltabelle gesucht wird (d. h. der Member der ordinaltabelle mit demselben Index wie der Zeichen folgen Zeiger in der Name-Zeiger Tabelle). Die resultierende Ordinalzahl ist ein Index in der Export Adress Tabelle, der den tatsächlichen Speicherort des gewünschten Symbols liefert. Auf jedes Export Symbol kann mit einer Ordinalzahl zugegriffen werden.

Wenn eine andere Bilddatei ein Symbol nach Ordinalzahl importiert, ist es nicht erforderlich, die Name-Zeiger Tabelle nach einer übereinstimmenden Zeichenfolge zu durchsuchen. Eine direkte Verwendung einer Ordinalzahl ist daher effizienter. Ein Export Name ist jedoch leichter zu merken und erfordert nicht, dass der Benutzer den Tabellenindex für das Symbol kennt.

#### <a name="export-directory-table"></a>Exportieren der Verzeichnis Tabelle

Die Export Symbol Informationen beginnen mit der Export Verzeichnis Tabelle, in der der Rest der Export Symbol Informationen beschrieben wird. Die Export Verzeichnis Tabelle enthält Adressinformationen, mit denen Importe in die Einstiegspunkte in diesem Bild aufgelöst werden.



| Offset         | Size          | Feld                                | BESCHREIBUNG                                                                                                                                                               |
|----------------|---------------|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Exportflags <br/>             | Reserviert, muss 0 sein. <br/>                                                                                                                                          |
| 4 <br/>  | 4 <br/> | Datums-/Uhrzeitstempel <br/>          | Das Datum und die Uhrzeit, zu der die Exportdaten erstellt wurden. <br/>                                                                                                           |
| 8 <br/>  | 2 <br/> | Hauptversion <br/>            | Die Hauptversionsnummer. Die Haupt-und neben Versionsnummern können vom Benutzer festgelegt werden. <br/>                                                                         |
| 10 <br/> | 2 <br/> | Nebenversion <br/>            | Die Nebenversionsnummer. <br/>                                                                                                                                     |
| 12 <br/> | 4 <br/> | Name der RVA <br/>                 | Die Adresse der ASCII-Zeichenfolge, die den Namen der dll enthält. Diese Adresse ist relativ zur Bildbasis. <br/>                                                |
| 16 <br/> | 4 <br/> | Ordinalbasis <br/>             | Die Anfangs Ordinalzahl für Exporte in diesem Bild. Dieses Feld gibt die Anfangs Ordinalzahl für die Export Adress Tabelle an. Sie wird in der Regel auf 1 festgelegt. <br/> |
| 20 <br/> | 4 <br/> | Adresstabellen Einträge <br/>    | Die Anzahl der Einträge in der Export Adress Tabelle. <br/>                                                                                                            |
| 24 <br/> | 4 <br/> | Anzahl von namens Zeigern <br/>  | Die Anzahl der Einträge in der Name-Zeiger Tabelle. Dies ist auch die Anzahl der Einträge in der ordinaltabelle. <br/>                                                     |
| 28 <br/> | 4 <br/> | Exportieren der Adress Tabelle RVA <br/> | Die Adresse der Export Adress Tabelle, relativ zur Bildbasis. <br/>                                                                                          |
| 32 <br/> | 4 <br/> | Namens Zeiger-RVA <br/>         | Die Adresse der Export Name-Zeiger Tabelle, relativ zur Bildbasis. Die Tabellengröße wird durch das Feld Anzahl der namens Zeiger angegeben. <br/>                       |
| 36 <br/> | 4 <br/> | Ordnungszahl Tabelle RVA <br/>        | Die Adresse der ordinaltabelle, relativ zur Bildbasis. <br/>                                                                                                 |



 

#### <a name="export-address-table"></a>Adress Tabelle exportieren

Die Export Adress Tabelle enthält die Adresse der exportierten Einstiegspunkte und der exportierten Daten und die absolute. Eine Ordinalzahl wird als Index in der Export Adress Tabelle verwendet.

Jeder Eintrag in der Export Adress Tabelle ist ein Feld, das in der folgenden Tabelle eines der beiden Formate verwendet. Wenn sich die angegebene Adresse nicht innerhalb des Export Abschnitts befindet (wie durch die Adresse und die Länge definiert, die im optionalen Header angegeben sind), ist das Feld eine Export-RVA, bei der es sich um eine tatsächliche Adresse im Code oder in den Daten handelt. Andernfalls ist das Feld eine Weiterleitungs-RVA, die ein Symbol in einer anderen dll benennt.



| Offset        | Size          | Feld                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|---------------|---------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Exportieren von RVA <br/>    | Die Adresse des exportierten Symbols, wenn es in den Arbeitsspeicher geladen wird, relativ zur Bildbasis. Beispielsweise die Adresse einer exportierten Funktion. <br/>                                                                                                                                                                                                                                                                                                       |
| 0 <br/> | 4 <br/> | Weiterleitungs-RVA <br/> | Der Zeiger auf eine NULL-terminierte ASCII-Zeichenfolge im Export Abschnitt. Diese Zeichenfolge muss innerhalb des Bereichs liegen, der im Export Table Data Directory-Eintrag angegeben wird. Siehe [optionale Header Datenverzeichnisse (nur Bild)](#optional-header-data-directories-image-only). Diese Zeichenfolge gibt den DLL-Namen und den Namen des Exports (z. b. "mydll. expfunc") oder den DLL-Namen und die Ordinalzahl des Exports an (z. b. "mydll. \# 27 "). <br/> |



 

Eine Weiterleitungs-RVA exportiert eine Definition aus einem anderen Bild, sodass Sie so angezeigt wird, als ob Sie vom aktuellen Image exportiert würde. Folglich wird das Symbol gleichzeitig importiert und exportiert.

Beispielsweise wird in Kernel32.dll unter Windows XP der Export mit dem Namen "heapzuordc" an die Zeichenfolge "Ntdll" weitergeleitet. Rtldepcateheap. " Dies ermöglicht es Anwendungen, das Windows XP-spezifische Modul Ntdll.dll zu verwenden, ohne dass Sie tatsächlich Import Verweise darauf enthalten. Die Import Tabelle der Anwendung bezieht sich nur auf Kernel32.dll. Daher ist die Anwendung nicht spezifisch für Windows XP und kann auf einem beliebigen Win32-System ausgeführt werden.

#### <a name="export-name-pointer-table"></a>Namens Zeiger Tabelle exportieren

Die Export Name-Zeiger Tabelle ist ein Array von Adressen (RVAs) in die Export Name-Tabelle. Die Zeiger sind jeweils 32 Bits und sind relativ zur Bildbasis. Die Zeiger werden lexikalisch angeordnet, um binäre suchen zuzulassen.

Ein Export Name wird nur definiert, wenn die Export Name-Zeiger Tabelle einen Zeiger darauf enthält.

#### <a name="export-ordinal-table"></a>Ordinaltabelle exportieren

Die Export ordinaltabelle ist ein Array von unausgewogenen 16-Bit-Indizes in die Export Adress Tabelle. Ordinale werden durch das ordinalbasisfeld der Export Verzeichnis Tabelle verzerrt. Anders ausgedrückt: die ordinalbasis muss von den Ordinalzahlen subtrahiert werden, um echte Indizes in die Export Adress Tabelle zu erhalten.

Die Export Name-Zeiger Tabelle und die Export ordinaltabelle bilden zwei parallele Arrays, die getrennt sind, um die Ausrichtung natürlicher Felder zuzulassen. Diese beiden Tabellen funktionieren in der Tat als eine Tabelle, in der die Export Name-Zeiger Spalte auf einen öffentlichen (exportierten) Namen zeigt, und die Export ordinalspalte gibt die entsprechende Ordinalzahl für diesen öffentlichen Namen an. Ein Member der Export Name-Zeiger Tabelle und ein Mitglied der Export ordinaltabelle werden mit der gleichen Position (Index) in den jeweiligen Arrays verknüpft.

Wenn also die Export Name-Zeiger Tabelle durchsucht wird und an Position i eine übereinstimmende Zeichenfolge gefunden wird, lautet der Algorithmus zum Suchen der RVA des Symbols und der unausgewogenen Ordinalzahl wie folgt:

```C++
i = Search_ExportNamePointerTable (name);
ordinal = ExportOrdinalTable [i];

rva = ExportAddressTable [ordinal];
biased_ordinal = ordinal + OrdinalBase;
```

Bei der Suche nach einem Symbol anhand der Ordinalzahl (ungebunden) lautet der Algorithmus zum Suchen der RVA und des Namens des Symbols wie folgt:

```C++
ordinal = biased_ordinal - OrdinalBase;
i = Search_ExportOrdinalTable (ordinal);

rva = ExportAddressTable [ordinal];
name = ExportNameTable [i];
```

#### <a name="export-name-table"></a>Export Name Table

Die Export Name-Tabelle enthält die tatsächlichen Zeichen folgen Daten, auf die von der Export Name-Zeiger Tabelle verwiesen wurde. Die Zeichen folgen in dieser Tabelle sind öffentliche Namen, die andere Bilder zum Importieren der Symbole verwenden können. Diese öffentlichen Export Namen sind nicht notwendigerweise identisch mit den privaten Symbolnamen, die die Symbole in ihrer eigenen Bilddatei und im eigenen Quellcode aufweisen, obwohl Sie sein können.

Jedes exportierte Symbol weist einen Ordinalwert auf, der lediglich der Index in der Export Adress Tabelle ist. Die Verwendung von Export Namen ist jedoch optional. Einige, alle oder keines der exportierten Symbole können Export Namen aufweisen. Für exportierte Symbole, die über Export Namen verfügen, werden die entsprechenden Einträge in der Export Name-Zeiger Tabelle und der Export ordinaltabelle zusammengeführt, um die einzelnen Namen einer Ordinalzahl zuzuordnen.

Die Struktur der Export Name-Tabelle ist eine Reihe von null-terminierten ASCII-Zeichen folgen mit variabler Länge.

### <a name="the-idata-section"></a>Der. iData-Abschnitt

Alle Bilddateien, die Symbole importieren, einschließlich praktisch aller ausführbaren Dateien (exe), verfügen über einen iData-Abschnitt. Ein typisches Datei Layout für die Import Informationen lautet folgendermaßen:

-   Verzeichnis Tabelle

    Verzeichniseintrag NULL

-   DLL1-Such Tabelle importieren

    Null

-   DLL2-Such Tabelle importieren

    Null

-   DLL3-Such Tabelle importieren

    Null

-   Hint-Name Tabelle

#### <a name="import-directory-table"></a>Importieren der Verzeichnis Tabelle

Die Import Informationen beginnen mit der Import-Verzeichnis Tabelle, in der die restlichen Import Informationen beschrieben werden. Die Import-Verzeichnis Tabelle enthält Adressinformationen, mit denen fixupverweise auf die Einstiegspunkte innerhalb eines dll-Images aufgelöst werden. Die Import-Verzeichnis Tabelle besteht aus einem Array von Import Verzeichnis Einträgen, einem Eintrag für jede DLL, auf die das Image verweist. Der letzte Verzeichniseintrag ist leer (mit NULL-Werten gefüllt), womit das Ende der Verzeichnis Tabelle angegeben wird.

Jeder Import Verzeichniseintrag weist das folgende Format auf:



| Offset         | Size          | Feld                                                 | BESCHREIBUNG                                                                                                                                                                                 |
|----------------|---------------|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Importieren der Nachschlage Tabelle RVA (Merkmale) <br/> | Die RVA der Import Such Tabelle. Diese Tabelle enthält einen Namen oder eine Ordinalzahl für jeden Import. (Der Name "Characteristics" wird in Winnt. h verwendet, beschreibt dieses Feld jedoch nicht mehr.) <br/> |
| 4 <br/>  | 4 <br/> | Datums-/Uhrzeitstempel <br/>                           | Der Stempel, der auf 0 (null) festgelegt wird, bis das Bild gebunden ist. Nachdem das Bild gebunden wurde, wird dieses Feld auf den Zeit-/datenstempel der DLL festgelegt. <br/>                                          |
| 8 <br/>  | 4 <br/> | Weiterleitungs Kette <br/>                           | Der Index des ersten Weiterleitungs Verweises. <br/>                                                                                                                                     |
| 12 <br/> | 4 <br/> | Name der RVA <br/>                                  | Die Adresse einer ASCII-Zeichenfolge, die den Namen der dll enthält. Diese Adresse ist relativ zur Bildbasis. <br/>                                                                   |
| 16 <br/> | 4 <br/> | RVA der Import Adress Tabelle (Thunk Table) <br/>    | Die RVA der Import Adress Tabelle. Der Inhalt dieser Tabelle ist mit dem Inhalt der Import Such Tabelle identisch, bis das Bild gebunden ist. <br/>                              |



 

#### <a name="import-lookup-table"></a>Nachschlage Tabelle importieren

Eine Import Such Tabelle ist ein Array von 32-Bit-Zahlen für das Format PE32 oder ein Array von 64-Bit-Zahlen für das Format PE32 +. Jeder Eintrag verwendet das Bitfeld Format, das in der folgenden Tabelle beschrieben wird. In diesem Format ist Bit 31 Das signifikanteste Bit für das Format PE32, und Bit 63 ist das signifikanteste Bit für das Format PE32 +. Die Auflistung dieser Einträge beschreibt alle Importe aus einer bestimmten dll. Der letzte Eintrag ist auf NULL (null) festgelegt, um das Ende der Tabelle anzugeben.



| Bit (e)            | Size           | Bitfeld                       | BESCHREIBUNG                                                                                                                                                               |
|-------------------|----------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 31/63 <br/> | 1 <br/>  | Ordinal-/namens-Flag <br/>   | Wenn dieses Bit festgelegt ist, importieren Sie nach Ordinalzahl. Andernfalls importieren Sie nach Namen. Bit wird als 0x80000000 für das Format PE32, 0x8000000000000000 für das Format PE32 + maskiert. <br/>                         |
| 15-0 <br/>  | 16 <br/> | Ordinalzahl <br/>      | Eine 16-Bit-Ordinalzahl. Dieses Feld wird nur verwendet, wenn das Bitfeld Ordinal/Name Flag den Wert 1 hat (Import by Ordinal). Bits 30-15 oder 62-15 muss 0 sein. <br/>                  |
| 30-0 <br/>  | 31 <br/> | Hinweis-/namenstabellen-RVA <br/> | Eine 31-Bit-RVA eines Hint-/namenstabelleneintrags. Dieses Feld wird nur verwendet, wenn das Bitfeld Ordinal/Name Flag 0 (nach Name importieren) ist. Für das Format PE32 + Bits 62-31 muss NULL sein. <br/> |



 

#### <a name="hintname-table"></a>Hint/Name-Tabelle

Eine Hint-/namens-Tabelle ist für den gesamten Import Abschnitt ausreichend. Jeder Eintrag in der Hint/Name-Tabelle weist das folgende Format auf:



| Offset         | Size                 | Feld            | BESCHREIBUNG                                                                                                                                                                                       |
|----------------|----------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/>        | Deuteten <br/> | Ein Index in die Export Name-Zeiger Tabelle. Eine Entsprechung wird zuerst mit diesem Wert versucht. Wenn dies nicht möglich ist, wird eine binäre Suche in der Export Name-Zeiger Tabelle der DLL ausgeführt. <br/>            |
| 2 <br/>  | -Variable <br/> | Name <br/> | Eine ASCII-Zeichenfolge, die den zu importierenden Namen enthält. Dies ist die Zeichenfolge, die mit dem öffentlichen Namen in der dll abgeglichen werden muss. Bei dieser Zeichenfolge wird die Groß-/Kleinschreibung beachtet und durch ein NULL Byte beendet <br/> |
| \* <br/> | 0 oder 1 <br/>   | Pad <br/>  | Ein nachfolgendes NULL-Pad-Byte, das nach dem nachfolgenden NULL-Byte angezeigt wird, um den nächsten Eintrag an einer geraden Grenze auszurichten. <br/>                                                        |



 

#### <a name="import-address-table"></a>Adress Tabelle importieren

Die Struktur und der Inhalt der Import Adress Tabelle sind identisch mit denen der Import Such Tabelle, bis die Datei gebunden ist. Während der Bindung werden die Einträge in der Import Adress Tabelle mit den 32-Bit-(für das Format PE32) oder 64-Bit-Adressen (für das Format PE32 +) der zu importierenden Symbole überschrieben. Diese Adressen sind die tatsächlichen Speicheradressen der Symbole, obwohl Sie technisch gesehen immer noch als "virtuelle Adressen" bezeichnet werden. Das Lade Modul verarbeitet die Bindung in der Regel.

### <a name="the-pdata-section"></a>Der pdata-Abschnitt

Der. pdata-Abschnitt enthält ein Array von Funktionstabellen Einträgen, die für die Ausnahmebehandlung verwendet werden. Dies wird durch den Ausnahme Tabelleneintrag im Image Datenverzeichnis gezeigt. Die Einträge müssen nach den Funktions Adressen (dem ersten Feld in jeder Struktur) sortiert werden, bevor Sie in das endgültige Bild ausgegeben werden. Die Zielplattform bestimmt, welche der drei unterschiedlichen Funktionstabellen-Eingabeformat Varianten, die unten beschrieben werden, verwendet wird.

Bei 32-Bit-MIPS-Images haben Funktionstabellen Einträge das folgende Format:



| Offset         | Size          | Feld                          | BESCHREIBUNG                                                                    |
|----------------|---------------|--------------------------------|--------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | BEGIN Address <br/>      | Der VA der entsprechenden Funktion. <br/>                              |
| 4 <br/>  | 4 <br/> | Endadresse <br/>        | Der VA-am Ende der Funktion. <br/>                                 |
| 8 <br/>  | 4 <br/> | Ausnahme Handler <br/>  | Der Zeiger auf den Ausnahmehandler, der ausgeführt werden soll. <br/>               |
| 12 <br/> | 4 <br/> | Handlerdaten <br/>       | Der Zeiger auf zusätzliche Informationen, die an den Handler weitergeleitet werden sollen. <br/> |
| 16 <br/> | 4 <br/> | Prologend Address <br/> | Der VA am Ende des Prolog der Funktion. <br/>                        |



 

Bei den Windows CE-Plattformen Arm, powerpc, SH3 und SH4 haben Funktionstabellen Einträge das folgende Format:



| Offset        | Size                | Feld                       | BESCHREIBUNG                                                                                                               |
|---------------|---------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/>       | BEGIN Address <br/>   | Der VA der entsprechenden Funktion. <br/>                                                                         |
| 4 <br/> | 8 Bit <br/>  | Prolog-Länge <br/>   | Die Anzahl der Anweisungen im Prolog der Funktion. <br/>                                                          |
| 4 <br/> | 22 Bits <br/> | Funktions Länge <br/> | Die Anzahl der Anweisungen in der Funktion. <br/>                                                                   |
| 4 <br/> | 1 Bit <br/>   | 32-Bit-Flag <br/>     | Wenn festgelegt, besteht die Funktion aus 32-Bit-Anweisungen. Wenn Clear, besteht die Funktion aus 16-Bit-Anweisungen. <br/> |
| 4 <br/> | 1 Bit <br/>   | Exception-Flag <br/>  | Wenn festgelegt, ist ein Ausnahmehandler für die Funktion vorhanden. Andernfalls ist kein Ausnahmehandler vorhanden. <br/>                 |



 

Für x64-und Itanium-Plattformen haben Funktionstabellen Einträge das folgende Format:



| Offset        | Size          | Feld                          | BESCHREIBUNG                                        |
|---------------|---------------|--------------------------------|----------------------------------------------------|
| 0 <br/> | 4 <br/> | BEGIN Address <br/>      | Die RVA der entsprechenden Funktion. <br/> |
| 4 <br/> | 4 <br/> | Endadresse <br/>        | Die RVA am Ende der Funktion. <br/>    |
| 8 <br/> | 4 <br/> | Informationen zum Entladen <br/> | Die RVA der Entlade Informationen. <br/>     |



 

### <a name="the-reloc-section-image-only"></a>Der. reloc-Abschnitt (nur Bild)

Die Basis Verschiebungs Tabelle enthält Einträge für alle Basis Umsetzungen im Image. Das Feld für die Basis Verschiebungs Tabelle in den optionalen Header Daten Verzeichnissen gibt die Anzahl der Bytes in der Basis Verschiebungs Tabelle an. Weitere Informationen finden Sie unter [optionale Header Datenverzeichnisse (nur Bild)](#optional-header-data-directories-image-only). Die Basis Verschiebungs Tabelle ist in Blöcke unterteilt. Jeder-Block stellt die Basis Umsetzungen für eine 4K-Seite dar. Jeder Block muss an einer 32-Bit-Grenze beginnen.

Das Lade Tool ist nicht erforderlich, um Basis Umsetzungen zu verarbeiten, die vom Linker aufgelöst werden, es sei denn, das Lade Abbild kann nicht an der Bildbasis geladen werden, die im PE-Header angegeben ist.

#### <a name="base-relocation-block"></a>Basis Verschiebungs Block

Jeder Basis Verschiebungs Block beginnt mit der folgenden Struktur:



| Offset        | Size          | Feld                  | BESCHREIBUNG                                                                                                                                              |
|---------------|---------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Seiten-RVA <br/>   | Die Bildbasis Plus RVA der Seite wird jedem Offset hinzugefügt, um das VA zu erstellen, in dem die Basis Verschiebung angewendet werden muss. <br/>                         |
| 4 <br/> | 4 <br/> | Blockgröße <br/> | Die Gesamtanzahl der Bytes im Basis Verschiebungs Block, einschließlich der Seiten-RVA-und Blockgrößen Felder und der folgenden Typen/Offset-Felder. <br/> |



 

Auf das Feld Block Größe folgt eine beliebige Anzahl von Typen-oder Offset Feld Einträgen. Jeder Eintrag ist ein Wort (2 Bytes) und weist die folgende Struktur auf:



| Offset        | Size                | Feld              | BESCHREIBUNG                                                                                                                                                                                                            |
|---------------|---------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 Bits <br/>  | type <br/>   | Ein Wert, der den Typ der zu verwendenden Basis Verschiebung angibt, der in den High 4 Bits des Worts gespeichert ist. Weitere Informationen finden Sie unter [Basis](#base-relocation-types)Verschiebungs Typen.<br/>                         |
| 0 <br/> | 12 Bits <br/> | Offset <br/> | Wird in den verbleibenden 12 Bits des Worts gespeichert, ein Offset von der Startadresse, die im RVA-Feld der Seite für den-Block angegeben wurde. Dieser Offset gibt an, wo die Basis Verschiebung angewendet werden soll. <br/> |



 

Um eine Basis Verschiebung anzuwenden, wird der Unterschied zwischen der bevorzugten Basisadresse und der Basis, an der das Image tatsächlich geladen wird, berechnet. Wenn das Bild an der bevorzugten Basis geladen wird, ist der Unterschied 0 (null), sodass die Basis Umsetzungen nicht angewendet werden müssen.

#### <a name="base-relocation-types"></a>Basis Verschiebungs Typen



| Konstante                                       | Wert          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| auf dem Image \_ rel \_ basiert \_ <br/>        | 0 <br/>  | Die grundlegende Verlagerung wird übersprungen. Dieser Typ kann zum Auffüllen eines-Blocks verwendet werden. <br/>                                                                                                                                                                                                                                                 |
| Image \_ rel \_ basiert \_ hoch <br/>            | 1 <br/>  | Bei der Basis Verschiebung werden die hohen 16 Bits des Unterschieds dem 16-Bit-Feld bei Offset hinzugefügt. Das 16-Bit-Feld stellt den hohen Wert eines 32-Bit-Worts dar. <br/>                                                                                                                                                               |
| Abbild \_ rel \_ basierend \_ niedrig <br/>             | 2 <br/>  | Bei der Basis Verschiebung werden die unteren 16 Bits der Differenz dem 16-Bit-Feld bei Offset hinzugefügt. Das 16-Bit-Feld stellt die niedrige Hälfte eines 32-Bit-Worts dar. <br/>                                                                                                                                                                  |
| Image \_ rel \_ based \_ highlow <br/>         | 3 <br/>  | Bei der Basis Verlagerung werden alle 32 Bits des Unterschieds auf das 32-Bit-Feld bei Offset angewendet. <br/>                                                                                                                                                                                                                              |
| Image \_ rel- \_ basiertes \_ highadj <br/>         | 4 <br/>  | Bei der Basis Verschiebung werden die hohen 16 Bits des Unterschieds dem 16-Bit-Feld bei Offset hinzugefügt. Das 16-Bit-Feld stellt den hohen Wert eines 32-Bit-Worts dar. Die unteren 16 Bits des 32-Bit-Werts werden in dem 16-Bit-Wort gespeichert, das dieser Basis Verlagerung folgt. Dies bedeutet, dass diese Basis Verlagerung zwei Slots einnimmt. <br/> |
| \_auf Image rel \_ basierende \_ MIPS \_ jmpaddr <br/>   | 5 <br/>  | Die Verschiebungs Interpretation ist vom Computertyp abhängig. <br/> Wenn der Computertyp MIPS ist, gilt die Basis Verlagerung für eine MIPS-Sprung Anweisung. <br/>                                                                                                                                                    |
| Image \_ rel \_ based \_ Arm \_ MOV32 <br/>      | 5 <br/>  | Diese Verschiebung ist nur dann sinnvoll, wenn der Computertyp "Arm" oder "Thumb" ist. Bei der Basis Verschiebung wird die 32-Bit-Adresse eines Symbols über ein aufeinander folgender Anweisungs paar von "muvw/muvt" angewendet. <br/>                                                                                                                                 |
| Image \_ rel- \_ basiertes \_ riscv \_ HIGH20 <br/>   | 5 <br/>  | Diese Verschiebung ist nur dann von Bedeutung, wenn der Computertyp RISC-V ist. Die Basis Verschiebung gilt für die hohen 20 Bits einer absoluten 32-Bit-Adresse. <br/>                                                                                                                                                                     |
|                                                | 6 <br/>  | Reserviert, muss NULL sein. <br/>                                                                                                                                                                                                                                                                                               |
| Bild- \_ rel- \_ basiertes Thumb- \_ \_ MOV32 <br/>    | 7 <br/>  | Diese Verschiebung ist nur sinnvoll, wenn der Computertyp Thumb ist. Bei der Basis Verschiebung wird die 32-Bit-Adresse eines Symbols auf ein aufeinander folgender Anweisungs paar von "muvw/muvt" angewendet. <br/>                                                                                                                                            |
| Image \_ rel- \_ basiertes \_ riscv \_ LOW12I <br/>   | 7 <br/>  | Diese Verschiebung ist nur dann von Bedeutung, wenn der Computertyp RISC-V ist. Die Basis Verschiebung gilt für die unteren 12 Bits einer absoluten 32-Bit-Adresse, die im RISC-V-I-Type-Anweisungs Format gebildet wird. <br/>                                                                                                                           |
| Image \_ rel- \_ basiertes \_ riscv \_ LOW12S <br/>   | 8 <br/>  | Diese Verschiebung ist nur dann von Bedeutung, wenn der Computertyp RISC-V ist. Die Basis Verschiebung gilt für die unteren 12 Bits einer absoluten 32-Bit-Adresse, die im RISC-V S-Type-Anweisungs Format gebildet wird. <br/>                                                                                                                           |
| \_Auf Image rel \_ basierende MIPS- \_ \_ JMPADDR16 <br/> | 9 <br/>  | Die Verschiebung ist nur sinnvoll, wenn der Computertyp MIPS ist. Die Basis Verschiebung gilt für eine MIPS16 Jump-Anweisung. <br/>                                                                                                                                                                                            |
| Image \_ rel \_ based \_ DIR64 <br/>           | 10 <br/> | Die Basis Verschiebung wendet den Unterschied auf das 64-Bit-Feld bei Offset an. <br/>                                                                                                                                                                                                                                             |



 

### <a name="the-tls-section"></a>Der. TLS-Abschnitt

Der Abschnitt ". TLS" bietet direkte PE-und COFF-Unterstützung für den statischen Thread lokalen Speicher (TLS). TLS ist eine spezielle Speicher Klasse, die von Windows unterstützt wird, wenn ein Datenobjekt keine automatische (Stapel-) Variable ist, sondern für jeden einzelnen Thread, der den Code ausführt, lokal ist. Daher kann jeder Thread einen anderen Wert für eine Variable, die mithilfe von TLS deklariert wurde, beibehalten.

Beachten Sie, dass jede Menge an TLS-Daten mithilfe der API-Aufrufe TlsAlloc, TlsFree, TlsSetValue und TlsGetValue unterstützt werden kann. Die PE-oder COFF-Implementierung ist ein alternativer Ansatz für die Verwendung der API und hat den Vorteil, dass Sie von der Programmiersprache der Programmiersprache der Programmiersprache einfacher ist. Diese Implementierung ermöglicht das definieren und Initialisieren von TLS-Daten auf ähnliche Weise wie gewöhnliche statische Variablen in einem Programm. Beispielsweise kann in Visual C++ eine statische TLS-Variable wie folgt definiert werden, ohne die Windows-API zu verwenden:

`__declspec (thread) int tlsFlag = 1;`

Um dieses Programmierkonstrukt zu unterstützen, gibt der PE-und COFF. TLS-Abschnitt die folgenden Informationen an: Initialisierungs Daten, Rückruf Routinen für die Thread spezifische Initialisierung und Beendigung sowie den TLS-Index, der in der folgenden Erörterung erläutert wird.

> [!Note]
>
> Statisch deklarierte TLS-Datenobjekte können nur in statisch geladenen Bilddateien verwendet werden. Dies macht es unzuverlässig, statische TLS-Daten in einer DLL zu verwenden, es sei denn, Sie wissen, dass die dll oder etwas, das statisch verknüpft ist, nie dynamisch mit der LoadLibrary-API-Funktion geladen wird.

 

Der ausführbare Code greift mithilfe der folgenden Schritte auf ein statisches TLS-Datenobjekt zu:

1.  Zur Verknüpfungs Zeit legt der Linker die Adresse des Index Felds des TLS-Verzeichnisses fest. Dieses Feld verweist auf einen Speicherort, an dem das Programm den TLS-Index empfängt.

    Die Microsoft-Lauf Zeit Bibliothek vereinfacht diesen Vorgang, indem ein Speicher Abbild des TLS-Verzeichnisses definiert und diesem der Sondername " \_ \_ TLS \_ used" (Intel x86-Plattformen) oder " \_ TLS \_ used" (andere Plattformen) erteilt wird. Der Linker sucht nach diesem Speicher Image und verwendet die Daten dort, um das TLS-Verzeichnis zu erstellen. Andere Compiler, die TLS unterstützen und mit dem Microsoft-Linker arbeiten, müssen dieselbe Technik verwenden.

2.  Wenn ein Thread erstellt wird, kommuniziert das Lade Modul die Adresse des TLS-Arrays des Threads, indem die Adresse des Thread Umgebungs Blocks (TEB) im FS-Register platziert wird. Ein Zeiger auf das TLS-Array befindet sich am Offset von 0x2c vom Anfang des TEB. Dieses Verhalten ist Intel x86-spezifisch.

3.  Das Lade Modul weist den Wert des TLS-Indexes an der Stelle zu, die durch die Adresse des Index Felds angegeben wurde.

4.  Der ausführbare Code Ruft den TLS-Index und auch den Speicherort des TLS-Arrays ab.

5.  Der Code verwendet den TLS-Index und den Speicherort des TLS-Arrays (multipliziert mit dem Index um 4 und verwendet ihn als Offset für das Array), um die Adresse des TLS-Datenbereichs für das angegebene Programm und Modul zu erhalten. Jeder Thread verfügt über einen eigenen TLS-Datenbereich. dieser ist jedoch für das Programm transparent, was nicht wissen muss, wie Daten für einzelne Threads zugeordnet werden.

6.  Auf ein einzelnes TLS-Datenobjekt wird als fester Offset im TLS-Datenbereich zugegriffen.

Das TLS-Array ist ein Array von Adressen, die vom System für jeden Thread verwaltet werden. Jede Adresse in diesem Array gibt den Speicherort der TLS-Daten für ein bestimmtes Modul (exe oder dll) innerhalb des Programms an. Der TLS-Index gibt den Member des Arrays an, der verwendet werden soll. Der Index ist eine Zahl (nur für das System sinnvoll), die das Modul identifiziert.

#### <a name="the-tls-directory"></a>Das TLS-Verzeichnis

Das TLS-Verzeichnis weist das folgende Format auf:



| Offset (das Format PE32/das Format PE32 +) | Größe (das Format PE32/das Format PE32 +) | Feld                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                         |
|----------------------|--------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>        | 4/8 <br/>    | Start-VA für Rohdaten <br/>    | Die Startadresse der TLS-Vorlage. Die Vorlage ist ein Datenblock, der zum Initialisieren von TLS-Daten verwendet wird. Das System kopiert alle diese Daten jedes Mal, wenn ein Thread erstellt wird, sodass er nicht beschädigt werden darf. Beachten Sie, dass diese Adresse keine RVA ist. Dabei handelt es sich um eine Adresse, für die im Abschnitt ". reloc" eine grundlegende Verlagerung vorhanden sein sollte. <br/> |
| 4/8 <br/>      | 4/8 <br/>    | Rohdaten Ende VA <br/>      | Die Adresse des letzten Bytes des TLS, mit Ausnahme der Füllung NULL. Wie beim Start-VA-Feld für Rohdaten ist dies ein VA und kein RVA. <br/>                                                                                                                                                                                                       |
| 8/16 <br/>     | 4/8 <br/>    | Adresse des Indexes <br/>     | Die Position, an der der TLS-Index empfangen werden soll, den das Lade Modul zuweist Dieser Speicherort befindet sich in einem normalen Daten Abschnitt, sodass ihm ein symbolischer Name zugewiesen werden kann, der für das Programm zugänglich ist. <br/>                                                                                                                                                    |
| 12/24 <br/>    | 4/8 <br/>    | Adresse der Rückrufe <br/> | Der Zeiger auf ein Array von TLS-Rückruf Funktionen. Das Array wird auf NULL festgelegt. wenn keine Rückruffunktion unterstützt wird, verweist dieses Feld auf 4 Bytes, die auf 0 (null) festgelegt sind. Weitere Informationen zum Prototyp für diese Funktionen finden Sie unter [TLS-Rückruf Funktionen](#tls-callback-functions).<br/>                                                      |
| 16/32 <br/>    | 4 <br/>      | Größe von 0 (null) <br/>    | Die Größe der Vorlage (in Bytes), die über die durch die unformatierten Felder Raw Data Start VA und RAW Data End VA getrennte initialisierten Daten hinausgeht. Die Gesamtgröße der Vorlage sollte mit der Gesamtgröße der TLS-Daten in der Bilddatei identisch sein. Der Wert 0 (null) ist die Datenmenge, die nach den initialisierten Daten ungleich 0 (null) liegt. <br/>                            |
| 20/36 <br/>    | 4 <br/>      | Merkmale <br/>      | In den vier Bits \[ 23:20 werden \] Ausrichtungs Informationen beschrieben. Mögliche Werte sind die als Bild-SCN-Ausrichtung definierten Werte \_ \_ \_ \* , die auch zum Beschreiben der Ausrichtung des Abschnitts in Objektdateien verwendet werden. Die anderen 28 Bits sind für die zukünftige Verwendung reserviert. <br/>                                                                                                       |



 

#### <a name="tls-callback-functions"></a>TLS-Rückruf Funktionen

Das Programm kann eine oder mehrere TLS-Rückruf Funktionen bereitstellen, um die zusätzliche Initialisierung und Beendigung von TLS-Datenobjekten zu unterstützen. Eine solche Rückruffunktion wird normalerweise zum Abrufen von Konstruktoren und Dekonstruktoren für-Objekte verwendet.

Obwohl es in der Regel nicht mehr als eine Rückruffunktion gibt, wird ein Rückruf als Array implementiert, damit Sie bei Bedarf weitere Rückruf Funktionen hinzufügen können. Wenn mehr als eine Rückruffunktion vorhanden ist, wird jede Funktion in der Reihenfolge aufgerufen, in der die Adresse im Array angezeigt wird. Ein NULL-Zeiger beendet das Array. Es ist durchaus zulässig, eine leere Liste zu haben (kein Rückruf wird unterstützt). in diesem Fall hat das Rückruf Array genau ein Element, d. h. einen NULL-Zeiger.

Der Prototyp für eine Rückruffunktion (auf die durch einen Zeiger vom Typ pimage- \_ TLS \_ -Rückruf verwiesen wird) verfügt über dieselben Parameter wie eine DLL-Einstiegspunkt Funktion:


```C++
typedef VOID
(NTAPI *PIMAGE_TLS_CALLBACK) (
    PVOID DllHandle,
    DWORD Reason,
    PVOID Reserved
    );
```



Der reservierte Parameter muss auf 0 (null) festgelegt werden. Der Reason-Parameter kann die folgenden Werte annehmen:



| Einstellung                          | Wert         | BESCHREIBUNG                                                                                          |
|----------------------------------|---------------|------------------------------------------------------------------------------------------------------|
| DLL- \_ Prozess \_ Anfügen <br/> | 1 <br/> | Ein neuer Prozess wurde gestartet, einschließlich des ersten Threads. <br/>                                   |
| DLL- \_ Thread \_ Anfügen <br/>  | 2 <br/> | Es wurde ein neuer Thread erstellt. Diese Benachrichtigung wird nur für den ersten Thread gesendet. <br/>      |
| Trennen des DLL- \_ Threads \_ <br/>  | 3 <br/> | Ein Thread wird beendet. Diese Benachrichtigung wird nur für den ersten Thread gesendet. <br/> |
| Trennen des DLL- \_ Prozesses \_ <br/> | 0 <br/> | Ein Prozess wird beendet, einschließlich des ursprünglichen Threads. <br/>                          |



 

### <a name="the-load-configuration-structure-image-only"></a>Struktur der Lade Konfiguration (nur Bild)

Die Struktur der Lade Konfiguration (config-Verzeichnis für die Image \_ Auslastung \_ \_ ) wurde in sehr eingeschränkten Fällen im Windows NT-Betriebssystem selbst verwendet, um verschiedene Funktionen zu beschreiben, die zu schwierig oder zu groß sind, um Sie im Dateiheader oder im optionalen Header des Bilds zu beschreiben. In den aktuellen Versionen von Microsoft Linker und Windows XP und höheren Versionen von Windows wird eine neue Version dieser Struktur für x86-Systeme mit 32-Bit-Version verwendet, die reservierte SEH-Technologien enthalten. Dadurch wird eine Liste von sicheren strukturierten Ausnahme Handlern bereitstellt, die das Betriebssystem während der Ausnahme Verteilung verwendet. Wenn sich die handleradresse im VA-Bereich eines Bilds befindet und als reservierte SEH-fähig markiert ist (d. h., dass die Image- \_ dllcharakteristika \_ No \_ SEH im DllCharacteristics-Feld des optionalen Headers, wie zuvor beschrieben, gelöscht wurde), muss der Handler in der Liste der bekannten sicheren Handler für das Bild enthalten sein. Andernfalls wird die Anwendung vom Betriebssystem beendet. Dadurch wird verhindert, dass in der Vergangenheit die "x86 Exception Handler Hijacking"-Ausnutzung verwendet wurde, um die Kontrolle über das Betriebssystem zu übernehmen.

Der Microsoft-Linker stellt automatisch eine standardmäßige Lade Konfigurations Struktur bereit, um die reservierten SEH-Daten einzubeziehen. Wenn der Benutzercode bereits eine Konfigurations Struktur für den Ladevorgang bereitstellt, muss er die neuen reservierten SEH-Felder enthalten. Andernfalls kann der Linker nicht die reservierten SEH-Daten enthalten, und das Bild ist nicht als enthaltene reservierte SEH gekennzeichnet.

#### <a name="load-configuration-directory"></a>Konfigurationsverzeichnis laden

Im Datenverzeichnis Eintrag für eine vorab reservierte SEH-Lade Konfigurations Struktur muss eine bestimmte Größe der Lade Konfigurations Struktur angegeben werden, da das Betriebssystem-Lade Modul stets einen bestimmten Wert erwartet. In diesem Zusammenhang ist die Größe tatsächlich nur eine Versions Überprüfung. Aus Kompatibilitätsgründen mit Windows XP und früheren Versionen von Windows muss die Größe 64 für x86-Images betragen.

#### <a name="load-configuration-layout"></a>Konfigurations Layout laden

Die Struktur der Lade Konfiguration weist das folgende Layout für 32-Bit-und 64-Bit PE-Dateien auf:



| Offset              | Size            | Feld                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                 |
|---------------------|-----------------|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>       | 4 <br/>   | Merkmale <br/>                | Flags, die Attribute der Datei angeben, die derzeit nicht verwendet werden. <br/>                                                                                                                                                                                                                   |
| 4 <br/>       | 4 <br/>   | TimeDateStamp <br/>                  | Datums-und Zeitstempelwert. Der Wert wird in der Anzahl der Sekunden dargestellt, die seit Mitternacht (00:00:00), dem 1. Januar 1970, der universellen koordinierten Zeit, gemäß der Systemuhr verstrichen sind. Der Zeitstempel kann mithilfe der C-Lauf Zeitfunktion (CRT) gedruckt werden. <br/> |
| 8 <br/>       | 2 <br/>   | MajorVersion <br/>                   | Hauptversionsnummer. <br/>                                                                                                                                                                                                                                                           |
| 10 <br/>      | 2 <br/>   | MinorVersion <br/>                   | Nebenversionsnummer. <br/>                                                                                                                                                                                                                                                           |
| 12 <br/>      | 4 <br/>   | Globalflagsclear <br/>               | Die globalen ladeflags, die für diesen Prozess gelöscht werden sollen, wenn der Ladevorgang den Prozess startet. <br/>                                                                                                                                                                                             |
| 16 <br/>      | 4 <br/>   | Globalflagsset <br/>                 | Die globalen lademoflags, die für diesen Prozess festgelegt werden, wenn das Lade Modul den Prozess startet. <br/>                                                                                                                                                                                               |
| 20 <br/>      | 4 <br/>   | Criticalsectiondefaulttimeout <br/>  | Der standardmäßige Timeout Wert, der für die kritischen Abschnitte dieses Prozesses verwendet werden soll, die abgebrochen werden. <br/>                                                                                                                                                                                       |
| 24 <br/>      | 4/8 <br/> | "Debug-Block Threshold" <br/>     | Arbeitsspeicher, der freigegeben werden muss, bevor er an das System zurückgegeben wird (in Bytes). <br/>                                                                                                                                                                                                        |
| 28/32 <br/>   | 4/8 <br/> | "De committotalfrethreshold" <br/>     | Gesamtmenge des freien Speicherplatzes in Bytes. <br/>                                                                                                                                                                                                                                          |
| 32/40 <br/>   | 4/8 <br/> | Lockprefixtable <br/>                | \[x86 nur \] das VA einer Liste von Adressen, in denen das Sperr Präfix verwendet wird, sodass Sie durch NOP auf Computern mit einem Prozessor ersetzt werden können. <br/>                                                                                                                                    |
| 36/48 <br/>   | 4/8 <br/> | Maximumallocationsize <br/>          | Maximale Zuordnungs Größe in Bytes. <br/>                                                                                                                                                                                                                                              |
| 40/56 <br/>   | 4/8 <br/> | Virtualmemorythreshold <br/>         | Maximale Größe des virtuellen Speichers in Bytes. <br/>                                                                                                                                                                                                                                          |
| 44/64 <br/>   | 4/8 <br/> | Processaffinitymask <br/>            | Das Festlegen dieses Felds auf einen Wert ungleich 0 (null) entspricht dem Aufrufen von setprocessaffinitymask mit diesem Wert während des Prozess Starts (nur exe-Datei). <br/>                                                                                                                                       |
| 48/72 <br/>   | 4 <br/>   | Processheapflags <br/>               | Prozessheap-Flags, die dem ersten Argument der HeapCreate-Funktion entsprechen. Diese Flags gelten für den Prozess Heap, der während des Prozess Starts erstellt wird. <br/>                                                                                                              |
| 52/76 <br/>   | 2 <br/>   | CSDVersion <br/>                     | Der Service Pack Versions Bezeichner. <br/>                                                                                                                                                                                                                                            |
| 54/78 <br/>   | 2 <br/>   | Reserviert <br/>                       | Muss Null sein. <br/>                                                                                                                                                                                                                                                                   |
| 56/80 <br/>   | 4/8 <br/> | Editlist <br/>                       | Reserviert für die Verwendung durch das System. <br/>                                                                                                                                                                                                                                                 |
| 60/88 <br/>   | 4/8 <br/> | Securitycookie <br/>                 | Ein Zeiger auf ein Cookie, das von Visual C++-oder GS-Implementierung verwendet wird. <br/>                                                                                                                                                                                                          |
| 64/96 <br/>   | 4/8 <br/> | "-Handlertable" <br/>                 | \[x86 nur \] die VA der sortierten RVAs-Tabelle jedes gültigen, eindeutigen SE-Handlers im Image. <br/>                                                                                                                                                                                  |
| 68/104 <br/>  | 4/8 <br/> | "-Handlercount" <br/>                 | \[x86 gibt nur \] die Anzahl eindeutiger Handler in der Tabelle an. <br/>                                                                                                                                                                                                                         |
| 72/112 <br/>  | 4/8 <br/> | Guardcfcheckfunctionpointer <br/>    | Der VA, bei dem der Check-Function-Zeiger für den Ablauf Steuerungs Wächter gespeichert wird. <br/>                                                                                                                                                                                                               |
| 76/120 <br/>  | 4/8 <br/> | Guardcfdispatchfunctionpointer <br/> | Der VA, bei dem der Dispatch-Funktionszeiger für den Ablauf Steuerungs Wächter gespeichert wird. <br/>                                                                                                                                                                                                            |
| 80/128 <br/>  | 4/8 <br/> | Guardcffunctiontable <br/>           | Der VA der sortierten Tabelle der RVAs der einzelnen Ablauf Steuerungs Schutz-Funktionen im Bild. <br/>                                                                                                                                                                                            |
| 84/136 <br/>  | 4/8 <br/> | Guardcffunctioncount <br/>           | Die Anzahl eindeutiger RVAs in der obigen Tabelle. <br/>                                                                                                                                                                                                                                    |
| 88/144 <br/>  | 4 <br/>   | "Guardflags" <br/>                     | Die Flags des Ablauf Steuerungs Schutzes. <br/>                                                                                                                                                                                                                                               |
| 92/148 <br/>  | 12 <br/>  | Der codeintegrity <br/>                  | Code Integritäts Informationen. <br/>                                                                                                                                                                                                                                                     |
| 104/160 <br/> | 4/8 <br/> | Guardadresssstakeniatentrytable <br/> | Die VA, in der die Ablauf Steuerungs Wächter-Adresse die IAT-Tabelle erstellt hat <br/>                                                                                                                                                                                                              |
| 108/168 <br/> | 4/8 <br/> | Guardadresssstakeniatentrycount <br/> | Die Anzahl eindeutiger RVAs in der obigen Tabelle. <br/>                                                                                                                                                                                                                                    |
| 112/176 <br/> | 4/8 <br/> | "Guardlongjumptarge" <br/>       | Die VA, in der die Ablauf Steuerungs Wächter-Tabelle mit langem Sprungziel gespeichert wird. <br/>                                                                                                                                                                                                               |
| 116/184 <br/> | 4/8 <br/> | Guardlongjumptargetcount <br/>       | Die Anzahl eindeutiger RVAs in der obigen Tabelle. <br/>                                                                                                                                                                                                                                    |



 

Das Feld "guardflags" enthält eine Kombination aus einem oder mehreren der folgenden Flags und unter Feldern:

-   Das Modul führt mithilfe der vom System bereitgestellten Unterstützung Ablauf Steuerungs Integritätsprüfungen durch.

    ` #define IMAGE_GUARD_CF_INSTRUMENTED  0x00000100`

-   Das Modul führt Ablauf Steuerungs-und Schreib Integritätsprüfungen durch.

    ` #define IMAGE_GUARD_CFW_INSTRUMENTED  0x00000200`

-   Das Modul enthält gültige Metadaten für Ablauf Steuerungs Ziel.

    `#define IMAGE_GUARD_CF_FUNCTION_TABLE_PRESENT  0x00000400`

-   Das Modul verwendet nicht das/GS Security Cookie.

    ` #define IMAGE_GUARD_SECURITY_COOKIE_UNUSED  0x00000800`

-   Module unterstützt Schreib geschütztes verzögertes Laden (IAT).

    `#define IMAGE_GUARD_PROTECT_DELAYLOAD_IAT  0x00001000`

-   Delta Load Import Table in einem eigenen. didat-Abschnitt (ohne weitere darin), der frei geschützt werden kann.

    ` #define IMAGE_GUARD_DELAYLOAD_IAT_IN_ITS_OWN_SECTION  0x00002000`

-   Das Modul enthält unterdrückte Export Informationen. Dadurch wird auch die Adresse der IAT-Tabelle angezeigt, die in der Lade Konfiguration enthalten ist.

    `#define  IMAGE_GUARD_CF_EXPORT_SUPPRESSION_INFO_PRESENT  0x00004000`

-   Das Modul ermöglicht die Unterdrückung von Exporten.

    `#define IMAGE_GUARD_CF_ENABLE_EXPORT_SUPPRESSION  0x00008000`

-   Das Modul enthält Informationen zum longjmp-Ziel.

    ` #define IMAGE_GUARD_CF_LONGJUMP_TABLE_PRESENT  0x00010000`

-   Maske für das Unterfeld, das den Schritt der Ablauf Steuerungs Schutz-Funktionstabellen Einträge enthält (d. h. die zusätzliche Anzahl von Bytes pro Tabelleneintrag).

    ` #define IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_MASK  0xF0000000`

Außerdem definiert der Windows SDK Winnt. h-Header dieses Makro für die Menge der Bits, um den Wert von "guardflags" mit der rechten Maustaste zu ändern, um die Ablauf Steuerungs Schutz-Funktions Tabelle zu rechtfertigen:

` #define IMAGE_GUARD_CF_FUNCTION_TABLE_SIZE_SHIFT  28`

### <a name="the-rsrc-section"></a>Der Abschnitt ". rsrc"

Ressourcen werden durch eine Binär sortierte Struktur auf mehreren Ebenen indiziert. Der allgemeine Entwurf kann 2 \* \* 31 Ebenen umfassen. Gemäß der Konvention verwendet Windows jedoch drei Ebenen:

<dl> type  
Name  
Sprache  
</dl>

Eine Reihe von Ressourcenverzeichnis Tabellen verknüpft alle Ebenen auf folgende Weise: auf jede Verzeichnis Tabelle folgt eine Reihe von Verzeichnis Einträgen, die den Namen oder Bezeichner (ID) für diese Ebene (Typ, Name oder Sprachebene) und eine Adresse einer Daten Beschreibung oder einer anderen Verzeichnis Tabelle angeben. Wenn die Adresse auf eine Daten Beschreibung verweist, handelt es sich bei den Daten um ein Blatt in der Struktur. Wenn die Adresse auf eine andere Verzeichnis Tabelle zeigt, werden in dieser Tabelle die Verzeichniseinträge auf der nächsten Ebene nach unten aufgelistet.

Der Typ, der Name und die Sprach-IDs eines Blatts werden durch den Pfad bestimmt, der durch Verzeichnis Tabellen zum Erreichen des Blatts übernommen wird. Die erste Tabelle bestimmt die Typ-ID, die zweite Tabelle (auf die durch den Verzeichniseintrag in der ersten Tabelle verwiesen wird) die namens-ID und die dritte Tabelle die Sprach-ID.

Die allgemeine Struktur des Abschnitts ". rsrc" lautet:



| Daten                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ressourcenverzeichnis Tabellen (und Ressourcenverzeichnis Einträge) <br/> | Eine Reihe von Tabellen, eine für jede Gruppe von Knoten in der Struktur. Alle Knoten der obersten Ebene (Type) werden in der ersten Tabelle aufgeführt. Einträge in dieser Tabelle verweisen auf Tabellen der zweiten Ebene. Jede Struktur der zweiten Ebene hat dieselbe Typkennung, aber unterschiedliche namens-IDs. Strukturen der dritten Ebene verfügen über dieselben Typ-und namens-IDs, aber unterschiedliche Sprach-IDs. <br/> Auf jede einzelne Tabelle folgen unmittelbar Verzeichniseinträge, in denen jeder Eintrag einen Namen oder einen numerischen Bezeichner und einen Zeiger auf eine Daten Beschreibung oder eine Tabelle auf der nächst niedrigeren Ebene aufweist. <br/> |
| Ressourcenverzeichnis Zeichenfolgen <br/>                                 | Unicode-Zeichen folgen mit zwei Byte Ausrichtung, die als Zeichen folgen Daten dienen, auf die von Verzeichnis Einträgen verwiesen wird. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Beschreibung der Ressourcen Daten <br/>                                  | Ein Array von Datensätzen, auf das von Tabellen verwiesen wird, die die tatsächliche Größe und den Speicherort der Ressourcen Daten beschreiben. Diese Datensätze sind die Blätter in der Ressourcen Beschreibungs Struktur. <br/>                                                                                                                                                                                                                                                                                                                                                                |
| Ressourcendaten <br/>                                              | Rohdaten des Ressourcen Abschnitts. Die Größen-und Speicherort Informationen im Feld für die Ressourcen Daten Beschreibungen trennen die einzelnen Bereiche der Ressourcen Daten. <br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

#### <a name="resource-directory-table"></a>Ressourcenverzeichnis Tabelle

Jede Ressourcenverzeichnis Tabelle weist das folgende Format auf. Diese Datenstruktur sollte als Überschrift einer Tabelle betrachtet werden, da die Tabelle tatsächlich aus Verzeichnis Einträgen besteht (siehe Abschnitt 6.9.2, "Ressourcenverzeichnis Einträge") und dieser Struktur:



| Offset         | Size          | Feld                              | BESCHREIBUNG                                                                                                                                                                     |
|----------------|---------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Merkmale <br/>        | Ressourcenflags. Dieses Feld ist für eine spätere Verwendung vorgesehen. Er ist zurzeit auf 0 (null) festgelegt. <br/>                                                                                 |
| 4 <br/>  | 4 <br/> | Datums-/Uhrzeitstempel <br/>        | Der Zeitpunkt, zu dem die Ressourcen Daten vom Ressourcen Compiler erstellt wurden. <br/>                                                                                               |
| 8 <br/>  | 2 <br/> | Hauptversion <br/>          | Die Hauptversionsnummer, die vom Benutzer festgelegt wird. <br/>                                                                                                                          |
| 10 <br/> | 2 <br/> | Nebenversion <br/>          | Die neben Versionsnummer, die vom Benutzer festgelegt wird. <br/>                                                                                                                          |
| 12 <br/> | 2 <br/> | Anzahl der namens Einträge <br/> | Die Anzahl der Verzeichniseinträge, die unmittelbar auf die Tabelle folgen, die Zeichen folgen zur Identifizierung von Typ-, Namens-oder sprach Einträgen verwenden (abhängig von der Ebene der Tabelle). <br/> |
| 14 <br/> | 2 <br/> | Anzahl der ID-Einträge <br/>   | Die Anzahl der Verzeichniseinträge direkt nach den Namenseinträgen, die numerische IDs für Typ-, Namens-oder sprach Einträge verwenden. <br/>                                    |



 

#### <a name="resource-directory-entries"></a>Ressourcenverzeichnis Einträge

Die Verzeichniseinträge bilden die Zeilen einer Tabelle. Jeder Ressourcenverzeichnis Eintrag weist das folgende Format auf. Ob der Eintrag ein Name oder ein ID-Eintrag ist, wird durch die Ressourcenverzeichnis Tabelle angegeben, die angibt, wie viele Namen-und ID-Einträge darauf folgen (Beachten Sie, dass alle namens Einträge allen ID-Einträgen der Tabelle vorangestellt sind). Alle Einträge für die Tabelle werden in aufsteigender Reihenfolge sortiert: die namens Einträge nach Zeichenfolge mit Beachtung der Groß-/Kleinschreibung und die ID-Einträge nach numerischen Werten. Offsets sind relativ zur Adresse im Image \_ Verzeichnis \_ Entry \_ Resource DataDirectory. Weitere Informationen finden Sie unter [Peering innerhalb des PE: eine Tour durch das ausführbare Win32-Format der ausführbaren Datei](/previous-versions/ms809762(v=msdn.10)#pe-file-resources) .



| Offset        | Size          | Feld                           | BESCHREIBUNG                                                                                                          |
|---------------|---------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------|
| 0 <br/> | 4 <br/> | Namens Offset <br/>         | Der Offset einer Zeichenfolge, die den Typ, den Namen oder den Sprach-ID-Eintrag abhängig von der Ebene der Tabelle enthält. <br/>     |
| 0 <br/> | 4 <br/> | Ganzzahlige ID <br/>          | Eine 32-Bit-Ganzzahl, die den Typ, den Namen oder den Sprach-ID-Eintrag angibt. <br/>                                   |
| 4 <br/> | 4 <br/> | Dateneingabe Offset <br/>   | High-Bit 0. Adresse eines Ressourcen Daten Eintrags (ein Blatt). <br/>                                                   |
| 4 <br/> | 4 <br/> | Unterverzeichnis Offset <br/> | High-Bit 1. Bei den unteren 31 Bits handelt es sich um die Adresse einer anderen Ressourcenverzeichnis Tabelle (die nächste Ebene unten). <br/> |



 

#### <a name="resource-directory-string"></a>Ressourcenverzeichnis Zeichenfolge

Der Bereich der Ressourcenverzeichnis Zeichenfolge besteht aus Unicode-Zeichen folgen, die Wort orientiert sind. Diese Zeichen folgen werden in Verbindung mit dem letzten Ressourcenverzeichnis Eintrag und vor dem ersten Ressourcen Dateneintrag gespeichert. Dadurch wird die Auswirkung dieser Zeichen folgen variabler Länge auf die Ausrichtung der Verzeichniseinträge mit fester Größe minimiert. Jede Ressourcenverzeichnis Zeichenfolge weist das folgende Format auf:



| Offset        | Size                 | Feld                      | BESCHREIBUNG                                                            |
|---------------|----------------------|----------------------------|------------------------------------------------------------------------|
| 0 <br/> | 2 <br/>        | Länge <br/>         | Die Größe der Zeichenfolge ohne das Längenfeld selbst. <br/> |
| 2 <br/> | -Variable <br/> | Unicode-Zeichenfolge <br/> | Die Unicode-Zeichen folgen Daten variabler Länge, die Wort bündig sind. <br/>     |



 

#### <a name="resource-data-entry"></a>Ressourcen Dateneintrag

Jeder Ressourcen Dateneintrag beschreibt eine tatsächliche Einheit von Rohdaten im Ressourcen Datenbereich. Ein Ressourcen Dateneintrag weist das folgende Format auf:



| Offset         | Size          | Feld                            | BESCHREIBUNG                                                                                                                                           |
|----------------|---------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/> | Daten-RVA <br/>             | Die Adresse einer Einheit von Ressourcen Daten im Ressourcen Datenbereich. <br/>                                                                         |
| 4 <br/>  | 4 <br/> | Size <br/>                 | Die Größe der Ressourcen Daten in Bytes, auf die das RVA-Feld "Data" verweist. <br/>                                                        |
| 8 <br/>  | 4 <br/> | codepage <br/>             | Die Codepage, die verwendet wird, um Code Punktwerte in den Ressourcen Daten zu decodieren. In der Regel ist die Codepage die Unicode-Codepage. <br/> |
| 12 <br/> | 4 <br/> | Reserviert, muss 0 sein. <br/> |                                                                                                                                                       |



 

### <a name="the-cormeta-section-object-only"></a>Der. cormeta-Abschnitt (nur Objekt)

Die CLR-Metadaten werden in diesem Abschnitt gespeichert. Es wird verwendet, um anzugeben, dass die Objektdatei verwalteten Code enthält. Das Format der Metadaten ist nicht dokumentiert, kann aber an die CLR-Schnittstellen für die Verarbeitung von Metadaten übergeben werden.

### <a name="the-sxdata-section"></a>Der sxdata-Abschnitt

Die gültigen Ausnahmehandler eines Objekts sind im Abschnitt " **. sxdata** " dieses Objekts aufgeführt. Der Abschnitt ist als Bild- \_ SCN \_ lnk \_ Info gekennzeichnet. Sie enthält den COFF-Symbol Index jedes gültigen Handlers, wobei 4 Bytes pro Index verwendet werden.

Außerdem markiert der Compiler ein COFF-Objekt als registrierte Seh, indem das absolute Symbol " @feat.00 " mit dem lsb des Wertfelds ausgegeben wird, das auf 1 festgelegt ist. Ein COFF-Objekt ohne registrierte SEH-Handler hätte das " @feat.00 "-Symbol, aber keinen **sxdata** -Abschnitt.

## <a name="archive-library-file-format"></a>Archivdatei Format (Bibliothek)

- [Signatur der Archivdatei](#archive-file-signature)
- [Archivierungs Element Header](#archive-member-headers)
- [Erster Linker-Member](#first-linker-member)
- [Zweites Linker-Mitglied](#second-linker-member)
- [Longnames-Member](#longnames-member)

Das COFF-Archivformat bietet einen Standardmechanismus zum Speichern von Sammlungen von Objektdateien. Diese Sammlungen werden in der Programmier Dokumentation häufig als Bibliotheken bezeichnet.

Die ersten 8 Bytes eines Archivs bestehen aus der Datei Signatur. Der Rest des Archivs besteht aus einer Reihe von Archiv Elementen, wie im folgenden dargestellt:

-   Der erste und zweite Member sind "Linker-Member". Jedes dieser Member verfügt über ein eigenes Format, wie im Abschnitt [Import Name Type](#import-name-type)beschrieben. In der Regel werden von einem Linker Informationen in diese Archivierungs Elemente eingefügt. Die Linker-Member enthalten das Verzeichnis des Archivs.

-   Das dritte Element ist der "longnames"-Member. Dieses optionale Element besteht aus einer Reihe von null-terminierten ASCII-Zeichen folgen, in denen jede Zeichenfolge der Name eines anderen Archiv Elements ist.

-   Der Rest des Archivs besteht aus Standard Membern (Object-File). Jedes dieser Member enthält den Inhalt einer gesamten Objektdatei.

Ein Archiv Element Header geht vor jedem Member. Die folgende Liste zeigt die allgemeine Struktur eines Archivs:

-   Signatur: "! &lt; Arch &gt; \\ n "
-   Header

    <dl> 1. Linker-Member  
    </dl>

-   Header

    <dl> 2. Linker-Member  
    </dl>

-   Header

    <dl> Longnames-Member  
    </dl>

-   Header

    <dl> Inhalt der obj-Datei 1  
    (COFF-Format)  
    </dl>

-   Header

    <dl> Inhalt der obj-Datei 2  
    (COFF-Format)  
    </dl>

### <a name="archive-file-signature"></a>Signatur der Archivdatei

Die Signatur der Archivdatei identifiziert den Dateityp. Jedes Dienstprogramm (z. b. ein linker), das eine Archivdatei als Eingabe annimmt, kann den Dateityp durchlesen dieser Signatur überprüfen. Die Signatur besteht aus den folgenden ASCII-Zeichen, in denen jedes nachstehende Zeichen buchstäblich dargestellt wird, mit Ausnahme des Zeilen Umleitungs \\ Zeichens (n):

`!<arch>\n`

### <a name="archive-member-headers"></a>Archivierungs Element Header

Jedem Element (linker, longnames oder Object-File-Member) wird ein Header vorangestellt. Ein Archiv Element Header weist das folgende Format auf, wobei jedes Feld eine ASCII-Text Zeichenfolge ist, die bündig und mit Leerzeichen am Ende des Felds aufgefüllt wird. Es gibt kein abschließendes NULL-Zeichen in einem dieser Felder.

Jeder Element Header beginnt an der ersten geraden Adresse nach dem Ende des vorherigen Archiv Elements.



| Offset         | Size           | Feld                     | BESCHREIBUNG                                                                                                                                                                                                 |
|----------------|----------------|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 16 <br/> | Name <br/>          | Der Name des Archiv Members, wobei ein Schrägstrich (/) zum Beenden des Namens angefügt wird. Wenn das erste Zeichen ein Schrägstrich ist, hat der Name eine besondere Interpretation, wie in der folgenden Tabelle beschrieben. <br/> |
| 16 <br/> | 12 <br/> | Date <br/>          | Das Datum und die Uhrzeit der Erstellung des Archiv Members: Dies ist die ASCII-Dezimal Darstellung der Anzahl von Sekunden seit 1/1/1970 UCT. <br/>                                                    |
| 28 <br/> | 6 <br/>  | Benutzer-ID <br/>       | Eine ASCII-Dezimal Darstellung der Benutzer-ID. Dieses Feld enthält keinen sinnvollen Wert auf Windows-Plattformen, da Microsoft-Tools alle Leerzeichen ausgeben. <br/>                                    |
| 34 <br/> | 6 <br/>  | Gruppen-ID <br/>      | Eine ASCII-Dezimal Darstellung der Gruppen-ID. Dieses Feld enthält keinen sinnvollen Wert auf Windows-Plattformen, da Microsoft-Tools alle Leerzeichen ausgeben. <br/>                                   |
| 40 <br/> | 8 <br/>  | Mode <br/>          | Eine ASCII-Oktaldarstellung des Dateimodus des Members. Dies ist der St \_ -Moduswert aus der C-Lauf Zeitfunktion \_ wstat. <br/>                                                                       |
| 48 <br/> | 10 <br/> | Size <br/>          | Eine ASCII-Dezimal Darstellung der Gesamtgröße des Archiv Members, ohne die Größe des Headers. <br/>                                                                                  |
| 58 <br/> | 2 <br/>  | Ende der Kopfzeile <br/> | Die zwei Bytes in der C-Zeichenfolge " \\ . n" (0x60 0x0A). <br/>                                                                                                                                               |



 

Das Feld Name hat eines der in der folgenden Tabelle aufgeführten Formate. Wie bereits erwähnt, wird jede dieser Zeichen folgen in einem Feld von 16 Bytes mit nachfolgenden Leerzeichen aufgefüllt und mit nachfolgenden Leerzeichen aufgefüllt:



| Inhalt des Namens Felds | BESCHREIBUNG                                                                                                                                                                                                                                                                                          |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Benennen <br/>      | Der Name des Archivierungs Members. <br/>                                                                                                                                                                                                                                                          |
| / <br/>          | Der Archivierungs Member ist eines der beiden Linker-Member. Beide Linker-Member haben diesen Namen. <br/>                                                                                                                                                                                          |
| // <br/>         | Der Archive-Member ist das longnames-Element, das aus einer Reihe von mit NULL endenden ASCII-Zeichen folgen besteht. Der longnames-Member ist das dritte Archiv Element und optional. <br/>                                                                     |
| /n <br/>         | Der Name des Archivierungs Elements befindet sich in Offset n innerhalb des longnames-Members. Die Zahl n ist die Dezimal Darstellung des Offsets. Beispiel: "/26" gibt an, dass der Name des Archiv Members 26 Bytes nach dem Anfang der Elementinhalte von longnames liegt. <br/> |



 

### <a name="first-linker-member"></a>Erster Linker-Member

Der Name des ersten Linker-Members ist "/". Der erste Linker-Member ist aus Gründen der Abwärtskompatibilität eingeschlossen. Er wird nicht von aktuellen Linkern verwendet, aber sein Format muss korrekt sein. Dieses Linker-Element stellt ein Verzeichnis mit Symbolnamen bereit, ebenso wie das zweite Linker-Mitglied. Für jedes Symbol gibt die Informationen an, wo der Archivierungs Member zu finden ist, der das Symbol enthält.

Der erste Linker-Member weist das folgende Format auf. Diese Informationen werden nach dem-Header angezeigt:



| Offset         | Size               | Feld                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                        |
|----------------|--------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/>      | Anzahl von Symbolen <br/> | Unsigned long-Wert, der die Anzahl der indizierten Symbole enthält. Diese Zahl wird im Big-Endian-Format gespeichert. Jedes Objekt dateimember definiert in der Regel ein oder mehrere externe Symbole. <br/>                                                                                                                                                                         |
| 4 <br/>  | 4 \* n <br/> | Offsets <br/>           | Ein Array von Dateioffsets zum Archivieren von Element Headern, wobei n gleich dem Feld Anzahl von Symbolen ist. Jede Zahl im Array ist ein Ganzzahl ohne Vorzeichen Long-Wert, der im Big-Endian-Format gespeichert ist. Für jedes Symbol, das in der Zeichen folgen Tabelle benannt ist, gibt das entsprechende Element im Offsets-Array den Speicherort des Archiv Members an, der das Symbol enthält. <br/> |
| \* <br/> | \* <br/>     | Zeichen folgen Tabelle <br/>      | Eine Reihe von null-terminierten Zeichen folgen, die alle Symbole im Verzeichnis benennen. Jede Zeichenfolge beginnt unmittelbar nach dem NULL-Zeichen in der vorherigen Zeichenfolge. Die Anzahl der Zeichen folgen muss gleich dem Wert des Felds "Anzahl der Symbole" sein. <br/>                                                                                                       |



 

Die Elemente im Offsets-Array müssen in aufsteigender Reihenfolge angeordnet werden. Diese Tatsache impliziert, dass die Symbole in der Zeichen folgen Tabelle entsprechend der Reihenfolge der Archivierungs Elemente angeordnet werden müssen. Beispielsweise müssen alle Symbole im ersten objektdateimember vor den Symbolen in der zweiten Objektdatei aufgeführt werden.

### <a name="second-linker-member"></a>Zweites Linker-Mitglied

Das zweite Linker-Element hat den Namen "/", wie auch das erste Linker-Mitglied. Obwohl beide Linker-Member ein Verzeichnis von Symbolen und Archivierungs Membern bereitstellen, die Sie enthalten, wird der zweite Linker-Member bevorzugt für den ersten von allen aktuellen Linkern verwendet. Der zweite Linker-Member schließt Symbolnamen in lexikalischen Reihenfolge ein, sodass die Suche anhand des Namens schneller durchsucht werden kann.

Der zweite Member weist das folgende Format auf. Diese Informationen werden nach dem-Header angezeigt:



| Offset         | Size               | Feld                         | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|--------------------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 4 <br/>      | Anzahl der Mitglieder <br/> | Eine ganze Zahl ohne Vorzeichen, die die Anzahl der Archivierungs Elemente enthält. <br/>                                                                                                                                                                                                                                                                                                                                |
| 4 <br/>  | 4 \* Mio. <br/> | Offsets <br/>           | Ein Array von Dateioffsets zum Archivieren von Element Headern, angeordnet in aufsteigender Reihenfolge. Jeder Offset ist eine unsignierte Länge. Die Zahl m ist gleich dem Wert des Felds number of Members. <br/>                                                                                                                                                                                                        |
| \* <br/> | 4 <br/>      | Anzahl von Symbolen <br/> | Eine ganze Zahl ohne Vorzeichen, die die Anzahl der indizierten Symbole enthält. Jedes Objekt dateimember definiert in der Regel ein oder mehrere externe Symbole. <br/>                                                                                                                                                                                                                                                        |
| \* <br/> | 2 \* n <br/> | Kei <br/>           | Ein Array von 1-basierten Indizes (unsigned Short), das Symbolnamen den Archiv Element Offsets zuordnet. Die Zahl n ist gleich der Anzahl von Symbolen. Für jedes Symbol, das in der Zeichen folgen Tabelle benannt ist, gibt das entsprechende Element im Index Array einen Index in das Offsets-Array an. Das Offsets-Array gibt wiederum den Speicherort des Archiv Elements zurück, das das Symbol enthält. <br/> |
| \* <br/> | \* <br/>     | Zeichen folgen Tabelle <br/>      | Eine Reihe von null-terminierten Zeichen folgen, die alle Symbole im Verzeichnis benennen. Jede Zeichenfolge beginnt unmittelbar nach dem NULL-Byte in der vorherigen Zeichenfolge. Die Anzahl der Zeichen folgen muss gleich dem Wert des Felds "Anzahl der Symbole" sein. In dieser Tabelle werden alle Symbolnamen in aufsteigender lexikalischer Reihenfolge aufgelistet. <br/>                                                                             |



 

### <a name="longnames-member"></a>Longnames-Member

Der Name des longnames-Members lautet "//". Der longnames-Member ist eine Reihe von Zeichen folgen für Archiv Elementnamen. Hier wird nur ein Name angezeigt, wenn nicht genügend Platz im Feld Name (16 Bytes) vorhanden ist. Der longnames-Member ist optional. Sie darf nur mit einem Header leer sein oder ohne einen Header vollständig fehlen.

Die Zeichen folgen werden mit Null beendet. Jede Zeichenfolge beginnt unmittelbar nach dem NULL-Byte in der vorherigen Zeichenfolge.

## <a name="import-library-format"></a>Format der Import Bibliothek

- [Header importieren](#import-header)
- [Importtyp](#import-type)

Herkömmliche Import Bibliotheken, d. h. Bibliotheken, die die Exporte aus einem Bild für die Verwendung durch eine andere beschreiben, entsprechen in der Regel dem Layout, das in Abschnitt 7, [Archivdatei Format (Bibliothek)](#archive-library-file-format)beschrieben wird. Der Hauptunterschied besteht darin, dass Member der Import Bibliothek Pseudo Objektdateien anstelle von echten enthalten, wobei jedes Element die Abschnitts Beiträge enthält, die zum Erstellen der Import Tabellen erforderlich sind, die im Abschnitt 6,4, [dem. iData-Abschnitt](#the-idata-section) , den der Linker generiert, beim Erstellen der Export Anwendung generiert wird.

Die Abschnitts Beiträge für einen Import können aus einem kleinen Satz von Informationen abgeleitet werden. Der Linker kann entweder die gesamten ausführlichen Informationen in der Import Bibliothek für jedes Element zum Zeitpunkt der Erstellung der Bibliothek generieren oder nur die kanonischen Informationen in die Bibliothek schreiben, und die Anwendung, die Sie später verwendet, generiert die erforderlichen Daten dynamisch.

In einer Import Bibliothek mit dem langen Format enthält ein einzelnes Mitglied die folgenden Informationen:

<dl> Member-Header archivieren  
Dateiheader  
Abschnitts Header  
Daten, die den einzelnen Abschnitts Headern entsprechen  
COFF-Symboltabelle  
Zeichenfolgen  
  
</dl>

Im Gegensatz dazu wird eine kurze Import Bibliothek wie folgt geschrieben:

<dl> Member-Header archivieren  
Header importieren  
NULL-terminierte Import namens Zeichenfolge  
Mit NULL endender DLL-namens Zeichenfolge  
</dl>

Dies sind ausreichende Informationen, um den gesamten Inhalt des Members zum Zeitpunkt der Verwendung genau zu rekonstruieren.

### <a name="import-header"></a>Header importieren

Der Import Header enthält die folgenden Felder und Offsets:



| Offset         | Size                | Feld                       | BESCHREIBUNG                                                                                                                  |
|----------------|---------------------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------|
| 0 <br/>  | 2 <br/>       | Sig1 <br/>            | Der Image \_ Datei \_ Computer muss \_ unbekannt sein. Weitere Informationen finden Sie unter [Computertypen](#machine-types). <br/>                |
| 2 <br/>  | 2 <br/>       | Sig2 <br/>            | Muss "0xFFFF" lauten. <br/>                                                                                                  |
| 4 <br/>  | 2 <br/>       | Version <br/>         | Die Struktur Version. <br/>                                                                                           |
| 6 <br/>  | 2 <br/>       | Machine <br/>         | Die Zahl, die den Typ des Ziel Computers angibt. Weitere Informationen finden Sie unter [Computertypen](#machine-types).<br/> |
| 8 <br/>  | 4 <br/>       | Time-Date Stempel <br/> | Das Datum und die Uhrzeit, zu der die Datei erstellt wurde. <br/>                                                                     |
| 12 <br/> | 4 <br/>       | Größe der Daten <br/>    | Die Größe der Zeichen folgen, die dem Header folgen. <br/>                                                                  |
| 16 <br/> | 2 <br/>       | Ordinal/Hinweis <br/>    | Entweder die Ordinalzahl oder der Hinweis für den Import, bestimmt durch den Wert im Feld "Name Type". <br/>                   |
| 18 <br/> | 2 Bits <br/>  | type <br/>            | Der Importtyp. Bestimmte Werte und Beschreibungen finden Sie unter [Importtyp](#import-type).<br/>                           |
|                | 3 Bits <br/>  | Namens Typen <br/>       | Der Import Namenstyp. Weitere Informationen finden Sie unter [Import Name Type](#import-name-type). <br/>                           |
|                | 11 Bit <br/> | Reserviert <br/>        | Reserviert, muss 0 sein. <br/>                                                                                             |



 

Auf diese Struktur folgen zwei NULL-terminierte Zeichen folgen, die den Namen des importierten Symbols und die dll beschreiben, von der es stammt.

### <a name="import-type"></a>Importtyp

Die folgenden Werte sind für das typanfeld im Import Header definiert:

| Konstante                  | Wert         | BESCHREIBUNG                                      |
|---------------------------|---------------|--------------------------------------------------|
| \_Code importieren <br/>  | 0 <br/> | Ausführbarer Code. <br/>                     |
| Importieren von \_ Daten <br/>  | 1 <br/> | Daten. <br/>                                |
| Importieren von \_ Konstanten <br/> | 2 <br/> | Wird als Konstante in der DEF-Datei angegeben. <br/> |

Diese Werte werden verwendet, um zu bestimmen, welche Abschnitts Beiträge vom Tool generiert werden müssen, das die Bibliothek verwendet, wenn Sie auf diese Daten zugreifen muss.

### <a name="import-name-type"></a>Typ des Import namens

Der mit NULL endend beendete Import Symbol Name folgt unmittelbar dem zugehörigen Import Header. Die folgenden Werte werden für das Feld "Name Type" im Import Header definiert. Sie geben an, wie der Name verwendet werden soll, um die richtigen Symbole zu generieren, die den Import darstellen:

| Konstante | Wert | BESCHREIBUNG |
| - | - | - |
| \_Ordinalzahl importieren | 0 | Der Import erfolgt durch Ordinalzahl. Dies gibt an, dass der Wert im Feld Ordinal/Hinweis des Import Headers die Ordinalzahl des Imports ist. Wenn diese Konstante nicht angegeben wird, sollte das Ordinal/Hint-Feld immer als Hinweis für den Import interpretiert werden. |
| Import \_ Name | 1 | Der Import Name ist identisch mit dem öffentlichen Symbolnamen. |
| Import \_ Name \_ NoPrefix | 2 | Der Import Name ist der öffentliche Symbol Name, aber das führende "?", "@" oder "optional" wird übersprungen \_ . |
| Import \_ Name \_ undekoriert | 3 | Der Import Name ist der öffentliche Symbol Name, überspringt jedoch die führende?, @ oder optional \_ und kürzt beim ersten @ . |

## <a name="appendix-a-calculating-authenticode-pe-image-hash"></a>Anhang A: Berechnen des Hashwerts für den Authenticode PE-Image

- [Was ist ein Authenticode PE-Image Hash?](#what-is-an-authenticode-pe-image-hash)
- [Was wird in einem Authenticode PE-Image-Hash abgedeckt?](#what-is-covered-in-an-authenticode-pe-image-hash)

Es wird erwartet, dass mehrere Attribut Zertifikate verwendet werden, um die Integrität der Images zu überprüfen. Die häufigste ist jedoch die Authenticode-Signatur. Eine Authenticode-Signatur kann verwendet werden, um zu überprüfen, ob die relevanten Abschnitte einer PE-Bilddatei auf irgendeine Weise aus dem Original Formular der Datei geändert wurden. Zum Ausführen dieser Aufgabe enthalten Authenticode-Signaturen etwas, das als PE-Abbild Hash bezeichnet wird.

### <a name="what-is-an-authenticode-pe-image-hash"></a>Was ist ein Authenticode PE-Image Hash?

Der Authenticode PE-bildhash bzw. der Dateihash ähnelt einer Datei Prüf Summe darin, dass er einen kleinen Wert erzeugt, der sich auf die Integrität einer Datei bezieht. Eine Prüfsumme wird von einem einfachen Algorithmus erstellt und wird hauptsächlich verwendet, um Speicherfehler zu erkennen. Das heißt, es wird verwendet, um zu erkennen, ob ein Speicherblock auf dem Datenträger beschädigt war und die darin gespeicherten Werte beschädigt wurden. Ein Dateihash ähnelt einer Prüfsumme darin, dass auch Datei Beschädigungen erkannt werden. Anders als bei den meisten Prüfsummen Algorithmen ist es jedoch sehr schwierig, eine Datei so zu ändern, dass Sie denselben Dateihash wie das ursprüngliche (unveränderte) Formular hat. Das heißt, eine Prüfsumme ist dafür vorgesehen, einfache Speicher Ausfälle zu erkennen, die zu Beschädigungen führen, aber ein Dateihash kann verwendet werden, um absichtliche und sogar feine Änderungen an einer Datei zu erkennen, z. b. solche, die von Viren, Hacker oder Trojanerprogrammen eingeführt wurden.

In einer Authenticode-Signatur wird der Dateihash mithilfe eines privaten Schlüssels, der nur dem Signatur Geber der Datei bekannt ist, digital signiert. Ein Software Consumer kann die Integrität der Datei überprüfen, indem er den Hashwert der Datei berechnet und ihn mit dem Wert des signierten Hashs vergleicht, der in der digitalen Signatur von Authenticode enthalten ist. Wenn die Dateihashes nicht identisch sind, wurde ein Teil der durch den PE-Abbild Hash behandelten Datei geändert.

### <a name="what-is-covered-in-an-authenticode-pe-image-hash"></a>Was wird in einem Authenticode PE-Image-Hash abgedeckt?

Es ist nicht möglich oder wünschenswert, alle Bild Datei Daten in die Berechnung des PE-Image-Hashs einzubeziehen. Manchmal stellt es einfach unerwünschte Merkmale dar (z. b. können Debuginformationen nicht aus öffentlich freigegebenen Dateien entfernt werden). Manchmal ist es einfach unmöglich. Beispielsweise ist es nicht möglich, alle Informationen in einer Bilddatei in eine Authenticode-Signatur aufzunehmen, die Authenticode-Signatur, die den PE-bildhash enthält, in das PE-Abbild einzufügen und später in der Lage zu sein, einen identischen PE-Abbild Hash zu generieren, indem alle Bild Datei Daten in die Berechnung eingeschlossen werden

#### <a name="process-for-generating-the-authenticode-pe-image-hash"></a>Prozess zum Erstellen des Authenticode PE-Image Hashs

In diesem Abschnitt wird beschrieben, wie ein PE-Abbild Hash berechnet wird und welche Teile des PE-Images geändert werden können, ohne die Authenticode-Signatur ungültig zu machen.

> [!NOTE]
> Der PE-Abbild Hash für eine bestimmte Datei kann in einer separaten Katalog Datei enthalten sein, ohne ein Attribut Zertifikat in die Hash Datei einzubeziehen. Dies ist relevant, da es möglich ist, den PE-Abbild Hash in einer mit Authenticode signierten Katalog Datei für ungültig zu erklären, indem ein PE-Image geändert wird, das keine Authenticode-Signatur enthält.

Alle Daten in Abschnitten des PE-Images, die in der Abschnitts Tabelle angegeben sind, werden vollständig mit Ausnahme der folgenden Ausschluss Bereiche versehen:

- **Das Feld für die Datei Prüf Summe der Windows-spezifischen Felder des optionalen Headers.** Diese Prüfsumme schließt die gesamte Datei ein (einschließlich aller Attribut Zertifikate in der Datei). Nach dem Einfügen der Authenticode-Signatur unterscheidet sich die Prüfsumme in der ganzen Wahrscheinlichkeit vom ursprünglichen Wert.

- **Informationen in Bezug auf Attribut Zertifikate**. Die Bereiche des PE-Images im Zusammenhang mit der Authenticode-Signatur sind nicht in der Berechnung des PE-Abbild Hashs enthalten, da Authenticode-Signaturen einem Image hinzugefügt oder daraus entfernt werden können, ohne dass die Gesamt Integrität des Images beeinträchtigt wird. Dies ist kein Problem, da Benutzer Szenarien vorhanden sind, die von der erneuten Signierung von PE-Abbildern oder dem Hinzufügen eines Zeitstempels abhängig sind. Authenticode schließt die folgenden Informationen aus der Hash Berechnung aus:

  - Das Feld für die Zertifikat Tabelle der optionalen Header Datenverzeichnisse.

  - Die Zertifikat Tabelle und die entsprechenden Zertifikate, auf die durch das direkt oben aufgeführte Feld Zertifikat Tabelle verwiesen wird.

  Um den PE-Abbild Hash zu berechnen, ordnet Authenticode die Abschnitte, die in der Abschnitts Tabelle angegeben sind, nach Adressbereich an und führt dann einen Hashwert für die resultierende Bytefolge durch, wobei die Ausschluss Bereiche übergeben werden.

- **Informationen zum Ende des letzten Abschnitts.** Der Bereich hinter dem letzten Abschnitt (definiert durch den höchsten Offset) ist nicht Hashwert. Dieser Bereich enthält häufig Debuginformationen. Debuginformationen können im Allgemeinen als Empfehlung für Debugger angesehen werden. Dies hat keine Auswirkung auf die tatsächliche Integrität des ausführbaren Programms. Es ist durchaus möglich, Debuginformationen aus einem Image zu entfernen, nachdem ein Produkt übermittelt wurde, und sich nicht auf die Funktionalität des Programms auswirken. Dies wird manchmal als Datenträger speichermeasure durchgeführt. Beachten Sie, dass Debuginformationen, die in den angegebenen Abschnitten des PE-Images enthalten sind, nicht entfernt werden können, ohne die Authenticode-Signatur ungültig zu machen.

Sie können das Tool MakeCert und SignTool verwenden, das im Windows Platform SDK bereitgestellt wird, um mit dem Erstellen und Überprüfen von Authenticode-Signaturen zu experimentieren. Weitere Informationen finden Sie weiter unten in der Referenz.

## <a name="references"></a>References

[Downloads und Tools für Windows (enthält die Windows SDK)](https://developer.microsoft.com/windows/downloads)

[Erstellen, anzeigen und Verwalten von Zertifikaten](/windows/desktop/SecCrypto/creating-viewing-and-managing-certificates)

[Exemplarische Vorgehensweise: Kernel Modus-Code Signierung (. doc)](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/KMCS_Walkthrough.doc)

[SignTool](/windows/desktop/SecCrypto/signtool)

[Windows Authenticode portable ausführbare Signatur Format (. docx)](https://download.microsoft.com/download/9/c/5/9c5b2167-8017-4bae-9fde-d599bac8184a/Authenticode_PE.docx)

[Imagehlp-Funktionen](/windows/desktop/Debug/imagehlp-functions)