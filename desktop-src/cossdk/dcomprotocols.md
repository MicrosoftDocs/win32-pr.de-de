---
description: Enthält eine Liste der Protokolle, die von DCOM verwendet werden sollen. Sie enthält ein Objekt für jedes Protokoll.
ms.assetid: f553ce01-39b6-4dc3-9696-978b390a5c7d
title: Dcomprotokolle-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DCOMProtocols
api_type:
- COM
api_location: ''
ms.openlocfilehash: 705940dae0f7ebe885db4c295714df538c56c705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483214"
---
# <a name="dcomprotocols-collection"></a>Dcomprotokolle-Sammlung

Enthält eine Liste der Protokolle, die von DCOM verwendet werden sollen. Sie enthält ein Objekt für jedes Protokoll.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.

## <a name="members"></a>Member

Die **dcomprotokolle** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

## <a name="related-collections"></a>Verwandte Auflistungen

Sie können von dieser Sammlung zu einer der folgenden Sammlungen navigieren:

-   [**ErrorInfo**](errorinfo.md)
-   [**PropertyInfo**](propertyinfo.md)
-   [**Relatedcollectioninfo**](relatedcollectioninfo.md)

Sie können von den folgenden Sammlungen aus zu dieser Sammlung navigieren:

-   [**Fasst**](root.md)

## <a name="properties"></a>Eigenschaften

Die folgenden Eigenschaften werden vom [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekt in der-Auflistung unterstützt:

-   [Name](#name)
-   [Order](#order)
-   [Protocolcode](#protocolcode)

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Name des Protokolls. Diese Eigenschaft wird zurückgegeben, wenn die [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | ReadWrite                                                                                                                                                   |
| type           | String                                                                                                                                                      |
| Standard        | "Neues Protokoll"                                                                                                                                              |
| Minimalsystem | Windows 2000                                                                                                                                                |



 

### <a name="order"></a>Auftrag



| Eingabe | Wert |
|----------------|-----------------------------------------|
| BESCHREIBUNG    | Die Reihenfolge, in der das Protokoll ausprobiert werden soll. |
| Access         | ReadWrite                               |
| type           | Long (0-65000)                          |
| Standard        | 0                                       |
| Minimalsystem | Windows 2000                            |



 

### <a name="protocolcode"></a>Protocolcode



| Eingabe | Wert |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Code, der die RPC-Protokoll Sequenz angibt. Die unterstützten Protokoll Codes umfassen Folgendes: ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ SPX. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | WriteOnce                                                                                                                                                                                                                                                                   |
| type           | String                                                                                                                                                                                                                                                                      |
| Standard        | ""                                                                                                                                                                                                                                                                          |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
