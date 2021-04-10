---
description: Das cutpoint-Attribut gibt an, wann ein Übergang von einer Quelle zum nächsten erfolgt, wenn der Übergang als Ausschneiden gerendert wird. Der Wert ist relativ zum Anfang des Übergangs.
ms.assetid: bdb0b8cd-025f-4b56-9cd4-f71c58ee809a
title: cutpoint-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd516bd67577906a0a06d8da692ffbd7563ce32f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124597"
---
# <a name="cutpoint-attribute"></a>cutpoint-Attribut

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das- `cutpoint` Attribut gibt an, wann ein Übergang von einer Quelle zum nächsten erfolgt, wenn der Übergang als Ausschneiden gerendert wird. Der Wert ist relativ zum Anfang des Übergangs.

## <a name="possible-values"></a>Mögliche Werte

Muss eine Zeichenfolge im Format " *hh: mm: SS. FF* " sein, wobei " *HH* = Hours, *mm* = Minutes, *SS* = seconds" und " *FF* = Sekundenbruchteile" sein muss. Beispiel: 1:04:30.512. Führende Einheiten können ausgelassen werden. Beispielsweise sind 3:00 (drei Minuten) und 45 (45 Sekunden) beide gültig.

## <a name="applies-to"></a>Gilt für

[**Übergang**](transition-element.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**Iamtimelinetrans:: setcutpoint**](iamtimelinetrans-setcutpoint.md)
</dt> </dl>

 

 



