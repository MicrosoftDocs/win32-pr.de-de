---
description: Control Flow Guard (CFG) ist ein hochoptimiertes Plattformsicherheitsfeature, das erstellt wurde, um Sicherheitsrisiken durch Speicherbeschädigungen zu beseitigen.
ms.assetid: 116EAD64-7CAE-455C-BA43-9492F78DE873
title: Ablaufsteuerungsschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62186a86f821e7eb350381c7dfbc500c80dd040f4321a8f630c7d408937a8460
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622817"
---
# <a name="control-flow-guard"></a>Ablaufsteuerungsschutz

## <a name="what-is-control-flow-guard"></a>Was ist Control Flow Guard?

Control Flow Guard (CFG) ist ein hochoptimiertes Plattformsicherheitsfeature, das erstellt wurde, um Sicherheitsrisiken durch Speicherbeschädigungen zu beseitigen. Durch die Strengung von Einschränkungen, von wo aus eine Anwendung Code ausführen kann, ist es für Exploits wesentlich schwieriger, beliebigen Code durch Sicherheitsrisiken wie Pufferüberläufe auszuführen. CFG erweitert frühere Exploit-Entschärfungstechnologien wie [/GS,](/cpp/build/reference/gs-buffer-security-check?view=vs-2019) [DEP](../memory/data-execution-prevention.md)und [ASLR.](/archive/blogs/michael_howard/address-space-layout-randomization-in-windows-vista)

Dieses Feature ist in Microsoft Visual Studio 2015 verfügbar und wird unter CFG-orientierte Versionen von Windows ausgeführt– den x86- und x64-Releases für Desktop und Server von Windows 10 und Windows 8.1 Update (KB3000850).

Wir empfehlen Entwicklern dringend, CFG für ihre Anwendungen zu aktivieren. Sie müssen CFG nicht für jeden Teil Ihres Codes aktivieren, da eine Mischung aus CFG-fähigem und nicht CFG-fähigem Code einwandfrei ausgeführt wird. Wenn CFG jedoch nicht für den ganzen Code aktiviert wird, können Lücken im Schutz geöffnet werden. Darüber hinaus funktioniert CFG-fähiger Code gut für CFG-nicht fähige Versionen von Windows und ist daher vollständig kompatibel mit ihnen.

## <a name="how-can-i-enable-cfg"></a>Wie kann ich CFG aktivieren?

In den meisten Fällen ist es nicht notwendig, den Quellcode zu ändern. Sie müssen ihrem Visual Studio 2015-Projekt nur eine Option hinzufügen, und der Compiler und linker aktivieren CFG.

Die einfachste Methode besteht in der Navigation zu Project Eigenschaftenkonfigurationseigenschaften **\| \| \| C/C++-Codegenerierung, \|** und wählen Sie ja **(/guard:cf)** für Control Flow Guard aus.

![cfg-Eigenschaft in Visual Studio](images/cfg-vs.png)

Alternativ können Sie **"/guard:cf"** zu den konfigurationseigenschaften von **Project \| \| \| C/C++-Befehlszeilenoptionen \| \|** (für den Compiler) und **"/guard:cf"** zu zusätzlichen Optionen für die Linkerbefehlszeile der Project-Eigenschaftenkonfigurationseigenschaften (für den **\| \| \| Linker) \| \|** hinzufügen.

![cfg-Eigenschaft für compiler](images/cfg-compiler.png)![cfg-Eigenschaft für Linker](images/cfg-linker.png)

Weitere [Informationen finden Sie unter /guard (Control Flow Guard](/cpp/build/reference/guard-enable-control-flow-guard?view=vs-2019) aktivieren).

Wenn Sie Ihr Projekt über die Befehlszeile erstellen, können Sie die gleichen Optionen hinzufügen. Wenn Sie beispielsweise ein Projekt namens test.cpp kompilieren, verwenden Sie **cl /guard:cf test.cpp /link /guard:cf**.

