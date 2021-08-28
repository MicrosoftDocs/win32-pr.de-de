---
description: Das Startattribut gibt die Startzeit eines Objekts relativ zum übergeordneten Objekt an.
ms.assetid: 971de88e-c1ee-4e07-bf8e-3153e4fd11f3
title: start-Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 227b04a8cd7dc366a9cf10a4930233cd834e2bea7faa64bb59c248049b9e9abe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650990"
---
# <a name="start-attribute"></a>start-Attribut

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Das `start` -Attribut gibt die Startzeit eines Objekts relativ zum übergeordneten Objekt an.

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

 

 



