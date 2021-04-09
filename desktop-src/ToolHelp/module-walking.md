---
title: Modul läuft
description: Eine Momentaufnahme, die die Modulliste für einen angegebenen Prozess enthält, enthält Informationen zu den einzelnen Modulen, ausführbaren Dateien oder DLL-Dateien (Dynamic Link Library), die vom angegebenen Prozess verwendet werden.
ms.assetid: 1b539e2f-1326-42aa-af58-ffd7e2833b9b
keywords:
- Dynamic Link Libraries
- Dynamic-Link-Bibliotheken, Enumerieren von DLLs
- Auflisten
- auflisten, DLLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6a844b536d12a15202f47ad9712f3f7ef55df0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101754"
---
# <a name="module-walking"></a>Modul läuft

Eine Momentaufnahme, die die Modulliste für einen angegebenen Prozess enthält, enthält Informationen zu den einzelnen Modulen, ausführbaren Dateien oder DLL-Dateien (Dynamic Link Library), die vom angegebenen Prozess verwendet werden. Mit der [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) -Funktion können Sie Informationen für das erste Modul in der Liste abrufen. Nachdem Sie das erste Modul in der Liste abgerufen haben, können Sie mithilfe der [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) -Funktion Informationen für nachfolgende Module in der Liste abrufen. **Module32First** und **Module32Next** füllen eine [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) -Struktur mit Informationen über das Modul.

Mit der [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) -Funktion können Sie einen erweiterten Fehlerstatus Code für [**Module32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first) und [**Module32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next) abrufen.

> [!Note]  
> Der Modul Bezeichner, der im **th32ModuleID** -Member von [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32)angegeben ist, hat nur eine Bedeutung in 16-Bit-Fenstern.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Durchlaufen der Modulliste](traversing-the-module-list.md)
</dt> </dl>

 

 