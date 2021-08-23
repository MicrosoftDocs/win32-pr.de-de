---
title: Hintergrundinformationen
description: Die Microsoft Active Accessibility-Komponente erstellt oleacc.dll Proxyobjekte, die IAccessible im Namen von Standardsteuerelementen Windows implementieren.
ms.assetid: c010af48-384c-40c0-ab52-c80b225502fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d154beb5d824bc722e713346129258c2d294d678a92c1b66d12035ce390f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052958"
---
# <a name="background-information"></a>Hintergrundinformationen

Die Microsoft Active Accessibility-Komponente erstellt oleacc.dll Proxyobjekte, die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) im Auftrag von Standardsteuerelementen Windows implementieren. Da diese Proxys standardbasierte Windows-Nachrichten und steuerelementspezifische APIs verwenden, um Informationen zu jedem Steuerelement zu sammeln, gab es keinen direkten Mechanismus zum Anpassen der Informationen, die diese Proxys über **IAccessible** verfügbar machen.

Derzeit können Sie eine vorhandene [**IAccessible-Implementierung**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) mithilfe von Unterklassen und Umbruchtechniken anpassen. Diese Techniken sind jedoch mühsam und fehleranfällig. Der Großteil des Codes, der geschrieben wurde, um eine oder zwei Eigenschaften zu überschreiben, betrifft die Implementierung von Unterklassen und Umschließen. nur ein kleiner Bruchteil führt die eigentliche Aufgabe aus, Informationen zu überschreiben. Dynamische Anmerkungen verbessern die Situation, indem sie ähnliche Funktionen bereitstellen, ohne dass Sie Unterklassen schreiben oder Code umschließen müssen. Stattdessen können Sie sich auf die Bereitstellung von Code konzentrieren, der die richtigen Informationen liefert. Mit der dynamischen Anmerkung können Entwickler Hinweise und andere nützliche Informationen an OLEACC übergeben, um die verfügbaren Informationen anzupassen. Diese Funktion allein reduziert die Kosten für die Microsoft Active Accessibility und ermöglicht Entwicklern, den Zugriff auf ihre Benutzeroberflächen deutlich zu verbessern.

 

 




