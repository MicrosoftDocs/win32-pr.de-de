---
description: Pack-Objekt
ms.assetid: e84a05a0-ea12-4bc1-83e1-1eb0dd291dc9
title: Pack-Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa8c565c45b802258b9d8b9955a2d28adc13c73c989805ce6b2663bc3006d7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058023"
---
# <a name="pack-object"></a>Pack-Objekt

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die [Windows Storage Verwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Ein Paketobjekt modelliert eine Datenträgergruppe, eine Sammlung von Datenträgern und Volumes, die vom Basis- oder dynamischen Softwareanbieter verwaltet werden. Ein Anbieter kann mehrere Paketobjekte enthalten.

Mithilfe der API können Anwendungen VDS anweisen, einem Paket einen oder mehrere Datenträger hinzuzufügen, die Datenträger an Volumes zu binden und die Datenträger optional als Einheit zwischen Hosts zu verschieben. Sie können ein vorhandenes Volume nicht in ein Paket importieren.

> [!Note]  
> Die Mitgliedschaft in einem Paket impliziert keine Konsistenz zwischen Datenträgern in Bezug auf Leistung, Medien, Verbindungsprotokoll oder andere Merkmale.

 

Datenträgerobjekte sind entweder nicht zugeordnet und werden von VDS verwaltet, oder sie sind Mitglieder genau eines Pakets. Der Basic-Softwareanbieter kann über null oder mehr Pakete verfügen, die jeweils einen einzelnen Basisdatenträger enthalten. Der Anbieter erzwingt keine Grenzwerte für die Anzahl der Volumes auf einem Basisdatenträger. Der dynamische Anbieter kann null oder mehr Pakete mit mehreren dynamischen Datenträgern in jedem Paket enthalten. Dieser Anbieter schränkt die Anzahl der Volumes auf einem Datenträger basierend auf der Größe von einem Megabyte der LDM-Datenbank (Logical Disk Manager) ein. Da ein Volume über mindestens einen Plex- und einen Datenträgerumfang verfügt, beträgt die maximale Anzahl von Volumes für ein Paket ungefähr 1.000. Die maximale Anzahl sinkt, wenn die Anzahl der Datenträger steigt.

Zusätzlich zu Datenträgerobjekten kann ein Paket mindestens ein LUN-Objekt enthalten, das von einem oder mehreren Hardwareanbietern implementiert wird. Für den Windows Kernel ist eine LUN nur ein anderer Datenträger. (LUN-Objekte müssen für den Computer, der das Anbieterprogramm ausführt, maskiert werden.) Wenn der Datenträger eine LUN ist, macht das LUN-Objekt sowohl die [**IVdsLun-**](/windows/desktop/api/Vds/nn-vds-ivdslun) als auch [**die IVdsDisk-Schnittstelle**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) verfügbar. Ein Paketobjekt verwendet **IVdsDisk** anstelle von **IVdsLun**, um die LUNs in einem Paket aufzuzählen. Eine ausführlichere Beschreibung einer LUN finden Sie im [LUN-Objekt](lun-object.md).

Die folgende Abbildung zeigt ein Paket mit zwei Membern: einem Datenträger und einer LUN. Eine Anwendung kann diese Objekte einem Onlinepaket hinzufügen und ein Volume auf der Grundlage des zugrunde liegenden Datenträgers und der Laufwerkseinheiten erstellen, die durch Spindeln dargestellt werden.

![Diagramm, das ein "Pack" mit einem Datenträger und einer LUN zeigt, die von einer Anwendung hinzugefügt wird, um ein Volume zu erstellen, das durch "Laufwerk" und "Spindel" dargestellt wird.](images/vdsdisksareluns.png)

Verwenden Sie die [**IVdsSwProvider::CreatePack-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) um ein neues Paketobjekt zu erstellen. Aufrufer können einen Zeiger auf ein bestimmtes Paket abrufen, indem sie das gewünschte Paketobjekt aus der Enumeration auswählen, die von der [**IVdsSwProvider:: QueryPacks-Methode**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) zurückgegeben wird. Mit einem Paketobjekt können Sie die Member eines Pakets hinzufügen, entfernen oder ersetzen. Wenn Sie einem Paket ein Datenträgerobjekt hinzufügen, initialisiert VDS einen Datenträger, um die Bindung aller vorhandenen Volumes zu aufheben. Im Gegensatz dazu behält eine LUN alle Bindungsdetails bei, wenn sie einem Paket hinzugefügt wird. Wenn Sie den letzten Datenträger aus einem Paket entfernen, löscht VDS das Paketobjekt, wenn der Aufrufer den letzten Verweis auf das Objekt freigibt.

Objekteigenschaften umfassen einen Objektbezeichner, einen Namen, den Paketstatus und Flags. Ein Onlinepaket steht zur Konfiguration und Verwendung zur Verfügung, ein Offlinepaket ist nicht verfügbar. VDS unterstützt eine beliebige Anzahl von Online- und Offlinepaketen.

**Windows Server 2003:** Unterstützt jeweils nur ein Onlinepaket.

VDS erzwingt ein Quorum von Onlinedatenträgern innerhalb eines Pakets. Das Quorum bestimmt, ob ein Paket einen Onlinestatus aufweisen kann, und verhindert, dass mehrere Hosts demselben Paket einen Onlinestatus gewähren. Wenn die Anzahl der Onlinedatenträger in einem Paket unter das Quorum (n/2 + 1) fällt, schalten VDS das Onlinepaket offline.

In der folgenden Tabelle sind verwandte Schnittstellen, Enumerationen und Strukturen aufgeführt.



| type                                              | Element                                                                                                |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| Schnittstellen, die immer von diesem Objekt verfügbar gemacht werden | [**IVdsPack**](/windows/desktop/api/Vds/nn-vds-ivdspack) und [**IVdsPack2**](/windows/desktop/api/Vds/nn-vds-ivdspack2) \* .                                     |
| Zugeordnete Enumerationen                           | [**VDS \_ PACK \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_pack_flag) und [**VDS PACK \_ \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_pack_status).             |
| Zugeordnete Strukturen                             | [**VDS \_ PACK \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) und [**VDS PACK \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification). |



 

**\* Windows Server 2003:** Diese Schnittstelle wird erst Windows Vista unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Softwareanbieterobjekte](software-provider-objects.md)
</dt> <dt>

[LUN-Objekt](lun-object.md)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> </dl>

 

 
