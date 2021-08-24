---
title: Leistung und Arbeitsspeicherverbrauch unter WOW64
description: Leistung und Arbeitsspeicherverbrauch unter WOW64 werden durch die folgenden Faktoren bestimmt.
ms.assetid: 77759840-7b1a-4956-a038-d6374b6ec354
keywords:
- Leistung unter WOW64 64-Bit-Windows-Programmierung
- Arbeitsspeicherverbrauch unter WOW64 64-Bit-Windows-Programmierung
- WOW64 64-Bit-Windows Programmierung, Leistung
- WOW64 64-Bit-Windows Programmierung, Arbeitsspeicherverbrauch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d5dd20cb42245318bf2666da788b9eea9e371c3945155c1b03b876fa513f5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119613830"
---
# <a name="performance-and-memory-consumption-under-wow64"></a>Leistung und Arbeitsspeicherverbrauch unter WOW64

Leistung und Arbeitsspeicherverbrauch unter WOW64 werden durch die folgenden Faktoren bestimmt:

-   Prozessorhardware. Die Anweisungsemulation wird auf dem Chip ausgeführt. Auf dem x64-Prozessor werden x86-Anweisungen nativ vom Prozessor ausgeführt. Daher ähnelt die Ausführungsgeschwindigkeit unter WOW64 auf x64 der Geschwindigkeit unter 32-Bit-Windows. Auf dem Intel Itanium-Prozessor und allen ARM64-Prozessoren ist mehr Software an der Emulation beteiligt, und die Leistung beeinträchtigt dies.
-   API-Thunk-Mehraufwand. Dieser Mehraufwand ist im Vergleich zu Systemaufrufen an den NT-Kernel gering. NT-Kernelfunktionen sollen nur selten aufgerufen werden.
-   Größe des virtuellen Arbeitsspeichers. Auf dem Intel Itanium-Prozessor erhöht WOW64 erheblichen Mehraufwand, wenn zwei oder mehr Instanzen derselben 32-Bit-Anwendung gleichzeitig ausgeführt werden. Dies liegt an den nativen 8-KB-Seiten auf intel Itanium, die die Emulation der nativen 4-KB-Seiten in der x86-Architektur erschweren (mehr Seiten werden als schreibbar markiert, alle beschreibbaren Seiten sind für den Prozess privat). Dies kann sich negativ auf die Skalierbarkeit von Terminaldiensten auf bestimmten Prozessoren auswirken. Dies ist für den x64-Prozessor nicht der Fall.
-   Arbeitssatz. WOW64 erhöht die Größe des Arbeitssatzes der Anwendung.

WOW64 ermöglicht 32-Bit-Anwendungen die Nutzung des 64-Bit-Kernels. Daher können 32-Bit-Anwendungen eine größere Anzahl von Kernelhandles und Fensterhandles verwenden. 32-Bit-Anwendungen können jedoch möglicherweise nicht so viele Threads unter WOW64 wie möglich erstellen, wenn sie nativ auf x86-basierten Systemen ausgeführt werden, da WOW64 einen zusätzlichen 64-Bit-Stapel (normalerweise 512 KB) für jeden Thread zuordnet. Darüber hinaus ist ein teil des Adressraums für WOW64 selbst und die verwendeten Datenstrukturen reserviert. Der reservierte Betrag hängt vom Prozessor ab. mehr ist für die Intel Itanium reserviert als für die x64- oder ARM64-Prozessoren.

Wenn für die Anwendung das Flag [**IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) im Imageheader festgelegt ist, erhält jede 32-Bit-Anwendung 4 GB virtuellen Adressraum in der WOW64-Umgebung. Wenn das Flag **IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE** nicht festgelegt ist, erhält jede 32-Bit-Anwendung 2 GB virtuellen Adressraum in der WOW64-Umgebung.

 

 