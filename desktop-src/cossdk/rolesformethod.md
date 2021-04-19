---
description: Enthält ein-Objekt für jede Rolle, die der Methode zugewiesen ist, mit der die Auflistung verknüpft ist. Die Rollen müssen bereits auf Anwendungsebene zugewiesen sein.
ms.assetid: 3a086163-e367-4dd1-996b-821b3e1111b2
title: Rolesformethod-Auflistung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForMethod
api_type:
- COM
api_location: ''
ms.openlocfilehash: c73ba5f7a14a5efc6711a65f211cd036e1c2a14d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346442"
---
# <a name="rolesformethod-collection"></a>Rolesformethod-Auflistung

Enthält ein-Objekt für jede Rolle, die der Methode zugewiesen ist, mit der die Auflistung verknüpft ist. Die Rollen müssen bereits auf Anwendungsebene zugewiesen sein.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.

## <a name="members"></a>Member

Die **rolesformethod** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Methodsforinterface**](methodsforinterface.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [Name](#name)

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Name der Rolle. Muss bereits eine Rolle sein, die der Anwendung zugewiesen ist (in der Rollen Auflistung angezeigt). Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | WriteOnce                                                                                                                                                                                                                                                                                                                                           |
| type           | String                                                                                                                                                                                                                                                                                                                                              |
| Standard        | "Neue Rolle"                                                                                                                                                                                                                                                                                                                                          |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
