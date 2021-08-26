---
description: Alle Benutzer haben Lesezugriff auf die Liste der Prozesse im System, und es gibt eine Reihe verschiedener Funktionen, die die aktiven Prozesse aufzählen. Die Funktion, die Sie verwenden sollten, hängt von Faktoren wie der gewünschten Plattformunterstützung ab.
ms.assetid: 4c73fb10-7ee8-4d8a-9cdb-a2ae59aef5bd
title: Prozessenumeration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05caa13d0f53fc87828669b2e19eba126c62c28f492b2f41d09caf2377321a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081320"
---
# <a name="process-enumeration"></a>Prozessenumeration

Alle Benutzer haben Lesezugriff auf die Liste der Prozesse im System, und es gibt eine Reihe verschiedener Funktionen, die die aktiven Prozesse aufzählen. Die Funktion, die Sie verwenden sollten, hängt von Faktoren wie der gewünschten Plattformunterstützung ab.

Die folgenden Funktionen werden zum Aufzählen von Prozessen verwendet.



| Funktion                                                    | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | Ruft den Prozessbezeichner für jedes Prozessobjekt im System ab.            |
| [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | Ruft Informationen zum ersten Prozess ab, der in einer Systemmomentaufnahme gefunden wurde.    |
| [**Process32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | Ruft Informationen zum nächsten Prozess ab, der in einer Systemmomentaufnahme aufgezeichnet wird.        |
| [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | Ruft Informationen zu den aktiven Prozessen auf dem angegebenen Terminalserver ab. |



 

Die toolhelp-Funktionen [**und EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) enumerieren alle Prozesse. Verwenden Sie zum Auflisten der Prozesse, die in einem bestimmten Benutzerkonto ausgeführt werden, [**WTSEnumerateProcesses,**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) und filtern Sie nach der Benutzer-SID. Sie können nach der Sitzungs-ID filtern, um Prozesse auszublenden, die in anderen Terminalserversitzungen ausgeführt werden.

Sie können Prozesse auch nach Benutzerkonto filtern, unabhängig von der Enumerationsfunktion, indem Sie [**OpenProcess,**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)und [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) mit **TokenUser aufrufen.** Sie können jedoch keinen Prozess öffnen, der durch einen Sicherheitsdeskriptor geschützt ist, es sei denn, Ihnen wurde Zugriff gewährt.

 

 
