---
description: Die maximale Anzahl von Sockets, die von einem bestimmten Windows Sockets-Dienstanbieter unterstützt werden, ist implementierungsspezifisch.
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: Maximale Anzahl unterstützter Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b567b9733dfb869c901ac499ca8dac66904c84bbe77d750780504acee076385f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569752"
---
# <a name="maximum-number-of-sockets-supported"></a>Maximale Anzahl unterstützter Sockets

Die maximale Anzahl von Sockets, die von einem bestimmten Windows Sockets-Dienstanbieter unterstützt werden, ist implementierungsspezifisch. Der Microsoft Winsock-Anbieter schränkt die maximale Anzahl von Sockets ein, die nur vom verfügbaren Arbeitsspeicher auf dem lokalen Computer unterstützt werden. Winsock-Drittanbieter können jedoch Einschränkungen hinsichtlich der Anzahl unterstützter Sockets aufweisen. Eine Anwendung sollte keine Annahmen über die Verfügbarkeit einer bestimmten Anzahl von Sockets treffen. Weitere Informationen zu diesem Thema finden Sie unter [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).

## <a name="fd_set-and-select"></a>FD \_ SET und Auswählen

Eine Reihe von \_ FD-XXX-Makros wird in der *Winsock2.h-Headerdatei* für die Verwendung beim Portieren von Anwendungen zum Windows aus der UNIX-Umgebung definiert. Diese Makros werden mit den [**Select-**](/windows/desktop/api/Winsock2/nf-winsock2-select) und [**WSAPoll-Funktionen**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) zum Portieren von Anwendungen in Windows verwendet. Die maximale Anzahl von Sockets, die eine Windows Sockets-Anwendung verwenden kann, wird von der Manifestkonstante FD SETSIZE nicht \_ beeinflusst. Dieser in der *Winsock2.h-Headerdatei* definierte Wert wird zum Erstellen der [**FD \_ SET-Strukturen verwendet,**](/windows/desktop/api/winsock/nf-winsock-fd_set) die mit **der Select-Funktion** verwendet werden. Der Standardwert in Winsock2.h ist 64. Wenn eine Anwendung für die Arbeit mit mehr als 64 Sockets mithilfe der **Select-** und **WSAPoll-Funktionen** konzipiert ist, sollte der Implementor das Manifest FD SETSIZE in jeder Quelldatei definieren, \_ bevor die *Winsock2.h-Headerdatei* eingeschlossen wird. Eine Möglichkeit dazu kann darin bestehen, die Definition in die Compileroptionen in das Makefile einzufügen. Beispielsweise können Sie "-DFD \_ SETSIZE=128" als Option zur Compilerbefehlszeile für Microsoft C++ hinzufügen. Es muss hervorgehoben werden, dass das Definieren von FD \_ SETSIZE als bestimmter Wert keine Auswirkungen auf die tatsächliche Anzahl von Sockets hat, die von einem Windows Sockets-Dienstanbieter bereitgestellt werden. Dieser Wert wirkt sich nur auf die FD \_ XXX-Makros aus, die von den **Select-** und **WSAPoll-Funktionen** verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**FD \_ SET**](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[Portieren von Socketanwendungen in Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**Auswählen**](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> <dt>

[**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 
