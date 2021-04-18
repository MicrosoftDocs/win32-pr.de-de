---
description: Enthält die Auflistungen der obersten Ebene im-Katalog.
ms.assetid: 6cd23e6a-53b8-42ec-97df-59281f019252
title: Stamm Sammlung
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
ms.openlocfilehash: ad896c69ab6fad75179c9bb30668143aa2ea741e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340109"
---
# <a name="root-collection"></a>Stamm Sammlung

Enthält die Auflistungen der obersten Ebene im-Katalog. Sie enthält keine [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekte oder unterstützt keine Eigenschaften.

Die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methode des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts wird **von der Stamm** Auflistung nicht unterstützt.

Sie können nicht von einer Auflistung **aus zur Stamm Sammlung navigieren** .

## <a name="members"></a>Member

Die **Stamm** Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Im folgenden finden Sie die Auflistungen der obersten Ebene im-Katalog:

-   [**ApplicationCluster**](applicationcluster.md)
-   [**ApplicationInstance**](applicationinstances.md)
-   [**Anwendungen**](applications.md)
-   [**Computer Liste**](computerlist.md)
-   [**Dcomprotokolle**](dcomprotocols.md)
-   [**Eventclassesforiid**](eventclassesforiid.md)
-   [**Filesforimport**](filesforimport.md)
-   [**Inprocservers**](inprocservers.md)
-   [**Legacyserver**](legacyservers.md)
-   [**LocalComputer**](localcomputer.md)
-   [**Partitionen**](partitions.md)
-   [**Partitionusers**](partitionusers.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)
-   [**Transientabonnements**](transientsubscriptions.md)
-   [**Wowinprocservers**](wowinprocservers.md)
-   [**Wowlegacyservers**](wowlegacyservers.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
