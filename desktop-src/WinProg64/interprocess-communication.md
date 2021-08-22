---
title: Prozessübergreifende Kommunikation
description: Die folgenden Techniken können für die Kommunikation zwischen 32-Bit- und 64-Bit-Anwendungen verwendet werden.
ms.assetid: 9a60ccfe-4ccf-44d7-9522-42609d95217b
keywords:
- Prozessübergreifende Kommunikation 64-Bit-Windows Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5089440caf6ac537a314e7e920796fadeac5817220ba91f283c297bd0451b705
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734120"
---
# <a name="interprocess-communication-between-32-bit-and-64-bit-applications"></a>Prozessübergreifende Kommunikation zwischen 32-Bit- und 64-Bit-Anwendungen

Die folgenden Techniken können für die Kommunikation zwischen 32-Bit- und 64-Bit-Anwendungen verwendet werden:

-   64-Bit-Versionen von Windows 32-Bit-Handles für die Interoperabilität verwenden. Wenn sie ein Handle zwischen 32-Bit- und 64-Bit-Anwendungen gemeinsam nutzen, sind nur die unteren 32 Bits von Bedeutung. Daher ist es sicher, das Handle zu abschneiden (wenn es von 64-Bit auf 32-Bit übergeben wird) oder das Handle zu signieren (wenn es von 32-Bit auf 64-Bit übergeben wird). Handles, die gemeinsam genutzt werden können, umfassen Handles für Benutzerobjekte wie Fenster **(HWND),** Handles für GDI-Objekte wie Stifte und Pinsel **(HBRUSH** und **HPEN)** und Handles für benannte Objekte wie Mutexe, Semaphore und Dateihandles.
-   Remoteprozeduraufrufe (RPC) können verwendet werden.
-   COM LocalServers kann verwendet werden, wenn sowohl 32-Bit- als auch 64-Bit-Proxy-/Stub-DLLs für alle verwendeten Schnittstellen registriert sind.
-   Freigegebener Speicher kann verwendet werden, wenn zeigerabhängige Typen ordnungsgemäß konvertiert (oder vermieden) werden.
-   Die [**Funktionen CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) und [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) können 32-Bit- und 64-Bit-Prozesse von 32-Bit- oder 64-Bit-Prozessen mit bestimmten Einschränkungen starten.

Eine ausführbare 64-Bit-Datei unter %windir% System32 kann nicht von einem 32-Bit-Prozess gestartet werden, da der Dateisystemumleitung den Pfad \\ umleiten kann. Deaktivieren Sie die Umleitung nicht, um dies zu erreichen. Verwenden Sie stattdessen %windir% \\ Sysnative. Weitere Informationen finden Sie unter [Dateisystem-Redirector](file-system-redirector.md).

 

 