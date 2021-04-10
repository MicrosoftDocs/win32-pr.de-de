---
description: Der Steuerungs Schutz (Control Flow Guard, cfg) ist ein hochoptimiertes Platt Form Sicherheits Feature, das erstellt wurde, um Sicherheitslücken im Speicher zu beheben.
ms.assetid: 116EAD64-7CAE-455C-BA43-9492F78DE873
title: Ablaufsteuerungsschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91cf97a648443135e7fee666ea4c259b1c32104e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132024"
---
# <a name="control-flow-guard"></a>Ablaufsteuerungsschutz

## <a name="what-is-control-flow-guard"></a>Was ist Ablauf Steuerungs Schutz?

Der Steuerungs Schutz (Control Flow Guard, cfg) ist ein hochoptimiertes Platt Form Sicherheits Feature, das erstellt wurde, um Sicherheitslücken im Speicher zu beheben. Durch das Platzieren von strengen Einschränkungen für den Ort, an dem eine Anwendung Code ausführen kann, ist es für Exploits weitaus schwieriger, beliebigen Code durch Sicherheitsrisiken, wie z. b. Pufferüberläufe, auszuführen. CFG erweitert frühere Technologien zur exploentschärfung, wie z. b. [/GS](/cpp/build/reference/gs-buffer-security-check?view=vs-2019), [DEP](../memory/data-execution-prevention.md)und [ASLR](/archive/blogs/michael_howard/address-space-layout-randomization-in-windows-vista).

Diese Funktion ist in Microsoft Visual Studio 2015 verfügbar und wird unter "cfg-fähige" Versionen von Windows – den x86-und x64-Releases für Desktop und Server von Windows 10 und Windows 8.1 Update (KB3000850) ausgeführt.

Wir empfehlen Entwicklern dringend, cfg für Ihre Anwendungen zu aktivieren. Sie müssen CFG nicht für jeden Teil Ihres Codes aktivieren, da eine Mischung aus cfg-aktiviertem und nicht cfg aktiviertem Code problemlos ausgeführt werden kann. Wenn aber cfg nicht für den gesamten Code aktiviert werden kann, können Lücken im Schutz geöffnet werden. Außerdem funktioniert der cfg-aktivierte Code in den "cfg-nicht-"-Versionen von Windows einwandfrei und ist daher vollständig kompatibel mit diesen.

## <a name="how-can-i-enable-cfg"></a>Wie kann ich cfg Aktivieren?

In den meisten Fällen ist es nicht erforderlich, Quellcode zu ändern. Sie müssen lediglich eine Option zu Ihrem Visual Studio 2015-Projekt hinzufügen, und der Compiler und Linker aktivieren cfg.

Die einfachste Methode besteht darin, zu den **Projekt \| Eigenschaften \| Konfigurations Eigenschaften \| C/C++- \| Code Generierung** zu navigieren und für Ablauf Steuerungs Schutz die Option **Ja (/Guard: CF)** auszuwählen.

![CFG-Eigenschaft in Visual Studio](images/cfg-vs.png)

Alternativ dazu können Sie auch **/Guard: CF** zu den **Projekt \| Eigenschaften \| Konfigurations Eigenschaften \| C/C++ \| Befehlszeile \| zusätzliche Optionen** (für den Compiler) und **/Guard: CF** zu **Projekt \| Eigenschaften \| Konfigurations Eigenschaften \| Weitere Optionen für die Linkerbefehlszeile \| \|** (für den Linker) hinzufügen.

![CFG-Eigenschaft für Compiler](images/cfg-compiler.png)![CFG-Eigenschaft für Linker](images/cfg-linker.png)

Weitere Informationen finden Sie unter [/Guard (Ablauf Steuerungs Schutz aktivieren)](/cpp/build/reference/guard-enable-control-flow-guard?view=vs-2019) .

Wenn Sie Ihr Projekt von der Befehlszeile aus entwickeln, können Sie dieselben Optionen hinzufügen. Wenn Sie z. b. ein Projekt mit dem Namen "Test. cpp" kompilieren, verwenden Sie **cl/Guard: CF Test. cpp/Link/Guard: CF**.

