---
description: Bei der physischen Adress Erweiterung (PE) handelt es sich um eine Prozessor Funktion, mit der x86-Prozessoren auf mehr als 4 GB physischen Arbeitsspeicher in fähigen Windows-Versionen zugreifen können.
ms.assetid: 1aec2414-cc93-4a86-955d-2433360c9125
title: Physical Address Extension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd313c1025eaaf4859436aebef90288c6d3fe49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050603"
---
# <a name="physical-address-extension"></a>Physical Address Extension

Bei der physischen Adress Erweiterung (PE) handelt es sich um eine Prozessor Funktion, mit der x86-Prozessoren auf mehr als 4 GB physischen Arbeitsspeicher in fähigen Windows-Versionen zugreifen können. Bestimmte 32-Bit-Versionen von Windows Server, die auf x86-basierten Systemen ausgeführt werden, können für den Zugriff auf bis zu 64 GB oder 128 GB an physischem Arbeitsspeicher verwenden. Dies hängt von der physischen Adressgröße des Prozessors ab. Weitere Informationen finden Sie unter Arbeits [Speicher Grenzwerte für Windows-Releases](memory-limits-for-windows-releases.md).

Die Intel Itanium-und x64-Prozessorarchitekturen können nativ auf mehr als 4 GB physischen Speicher zugreifen und somit nicht die Entsprechung von "PE" bereitstellen. Die Verwendung von "bin" wird nur von 32-Bit-Versionen von Windows verwendet, die auf x86-basierten Systemen ausgeführt werden.

Bei der Verwendung von PE wechselt das Betriebssystem von der zweistufigen linearen Adressübersetzung in die Adressübersetzung mit drei Ebenen. Anstatt eine lineare Adresse in drei separate Felder zur Indizierung in Speicher Tabellen aufzuteilen, wird Sie in vier separate Felder aufgeteilt: ein 2-Bit-Bitfeld, 2 9-Bit-Bitfelder und ein 12-Bit-Bitfeld, das der von der Intel-Architektur (4 KB) implementierten Seitengröße entspricht. Die Größe von Seitentabellen Einträgen (PTEs) und Seiten Verzeichnis Einträgen (PDEs) im PAE-Modus wird von 32 auf 64 Bits angehoben. Die zusätzlichen Bits ermöglichen einem Betriebssystem-Pte oder PDE den Verweis auf physischen Speicher über 4 GB.

