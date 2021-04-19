---
description: Die reglocator-Tabelle enthält die Informationen, die für die Suche nach einer Datei oder einem Verzeichnis mithilfe der Registrierung erforderlich sind, oder um nach einem bestimmten Registrierungs Eintrag zu suchen. Diese Tabelle weist die folgenden Spalten auf.
ms.assetid: dc88b083-cc1d-46d7-9be8-29ebbf3767a0
title: Reglocator-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db5084b8c6fd8d10372759bdba65abbb4dfe7261
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351663"
---
# <a name="reglocator-table"></a>Reglocator-Tabelle

Die reglocator-Tabelle enthält die Informationen, die für die Suche nach einer Datei oder einem Verzeichnis mithilfe der Registrierung erforderlich sind, oder um nach einem bestimmten Registrierungs Eintrag zu suchen. Diese Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Signatur\_ | [Bezeichner](identifier.md) | J   | N        |
| Root        | [Integer](integer.md)       | N   | N        |
| Schlüssel         | [Regfad](regpath.md)       | N   | N        |
| Name        | [Großformatige](formatted.md)   | N   | J        |
| Typ        | [Integer](integer.md)       | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Unter\_
</dt> <dd>

Der Wert im Feld Signatur \_ stellt eine eindeutige Signatur dar, bei der es sich um einen externen Schlüssel in Spalte 1 der [Signatur](signature-table.md) Tabelle handelt. Wenn diese Signatur in der Signatur Tabelle vorhanden ist, wird die Suche nach einer Datei durchsucht. Wenn diese Signatur in der Signatur Tabelle nicht vorhanden ist und der Wert der Type-Spalte **msidblocatortyperawvalue** lautet, ist die Suche nach dem Namen des Registrierungsschlüssels, auf den von der reglocator-Tabelle verwiesen wird. Andernfalls ist die Suche nach einem Verzeichnis, auf das von der reglocator-Tabelle verwiesen wird.

</dd> <dt>

<span id="Root"></span><span id="root"></span><span id="ROOT"></span>Fasst
</dt> <dd>

Der vordefinierte Stamm Schlüssel für den Registrierungs Wert.



| Konstante                          | Hexadezimal | Decimal | Stamm Schlüssel             |
|-----------------------------------|-------------|---------|----------------------|
| **msidbregistryrootclassesroot**  | 0x000       | 0       | HKEY- \_ Klassen Stamm \_  |
| **msidbregistryrootcurrentuser**  | 0x001       | 1       | Aktueller HKEY- \_ \_ Benutzer  |
| **msidbregistryrootlocalmachine** | 0x002       | 2       | lokaler HKEY- \_ \_ Computer |
| **msidbregistryrootusers**        | 0x003       | 3       | HKEY- \_ Benutzer          |



 

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Wichtigen
</dt> <dd>

Der Schlüssel für den Registrierungs Wert.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Der Name des Registrierungswerts. Wenn dieser Wert NULL ist, wird der Wert aus dem unbenannten oder Standardwert des Schlüssels abgerufen, sofern vorhanden.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Sorte
</dt> <dd>

Ein Wert, der bestimmt, ob der Registrierungs Wert ein Dateiname, ein Verzeichnis Speicherort oder ein unformatierten Registrierungs Wert ist.

In der folgenden Tabelle sind gültige Werte aufgeführt. Legen Sie einen der ersten drei Werte und **msidbLocatorType64bit** bei Bedarf fest. Wenn der Eintrag in diesem Feld nicht vorhanden ist, wird Type auf 1 festgelegt.



| Konstante                      | Hexadezimal | Decimal | BESCHREIBUNG                                                                                                                                                        |
|-------------------------------|-------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **msidbloprojekttypedirectory** | 0x000       | 0       | Der Schlüssel Pfad ist ein Verzeichnis.                                                                                                                                           |
| **msidblo-typefilename**  | 0x001       | 1       | Der Schlüssel Pfad ist ein Dateiname.                                                                                                                                           |
| **msidbloserortyperawvalue**  | 0x002       | 2       | Der Schlüssel Pfad ist ein Registrierungs Wert.                                                                                                                                      |
| **msidbLocatorType64bit**     | 0x010       | 16      | Legen Sie dieses Bit fest, damit das Installationsprogramm den 64-Bit-Teil der Registrierung durchsucht. Legen Sie dieses Bit nicht fest, damit das Installationsprogramm den 32-Bit-Teil der Registrierung durchsucht. |



 

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass das Installationsprogramm den Wert der Eigenschaft, die im Feld "Eigenschaft" der [AppSearch](appsearch-table.md) -Tabelle angegeben ist, auf den Registrierungs Wert festlegt, wenn der Wert im type-Feld " **msidblokatortyperawvalue**" ist. Das Installationsprogramm fügt dem Registrierungs Wert ein Präfix hinzu, das den Typ des Registrierungs Werts identifiziert. Weitere Informationen zu Typen von Registrierungs Werten finden Sie unter [Registrierungs Werttypen](../sysinfo/registry-value-types.md).



| Registrierungstyp   | Durch Installer hinzugefügtes Präfix                                                                                                               |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| REG- \_ SZ         | Keine, aber wenn das erste Zeichen des Registrierungs Werts ist \# , schützt das Installationsprogramm das Zeichen, indem es einem anderen vorangestellt wird \# .            |
| DWORD           | " \# ", optional gefolgt von "+" oder "-"                                                                                                  |
| REG \_ Expand \_ SZ | "\#%"                                                                                                                                   |
| REG \_ \_ MultiSZ  | Null. Der Installer legt die-Eigenschaft auf einen Wert fest, der mit Null beginnt und mit einem NULL-Wert endet.                                          |
| REG- \_ Binärdatei     | " \# x" im Fall von reg \_ Binary konvertiert und speichert das Installationsprogramm jede hexadezimal Ziffer (Nibble) als ASCII-Zeichen mit dem Präfix " \# x". |



 

In der Regel werden die Spalten in dieser Tabelle nicht lokalisiert. Wenn ein Autor eine Suche nach Produkten in mehreren Sprachen beschließt, muss für jede Sprache ein separater Eintrag in der Tabelle enthalten sein.

Beachten Sie, dass es nicht möglich ist, die reglocator-Tabelle zu verwenden, um nur auf das vorhanden sein des Schlüssels zu überprüfen. Sie können jedoch nach dem Standardwert eines Schlüssels suchen und dessen Wert abrufen, wenn er nicht leer ist.

Weitere Informationen finden Sie unter [Suchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
[ICE80](ice80.md)  
</dl>

 

 
