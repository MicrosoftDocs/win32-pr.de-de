---
title: Debuggen WOW64
description: Anwendungen, die unter WOW64 ausgeführt werden, können entweder mit einem x86-gehosteten Debugger oder einem nativen Debugger Debuggen.
ms.assetid: e0945bdd-998d-4531-869f-21c505cb2135
keywords:
- WOW64 64-Bit-Windows-Programmierung, Debuggen
- Debuggen WOW64 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc7590b0b4f44f9e1a48a204723fb0652b9c2e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390877"
---
# <a name="debugging-wow64"></a>Debuggen WOW64

Anwendungen, die unter WOW64 ausgeführt werden, können auf zwei Arten deentschlbelt werden

-   Verwenden Sie einen x86-gehosteten Debugger wie z. b. ntiond, WinDbg oder Visual Studio. Die 32-Bit-NTSD wird in "% SystemRoot% \\ syswow64" in Einzelhandels Installationen installiert. Beachten Sie, dass x86-Debugger zum Debuggen von x86-Code verwendet werden können. er kann jedoch nicht verwendet werden, um Breakpoints innerhalb der WOW64-Thunk-Ebene zu disassemblieren oder festzulegen, da es 64 sich um einen
-   Verwenden Sie einen systemeigenen Debugger wie CDB, NZD oder WinDbg und die WOW64-Debugger-Erweiterung, Wow64exts.dll. Wenn der Native Debugger unterbrochen wird, während sich der Prozessor im x86-Modus befindet, stellt der Debugger den Prozess als x86-Prozess dar. Wenn sich der Prozessor im einheitlichen Modus befindet, zeigt der Debugger den Prozess als Native an.

CDB, NZD und WinDbg sind in Debuggingtools für Windows enthalten. Weitere Informationen finden Sie in der Dokumentation [zu Debuggingtools für Windows](/windows-hardware/drivers/debugger/) .

Die Wow64exts-Debugger-Erweiterung wird mit WinDbg installiert. Verwenden Sie den Befehl! Load wow64exts, um die Debugger-Erweiterung zu laden. In der folgenden Tabelle sind die wow64exts-Debugger-Erweiterungs Befehle aufgeführt.



| Get-Help                | BESCHREIBUNG                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| ! wow64exts. SW          | Wechselt zwischen x86-und einheitlichen Modus.                                                                                                    |
| ! wow64exts. k- *Anzahl*   | Sichert eine kombinierte 32-Bit/64-Bit-Stapel Überwachung. Wenn *count* angegeben wird, sichert der Befehl die ersten *Anzahl* Adressen in jeder Stapel Überwachung.  |
| ! wow64exts.info        | Sichert grundlegende Informationen über den Peer des Prozesses, den TEB des aktuellen Threads und die von WOW64 verwendeten TLS-Slots (Thread Local Storage). |
| ! wow64exts. r- *Adresse* | Sichert den Kontext für die angegebene Adresse. Wenn *Address* nicht angegeben wird, gibt der Befehl den Kontext für den Prozessor aus.                     |



 

 

 