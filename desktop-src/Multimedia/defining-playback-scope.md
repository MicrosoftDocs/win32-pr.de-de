---
title: Definieren des Wiedergabe Bereichs
description: Definieren des Wiedergabe Bereichs
ms.assetid: f2563226-7af1-4cb3-b468-c59738feeda2
keywords:
- Mciwndplayfrom-Makro
- Mciwndplayto-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518fc80588147c4ccbbca619452b714333a8a34d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947689"
---
# <a name="defining-playback-scope"></a>Definieren des Wiedergabe Bereichs

Mciwnd stellt Makros bereit, mit denen Sie den Wiedergabe *Bereich* definieren können. Der Bereich ist der Teil der Wiedergabe, den Sie wiedergeben möchten. Beispielsweise können Sie den Inhalt an einer anderen Position als der Anfangsposition wiedergeben, indem Sie das [**mciwndplayfrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom) -Makro verwenden. Dieses Makro wechselt an die angegebene Position, beginnt mit der Wiedergabe und wird bis zum Ende des Inhalts fortgesetzt. Entsprechend können Sie den Inhalt für einen angegebenen Endpunkt wiedergeben, indem Sie das [**mciwndplayto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto) -Makro verwenden. Dieses Makro beginnt an der aktuellen Wiedergabe Position und wird wiedergegeben, bis die angegebene Position erreicht oder das Ende des Inhalts erreicht ist, je nachdem, was zuerst eintritt.

Außerdem können Sie die Anfangs-und Endpositionen definieren, indem Sie das [**mciwndplayfromto**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto) -Makro verwenden. Dieses Makro wechselt an die angegebene Anfangsposition und wird wiedergegeben, bis die angegebene Endposition oder das Ende des Inhalts erreicht ist.

 

 




