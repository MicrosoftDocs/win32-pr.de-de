---
description: Dateizuordnungen definieren, wie die Shell einen Dateityp auf dem System behandelt.
ms.assetid: A1C05857-26F8-4d4a-977B-4782E8AFA317
title: Funktionsweise von Dateizuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd12386ec7e850d160a6377ddff9b807e6dccfe101ad45285bdc9d7f2661a0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032728"
---
# <a name="how-file-associations-work"></a>Funktionsweise von Dateizuordnungen

Dateizuordnungen definieren, wie die Shell einen [Dateityp auf](fa-file-types.md) dem System behandelt.

Dieses Thema ist wie folgt organisiert:

-   [Informationen zu Dateizuordnungen](#about-file-associations)
-   [Wann Sie Dateizuordnungen implementieren oder ändern sollten](#when-you-should-implement-or-modify-file-associations)
-   [Funktionsweise von Dateizuordnungen](#how-file-associations-work)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="about-file-associations"></a>Informationen zu Dateizuordnungen

Dateizuordnungen steuern die folgenden Funktionen:

-   Welche Anwendung wird gestartet, wenn ein Benutzer auf eine Datei doppelklickt.
-   Welches Symbol wird für eine Datei standardmäßig angezeigt?
-   Wie der Dateityp angezeigt wird, wenn er im Windows angezeigt wird.
-   Welche Befehle im Kontextmenü einer Datei angezeigt werden.
-   Andere Benutzeroberflächenfeatures, z. B. QuickInfos, Kachelinformationen und der Detailbereich.

Anwendungsentwickler können Dateizuordnungen verwenden, um zu steuern, wie die Shell benutzerdefinierte Dateitypen behandelt, oder um eine Anwendung vorhandenen Dateitypen zu zuordnen. Wenn beispielsweise eine Anwendung installiert wird, kann die Anwendung überprüfen, ob vorhandene Dateizuordnungen vorhanden sind, und diese Dateizuordnungen entweder erstellen oder überschreiben.

Benutzer können einige Aspekte von Dateizuordnungen steuern, um anzupassen, wie die Shell einen Dateityp behandelt, indem sie entweder die **Open With-Benutzeroberfläche** verwenden oder die Registrierung bearbeiten.

Im Fenster Windows Explorer, das im folgenden Screenshot angezeigt wird, zeigt die Shell verschiedene Symbole für jede Datei an, basierend auf dem Symbol, das dem Dateityp zugeordnet ist. Wenn der Benutzer auf die Datei Sample **Bitmap Image** doppelklickt, startet die Shell Paint und verwendet sie, um die Datei zu öffnen, da Paint auf diesem System .bmp ist. Benutzer können diese Aktionen mithilfe von Dateizuordnungen steuern.

![Abbildung der Funktionsweise von Dateizuordnungen in der Praxis](images/file-assoc/fileassoc-icons.png)

## <a name="when-you-should-implement-or-modify-file-associations"></a>Wann Sie Dateizuordnungen implementieren oder ändern sollten

Anwendungen können Dateien für verschiedene Zwecke verwenden: Einige Dateien werden ausschließlich von der Anwendung verwendet und werden in der Regel nicht von Benutzern aufgerufen, während andere Dateien vom Benutzer erstellt werden und häufig in der Shell geöffnet, gesucht und angezeigt werden.

Sofern Ihr benutzerdefinierter Dateityp nicht ausschließlich von der Anwendung verwendet wird, sollten Sie dateizuordnungen dafür implementieren. Als allgemeine Regel sollten Sie Dateizuordnungen für Ihren benutzerdefinierten Dateityp implementieren, wenn Sie erwarten, dass der Benutzer direkt mit diesen Dateien interagiert. Dazu gehört die Verwendung der Shell zum Durchsuchen und Öffnen der Dateien, das Durchsuchen des Inhalts oder der Eigenschaften der Dateien und das Anzeigen einer Vorschau der Dateien.

Wenn Ihre Anwendung einen vorhandenen Dateityp verarbeitet, ändern Sie die Dateiassoz erst, wenn Sie die Art und Weise ändern möchten, wie die Shell alle Dateien dieses Typs behandelt.

## <a name="how-file-associations-work"></a>Funktionsweise von Dateizuordnungen

Dateien werden in der Shell als Shellelemente verfügbar gemacht. Um Dateizuordnungen zu steuern, können Anwendungsentwickler eine Zuordnung zwischen dem Dateityp und den Handlern registrieren (COM-Objekte, die Funktionen für die Shellelemente des Dateityps bereitstellen). Wenn die Shell die Dateizuordnungen eines Dateityps abfragen muss, erstellt sie ein Array von Registrierungsschlüsseln, die die Zuordnungen für den Dateityp enthalten, und überprüft diese Schlüssel auf die entsprechenden Dateizuordnungen.

## <a name="additional-resources"></a>Weitere Ressourcen

-   Konzeptionelle Hintergrundinformationen zu Dateizuordnungen finden Sie unter [Übersicht über Verben und Dateizuordnungen.](fa-verbs.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsregistrierung](app-registration.md)
</dt> <dt>

[Dateitypen](fa-file-types.md)
</dt> <dt>

[Inhaltsansicht nach Dateityp oder Art](prophand-content-view.md)
</dt> <dt>

[Dateitypverifizierer](file-type-verifier.md)
</dt> <dt>

[Dateityphandler](fa-file-extensions.md)
</dt> <dt>

[Programmgesteuerte Bezeichner](fa-progids.md)
</dt> <dt>

[Wahrgenommene Typen](fa-perceivedtypes.md)
</dt> <dt>

[Zuordnungsarrays](fa-associationarray.md)
</dt> </dl>

 

 



