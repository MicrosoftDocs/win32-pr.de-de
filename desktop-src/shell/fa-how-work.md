---
description: Dateizuordnungen definieren, wie die Shell einen Dateityp im System behandelt.
ms.assetid: A1C05857-26F8-4d4a-977B-4782E8AFA317
title: Funktionsweise von Dateizuordnungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cf307e40bb6165da4a2547fb8dafc1791a11ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215961"
---
# <a name="how-file-associations-work"></a>Funktionsweise von Dateizuordnungen

Dateizuordnungen definieren, wie die Shell einen [Dateityp](fa-file-types.md) im System behandelt.

Dieses Thema ist wie folgt organisiert:

-   [Informationen zu Dateizuordnungen](#about-file-associations)
-   [Beim implementieren oder Ändern von Dateizuordnungen](#when-you-should-implement-or-modify-file-associations)
-   [Funktionsweise von Dateizuordnungen](#how-file-associations-work)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="about-file-associations"></a>Informationen zu Dateizuordnungen

Dateizuordnungen steuern die folgenden Funktionen:

-   Welche Anwendung gestartet wird, wenn ein Benutzer auf eine Datei doppelklickt.
-   Welches Symbol standardmäßig für eine Datei angezeigt wird.
-   Gibt an, wie der Dateityp im Windows-Explorer angezeigt wird.
-   Welche Befehle im Kontextmenü einer Datei angezeigt werden.
-   Andere Funktionen der Benutzeroberfläche, z. b. Quick Infos, Kachel Informationen und der Detailbereich.

Anwendungsentwickler können Dateizuordnungen verwenden, um zu steuern, wie die Shell benutzerdefinierte Dateitypen behandelt, oder um einer Anwendung vorhandene Dateitypen zuzuordnen. Wenn beispielsweise eine Anwendung installiert ist, kann die Anwendung überprüfen, ob vorhandene Dateizuordnungen vorhanden sind, und diese Dateizuordnungen erstellen oder überschreiben.

Benutzer können einige Aspekte von Dateizuordnungen steuern, um anzupassen, wie die Shell einen Dateityp behandelt, indem Sie entweder die Option mit der Benutzeroberfläche **Öffnen** und die Registrierung bearbeiten.

Im Windows-Explorer-Fenster, das im Screenshot unten angezeigt wird, zeigt die Shell basierend auf dem Symbol, das dem Dateityp zugeordnet ist, unterschiedliche Symbole für jede Datei an. Wenn der Benutzer auf das **Bitmapbild der Datei Stichprobe** doppelklickt, wird Paint gestartet und zum Öffnen der Datei verwendet, da Paint auf diesem System mit BMP-Dateien verknüpft ist. Personen können diese Aktionen mithilfe von Dateizuordnungen steuern.

![Darstellung der Funktionsweise von Dateizuordnungen in der Praxis](images/file-assoc/fileassoc-icons.png)

## <a name="when-you-should-implement-or-modify-file-associations"></a>Beim implementieren oder Ändern von Dateizuordnungen

Anwendungen können Dateien für verschiedene Zwecke verwenden: einige Dateien werden ausschließlich von der Anwendung verwendet, und es wird in der Regel nicht von Benutzern darauf zugegriffen, während andere Dateien vom Benutzer erstellt und häufig geöffnet, gesucht und in der Shell angezeigt werden.

Wenn Ihr benutzerdefinierter Dateityp ausschließlich von der Anwendung verwendet wird, sollten Sie Dateizuordnungen für ihn implementieren. Als allgemeine Regel implementieren Sie Dateizuordnungen für Ihren benutzerdefinierten Dateityp, wenn Sie davon ausgehen, dass der Benutzer in irgendeiner Weise direkt mit diesen Dateien interagieren soll. Dazu gehört die Verwendung der Shell zum Durchsuchen und Öffnen der Dateien, zum Durchsuchen des Inhalts oder der Eigenschaften der Dateien und zum Anzeigen der Vorschau der Dateien.

Wenn die Anwendung einen vorhandenen Dateityp verarbeitet, ändern Sie die Datei Zuordnung nur, wenn Sie die Art und Weise ändern möchten, wie die Shell alle Dateien dieses Typs verarbeitet.

## <a name="how-file-associations-work"></a>Funktionsweise von Dateizuordnungen

Dateien werden in der Shell als shellelemente verfügbar gemacht. Um Dateizuordnungen zu steuern, können Anwendungsentwickler eine Zuordnung zwischen dem Dateityp und den Handlern (COM-Objekte, die Funktionalität für die shellelemente des Dateityps bereitstellen) registrieren. Wenn die Shell die Dateizuordnungen eines Dateityps Abfragen muss, erstellt Sie ein Array von Registrierungs Schlüsseln, die die Zuordnungen für den Dateityp enthalten, und überprüft diese Schlüssel auf die zu verwendenden Dateizuordnungen.

## <a name="additional-resources"></a>Weitere Ressourcen

-   Konzeptionelle Hintergrundinformationen zu Dateizuordnungen finden Sie unter [Übersicht über Verben und Dateizuordnungen](fa-verbs.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungs Registrierung](app-registration.md)
</dt> <dt>

[Dateitypen](fa-file-types.md)
</dt> <dt>

[Inhaltsansicht nach Dateityp oder-Art](prophand-content-view.md)
</dt> <dt>

[Dateityp Überprüfung](file-type-verifier.md)
</dt> <dt>

[Dateityp Handler](fa-file-extensions.md)
</dt> <dt>

[Programmgesteuerte Bezeichner](fa-progids.md)
</dt> <dt>

[Wahrgenommene Typen](fa-perceivedtypes.md)
</dt> <dt>

[Zuordnungs Arrays](fa-associationarray.md)
</dt> </dl>

 

 



