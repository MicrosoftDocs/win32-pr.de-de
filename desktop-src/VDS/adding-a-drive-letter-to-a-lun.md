---
description: Hinzufügen eines Laufwerkbuchstabens zu einer LUN
ms.assetid: 3f350312-3f1f-4020-90d0-85521ea9c7c8
title: Hinzufügen eines Laufwerkbuchstabens zu einer LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 388c59a2e1b719e792855460f45fa0c04add7502f8e06aba56f0416a212a9aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755499"
---
# <a name="adding-a-drive-letter-to-a-lun"></a>Hinzufügen eines Laufwerkbuchstabens zu einer LUN

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Laufwerkbuchstaben können Volumeobjekten direkt zugewiesen werden. Wenn Ihr Datenträger jedoch ein LUN-Objekt ist, müssen Sie einige zusätzliche Schritte ausführen.

**So weisen Sie einem LUN-Objekt einen Laufwerkbuchstaben zu**

1.  Entmasken Sie die LUN bei Bedarf für den lokalen Host.
    > [!Note]  
    > Sie können keine Softwareverwaltungsvorgänge für ein LUN-Objekt ausführen, das innerhalb der aktuellen VDS-Sitzung für einen anderen Computer nicht maskiert ist.

     

2.  Rufen Sie [**die IVdsService::Reenumerate-Methode**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) auf dem Computer auf, auf dem der Hardwareanbieter ausgeführt wird.
3.  Initialisieren Sie die LUN wie folgt als Basisdatenträger:
    1.  Rufen Sie [**die IUnknown::QueryInterface-Methode**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für das LUN-Objekt auf, um eine Abfrage für die [**IVdsDisk-Schnittstelle**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) auszuführen.
    2.  Rufen Sie die [**IVdsSwProvider::CreatePack-Methode auf,**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) um ein Basispaket zu erstellen.
    3.  Rufen Sie die [**IVdsPack::AddDisk-Methode**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) auf, um den Datenträger dem neuen Paket hinzuzufügen.
4.  Erstellen Sie eine Partition auf dem Datenträger, und beziehen Sie das Volumeobjekt wie folgt:
    1.  Rufen Sie [**die IVdsCreatePartitionEx::CreatePartitionEx-Methode**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) auf, um eine Partition zu erstellen.
    2.  Rufen Sie [**die IVdsAsync::Wait-Methode**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) für das asynchrone Objekt auf, das von [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) zurückgegeben wird, um den Volumebezeichner aus der [**VDS \_ ASYNC \_ OUTPUT-Struktur**](/windows/desktop/api/Vds/ns-vds-vds_async_output) zu erhalten.
    3.  Übergeben Sie den Volumebezeichner als Parameter an die [**IVdsService::GetObject-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) um einen Volumeobjektzeiger zu erhalten.
5.  Rufen Sie die [**IVdsVolumeMF::AddAccessPath-Methode**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) auf, um den Laufwerkbuchstaben zu zuweisen.

> [!Note]  
> Die [**IVdsAdvancedDisk::AssignDriveLetter-Methode**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) weist Laufwerkbuchstaben Partitionen ohne zugeordnete Volumes zu, z. B. OEM- oder ESP-Partitionen. Sie können damit einem LUN-Objekt keinen Laufwerkbuchstaben zuweisen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von VDS](using-vds.md)
</dt> <dt>

[**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> <dt>

[**IVdsCreatePartitionEx::CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex)
</dt> <dt>

[**IVdsAsync::Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[**\_ASYNCHRONE \_ VDS-AUSGABE**](/windows/desktop/api/Vds/ns-vds-vds_async_output)
</dt> <dt>

[**IVdsVolumeMF::AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath)
</dt> <dt>

[**IVdsAdvancedDisk::AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter)
</dt> </dl>

 

 
