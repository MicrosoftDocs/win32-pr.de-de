---
description: Hinzufügen eines Laufwerk Buchstabens zu einer LUN
ms.assetid: 3f350312-3f1f-4020-90d0-85521ea9c7c8
title: Hinzufügen eines Laufwerk Buchstabens zu einer LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426a4f3bf720b21a02462edde4a381012d2084d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347142"
---
# <a name="adding-a-drive-letter-to-a-lun"></a>Hinzufügen eines Laufwerk Buchstabens zu einer LUN

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Sie können volumeobjekten direkt Laufwerk Buchstaben zuweisen. Wenn Ihr Datenträger jedoch ein LUN-Objekt ist, sind einige zusätzliche Schritte erforderlich.

**So weisen Sie einem LUN-Objekt einen Laufwerk Buchstaben zu**

1.  Deaktivieren Sie ggf. die LUN auf dem lokalen Host.
    > [!Note]  
    > Sie können keine Software Verwaltungsvorgänge für ein LUN-Objekt ausführen, das in der aktuellen VDS-Sitzung auf einem anderen Computer unmaskiert ist.

     

2.  Rufen Sie die [**ivdsservice:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) -Methode auf dem Computer auf, auf dem der Hardware Anbieter ausgeführt wird.
3.  Initialisieren Sie die LUN als Basis Datenträger wie folgt:
    1.  Rufen Sie die [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode für das LUN-Objekt auf, um die [**ivdsdisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) -Schnittstelle abzufragen.
    2.  Rufen Sie die [**ivdsswprovider:: | atepack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) -Methode auf, um ein Basic Pack zu erstellen.
    3.  Rufen Sie die [**ivdspack:: adddisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) -Methode auf, um den Datenträger dem neuen Paket hinzuzufügen.
4.  Erstellen Sie eine Partition auf dem Datenträger, und rufen Sie das Volume-Objekt wie folgt ab:
    1.  Rufen Sie die [**ivdscreatepartitionex:: | atepartitionex**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) -Methode auf, um eine Partition zu erstellen.
    2.  Rufen Sie die [**ivdsasync:: Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait) -Methode für das Async-Objekt auf, das von " [**kreatepartitionex**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) " zurückgegeben wird, um den volumebezeichner aus der [**VDS- \_ Async- \_ Ausgabe**](/windows/desktop/api/Vds/ns-vds-vds_async_output) Struktur zu
    3.  Übergeben Sie den volumebezeichner als Parameter an die [**ivdsservice:: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) -Methode, um einen volumeobjektzeiger zu erhalten.
5.  Rufen Sie die [**ivdsvolumemf:: addaccesspath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) -Methode auf, um den Laufwerk Buchstaben zuzuweisen.

> [!Note]  
> Die [**ivdsadvanceddisk:: zuordtionsetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter) -Methode weist Partitionen ohne zugeordnete Volumes (z. b. OEM-oder ESP-Partitionen) Laufwerk Buchstaben zu. Sie können Sie nicht verwenden, um einem LUN-Objekt einen Laufwerk Buchstaben zuzuweisen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von VDS](using-vds.md)
</dt> <dt>

[**Ivdsservice:: REENUMERATE**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**Ivdsdisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[**Ivdsswprovider:: kreatepack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**Ivdspack:: adddisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> <dt>

[**Ivdscreatepartitionex:: kreatepartitionex**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex)
</dt> <dt>

[**Ivdsasync:: Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[**asynchrone VDS- \_ \_ Ausgabe**](/windows/desktop/api/Vds/ns-vds-vds_async_output)
</dt> <dt>

[**Ivdsvolumemf:: addaccesspath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath)
</dt> <dt>

[**Ivdsadvanceddisk:: zuder zutragplatte**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter)
</dt> </dl>

 

 
