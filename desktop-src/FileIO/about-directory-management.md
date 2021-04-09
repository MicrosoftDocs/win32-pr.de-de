---
description: Ein Verzeichnis, das mindestens ein Verzeichnis enthält, ist das übergeordnete Element des enthaltenen Verzeichnisses oder der Verzeichnisse, und jedes enthaltene Verzeichnis ist ein untergeordnetes Element des übergeordneten Verzeichnisses. Die hierarchische Struktur der Verzeichnisse wird als Verzeichnisstruktur bezeichnet.
ms.assetid: e8a7bf82-0f3c-4ad9-9d10-25c4d69733dc
title: Informationen zur Verzeichnis Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e3a90b6cc99a480f798e632512770c904291a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862659"
---
# <a name="about-directory-management"></a>Informationen zur Verzeichnis Verwaltung

Ein Verzeichnis, das mindestens ein Verzeichnis enthält, ist das über *geordnete* Element des enthaltenen Verzeichnisses oder der Verzeichnisse, und jedes enthaltene Verzeichnis *ist ein unter* geordnetes Element des übergeordneten Verzeichnisses. Die hierarchische Struktur der Verzeichnisse wird als *Verzeichnis* Struktur bezeichnet.

Das NTFS-Dateisystem implementiert die logische Verbindung zwischen einem Verzeichnis und den darin enthaltenen Dateien als *Verzeichniseintrags Tabelle*. Wenn eine Datei in ein Verzeichnis verschoben wird, wird ein Eintrag in der Tabelle für die verschoderte Datei erstellt, und der Name der Datei wird in den Eintrag eingefügt. Wenn eine in einem Verzeichnis enthaltene Datei gelöscht wird, werden der Name und der Eintrag, die der gelöschten Datei entsprechen, ebenfalls aus der Tabelle gelöscht. In einer Verzeichniseintrags Tabelle können mehrere Einträge für eine einzelne Datei vorhanden sein. Wenn ein zusätzlicher Eintrag in der Tabelle für eine Datei erstellt wird, wird dieser Eintrag als *hardlink* zu dieser Datei bezeichnet. Es gibt keine Beschränkung für die Anzahl der festen Links, die für eine einzelne Datei erstellt werden können.

Verzeichnisse können auch Verbindungen und Analyse Punkte enthalten.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                 | BESCHREIBUNG                                                                                            |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Erstellen und Löschen von Verzeichnissen](creating-and-deleting-directories.md)<br/> | Eine Anwendung kann Verzeichnisse Programm gesteuert erstellen und löschen.<br/>                          |
| [Verzeichnis Handles](obtaining-a-handle-to-a-directory.md)<br/>                 | Wenn ein Prozess ein Verzeichnis Objekt erstellt oder öffnet, empfängt es ein Handle für das Objekt.<br/> |
| [Reparse Points](reparse-points.md)<br/>                                       | Beschreibt Analyse Punkte.<br/>                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zur Verzeichnis Verwaltung](directory-management-reference.md)
</dt> </dl>

 

 




