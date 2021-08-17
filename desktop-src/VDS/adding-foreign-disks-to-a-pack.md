---
description: Hinzufügen von Fremddatenträgern zu einem Paket
ms.assetid: 4018c742-1d23-47b9-a787-69bf8847b54a
title: Hinzufügen von Fremddatenträgern zu einem Paket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26b83dd76cdc3f1637c07d8d9d818fdaf61fb093151f23aea06f0e9c7f81d6a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755455"
---
# <a name="adding-foreign-disks-to-a-pack"></a>Hinzufügen von Fremddatenträgern zu einem Paket

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

In der Regel ist ein fremder Datenträger ein dynamischer Datenträger, der auf einem Computer zugeordnet und physisch auf einen anderen Computer verschoben wird. Jeder Datenträger, der zu einem anderen Paket als dem Onlinepaket gehört, wird jedoch als fremder Datenträger betrachtet, der zu einem fremden Datenträgerpaket gehört.

Für ein Fremdpaket ist das **VDS \_ PKF \_ FOREIGN-Flag** im **ulFlags-Member** der [**VDS \_ PACK \_ PROP-Struktur**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) festgelegt. Fremdpakete sind immer offline.

Im folgenden Verfahren wird beschrieben, wie Sie einen oder mehrere fremder Datenträger importieren.

**So importieren Sie einen oder mehrere fremder Datenträger**

1.  Verschieben Sie Datenträger auf den neuen Computer.
2.  Verwenden Sie auf dem neuen Computer die [**IVdsService::Reenumerate-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) um die Fremddatenträger zu installieren.
3.  Wählen Sie das Onlinepaket als Zielpaket aus, das die fremden Datenträger empfängt. Wenn kein Onlinepaket vorhanden ist, verwenden Sie die [**IVdsSwProvider::CreatePack-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) um ein neues leeres Paket zu erstellen.
4.  Verwenden Sie [**die IVdsPack::MigrateDisks-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) um die Datenträger in das neue dynamische Paket zu importieren.
5.  Verwenden Sie die [**IVdsSwProvider::QueryPacks-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) um die Pakete und [**IVdsPack::GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) zu aufzählen, um zu bestimmen, welches Paket jetzt das Onlinepaket ist.

Wenn Sie ein neues leeres Zielpaket erstellen, werden die fremden Datenträger nicht tatsächlich zu diesem Paket migriert. Stattdessen wird das Foreign Pack als online markiert, das **VDS \_ PKF \_ FOREIGN-Flag** für das Paket wird gelöscht (sodass das Paket nicht mehr fremd ist), und das erstellte Zielpaket wird verworfen.

> [!Note]  
> Verwenden Sie [**die IVdsPack::AddDisk-Methode,**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) um einem Paket nicht zugewiesene Datenträger (Datenträger, die nicht von einem Anbieter beansprucht werden) hinzuzufügen. Ein nicht zugewiesener Datenträger darf nicht fremd sein.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von VDS](using-vds.md)
</dt> <dt>

[**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks)
</dt> <dt>

[**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> </dl>

 

 
