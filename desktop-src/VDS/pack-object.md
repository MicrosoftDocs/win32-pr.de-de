---
description: Pack-Objekt
ms.assetid: e84a05a0-ea12-4bc1-83e1-1eb0dd291dc9
title: Pack-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b01978747df5ccc273a31ae2f516b35c01df96
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104568759"
---
# <a name="pack-object"></a>Pack-Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein Pack-Objekt modelliert eine Datenträger Gruppe, eine Sammlung von Datenträgern und Volumes, die vom Basic-oder dynamischen Softwareanbieter verwaltet werden. Ein Anbieter kann mehrere Paket Objekte enthalten.

Mithilfe der API können Anwendungen VDS anweisen, einem Paket einen oder mehrere Datenträger hinzuzufügen, die Datenträger an Volumes zu binden und die Datenträger optional als Einheit zwischen den Hosts zu verschieben. Sie können ein vorhandenes Volume nicht in ein Paket importieren.

> [!Note]  
> Die Mitgliedschaft in einem Paket impliziert nicht die Konsistenz zwischen Datenträgern in Bezug auf die Leistung, Medien, das Verbindungsprotokoll oder andere Merkmale.

 

Datenträger Objekte sind entweder nicht zugeordnet und werden von VDS verwaltet, oder Sie sind Mitglieder von genau einem Paket. Der Basic-Softwareanbieter kann über NULL oder mehr Pakete verfügen, die jeweils einen einzelnen Basis Datenträger enthalten. Die Anzahl der Volumes auf einem Basis Datenträger wird von dem Anbieter nicht beschränkt. Der dynamische Anbieter kann über 0 (null) oder mehr Pakete mit mehreren dynamischen Datenträgern in jedem Paket verfügen. Dieser Anbieter schränkt die Anzahl der Volumes auf einem Datenträger auf Grundlage der 1-Megabyte-Größe der LDM-Datenbank (Logical Disk Manager) ein. Wenn ein Volume über mindestens einen Plex-und einen Datenträger Block verfügt, beträgt die maximale Anzahl von Volumes für ein Paket ungefähr 1000. Die maximale Anzahl sinkt, wenn die Anzahl der Datenträger steigt.

Zusätzlich zu den Datenträger Objekten kann ein Paket ein oder mehrere LUN-Objekte enthalten, die von einem oder mehreren Hardwareanbietern implementiert werden. Für den Windows-Kernel ist eine LUN nur ein anderer Datenträger. (LUN-Objekte müssen auf dem Computer, auf dem das Anbieter Programm ausgeführt wird, nicht maskiert werden.) Wenn der Datenträger eine LUN ist, macht das LUN-Objekt sowohl die [**ivdslun**](/windows/desktop/api/Vds/nn-vds-ivdslun) -als auch die [**ivdsdisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) -Schnittstelle verfügbar. Ein Pack-Objekt verwendet **ivdsdisk** anstelle von **ivdslun**, um die LUNs in einem Paket aufzuzählen. Eine ausführlichere Beschreibung einer LUN finden Sie unter dem [LUN-Objekt](lun-object.md).

Die folgende Abbildung zeigt ein Paket mit zwei Membern: einem Datenträger und einer LUN. Eine Anwendung kann diese Objekte einem Online Paket hinzufügen und ein Volume aus den zugrunde liegenden Datenträgern erstellen und die durch Spindeln dargestellten Datenträger Blöcke erweitern.

![Diagramm, das ein "Pack" mit einem Datenträger und eine LUN anzeigt, die von einer Anwendung hinzugefügt wird, um ein Volume zu erstellen, das durch ein "Laufwerk" und "Spindel" dargestellt wird.](images/vdsdisksareluns.png)

Verwenden Sie die [**ivdsswprovider:: | atepack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) -Methode, um ein neues Pack-Objekt zu erstellen. Aufrufer können einen Zeiger auf ein bestimmtes Paket abrufen, indem Sie das gewünschte Paket Objekt aus der-Enumeration auswählen, das von der [**ivdsswprovider:: querypacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) -Methode zurückgegeben wird. Mit einem Pack-Objekt können Sie die Mitglieder eines Pakets hinzufügen, entfernen oder ersetzen. Wenn Sie einem Paket ein Datenträger Objekt hinzufügen, initialisiert VDS einen Datenträger, um die Bindung aller vorhandenen Volumes aufzuheben. Im Gegensatz dazu behält eine LUN alle Bindungs Details bei, wenn Sie zu einem Paket hinzugefügt wird. Wenn Sie den letzten Datenträger aus einem Paket entfernen, löscht VDS das Paket Objekt, wenn der Aufrufer den letzten Verweis auf das Objekt freigibt.

Zu den Objekteigenschaften gehören ein Objekt Bezeichner, ein Name, ein Paketstatus und Flags. Ein Online Pack ist für die Konfiguration und Verwendung verfügbar. ein Offline Paket ist nicht verfügbar. VDS unterstützt eine beliebige Anzahl von Online-und Offline Paketen.

**Windows Server 2003:** Unterstützt jeweils nur ein Online Paket.

VDS erzwingt ein Quorum von Online Datenträgern innerhalb eines Pakets. Das Quorum bestimmt, ob ein Paket einen Online Status aufweisen kann, und verhindert, dass mehrere Hosts dem gleichen Paket einen Online Status gewähren. Wenn die Anzahl der Online Datenträger in einem Paket unterhalb des Quorums (n/2 + 1) liegt, wird das Online Paket von VDS offline geschaltet.

In der folgenden Tabelle werden verwandte Schnittstellen, Enumerationen und Strukturen aufgelistet.



| type                                              | Element                                                                                                |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| Schnittstellen, die von diesem Objekt immer verfügbar gemacht werden | [**Ivdspack**](/windows/desktop/api/Vds/nn-vds-ivdspack) und [**IVdsPack2**](/windows/desktop/api/Vds/nn-vds-ivdspack2) \* .                                     |
| Zugehörige Enumerationen                           | [**VDS \_ \_Packflag**](/windows/desktop/api/Vds/ne-vds-vds_pack_flag) und [**VDS \_ Pack- \_ Status**](/windows/desktop/api/Vds/ne-vds-vds_pack_status).             |
| Zugeordnete Strukturen                             | [**VDS \_ Paket- \_ Prop**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) -und [**VDS-Paket- \_ \_ Benachrichtigung**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification). |



 

**\* Windows Server 2003:** diese Schnittstelle wird bis Windows Vista nicht unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Software Anbieter Objekte](software-provider-objects.md)
</dt> <dt>

[LUN-Objekt](lun-object.md)
</dt> <dt>

[**Ivdslun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[**Ivdsdisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> </dl>

 

 
