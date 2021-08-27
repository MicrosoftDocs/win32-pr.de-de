---
description: Das Stop-Attribut gibt die Stoppzeit eines Objekts relativ zum übergeordneten Objekt an.
ms.assetid: 1bda3472-abda-4672-9b82-311163e56fe0
title: stop-Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f8ccae1ff4a9a067ccf8ee90438cfb87e3260d41a7fac009afb4b4153e4ddf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050171"
---
# <a name="stop-attribute"></a>stop-Attribut

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Das `stop` -Attribut gibt die Stoppzeit eines Objekts relativ zum übergeordneten Objekt an.

## <a name="possible-values"></a>Mögliche Werte

Muss eine Zeichenfolge im Format *hh:mm:ss.ff* sein, wobei *hh* = hours, *mm* = minutes, *ss* = seconds und *ff* = fractions of seconds ist. Beispiel: 1:04:30.512. Führende Einheiten können weggelassen werden. Beispielsweise sind 3:00 (drei Minuten) und 45 (45 Sekunden) beide gültig.

## <a name="applies-to"></a>Gilt für

[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



