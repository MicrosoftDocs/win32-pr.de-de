---
description: '4-Gigabyte-Optimierung: bcdedit und Boot.ini'
ms.assetid: 991eb86f-9e6f-4084-8b6f-f979e42104b5
title: '4-Gigabyte-Optimierung: bcdedit und Boot.ini'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f997ae09748370d5ec8ec246da80b6440d7aaf45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215914"
---
# <a name="4-gigabyte-tuning-bcdedit-and-bootini"></a>4-Gigabyte-Optimierung: bcdedit und Boot.ini

Bei 32-Bit-Editionen von Windows sind für Anwendungen 4 Gigabyte (GB) virtueller Adressraum verfügbar. Der virtuelle Adressraum ist dividiert, sodass der Anwendung 2 GB zur Verfügung stehen und die anderen 2 GB nur für das System verfügbar sind. Das mit dem Befehl *bcdedit/set reaseuserva* aktivierte Feature zur Optimierung von 4 Gigabyte (4GT oder 4GT RAM) erhöht den virtuellen Adressraum, der für die Anwendung zur Verfügung steht, auf bis zu 3 GB und reduziert den für das System verfügbaren Betrag zwischen 1 und 2 GB.

Bei Anwendungen, die Arbeitsspeicher intensiv sind, wie z. b. Datenbank-Managementsysteme (DBMS), kann die Verwendung eines größeren virtuellen Adressraums erhebliche Leistungs-und Skalierbarkeits Vorteile bieten. Der Dateicache, der Auslagerungs Pool und der nicht Auslagerungs Pool sind jedoch kleiner, was sich negativ auf Anwendungen mit starker Netzwerk-oder e/a-Auslastung auswirken kann. Daher empfiehlt es sich, die Anwendung unter Last zu testen und die Leistungsindikatoren zu überprüfen, um festzustellen, ob Ihre Anwendung von dem größeren Adressraum profitiert.

Um 4GT zu aktivieren, verwenden Sie den Befehl [bcdedit/set](/windows-hardware/drivers/devtest/bcdedit--set) , um die Option für den **starteuserva** -Start Eintrag auf einen Wert zwischen 2048 (2 GB) und 3072 (3 GB) festzulegen.

**Windows Server 2003 und früher:** Fügen Sie zum Aktivieren von 4GT den **/3GB** -Schalter zur Boot.ini Datei hinzu. Der Schalter " **/3GB** " wird auf den folgenden Systemen unterstützt:

-   Windows Server 2003
-   Windows XP Professional

Mit dem **/3GB** -Switch werden für Anwendungen ein vollständiger virtueller Adressraum von 3 GB zur Verfügung gestellt, und der für das System verfügbare Betrag wird auf 1 GB reduziert. Unter Windows Server 2003 kann der für Anwendungen verfügbare Adressraum angepasst werden, indem der **Option/USERVA bei** -Schalter in Boot.ini auf einen Wert zwischen 2048 und 3072 festgelegt wird. dadurch erhöht sich der für das System verfügbare Adressraum. Dadurch kann die Gesamtsystemleistung beibehalten werden, wenn die Anwendung mehr als 2 GB, aber weniger als 3 GB Adressraum erfordert.

Damit eine Anwendung den größeren Adressraum verwenden kann, legen Sie das Flag für die Groß-und Adresserkennung der [**Abbild \_ Datei \_ \_ \_**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) im Image-Header fest. Der in Microsoft Visual C++ enthaltene Linker unterstützt den Schalter **/LARGEADDRESSAWARE** , um dieses Flag festzulegen. Das Festlegen dieses Flags und das anschließende Ausführen der Anwendung auf einem System, das über keinen 4GT-Support verfügt, sollte sich nicht auf die Anwendung auswirken.

Bei 64-Bit-Editionen von Windows sind für 32-Bit-Anwendungen, die mit dem Flag für die [**Image \_ Datei mit \_ großen \_ Adressen \_**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) gekennzeichnet sind, 4 GB Adressraum verfügbar.

**Itanium-Editionen von Windows Server 2003:** Vor SP1 sind für 32-Bit-Prozesse nur 2 GB Adressraum verfügbar.

Verwenden Sie die folgenden Richtlinien zur Unterstützung von 4GT in-Anwendungen:

-   Adressen in der Nähe der 2-GB-Grenze werden in der Regel von verschiedenen System-DLLs verwendet. Daher kann ein 32-Bit-Prozess nicht mehr als 2 GB zusammenhängenden Speicher zuweisen, auch wenn der gesamte 4-GB-Adressraum verfügbar ist.
-   Verwenden Sie die [**GlobalMemoryStatus usex**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) -Funktion, um die Gesamtmenge des virtuellen Speicherplatzes für den Benutzer abzurufen. Verwenden Sie die [**GetSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) -Funktion, um die höchstmögliche Benutzer Adresse abzurufen. Erkennen Sie den tatsächlichen Wert immer zur Laufzeit, und vermeiden Sie die Verwendung von hart verdrahteten Konstanten Definitionen wie z `#define HIGHEST_USER_ADDRESS 0xC0000000` . b.:.
-   Vermeiden Sie signierte Vergleiche mit Zeigern, da Sie möglicherweise dazu führen, dass Anwendungen auf einem 4GT-fähigen Systemabstürzen. Eine Bedingung wie die folgende ist für einen Zeiger, der oberhalb von 2 GB liegt, auf false fest `if (pointer > 40000000)` .
-   Code, der das höchste Bit eines Zeigers für einen Anwendungs definierten Zweck verwendet, schlägt fehl, wenn 4GT aktiviert ist. Beispielsweise kann ein 32-Bit-Wort als benutzermodusadresse angesehen werden, wenn es unter 0x80000000 liegt, und ein Fehlercode, wenn dies der Fall ist. Dies gilt nicht für 4GT.

[**Virtualzuordc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) gibt in der Regel niedrige Adressen vor hohen Adressen zurück. Der Prozess verwendet daher möglicherweise nicht sehr hohe Adressen, es sei denn, er ordnet viel Speicherplatz zu oder verfügt über einen fragmentierten virtuellen Adressraum. Geben Sie beim Aufrufen von **VirtualAlloc** den Wert **\_ Top- \_ down** an, oder legen Sie den folgenden Registrierungs Wert auf 0x100000 fest, um Zuordnungen für die Zuordnung von höheren Adressen vor niedrigeren Adressen zu Testzwecken zu erzwingen:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager** \\ **Memory Management** \\ **zustandspreference**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeitsspeicher Grenzwerte für Windows-Releases](memory-limits-for-windows-releases.md)
</dt> <dt>

[Physical Address Extension](physical-address-extension.md)
</dt> <dt>

[4GT Technische Referenz](/previous-versions/windows/it-pro/windows-server-2003/cc778496(v=ws.10))
</dt> </dl>

 

 
