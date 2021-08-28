---
description: Das mstart-Attribut gibt die Startzeit eines Clips relativ zur ursprünglichen Mediendatei an.
ms.assetid: ed63f448-8ca3-4733-afc0-2d743f82bebe
title: mstart-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c65ffcb7d3da41f3e1f1232e37a6f5786755980eb63a8bbc554bbe726f453e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050950"
---
# <a name="mstart-attribute"></a>mstart-Attribut

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Das `mstart` -Attribut gibt die Startzeit eines Clips relativ zur ursprünglichen Mediendatei an.

## <a name="applies-to"></a>Gilt für

[**clip**](clip-element.md)

## <a name="possible-values"></a>Mögliche Werte

Muss eine Zeichenfolge im Format *hh:mm:ss.ff* sein, wobei *hh* = hours, *mm* = minutes, *ss* = seconds und *ff* = fractions of seconds ist. Beispiel: 1:04:30.512. Führende Einheiten können weggelassen werden. Beispielsweise sind 3:00 (drei Minuten) und 45 (45 Sekunden) beide gültig.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