Sie haben auch die Möglichkeit, den Satz von icalltarget-Adressen, die von CFG als gültig eingestuft werden, mithilfe von [**setprocessvalidcalltargets**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessvalidcalltargets) aus der-Speicherverwaltungs-API dynamisch zu steuern. Dieselbe API kann verwendet werden, um anzugeben, ob Seiten ungültige oder gültige Ziele für cfg sind. Die [**VirtualProtect**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualprotect) -und [**virtualdepc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) -Funktionen behandeln standardmäßig einen angegebenen Bereich von ausführbaren und zugeteilten Seiten als gültige indirekte callziele. Es ist möglich, dieses Verhalten außer Kraft zu setzen, z. b. bei der Implementierung eines Just-in-Time-Compilers  , indem Sie beim Aufrufen von " **VirtualProtect** " die Option " [](/windows/desktop/Memory/memory-protection-constants) **Seiten \_ Ziele \_** " angeben **\_ \_ \_**

## <a name="how-do-i-tell-that-a-binary-is-under-control-flow-guard"></a>Wie erkenne ich, dass eine Binärdatei unter Ablauf Steuerungs Schutz ist?

Führen Sie das [(dumpbin-Tool](/cpp/build/reference/dumpbin-reference) (das in der Visual Studio 2015-Installation enthalten ist) über die Visual Studio-Eingabeaufforderung mit den Optionen */Headers* und */LOADCONFIG* aus: **(dumpbin/Headers/LOADCONFIG test.exe**. Die Ausgabe für eine Binärdatei unter cfg sollte anzeigen, dass die Header Werte "Guard" enthalten, und die Werte der Lade Konfiguration enthalten "CF instrumentiert" und "FID Table Present".

![Ausgabe von (dumpbin/Headers](images/cfg-dumpbin-headers.png)

![Ausgabe von (dumpbin/LOADCONFIG](images/cfg-dumpbin-loadconfig.png)

## <a name="how-does-cfg-really-work"></a>Wie funktioniert cfg wirklich?

Software Sicherheitslücken werden oft ausgenutzt, wenn ein ausgelaufendes Programm unwahrscheinliche, ungewöhnliche oder Extreme Daten bereitstellt. Ein Angreifer kann z. b. ein Pufferüberlauf-Sicherheitsrisiko ausnutzen, indem er mehr Eingaben für ein Programm als erwartet bereitstellt, wodurch der Bereich, der vom Programm reserviert ist, zum Speichern einer Antwort überschritten wird. Dadurch kann der angrenzende Arbeitsspeicher beschädigt werden, der einen Funktionszeiger enthalten kann. Wenn das Programm diese Funktion aufruft, springt es möglicherweise zu einem unbeabsichtigten Speicherort, der vom Angreifer festgelegt wurde.

Eine potente Kombination der Kompilierungs-und Laufzeitunterstützung von CFG implementiert jedoch die Ablauf Steuerungs Integrität, die eng einschränkt, wo indirekte Aufruf Anweisungen ausgeführt werden können.

Der Compiler führt Folgendes aus:

1.  Fügt dem kompilierten Code Lightweight-Sicherheitsüberprüfungen hinzu.
2.  Identifiziert den Satz von Funktionen in der Anwendung, die gültige Ziele für indirekte Aufrufe sind.

Die Runtime-Unterstützung, die vom Windows-Kernel bereitgestellt wird:

1.  Verwaltet den Zustand, der gültige indirekte Rückruf Ziele identifiziert, effizient.
2.  Implementiert die Logik, die überprüft, ob ein indirektes aufrufsziel gültig ist.

So veranschaulichen Sie Folgendes:

![CFG-Pseudo Code](images/cfg-pseudocode.jpg)

Wenn bei einer cfg-Überprüfung zur Laufzeit ein Fehler auftritt, beendet Windows das Programm sofort und unterbricht dadurch alle Exploits, die versuchen, indirekt eine ungültige Adresse aufzurufen.

 

 
