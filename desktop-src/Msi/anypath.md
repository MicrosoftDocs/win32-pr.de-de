---
description: Der AnyPath-Datentyp ist eine Textzeichenfolge, die entweder einen vollständigen oder einen relativen Pfad enthält.
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: AnyPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab5d8e7aaf4e92c2b33379b92b00263df07366ff340346aa19518478f8f2394
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045780"
---
# <a name="anypath"></a>AnyPath

Der AnyPath-Datentyp ist eine Textzeichenfolge, die entweder einen vollständigen oder einen relativen Pfad enthält. Wenn Sie einen relativen Pfad angeben, können Sie einen langen Dateinamen mit dem kurzen Dateinamen angeben, indem Sie die kurzen und langen Namen durch einen vertikalen Balken ( ) \| trennen. Beachten Sie, dass Sie auf diese Weise nicht mehrere Ebenen eines Verzeichnisses oder vollqualifizierter Pfade angeben können. Der Pfad kann Eigenschaften enthalten, die in eckige Klammern () eingeschlossen \[ \] sind.

Beispiele für gültige AnyPath-Daten:

-   \\\\server \\ share \\ temp
-   c: \\ temp
-   \\Temp
-   projec~1 \| Project Status

Beispiele für ungültige AnyPath-Daten:

-   c: \\ temp \\ projec~1 \| c: temp one Project \\ \\ Status
-   \\temp \\ projec~1 \| \\ temp one Project \\ Status

 

 



