---
description: Das Start-Attribut gibt die Startzeit eines Objekts relativ zum übergeordneten Objekt an.
ms.assetid: 971de88e-c1ee-4e07-bf8e-3153e4fd11f3
title: Start Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b377d0d83c86b981400a784904cf0423f0cca20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359451"
---
# <a name="start-attribute"></a>Start Attribut

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das- `start` Attribut gibt die Startzeit eines Objekts relativ zum übergeordneten Objekt an.

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

 

 



