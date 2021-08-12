---
description: Das Cutpointattribut gibt an, wann ein Übergang von einer Quelle zur nächsten schneidet, wenn der Übergang als Schnitt gerendert wird. Der Wert ist relativ zum Beginn des Übergangs.
ms.assetid: bdb0b8cd-025f-4b56-9cd4-f71c58ee809a
title: cutpoint-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7332d3ef1b608b192b18e0d32bc99bce547058754950847e0a9767eb500a1553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654591"
---
# <a name="cutpoint-attribute"></a>cutpoint-Attribut

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Das -Attribut gibt an, wann ein Übergang von einer Quelle zur nächsten schneidet, wenn der Übergang `cutpoint` als Schnitt gerendert wird. Der Wert ist relativ zum Beginn des Übergangs.

## <a name="possible-values"></a>Mögliche Werte

Muss eine Zeichenfolge im Format *hh:mm:ss.ff* sein, wobei *hh* = hours, *mm* = minutes, *ss* = seconds und *ff* = fractions of seconds ist. Beispiel: 1:04:30.512. Führende Einheiten können weggelassen werden. Beispielsweise sind 3:00 (drei Minuten) und 45 (45 Sekunden) beide gültig.

## <a name="applies-to"></a>Gilt für

[**Übergang**](transition-element.md)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XTL-Attribute](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md)
</dt> </dl>

 

 



