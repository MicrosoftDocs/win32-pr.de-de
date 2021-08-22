---
description: Enthält ein -Objekt für jede Abonnenteneigenschaft für die übergeordnete TransientSubscriptions-Auflistung. Vorübergehende Abonnements können für ausgeführte Objektinstanzen im laufenden Betrieb erstellt werden, und sie verschwinden, wenn das Objekt zerstört wird.
ms.assetid: b4f003b0-db9d-45f1-a57d-3e4d321289ca
title: TransientSubscriberProperties-Auflistung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriberProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: c29865978f65bb0f512e8b55ef9c5ad4bb1755d77bc322d5b0c34603702f3794
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119372700"
---
# <a name="transientsubscriberproperties-collection"></a>TransientSubscriberProperties-Auflistung

Enthält ein -Objekt für jede Abonnenteneigenschaft für die übergeordnete [**TransientSubscriptions-Auflistung.**](transientsubscriptions.md) Vorübergehende Abonnements können für ausgeführte Objektinstanzen im laufenden Betrieb erstellt werden, und sie verschwinden, wenn das Objekt zerstört wird.

Diese Auflistung unterstützt die [**Add-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) und [**Remove-Methoden**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) des [**COMAdminCatalogCollection-Objekts.**](comadmincatalogcollection.md)

## <a name="members"></a>Member

Die **TransientSubscriberProperties-Auflistung** erbt von der [**IUnknown-Schnittstelle,**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) verfügt aber nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**Propertyinfo**](propertyinfo.md)
-   [**RelatedCollectionInfo**](relatedcollectioninfo.md)

Sie können aus den folgenden Sammlungen zu dieser Sammlung navigieren:

-   [**TransientSubscriptions**](transientsubscriptions.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject-Objekt**](comadmincatalogobject.md) in der Auflistung unterstützt:

-   [Name](#name)
-   [Wert](#value)

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Name der Eigenschaft. Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Key-**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) oder [**Name-Eigenschaftsmethode**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) für ein Objekt dieser Auflistung aufgerufen wird. |
| Zugriff         | WriteOnce                                                                                                                                                                                                                                                              |
| type           | String                                                                                                                                                                                                                                                                 |
| Standard        | "Neue Eigenschaft"                                                                                                                                                                                                                                                         |
| Mindestsystem | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="value"></a>Wert



| Eingabe | Wert |
|----------------|---------------------------|
| BESCHREIBUNG    | Ein -Wert für die -Eigenschaft. |
| Zugriff         | ReadWrite                 |
| type           | Variant                   |
| Standard        | Nicht zutreffend                       |
| Mindestsystem | Windows 2000              |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[COM+-Verwaltungssammlungen](com--administration-collections.md)
</dt> </dl>

 

 
