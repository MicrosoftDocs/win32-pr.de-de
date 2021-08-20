---
title: Textkombinationen
description: Textkombinationen
ms.assetid: 0220b77e-5f1e-4569-a8fe-5085e0c16338
keywords:
- Windows Media Player Mobile Skins, Marquees
- skins,marquees
- Referenz für Skins, Marquees
- Marquees in Skins, Textkombinationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0d937d0ae2f90fe37ea8f4af1208443bbb127d622a83ecb5f556ddff596824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117933418"
---
# <a name="text-combinations"></a>Textkombinationen

Bei diesem Wert handelt es sich um eine Liste von Textanzeigefeldkombinationen, die durch Kommas getrennt sind. Textanzeigefelder können durch ein Pluszeichen miteinander verknüpft werden, um einen neuen Markquee-Anzeigewert zu erstellen, und jeder im Abschnitt Texttyp definierte Texttyp kann in Ihrem Festzelt verwendet werden.

Wenn Sie bestimmen, was angezeigt werden soll, wertet Windows Media Player Mobile jedes Element in der Liste aus, um festzustellen, ob alle Teile verfügbar sind. Andernfalls wird das nächste Element ausgewertet usw., bis alle verfügbaren Teile gefunden wurden. Wenn Sie z. B. Autor und Titel anzeigen möchten, aber nicht sicher sind, ob beide verfügbar sind, verwenden Sie den folgenden Wert:


```C++
Title+Author, Title, Author

```



Im vorherigen Beispiel wird Titel+Autor angezeigt, wenn der Titel und der Autor für das Medienelement definiert wurden. Wenn beide nicht definiert sind, wird der Titel ausgewertet und angezeigt, wenn er definiert ist. Wenn der Titel nicht definiert ist, wird der Autor angezeigt, wenn er definiert ist. Wenn keines definiert ist, wird nichts angezeigt.

Wenn Sie das Pluszeichen für die Verkettung verwenden, stellen Sie sicher, dass auf beiden Seiten des Pluszeichens keine Leerzeichen vorhanden sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Marquee**](marquee.md)
</dt> <dt>

[**Texttyp**](text-type.md)
</dt> </dl>

 

 