In 32-Bit-Fenstern, die auf x64-basierten Systemen ausgeführt werden, bietet auch eine Reihe erweiterter System-und Prozessor Features, wie z. b. die Hardware aktivierte [Daten Ausführungs Verhinderung (Data Execution Prevention](data-execution-prevention.md) , DEP), [nicht einheitlicher Speicherzugriff (Non-Uniform Memory Access, NUMA)](../procthread/numa-support.md)und die Möglichkeit, einem System während der Ausführung Arbeitsspeicher hinzuzufügen (Speicherplatz

Der für einen Prozess verfügbare virtuelle Adressraum wird von der Kategorie nicht geändert. Jeder Prozess, der in 32-Bit-Windows ausgeführt wird, ist immer noch auf einen virtuellen Adressraum von 4 GB beschränkt.

## <a name="system-support-for-pae"></a>System Unterstützung für die

Der Wert von "bin" wird nur für die folgenden 32-Bit-Versionen von Windows unterstützt, die auf x86-basierten Systemen ausgeführt werden

-   Windows 7 (nur 32 Bit)
-   Windows Server 2008 (nur 32 Bit)
-   Windows Vista (nur 32 Bit)
-   Windows Server 2003 (nur 32 Bit)
-   Windows XP (nur 32 Bit)

## <a name="enabling-pae"></a>Aktivieren von "bin"

Wenn die DEP-Funktion auf einem Computer aktiviert ist, der das Hardware fähige DEP-Gerät unterstützt, oder wenn der Computer für das Hinzufügen von Arbeitsspeicher Geräten im Arbeitsspeicher mit einem Wert von mehr als 4 GB konfiguriert ist. Wenn der Computer kein Hardware fähiges DEP-Gerät unterstützt oder nicht für das Hinzufügen von Arbeitsspeicher Geräten im Arbeitsspeicher in einem Arbeitsspeicher Bereich von mehr als 4 GB konfiguriert ist, muss die-Option explizit aktiviert werden.

Verwenden Sie zum expliziten Aktivieren von PAE den folgenden [**Bcdedit**](/windows-hardware/drivers/devtest/bcdedit--set) -Befehl/Set, um die Option für den **PAE** -Start Eintrag festzulegen:

 **bcdedit/set \[ {ID} \] PAE forceenable**  


Wenn DEP aktiviert ist, kann die Funktion nicht deaktiviert werden. Verwenden Sie die folgenden [**bcdedit/set**](/windows-hardware/drivers/devtest/bcdedit--set) -Befehle, um DEP und PAE zu deaktivieren:

 **bcdedit/set \[ {ID} \] NX AlwaysOff**  
**bcdedit/set \[ {ID} \] PAE forcedeaktiviert**  


**Windows Server 2003 und Windows XP:** Verwenden Sie zum Aktivieren von "PE" den Schalter " **/PAE-Schalter** " in der [boot.ini](/windows-hardware/drivers/devtest/overview-of-the-boot-ini-file) -Datei. Verwenden Sie zum Deaktivieren von "PE" den **/NOPAE** -Schalter. Verwenden Sie zum Deaktivieren des DEP den **/Execute** -Schalter.

## <a name="comparing-pae-and-other-large-memory-support"></a>Vergleichen von Unterstützung von "PE" und anderem Umfang

Die Erweiterungen von "PE", " [4 Gigabyte](4-gigabyte-tuning.md) " (4GT) und " [Address windowingextensions](address-windowing-extensions.md) " (AWE) dienen unterschiedlichen Zwecken und können unabhängig voneinander verwendet werden:

-   Das Betriebssystem ermöglicht dem Betriebssystem den Zugriff auf und die Verwendung von mehr als 4 GB physischem Arbeitsspeicher.
-   4GT vergrößert den Teil des virtuellen Adressraums, der einem Prozess von 2 GB bis zu 3 GB zur Verfügung steht.
-   Bei AWE handelt es sich um einen Satz von APIs, mit denen ein Prozess nicht auslagerbarer physischer Speicher zuordnen und dann Teile dieses Speichers dynamisch dem virtuellen Adressraum des Prozesses zuordnen kann.

Wenn weder "4GT" noch "AWE" verwendet wird, wird die Größe des physischen Speichers, der von einem einzelnen 32-Bit-Prozess verwendet werden kann, durch die Größe des Adressraums (2 GB) beschränkt. In diesem Fall kann ein für die PE aktiviertes System immer noch mehr als 4 GB RAM verwenden, um mehrere Prozesse gleichzeitig auszuführen oder Datei Daten im Arbeitsspeicher zwischenzuspeichern.

4GT kann mit oder ohne paar verwendet werden. Einige Versionen von Windows schränken jedoch die maximale Menge an physischem Arbeitsspeicher ein, die bei Verwendung von 4GT unterstützt werden kann. Bei solchen Systemen wird durch das Starten mit 4GT aktiviert das Betriebssystem ignoriert, dass der Arbeitsspeicher über den Grenzwert hinausgeht.

AWE erfordert weder "PE" noch "4GT", wird aber häufig in Verbindung mit "PE" verwendet, um mehr als 4 GB physischen Arbeitsspeicher aus einem einzelnen 32-Bit-Prozess zuzuordnen.

## <a name="related-topics"></a>Zugehörige Themen



[**Isprocessorfeaturepräsentiert**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent)
</dt> <dt>

[Technische Referenz zu "PE x86"](/previous-versions/windows/it-pro/windows-server-2003/cc728455(v=ws.10))
</dt> </dl>

 

 
