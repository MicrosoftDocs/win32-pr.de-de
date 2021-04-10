---
title: Value-Eigenschaft
description: Die Value-Eigenschaft stellt eine Textdarstellung der visuellen Informationen dar, die in einem-Objekt enthalten sind. Die Value-Eigenschaft wird nicht von allen Objekten unterstützt.
ms.assetid: 89b99645-31f5-458a-ae61-a72bf1338195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6cd3ad86b9ce3a4fcc917fc4f49792adf432bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310152"
---
# <a name="value-property"></a>Value-Eigenschaft

Die **value** -Eigenschaft stellt eine Textdarstellung der visuellen Informationen dar, die in einem-Objekt enthalten sind. Die **value** -Eigenschaft wird nicht von allen Objekten unterstützt.

Die **value** -Eigenschaft wird durch Aufrufen von [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)abgerufen.

Die **value** -Eigenschaft teilt dem Client Informationen zu den visuellen Informationen zu, die in einem-Objekt enthalten sind. Beispielsweise ist der Wert eines Bearbeitungs Steuer Elements der enthaltene Text, während ein Menü Element keinen Wert besitzt.

## <a name="providing-hierarchical-information"></a>Bereitstellen hierarchischer Informationen

Die **value** -Eigenschaft stellt hierarchische Informationen in Fällen wie einem Strukturansicht-Steuerelement bereit. Obwohl das übergeordnete Objekt im Strukturansicht-Steuerelement keine Informationen in der **value** -Eigenschaft bereitstellt, verfügt jedes Element im Steuerelement über einen NULL basierten Wert, der die Ebene innerhalb der Hierarchie darstellt. Elemente der obersten Ebene haben den Wert 0 (null), Elemente der zweiten Ebene haben den Wert 1 usw.

 

 




