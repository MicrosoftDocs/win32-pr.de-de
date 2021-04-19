---
description: Die msiflehash-Tabelle wird zum Speichern eines 128-Bit-Hashs einer Quelldatei verwendet, die vom Windows Installer Paket bereitgestellt wird. Der Hash wird in 4 32-Bit-Werte aufgeteilt und in separaten Spalten der Tabelle gespeichert.
ms.assetid: 972a2784-418d-4cb3-b13c-df89b079e94c
title: Msiflehash-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86acb299e5d7f099a8d49affc64810d128e88369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345701"
---
# <a name="msifilehash-table"></a>Msiflehash-Tabelle

Die **msiflehash** -Tabelle wird zum Speichern eines 128-Bit-Hashs einer Quelldatei verwendet, die vom Windows Installer Paket bereitgestellt wird. Der Hash wird in 4 32-Bit-Werte aufgeteilt und in separaten Spalten der Tabelle gespeichert.

Windows Installer können Datei hashvorgänge verwenden, um unnötige Datei Kopien zu erkennen und zu entfernen. Ein in der **msimehasash** -Tabelle gespeicherter Dateihash kann mit einem Hash einer vorhandenen Datei auf dem Computer des Benutzers verglichen werden, der durch Aufrufen von " [**msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)" abgerufen wurde. Die **msiflehash** -Tabelle kann nur mit Dateien ohne Versions Angabe verwendet werden.

Die **msiflehash** -Tabelle weist die folgenden Spalten auf.



| Spalte    | Typ                               | Schlüssel | Nullwerte zulässig |
|-----------|------------------------------------|-----|----------|
| Datei\_    | [Bezeichner](identifier.md)       | J   | N        |
| Optionen   | [Integer](integer.md)             | N   | N        |
| HashPart1 | [Doubleiteger](doubleinteger.md) | N   | N        |
| HashPart2 | [Doubleiteger](doubleinteger.md) | N   | N        |
| HashPart3 | [Doubleiteger](doubleinteger.md) | N   | N        |
| Hashpart4 | [Doubleiteger](doubleinteger.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Fremdschlüssel für [Dateitabelle](file-table.md). 72 char-Zeichenfolge

</dd> <dt>

<span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Optionen
</dt> <dd>

Diese Spalte muss den Wert 0 aufweisen und ist für die zukünftige Verwendung reserviert.

</dd> <dt>

<span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1
</dt> <dd>

Die ersten 32 Bits des Hashwerts. Der in diesem Feld eingegebene Dateihash muss durch Aufrufen von " [**msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) " oder der " [**flehash**](installer-filehash.md)"-Methode abgerufen werden. Verwenden Sie keine anderen Methoden.

</dd> <dt>

<span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2
</dt> <dd>

Zweites 32 Bits Hash. Der in diesem Feld eingegebene Dateihash muss durch Aufrufen von " [**msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) " oder der " [**flehash**](installer-filehash.md)"-Methode abgerufen werden. Verwenden Sie keine anderen Hash Methoden.

</dd> <dt>

<span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3
</dt> <dd>

Dritte 32 Bits Hash. Der in diesem Feld eingegebene Dateihash muss durch Aufrufen von " [**msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) " oder der " [**flehash**](installer-filehash.md)"-Methode abgerufen werden. Verwenden Sie keine anderen Methoden.

</dd> <dt>

<span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4
</dt> <dd>

Fourth 32 Bits Hash. Der in diesem Feld eingegebene Dateihash muss durch Aufrufen von " [**msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) " oder der " [**flehash**](installer-filehash.md)"-Methode abgerufen werden. Verwenden Sie keine anderen Methoden.

</dd> </dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE60](ice60.md)  
[ICE66](ice66.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> <dt>

[Standardmäßige Datei Versionsverwaltung](default-file-versioning.md)
</dt> </dl>

 

 



