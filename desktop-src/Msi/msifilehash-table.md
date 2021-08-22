---
description: Die MsiFileHash-Tabelle wird verwendet, um einen 128-Bit-Hash einer Quelldatei zu speichern, die vom Windows Installer-Paket bereitgestellt wird. Der Hash wird in vier 32-Bit-Werte aufgeteilt und in separaten Spalten der Tabelle gespeichert.
ms.assetid: 972a2784-418d-4cb3-b13c-df89b079e94c
title: MsiFileHash-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc43c7fd812781057ec0be271ffc370a6b5eb2e3054926e1f969383c0fb390c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944947"
---
# <a name="msifilehash-table"></a>MsiFileHash-Tabelle

Die **MsiFileHash-Tabelle** wird verwendet, um einen 128-Bit-Hash einer Quelldatei zu speichern, die vom Windows Installer-Paket bereitgestellt wird. Der Hash wird in vier 32-Bit-Werte aufgeteilt und in separaten Spalten der Tabelle gespeichert.

Windows Das Installationsprogramm kann Dateihashing als Mittel verwenden, um unnötiges Kopieren von Dateien zu erkennen und zu vermeiden. Ein in der **MsiFileHash-Tabelle** gespeicherter Dateihash kann mit einem Hash einer vorhandenen Datei auf dem Computer des Benutzers verglichen werden, der durch Aufrufen von [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)abgerufen wird. Die **MsiFileHash-Tabelle** kann nur mit Dateien ohneVersion verwendet werden.

Die **MsiFileHash-Tabelle** enthält die folgenden Spalten.



| Spalte    | Typ                               | Key | Nullwerte zulässig |
|-----------|------------------------------------|-----|----------|
| Datei\_    | [Identifier](identifier.md)       | J   | N        |
| Optionen   | [Integer](integer.md)             | N   | N        |
| HashPart1 | [DoubleInteger](doubleinteger.md) | N   | N        |
| HashPart2 | [DoubleInteger](doubleinteger.md) | N   | N        |
| HashPart3 | [DoubleInteger](doubleinteger.md) | N   | N        |
| Hashpart4 | [DoubleInteger](doubleinteger.md) | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Fremdschlüssel für [Dateitabelle](file-table.md). Zeichenfolge mit 72 Zeichen.

</dd> <dt>

<span id="Options"></span><span id="options"></span><span id="OPTIONS"></span>Optionen
</dt> <dd>

Diese Spalte muss 0 sein und ist für die zukünftige Verwendung reserviert.

</dd> <dt>

<span id="HashPart1"></span><span id="hashpart1"></span><span id="HASHPART1"></span>HashPart1
</dt> <dd>

Erste 32 Bits hash. Der in dieses Feld eingegebene Dateihash muss durch Aufrufen von [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) oder der [**FileHash-Methode**](installer-filehash.md)abgerufen werden. Verwenden Sie keine anderen Methoden.

</dd> <dt>

<span id="HashPart2"></span><span id="hashpart2"></span><span id="HASHPART2"></span>HashPart2
</dt> <dd>

Zweite 32 Bits Hash. Der in dieses Feld eingegebene Dateihash muss durch Aufrufen von [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) oder der [**FileHash-Methode**](installer-filehash.md)abgerufen werden. Verwenden Sie keine anderen Hashmethoden.

</dd> <dt>

<span id="HashPart3"></span><span id="hashpart3"></span><span id="HASHPART3"></span>HashPart3
</dt> <dd>

Dritte 32 Bits Hash. Der in dieses Feld eingegebene Dateihash muss durch Aufrufen von [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) oder der [**FileHash-Methode**](installer-filehash.md)abgerufen werden. Verwenden Sie keine anderen Methoden.

</dd> <dt>

<span id="HashPart4"></span><span id="hashpart4"></span><span id="HASHPART4"></span>HashPart4
</dt> <dd>

Vierte 32 Bits Hash. Der in dieses Feld eingegebene Dateihash muss durch Aufrufen von [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) oder der [**FileHash-Methode**](installer-filehash.md)abgerufen werden. Verwenden Sie keine anderen Methoden.

</dd> </dl>

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE60](ice60.md)  
[ICE66](ice66.md)  
</dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha)
</dt> <dt>

[Standarddateiversionsierung](default-file-versioning.md)
</dt> </dl>

 

 



