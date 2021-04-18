---
description: Das verschlüsselte Dateisystem (EFS) bietet kryptografischen Schutz einzelner Dateien auf NTFS-Dateisystemvolumes mithilfe eines Public-Key-Systems.
ms.assetid: 5f20109f-727d-44a9-90a1-0adc19b00d28
title: Dateiverschlüsselung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55c05d8d746e597fe180feffe25f7f553819e822
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352533"
---
# <a name="file-encryption"></a>Dateiverschlüsselung

Das verschlüsselte Datei System (EFS) bietet eine zusätzliche Sicherheitsebene für Dateien und Verzeichnisse. Es bietet kryptografischen Schutz einzelner Dateien auf NTFS-Dateisystem Volumes mithilfe eines Public-Key-Systems.

Normalerweise ist die Zugriffs Steuerung auf Datei-und Verzeichnisobjekte, die vom Windows-Sicherheitsmodell bereitgestellt werden, ausreichend, um nicht autorisierten Zugriff auf vertrauliche Informationen zu schützen. Wenn jedoch ein Laptop mit sensiblen Daten verloren geht oder gestohlen wird, kann der Sicherheitsschutz dieser Daten beeinträchtigt werden. Durch das Verschlüsseln der Dateien wird die Sicherheit erhöht.

Um zu ermitteln, ob ein Dateisystem Dateiverschlüsselung für Dateien und Verzeichnisse unterstützt, müssen Sie die [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) -Funktion aufrufen und das **FS- \_ \_ Dateiverschlüsselungs** -Bitflag untersuchen. Beachten Sie, dass die folgenden Elemente nicht verschlüsselt werden können:

-   Komprimierte Dateien
-   Systemdateien
-   System Verzeichnisse
-   Stamm Verzeichnisse
-   Transaktionen

Sparsesdateien können verschlüsselt werden.

TxF unterstützt die meisten Vorgänge für EFS-Dateien (verschlüsselte Datei System) nicht. Die einzigen Vorgänge, die TxF unterstützt, sind Lesevorgänge wie z. b. " [**leseverschlüsseltedfileraw**](/windows/desktop/api/WinBase/nf-winbase-readencryptedfileraw)".

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                               | BESCHREIBUNG                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Behandeln von verschlüsselten Dateien und Verzeichnissen](handling-encrypted-files-and-directories.md)<br/> | Eine Datei, die als verschlüsselt gekennzeichnet ist, wird vom NTFS-Dateisystem mithilfe des aktuellen Verschlüsselungs Treibers verschlüsselt.<br/>                                                          |
| [Verschlüsselte Dateien und Benutzerschlüssel](encrypted-files-and-user-keys.md)<br/>                       | Listet die Funktionen auf, die zum Erstellen eines neuen Schlüssels, zum Hinzufügen eines Schlüssels zu einer verschlüsselten Datei, zum Abfragen der Schlüssel für eine verschlüsselte Datei und zum Entfernen von Schlüsseln aus einer verschlüsselten Datei verwendet werden.<br/> |
| [Sichern und Wiederherstellen verschlüsselter Dateien](backup-and-restore-of-encrypted-files.md)<br/>       | Die unformatierten Verschlüsselungsfunktionen ermöglichen die Sicherung verschlüsselter Dateien.<br/>                                                                                                |



 

Weitere Informationen zur Verschlüsselung finden Sie unter [Hinzufügen von Benutzern zu einer verschlüsselten Datei](adding-users-to-an-encrypted-file.md).

Weitere Informationen zur Kryptografie finden Sie unter [Cryptography](/windows/desktop/SecCrypto/cryptography-portal).

 

