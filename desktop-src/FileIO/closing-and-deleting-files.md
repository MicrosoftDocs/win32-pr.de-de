---
description: Um Betriebssystemressourcen effizient zu verwenden, sollte eine Anwendung Dateien schließen, wenn Sie nicht mehr benötigt werden, indem Sie die CloseHandle-Funktion verwenden. Wenn eine Datei geöffnet ist, wenn eine Anwendung beendet wird, wird Sie vom System automatisch geschlossen.
ms.assetid: 6cf9694a-00c4-4750-8822-c25a1a102fd4
title: Schließen und Löschen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3da31fe7ff38a1bbd1555e2685ceab9ae432574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357019"
---
# <a name="closing-and-deleting-files"></a>Schließen und Löschen von Dateien

Um Betriebssystemressourcen effizient zu verwenden, sollte eine Anwendung Dateien schließen, wenn Sie nicht mehr benötigt werden, indem Sie die [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion verwenden. Wenn eine Datei geöffnet ist, wenn eine Anwendung beendet wird, wird Sie vom System automatisch geschlossen.

Die [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) -Funktion kann verwendet werden, um eine Datei beim Schließen zu löschen. Eine Datei kann erst gelöscht werden, wenn alle Handles geschlossen wurden. Wenn eine Datei nicht gelöscht werden kann, kann Ihr Name nicht wieder verwendet werden. Um einen Dateinamen sofort wiederzuverwenden, benennen Sie die vorhandene Datei um.

Wenn Sie eine geöffnete Datei oder ein Verzeichnis auf einem Remote Computer löschen, die bereits auf dem Remote Computer ohne den Berechtigungs Satz für die Lese Freigabe geöffnet wurde [**, dürfen Sie**](/windows/desktop/api/WinBase/nf-winbase-openfile) nicht die Datei oder das Verzeichnis für den Lösch [**Vorgang aufrufen.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Dies führt zu einer Freigabe Verletzung.

 

 
