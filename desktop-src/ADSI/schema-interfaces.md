---
title: Schemaschnittstellen
description: Schemaschnittstellen
ms.assetid: b3427202-352b-4b35-877e-d28fb3d3906a
ms.tgt_platform: multiple
keywords:
- Schemaschnittstellen ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dfa22a32a4d93c36a7419d48ea6127c2345ffdea62686147d1ba08c41ea7992
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770554"
---
# <a name="schema-interfaces"></a>Schemaschnittstellen

Der Schemacontainer enthält eine Reihe von Schemadefinitionen, die an einen Teil der Namespacestruktur des Anbieters angefügt sind. In der Regel verfügt jede Instanz eines Namespace über ein eigenes Schema. In der folgenden Abbildung definiert der ADSI-Beispielanbieter beispielsweise einen Schemacontainer in jedem der Stammknoten "Seattle" und "Toronto".

![Schemaeinschluss](images/schemacont.png)

Um eine ADSI-Implementierung für einen Anbieter zu erstellen, müssen Sie Schemaverwaltungsobjekte bereitstellen, die den zugrunde liegenden Namespace des Anbieters widerspiegeln und ADSI-Schemaschnittstellen unterstützen. Im Folgenden sind die ADSI-Schemaschnittstellen aufgeführt, die im Schemacontainer enthalten sind.

-   [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) stellt Verzeichnisdienstklassen dar.
-   [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) stellt Verzeichnisdiensteigenschaften dar, die einzelne oder mehrere Werte aufweisen.
-   [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) stellt den einzelnen VARIANT-Typ dar.

Von ADSI definierte Schnittstellen können bestimmte Eigenschaften und Syntaxen für Ihren Anbieter unterstützen. Anbieter können eine ADSI-Definition mithilfe der Methoden erweitern, die Eigenschaften erstellen und darauf zugreifen. Beispielsweise können Sie die Methoden der [**IADs-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iads) wie [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GetEx,**](/windows/desktop/api/Iads/nf-iads-iads-getex) [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) und [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex)verwenden. Anbieter können auch zusätzliche Eigenschaften über zusätzliche Schnittstellen unterstützen. Eine vollständige Liste der ADSI-Schnittstellen finden Sie unter [ADSI-Schnittstellen.](adsi-interfaces.md)

Eine ADSI-Anbieterkomponente mit einem komplexen Namespace lässt möglicherweise zu, dass mehrere Schemas in einer Namespaceinstanz vorhanden sind, die sich jeweils an einem anderen Teil der Struktur befinden. Die [**IADs::Schema-Eigenschaft**](iads-property-methods.md) eines Objekts benennt jedoch immer seine eigene Schemadefinition.

 

 




