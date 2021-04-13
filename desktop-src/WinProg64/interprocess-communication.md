---
title: Prozessübergreifende Kommunikation
description: Die folgenden Verfahren können für die Kommunikation zwischen 32-Bit-und 64-Bit-Anwendungen verwendet werden.
ms.assetid: 9a60ccfe-4ccf-44d7-9522-42609d95217b
keywords:
- prozessübergreifende Kommunikation 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2398174f011127973dfd0b1773e6eb040cdde898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390703"
---
# <a name="interprocess-communication-between-32-bit-and-64-bit-applications"></a>Prozessübergreifende Kommunikation zwischen 32-Bit-und 64-Bit-Anwendungen

Die folgenden Verfahren können für die Kommunikation zwischen 32-Bit-und 64-Bit-Anwendungen verwendet werden:

-   64-Bit-Versionen von Windows verwenden 32-Bit-Handles für die Interoperabilität. Wenn ein Handle zwischen 32-Bit-und 64-Bit-Anwendungen gemeinsam genutzt wird, sind nur die niedrigeren 32 Bits signifikant, sodass es sicher ist, das Handle (bei der Übergabe von 64 Bit an 32-Bit) oder das Signieren des Handles (bei Übergabe von 32-Bit an 64-Bit) zu kürzen. Handles, die freigegeben werden können, sind Handles für Benutzer Objekte wie Windows (**HWND**), Handles für GDI-Objekte wie z. b. Stifte und Pinsel (**hBrush** und **HPEN**) und Handles für benannte Objekte wie Mutexen, Semaphore und Datei Handles.
-   Remote Prozedur Aufrufe (RPC) können verwendet werden.
-   COM localservers können verwendet werden, wenn sowohl 32-Bit-als auch 64-Bit-Proxy-/Stub-DLLs für alle verwendeten Schnittstellen registriert sind.
-   Shared Memory kann verwendet werden, wenn Zeiger abhängige Typen ordnungsgemäß konvertiert (oder vermieden) werden.
-   Die Funktionen " [**deateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) " und " [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) " können 32-Bit-und 64-Bit-Prozesse von 32-Bit-oder 64-Bit-Prozessen mit bestimmten Einschränkungen starten.

Eine ausführbare 64-Bit-Datei unter% windir% \\ system32 kann nicht von einem 32-Bit-Prozess gestartet werden, da der Dateisystem-Redirector den Pfad umleitet. Deaktivieren Sie die Umleitung nicht, um dies zu erreichen. Verwenden Sie stattdessen% windir% \\ sysnative. Weitere Informationen finden Sie unter [File System Redirector](file-system-redirector.md).

 

 