---
title: Hilfsfunktionen für die Instanzerstellung
description: Hilfsfunktionen für die Instanzerstellung
ms.assetid: 0b9b7bcf-f0f0-42c4-945e-63a532640d4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84956f6040aaba13b46dea92bea611a49d5d8de3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039653"
---
# <a name="instance-creation-helper-functions"></a>Hilfsfunktionen für die Instanzerstellung

In früheren Versionen von com war der primäre Mechanismus, der zum Erstellen einer Objektinstanz verwendet wurde, die [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion. Diese Funktion kapselt den Prozess der Erstellung eines Klassen Objekts mithilfe dieses-Objekts, um eine neue-Instanz zu erstellen und das-Klassenobjekt freizugeben. Eine weitere Funktion dieser Art ist die spezifischere [**olecreate**](/windows/desktop/api/ole/nf-ole-olecreate), das OLE-Verbund Dokument-Hilfsprogramm, das ein Klassenobjekt erstellt und einen Zeiger auf ein angefordertes Objekt abruft.

Um den Prozess der Instanzerstellung auf verteilten Systemen zu glätten, hat com vier wichtige neue Instanzen Erstellungs Mechanismen eingeführt:

-   Klassenmoniker und [ **iclassactivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator)
-   [**Cokreateingestanceex**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [**Cogetinstancefromistorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)

Ein klassenmoniker ermöglicht es Ihnen, die Klasse eines Objekts zu identifizieren, und wird in der Regel mit einem anderen Moniker verwendet, wie z. b. einem dateimoniker, um den Speicherort des Objekts anzugeben. Dies ermöglicht es Ihnen, an ein Objekt zu binden und den Server anzugeben, der für dieses Objekt gestartet werden soll. Klassenmoniker können auch rechts von Monikern zusammengesetzt werden, die die Bindung an die [**iclassactivator**](/windows/desktop/api/ObjIdl/nn-objidl-iclassactivator) -Schnittstelle unterstützen. Weitere Informationen finden Sie unter [klassenmoniker](class-monikers.md).

[**Cokreateinstanceex**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) erweitert [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) so, dass es möglich ist, ein einzelnes nicht initialisiertes Objekt zu erstellen, das mit der angegebenen CLSID auf einem angegebenen Remote Computer verknüpft ist. Anstatt eine einzelne Schnittstelle anzufordern und einen einzelnen Zeiger auf diese Schnittstelle zu erhalten, können Sie mit **cokreateinstanceex** außerdem mehrere Schnittstellen Abfragen und (falls verfügbar) Zeiger auf Sie in einem einzigen Roundtrip abrufen, wodurch weniger Roundtrips zwischen Computern zulässig sind. Dadurch kann die Remote Objekt Interaktion wesentlich effizienter werden. Zu diesem Zweck verwendet die-Funktion ein Array von [**\_ multiqi**](/windows/win32/api/objidlbase/ns-objidlbase-multi_qi) -Strukturen.

Das Erstellen eines Objekts über [**cokreateinstanceex**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex) erfordert weiterhin, dass das Objekt durch einen Aufrufen einer der Initialisierungs Schnittstellen (z. b. [**IPersistStorage:: Load**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-load)) initialisiert wird. Die Hilfsfunktionen [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) und [**cogetinstancefromistorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) Kapseln sowohl die Instanzen Erstellungs Potenz von **cokreateinstanceex** als auch die Initialisierung, das erste aus einer Datei und das letztere aus einem Speicher.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen eines Objekts über ein Klassenobjekt](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 