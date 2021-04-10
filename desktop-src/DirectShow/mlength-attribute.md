---
description: Das mlength-Attribut gibt die Dauer einer Quelldatei an. Dieser Wert muss die tatsächliche Dauer sein, oder es können Renderingfehler auftreten.
ms.assetid: f33ce85c-df61-4248-8dea-677162fa1a07
title: mlength-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eadc288e29d99df0e6af7f06e1404d86f6a938
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957696"
---
# <a name="mlength-attribute"></a>mlength-Attribut

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das- `mlength` Attribut gibt die Dauer einer Quelldatei an. Dieser Wert muss die tatsächliche Dauer sein, oder es können Renderingfehler auftreten.

## <a name="applies-to"></a>Gilt für

[**Techno**](clip-element.md)

## <a name="possible-values"></a>Mögliche Werte

Muss eine Zeichenfolge im Format " *hh: mm: SS. FF* " sein, wobei " *HH* = Hours, *mm* = Minutes, *SS* = seconds" und " *FF* = Sekundenbruchteile" sein muss. Beispiel: 1:04:30.512. Führende Einheiten können ausgelassen werden. Beispielsweise sind 3:00 (drei Minuten) und 45 (45 Sekunden) beide gültig.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**Iamtimelinesrc:: setmedialength**](iamtimelinesrc-setmedialength.md)
</dt> </dl>

 

 



