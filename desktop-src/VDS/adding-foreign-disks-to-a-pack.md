---
description: Hinzufügen von fremden Datenträgern zu einem Paket
ms.assetid: 4018c742-1d23-47b9-a787-69bf8847b54a
title: Hinzufügen von fremden Datenträgern zu einem Paket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fbfa2ff3d00857fd4e1b92e78f1760c25ce516b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349279"
---
# <a name="adding-foreign-disks-to-a-pack"></a>Hinzufügen von fremden Datenträgern zu einem Paket

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

In den meisten Fällen ist ein fremd Datenträger ein dynamischer Datenträger, der auf einem Computer zugeordnet und physisch auf einen anderen Computer verschoben wird. Alle Datenträger, die einem anderen Paket als dem Online Paket angehören, werden jedoch als fremd Datenträger betrachtet, der zu einem fremden Festplatten Paket gehört.

Ein Foreign Pack verfügt über das **VDS- \_ PKF- \_ Fremd** Kennzeichen, das im **ulflags** -Member der prop-Struktur des [**VDS- \_ Pakets \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop) festgelegt ist. Fremd Pakete sind immer offline.

Im folgenden Verfahren wird beschrieben, wie ein oder mehrere fremd Datenträger importiert werden.

**So importieren Sie einen oder mehrere fremd Datenträger**

1.  Verschieben Sie Datenträger auf den neuen Computer.
2.  Verwenden Sie auf dem neuen Computer die [**ivdsservice:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) -Methode, um die fremd Datenträger zu installieren.
3.  Wählen Sie das Online Paket als Ziel Paket aus, das die fremden Datenträger empfängt. Wenn kein Online Paket vorhanden ist, verwenden Sie die [**ivdsswprovider:: Deepack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) -Methode, um ein neues leeres Paket zu erstellen.
4.  Verwenden Sie die [**ivdspack:: MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) -Methode, um die Datenträger in das neue dynamische Paket zu importieren.
5.  Verwenden Sie die [**ivdsswprovider:: querypacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) -Methode zum Auflisten der Pakete und [**ivdspack:: GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) , um zu bestimmen, welches Paket nun das Online Paket ist.

Wenn Sie ein neues leeres Ziel Paket erstellen, werden die fremd Datenträger nicht tatsächlich zu diesem Paket migriert. Stattdessen ist das fremd Paket als Online gekennzeichnet, das **VDS \_ PKF- \_ Fremd** Kennzeichen für das Paket wird gelöscht (sodass das Paket nicht mehr fremd ist), und das von Ihnen erstellte Ziel Paket wird verworfen.

> [!Note]  
> Verwenden Sie die [**ivdspack:: adddisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) -Methode, um nicht zugeordnete Datenträger – Datenträger, die nicht von einem Anbieter beansprucht werden – einem Paket hinzuzufügen. Ein nicht zugeordneter Datenträger kann nicht fremd sein.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von VDS](using-vds.md)
</dt> <dt>

[**Ivdsservice:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**Ivdsswprovider:: kreatepack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**Ivdspack:: MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks)
</dt> <dt>

[**Ivdspack:: adddisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> </dl>

 

 
