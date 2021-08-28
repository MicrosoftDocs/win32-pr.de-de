---
description: Das verschlüsselte Dateisystem (Encrypted File System, EFS) bietet kryptografischen Schutz einzelner Dateien auf NTFS-Dateisystemvolumes mithilfe eines Systems mit öffentlichem Schlüssel.
ms.assetid: 5f20109f-727d-44a9-90a1-0adc19b00d28
title: Dateiverschlüsselung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61dbbfa82024bea13eab9e672b482ea18bc1051cd6e86b97d2a405351e3b078b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107570"
---
# <a name="file-encryption"></a>Dateiverschlüsselung

Das verschlüsselte Dateisystem (Encrypted File System, EFS) bietet eine zusätzliche Sicherheitsstufe für Dateien und Verzeichnisse. Er bietet kryptografischen Schutz einzelner Dateien auf NTFS-Dateisystemvolumes mithilfe eines Systems mit öffentlichem Schlüssel.

In der Regel ist die Zugriffssteuerung auf Datei- und Verzeichnisobjekte, die vom Windows-Sicherheitsmodell bereitgestellt werden, ausreichend, um nicht autorisierten Zugriff auf vertrauliche Informationen zu schützen. Wenn jedoch ein Laptop mit sensiblen Daten verloren geht oder gestohlen wird, kann der Sicherheitsschutz dieser Daten gefährdet sein. Die Verschlüsselung der Dateien erhöht die Sicherheit.

Um zu bestimmen, ob ein Dateisystem die Dateiverschlüsselung für Dateien und Verzeichnisse unterstützt, rufen Sie die [**GetVolumeInformation-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) auf, und untersuchen Sie das **FS FILE \_ \_ ENCRYPTION-Bitflag.** Beachten Sie, dass die folgenden Elemente nicht verschlüsselt werden können:

-   Komprimierte Dateien
-   Systemdateien
-   Systemverzeichnisse
-   Stammverzeichnisse
-   Transaktionen

Sparsedateien können verschlüsselt werden.

TxF unterstützt die meisten Vorgänge für EFS-Dateien (Encrypted File System) nicht. Die einzigen Vorgänge, die TxF unterstützt, sind Lesevorgänge wie [**ReadEncryptedFileRaw.**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                               | Beschreibung                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Behandeln verschlüsselter Dateien und Verzeichnisse](handling-encrypted-files-and-directories.md)<br/> | Eine als verschlüsselt markierte Datei wird vom NTFS-Dateisystem mithilfe des aktuellen Verschlüsselungstreibers verschlüsselt.<br/>                                                          |
| [Verschlüsselte Dateien und Benutzerschlüssel](encrypted-files-and-user-keys.md)<br/>                       | Listet die Funktionen zum Erstellen eines neuen Schlüssels, Hinzufügen eines Schlüssels zu einer verschlüsselten Datei, Abfragen der Schlüssel für eine verschlüsselte Datei und Entfernen von Schlüsseln aus einer verschlüsselten Datei auf.<br/> |
| [Sichern und Wiederherstellen verschlüsselter Dateien](backup-and-restore-of-encrypted-files.md)<br/>       | Die Unformatieren von Verschlüsselungsfunktionen ermöglichen die Sicherung verschlüsselter Dateien.<br/>                                                                                                |



 

Weitere Informationen zur Verschlüsselung finden Sie unter [Hinzufügen von Benutzern zu einer verschlüsselten Datei.](adding-users-to-an-encrypted-file.md)

Weitere Informationen zur Kryptografie finden Sie unter [Kryptografie.](/windows/desktop/SecCrypto/cryptography-portal)

 

