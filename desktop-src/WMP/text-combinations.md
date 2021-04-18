---
title: Text Kombinationen
description: Text Kombinationen
ms.assetid: 0220b77e-5f1e-4569-a8fe-5085e0c16338
keywords:
- Windows Media Player Mobile Skins, marquees
- Skins, marquees
- Referenz für Skins, marquees
- marquees in Skins, Text Kombinationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5668a9e18555b871c82bae7ed1826766ec9429e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515842"
---
# <a name="text-combinations"></a>Text Kombinationen

Bei diesem Wert handelt es sich um eine durch Kommas getrennte Liste von Text-Anzeige Feld Kombinationen. Textanzeige Felder können mit einem Pluszeichen verknüpft werden, um einen neuen Marquee-Anzeige Wert zu erstellen, und jeder Texttyp, der im Abschnitt "Texttyp" definiert ist, kann im Marquee verwendet werden.

Wenn Sie bestimmen, was angezeigt werden soll, wertet Windows Media Player Mobile jedes Element in der Liste aus, um festzustellen, ob alle Teile verfügbar sind. Wenn dies nicht der Fall ist, wird das nächste Element ausgewertet usw., bis alle verfügbaren Teile gefunden wurden. Wenn Sie z. b. Author und Title anzeigen möchten, aber nicht sicher sind, ob beides verfügbar ist, verwenden Sie den folgenden Wert:


```C++
Title+Author, Title, Author

```



Im vorherigen Beispiel wird der Titel + Author angezeigt, wenn der Titel und der Autor für das Medien Element definiert wurden. Wenn beides nicht definiert ist, wird der Titel ausgewertet und bei der Definition angezeigt. Wenn der Titel nicht definiert ist, wird der Autor angezeigt, wenn er definiert ist. Wenn keines von beiden definiert ist, wird nichts angezeigt.

Wenn Sie das Pluszeichen für die Verkettung verwenden, stellen Sie sicher, dass keine Leerzeichen auf beiden Seiten des Plus Zeichens vorhanden sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Marquee**](marquee.md)
</dt> <dt>

[**Texttyp**](text-type.md)
</dt> </dl>

 

 




