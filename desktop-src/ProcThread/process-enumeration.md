---
description: Alle Benutzer haben Lesezugriff auf die Liste der Prozesse im System, und es gibt eine Reihe verschiedener Funktionen, mit denen die aktiven Prozesse aufgelistet werden. Die Funktion, die Sie verwenden sollten, hängt von Faktoren wie der Unterstützung gewünschter Plattformen ab.
ms.assetid: 4c73fb10-7ee8-4d8a-9cdb-a2ae59aef5bd
title: Process-Enumeration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911d11a50e898656b56fe89001811b939473c2e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358446"
---
# <a name="process-enumeration"></a>Process-Enumeration

Alle Benutzer haben Lesezugriff auf die Liste der Prozesse im System, und es gibt eine Reihe verschiedener Funktionen, mit denen die aktiven Prozesse aufgelistet werden. Die Funktion, die Sie verwenden sollten, hängt von Faktoren wie der Unterstützung gewünschter Plattformen ab.

Die folgenden Funktionen werden zum Auflisten von Prozessen verwendet.



| Funktion                                                    | BESCHREIBUNG                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | Ruft den Prozess Bezeichner für jedes Prozess Objekt im System ab.            |
| [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | Ruft Informationen zum ersten Prozess ab, der in einer System Momentaufnahme aufgetreten ist.    |
| [**Process32Next**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | Ruft Informationen zum nächsten Prozess ab, der in einer System Momentaufnahme aufgezeichnet wurde.        |
| [**Wtsenum erateprocesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | Ruft Informationen zu den aktiven Prozessen auf dem angegebenen Terminal Server ab. |



 

Die toolhelp-Funktionen [](/windows/win32/api/psapi/nf-psapi-enumprocesses) und enumerationsenumerationsenumerieren alle Prozesse. Zum Auflisten der Prozesse, die in einem bestimmten Benutzerkonto ausgeführt werden, verwenden Sie [**wtsenumerateprocesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) und Filtern die Benutzer-SID. Sie können nach der Sitzungs-ID filtern, um Prozesse auszublenden, die in anderen Terminal Server Sitzungen ausgeführt werden.

Sie können Prozesse unabhängig von der Enumerationsfunktion auch nach Benutzerkonto filtern, indem Sie [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)und [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) mit **tokenuser** aufrufen. Es ist jedoch nicht möglich, einen Prozess zu öffnen, der durch eine Sicherheits Beschreibung geschützt ist, es sei denn, Ihnen wurde der Zugriff gewährt.

 

 
