---
description: Ein Sockethandle kann optional ein Dateihandle in Windows Sockets 2 sein. Ein Sockethandle eines Winsock-Anbieters kann mit anderen Nicht-Winsock-Funktionen wie ReadFile, WriteFile, ReadFileEx und WriteFileEx verwendet werden.
ms.assetid: 986dd9d8-52be-47aa-92b2-6cd40b83f5de
title: Sockethandles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91a9c9c642c317e9ab4ef897a20b68184df2c04324bcb76c33dea762e78c2846
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740034"
---
# <a name="socket-handles"></a>Sockethandles

Ein Sockethandle kann optional ein Dateihandle in Windows Sockets 2 sein. Ein Sockethandle eines Winsock-Anbieters kann mit anderen Nicht-Winsock-Funktionen wie [**ReadFile,**](/windows/win32/api/fileapi/nf-fileapi-readfile) [**WriteFile,**](/windows/win32/api/fileapi/nf-fileapi-writefile) [**ReadFileEx**](/windows/win32/api/fileapi/nf-fileapi-readfileex)und [**WriteFileEx**](/windows/win32/api/fileapi/nf-fileapi-writefileex)verwendet werden.

Der **XP1 \_ IFS \_ HANDLES-Member** in der Protokollinformationsstruktur für einen Anbieter bestimmt, ob ein Sockethandle eines Anbieters ein INSTALLABLE FILE SYSTEM-Handle (IFS) ist. Sockethandles, die IFS-Handles sind, können ohne Leistungseinbußen mit anderen Nicht-Winsock-Funktionen (z.B.[**ReadFile**](/windows/win32/api/fileapi/nf-fileapi-readfile) und [**WriteFile)**](/windows/win32/api/fileapi/nf-fileapi-writefile)verwendet werden. Alle Nicht-IFS-Sockethandles bei Verwendung mit Nicht-Winsock-Funktionen (z.B.**ReadFile** und **WriteFile)** führen zu Interaktionen zwischen dem Anbieter und dem Dateisystem, bei denen zusätzlicher Verarbeitungsaufwand erforderlich ist, der zu erheblichen Leistungseinbußen führen kann. Wenn Sockethandles mit Nicht-Winsock-Funktionen verwendet werden, werden die vom Basisdateisystem weitergegebenen Fehlercodes nicht immer Winsock-Fehlercodes zugeordnet. Daher wird empfohlen, Sockethandles nur mit Winsock-Funktionen zu verwenden.

Ein Sockethandle sollte nicht mit der [**DuplicateHandle-Funktion**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) verwendet werden. Das Vorhandensein von mehrstufigen Dienstanbietern (LSPs) kann dazu führen, dass dies fehlschlägt, und es gibt keine Möglichkeit für den Zielprozess, das Sockethandle zu importieren.

> [!Note]  
> Mehrstufige Dienstanbieter sind veraltet. Verwenden Sie ab Windows 8 und Windows Server 2012 [Windows Filterplattform](../fwp/windows-filtering-platform-start-page.md).

 

Windows Sockets 2 hat bestimmte Funktionen erweitert, die Daten mithilfe von Handles zwischen Sockets übertragen. Die Funktionen bieten spezifische Vorteile für Sockets zum Übertragen von Daten und umfassen [**WSARecv,**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend)und [**WSADuplicateSocket.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaduplicatesocketa)

 

 
