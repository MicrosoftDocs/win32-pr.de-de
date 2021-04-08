---
title: Sitzungs-zu-Sitzung-Aktivierung mit einem sitzungsmoniker
description: Die Sitzungs-zu-Sitzung-Aktivierung (auch Sitzungs übergreifende Aktivierung genannt) ermöglicht einem Client Prozess das Starten (aktivieren) eines lokalen Server Prozesses für eine bestimmte Sitzung.
ms.assetid: d405c276-040b-4cde-aeb2-482a25e2867f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2714f3dbe7b23c8b7f04d4271018891960b87f76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729617"
---
# <a name="session-to-session-activation-with-a-session-moniker"></a>Sitzungs-zu-Sitzung-Aktivierung mit einem sitzungsmoniker

Die Sitzungs-zu-Sitzung-Aktivierung (auch Sitzungs übergreifende Aktivierung genannt) ermöglicht einem Client Prozess das Starten (aktivieren) eines lokalen Server Prozesses für eine bestimmte Sitzung. Diese Funktion ist für Anwendungen verfügbar, die so konfiguriert sind, dass Sie im Sicherheitskontext des interaktiven Benutzers ausgeführt werden, der auch als "runas Interactive User"-Objekt Aktivierungs Modus bezeichnet wird. Weitere Informationen zu Sicherheits Kontexten finden Sie [im Sicherheitskontext des Clients](/windows/desktop/SecAuthZ/the-client-security-context).

Verteiltes com (DCOM) ermöglicht die Objekt Aktivierung pro Sitzung mithilfe eines vom System bereitgestellten [sitzungsmonikers](session-monikers.md). Andere vom System bereitgestellte Moniker sind [dateimoniker](../com/file-monikers.md), [elementmoniker](../com/item-monikers.md), generische zusammen [gesetzte Moniker](../com/composite-monikers.md), [Anti-Moniker](../com/anti-monikers.md), [zeigermoniker](../com/pointer-monikers.md)und [URL-Moniker](../com/url-monikers.md).

Damit der sitzungsmoniker verwendet werden kann, muss die DCOM-Anwendung so festgelegt werden, dass Sie als interaktiver Benutzer ausgeführt wird. Dies kann mithilfe des Verwaltungs Tools Komponenten Dienste, Anzeigen der Eigenschaften der DCOM-Anwendung und auswählen **des interaktiven Benutzers** auf der Registerkarte **Identität** festgelegt werden. Weitere Informationen zu den möglichen Sicherheitsrisiken im Zusammenhang mit der Festlegung einer DCOM-Anwendung für die Verwendung als interaktiver Benutzer in einer Remotedesktopdienste Umgebung finden Sie im Abschnitt "Anwendungs Identität (com)" der com-Dokumentation im Platform Software Development Kit (SDK).

Wenn ein anderer Benutzertyp ausgewählt ist, um die Anwendung auszuführen, wird der sitzungsmoniker von der Anwendung ignoriert. Der sitzungsmoniker wird auch von com+-Server Anwendungen ignoriert. Weitere Informationen zu anderen Methoden zum Auswählen des Benutzer Typs zum Ausführen der Anwendung finden Sie in der com-Dokumentation im Platform SDK.

Um einen sitzungsmoniker zu erstellen, müssen Sie die Sitzungs-ID der Remotedesktopdienste Sitzung mit einem klassenmoniker verfassen, der die Klassen-ID des Prozess Servers angibt.

**So erstellen Sie einen sitzungsmoniker**

1.  Legen Sie den anzeigen amen des klassenmonikers mit dem anzeigen amen des sitzungsmonikers mit der folgenden Syntax als Präfix:

    ``` syntax
    "Session:[digits]!clsid:[class id]"
    ```

    , wobei *Ziffern* die Sitzungs-ID der Sitzung darstellt, für die der Server Prozess gestartet wird, und WHERE *Class ID* die Klassen-ID des Servers darstellt. Beachten Sie, dass die Sitzungs-ID eine Basis-10-Nummer ist.

    Bei Computern, auf denen Windows XP oder höher ausgeführt wird, führt die Verwendung der folgenden Syntax dazu, dass com die Aktivierung an die derzeit aktive physische Konsolen Sitzung sendet, je nachdem, wie die Sitzungs-ID lautet:

    ``` syntax
    "Session:Console!clsid:[class id]"
    ```

2.  Nachdem Sie den sitzungsmoniker erstellt haben, können Sie das Ergebnis entweder an die Funktion " [**mkparamesedisplayname**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) " oder an die Funktion " [mkzisedisplaynameex](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) " übergeben.

Sie können einen sitzungsmoniker auf die gleiche Weise verwenden wie einen beliebigen anderen Moniker.

Ein Codebeispiel, in dem veranschaulicht wird, wie Sie einen lokalen Server Prozess für eine bestimmte Sitzung aktivieren, finden [Sie unter using an Session Moniker](using-a-session-moniker.md).

Weitere Informationen zur Objekt Aktivierung, vom System bereitgestellte Moniker und klassenmoniker finden Sie in der com-Dokumentation im Platform SDK.

> [!Note]  
> Prozesse, die Sitzungs übergreifend erstellt werden, weisen eine Obergrenze für die Größe des Umgebungs Blocks auf. Dieser Grenzwert beträgt ca. 4 KB, kann jedoch je nach den anderen zum Erstellen des Prozesses benötigten Informationen (z. b. Dateinamen, Verzeichnisse und Parameter für den neuen Prozess) größer oder kleiner sein.

 

 

 