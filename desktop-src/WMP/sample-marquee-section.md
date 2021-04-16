---
title: Beispiel Abschnitt "Marquee"
description: Beispiel Abschnitt "Marquee"
ms.assetid: 44ed3257-2e1a-4b8d-9d55-a13b0400422d
keywords:
- Windows Media Player Mobile Skins, marquees
- Skins, marquees
- Referenz für Skins, marquees
- marquees in Skins, Marquee (Abschnitt)
- Skin-Definitions Dateien, Marquee-Abschnitt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f66588d81b22051a9289a80c8733d5cfe154bed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471604"
---
# <a name="sample-marquee-section"></a>Beispiel Abschnitt "Marquee"

Die folgenden Zeilen zeigen einen typischen Marquee-Abschnitt einer Skin-Definitionsdatei:


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>

//  ----------   ------       -------      ------------------------

    3,2,234,20   Tahoma,12,N  255,0,0    Title+Author, Title, Author


```



Dadurch wird ein Marquee-Anzeige Feld definiert, das den Titel und den Autor anzeigt, wenn beide definiert sind, den Titel, wenn nur der Titel definiert ist, oder den Namen des Autors, wenn nur der Autor definiert ist. Wenn keines von beiden definiert ist, wird nichts angezeigt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Marquee**](marquee.md)
</dt> </dl>

 

 




