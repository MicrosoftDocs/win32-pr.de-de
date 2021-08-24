---
description: Um Betriebssystemressourcen effizient zu verwenden, sollte eine Anwendung Dateien schließen, wenn sie nicht mehr benötigt werden, indem die CloseHandle-Funktion verwendet wird. Wenn eine Datei geöffnet ist, wenn eine Anwendung beendet wird, schließt das System sie automatisch.
ms.assetid: 6cf9694a-00c4-4750-8822-c25a1a102fd4
title: Schließen und Löschen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03c74ad36f2f099b8d2430f52cc2c40b789862c691f56df1ccebcd20e82586ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696300"
---
# <a name="closing-and-deleting-files"></a>Schließen und Löschen von Dateien

Um Betriebssystemressourcen effizient zu verwenden, sollte eine Anwendung Dateien schließen, wenn sie nicht mehr benötigt werden, indem die [**CloseHandle-Funktion**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) verwendet wird. Wenn eine Datei geöffnet ist, wenn eine Anwendung beendet wird, schließt das System sie automatisch.

Die [**DeleteFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) kann verwendet werden, um eine Datei beim Schließen zu löschen. Eine Datei kann erst gelöscht werden, wenn alle Handles für sie geschlossen wurden. Wenn eine Datei nicht gelöscht werden kann, kann ihr Name nicht wiederverwendet werden. Um einen Dateinamen sofort wiederzuverwenden, benennen Sie die vorhandene Datei um.

Wenn Sie eine geöffnete Datei oder ein Verzeichnis auf einem Remotecomputer löschen und diese bereits auf dem Remotecomputer geöffnet wurde, ohne dass die Berechtigung für die Lesefreigabe festgelegt wurde, rufen [**Sie createFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) oder [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) nicht auf, um die Datei oder das Verzeichnis zuerst zum Löschen zu öffnen. Dies führt zu einem Freigabeverstoß.

 

 
