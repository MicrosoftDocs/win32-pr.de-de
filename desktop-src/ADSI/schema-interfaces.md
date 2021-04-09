---
title: Schema Schnittstellen
description: Schema Schnittstellen
ms.assetid: b3427202-352b-4b35-877e-d28fb3d3906a
ms.tgt_platform: multiple
keywords:
- Schema Schnittstellen ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f414fdea2418fb92a0a3c8c9e8bf88eb6d7f00b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947333"
---
# <a name="schema-interfaces"></a>Schema Schnittstellen

Der Schema Container enthält einen Satz von Schema Definitionen, die an einen Teil der Namespace Struktur des Anbieters angefügt werden. In der Regel verfügt jede Instanz eines Namespace über ein eigenes Schema. In der folgenden Abbildung definiert z. b. der ADSI-Beispiel Anbieter einen Schema Container in jedem der Stamm Knoten "Seattle" und "Toronto".

![Schema Kapselung](images/schemacont.png)

Zum Erstellen einer ADSI-Implementierung für einen Anbieter müssen Sie Schema Verwaltungs Objekte bereitstellen, die den zugrunde liegenden Namespace des Anbieters widerspiegeln und die ADSI-Schema Schnittstellen unterstützen. Im folgenden finden Sie eine Liste der ADSI-Schema Schnittstellen, die im Schema Container enthalten sind.

-   [**Iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) stellt Verzeichnisdienst Klassen dar.
-   [**Iadsproperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) stellt Verzeichnisdienst Eigenschaften mit einzelnen oder mehreren Werten dar.
-   [**Iadssyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) stellt den einzelnen Variant-Typ dar.

Von ADSI definierte Schnittstellen können bestimmte Eigenschaften und Syntaxen für Ihren Anbieter unterstützen. Anbieter können eine ADSI-Definition mithilfe der Methoden erweitern, die Eigenschaften erstellen und aufrufen. Sie können z. b. die Methoden der [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle verwenden, z. b. [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**Getex**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) und [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex). Anbieter können zusätzliche Eigenschaften auch über zusätzliche Schnittstellen unterstützen. Eine umfassende Liste der ADSI-Schnittstellen finden Sie unter [ADSI-Schnittstellen](adsi-interfaces.md).

Eine ADSI-Anbieter Komponente mit einem komplexen Namespace kann möglicherweise mehrere Schemas in einer Namespace Instanz enthalten, die jeweils in einem anderen Teil der Struktur vorhanden sind. Die [**IADs:: Schema**](iads-property-methods.md) -Eigenschaft eines Objekts benennt jedoch immer seine eigene Schema Definition.

 

 




