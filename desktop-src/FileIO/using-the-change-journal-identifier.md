---
description: Das NTFS-Dateisystem ordnet jedem Änderungsjournal einen 64-Bit-Bezeichner ohne Vorzeichen zu.
ms.assetid: 5ae79460-b69a-4901-a417-1d5358dcba29
title: Verwenden des Änderungsjournalbezeichners
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0483c171b69bcee0faf8df9f325d4ee8ffcb6e904f6aa0cd3c720b83df326e3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015068"
---
# <a name="using-the-change-journal-identifier"></a>Verwenden des Änderungsjournalbezeichners

Das NTFS-Dateisystem ordnet jedem Änderungsjournal einen 64-Bit-Bezeichner ohne Vorzeichen zu. Das Journal wird mit diesem Bezeichner versehen, wenn es erstellt wird. Das Dateisystem stempelt das Journal mit einem neuen Bezeichner, wobei die vorhandenen USN-Datensätze (Update Sequence Number) entweder unbrauchbar sind oder sein können.

Das NTFS-Dateisystem verwendet beispielsweise ein Änderungsjournal mit einem neuen Bezeichner erneut, wenn ein Volume von einer Version von NTFS in eine andere und dann zurück verschoben wird. Eine solche Bewegung kann in einer Dual-Boot-Umgebung oder bei der Arbeit mit Wechselmedien geschehen.

Um den Bezeichner des aktuellen Änderungsjournals auf einem angegebenen Volume zu erhalten, verwenden Sie den [**FSCTL \_ QUERY \_ USN \_ JOURNAL-Steuerungscode.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) Um diese und alle anderen Change Journal-Vorgänge ausführen zu können, müssen Sie über Systemadministratorberechtigungen verfügen. Das heißt, Sie müssen Mitglied der Gruppe Administratoren sein.

Wenn ein Administrator das Änderungsjournal löscht und neu erstellt, z. B. wenn sich der aktuelle USN-Wert dem maximal möglichen USN-Wert nähert, beginnen die USN-Werte erneut bei 0 (null). Wenn das NTFS-Dateisystem ein Journal mit einem neuen Bezeichner stempelt, anstatt das Journal neu zu erstellen, wird die USN nicht auf null zurückgesetzt, sondern von der aktuellen USN fortgesetzt. In beiden Fällen sind alle vorhandenen USNs kleiner als alle zukünftigen USNs.

Wenn Sie Informationen zu einem bestimmten Satz von Datensätzen benötigen, verwenden Sie den [**FSCTL \_ QUERY \_ USN JOURNAL-Steuerungscode, \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) um den Bezeichner des Änderungsjournals zu erhalten. Verwenden Sie dann den [**FSCTL \_ READ \_ USN JOURNAL-Steuerungscode, \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) um die für Sie interessanten Journaldatensätze zu lesen. Das NTFS-Dateisystem gibt nur Datensätze zurück, die für das durch den Bezeichner angegebene Journal gültig sind.

Ihre Anwendung benötigt sowohl die USNs der Datensätze als auch den Bezeichner, um das Journal zu lesen. Diese Anforderung bietet eine Integritätsprüfung für Fälle, in denen Ihre Anwendung die vorhandenen Datensätze in der Datei ignorieren sollte und in denen Datensätze in vorherigen Instanzen des Journals für dasselbe Volume geschrieben wurden.

Um die Datensätze zu erhalten, an denen Sie interessiert sind, müssen Sie am ältesten Datensatz (d. h. mit der niedrigsten USN) beginnen und vorwärts suchen, bis Sie den ersten datensatz von Interesse finden.

 

 
