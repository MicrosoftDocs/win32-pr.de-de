---
title: Ausnahmebehandlung unter WOW64
description: WOW64 verwendet native x64-, ia64- oder ARM64-Ausnahmen als Transport für x86-Ausnahmen. Daher verhalten sich nicht abweichende Ausnahmen in einer 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, wie native 64-Bit-Ausnahmen.
ms.assetid: 2EE1A1F3-A691-4ee6-9587-7FF7C4F9DD98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7d461a809ac35a4742f9bdbbaeb461eb6d7365075d9c4b57334a94f434c1e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561526"
---
# <a name="exception-handling-under-wow64"></a>Ausnahmebehandlung unter WOW64

WOW64 verwendet native x64-, ia64- oder ARM64-Ausnahmen als Transport für x86-Ausnahmen. Daher verhalten sich nicht abweichende Ausnahmen in einer 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, wie native 64-Bit-Ausnahmen.

In einer Anwendung, die auf einer 32-Bit-Version von Windows ausgeführt wird, werden nicht abgefangene Ausnahmen an Ausnahmehandler auf höherer Ebene der Anwendung übergeben, sofern verfügbar. In der gleichen 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, unterdrückt das System möglicherweise nicht abweichende Ausnahmen.

**Windows Vista, Windows Server 2003 und Windows XP:** In derselben 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, ruft das System die Ausnahmefilter auf, unterdrückt jedoch möglicherweise nicht abfangende Ausnahmen, ohne die zugeordneten Handler auf. Dieses Verhalten hat sich ab Windows Vista mit Service Pack 1 (SP1) geändert.

Weitere Informationen zu nicht erfassten Ausnahmen in Window-Prozeduren finden Sie in der [WindowProc-Funktion.](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

 

 