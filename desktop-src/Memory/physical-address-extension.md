---
description: Physical Address Extension (PAE) ist ein Prozessorfeature, das x86-Prozessoren den Zugriff auf mehr als 4 GB physischen Speicher in fähigen Versionen von Windows.
ms.assetid: 1aec2414-cc93-4a86-955d-2433360c9125
title: Physical Address Extension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2fd9193a19d228f26a09865086c59b65c0019b3cee42142dfd27188eff30169
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979720"
---
# <a name="physical-address-extension"></a>Physical Address Extension

Physical Address Extension (PAE) ist ein Prozessorfeature, das x86-Prozessoren den Zugriff auf mehr als 4 GB physischen Speicher in fähigen Versionen von Windows. Bestimmte 32-Bit-Versionen von Windows Server, die auf x86-basierten Systemen ausgeführt werden, können PAE verwenden, um abhängig von der physischen Adressgröße des Prozessors auf bis zu 64 GB oder 128 GB physischen Arbeitsspeicher zu zugreifen. Weitere Informationen finden Sie unter [Arbeitsspeicherlimits für Windows Releases.](memory-limits-for-windows-releases.md)

Die Intel Itanium- und x64-Prozessorarchitekturen können nativ auf mehr als 4 GB physischen Speicher zugreifen und bieten daher nicht das Äquivalent zu PAE. PAE wird nur von 32-Bit-Versionen von Windows auf x86-basierten Systemen verwendet.

Mit PAE wechselt das Betriebssystem von der linearen Adressübersetzung auf zwei Ebene in die Adressübersetzung auf drei Ebene. Anstatt eine lineare Adresse in drei separate Felder für die Indizierung in Speichertabellen zu unterteilen, wird sie in vier separate Felder aufgeteilt: ein 2-Bit-Bitfeld, zwei 9-Bit-Bitfelder und ein 12-Bit-Bitfeld, das der von der Intel-Architektur implementierten Seitengröße entspricht (4 KB). Die Größe von Seitentabelleneinträgen (Page Table Entries, PTEs) und Seitenverzeichniseinträgen (PDEs) im PAE-Modus wird von 32 auf 64 Bits erhöht. Die zusätzlichen Bits ermöglichen einem PTE- oder PDE-Betriebssystem, auf physischen Speicher über 4 GB zu verweisen.

In 32-Bit-Windows, die auf x64-basierten Systemen ausgeführt werden, ermöglicht PAE auch mehrere erweiterte System- und Prozessorfeatures, darunter hardwarefähige Datenausführungsverhindung (Data [Execution Prevention,](data-execution-prevention.md) DEP), nicht einheitlicher Speicherzugriff [(NON-Uniform Memory Access, NUMA)](../procthread/numa-support.md)und die Möglichkeit, einem System während der Ausführung Arbeitsspeicher hinzuzufügen (Hot-Add-Arbeitsspeicher).

Pae ändert nicht die Menge des virtuellen Adressraums, der für einen Prozess verfügbar ist. Jeder Prozess, der in 32-Bit-Windows ausgeführt wird, ist weiterhin auf einen virtuellen Adressraum von 4 GB beschränkt.

## <a name="system-support-for-pae"></a>Systemunterstützung für PAE

PAE wird nur in den folgenden 32-Bit-Versionen von Windows auf x86-basierten Systemen unterstützt:

-   Windows 7 (nur 32 Bit)
-   Windows Server 2008 (nur 32 Bit)
-   Windows Vista (nur 32-Bit)
-   Windows Server 2003 (nur 32 Bit)
-   Windows XP (nur 32-Bit)

## <a name="enabling-pae"></a>Aktivieren der PAE

Windows aktiviert PAE automatisch, wenn DEP auf einem Computer aktiviert ist, der hardwarefähigen DEP unterstützt, oder wenn der Computer für Hot-Add-Speichergeräte in Arbeitsspeicherbereichen über 4 GB konfiguriert ist. Wenn der Computer keinen hardwarefähigen DEP unterstützt oder nicht für Hot-Add-Speichergeräte im Arbeitsspeicher von mehr als 4 GB konfiguriert ist, muss PAE explizit aktiviert werden.

Um PAE explizit zu aktivieren, verwenden Sie den folgenden [**BCDEdit /set-Befehl,**](/windows-hardware/drivers/devtest/bcdedit--set) um die Option für den **Pae-Starteintrag** zu festlegen:

 **bcdedit /set \[ {ID} \] pae ForceEnable**  


Wenn DEP aktiviert ist, kann PAE nicht deaktiviert werden. Verwenden Sie die folgenden [**BCDEdit /set-Befehle,**](/windows-hardware/drivers/devtest/bcdedit--set) um DEP und PAE zu deaktivieren:

 **bcdedit /set \[ {ID} \] nx AlwaysOff**  
**bcdedit /set \[ {ID} \] pae ForceDisable**  


**Windows Server 2003 und Windows XP:** Verwenden Sie zum Aktivieren der PAE den **Schalter /PAE** in der [boot.ini](/windows-hardware/drivers/devtest/overview-of-the-boot-ini-file) Datei. Verwenden Sie zum Deaktivieren der PAE **den Schalter /NOPAE.** Verwenden Sie zum Deaktivieren von DEP den **Schalter /EXECUTE.**

## <a name="comparing-pae-and-other-large-memory-support"></a>Vergleichen von PAE und anderer Unterstützung für großen Arbeitsspeicher

PAE, [4-Gigabyte-Optimierung](4-gigabyte-tuning.md) (4GT) und [Adressfenstererweiterungen](address-windowing-extensions.md) (Address Windowing Extensions, AWE) dienen verschiedenen Zwecken und können unabhängig voneinander verwendet werden:

-   Pae ermöglicht dem Betriebssystem den Zugriff auf und die Verwendung von mehr als 4 GB physischem Speicher.
-   4GT erhöht den Teil des virtuellen Adressraums, der für einen Prozess verfügbar ist, von 2 GB auf bis zu 3 GB.
-   AWE ist ein Satz von APIs, mit denen ein Prozess nicht auspageten physischen Speicher zuordnen und dann Teile dieses Arbeitsspeichers dynamisch dem virtuellen Adressraum des Prozesses zuordnen kann.

Wenn weder 4GT noch AWE verwendet werden, wird die Menge des physischen Speichers, den ein einzelner 32-Bit-Prozess verwenden kann, durch die Größe des Adressraums (2 GB) beschränkt. In diesem Fall kann ein PAE-fähiges System weiterhin mehr als 4 GB RAM nutzen, um mehrere Prozesse gleichzeitig ausführen oder Dateidaten im Arbeitsspeicher zwischenspeichern zu können.

4GT kann mit oder ohne PAE verwendet werden. Einige Versionen von Windows begrenzen jedoch die maximale Menge an physischem Arbeitsspeicher, die unterstützt werden kann, wenn 4GT verwendet wird. Auf solchen Systemen führt das Starten mit aktivierter 4GT-Funktion dazu, dass das Betriebssystem jeglichen Arbeitsspeicher ignoriert, der den Grenzwert überschreitet.

AWE erfordert keine PAE oder 4GT, wird aber häufig zusammen mit PAE verwendet, um mehr als 4 GB physischen Speicher aus einem einzelnen 32-Bit-Prozess zu reservieren.

## <a name="related-topics"></a>Zugehörige Themen



[**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent)
</dt> <dt>

[Technische Referenz zu PAE X86](/previous-versions/windows/it-pro/windows-server-2003/cc728455(v=ws.10))
</dt> </dl>

 

 
