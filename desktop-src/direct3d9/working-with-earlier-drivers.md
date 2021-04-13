---
description: In diesem Abschnitt werden Probleme aufgelistet, die bei der Arbeit mit Direct3D 9 für Treiber auftreten können, die für frühere Versionen von Direct3D als Direct3D 9 geschrieben wurden.
ms.assetid: 891198e8-6c45-4f03-99bb-e24a4082b0d8
title: Arbeiten mit früheren Treibern (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76567bc4778924835e20a476b03dc94ea77739fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392413"
---
# <a name="working-with-earlier-drivers-direct3d-9"></a>Arbeiten mit früheren Treibern (Direct3D 9)

In diesem Abschnitt werden Probleme aufgelistet, die bei der Arbeit mit Direct3D 9 für Treiber auftreten können, die für frühere Versionen von Direct3D als Direct3D 9 geschrieben wurden.

-   Beim Arbeiten mit einem T&L HAL-Gerät wird die Nebel Intensität berechnet, aber der absolute Wert Vorgang wird nicht auf diesen Wert angewendet. Stattdessen bleibt der Wert negativ, wenn dies der berechnete Wert ist. Die beste Möglichkeit, diese Situation zu vermeiden, ist die angemessene Einrichtung von Transformationen. Eine weniger bevorzugte Methode besteht darin, die Werte für "Nebel Start" und "Nebel" zu ändern, um Sie abzugleichen.

Um nach einem Direct3D 9-Treiber zu suchen, suchen Sie im DevCaps2-Member von D3DCAPS9 nach einem Wert ungleich 0 (null) für D3DDEVCAPS2 \_ Streamoffset. [](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmiertipps](programming-tips.md)
</dt> </dl>

 

 



