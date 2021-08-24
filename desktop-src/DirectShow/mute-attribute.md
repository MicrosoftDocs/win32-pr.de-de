---
description: Das Mute-Attribut gibt den Stummschaltungszustand des Objekts an.
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: Mute-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d89632e632ec4dbf0fe76a915e073baa769044fa1eaad455c16dd3065dc1c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791040"
---
# <a name="mute-attribute"></a>Mute-Attribut

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Das `mute` -Attribut gibt den Stummschaltungszustand des Objekts an. Wenn der Wert **TRUE** ist, werden weder das Objekt noch seine untergeordneten Elemente gerendert. Wenn der Wert **FALSE** ist, wird das Objekt gerendert, und seine untergeordneten Elemente werden entsprechend ihrem eigenen Stummschaltungszustand gerendert. Der Standardwert ist **FALSE**.

## <a name="possible-values"></a>Mögliche Werte

Die folgenden Werte sind als TRUE definiert: y, Y, t, T, 1. Die folgenden Werte sind als FALSE definiert: n, N, f, F, 0 (null).

## <a name="applies-to"></a>Gilt für

[**Clip,**](clip-element.md) [**zusammengesetzt,**](composite-element.md) [**Effekt,**](effect-element.md) [**Gruppe,**](group-element.md) [**Zeitachse,**](timeline-element.md) [**Übergang**](transition-element.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetMuted**](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 



