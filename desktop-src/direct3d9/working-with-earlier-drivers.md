---
description: In diesem Abschnitt werden Probleme aufgeführt, die bei der Arbeit mit Direct3D 9 auf Treibern auftreten können, die für Versionen von Direct3D vor Direct3D 9 geschrieben wurden.
ms.assetid: 891198e8-6c45-4f03-99bb-e24a4082b0d8
title: Arbeiten mit früheren Treibern (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24284c706d49ce3294e23486f72150ffd74ee376e2be0d7d06dca09877eb7cc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796909"
---
# <a name="working-with-earlier-drivers-direct3d-9"></a>Arbeiten mit früheren Treibern (Direct3D 9)

In diesem Abschnitt werden Probleme aufgeführt, die bei der Arbeit mit Direct3D 9 auf Treibern auftreten können, die für Versionen von Direct3D vor Direct3D 9 geschrieben wurden.

-   Bei der Arbeit mit einem T&L CT-Gerät wird die Intensität der Intensität berechnet, aber der Vorgang mit absolutem Wert wird nicht auf diesen Wert angewendet. Stattdessen bleibt der Wert negativ, wenn dies berechnet wird. Die beste Möglichkeit, diese Situation zu vermeiden, ist die entsprechende Einrichtung von Transformationen. Eine weniger bevorzugte Methode ist es, die Übereinstimmung der Werte für "alle Start- und Endwerte" negativ zu machen.

Um nach einem Direct3D 9-Treiber zu suchen, suchen Sie im \_ DevCaps2-Mitglied [**von D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)nach einem Wert ungleich 0 (null) für D3DDEVCAPS2 STREAMOFFSET.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieren Tipps](programming-tips.md)
</dt> </dl>

 

 



