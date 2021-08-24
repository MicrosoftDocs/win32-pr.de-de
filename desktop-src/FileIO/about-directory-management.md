---
description: Ein Verzeichnis, das ein oder mehrere Verzeichnisse enthält, ist das übergeordnete Verzeichnis des enthaltenen Verzeichnisses, und jedes enthaltene Verzeichnis ist ein untergeordnetes Element des übergeordneten Verzeichnisses. Die hierarchische Struktur von Verzeichnissen wird als Verzeichnisstruktur bezeichnet.
ms.assetid: e8a7bf82-0f3c-4ad9-9d10-25c4d69733dc
title: Informationen zur Verzeichnisverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9cc59e465e1d97b28b1cfdff35c5f288e56b5eb0ee9800273873ffe6476868b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766410"
---
# <a name="about-directory-management"></a>Informationen zur Verzeichnisverwaltung

Ein Verzeichnis, das ein oder  mehrere Verzeichnisse enthält, ist das übergeordnete Verzeichnis  des enthaltenen Verzeichnisses, und jedes enthaltene Verzeichnis ist ein untergeordnetes Element des übergeordneten Verzeichnisses. Die hierarchische Struktur von Verzeichnissen wird als *Verzeichnisstruktur bezeichnet.*

Das NTFS-Dateisystem implementiert die logische Verknüpfung zwischen einem Verzeichnis und den dateien, die es als *Verzeichniseintragstabelle enthält.* Wenn eine Datei in ein Verzeichnis verschoben wird, wird ein Eintrag in der Tabelle für die verschobene Datei erstellt, und der Name der Datei wird im Eintrag platziert. Wenn eine in einem Verzeichnis enthaltene Datei gelöscht wird, werden der Name und der Eintrag, der der gelöschten Datei entspricht, ebenfalls aus der Tabelle gelöscht. In einer Verzeichniseintragstabelle kann mehr als ein Eintrag für eine einzelne Datei vorhanden sein. Wenn in der Tabelle für eine Datei ein zusätzlicher Eintrag erstellt wird, wird dieser Eintrag als harter *Link zu* dieser Datei bezeichnet. Es gibt keine Beschränkung für die Anzahl harter Links, die für eine einzelne Datei erstellt werden können.

Verzeichnisse können auch Verbindungen und Aufbereitungspunkte enthalten.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                 | Beschreibung                                                                                            |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Erstellen und Löschen von Verzeichnissen](creating-and-deleting-directories.md)<br/> | Eine Anwendung kann Verzeichnisse programmgesteuert erstellen und löschen.<br/>                          |
| [Verzeichnishandles](obtaining-a-handle-to-a-directory.md)<br/>                 | Wenn ein Prozess ein Verzeichnisobjekt erstellt oder öffnet, empfängt er ein Handle für das -Objekt.<br/> |
| [Reparse Points](reparse-points.md)<br/>                                       | Beschreibt Aufbereitungspunkte.<br/>                                                                   |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verzeichnisverwaltungsreferenz](directory-management-reference.md)
</dt> </dl>

 

 




