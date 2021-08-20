---
title: Modul zu Fuß
description: Eine Momentaufnahme, die die Modulliste für einen angegebenen Prozess enthält, enthält Informationen zu jedem Modul, jeder ausführbaren Datei oder dynamic-link library (DLL), die vom angegebenen Prozess verwendet wird.
ms.assetid: 1b539e2f-1326-42aa-af58-ffd7e2833b9b
keywords:
- Dynamic Link-Bibliotheken
- Dynamic Link-Bibliotheken, Auflisten von DLLs
- Auflisten
- Auflisten, DLLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61e72fcdbcae52a78e62465b12845077572b6b4669e1b0744c26d50ddfd2a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126490"
---
# <a name="module-walking"></a>Modul zu Fuß

Eine Momentaufnahme, die die Modulliste für einen angegebenen Prozess enthält, enthält Informationen zu jedem Modul, jeder ausführbaren Datei oder dynamic-link library (DLL), die vom angegebenen Prozess verwendet wird. Sie können Informationen für das erste Modul in der Liste abrufen, indem Sie die [**Module32First-Funktion**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) verwenden. Nachdem Sie das erste Modul in der Liste abgerufen haben, können Sie mithilfe der [**Module32Next-Funktion**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) Informationen zu nachfolgenden Modulen in der Liste abrufen. **Module32First** und **Module32Next** füllen eine [**MODULEENTRY32-Struktur**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) mit Informationen zum Modul aus.

Sie können einen erweiterten Fehlerstatuscode für [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) und [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) mithilfe der [**GetLastError-Funktion**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) abrufen.

> [!Note]  
> Der Modulbezeichner, der im **th32ModuleID-Member** von [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32)angegeben ist, hat nur in 16-Bit-Windows.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Durchlaufen der Modulliste](traversing-the-module-list.md)
</dt> </dl>

 

 