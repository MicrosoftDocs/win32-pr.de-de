---
description: Funktionen, die zum Auflisten bereitgestellter Ordner auf einem Volume verwendet werden.
ms.assetid: 052a363f-adfd-4f66-a8b0-5d9d37eedcb0
title: Auflisten eingebundenes Ordner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29585100a4b8a94e1b7b78d36b6f0fda228094d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362305"
---
# <a name="enumerating-mounted-folders"></a>Auflisten eingebundenes Ordner

Die folgenden Funktionen werden verwendet, um die bereitgestellten Ordner auf einem angegebenen NTFS-Volume aufzulisten:

-   [**Findfirstvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)
-   [**Findnextvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)
-   [**Findvolumemountpointclose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)

Diese Funktionen funktionieren ähnlich wie die Funktionen " [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)", " [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)" und " [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) ".

Zum Auflisten eingebundenes Ordner auf einem Volume ermitteln Sie zunächst, ob das Volume bereitgestellte Ordner unterstützt. Verwenden Sie hierzu den von den Funktionen " [**findfirstvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) " und " [**findnextvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew) " zurückgegebenen Volumenamen, um die [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) -Funktion aufzurufen. Die zurückgegebenen Namen enthalten einen nachfolgenden umgekehrten Schrägstrich (der \) mit der [**GetDriveType**](/windows/desktop/api/FileAPI/nf-fileapi-getdrivetypea) -Funktion und den zugehörigen Funktionen kompatibel ist). Weitere Informationen zu den Funktionen, die zum Scannen der Volumes auf einem Computer verwendet werden, finden Sie unter Auflisten von [Volumes](enumerating-volumes.md). Wenn Sie die **GetVolumeInformation** -Funktion aufrufen und "NTFS" im *lpfilesystemnamebuffer* -Parameter zurückgegeben wird, ist das Volume ein NTFS-Volume. Das NTFS-Dateisystem unterstützt eingebundene Ordner.

Wenn das Volume ein NTFS-Volume ist, starten Sie eine Suche nach den bereitgestellten Ordnern durch Aufrufen von [**findfirstvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa). Wenn die Suche erfolgreich ist, verarbeiten Sie die Ergebnisse gemäß den Anforderungen Ihrer Anwendung. Verwenden Sie dann [**findnextvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa) in einer Schleife, um die bereitgestellten Ordner einzeln zu suchen und zu verarbeiten. Wenn keine weiteren bereitgestellten Ordner aufgelistet werden müssen, schließen Sie das Such handle, indem Sie [**findvolumemountpointclose**](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose)aufrufen. Beachten Sie, dass bei der Suche nur die eingebundenen Ordner, die sich auf dem angegebenen Volume befinden, gefunden werden.

Sie sollten keine Korrelation zwischen der Reihenfolge der bereitgestellten Ordner, die von diesen Funktionen zurückgegeben werden, und der Reihenfolge der bereitgestellten Ordner annehmen, die von anderen Funktionen oder Tools zurückgegeben werden.

 

 



