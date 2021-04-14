---
title: Leistung und Arbeitsspeicher Verbrauch unter WOW64
description: Der Leistungs-und Arbeitsspeicher Verbrauch unter WOW64 wird durch die folgenden Faktoren bestimmt.
ms.assetid: 77759840-7b1a-4956-a038-d6374b6ec354
keywords:
- Leistung unter WOW64 64-Bit-Windows-Programmierung
- Arbeitsspeicher Nutzung unter WOW64 64-Bit-Windows-Programmierung
- WOW64 64-Bit-Windows-Programmierung, Leistung
- WOW64 64-Bit-Windows-Programmierung, Arbeitsspeicher Nutzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8928e7d50c8396aa2b5b34081af3e4ee2719e044
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390875"
---
# <a name="performance-and-memory-consumption-under-wow64"></a>Leistung und Arbeitsspeicher Verbrauch unter WOW64

Der Leistungs-und Arbeitsspeicher Verbrauch unter WOW64 wird durch die folgenden Faktoren bestimmt:

-   Prozessor Hardware. Die Anweisungs Emulation wird auf dem Chip ausgeführt. Auf dem x64-Prozessor werden x86-Anweisungen nativ vom Prozessor ausgeführt. Daher ist die Ausführungsgeschwindigkeit unter WOW64 auf x64 vergleichbar mit der Geschwindigkeit unter 32-Bit-Windows. Auf dem Intel Itanium-Prozessor und allen ARM64-Prozessoren ist mehr Software an der Emulation beteiligt, und die Leistung wird dadurch beeinträchtigt.
-   API-Thunk-Aufwand. Dieser Aufwand ist im Vergleich zu Systemaufrufen an den NT-Kernel gering. NT-Kernelfunktionen sollen nur selten aufgerufen werden.
-   Größe des virtuellen Arbeitsspeichers. Auf dem Intel Itanium-Prozessor erhöht WOW64 einen erheblichen mehr Aufwand, wenn mindestens zwei Instanzen der gleichen 32-Bit-Anwendung gleichzeitig ausgeführt werden. Dies liegt an den nativen 8-KB-Seiten auf dem Intel Itanium, der die Emulation der systemeigenen 4-KB-Seiten in der x86-Architektur erschwert (mehr Seiten werden als beschreibbar gekennzeichnet; Alle beschreibbaren Seiten sind für den Prozess privat). Dies kann sich negativ auf die Skalierbarkeit von Terminal Diensten auf bestimmten Prozessoren auswirken. Dies ist für den x64-Prozessor nicht der Fall.
-   Workingset. WOW64 vergrößert die Größe des Workingsets der Anwendung.

WOW64 ermöglicht es 32-Bit-Anwendungen, den 64-Bit-Kernel zu nutzen. Daher können 32-Bit-Anwendungen eine größere Anzahl von Kernel Handles und Fenster Handles verwenden. 32-Bit-Anwendungen können jedoch möglicherweise nicht so viele Threads unter WOW64 erstellen, wie Sie bei der nativen Ausführung auf x86-basierten Systemen möglich sind, da WOW64 einen zusätzlichen 64-Bit-Stapel (in der Regel 512 KB) für jeden Thread zuordnet. Außerdem ist eine bestimmte Menge an Adressraum für WOW64 und die verwendeten Datenstrukturen reserviert. Der reservierte Betrag hängt vom Prozessor ab. mehr ist auf dem Intel Itanium als auf den x64-oder ARM64-Prozessoren reserviert.

Wenn für die Anwendung das Flag für die [**Image \_ Datei mit \_ großen \_ Adress \_**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) Werten im Image Header festgelegt ist, erhält jede 32-Bit-Anwendung 4 GB virtuellen Adressraum in der WOW64-Umgebung. Wenn das Flag zum **\_ \_ Erkennen von großen \_ Adressen \_ für die Image Datei** nicht festgelegt ist, erhält jede 32-Bit-Anwendung 2 GB virtuellen Adressraum in der WOW64-Umgebung.

 

 