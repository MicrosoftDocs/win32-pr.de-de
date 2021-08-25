---
title: Definieren des Wiedergabebereichs
description: Definieren des Wiedergabebereichs
ms.assetid: f2563226-7af1-4cb3-b468-c59738feeda2
keywords:
- MCIWndPlayFrom-Makro
- MCIWndPlayTo-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1853c74cc4115cee72e4253e339f934e73b8d8e7e223f1b91e9992969c4ce3f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785420"
---
# <a name="defining-playback-scope"></a>Definieren des Wiedergabebereichs

MCIWnd bietet Makros, mit denen Sie den Wiedergabebereich *definieren können.* Der Bereich ist der Teil der Wiedergabe, den Sie wiedergeben möchten. Beispielsweise können Sie den Inhalt mithilfe des [**MCIWndPlayFrom-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) von einer anderen Position als der Anfangsposition wieder geben. Dieses Makro wechselt an die angegebene Position, beginnt die Wiedergabe und fährt mit dem Ende des Inhalts fort. Auf ähnliche Weise können Sie den Inhalt mithilfe des [**MCIWndPlayTo-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) bis zu einem angegebenen Endpunkt wieder geben. Dieses Makro beginnt an der aktuellen Wiedergabeposition und wird abspielt, bis es die angegebene Position erreicht oder das Ende des Inhalts erreicht ist, was zuerst kommt.

Außerdem können Sie sowohl die Anfangs- als auch die Endposition mithilfe des [**MCIWndPlayFromTo-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) definieren. Dieses Makro wechselt zur angegebenen Anfangsposition und wird abspielt, bis die angegebene Endposition oder das Ende des Inhalts erreicht ist.

 

 




