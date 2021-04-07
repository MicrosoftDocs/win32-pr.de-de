---
title: Heap Listen und Heap-Walking
description: Eine Momentaufnahme, die die Heap Liste für einen angegebenen Prozess enthält, enthält Identifikationsinformationen für jeden Heap, der dem angegebenen Prozess zugeordnet ist, sowie ausführliche Informationen zu den einzelnen Heaps.
ms.assetid: 631096fd-cb2c-4b19-aa71-d47060e2715c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5a9b8d30e2de1bf5ab37de03fdcb3fde663417
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727969"
---
# <a name="heap-lists-and-heap-walking"></a>Heap Listen und Heap-Walking

Eine Momentaufnahme, die die Heap Liste für einen angegebenen Prozess enthält, enthält Identifikationsinformationen für jeden Heap, der dem angegebenen Prozess zugeordnet ist, sowie ausführliche Informationen zu den einzelnen Heaps. Sie können einen Bezeichner für den ersten Heap der Heap Liste abrufen, indem Sie die [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) -Funktion verwenden. Nachdem Sie den ersten Heap in der Liste abgerufen haben, können Sie die Heap Liste für nachfolgende Heaps durchlaufen, die dem Prozess zugeordnet sind, indem Sie die [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) -Funktion verwenden. **Heap32ListFirst** und **Heap32ListNext** füllen eine [**HEAPLIST32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heaplist32) -Struktur mit der Prozess-ID, der Heap Kennung und den Flags auf, die den Heap beschreiben.

Sie können Informationen zum ersten Heap eines Heaps mithilfe der [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) -Funktion abrufen. Nachdem Sie den ersten Block eines Heaps abgerufen haben, können Sie Informationen zu nachfolgenden Blöcken desselben Heaps mithilfe der [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) -Funktion abrufen. **Heap32First** und **Heap32Next** füllen eine [**HEAPENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) -Struktur mit Informationen für den entsprechenden Block eines Heaps.

Sie können einen erweiterten Fehlerstatus Code für [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst), [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext), [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)und [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) abrufen, indem Sie die [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion verwenden.

> [!Note]  
> Der Heap Bezeichner, der im **th32HeapID** -Member der [**HEAPENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) -Struktur angegeben ist, ist nur für die Tool Hilfefunktionen von Bedeutung. Es ist kein Handle, auch wenn es nicht von anderen Funktionen verwendet werden kann.

 

 

 