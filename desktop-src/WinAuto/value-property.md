---
title: Value-Eigenschaft
description: Die Value-Eigenschaft stellt eine Textdarstellung der visuellen Informationen in einem -Objekt zur Verfügung. Nicht alle Objekte unterstützen die Value-Eigenschaft.
ms.assetid: 89b99645-31f5-458a-ae61-a72bf1338195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcebf689016add11008b5d8249ce4eaa8adf4a99a406afea8d1267f01f94201f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133273"
---
# <a name="value-property"></a>Value-Eigenschaft

Die **Value-Eigenschaft** stellt eine Textdarstellung der visuellen Informationen in einem -Objekt zur Verfügung. Nicht alle Objekte unterstützen die **Value-Eigenschaft.**

Die **Value-Eigenschaft** wird durch Aufrufen von [**IAccessible::get \_ accValue abgerufen.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)

Die **Value-Eigenschaft** informiert den Client über die visuellen Informationen, die in einem -Objekt enthalten sind. Der Wert eines Bearbeitungssteuerelements ist beispielsweise der enthaltene Text, während ein Menüelement keinen Wert hat.

## <a name="providing-hierarchical-information"></a>Bereitstellen hierarchischer Informationen

Die **Value-Eigenschaft** stellt hierarchische Informationen in Fällen wie einem Strukturansicht-Steuerelement zur Verfügung. Obwohl das übergeordnete Objekt im Strukturansicht-Steuerelement keine Informationen in der **Value-Eigenschaft** enthält, verfügt jedes Element innerhalb des Steuerelements über einen nullbasierten Wert, der seine Ebene innerhalb der Hierarchie darstellt. Elemente der obersten Ebene haben den Wert 0 (null), Elemente der zweiten Ebene den Wert 1 und so weiter.

 

 




