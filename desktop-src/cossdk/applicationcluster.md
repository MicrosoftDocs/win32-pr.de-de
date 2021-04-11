---
description: Enthält eine Liste der Server Computer im Anwendungs Cluster. Sie enthält ein-Objekt für jeden Server.
ms.assetid: 8722080a-cf95-4c29-9eb7-99c6df93611f
title: ApplicationCluster-Sammlung
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationCluster
api_type:
- COM
api_location: ''
ms.openlocfilehash: 00a54f5c79bcbaf4ef61b130db556fc27f264101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126596"
---
# <a name="applicationcluster-collection"></a>ApplicationCluster-Sammlung

Enthält eine Liste der Server Computer im Anwendungs Cluster. Sie enthält ein-Objekt für jeden Server. Dabei handelt es sich um eine Auflistung der obersten Ebene.

Der Anwendungs Cluster wird für Zwecke des CLB-Dienstanbieter (Component Load Balancing, Komponenten Lastenausgleich) definiert. Damit die Anwendungs Cluster Sammlung verwendet werden kann, muss der CLB-Dienst auf dem Computer installiert sein.

Sie legen einen Router im Anwendungs Cluster mit der isrouter-Eigenschaft für das [**LocalComputer**](localcomputer.md) -Sammlungsobjekt fest, und Sie legen fest, dass für eine bestimmte [**Komponente ein Lasten**](components.md) Ausgleich mit der LoadBalancingSupported-Eigenschaft eines komponentenauflistungs Objekts ausgeführt werden soll.

Diese Auflistung unterstützt die [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) -und [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) -Methoden des [**comadmincatalogcollection**](comadmincatalogcollection.md) -Objekts.

## <a name="members"></a>Member

Die **ApplicationCluster** -Auflistung erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.

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

### <a name="name"></a>Name



| Eingabe | Wert |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BESCHREIBUNG    | Der Name des Servers. Zusätzliche Leerzeichen am Anfang und Ende der Zeichenfolge werden entfernt. Diese Eigenschaft wird zurückgegeben, wenn die [**Schlüssel**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) -oder [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) -Eigenschaften Methode für ein Objekt dieser Auflistung aufgerufen wird. |
| Access         | WriteOnce                                                                                                                                                                                                                                                            |
| type           | String                                                                                                                                                                                                                                                               |
| Standard        | "Neuer Computer"                                                                                                                                                                                                                                                       |
| Minimalsystem | Windows 2000                                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Com+-Verwaltungs Sammlungen](com--administration-collections.md)
</dt> </dl>

 

 
