---
description: Dieses Attribut misst, wie weit die Statusanzeigeleiste gefüllt ist.
ms.assetid: d2b64cdf-e0b4-4c92-9cce-7f50753b875f
title: Statussteuerelementattribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a867772ff1452087ab22da76d3c1f93aea32e5ad50bd23ffe8ace62889086781
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074630"
---
# <a name="progress-control-attribute"></a>Statussteuerelementattribut

Dieses Attribut misst, wie weit die Statusanzeigeleiste gefüllt ist. Der Datensatz enthält zwei ganze Zahlen und eine Zeichenfolge. Die erste Zahl ist der Fortschritt, die zweite Zahl ist der Bereich (die maximal mögliche Zahl für den Fortschritt). Bei der Einstellung können die ganzen Zahlen als ganzzahlige Felder oder Zeichenfolgen eingegeben werden, die die ganzen Zahlen enthalten. Wenn die zweite Zahl fehlt, wird davon ausgegangen, dass sie die Standardzahl (1024) ist. Wenn der Fortschritt größer als der Bereich ist, wird er in den Bereich geändert. Das dritte Feld ist eine Zeichenfolge, der Name der Aktion, deren Status angezeigt wird.

Weitere Informationen finden Sie unter [Erstellen eines ProgressBar-Steuerelements](authoring-a-progressbar-control.md)und [Hinzufügen von benutzerdefinierten Aktionen zur ProgressBar.](adding-custom-actions-to-the-progressbar.md)

## <a name="valid-controls"></a>Gültige Steuerelemente

[Progressbar](progressbar-control.md)

## <a name="associated-bit-flags"></a>Zugeordnete Bitflags

Dieses Attribut verwendet keine Bitflags.

## <a name="remarks"></a>Hinweise

Weitere Informationen finden Sie unter [Steuerelementattribute](control-attributes.md) und das Steuerelement, das Sie unter [Steuerelemente](controls.md)erstellen müssen.

 

 



