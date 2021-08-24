---
title: Thread Walking
description: Eine Momentaufnahme, die die Threadliste enthält, enthält Informationen zu jedem Thread jedes derzeit ausgeführten Prozesses.
ms.assetid: 2440b781-652d-4d73-b173-87504e7b49b5
keywords:
- Auflisten
- Aufzählung, Threads
- Threads
- Threads, Aufzählen von Threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4f75f4690be05a7703dab80965fb41035da03cb21f244a4b5a9039a4a61ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513850"
---
# <a name="thread-walking"></a>Thread Walking

Eine Momentaufnahme, die die Threadliste enthält, enthält Informationen zu jedem Thread jedes derzeit ausgeführten Prozesses. Sie können Informationen für den ersten Thread in der Liste abrufen, indem Sie die [**Funktion Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) verwenden. Nach dem Abrufen des ersten Threads in der Liste können Sie Informationen für nachfolgende Threads abrufen, indem Sie die [**Funktion Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) verwenden. **Thread32First** und **Thread32Next** füllen eine [**THREADENTRY32-Struktur**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) mit Informationen zu einzelnen Threads in der Momentaufnahme aus.

Sie können die Threads eines bestimmten Prozesses aufzählen, indem Sie eine Momentaufnahme erstellen, die die Threads enthält, und dann die Threadliste durchlaufen und Informationen zu den Threads behalten, die denselben Prozessbezeichner wie der angegebene Prozess aufweisen.

Sie können einen erweiterten Fehlerstatuscode für [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) und [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) abrufen, indem Sie die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) verwenden.

> [!Note]  
> Der Inhalt des **th32ThreadID-Members** von [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) ist ein Threadbezeichner und kann von allen Funktionen verwendet werden, die einen Threadbezeichner erfordern.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Durchlaufen der Threadliste](traversing-the-thread-list.md)
</dt> </dl>

 

 