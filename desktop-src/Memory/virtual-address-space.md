---
description: Der virtuelle Adressraum für einen Prozess ist der Satz von virtuellen Speicheradressen, der verwendet werden kann. Der Adressraum für jeden Prozess ist privat, und von anderen Prozessen kann nicht darauf zugegriffen werden, es sei denn, er ist freigegeben.
ms.assetid: 747f9f53-a595-4f4b-8b81-3123d59edb2f
title: Virtueller Adressraum (Speicherverwaltung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6584d0404799e6b0e5ab343c7d8b39d7f8d741a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959083"
---
# <a name="virtual-address-space-memory-management"></a>Virtueller Adressraum (Speicherverwaltung)

Der virtuelle Adressraum für einen Prozess ist der Satz von virtuellen Speicheradressen, der verwendet werden kann. Der Adressraum für jeden Prozess ist privat, und von anderen Prozessen kann nicht darauf zugegriffen werden, es sei denn, er ist freigegeben.

Eine virtuelle Adresse stellt nicht den tatsächlichen physischen Speicherort eines Objekts im Arbeitsspeicher dar. Stattdessen behält das System eine *Seiten Tabelle* für jeden Prozess bei, bei dem es sich um eine interne Datenstruktur handelt, mit der virtuelle Adressen in die entsprechenden physischen Adressen übersetzt werden. Jedes Mal, wenn ein Thread auf eine Adresse verweist, übersetzt das System die virtuelle Adresse in eine physische Adresse.

Der virtuelle Adressraum für 32-Bit-Windows beträgt 4 Gigabyte (GB) und ist in zwei Partitionen unterteilt: eine für den Prozess und die andere für die Verwendung durch das System reserviert. Weitere Informationen zum virtuellen Adressraum in 64-Bit-Fenstern finden Sie unter [Virtueller Adressraum in 64-Bit-Fenstern](../winprog64/virtual-address-space.md).

Weitere Informationen zum virtuellen Arbeitsspeicher finden Sie in den folgenden Themen:

-   [Virtueller Adressraum und physischer Speicher](virtual-address-space-and-physical-storage.md)
-   [Arbeitssatz](working-set.md)
-   [Seiten Status](page-state.md)
-   [Bereich von zugewiesener Arbeitsspeicher](scope-of-allocated-memory.md)
-   [Datenausführungsverhinderung](data-execution-prevention.md)
-   [Arbeitsspeicherschutz](memory-protection.md)
-   [Arbeitsspeicher Grenzwerte für Windows-Releases](memory-limits-for-windows-releases.md)

## <a name="default-virtual-address-space-for-32-bit-windows"></a>Standardmäßiger virtueller Adressraum für 32-Bit-Windows

In der folgenden Tabelle wird der Standard Speicherbereich für jede Partition angezeigt.



| Speicherbereich                             | Verbrauch                |
|------------------------------------------|----------------------|
| Niedriges 2 GB (0x00000000 bis 0x7FFFFFFF)  | Wird vom-Prozess verwendet. |
| High 2 GB (0x80000000 bis 0xffffffff) | Wird vom System verwendet.  |



 

## <a name="virtual-address-space-for-32-bit-windows-with-4gt"></a>Virtueller Adressraum für 32-Bit-Windows mit 4GT

Wenn die [4-Gigabyte-](4-gigabyte-tuning.md) Optimierung (4GT) aktiviert ist, lautet der Speicherbereich für jede Partition wie folgt.



| Speicherbereich                             | Verbrauch                |
|------------------------------------------|----------------------|
| Niedrig 3 GB (0x00000000 bis 0xBFFFFFFF)  | Wird vom-Prozess verwendet. |
| Hoch 1 GB (0xC0000000 bis 0xffffffff) | Wird vom System verwendet.  |



 

Nach der Aktivierung von 4GT hat ein Prozess, bei dem das Flag für die [**Image \_ Datei mit \_ großen \_ Adressen \_**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) Werten in seinem Bild Header festgelegt wurde, Zugriff auf die zusätzlichen 1 GB Arbeitsspeicher über den unteren 2 GB.

## <a name="adjusting-the-virtual-address-space-for-32-bit-windows"></a>Anpassen des virtuellen Adressraums für 32-Bit-Windows

Sie können den folgenden Befehl verwenden, um eine Start Eintrags Option festzulegen, mit der die Größe der Partition konfiguriert wird, die für den Prozess zur Verfügung steht, um einen Wert zwischen 2048 (2 GB) und 3072 (3 GB) zu verwenden:

[Bcdedit/set](/windows-hardware/drivers/devtest/bcdedit--set) **Erhöhung** von *Megabytes*

Nachdem die Option Boot Entry festgelegt wurde, lautet der Arbeitsspeicher Bereich für jede Partition wie folgt.



| Speicherbereich                            | Verbrauch                |
|-----------------------------------------|----------------------|
| Niedrig (0x00000000 bis *Megabyte*)    | Wird vom-Prozess verwendet. |
| Hoch (*Megabytes*+ 1 bis 0xffffffff) | Wird vom System verwendet.  |



 

**Windows Server 2003:** Legen Sie den **Option/USERVA bei** -Schalter in boot.ini auf einen Wert zwischen 2048 und 3072 fest.

 

 
