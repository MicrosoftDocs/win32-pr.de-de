---
title: Thread-Walking
description: Eine Momentaufnahme, die die Thread Liste enthält, enthält Informationen zu jedem Thread jedes aktuell ausgeführten Prozesses.
ms.assetid: 2440b781-652d-4d73-b173-87504e7b49b5
keywords:
- Auflisten
- auflisten, Threads
- Threads
- Threads, Enumerieren von Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32eff584aedaa3f6124cc358a4ee9d2a94962843
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341735"
---
# <a name="thread-walking"></a>Thread-Walking

Eine Momentaufnahme, die die Thread Liste enthält, enthält Informationen zu jedem Thread jedes aktuell ausgeführten Prozesses. Mit der [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) -Funktion können Sie Informationen für den ersten Thread in der Liste abrufen. Nachdem Sie den ersten Thread in der Liste abgerufen haben, können Sie mithilfe der [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) -Funktion Informationen für nachfolgende Threads abrufen. **Thread32First** und **Thread32Next** füllen eine [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) -Struktur mit Informationen zu einzelnen Threads in der Momentaufnahme.

Sie können die Threads eines bestimmten Prozesses auflisten, indem Sie eine Momentaufnahme erstellen, die die Threads einschließt, und dann durch Durchlaufen der Thread Liste die Informationen zu den Threads, die dieselbe Prozess-ID wie der angegebene Prozess aufweisen, beibehalten.

Mit der [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion können Sie einen erweiterten Fehlerstatus Code für [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) und [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) abrufen.

> [!Note]  
> Der Inhalt des **th32ThreadID** -Members von [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) ist ein Thread Bezeichner, der von allen Funktionen verwendet werden kann, die einen Thread Bezeichner erfordern.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Durchlaufen der Thread Liste](traversing-the-thread-list.md)
</dt> </dl>

 

 