---
title: Beispielabschnitt "Marquee"
description: Beispielabschnitt "Marquee"
ms.assetid: 44ed3257-2e1a-4b8d-9d55-a13b0400422d
keywords:
- Windows Media Player Mobile Skins, Marquees
- Skins, Marquees
- Referenz für Skins,Marquees
- Marquees in skins,Marquee section
- Skindefinitionsdateien,Abschnitt "Marquee"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f8a3e013bb3a09a06f03715f0e7c4914e8e8d344c55843a643d5b8a9bf0479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508120"
---
# <a name="sample-marquee-section"></a>Beispielabschnitt "Marquee"

Die folgenden Zeilen zeigen einen typischen Abschnitt "Marquee" einer Skindefinitionsdatei:


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>

//  ----------   ------       -------      ------------------------

    3,2,234,20   Tahoma,12,N  255,0,0    Title+Author, Title, Author


```



Dadurch wird ein Festzelt-Anzeigefeld definiert, in dem titel und author angezeigt werden, wenn beide definiert sind, den Titel, wenn nur Title definiert ist, oder den Namen des Autors, wenn nur Author definiert ist. Wenn keines von beiden definiert ist, wird nichts angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Marquee**](marquee.md)
</dt> </dl>

 

 




