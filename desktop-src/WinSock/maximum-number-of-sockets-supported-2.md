---
description: Die maximale Anzahl von Sockets, die von einem bestimmten Windows Sockets-Dienstanbieter unterstützt werden, ist Implementierungs spezifisch.
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: Maximale Anzahl unterstützter Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207893836a411a2465ffcefe10e838c2e8b59011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357331"
---
# <a name="maximum-number-of-sockets-supported"></a>Maximale Anzahl unterstützter Sockets

Die maximale Anzahl von Sockets, die von einem bestimmten Windows Sockets-Dienstanbieter unterstützt werden, ist Implementierungs spezifisch. Der Microsoft Winsock-Anbieter schränkt die maximale Anzahl von Sockets ein, die nur durch den verfügbaren Speicher auf dem lokalen Computer unterstützt wird. Allerdings können Winsock-Anbieter von Drittanbietern Einschränkungen hinsichtlich der Anzahl der unterstützten Sockets aufweisen. Eine Anwendung sollte keine Annahmen über die Verfügbarkeit einer bestimmten Anzahl von Sockets treffen. Weitere Informationen zu diesem Thema finden Sie unter [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).

## <a name="fd_set-and-select"></a>FD \_ festgelegt und auswählen

\_In der Header Datei " *Winsock2. h* " sind eine Reihe von FD xxx-Makros definiert, die zum Portieren von Anwendungen auf Windows aus der UNIX-Umgebung verwendet werden können. Diese Makros werden zusammen mit den Funktionen [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) und [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) zum Portieren von Anwendungen auf Windows verwendet. Die maximale Anzahl von Sockets, die eine Windows Sockets-Anwendung verwenden kann, wird von der Manifestressource FD \_ SetSize nicht beeinträchtigt. Dieser Wert, der in der Header Datei " *Winsock2. h* " definiert ist, wird zum Erstellen der mit **Select** -Funktion verwendeten [**FD- \_ set**](/windows/desktop/api/winsock/nf-winsock-fd_set) -Strukturen verwendet. Der Standardwert in Winsock2. h ist 64. Wenn eine Anwendung in der Lage ist, mehr als 64 Sockets mithilfe der **Select** -und **wsapoll** -Funktionen zu verwenden, sollte die Implementierung das Manifest- \_ SetSize-Manifest in jeder Quelldatei definieren, bevor die *Winsock2. h* -Header Datei eingeschlossen wird. Eine Möglichkeit, dies zu tun, besteht darin, die Definition innerhalb der Compileroptionen in das Makefile aufzunehmen. Beispielsweise können Sie "-DFD \_ SetSize = 128" als Option zur Compilerbefehlszeile für Microsoft C++ hinzufügen. Es muss betont werden, dass \_ die Definition von FD SetSize als bestimmter Wert keine Auswirkung auf die tatsächliche Anzahl der Sockets ist, die von einem Windows Sockets Service-Anbieter bereitgestellt werden. Dieser Wert wirkt sich nur auf die FD \_ xxx-Makros aus, die von den Funktionen **Select** und **wsapoll** verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**FD- \_ Satz**](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[Portieren von Socketanwendungen auf Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**Auswahl**](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> <dt>

[**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[**Wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 
