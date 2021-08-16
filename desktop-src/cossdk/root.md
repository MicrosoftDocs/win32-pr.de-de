---
description: Enthält die Auflistungen der obersten Ebene im Katalog.
ms.assetid: 6cd23e6a-53b8-42ec-97df-59281f019252
title: Stammsammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Root
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0aba7a308a37ee531adf0886b8d06d4fd8c17369f73bd2bddf3211c2c184a4fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547017"
---
# <a name="root-collection"></a>Stammsammlung

Enthält die Auflistungen der obersten Ebene im Katalog. Sie enthält keine [**COMAdminCatalogObject-Objekte**](comadmincatalogobject.md) und unterstützt keine Eigenschaften.

Die **Root-Auflistung** unterstützt die [**Add-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) und [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts**](comadmincatalogcollection.md) nicht.

Sie können aus keiner Sammlung zur **Stammsammlung** navigieren.

## <a name="members"></a>Member

Die  Stammauflistung erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt aber nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Im Folgenden werden die Sammlungen der obersten Ebene im Katalog angezeigt:

-   [**ApplicationCluster**](applicationcluster.md)
-   [**ApplicationInstances**](applicationinstances.md)
-   [**Anwendungen**](applications.md)
-   [**ComputerList**](computerlist.md)
-   [**DCOMProtocols**](dcomprotocols.md)
-   [**EventClassesForIID**](eventclassesforiid.md)
-   [**FilesForImport**](filesforimport.md)
-   [**InprocServers**](inprocservers.md)
-   [**LegacyServer**](legacyservers.md)
-   [**LocalComputer**](localcomputer.md)
-   [**Partitionen**](partitions.md)
-   [**PartitionUsers**](partitionusers.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**TransientSubscriptions**](transientsubscriptions.md)
-   [**WOWInprocServers**](wowinprocservers.md)
-   [**WOWLegacyServers**](wowlegacyservers.md)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
