---
description: Der virtuelle Adressraum für einen Prozess ist der Satz von virtuellen Speicheradressen, die er verwenden kann. Der Adressraum für jeden Prozess ist privat und kann nur von anderen Prozessen aufgerufen werden, wenn er freigegeben wird.
ms.assetid: 747f9f53-a595-4f4b-8b81-3123d59edb2f
title: Virtueller Adressraum (Speicherverwaltung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a5c9b6aa7fce3be508cae2afd67767f9deaa25e1fe4aa38c4530529f64d7df7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040080"
---
# <a name="virtual-address-space-memory-management"></a>Virtueller Adressraum (Speicherverwaltung)

Der virtuelle Adressraum für einen Prozess ist der Satz von virtuellen Speicheradressen, die er verwenden kann. Der Adressraum für jeden Prozess ist privat und kann nur von anderen Prozessen aufgerufen werden, wenn er freigegeben wird.

Eine virtuelle Adresse stellt nicht den tatsächlichen physischen Speicherort eines Objekts im Arbeitsspeicher dar. Stattdessen verwaltet das System  eine Seitentabelle für jeden Prozess. Dabei handelt es sich um eine interne Datenstruktur, mit der virtuelle Adressen in die entsprechenden physischen Adressen übersetzt werden. Jedes Mal, wenn ein Thread auf eine Adresse verweist, übersetzt das System die virtuelle Adresse in eine physische Adresse.

Der virtuelle Adressraum für 32-Bit-Windows ist 4 Gb groß und in zwei Partitionen unterteilt: eine für die Verwendung durch den Prozess und die andere für die Verwendung durch das System. Weitere Informationen zum virtuellen Adressraum in 64-Bit-Windows finden Sie unter Virtueller Adressraum [in 64-Bit-Windows](../winprog64/virtual-address-space.md).

Weitere Informationen zum virtuellen Arbeitsspeicher finden Sie in den folgenden Themen:

-   [Virtueller Adressraum und physische Storage](virtual-address-space-and-physical-storage.md)
-   [Arbeitssatz](working-set.md)
-   [Seitenstatus](page-state.md)
-   [Bereich des zugeordneten Arbeitsspeichers](scope-of-allocated-memory.md)
-   [Datenausführungsverhinderung](data-execution-prevention.md)
-   [Arbeitsspeicherschutz](memory-protection.md)
-   [Arbeitsspeicherlimits für Windows Releases](memory-limits-for-windows-releases.md)

## <a name="default-virtual-address-space-for-32-bit-windows"></a>Virtueller Standardadressenbereich für 32-Bit-Windows

Die folgende Tabelle zeigt den Standardspeicherbereich für jede Partition.



| Arbeitsspeicherbereich                             | Verbrauch                |
|------------------------------------------|----------------------|
| Niedrige 2 GB (0x00000000 bis 0x7FFFFFFF)  | Wird vom Prozess verwendet. |
| Hohe 2 GB (0x80000000 bis 0xFFFFFFFF) | Wird vom System verwendet.  |



 

## <a name="virtual-address-space-for-32-bit-windows-with-4gt"></a>Virtueller Adressraum für 32-Bit-Windows mit 4GT

Wenn [die Optimierung mit 4 GIGABYTE](4-gigabyte-tuning.md) (4GT) aktiviert ist, lautet der Arbeitsspeicherbereich für jede Partition wie folgt.



| Arbeitsspeicherbereich                             | Verbrauch                |
|------------------------------------------|----------------------|
| Niedrige 3 GB (0x00000000 bis 0xBFFFFFFF)  | Wird vom Prozess verwendet. |
| Hohe 1 GB (0xC0000000 bis 0xFFFFFFFF) | Wird vom System verwendet.  |



 

Nachdem 4GT aktiviert wurde, hat ein Prozess, für den das [**Flag IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) im Imageheader festgelegt ist, Zugriff auf die zusätzlichen 1 GB Arbeitsspeicher über den unteren 2 GB.

## <a name="adjusting-the-virtual-address-space-for-32-bit-windows"></a>Anpassen des virtuellen Adressraums für 32-Bit-Windows

Mit dem folgenden Befehl können Sie eine Starteintragsoption festlegen, mit der die Größe der Partition, die vom Prozess verwendet werden kann, auf einen Wert zwischen 2048 (2 GB) und 3072 (3 GB) konfiguriert wird:

[BCDEdit /set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *Megabytes*

Nachdem die Starteintragsoption festgelegt wurde, lautet der Arbeitsspeicherbereich für jede Partition wie folgt.



| Arbeitsspeicherbereich                            | Verbrauch                |
|-----------------------------------------|----------------------|
| Niedrig (0x00000000 bis *Megabyte)*    | Wird vom Prozess verwendet. |
| Hoch (*Megabyte +1* bis 0xFFFFFFFF) | Wird vom System verwendet.  |



 

**Windows Server 2003:** Legen Sie **den Schalter /USERVA** in boot.ini auf einen Wert zwischen 2048 und 3072 fest.

 

 
