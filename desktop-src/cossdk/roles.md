---
description: Die Rollen Sammlung bezieht sich immer auf ein Objekt in der Anwendungs Auflistung. Sie enthält ein-Objekt für jede Rolle, die der Anwendung zugewiesen ist, mit der Sie verknüpft ist.
ms.assetid: 87f39c2a-ad66-4390-9220-06751dcebd95
title: Rollen Sammlung
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
ms.openlocfilehash: f676a53f5fe54e42ca2a489ad834b9c91e4e0ef5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214262"
---
# <a name="roles-collection"></a>Rollen Sammlung

Die **Rollen** Sammlung bezieht sich immer auf ein Objekt in der [**Anwendungs**](applications.md) Auflistung. Sie enthält ein-Objekt für jede Rolle, die der Anwendung zugewiesen ist, mit der Sie verknüpft ist.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.

## <a name="members"></a>Member

Die **Rollen** Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)
-   [**Usersinrole**](usersinrole.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Anwendungen**](applications.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [Beschreibung](#description)
-   [Name](#name)

### <a name="description"></a>BESCHREIBUNG



| Eingabe | Wert |
|----------------|----------------------------|
| BESCHREIBUNG    | Eine Beschreibung der Rolle. |
| Access         | ReadWrite                  |
| type           | String                     |
| Standard        | ""                         |
| Minimalsystem | Windows 2000               |



 

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Name der Rolle. Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | WriteOnce                                                                                                                                                                                                                                                   |
| type           | String                                                                                                                                                                                                                                                      |
| Standard        | "Neue Rolle"                                                                                                                                                                                                                                                  |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
