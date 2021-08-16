---
description: Anwendungen können Minidumpdateien im Benutzermodus erstellen, die eine nützliche Teilmenge der Informationen enthalten, die in einer Absturzabbilddatei enthalten sind.
ms.assetid: c5de86a4-6dab-4408-8093-66117eb4de10
title: Minidumpdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412e719d54f34c9766981667be35990c37ae3511eaecc8836ceac0311a5105e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406090"
---
# <a name="minidump-files"></a>Minidumpdateien

Anwendungen können Minidumpdateien im Benutzermodus erstellen, die eine nützliche Teilmenge der Informationen enthalten, die in einer Absturzabbilddatei enthalten sind. Anwendungen können Minidumpdateien sehr schnell und effizient erstellen. Da Minidumpdateien klein sind, können sie problemlos über das Internet an den technischen Support für die Anwendung gesendet werden.

Eine Minidumpdatei enthält nicht so viele Informationen wie eine vollständige Absturzabbilddatei, aber sie enthält genügend Informationen, um grundlegende Debugvorgänge auszuführen. Zum Lesen einer Minidumpdatei müssen die Binärdateien und Symboldateien für den Debugger verfügbar sein.

Aktuelle Versionen von Microsoft Office und Microsoft Windows Minidumpdateien erstellen, um Fehler auf den Computern von Kunden zu analysieren.

Die folgenden DbgHelp-Funktionen werden mit Minidumpdateien verwendet.

<dl>

[**MiniDumpCallback**](/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine)  
[**MiniDumpReadDumpStream**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpreaddumpstream)  
[**MiniDumpWriteDump**](/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump)  
</dl>

 

 



