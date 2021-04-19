---
description: Wenn Sie die internen Konsistenzprüfungen, die Sie benötigen, in den in der ICE-Referenz aufgeführten, benutzerdefinierten Ice-Aktionen nicht finden können, müssen Sie Ihr eigenes Eis vorbereiten, um das Paket zu überprüfen.
ms.assetid: d9ff43ee-8e7a-4132-ac2f-232dc24606d8
title: Aufbauen eines Eis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2de8dab0284a612723461d11b420ed1f22b244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349165"
---
# <a name="building-an-ice"></a>Aufbauen eines Eis

Wenn Sie die [internen Konsistenz](internal-consistency-evaluators-ices.md) Prüfungen, die Sie benötigen, in den in der [Ice-Referenz](ice-reference.md)aufgeführten, benutzerdefinierten Ice-Aktionen nicht finden können, müssen Sie Ihr eigenes Eis vorbereiten, um das Paket zu überprüfen.

Wenn Sie benutzerdefinierte Ice-Aktionen erstellen, sollten Sie folgende Schritte ausführen:

-   Basieren Sie auf den ICES nur auf benutzerdefinierte Aktionen der Typen, die in der angezeigten Tabelle aufgeführt sind.
-   [**Msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) anrufen und einen installmessage- \_ Benutzertyp von Message veröffentlichen. Befolgen Sie beim Erstellen von Ice-Nachrichten das Nachrichtenformat in den [Richtlinien](ice-message-guidelines.md)für die Ice-Nachricht.
-   Schreiben Sie Ihr Eis so, dass alle API-Fehler erfasst werden und immer Fehler erfolgreich zurückgegeben werden \_ . Dies ist erforderlich, damit nachfolgende benutzerdefinierte Aktionen nach dem Ausfall eines ICE ausgeführt werden können.

Benutzerdefinierte Ice-Aktionen sind auf die folgenden benutzerdefinierten Aktions Typen beschränkt.



| Benutzerdefinierter Aktionstyp                                 | BESCHREIBUNG               |
|----------------------------------------------------|---------------------------|
| [Benutzerdefinierter Aktionstyp 1](custom-action-type-1.md)   | DLL im binären Stream      |
| [Benutzerdefinierter Aktionstyp 2](custom-action-type-2.md)   | EXE im binären Stream      |
| [Benutzerdefinierter Aktionstyp 5](custom-action-type-5.md)   | JScript im binären Stream  |
| [Benutzerdefinierter Aktionstyp 6](custom-action-type-6.md)   | VBScript im binären Stream |
| [Benutzerdefinierter Aktionstyp 37](custom-action-type-37.md) | JScript-Code als Zeichenfolge    |
| [Benutzerdefinierter Aktionstyp 38](custom-action-type-38.md) | VBScript-Code als Zeichenfolge   |



 

Wenn Sie eine benutzerdefinierte Ice-Aktion erstellen, gehen Sie wie folgt vor:

-   Gehen Sie nicht davon aus, dass das Handle für die Engine, das das Ice empfängt, eine Installations Instanz der Installer-Datenbank ist. Wenn es sich nicht um eine-Installations Instanz handelt, werden bestimmte Eigenschaften nicht definiert, die Quell-und Zielverzeichnisse werden nicht aufgelöst, und die aktuellen Funktions Zustände sind nicht definiert.
-   Verlassen Sie sich weder auf die vorherige Ausführung noch auf die Nichtausführung von Installationsprogramm Aktionen, benutzerdefinierten Aktionen oder anderen Eis. Da ein vorheriger Ice temporäre Spalten in einer beliebigen Tabelle erstellt hat, sollten Autoren nach Möglichkeit nach Möglichkeit auf Spalten verweisen. Der ICES sollte alle temporären Spalten oder Tabellen bereinigen, bevor Sie beendet werden.
-   Gehen Sie nicht davon aus, dass die Autoren auf ein Bild des Quell Verzeichnisses der Datenbank zugreifen können.
-   Gehen Sie nicht davon aus, dass die an der Datenbank vorgenommenen Änderungen nicht beibehalten werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sample Ice in C++](sample-ice-in-c-.md)
</dt> <dt>

[Sample Ice in VBScript](sample-ice-in-vbscript.md)
</dt> </dl>

 

 



