---
description: Interne Konsistenzauswertungen, auch ICEs genannt, sind benutzerdefinierte Aktionen, die in VBScript, JScript oder als DLL oder EXE geschrieben werden.
ms.assetid: 0789103d-ae34-46be-a9fb-093e066d6d4b
title: Interne Konsistenzauswertungen – ICEs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744915d7f484128095e308f390caae75323775b684b38a0184592dc99a2700f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043380"
---
# <a name="internal-consistency-evaluators---ices"></a>Interne Konsistenzauswertungen – ICEs

Interne Konsistenzauswertungen, auch ICEs genannt, sind benutzerdefinierte Aktionen, die in VBScript, JScript oder als DLL oder EXE geschrieben werden. Wenn diese benutzerdefinierten Aktionen ausgeführt werden, wird die Datenbank auf Einträge in Datenbankdatensätzen überprüft, die bei der individuellen Untersuchung gültig sind, aber im Kontext der gesamten Datenbank zu falschem Verhalten führen können. Beachten Sie, dass sich dies von der Überprüfung für einzelne Datensätze mit [**msiViewModify ab unterscheiden.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)

Die Tabelle Component [kann](component-table.md) beispielsweise mehrere Komponenten auflisten, die alle gültig sind, wenn sie einzeln mit [**MsiViewModify getestet werden.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) **MsiViewModify** würde den Fehler jedoch nicht abfangen, wenn zwei Komponenten dieselbe [GUID wie](guid.md) ihr Komponentencode verwenden. Die benutzerdefinierte [Aktion ICE08](ice08.md) wurde entwickelt, um zu überprüfen, ob die Component-Tabelle keine doppelten Komponentencode-GUIDs enthält.

Benutzerdefinierte ICE-Aktionen geben vier Arten von Nachrichten zurück:

-   [**Fehler**](merge-errors.md) Fehlermeldungen melden die Datenbankerstellung, die ein falsches Verhalten verursacht. Beispielsweise führen doppelte Komponenten-GUIDs dazu, dass das Installationsprogramm Komponenten falsch registriert.
-   **Warnungen** Warnmeldungen melden die Datenbankerstellung, die in bestimmten Fällen ein falsches Verhalten verursacht. Warnungen können auch unerwartete Nebeneffekte der Datenbankerstellung melden. Wenn Sie z. B. den gleichen Eigenschaftennamen in zwei Bedingungen eingeben, die sich nur durch die Groß-/Kleinbuchstaben im Namen unterscheiden. Da beim Installationsprogramm die Kleinschreibung beachtet wird, behandelt das Installationsprogramm diese als unterschiedliche Eigenschaften.
-   **Fehler** Fehlermeldungen melden den Fehler der benutzerdefinierten ICE-Aktion. Fehler werden häufig durch eine Datenbank mit so schwerwiegenden Problemen verursacht, dass das ICE nicht einmal ausgeführt werden kann.
-   **Information** Informationsmeldungen enthalten Informationen aus dem ICE und weisen nicht auf ein Problem mit der Datenbank hin. Häufig handelt es sich um Informationen über das ICE selbst, z. B. eine kurze Beschreibung. Sie können auch Statusinformationen bereitstellen, während der ICE ausgeführt wird.

Weitere Informationen finden Sie unter [Verwenden von internen Konsistenzauswertungen.](using-internal-consistency-evaluators.md)

 

 



