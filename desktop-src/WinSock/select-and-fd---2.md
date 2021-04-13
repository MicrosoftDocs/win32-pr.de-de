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
# <a name="select-fd_set-and-fd_xxx-macros"></a><span data-ttu-id="c986e-103">Makros für Auswahl, FD \_ -Satz und FD \_ xxx</span><span class="sxs-lookup"><span data-stu-id="c986e-103">Select, FD\_SET, and FD\_XXX Macros</span></span>

<span data-ttu-id="c986e-104">Da Sockets nicht durch die kleine, nicht negative ganze Zahl im Unix-Stil dargestellt werden, wurde die Implementierung der [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -Funktion in Windows Sockets geändert.</span><span class="sxs-lookup"><span data-stu-id="c986e-104">Since sockets are not represented by the UNIX-style, small, non-negative integer, the implementation of the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) function was changed in Windows Sockets.</span></span> <span data-ttu-id="c986e-105">Jeder Satz von Sockets wird immer noch durch die **FD- \_ set** -Struktur dargestellt. statt jedoch als Bitmaske gespeichert zu werden, wird der Satz als ein Array von Sockets implementiert.</span><span class="sxs-lookup"><span data-stu-id="c986e-105">Each set of sockets is still represented by the **FD\_SET** structure, but instead of being stored as a bitmask, the set is implemented as an array of sockets.</span></span> <span data-ttu-id="c986e-106">Um potenzielle Probleme zu vermeiden, müssen Anwendungen die Verwendung der FD xxx- \_ Makros zum Festlegen, initialisieren, löschen und Überprüfen der [**FD- \_ set**](/windows/desktop/api/winsock/nf-winsock-fd_set) -Strukturen einhalten.</span><span class="sxs-lookup"><span data-stu-id="c986e-106">To avoid potential problems, applications must adhere to the use of the FD\_XXX macros to set, initialize, clear, and check the [**FD\_SET**](/windows/desktop/api/winsock/nf-winsock-fd_set) structures.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c986e-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c986e-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c986e-108">Portieren von Socketanwendungen auf Winsock</span><span class="sxs-lookup"><span data-stu-id="c986e-108">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="c986e-109">Überlegungen zur Winsock-Programmierung</span><span class="sxs-lookup"><span data-stu-id="c986e-109">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



