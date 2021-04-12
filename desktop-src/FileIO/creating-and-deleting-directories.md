---
description: Eine Anwendung kann Verzeichnisse Programm gesteuert erstellen und löschen.
ms.assetid: 52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32
title: Erstellen und Löschen von Verzeichnissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140547594271e13bc78bfa78336f167f228879a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130453"
---
# <a name="creating-and-deleting-directories"></a>Erstellen und Löschen von Verzeichnissen

Eine Anwendung kann Verzeichnisse Programm gesteuert erstellen und löschen.

Wenn Sie ein neues Verzeichnis erstellen möchten, verwenden Sie die Funktion " [**kreatedirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya)", " [**kreatedirectoryex**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)" oder " [**kreatedirectorytransfailed**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) ". Ein Verzeichnis erhält den Namen, der beim Erstellen angegeben wird. Die Konventionen für die Benennung eines Verzeichnisses folgen den Konventionen zum Benennen einer Datei. Eine Beschreibung dieser Konventionen finden Sie unter [Benennen einer Datei](naming-a-file.md).

Um ein vorhandenes Verzeichnis zu löschen, verwenden Sie die Funktion [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) oder [**removedirectorytransktive**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) . Bevor Sie ein Verzeichnis entfernen, müssen Sie sicherstellen, dass das Verzeichnis leer ist und dass Sie über die Berechtigung zum Löschen des Zugriffs für das Verzeichnis verfügen. Um Letzteres durchzuführen, müssen Sie die [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) -Funktion aufrufen.

 

 
