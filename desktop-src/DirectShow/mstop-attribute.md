---
description: Das attribut mstop gibt die Beendigungszeit eines Clips relativ zur ursprünglichen Mediendatei an.
ms.assetid: 01559d29-9c7b-4842-a1f7-16552adbda43
title: mstop-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d432c3ed9ff80a9252def74fb553ed307668b36e660d96963baae0f4d0db04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072936"
---
# <a name="mstop-attribute"></a>mstop-Attribut

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Das `mstop` -Attribut gibt die Beendigungszeit eines Clips relativ zur ursprünglichen Mediendatei an.

## <a name="applies-to"></a>Gilt für

[**clip**](clip-element.md)

## <a name="possible-values"></a>Mögliche Werte

Muss eine Zeichenfolge im Format *hh:mm:ss.ff* sein, wobei *hh* = hours, *mm* = minutes, *ss* = seconds und *ff* = fractions of seconds ist. Beispiel: 1:04:30.512. Führende Einheiten können weggelassen werden. Beispielsweise sind 3:00 (drei Minuten) und 45 (45 Sekunden) gültig.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



