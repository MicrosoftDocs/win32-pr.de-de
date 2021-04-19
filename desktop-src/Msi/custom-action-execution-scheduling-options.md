---
description: Da eine benutzerdefinierte Aktion sowohl in der UI-als auch in der Execute Sequence-Tabelle geplant werden kann und entweder im Dienst-oder Client Prozess ausgeführt werden kann, kann eine benutzerdefinierte Aktion möglicherweise mehrmals ausgeführt werden.
ms.assetid: a3ffeecb-cdd6-43af-a3fe-48e3e843ec8b
title: Ausführungszeit Planungsoptionen für benutzerdefinierte Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfa5aee44f3ad357eefc6f9dd9c5ee5ae45797c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348662"
---
# <a name="custom-action-execution-scheduling-options"></a>Ausführungszeit Planungsoptionen für benutzerdefinierte Aktionen

Da eine benutzerdefinierte Aktion sowohl in der UI-als auch in der Execute Sequence-Tabelle geplant werden kann und entweder im Dienst-oder Client Prozess ausgeführt werden kann, kann eine benutzerdefinierte Aktion möglicherweise mehrmals ausgeführt werden.

Beachten Sie, dass das Installationsprogramm:

-   Führt Aktionen in einer Sequenz Tabelle sofort standardmäßig aus.
-   Führt keine Aktion aus, wenn das Feld für den bedingten Ausdruck der Sequenz Tabelle als false ausgewertet wird.
-   Verarbeitet die UI-Sequenz Tabelle im Client Prozess, wenn die Schnittstellen Ebene des internen Benutzers auf den vollständigen Benutzeroberflächen Modus festgelegt ist (Weitere Informationen finden Sie unter [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) für eine Beschreibung der UI-Ebenen).
-   Ist ein Dienst, der bei Verwendung von Windows 2000 standardmäßig registriert ist, und in diesem Fall wird die Execute Sequence-Tabelle im Installerdienst verarbeitet.

Sie können die folgenden Optionsflags verwenden, um die sofortige Ausführung von benutzerdefinierten Aktionen zu steuern. Fügen Sie zum Festlegen einer Option den Wert in dieser Tabelle dem Wert im Feld Typ der [Tabelle CustomAction](customaction-table.md)hinzu. Keines der folgenden Flags sollte mit [benutzerdefinierten Aktionen für die verzögerte Ausführung](deferred-execution-custom-actions.md)verwendet werden.

<dl> <dt>

<span id="_default_"></span><span id="_DEFAULT_"></span>vorgegebene
</dt> <dd>

Hexadezimalwert: 0x00000000

Dezimalwert: 0

Immer ausführen. Die Aktion kann zweimal ausgeführt werden, wenn Sie in beiden Sequenz Tabellen vorhanden ist.

</dd> <dt>

<span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbcustomaktiontypefirstsequence** 
</dt> <dd>

Hexadezimalwert: 0x00000100

Dezimalzahl: 256

Führen Sie nicht mehr als einmal aus, wenn Sie in beiden Sequenz Tabellen vorhanden sind. Überspringt immer die Aktion in der Ausführungssequenz, wenn die UI-Sequenz ausgeführt wurde. Keine Auswirkung in der UI-Sequenz. Die Aktion muss nicht in der UI-Sequenz vorhanden sein oder ausgeführt werden, damit Sie in der Ausführungssequenz übersprungen werden kann. Von der Installations Dienst Registrierung nicht betroffen.

</dd> <dt>

<span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbcustomaktiontypeonceperprocess**
</dt> <dd>

Hexadezimalwert: 0x00000200

Dezimalzahl: 512

Ausführung einmal pro Prozess, wenn in beiden Sequenz Tabellen. Überspringt die Aktion in der Ausführungssequenz, wenn die UI-Sequenz im selben Prozess ausgeführt wurde, z. b. beide werden im Client Prozess ausgeführt. Wird verwendet, um zu verhindern, dass Aktionen, die den Sitzungszustand ändern (z. b. Eigenschaften-und Datenbankdaten), zweimal

</dd> <dt>

<span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbcustomaktiontypeclientrepeat**
</dt> <dd>

Hexadezimalwert: 0x00000300

Dezimalzahl: 768

Nur ausführen, wenn auf dem Client ausgeführt wird, nachdem die UI-Sequenz ausgeführt wurde. Die Aktion wird nur ausgeführt, wenn die Ausführungssequenz auf dem Client nach der Benutzeroberflächen Sequenz ausgeführt wird. Kann verwendet werden, um entweder/oder Logik bereitzustellen oder um die UI-bezogene Verarbeitung zu unterdrücken, falls dies für die Client Sitzung bereits erfolgt ist.

</dd> </dl>

Beachten Sie, dass zum Ausführen einer benutzerdefinierten Aktion in zwei verschiedenen Laufzeiten zwei Einträge in der [Tabelle CustomAction](customaction-table.md) erstellt werden. Um z. b. eine benutzerdefinierte Aktion zu haben, die eine C/C++ Dynamic Link Library (dll) aufruft ( [benutzerdefinierter Aktionstyp 1](custom-action-type-1.md)), wenn der Modus msirunmode \_ geplant und msirunmode \_ Rollback ist, fügen Sie zwei Einträge in die Tabelle CustomAction ein, die dieselbe DLL aufrufen, aber unterschiedliche numerische Typen aufweisen. Fügen Sie Code ein, der [**msigetmode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) aufruft, um zu bestimmen, wann welche benutzerdefinierte Aktion auszuführen ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu benutzerdefinierten Aktionen](custom-action-reference.md)
</dt> <dt>

[Informationen zu benutzerdefinierten Aktionen](about-custom-actions.md)
</dt> <dt>

[Verwenden von benutzerdefinierten Aktionen](using-custom-actions.md)
</dt> </dl>

 

 



