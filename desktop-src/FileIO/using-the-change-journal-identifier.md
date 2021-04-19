---
description: Das NTFS-Dateisystem ordnet jedem Änderungs Journal einen 64-Bit-Bezeichner ohne Vorzeichen zu.
ms.assetid: 5ae79460-b69a-4901-a417-1d5358dcba29
title: Verwenden des Änderungs Journal Bezeichners
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692acf98403e45b6bdafd3cd4791a64dd1beb532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347052"
---
# <a name="using-the-change-journal-identifier"></a>Verwenden des Änderungs Journal Bezeichners

Das NTFS-Dateisystem ordnet jedem Änderungs Journal einen 64-Bit-Bezeichner ohne Vorzeichen zu. Das Journal wird mit diesem Bezeichner versehen, wenn er erstellt wird. Das Dateisystem stempelt das Journal mit einem neuen Bezeichner, bei dem die vorhandenen Datensätze der Update Sequenznummer (Update Sequence Number, US) nicht verwendet werden können.

Das NTFS-Dateisystem stempelt z. b. ein Änderungs Journal mit einem neuen Bezeichner neu, wenn ein Volume von einer Version von NTFS zu einer anderen und dann zurück verschoben wird. Ein solcher Verschiebe Vorgang kann in einer Dual-Boot-Umgebung oder bei der Arbeit mit Wechselmedien erfolgen.

Um den Bezeichner des aktuellen Änderungs Journals für ein angegebenes Volume zu erhalten, verwenden Sie den FSCTL-Abfrage-Steuerelement- [**\_ \_ \_ Journal**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) Steuerungs Code. Um dies und alle anderen Änderungs Journal Vorgänge ausführen zu können, müssen Sie über Systemadministrator Rechte verfügen. Das heißt, Sie müssen Mitglied der Gruppe "Administratoren" sein.

Wenn ein Administrator das Änderungs Journal löscht und neu erstellt, z. b. wenn der aktuelle Wert des Werts für die maximal zulässige Verwendung den maximal möglichen Wert erreicht hat, beginnen die Werte der Wert Sequenz erneut von NULL. Wenn das NTFS-Dateisystem ein Journal mit einem neuen Bezeichner stempelt, anstatt das Journal neu zu erstellen, wird die Benutzer-ID nicht auf Null zurückgesetzt, sondern wird von der aktuellen Benutzer-ID fortgesetzt. In beiden Fällen sind alle vorhandenen Anwendungen kleiner als alle zukünftigen Anwendungen.

Wenn Sie Informationen zu einer bestimmten Gruppe von Datensätzen benötigen, verwenden Sie den FSCTL-Abfrage-Steuerelement Code für das [**\_ \_ \_ Journal**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) , um den Änderungs Journal Bezeichner abzurufen. Verwenden Sie dann den [**FSCTL- \_ gelesenen \_ \_ Journal**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) -Steuerungs Code, um die von Interesse gelesenen Journal Daten zu lesen. Das NTFS-Dateisystem gibt nur Datensätze zurück, die für das durch den Bezeichner angegebene Journal gültig sind.

Die Anwendung benötigt sowohl die Datensätze als auch den Bezeichner, um das Journal lesen zu können. Diese Anforderung stellt eine Integritäts Überprüfung für Fälle bereit, in denen Ihre Anwendung die vorhandenen Datensätze in der Datei ignorieren sollte und in früheren Instanzen des Journal für das gleiche Volume Datensätze geschrieben wurden.

Zum Abrufen der Datensätze, für die Sie sich interessieren, müssen Sie mit dem ältesten Datensatz beginnen (d. h. mit der niedrigsten Priorität) und die Überprüfung fortzusetzen, bis Sie den ersten gewünschten Eintrag gefunden haben.

 

 
