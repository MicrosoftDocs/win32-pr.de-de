---
title: Heaplisten und Heap-Walking
description: Eine Momentaufnahme, die die Heapliste für einen angegebenen Prozess enthält, enthält Identifikationsinformationen für jeden Heap, der dem angegebenen Prozess zugeordnet ist, und ausführliche Informationen zu jedem Heap.
ms.assetid: 631096fd-cb2c-4b19-aa71-d47060e2715c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cc1eaa2093715e3f42fd52cc5191bedf5a0ac137cf93df57daa5ef590e2471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058228"
---
# <a name="heap-lists-and-heap-walking"></a>Heaplisten und Heap-Walking

Eine Momentaufnahme, die die Heapliste für einen angegebenen Prozess enthält, enthält Identifikationsinformationen für jeden Heap, der dem angegebenen Prozess zugeordnet ist, und ausführliche Informationen zu jedem Heap. Sie können einen Bezeichner für den ersten Heap der Heapliste abrufen, indem Sie die [**Heap32ListFirst-Funktion**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) verwenden. Nach dem Abrufen des ersten Heaps in der Liste können Sie die Heapliste für nachfolgende Heaps durchlaufen, die dem Prozess zugeordnet sind, indem Sie die [**Heap32ListNext-Funktion**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) verwenden. **Heap32ListFirst** und **Heap32ListNext** füllen eine [**HEAPLIST32-Struktur**](/windows/win32/api/tlhelp32/ns-tlhelp32-heaplist32) mit dem Prozessbezeichner, dem Heapbezeichner und Flags, die den Heap beschreiben.

Sie können Informationen zum ersten Block eines Heaps mithilfe der [**Heap32First-Funktion**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) abrufen. Nach dem Abrufen des ersten Blocks eines Heaps können Sie Mithilfe der [**Heap32Next-Funktion**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) Informationen zu nachfolgenden Blöcken desselben Heaps abrufen. **Heap32First** und **Heap32Next** füllen eine [**HEAPENTRY32-Struktur**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) mit Informationen für den entsprechenden Block eines Heaps aus.

Sie können einen erweiterten Fehlerstatuscode für [**Heap32ListFirst,**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) [**Heap32ListNext,**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)und [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) abrufen, indem Sie die [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) verwenden.

> [!Note]  
> Der Heapbezeichner, der im **th32HeapID-Member** der [**HEAPENTRY32-Struktur**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) angegeben ist, hat nur für die Toolhilfefunktionen eine Bedeutung. Es ist weder ein Handle noch kann es von anderen Funktionen verwendet werden.

 

 

 