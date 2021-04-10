---
description: Anwendungen können Minidump-Dateien im Benutzermodus entwickeln, die eine nützliche Teilmenge der in einer Absturz Abbild Datei enthaltenen Informationen enthalten.
ms.assetid: c5de86a4-6dab-4408-8093-66117eb4de10
title: Minidumpdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fcd57611cd0b6e5f4f5abdf8bc535f8222feb7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126061"
---
# <a name="minidump-files"></a>Minidumpdateien

Anwendungen können Minidump-Dateien im Benutzermodus entwickeln, die eine nützliche Teilmenge der in einer Absturz Abbild Datei enthaltenen Informationen enthalten. Anwendungen können minidumpdateien sehr schnell und effizient erstellen. Da minidumpdateien klein sind, können Sie problemlos über das Internet an den technischen Support für die Anwendung gesendet werden.

Eine Minidumpdatei enthält nicht so viele Informationen wie eine vollständige Absturz Abbild Datei, Sie enthält jedoch genug Informationen, um grundlegende debuggingvorgänge auszuführen. Um eine Minidump-Datei zu lesen, müssen die Binärdateien und Symbol Dateien für den Debugger verfügbar sein.

Die aktuellen Versionen von Microsoft Office und Microsoft Windows erstellen minidumpdateien zum Zweck der Analyse von Fehlern auf den Computern der Kunden.

Die folgenden dbghelp-Funktionen werden mit Minidump-Dateien verwendet.

<dl>

[**Minidumpcallback**](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[**Minidumpreaddumpstream**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



