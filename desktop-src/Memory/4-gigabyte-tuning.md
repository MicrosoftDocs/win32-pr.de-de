---
description: '4-Gigabyte-Optimierung: BCDEdit und Boot.ini'
ms.assetid: 991eb86f-9e6f-4084-8b6f-f979e42104b5
title: '4-Gigabyte-Optimierung: BCDEdit und Boot.ini'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84c8cd7b824669abbe684af91d848f445fe287c333c04abc08c676f3e125d2b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386699"
---
# <a name="4-gigabyte-tuning-bcdedit-and-bootini"></a>4-Gigabyte-Optimierung: BCDEdit und Boot.ini

In 32-Bit-Editionen von Windows sind für Anwendungen 4 GIGABYTE (GB) virtueller Adressraum verfügbar. Der virtuelle Adressraum ist so aufgeteilt, dass 2 GB für die Anwendung und die anderen 2 GB nur für das System verfügbar sind. Das 4-Gigabyte-Optimierungsfeature (4GT- oder 4GT-RAM-Optimierung), das mit dem Befehl *BCDEdit /set increaseuserva* aktiviert wird, erhöht den virtuellen Adressraum, der für die Anwendung verfügbar ist, auf bis zu 3 GB und reduziert die für das System verfügbare Menge auf zwischen 1 und 2 GB.

Bei speicherintensiven Anwendungen wie Datenbankverwaltungssystemen (DBMS) kann die Verwendung eines größeren virtuellen Adressraums erhebliche Leistungs- und Skalierbarkeitsvorteile bieten. Der Dateicache, der ausgelagerte Pool und der nicht ausgelagerte Pool sind jedoch kleiner, was sich negativ auf Anwendungen mit hohem Netzwerkbetrieb oder E/A auswirken kann. Daher sollten Sie Ihre Anwendung unter Last testen und die Leistungsindikatoren untersuchen, um zu ermitteln, ob Ihre Anwendung vom größeren Adressraum profitiert.

Verwenden Sie zum Aktivieren von 4GT den Befehl [BCDEdit /set,](/windows-hardware/drivers/devtest/bcdedit--set) um die Starteintragsoption **increaseuserva** auf einen Wert zwischen 2048 (2 GB) und 3072 (3 GB) festzulegen.

**Windows Server 2003 und früher:** Um 4GT zu aktivieren, fügen Sie der datei Boot.ini den Schalter **/3GB** hinzu. Der **Schalter /3GB** wird auf den folgenden Systemen unterstützt:

-   Windows Server 2003
-   Windows XP Professional

Der **Schalter "/3GB"** stellt anwendungen vollständig 3 GB an virtuellem Adressraum zur Verfügung und reduziert die für das System verfügbare Menge auf 1 GB. Auf Windows Server 2003 kann der für Anwendungen verfügbare Adressraum angepasst werden, indem der **Schalter /USERVA** in Boot.ini auf einen Wert zwischen 2048 und 3072 festgelegt wird, wodurch sich der für das System verfügbare Adressraum erhöht. Dies kann dazu beitragen, die Gesamtleistung des Systems aufrechtzuerhalten, wenn die Anwendung mehr als 2 GB, aber weniger als 3 GB Adressraum benötigt.

Um einer Anwendung die Verwendung des größeren Adressraums zu ermöglichen, legen Sie das [**Flag IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) im Imageheader fest. Der in Microsoft Visual C++ enthaltene Linker unterstützt den Schalter **/LARGEADDRESSAWARE,** um dieses Flag festzulegen. Das Festlegen dieses Flags und anschließendes Ausführen der Anwendung auf einem System ohne 4GT-Unterstützung sollte sich nicht auf die Anwendung auswirken.

In 64-Bit-Editionen von Windows verfügen 32-Bit-Anwendungen, die mit dem Flag [**IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) gekennzeichnet sind, über 4 GB Adressraum.

**Itanium-Editionen von Windows Server 2003:** Vor SP1 sind für 32-Bit-Prozesse nur 2 GB Adressraum verfügbar.

Verwenden Sie die folgenden Richtlinien, um 4GT in Anwendungen zu unterstützen:

-   Adressen in der Nähe der 2-GB-Grenze werden in der Regel von verschiedenen System-DLLs verwendet. Daher kann ein 32-Bit-Prozess nicht mehr als 2 GB zusammenhängenden Arbeitsspeicher zuordnen, auch wenn der gesamte 4-GB-Adressraum verfügbar ist.
-   Verwenden Sie die [**GlobalMemoryStatusEx-Funktion,**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) um den gesamten virtuellen Benutzerbereich abzurufen. Verwenden Sie die [**GetSystemInfo-Funktion,**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) um die höchstmögliche Benutzeradresse abzurufen. Erkennen Sie zur Laufzeit immer den tatsächlichen Wert, und vermeiden Sie die Verwendung hartverkabelter Konstantendefinitionen, z. B.: `#define HIGHEST_USER_ADDRESS 0xC0000000` .
-   Vermeiden Sie signierte Vergleiche mit Zeigern, da sie dazu führen können, dass Anwendungen auf einem 4GT-fähigen System abstürzten. Eine Bedingung wie die folgende ist false für einen Zeiger, der über 2 GB liegt: `if (pointer > 40000000)` .
-   Code, der das höchste Bit eines Zeigers für einen anwendungsdefiniertem Zweck verwendet, schlägt fehl, wenn 4GT aktiviert ist. Beispielsweise kann ein 32-Bit-Wort als Benutzermodusadresse betrachtet werden, wenn es unter 0x80000000 ist, und ein Fehlercode, falls oben angegeben. Dies gilt nicht für 4GT.

[**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) gibt in der Regel niedrige Adressen vor hohen Adressen zurück. Daher verwendet Ihr Prozess möglicherweise keine sehr hohen Adressen, es sei denn, er belegt viel Arbeitsspeicher oder verfügt über einen fragmentierten virtuellen Adressraum. Um zu Testzwecken die Zuordnung von Zuordnungen von höheren Adressen vor niedrigeren Adressen zu erzwingen, geben Sie **MEM \_ TOP \_ DOWN** beim Aufrufen von **VirtualAlloc** an, oder legen Sie den folgenden Registrierungswert auf 0x100000 fest:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager** Memory \\ **Management** \\ **AllocationPreference**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeitsspeicherlimits für Windows Releases](memory-limits-for-windows-releases.md)
</dt> <dt>

[Physical Address Extension](physical-address-extension.md)
</dt> <dt>

[Technische Referenz zu 4GT](/previous-versions/windows/it-pro/windows-server-2003/cc778496(v=ws.10))
</dt> </dl>

 

 
