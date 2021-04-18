---
description: Ein Sockethandle kann optional ein Datei Handle in Windows Sockets 2 sein. Ein Sockethandle von einem Winsock-Anbieter kann mit anderen nicht-Winsock-Funktionen wie z. b. "Read File", "Write file", "infofileex" und "Write fileex" verwendet werden.
ms.assetid: 986dd9d8-52be-47aa-92b2-6cd40b83f5de
title: Sockethandles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6ca8ed935819e018a59c52fb43dcf816530c07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347096"
---
# <a name="socket-handles"></a>Sockethandles

Ein Sockethandle kann optional ein Datei Handle in Windows Sockets 2 sein. Ein Sockethandle von einem Winsock-Anbieter kann mit anderen nicht-Winsock-Funktionen wie z. b. "read [**File**](/windows/win32/api/fileapi/nf-fileapi-readfile)", " [**Write File**](/windows/win32/api/fileapi/nf-fileapi-writefile)", " [**infofileex**](/windows/win32/api/fileapi/nf-fileapi-readfileex)" und " [**Write fileex**](/windows/win32/api/fileapi/nf-fileapi-writefileex)" verwendet werden.

Der **XP1 \_ IFS \_ Handles** -Member in der Struktur der Protokollinformationen für einen-Anbieter bestimmt, ob ein Sockethandle eines Anbieters ein-IFS-handle (Installable File System) ist. Sockethandles, die IFS-Handles sind, können ohne Leistungseinbußen mit anderen nicht-Winsock-Funktionen (z. b. "read [**File**](/windows/win32/api/fileapi/nf-fileapi-readfile) " und " [**Write File**](/windows/win32/api/fileapi/nf-fileapi-writefile)") verwendet werden. Alle nicht-IFS-Sockethandles bei Verwendung mit nicht-Winsock-Funktionen (z. b. "read **File** " und " **Write File**") führen zu Interaktionen zwischen dem Anbieter und dem Dateisystem, bei denen zusätzlicher Verarbeitungsaufwand beteiligt ist, was zu einem erheblichen Leistungsverlust führen kann. Wenn Sie Sockethandles mit nicht-Winsock-Funktionen verwenden, werden die Fehlercodes, die vom Basisdatei System weitergegeben werden, nicht immer den Winsock-Fehlercodes zugeordnet. Daher wird empfohlen, Sockethandles nur mit Winsock-Funktionen zu verwenden.

Ein Sockethandle sollte nicht mit der [**duplialisiehandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) -Funktion verwendet werden. Das vorhanden sein von geschichteten Dienstanbietern (LSPs) kann dazu führen, dass dies fehlschlägt und der Ziel Prozess das Sockethandle nicht importieren kann.

> [!Note]  
> Mehrstufige Dienstanbieter sind veraltet. Ab Windows 8 und Windows Server 2012 verwenden Sie die [Windows-Filter Plattform](../fwp/windows-filtering-platform-start-page.md).

 

Windows Sockets 2 hat bestimmte Funktionen erweitert, mit denen Daten zwischen Sockets mithilfe von Handles übertragen werden. Die Funktionen bieten spezielle Vorteile für Sockets zum Übertragen von Daten und einschließen von [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**wsasend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)und [**wsaduplieresocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa).

 

 
