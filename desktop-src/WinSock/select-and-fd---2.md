---
description: Da Sockets nicht durch die kleine, nicht negative ganze Zahl im Unix-Stil dargestellt werden, wurde die Implementierung der SELECT-Funktion in Windows Sockets geändert.
ms.assetid: 97c7996c-c541-4673-b26f-d66f3fc0b62e
title: SELECT-, fd_set-und FD_XXX-Makros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9bce15e921bf6566717a30114af73530406e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528628"
---
# <a name="select-fd_set-and-fd_xxx-macros"></a>Makros für Auswahl, FD \_ -Satz und FD \_ xxx

Da Sockets nicht durch die kleine, nicht negative ganze Zahl im Unix-Stil dargestellt werden, wurde die Implementierung der [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -Funktion in Windows Sockets geändert. Jeder Satz von Sockets wird immer noch durch die **FD- \_ set** -Struktur dargestellt. statt jedoch als Bitmaske gespeichert zu werden, wird der Satz als ein Array von Sockets implementiert. Um potenzielle Probleme zu vermeiden, müssen Anwendungen die Verwendung der FD xxx- \_ Makros zum Festlegen, initialisieren, löschen und Überprüfen der [**FD- \_ set**](/windows/desktop/api/winsock/nf-winsock-fd_set) -Strukturen einhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Portieren von Socketanwendungen auf Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Überlegungen zur Winsock-Programmierung](winsock-programming-considerations.md)
</dt> </dl>

 

 



