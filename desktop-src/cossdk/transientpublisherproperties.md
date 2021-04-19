---
description: Enthält ein-Objekt für jede vorübergehende Verleger Eigenschaft für die übergeordnete transientabonnements-Auflistung. Vorübergehende Abonnements können dynamisch für das Ausführen von Objektinstanzen erstellt werden, und Sie verschwinden, wenn das Objekt zerstört wird.
ms.assetid: 63921caa-5c22-4203-b1a3-f143928f4742
title: Transientpublisherproperties-Auflistung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientPublisherProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 707cb974dce632c6eb5f65bc38f1fff8b779e54d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342606"
---
# <a name="transientpublisherproperties-collection"></a>Transientpublisherproperties-Auflistung

Enthält ein-Objekt für jede vorübergehende Verleger Eigenschaft für die übergeordnete [**transientabonnements**](transientsubscriptions.md) -Auflistung. Vorübergehende Abonnements können dynamisch für das Ausführen von Objektinstanzen erstellt werden, und Sie verschwinden, wenn das Objekt zerstört wird.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.

## <a name="members"></a>Member

Die **transientpublisherproperties** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Transientabonnements**](transientsubscriptions.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [Name](#name)
-   [Wert](#value)

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Den Namen der Eigenschaft. Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | WriteOnce                                                                                                                                                                                                                                                              |
| type           | String                                                                                                                                                                                                                                                                 |
| Standard        | "Neue Eigenschaft"                                                                                                                                                                                                                                                         |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                           |



 

### <a name="value"></a>Wert



| Eingabe | Wert |
|----------------|---------------------------|
| BESCHREIBUNG    | Ein-Wert für die-Eigenschaft. |
| Access         | ReadWrite                 |
| type           | Variant                   |
| Standard        | –                       |
| Minimalsystem | Windows 2000              |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
