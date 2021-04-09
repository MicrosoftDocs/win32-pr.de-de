---
description: Die folgenden Begriffe werden verwendet, um das Debuggen zu beschreiben.
ms.assetid: 580f2787-d944-4350-a2c2-c00816b3f515
title: Debug-Terminologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa12e24a6c763f9cda983ad961ba85a41c63cec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958137"
---
# <a name="debugging-terminology"></a>Debug-Terminologie

Die folgenden Begriffe werden verwendet, um das Debuggen zu beschreiben.

<dl> <dt>

<span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Blauer Bildschirm
</dt> <dd>

Wenn das System ein Hardwareproblem, Daten Inkonsistenz oder einen ähnlichen Fehler feststellt, wird möglicherweise ein blauer Bildschirm mit Informationen angezeigt, mit denen die Ursache des Fehlers bestimmt werden kann. Diese Informationen umfassen den Endzeitpunkt und ob eine Absturz Abbild Datei erstellt wurde. Sie kann auch eine Liste geladener Treiber und eine Stapel Überwachung enthalten.

</dd> <dt>

<span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Absturz Abbild Datei
</dt> <dd>

Sie können das System so konfigurieren, dass Informationen in eine Absturz Abbild Datei auf der Festplatte geschrieben werden, wenn ein Stoppcode generiert wird. Die Datei enthält Informationen, die der Debugger verwenden kann, um den Fehler zu analysieren. Diese Datei kann so groß wie der physische Arbeitsspeicher auf dem Computer sein.

</dd> <dt>

<span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Debugger
</dt> <dd>

Ein Programm, das entwickelt wurde, um Fehler in einem anderen Programm zu erkennen, zu finden und zu korrigieren. Sie ermöglicht es dem Entwickler, die Ausführung des Prozesses und der zugehörigen Threads zu durchlaufen, Arbeitsspeicher, Variablen und andere Elemente von Prozess-und Thread Kontext zu überwachen.

</dd> <dt>

<span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Kernel Modus
</dt> <dd>

Der Prozessor Modus, in dem Systemdienste und Gerätetreiber ausgeführt werden. Alle Schnittstellen und CPU-Anweisungen sind verfügbar, und der Zugriff auf den gesamten Speicher ist möglich.

</dd> <dt>

<span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Minidumpdatei
</dt> <dd>

Anwendungen können Minidump-Dateien im Benutzermodus entwickeln, die eine nützliche Teilmenge der in einer Absturz Abbild Datei enthaltenen Informationen enthalten. Weitere Informationen finden Sie unter [Minidump files](minidump-files.md).

</dd> <dt>

<span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>Code Abbrechen
</dt> <dd>

Der Fehlercode, der den Fehler angibt, mit dem der Systemkernel nicht mehr ausgeführt wird.

</dd> <dt>

<span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Symbol Dateien
</dt> <dd>

Alle Systemanwendungen, Treiber und DLLs werden so erstellt, dass Ihre Debuginformationen in separaten Dateien gespeichert werden, die als Symbol Dateien bezeichnet werden. Daher ist das System kleiner und schneller, aber es kann dennoch debuggten werden, wenn die Symbol Dateien installiert sind. Weitere Informationen finden Sie unter [Symbol Dateien](symbol-files.md).

</dd> <dt>

<span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>Benutzermodus
</dt> <dd>

Der Prozessor Modus, in dem Anwendungen ausgeführt werden. Ein eingeschränkter Satz von Schnittstellen ist in diesem Modus verfügbar, und der Zugriff auf Systemdaten ist begrenzt.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren von automatischem Debugging](configuring-automatic-debugging.md)
</dt> </dl>

 

 



