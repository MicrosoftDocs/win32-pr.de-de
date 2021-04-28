---
description: 'UsersInPartitionRole-Auflistung: Enthält ein Objekt für jeden Benutzer in der Rolle, mit der die Auflistung verknüpft ist.'
ms.assetid: c6aebf7a-04d1-4c7c-a015-bc6fb4841c4a
title: UsersInPartitionRole-Auflistung
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
ms.openlocfilehash: 2a4c134ebead08ef576337528a8ef75d8b8be21a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105548"
---
# <a name="usersinpartitionrole-collection"></a>UsersInPartitionRole-Auflistung

Enthält ein -Objekt für jeden Benutzer in der Rolle, mit der die Auflistung verknüpft ist.

Diese Auflistung unterstützt die [**Add-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) und [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Member

Die **UsersInPartitionRole-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt aber nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Sie können aus den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**RolesForPartition**](rolesforpartition.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [Benutzer](#usersinpartitionrole-collection)

### <a name="user"></a>Benutzer



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Benutzername. Diese Eigenschaft wird zurückgegeben, wenn die [**Key-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) oder [**Name-Eigenschaftsmethode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | WriteOnce                                                                                                                                                                             |
| type           | String                                                                                                                                                                                |
| Standard        | "Neuer Benutzer"                                                                                                                                                                            |
| Mindestsystem | Windows Server 2003                                                                                                                                                                   |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
