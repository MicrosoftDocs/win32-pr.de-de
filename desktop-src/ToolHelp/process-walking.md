---
title: Prozessablauf
description: Eine Momentaufnahme, die die Prozessliste enthält, enthält Informationen zu jedem derzeit ausgeführten Prozess.
ms.assetid: 4fb55763-2206-48ad-8b1f-ed2c33b6f56b
keywords:
- Auflisten
- Aufzählen,Prozesse
- Prozesse
- Prozesse,Aufzählen von Prozessen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6efa129182da256a6ce62b3754ea422df908248f7b0ecc30d3b690c29ffaf9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419660"
---
# <a name="process-walking"></a>Prozessablauf

Eine Momentaufnahme, die die Prozessliste enthält, enthält Informationen zu jedem derzeit ausgeführten Prozess. Sie können Informationen für den ersten Prozess in der Liste abrufen, indem Sie die [**Process32First-Funktion**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) verwenden. Nach dem Abrufen des ersten Prozesses in der Liste können Sie die Prozessliste für nachfolgende Einträge mithilfe der [**Process32Next-Funktion**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) durchlaufen. **Process32First** und **Process32Next** füllen eine [**PROCESSENTRY32-Struktur**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) mit Informationen zu einem Prozess in der Momentaufnahme aus. Ein Beispiel finden Sie unter [Erstellen einer Momentaufnahme und Anzeigen von Prozessen.](taking-a-snapshot-and-viewing-processes.md)

Sie können einen erweiterten Fehlerstatuscode für [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) und [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) mithilfe der [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) abrufen.

Sie können den Arbeitsspeicher in einem bestimmten Prozess mithilfe der [**Toolhelp32ReadProcessMemory-Funktion**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) (oder der [**VirtualQueryEx-Funktion)**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) in einen Puffer einlesen.

> [!Note]  
> Der Inhalt der **Member th32ProcessID** und **th32ParentProcessID** von [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) sind Prozessbezeichner und können von allen Funktionen verwendet werden, die einen Prozessbezeichner erfordern.

 

 

 