---
description: Wenn Sie die internen Konsistenzauswertungen, die Sie benötigen, nicht unter den vorhandenen benutzerdefinierten ICE-Aktionen finden können, die in der ICE-Referenz aufgeführt sind, müssen Sie Ihr eigenes ICE vorbereiten, um Ihr Paket zu überprüfen.
ms.assetid: d9ff43ee-8e7a-4132-ac2f-232dc24606d8
title: Erstellen eines ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b4b79ab8e17d53ccfb60484c0d307f668c44a7a0e530cf776b10e73a697541c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500764"
---
# <a name="building-an-ice"></a>Erstellen eines ICE

Wenn Sie die [internen Konsistenzauswertungen](internal-consistency-evaluators-ices.md) nicht finden können, die Sie unter den vorhandenen benutzerdefinierten ICE-Aktionen in der [ICE-Referenz](ice-reference.md)benötigen, müssen Sie Ihr eigenes ICE vorbereiten, um Ihr Paket zu überprüfen.

Beim Erstellen von benutzerdefinierten ICE-Aktionen sollten Sie folgende Schritte ausführen:

-   Basieren Sie die ICEs nur auf benutzerdefinierten Aktionen von Typen, die in der angezeigten Tabelle aufgeführt sind.
-   Rufen Sie [**MsiProcessMessage auf,**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) und senden Sie einen INSTALLMESSAGE \_ USER-Nachrichtentyp. Wenn Sie Ihre ICE-Nachrichten erstellen, befolgen Sie das Nachrichtenformat in den [ICE-Nachrichtenrichtlinien.](ice-message-guidelines.md)
-   Schreiben Sie Ihren ICE so, dass api-Fehler erfasst werden, und geben Sie immer ERROR \_ SUCCESS zurück. Dies ist erforderlich, damit nachfolgende benutzerdefinierte Aktionen nach dem Ausfall eines ICE ausgeführt werden können.

Benutzerdefinierte ICE-Aktionen sind auf die folgenden benutzerdefinierten Aktionstypen beschränkt.



| Benutzerdefinierter Aktionstyp                                 | Beschreibung               |
|----------------------------------------------------|---------------------------|
| [Benutzerdefinierter Aktionstyp 1](custom-action-type-1.md)   | DLL im binären Stream      |
| [Benutzerdefinierter Aktionstyp 2](custom-action-type-2.md)   | EXE im binären Stream      |
| [Benutzerdefinierter Aktionstyp 5](custom-action-type-5.md)   | JScript im binären Stream  |
| [Benutzerdefinierter Aktionstyp 6](custom-action-type-6.md)   | VBScript im binären Stream |
| [Benutzerdefinierter Aktionstyp 37](custom-action-type-37.md) | JScript Code als Zeichenfolge    |
| [Benutzerdefinierter Aktionstyp 38](custom-action-type-38.md) | VBScript-Code als Zeichenfolge   |



 

Gehen Sie beim Erstellen einer benutzerdefinierten ICE-Aktion wie folgt vor:

-   Gehen Sie nicht davon aus, dass das Handle für die Engine, die der ICE empfängt, eine Installationsinstanz der Installationsdatenbank ist. Wenn es sich nicht um eine Installationsinstanz handelt, werden bestimmte Eigenschaften nicht definiert, die Quell- und Zielverzeichnisse werden nicht aufgelöst, und die aktuellen Featurezustände werden nicht definiert.
-   Verlassen Sie sich nicht auf die vorherige oder nicht ausgeführte Installationsprogrammaktion, benutzerdefinierte Aktion oder einen anderen ICE. Da ein früherer ICE möglicherweise temporäre Spalten in einer Beliebigen Tabelle erstellt hat, sollten Autoren nach Möglichkeit nach Namen auf Spalten verweisen. ICEs sollten alle temporären Spalten oder Tabellen bereinigen, bevor sie beendet werden.
-   Gehen Sie nicht davon aus, dass Autoren Zugriff auf ein Image des Quellverzeichnisses der Datenbank haben.
-   Gehen Sie nicht davon aus, dass an der Datenbank vorgenommene Änderungen nicht beibehalten werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Beispiel in C++](sample-ice-in-c-.md)
</dt> <dt>

[ICE-Beispiel in VBScript](sample-ice-in-vbscript.md)
</dt> </dl>

 

 



