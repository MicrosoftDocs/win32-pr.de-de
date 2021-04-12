---
title: Prozess läuft
description: Eine Momentaufnahme, die die Prozessliste enthält, enthält Informationen zu jedem aktuell ausgeführten Prozess.
ms.assetid: 4fb55763-2206-48ad-8b1f-ed2c33b6f56b
keywords:
- Auflisten
- auflisten, Prozesse
- Prozesse
- Prozesse, Auflisten von Prozessen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc95f0de4021ce3c355286376decbdecef2c883
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473549"
---
# <a name="process-walking"></a>Prozess läuft

Eine Momentaufnahme, die die Prozessliste enthält, enthält Informationen zu jedem aktuell ausgeführten Prozess. Sie können Informationen für den ersten Prozess in der Liste abrufen, indem Sie die [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) -Funktion verwenden. Nachdem Sie den ersten Prozess in der Liste abgerufen haben, können Sie die Prozessliste für nachfolgende Einträge durchlaufen, indem Sie die [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) -Funktion verwenden. **Process32First** und **Process32Next** füllen eine [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) -Struktur mit Informationen über einen Prozess in der Momentaufnahme. Ein Beispiel finden [Sie unter Erstellen einer Momentaufnahme und Anzeigen von Prozessen](taking-a-snapshot-and-viewing-processes.md).

Mit der [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion können Sie einen erweiterten Fehlerstatus Code für [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) und [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) abrufen.

Sie können den Arbeitsspeicher in einem bestimmten Prozess mithilfe der [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) -Funktion (oder der [**virtualqueryex**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) -Funktion) in einen Puffer einlesen.

> [!Note]  
> Die Inhalte der **th32ProcessID** -und **th32ParentProcessID** -Member von [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) sind Prozess Bezeichner und können von allen Funktionen verwendet werden, die eine Prozess-ID erfordern.

 

 

 