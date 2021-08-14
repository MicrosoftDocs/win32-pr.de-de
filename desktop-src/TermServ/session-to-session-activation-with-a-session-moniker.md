---
title: Sitzungs-zu-Sitzung-Aktivierung mit einem Sitzungsmoniker
description: Die Sitzungs-zu-Sitzung-Aktivierung (auch als sitzungsübergreifende Aktivierung bezeichnet) ermöglicht es einem Clientprozess, einen lokalen Serverprozess in einer angegebenen Sitzung zu starten (zu aktivieren).
ms.assetid: d405c276-040b-4cde-aeb2-482a25e2867f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 213627facdd2dee9e4ba7cc698d2be5455424b4394d295448a07aeb52788dd42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988130"
---
# <a name="session-to-session-activation-with-a-session-moniker"></a>Sitzungs-zu-Sitzung-Aktivierung mit einem Sitzungsmoniker

Die Sitzungs-zu-Sitzung-Aktivierung (auch als sitzungsübergreifende Aktivierung bezeichnet) ermöglicht es einem Clientprozess, einen lokalen Serverprozess in einer angegebenen Sitzung zu starten (zu aktivieren). Dieses Feature ist für Anwendungen verfügbar, die für die Ausführung im Sicherheitskontext des interaktiven Benutzers konfiguriert sind, der auch als Objektaktivierungsmodus "Interaktiver RunAs-Benutzer" bezeichnet wird. Weitere Informationen zu Sicherheitskontexten finden Sie unter [Sicherheitskontext des Clients.](/windows/desktop/SecAuthZ/the-client-security-context)

Distributed COM (DCOM) ermöglicht die Objektaktivierung pro Sitzung mithilfe eines vom System bereitgestellten [Sitzungsmonikers.](session-monikers.md) Andere vom System bereitgestellte Moniker umfassen [Dateimoniker,](../com/file-monikers.md) [Elementmoniker,](../com/item-monikers.md)generische zusammengesetzte [Moniker,](../com/composite-monikers.md)Antimoniker, [Zeigermoniker](../com/pointer-monikers.md)und [URL-Moniker.](../com/url-monikers.md) [](../com/anti-monikers.md)

Um den Sitzungsmoniker verwenden zu können, muss die DCOM-Anwendung so festgelegt werden, dass sie als interaktiver Benutzer ausgeführt wird. Sie können dies festlegen, indem Sie das Verwaltungstool für Komponentendienste verwenden, die Eigenschaften der DCOM-Anwendung anzeigen und auf der Registerkarte Identität die Option **Der** interaktive Benutzer **auswählen.** Weitere Informationen zu den möglichen Sicherheitsrisiken im Zusammenhang mit dem Festlegen einer DCOM-Anwendung, die als interaktiver Benutzer in einer Remotedesktopdienste-Umgebung ausgeführt wird, finden Sie im Abschnitt "Anwendungsidentität (COM)" der COM-Dokumentation im Platform Software Development Kit (SDK).

Wenn ein anderer Benutzertyp zum Ausführen der Anwendung ausgewählt ist, wird der Sitzungsmoniker von der Anwendung ignoriert. Der Sitzungsmoniker wird auch von COM+-Serveranwendungen ignoriert. Weitere Informationen zu anderen Methoden zum Auswählen des Benutzertyps zum Ausführen der Anwendung finden Sie in der COM-Dokumentation im Platform SDK.

Um einen Sitzungsmoniker zu erstellen, müssen Sie die Sitzungs-ID der Remotedesktopdienste-Sitzung mit einem Klassenmoniker zusammenstellen, der die Klassen-ID des Prozessservers angibt.

**So erstellen Sie einen Sitzungsmoniker**

1.  Stellen Sie dem Anzeigenamen des Klassenmonikers mithilfe der folgenden Syntax den Anzeigenamen des Sitzungsmonikers voran:

    ``` syntax
    "Session:[digits]!clsid:[class id]"
    ```

    Dabei *stellen Ziffern die Sitzungs-ID* der Sitzung dar, in der der Serverprozess gestartet wird, und wobei die Klassen-ID die Klassen-ID des Servers darstellt.  Beachten Sie, dass die Sitzungs-ID eine Basis-10-Zahl ist.

    Bei Computern, auf denen Windows XP oder höher ausgeführt wird, führt die Verwendung der folgenden Syntax dazu, dass COM die Aktivierung an die derzeit aktive physische Konsolensitzung sendet, unabhängig von der Sitzungs-ID:

    ``` syntax
    "Session:Console!clsid:[class id]"
    ```

2.  Nachdem Sie den Sitzungsmoniker erstellt haben, können Sie das Ergebnis entweder an die [**MkParseDisplayName-Funktion**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) oder die [MkParseDisplayNameEx-Funktion](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) übergeben.

Sie können einen Sitzungsmoniker auf die gleiche Weise wie jeden anderen Moniker verwenden.

Ein Codebeispiel, das veranschaulicht, wie ein lokaler Serverprozess in einer angegebenen Sitzung aktiviert wird, finden Sie unter [Verwenden eines Sitzungsmonikers.](using-a-session-moniker.md)

Weitere Informationen zur Objektaktivierung, vom System bereitgestellten Monikern und Klassenmonikern finden Sie in der COM-Dokumentation im Platform SDK.

> [!Note]  
> Prozesse, die sitzungsübergreifend erstellt werden, haben eine Obergrenze für die Größe des Umgebungsblocks. Dieser Grenzwert beträgt etwa 4 KB, kann jedoch größer oder kleiner sein, je nachdem, welche anderen Informationen zum Erstellen des Prozesses erforderlich sind (z. B. Dateinamen, Verzeichnisse und Parameter für den neuen Prozess).

 

 

 