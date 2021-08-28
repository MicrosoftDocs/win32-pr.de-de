---
title: Debuggen von WOW64
description: Anwendungen, die unter WOW64 ausgeführt werden, können entweder mit einem x86-gehosteten Debugger oder einem nativen Debugger debuggen werden.
ms.assetid: e0945bdd-998d-4531-869f-21c505cb2135
keywords:
- WOW64 64-Bit Windows Programmieren, Debuggen
- Debuggen von WOW64 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa0f101f382239d146cf668e46efc245753f86ec3c876087f9a4a94bbd356f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121810"
---
# <a name="debugging-wow64"></a>Debuggen von WOW64

Anwendungen, die unter WOW64 ausgeführt werden, können auf zwei Arten gedebuggt werden:

-   Verwenden Sie einen x86-gehosteten Debugger wie NTSD, WinDbg oder Visual Studio. Die 32-Bit-NTSD wird in %systemroot% \\ syswow64 auf Einzelhandelsinstallationen installiert. Beachten Sie, dass x86-Debugger zum Debuggen von x86-Code verwendet werden können, aber nicht zum Disassemblieren oder Festlegen von Haltepunkten innerhalb der WOW64-Thunkebene verwendet werden können, da es sich um nativen 64-Bit-Code handelt.
-   Verwenden Sie einen nativen Debugger wie CDB, NTSD oder WinDbg und die WOW64-Debuggererweiterung Wow64exts.dll. Wenn der systemeigene Debugger unterbrochen wird, während sich der Prozessor im x86-Modus befindet, stellt der Debugger den Prozess als x86-Prozess dar. Wenn sich der Prozessor im einheitlichen Modus befindet, stellt der Debugger den Prozess als nativ dar.

CDB, NTSD und WinDbg sind in den Debugtools für Windows enthalten. Weitere Informationen finden Sie in der Dokumentation [debuggen von Tools für Windows.](/windows-hardware/drivers/debugger/)

Die Wow64exts-Debuggererweiterung wird mit WinDbg installiert. Verwenden Sie den Befehl !load wow64exts, um die Debuggererweiterung zu laden. In der folgenden Tabelle sind die Debuggererweiterungsbefehle !wow64exts aufgeführt.



| Befehl                | Beschreibung                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| !wow64exts.sw          | Wechselt zwischen x86 und dem einheitlichen Modus.                                                                                                    |
| !wow64exts.k *count*   | Dumpt eine kombinierte 32-Bit-/64-Bit-Stapelüberwachung. Wenn *count* angegeben ist, gibt der Befehl die ersten *Zähladressen* in jeder Stapelüberwachung aus.  |
| !wow64exts.info        | Gibt grundlegende Informationen über den PEB des Prozesses, den TEB des aktuellen Threads und die von WOW64 verwendeten TLS-Slots (Thread Local Storage) ab. |
| !wow64exts.r *address* | Gibt den Kontext für die angegebene Adresse aus. Wenn *address* nicht angegeben ist, gibt der Befehl den Kontext für den Prozessor aus.                     |



 

 

 