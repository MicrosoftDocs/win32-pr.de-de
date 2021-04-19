---
description: Mit diesem Attribut wird gemessen, wie weit die Status Indikator Leiste ausgefüllt ist.
ms.assetid: d2b64cdf-e0b4-4c92-9cce-7f50753b875f
title: Fortschritts Steuerungs Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8854106ebacc8af2bdc0acfb58c5afc5d700df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360855"
---
# <a name="progress-control-attribute"></a>Fortschritts Steuerungs Attribut

Mit diesem Attribut wird gemessen, wie weit die Status Indikator Leiste ausgefüllt ist. Der Datensatz enthält zwei ganze Zahlen und eine Zeichenfolge. Die erste Zahl ist der Fortschritt, die zweite Zahl der Bereich (die maximal mögliche Anzahl für den Fortschritt). Bei der Einstellung können die ganzen Zahlen als ganzzahlige Felder oder Zeichen folgen eingegeben werden, die die ganzen Zahlen enthalten. Wenn die zweite Zahl fehlt, wird angenommen, dass es sich um den Standardwert (1024) handelt. Wenn der Fortschritt größer als der Bereich ist, wird er in den Bereich geändert. Das dritte Feld ist eine Zeichenfolge, der Name der Aktion, deren Status angezeigt wird.

Weitere Informationen finden Sie unter [Erstellen eines ProgressBar-Steuer](authoring-a-progressbar-control.md)Elements und [Hinzufügen von benutzerdefinierten Aktionen zu "ProgressBar](adding-custom-actions-to-the-progressbar.md)".

## <a name="valid-controls"></a>Gültige Steuerelemente

[ProgressBar](progressbar-control.md)

## <a name="associated-bit-flags"></a>Zugehörige Bitflags

Dieses Attribut verwendet keine Bitflags.

## <a name="remarks"></a>Bemerkungen

Siehe [Steuerelement Attribute](control-attributes.md) und das Steuerelement, das Sie unter Steuer [Elementen](controls.md)erstellen müssen.

 

 



