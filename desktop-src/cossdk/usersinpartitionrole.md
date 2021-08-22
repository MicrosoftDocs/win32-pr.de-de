---
description: 'UsersInPartitionRole-Auflistung: Enthält ein -Objekt für jeden Benutzer in der Rolle, mit der die Sammlung verknüpft ist.'
ms.assetid: c6aebf7a-04d1-4c7c-a015-bc6fb4841c4a
title: UsersInPartitionRole-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInPartitionRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: d07c62fc6c6cc871f803b1f752201bd500e2705c3cfca272ff350ffd018f6018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499645"
---
# <a name="usersinpartitionrole-collection"></a>UsersInPartitionRole-Sammlung

Enthält ein -Objekt für jeden Benutzer in der Rolle, mit der die Auflistung verknüpft ist.

Diese Sammlung unterstützt die [**Add- und**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Member

Die **UsersInPartitionRole-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Sammlungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Sie können von den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**RolesForPartition**](rolesforpartition.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [Benutzer](#usersinpartitionrole-collection)

### <a name="user"></a>User



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Der Benutzername. Diese Eigenschaft wird zurückgegeben, wenn die [**Key-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) oder [**Name-Eigenschaftsmethode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | WriteOnce                                                                                                                                                                             |
| type           | String                                                                                                                                                                                |
| Standard        | "Neuer Benutzer"                                                                                                                                                                            |
| Mindestsystem | Windows Server 2003                                                                                                                                                                   |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
