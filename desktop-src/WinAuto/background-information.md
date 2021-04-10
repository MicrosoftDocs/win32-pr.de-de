---
title: Hintergrundinformationen
description: Die Microsoft Active Accessibility-Komponente, oleacc.dll, erstellt Proxy Objekte, die im Namen von standardmäßigen Windows-Steuerelementen IAccessible implementieren.
ms.assetid: c010af48-384c-40c0-ab52-c80b225502fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0a9b044f8035a474f02b8457dc99ec39aca73c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100650"
---
# <a name="background-information"></a>Hintergrundinformationen

Die Microsoft Active Accessibility-Komponente, oleacc.dll, erstellt Proxy Objekte, die im Namen von standardmäßigen Windows-Steuerelementen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementieren. Da diese Proxys standardmäßige Windows-Meldungen und Steuerelement spezifische APIs verwenden, um Informationen zu jedem Steuerelement zu sammeln, gibt es keinen direkten Mechanismus zum Anpassen der Informationen, die diese Proxys über **iaccess verfügbar** machen.

Derzeit können Sie eine vorhandene [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Implementierung mithilfe von Unterklassen und Umbrüchen anpassen. Diese Techniken sind jedoch mühsam und fehleranfällig. Tatsächlich ist der Großteil des Codes, der zum Überschreiben von einer oder zwei Eigenschaften geschrieben wird, mit der Implementierung von Unterklassen und Wrapping verbunden. nur ein kleiner Bruchteil führt die eigentliche Aufgabe der Überschreibung von Informationen aus. Durch die dynamische Anmerkung wird die Situation verbessert, indem ähnliche Funktionen bereitgestellt werden, ohne dass Sie eine Unterklassen-oder Wrapping Code schreiben müssen. Stattdessen können Sie sich auf die Bereitstellung von Code konzentrieren, der die richtigen Informationen liefert. Die dynamische Anmerkung ermöglicht Entwicklern, Hinweise und andere nützliche Informationen an oleacc zu übergeben, um die Informationen anzupassen, die Sie verfügbar macht. Diese Funktion allein reduziert die Kosten für die Unterstützung von Microsoft Active Accessibility und ermöglicht Entwicklern, den Zugriff auf die Benutzeroberflächen erheblich zu verbessern.

 

 




