---
description: Die folgenden Begriffe werden beim Beschreiben des Debuggens verwendet.
ms.assetid: 580f2787-d944-4350-a2c2-c00816b3f515
title: Debugterminologie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feb8de5035887f3d3c19cca1e8475ff17cb930b1142c712481e096e0e612ea81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692070"
---
# <a name="debugging-terminology"></a>Debugterminologie

Die folgenden Begriffe werden beim Beschreiben des Debuggens verwendet.

<dl> <dt>

<span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Blauer Bildschirm
</dt> <dd>

Wenn auf dem System ein Hardwareproblem, eine Dateninkonsistenz oder ein ähnlicher Fehler auftritt, wird möglicherweise ein Blaubildschirm mit Informationen angezeigt, mit denen die Ursache des Fehlers ermittelt werden kann. Diese Informationen enthalten den STOP-Code und die Angabe, ob eine Absturzabbilddatei erstellt wurde. Sie kann auch eine Liste geladener Treiber und eine Stapelüberwachung enthalten.

</dd> <dt>

<span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Absturzabbilddatei
</dt> <dd>

Sie können das System so konfigurieren, dass Informationen in eine Absturzabbilddatei auf Ihrer Festplatte geschrieben werden, wenn ein STOP-Code generiert wird. Die Datei enthält Informationen, die der Debugger zum Analysieren des Fehlers verwenden kann. Diese Datei kann so groß sein wie der physische Speicher, der auf dem Computer enthalten ist.

</dd> <dt>

<span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Debugger
</dt> <dd>

Ein Programm, das dazu dient, Fehler in einem anderen Programm zu erkennen, zu finden und zu beheben. Es ermöglicht dem Entwickler, die Ausführung des Prozesses und seiner Threads schrittweise zu durchlaufen, Arbeitsspeicher, Variablen und andere Elemente des Prozess- und Threadkontexts zu überwachen.

</dd> <dt>

<span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Kernelmodus
</dt> <dd>

Der Prozessormodus, in dem Systemdienste und Gerätetreiber ausgeführt werden. Alle Schnittstellen und CPU-Anweisungen sind verfügbar, und der gesamte Arbeitsspeicher ist verfügbar.

</dd> <dt>

<span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Minidump-Datei
</dt> <dd>

Anwendungen können Minidumpdateien im Benutzermodus erstellen, die eine nützliche Teilmenge der Informationen enthalten, die in einer Absturzabbilddatei enthalten sind. Weitere Informationen finden Sie unter [Minidumpdateien.](minidump-files.md)

</dd> <dt>

<span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>STOP-Code
</dt> <dd>

Der Fehlercode, der den Fehler identifiziert, durch den die weitere Ausführung des Systemkernels beendet wurde.

</dd> <dt>

<span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Symboldateien
</dt> <dd>

Alle Systemanwendungen, Treiber und DLLs werden so erstellt, dass sich ihre Debuginformationen in separaten Dateien befinden, die als Symboldateien bezeichnet werden. Daher ist das System kleiner und schneller, kann aber trotzdem debuggt werden, wenn die Symboldateien installiert sind. Weitere Informationen finden Sie unter [Symboldateien.](symbol-files.md)

</dd> <dt>

<span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>Benutzermodus
</dt> <dd>

Der Prozessormodus, in dem Anwendungen ausgeführt werden. In diesem Modus ist ein eingeschränkter Satz von Schnittstellen verfügbar, und der Zugriff auf Systemdaten ist eingeschränkt.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konfigurieren des automatischen Debuggens](configuring-automatic-debugging.md)
</dt> </dl>

 

 



