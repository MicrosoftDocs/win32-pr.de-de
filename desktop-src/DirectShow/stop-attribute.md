---
description: Das Attribut "beenden" gibt die Endzeit eines Objekts relativ zum übergeordneten Objekt an.
ms.assetid: 1bda3472-abda-4672-9b82-311163e56fe0
title: Attribut "Ende"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6deb3f2a422cb8100da32c0427caf6436e72fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359449"
---
# <a name="stop-attribute"></a>Attribut "Ende"

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das- `stop` Attribut gibt die Endzeit eines Objekts relativ zum übergeordneten Objekt an.

## <a name="possible-values"></a>Mögliche Werte

Muss eine Zeichenfolge im Format " *hh: mm: SS. FF* " sein, wobei " *HH* = Hours, *mm* = Minutes, *SS* = seconds" und " *FF* = Sekundenbruchteile" sein muss. Beispiel: 1:04:30.512. Führende Einheiten können ausgelassen werden. Beispielsweise sind 3:00 (drei Minuten) und 45 (45 Sekunden) beide gültig.

## <a name="applies-to"></a>Gilt für

[**Clip**](clip-element.md), [**Effekt**](effect-element.md), [**Übergang**](transition-element.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**Iamtimelineobj:: setstartstation**](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



