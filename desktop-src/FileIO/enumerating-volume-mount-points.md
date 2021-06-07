---
description: Funktionen zum Aufzählen bereitgestellter Ordner auf einem Volume.
ms.assetid: 052a363f-adfd-4f66-a8b0-5d9d37eedcb0
title: Aufzählen bereitgestellter Ordner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b047e4af74f33d6bc56476734f0f39c41dd14f
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386659"
---
# <a name="enumerating-mounted-folders"></a>Aufzählen bereitgestellter Ordner

Die folgenden Funktionen werden verwendet, um die bereitgestellten Ordner auf einem angegebenen NTFS-Volume aufzuzählen:

-   [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)
-   [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)
-   [**FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)

Diese Funktionen funktionieren ähnlich wie die Funktionen [**FindFirstFile,**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)und [**FindClose.**](/windows/desktop/api/FileAPI/nf-fileapi-findclose)

Um bereitgestellte Ordner auf einem Volume aufzuzählen, ermitteln Sie zunächst, ob das Volume bereitgestellte Ordner unterstützt. Verwenden Sie hierzu den Volumenamen, der von den Funktionen [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) und [**FindNextVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) zurückgegeben wird, um die [**GetVolumeInformation-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) aufzurufen. Die zurückgegebenen Namen enthalten einen nachgestellten umgekehrten Schrägstrich \\ (), der mit der [**GetDriveType-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) und zugehörigen Funktionen kompatibel ist. Weitere Informationen zu den Funktionen, die zum Überprüfen der Volumes auf einem Computer verwendet werden, finden Sie unter [Aufzählen von Volumes.](enumerating-volumes.md) Wenn Sie die **GetVolumeInformation-Funktion** aufrufen und "NTFS" im *lpFileSystemNameBuffer-Parameter* zurückgegeben wird, ist das Volume ein NTFS-Volume. Das NTFS-Dateisystem unterstützt bereitgestellte Ordner.

Wenn es sich bei dem Volume um ein NTFS-Volume handelt, beginnen Sie mit der Suche nach den bereitgestellten Ordnern, indem [**Sie FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)aufrufen. Wenn die Suche erfolgreich ist, verarbeiten Sie die Ergebnisse gemäß den Anforderungen Ihrer Anwendung. Verwenden Sie dann [**FindNextVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa) in einer Schleife, um die bereitgestellten Ordner einzeln zu suchen und zu verarbeiten. Wenn keine bereitgestellten Ordner mehr aufzuzählen sind, schließen Sie das Suchhandle, indem [**Sie FindVolumeMountPointClose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)aufrufen. Beachten Sie, dass die Suche nur die bereitgestellten Ordner findet, die sich auf dem angegebenen Volume befinden.

Sie sollten keine Korrelation zwischen der Reihenfolge der bereitgestellten Ordner, die von diesen Funktionen zurückgegeben werden, und der Reihenfolge der bereitgestellten Ordner annehmen, die von anderen Funktionen oder Tools zurückgegeben werden.

 

 



