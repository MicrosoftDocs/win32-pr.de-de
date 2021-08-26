---
description: Die Roles-Auflistung ist immer mit einem Objekt in der Anwendungssammlung verknüpft. Sie enthält ein -Objekt für jede Rolle, die der Anwendung zugewiesen ist, mit der sie verknüpft ist.
ms.assetid: 87f39c2a-ad66-4390-9220-06751dcebd95
title: Rollensammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Roles
api_type:
- COM
api_location: ''
ms.openlocfilehash: 133477d82f718b992a628bde8af58f22d8d50a9e4974816c7c8f56be7ba8e33f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029470"
---
# <a name="roles-collection"></a>Rollensammlung

Die **Roles-Auflistung** ist immer mit einem Objekt in der [**Anwendungssammlung**](applications.md) verknüpft. Sie enthält ein -Objekt für jede Rolle, die der Anwendung zugewiesen ist, mit der sie verknüpft ist.

Diese Sammlung unterstützt die [**Add- und**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Member

Die **Roles-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Sammlungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)
-   [**UsersInRole**](usersinrole.md)

Sie können von den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**Anwendungen**](applications.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [Beschreibung](#description)
-   [Name](#name)

### <a name="description"></a>BESCHREIBUNG



| Eingabe | Wert |
|----------------|----------------------------|
| BESCHREIBUNG    | Eine Beschreibung der Rolle. |
| Zugriff         | ReadWrite                  |
| type           | String                     |
| Standard        | ""                         |
| Mindestsystem | Windows 2000               |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Name der Rolle. Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Key-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) oder [**Name-Eigenschaftsmethode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | WriteOnce                                                                                                                                                                                                                                                   |
| type           | String                                                                                                                                                                                                                                                      |
| Standard        | "Neue Rolle"                                                                                                                                                                                                                                                  |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
