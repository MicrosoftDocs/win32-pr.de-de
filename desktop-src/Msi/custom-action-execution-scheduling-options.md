---
description: Da eine benutzerdefinierte Aktion sowohl in der Benutzeroberfläche als auch in der Ausführungssequenztabelle geplant und entweder im Dienst- oder Clientprozess ausgeführt werden kann, kann eine benutzerdefinierte Aktion möglicherweise mehrmals ausgeführt werden.
ms.assetid: a3ffeecb-cdd6-43af-a3fe-48e3e843ec8b
title: Optionen für die Planung der Ausführung benutzerdefinierter Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91adbee99684a5a9db0701c2371c8c517547b4d91881518d72fe7c25c0d189be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520100"
---
# <a name="custom-action-execution-scheduling-options"></a>Optionen für die Planung der Ausführung benutzerdefinierter Aktionen

Da eine benutzerdefinierte Aktion sowohl in der Benutzeroberfläche als auch in der Ausführungssequenztabelle geplant und entweder im Dienst- oder Clientprozess ausgeführt werden kann, kann eine benutzerdefinierte Aktion möglicherweise mehrmals ausgeführt werden.

Beachten Sie, dass das Installationsprogramm:

-   Führt Aktionen in einer Sequenztabelle standardmäßig sofort aus.
-   Führt keine Aktion aus, wenn das Feld für den bedingten Ausdruck der Sequenztabelle falseausgewertet wird.
-   Verarbeitet die Sequenztabelle der Benutzeroberfläche im Clientprozess, wenn die Benutzeroberflächenebene des internen Benutzers auf den vollständigen Benutzeroberflächenmodus festgelegt ist (eine Beschreibung der Benutzeroberflächenebenen finden Sie unter [**MsiSetInternalUI).**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
-   Ist ein Dienst, der bei Verwendung von Windows 2000 standardmäßig registriert ist, und in diesem Fall wird die Ausführungssequenztabelle im Installationsprogrammdienst verarbeitet.

Sie können die folgenden Optionsflags verwenden, um mehrere sofortige Ausführungen benutzerdefinierter Aktionen zu steuern. Fügen Sie zum Festlegen einer Option den Wert in dieser Tabelle dem Wert im Feld Typ der [CustomAction-Tabelle hinzu.](customaction-table.md) Keines der folgenden Flags sollte mit benutzerdefinierten Aktionen mit [verzögerter Ausführung verwendet werden.](deferred-execution-custom-actions.md)

<dl> <dt>

<span id="_default_"></span><span id="_DEFAULT_"></span>(Standard)
</dt> <dd>

Hexadezimal: 0x00000000

Decimal: 0

Führen Sie immer aus. Die Aktion kann zweimal ausgeführt werden, wenn sie in beiden Sequenztabellen vorhanden ist.

</dd> <dt>

<span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence** 
</dt> <dd>

Hexadezimal: 0x00000100

Decimal: 256

Führen Sie nicht mehr als einmal aus, wenn sie in beiden Sequenztabellen vorhanden ist. Überspringt die Aktion in der Ausführungssequenz immer, wenn die Benutzeroberflächensequenz ausgeführt wurde. Keine Auswirkung in der Benutzeroberflächensequenz. Die Aktion muss nicht in der Sequenz der Benutzeroberfläche vorhanden sein oder ausgeführt werden, um in der Ausführungssequenz übersprungen zu werden. Von der Dienstregistrierung nicht betroffen.

</dd> <dt>

<span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**
</dt> <dd>

Hexadezimal: 0x00000200

Dezimalzahl: 512

Führen Sie einmal pro Prozess aus, wenn in beiden Sequenztabellen. Überspringt die Aktion in der Ausführungssequenz, wenn die Benutzeroberflächensequenz im gleichen Prozess ausgeführt wurde, z. B. beide im Clientprozess ausgeführt wurden. Wird verwendet, um zu verhindern, dass Aktionen, die den Sitzungszustand ändern, z. B. Eigenschaften- und Datenbankdaten, zweimal ausgeführt werden.

</dd> <dt>

<span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**
</dt> <dd>

Hexadezimal: 0x00000300

Dezimalzahl: 768

Führen Sie nur aus, wenn sie auf dem Client ausgeführt wird, nachdem die Benutzeroberflächensequenz ausgeführt wurde. Die Aktion wird nur ausgeführt, wenn die Ausführungssequenz auf dem Client nach der Benutzeroberflächensequenz ausgeführt wird. Kann verwendet werden, um entweder/oder Logik zur Verfügung zu stellen oder um die benutzeroberflächenbezogene Verarbeitung zu unterdrücken, wenn dies bereits für die Clientsitzung erfolgt ist.

</dd> </dl>

Beachten Sie, dass Sie zwei Einträge in der CustomAction-Tabelle erstellen, um eine benutzerdefinierte Aktion in zwei verschiedenen [Ausführungsmodi ausführen zu können.](customaction-table.md) Um beispielsweise eine benutzerdefinierte Aktion zu haben, die eine C/C++-DLL [(Dynamic Link](custom-action-type-1.md)Library) aufruft ( Benutzerdefinierter Aktionstyp 1 ), wenn der Modus MSIRUNMODE SCHEDULED und \_ MSIRUNMODE ROLLBACK ist, legen Sie zwei Einträge in der CustomAction-Tabelle ab, die dieselbe DLL aufrufen, aber unterschiedliche numerische Typen \_ haben. Fügen Sie Code ein, der [**MsiGetMode aufruft,**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) um zu bestimmen, wann welche benutzerdefinierte Aktion ausgeführt werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu benutzerdefinierten Aktionen](custom-action-reference.md)
</dt> <dt>

[Informationen zu benutzerdefinierten Aktionen](about-custom-actions.md)
</dt> <dt>

[Verwenden benutzerdefinierter Aktionen](using-custom-actions.md)
</dt> </dl>

 

 



