---
description: Das Attribut stumm gibt den stumm Zustand des Objekts an.
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: stumm Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4e43feb16d75312cedd0caf5c217af2dd71332
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124898"
---
# <a name="mute-attribute"></a>stumm Attribut

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das `mute` -Attribut gibt den stumm Zustand des-Objekts an. Wenn der Wert **true** ist, wird weder das Objekt noch seine untergeordneten Elemente gerendert. Wenn der Wert **false** ist, wird das Objekt gerendert, und die untergeordneten Elemente werden entsprechend Ihrem eigenen stumm Zustand gerendert. Der Standardwert ist **FALSE**.

## <a name="possible-values"></a>Mögliche Werte

Die folgenden Werte sind als true definiert: y, y, t, t, 1. Die folgenden Werte sind als false definiert: n, n, f, f, 0 (null).

## <a name="applies-to"></a>Gilt für

[**Clip**](clip-element.md), zusammen [**gesetzte**](composite-element.md), [**Effekte**](effect-element.md), [**Gruppe**](group-element.md), [**Zeitachse**](timeline-element.md), [**Übergang**](transition-element.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**Iamtimelineobj:: setstumm**](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 



