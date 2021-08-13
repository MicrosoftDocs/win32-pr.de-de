---
description: Enthält ein -Objekt für jede Rolle, die der Komponente zugewiesen ist, mit der die Auflistung verknüpft ist. Die Rollen müssen bereits auf Anwendungsebene zugewiesen sein.
ms.assetid: c253c72f-908e-4990-ac1a-27e32c99283c
title: RolesForComponent-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: e0acd1bfd374c4d0cdb2eb43b49288f0527847abeec97d8bb96c0c5aecd74585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547007"
---
# <a name="rolesforcomponent-collection"></a>RolesForComponent-Sammlung

Enthält ein -Objekt für jede Rolle, die der Komponente zugewiesen ist, mit der die Auflistung verknüpft ist. Die Rollen müssen bereits auf Anwendungsebene zugewiesen sein.

Diese Sammlung unterstützt die [**Add- und**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Member

Die **RolesForComponent-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Sammlungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Sie können von den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**Komponenten**](components.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [Name](#name)

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschreibung    | Der Name der Rolle. Muss der Anwendung bereits eine Rolle zugewiesen sein (wird in der Sammlung Rollen angezeigt). Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Key-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) oder [**Name-Eigenschaftsmethode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | WriteOnce                                                                                                                                                                                                                                                                                                                                           |
| type           | String                                                                                                                                                                                                                                                                                                                                              |
| Standard        | "Neue Rolle"                                                                                                                                                                                                                                                                                                                                          |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
