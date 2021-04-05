---
title: Marquee-Abschnitt
description: Marquee-Abschnitt
ms.assetid: ff48c922-e6fc-4ba2-89ad-dcb34be0fea5
keywords:
- Windows Media Player Mobile Skins, marquees
- Skins, marquees
- Erstellen von Skins, Marquee section
- Schreiben von Code für Skins, Marquee (Abschnitt)
- marquees in Skins, Marquee (Abschnitt)
- Skin-Definitions Dateien, Marquee-Abschnitt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdf92a9f8ba3c1ca34559d355801d74ba6ed6382
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714519"
---
# <a name="marquee-section"></a>Marquee-Abschnitt

Der Marquee-Abschnitt enthält Informationen zum Marquee-Textfeld, in dem Scrolltext angezeigt wird:


```C++
[ Marquee ]

//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------
    100,150,100,20   Tahoma,12,N  255,0,0    Title+Author, Author, Title

```



Dadurch werden der Titel und der Autor des aktuellen Medien Elements angezeigt, obwohl Sie beliebige Texttypen im Marquee anzeigen können. Beispielsweise können Sie auch filename, Status und Wiedergabeliste in Ihrem Marquee einschließen.

> [!Note]  
> Um die Kompatibilität mit Versionen von Windows Media Player Mobile zu gewährleisten, die älter als Windows Media Player 10 Mobile sind, wird die Verwendung von "Marquis" in einer Skin-Definitionsdatei weiterhin als gültig betrachtet.

 

Weitere Informationen zum Abschnitt "Marquee" finden Sie unter [Marquee](marquee.md) in der Skin-Referenz.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben des Codes**](writing-the-code.md)
</dt> </dl>

 

 




