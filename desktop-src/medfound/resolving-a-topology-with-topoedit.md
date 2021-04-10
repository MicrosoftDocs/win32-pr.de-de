---
description: Auflösen einer Topologie mit topoedit
ms.assetid: da3e2bbc-7c9f-4a15-8842-c1bb00662cd2
title: Auflösen einer Topologie mit topoedit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8397e380b19a6f45736c06e859d2a80456aad079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215013"
---
# <a name="resolving-a-topology-with-topoedit"></a>Auflösen einer Topologie mit topoedit

Es gibt zwei Arten von Topologien:

-   Partielle Topologie. Der Quellknoten ist direkt mit dem Ausgabe Knoten verbunden. In einigen Fällen kann eine partielle Topologie über einige zwischen Transformations Knoten verfügen, z. b. Effekte, aber nicht alle. Die nicht ausgelassenen Transformations Knoten sind in der Regel Decoder oder Formatierungs-MFTs, wie z. b. Farb Konverter und audioresamplers.

-   Vollständige Topologie. Der Quellknoten ist über einen Transformations Knoten mit dem Ausgabe Knoten verbunden. Dieser Topologietyp muss über jeden Knoten verfügen, um Daten verarbeiten zu können.

Topoedit kann nur vollständige Topologien wiedergeben. Topoedit verwendet das von Media Foundation bereitgestellte topologieladeobjekt, um eine partielle Topologie in eine vollständige Topologie zu konvertieren, indem die erforderlichen Transformationen eingefügt werden. Der Prozess der Erstellung einer vollständigen Topologie wird als Auflösen einer Topologie bezeichnet.

Informationen zu Topologietypen finden Sie im Abschnitt partielle Topologien in Informationen [zu Topologien](about-topologies.md).

Bevor Sie eine Topologie auflösen, stellen Sie Folgendes sicher:

-   Die Topologie enthält einen Quellknoten und einen Ausgabe Knoten.

-   Der Quell-und der Ausgabe Knoten sind über eine gültige Knoten Verbindung verbunden. Während der topologieauflösung überprüft das topologielader den Medientyp der Knoten auf Kompatibilität. Wenn eine ungültige Knoten Verbindung vorhanden ist, schlägt der Prozess fehl, und es wird eine Fehlermeldung angezeigt.

Klicken Sie zum Auflösen einer Topologie im Menü **Topologie** auf **Topologie auflösen**.

Die Symbolleiste gibt den Status der Topologie an: **\[ aufgelöst \]** oder **\[ nicht aufgelöst \]**.

Wenn topoedit eine Topologie erfolgreich auflöst, wird der **topologiestatus** auf **\[ aufgelöst \]** festgelegt, und die Wiedergabe Steuerelemente werden aktiviert.

Jedes Mal, wenn Sie Änderungen an der Topologie vornehmen, wird der **topologiestatus** auf **\[ nicht aufgelöst \]** festgelegt, was darauf hinweist, dass er erneut aufgelöst werden muss.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von Topologien mithilfe von topoedit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[Topoedit](topoedit.md)
</dt> </dl>

 

 



