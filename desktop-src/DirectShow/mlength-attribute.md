---
description: Das mlength-Attribut gibt die Dauer einer Quelldatei an. Dieser Wert muss die tatsächliche Dauer sein, oder es können Renderingfehler auftreten.
ms.assetid: f33ce85c-df61-4248-8dea-677162fa1a07
title: mlength-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2aac65cd917fe99e296298bac425e0ff76ca18fc51c82e9294eaedf0ef1c23c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051150"
---
# <a name="mlength-attribute"></a>mlength-Attribut

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Das `mlength` -Attribut gibt die Dauer einer Quelldatei an. Dieser Wert muss die tatsächliche Dauer sein, oder es können Renderingfehler auftreten.

## <a name="applies-to"></a>Gilt für

[**clip**](clip-element.md)

## <a name="possible-values"></a>Mögliche Werte

Muss eine Zeichenfolge im Format *hh:mm:ss.ff* sein, wobei *hh* = hours, *mm* = minutes, *ss* = seconds und *ff* = fractions of seconds ist. Beispiel: 1:04:30.512. Führende Einheiten können weggelassen werden. Beispielsweise sind 3:00 (drei Minuten) und 45 (45 Sekunden) beide gültig.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaLength**](iamtimelinesrc-setmedialength.md)
</dt> </dl>

 

 



