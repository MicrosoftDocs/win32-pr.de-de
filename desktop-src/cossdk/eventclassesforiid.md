---
description: Ruft Informationen zu Ereignis Klassen ab.
ms.assetid: 33a87692-cacf-4a1c-974e-8d0e20295333
title: Eventclassesforiid-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventClassesForIID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 635ff6e87d68bfdcb4e82a24673c4ced00a7f81d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126589"
---
# <a name="eventclassesforiid-collection"></a>Eventclassesforiid-Sammlung

Ruft Informationen zu Ereignis Klassen ab.

Die Verbindung zwischen Verleger und Abonnent wird von einem [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) -Objekt verwaltet, bei dem es sich um eine COM+-Komponente handelt, die die Schnittstellen und Methoden enthält, die von einem Verleger zum Auslösen von Ereignissen verwendet werden.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.

## <a name="members"></a>Member

Die **eventclassesforiid** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Fasst**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [Anwendung](#application)
-   [Bitness](#bitness)
-   [CLSID](#clsid)
-   [Beschreibung](#description)
-   [Isprivatecomponent](#isprivatecomponent)
-   [ProgID](#progid)

### <a name="application"></a>Application



| Eingabe | Wert |
|----------------|----------------------------------------------------------|
| BESCHREIBUNG    | Die GUID für die Anwendung, die die Ereignisklasse enthält. |
| Access         | ReadOnly                                                 |
| type           | String                                                   |
| Standard        | –                                                      |
| Minimalsystem | Windows XP                                               |



 

### <a name="bitness"></a>Bitness



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Stellt den binären bikretivität der Ereignisklasse dar. Auf Systemen, die 64-Bit-Windows verwenden, unterscheidet diese Eigenschaft zwischen 64-Bit-Komponenten und 32-Bit-Komponenten. |
| Access         | ReadOnly                                                                                                                                                                |
| type           | Lange mögliche Werte: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)                                                                                           |
| Standard        | –                                                                                                                                                                     |
| Minimalsystem | Windows XP                                                                                                                                                              |



 

### <a name="clsid"></a>CLSID



| Eingabe | Wert |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Die GUID für die Ereignisklasse. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                                      |
| type           | String                                                                                                                                                        |
| Standard        | –                                                                                                                                                           |
| Minimalsystem | Windows XP                                                                                                                                                    |



 

### <a name="description"></a>BESCHREIBUNG



| Eingabe | Wert |
|----------------|----------------------------|
| BESCHREIBUNG    | Beschreibt die-Ereignisklasse. |
| Access         | ReadOnly                   |
| type           | String                     |
| Standard        | ""                         |
| Minimalsystem | Windows XP                 |



 

### <a name="isprivatecomponent"></a>Isprivatecomponent



| Eingabe | Wert |
|----------------|---------------------------------------------------------|
| BESCHREIBUNG    | Gibt an, ob die Ereignis Klassen Komponente privat ist. |
| Access         | ReadOnly                                                |
| type           | Bool                                                    |
| Standard        | Falsch                                                   |
| Minimalsystem | Windows XP                                              |



 

### <a name="progid"></a>ProgID



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Ein Anzeige Name, der zum Identifizieren der Ereignisklasse verwendet wird. Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadOnly                                                                                                                                                                            |
| type           | String                                                                                                                                                                              |
| Standard        | ""                                                                                                                                                                                  |
| Minimalsystem | Windows XP                                                                                                                                                                          |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
