---
description: Enthält ein-Objekt für jeden Partitions Benutzer.
ms.assetid: baec56ae-be8a-42a7-90bc-1db7c5cd7fe2
title: Partitionusers-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PartitionUsers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1521642879037938451decd873a9aa14211ce296
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343001"
---
# <a name="partitionusers-collection"></a>Partitionusers-Sammlung

Enthält ein-Objekt für jeden Partitions Benutzer.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.

## <a name="members"></a>Member

Die **partitionusers** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Fasst**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [AccountName](#accountname)
-   [Defaultpartitionid](#defaultpartitionid)

### <a name="accountname"></a>AccountName



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Name des Partitions Benutzerkontos. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | WriteOnce                                                                                                                                                                                                    |
| type           | String                                                                                                                                                                                                       |
| Standard        | "Neuer Benutzer"                                                                                                                                                                                                   |
| Minimalsystem | Windows Server 2003                                                                                                                                                                                          |



 

### <a name="defaultpartitionid"></a>Defaultpartitionid



| Eingabe | Wert |
|----------------|--------------------------------------------------------------------|
| BESCHREIBUNG    | Der Globally Unique Identifier für die Basis Anwendungs Partition. |
| Access         | ReadWrite                                                          |
| type           | String                                                             |
| Standard        | {41e90f 3E-56c1-4633-81c3-6e8bac8bdd70}                             |
| Minimalsystem | Windows Server 2003                                                |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
