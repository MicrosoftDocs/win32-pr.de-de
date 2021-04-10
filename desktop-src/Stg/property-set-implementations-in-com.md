---
title: Eigenschaften Satz Implementierungen in com
description: Eigenschaften Satz Implementierungen in com
ms.assetid: 52d7b534-f81a-4cc9-b5ea-9538bfff056c
keywords:
- Strukturierter Speicher, Verwendung von Eigenschafts Satz Verwendungen in com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8ee68fcd36958e0b7b0648e40f6e3c480f31d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948843"
---
# <a name="property-set-implementations-in-com"></a>Eigenschaften Satz Implementierungen in com

Obwohl das Potenzial für die Verwendung von persistenten Eigenschaften Sätzen nicht vollständig abgetippt ist, gibt es derzeit zwei primäre Verwendungsmöglichkeiten:

-   Speichern von Zusammenfassungs Informationen mit einem Objekt, z. b. einem Dokument
-   Übertragen von Eigenschafts Daten zwischen Objekten

COM-Eigenschaften Sätze wurden entwickelt, um Daten zu speichern, die für die Darstellung als eine Auflistung differenzierter Werte mit mittlerer Größenordnung geeignet sind. Datasets, die zu groß sind, um dies zu tun, sollten in separate Streams, Storages und/oder Eigenschafts Sätze unterteilt werden. Das Datenformat der com-Eigenschaften Gruppe war nicht dazu gedacht, einen Ersatz für eine Datenbank mit vielen kleinen Objekten bereitzustellen.

COM stellt Implementierungen der Eigenschaften Satz Schnittstellen für verschiedene Objekte zusammen mit drei Hilfsfunktionen bereit. Im folgenden Abschnitt werden einige Leistungsmerkmale dieser Implementierungen beschrieben. Weitere Informationen zu bestimmten Schnittstellen und zum erhalten eines Zeigers auf diese Schnittstellen finden Sie im Abschnitt com-Verweis:

-   [IPropertySetStorage – Implementierung der Verbund Datei](ipropertysetstorage-compound-file-implementation.md)

    Die Implementierung von Verbund Dateien, die die [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -und [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Schnittstellen bereitstellt, stellt auch die [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -und [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstellen bereit. Bei einer Implementierung der Verbund Datei von **IStorage** kann die **IPropertySetStorage** -Schnittstelle durch Aufrufen von [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))abgerufen werden.

-   [IPropertySetStorage – NTFS-Datei System Implementierung](ipropertysetstorage-ntfs-file-system-implementation.md)

    Die [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle und die [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) -Schnittstelle können auch für NTFS-Dateien abgerufen werden, die keine Verbund Dateien sind. Daher ist es möglich, diese Schnittstellen für alle Dateien auf einem NTFS-Volume zu erhalten.

-   [IPropertySetStorage – eigenständige Implementierung](ipropertysetstorage-stand-alone-implementation.md)

    Wenn diese Implementierung von [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) und [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) instanziiert wird, erhält Sie einen Zeiger auf ein Objekt, das die [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle unterstützt. Anschließend werden die Eigenschafts Satz-Speicher in diesem Speicher Objekt manipuliert. Folglich ist es möglich, auf Eigenschafts Sätze für jedes Objekt zuzugreifen und diese zu bearbeiten, das unterstützt.

-   [Überlegungen zur IPropertySetStorage-Implementierung](ipropertysetstorage-implementation-considerations.md)

    Beim Bereitstellen einer Implementierung der [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle müssen mehrere Probleme berücksichtigt werden. Informationen zu diesen *Implementierungs Überlegungen* finden Sie im Abschnitt com-Referenz.

Außerdem gibt es vier Hilfsfunktionen, die beim Umgang mit Eigenschaften helfen sollen, die aus einer Eigenschaft in den Arbeitsspeicher gelesen wurden (in eine [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur):

-   [**Propvariantinit**](/windows/desktop/api/PropIdl/nf-propidl-propvariantinit)
-   [**Propvariantclear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)
-   [**"Frepropvariantarray"**](/windows/win32/api/combaseapi/nf-combaseapi-freepropvariantarray)
-   [**Propvariantcopy**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantcopy)

In den folgenden Abschnitten werden Eigenschaften Satz Implementierungen in com ausführlicher erläutert:

-   [Verwalten von Eigenschafts Sätzen](managing-property-sets.md)
-   [Überlegungen zu Eigenschaften Gruppen](property-set-considerations.md)
-   [Speichern von Eigenschafts Sätzen](storing-property-sets.md)
-   [Leistungsmerkmale](performance-characteristics.md)
-   [Implementieren des Eigenschaften Satzes für Zusammenfassungs Informationen](implementing-the-summary-information-property-set.md)
-   [Überlegungen zur IPropertySetStorage-Implementierung](ipropertysetstorage-implementation-considerations.md)

 

 