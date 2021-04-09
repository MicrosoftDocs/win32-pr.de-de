---
title: Ausnahmebehandlung unter WOW64
description: WOW64 verwendet Native x64-, ia64-oder ARM64-Ausnahmen als Transport für x86-Ausnahmen. Daher verhalten sich nicht abgefangene Ausnahmen in einer 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, wie native 64-Bit-Ausnahmen.
ms.assetid: 2EE1A1F3-A691-4ee6-9587-7FF7C4F9DD98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb57e56b85be4769d452a5772ff7b0024724641
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039470"
---
# <a name="exception-handling-under-wow64"></a>Ausnahmebehandlung unter WOW64

WOW64 verwendet Native x64-, ia64-oder ARM64-Ausnahmen als Transport für x86-Ausnahmen. Daher verhalten sich nicht abgefangene Ausnahmen in einer 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, wie native 64-Bit-Ausnahmen.

In einer Anwendung, die auf einer 32-Bit-Version von Windows ausgeführt wird, werden nicht abgefangene Ausnahmen an die übergeordneten Ausnahmehandler der Anwendung weitergegeben, sofern verfügbar. In derselben 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, unterdrückt das System möglicherweise nicht abgefangene Ausnahmen.

**Windows Vista, Windows Server 2003 und Windows XP:** In derselben 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, ruft das System die Ausnahme Filter auf, unterdrückt jedoch möglicherweise nicht abgefangene Ausnahmen, ohne die zugehörigen Handler aufzurufen. Dieses Verhalten hat sich seit Windows Vista mit Service Pack 1 (SP1) geändert.

Weitere Informationen zu nicht abgefangenen Ausnahmen in Windows-Prozeduren finden Sie unter der [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.

 

 