Sie haben auch die Möglichkeit, den Satz von icall-Zieladressen, die von CFG als gültig angesehen werden, dynamisch mithilfe von [**SetProcessValidCallTargets**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessvalidcalltargets) aus der Memory-Verwaltungs-API. Dieselbe API kann verwendet werden, um anzugeben, ob Seiten ungültige oder gültige Ziele für CFG sind. Die [**Funktionen VirtualProtect**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotect) und [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) behandeln standardmäßig einen angegebenen Bereich von ausführbaren Und-Committed-Seiten als gültige indirekte Aufrufziele. Es ist möglich, dieses Verhalten zu überschreiben, z. B. beim Implementieren eines Just-in-Time-Compilers, indem **PAGE \_ TARGETS \_ INVALID** beim Aufruf von **VirtualAlloc** oder **PAGE TARGETS NO \_ \_ \_ UPDATE** beim Aufrufen von **VirtualProtect** angegeben wird, wie unter [**Memory Protection Constants**](/windows/desktop/Memory/memory-protection-constants)beschrieben.

## <a name="how-do-i-tell-that-a-binary-is-under-control-flow-guard"></a>Wie erstelle ich, dass eine Binärdatei unter Control Flow Guard steht?

Führen Sie das [Tool dumpbin](/cpp/build/reference/dumpbin-reference) (in der Installation von Visual Studio 2015 enthalten) über die Visual Studio-Eingabeaufforderung mit den Optionen */headers* und */loadconfig* aus: **dumpbin /headers /loadconfig test.exe**. Die Ausgabe für eine Binärdatei unter CFG sollte zeigen, dass die Headerwerte "Guard" enthalten und dass die Werte für die Ladekonfiguration "CF Instrumented" und "FID table present" enthalten.

![Ausgabe von dumpbin /headers](images/cfg-dumpbin-headers.png)

![Ausgabe von dumpbin /loadconfig](images/cfg-dumpbin-loadconfig.png)

## <a name="how-does-cfg-really-work"></a>Wie funktioniert CFG wirklich?

Softwareschwachstellen werden häufig ausgenutzt, indem unwahrscheinliche, ungewöhnliche oder extreme Daten für ein ausgeführtes Programm zur Verfügung stehen. Beispielsweise kann ein Angreifer ein Pufferüberlauf-Sicherheitsrisiko ausnutzen, indem er mehr Eingaben für ein Programm als erwartet liefert, wodurch der vom Programm reservierte Bereich für eine Antwort überlaufen wird. Dies könnte angrenzenden Arbeitsspeicher beschädigt, der einen Funktionszeiger halten kann. Wenn das Programm diese Funktion aufruft, kann es zu einem unbeabsichtigten Speicherort springen, der vom Angreifer angegeben wird.

Eine kombination aus Kompilier- und Laufzeitunterstützung von CFG implementiert jedoch die Ablaufsteuerungsintegrität, die eng einschränkt, wo Anweisungen für indirekte Aufrufe ausgeführt werden können.

Der Compiler führt folgende Schritte aus:

1.  Fügt dem kompilierten Code einfache Sicherheitsüberprüfungen hinzu.
2.  Identifiziert den Satz von Funktionen in der Anwendung, die gültige Ziele für indirekte Aufrufe sind.

Die Laufzeitunterstützung, die vom Windows bereitgestellt wird:

1.  Verwaltet effizient den Zustand, der gültige indirekte Aufrufziele identifiziert.
2.  Implementiert die Logik, die überprüft, ob ein indirektes Aufrufziel gültig ist.

Zur Veranschaulichung:

![CFG-Pseudocode](images/cfg-pseudocode.jpg)

Wenn eine CFG-Überprüfung zur Laufzeit fehlschlägt, beendet Windows das Programm sofort und unterbricht somit alle Exploits, die versuchen, indirekt eine ungültige Adresse aufrufen.

 

 
