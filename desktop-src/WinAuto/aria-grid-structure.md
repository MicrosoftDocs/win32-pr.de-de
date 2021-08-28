---
title: ARIA-Rasterstrukturfehler
description: ARIA-Rasterstrukturfehler
ms.assetid: 8B2AEC98-1056-4560-AD6E-C6ECA0B94692
keywords:
- AriaGridStructureErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b91010417ed01f211859839ceab124b299b10679b3d460f860c03e5b2473f77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122380"
---
# <a name="aria-grid-structure-error"></a>ARIA-Rasterstrukturfehler

## <a name="text"></a>Text

Das Element mit der **Rasterrolle** hat keine entsprechende Rasterstruktur oder kein barrierefreies Markup.

## <a name="type"></a>type

Fehler

## <a name="description"></a>Beschreibung

Dieser Fehler gilt für benutzerdefinierte Elemente, für die das **Rollenattribut** auf "grid" festgelegt ist. Sie gilt nicht für HTML-Tabellentags, die die implizite **Rolle** "grid" haben.

Ein Element,  dessen Rollenattribut auf "grid" festgelegt ist, muss über die Struktur verfügen, die von der Rasterrolle Web Accessibility Initiative - Accessible Rich Internet Applications (CAB-ARIA) definiert wird, einschließlich des barrierefreien Namens für das Raster und seiner Headerunterelemente.

Um diesen Fehler zu beheben, überprüfen Sie Ihre Implementierung, um sicherzustellen, dass sie mit der SPEZIFIKATION VON CAB-ARIA übereinstimmt. Stellen Sie insbesondere sicher, dass die Struktur die folgenden Regeln erfüllt.

-   **grid** enthält **Zeilen-** oder **Zeilengruppenelemente.**
-   **rowgroup** enthält **Zeilenelemente.**
-   **Zeilenelemente** enthalten **Columnheader-** oder **gridcell-** oder **rowheader-Elemente.**

Ein barrierefreier Name sollte für **raster-,** **columnheader-,** **gridcell-** und **rowheader-Elemente** mit einem der folgenden Attribute definiert werden.

-   [**aria-labeldby-Attribut**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) zum Verweisen auf das Element, das Text enthält.
-   [**aria-label-Attribut,**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) um den barrierefreien Namen direkt festzulegen.
-   [**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) zum Erstellen einer QuickInfo, die gleichzeitig als Name verwendet wird.

 

 




