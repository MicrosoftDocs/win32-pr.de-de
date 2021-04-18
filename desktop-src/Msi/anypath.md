---
description: Der anypath-Datentyp ist eine Text Zeichenfolge, die entweder einen vollständigen Pfad oder einen relativen Pfad enthält.
ms.assetid: fe8a4d2a-1960-40af-a0e4-4d65accdd388
title: Anypath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ab6265874616bb0bb1a2f61098cdbabfa8ea24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347547"
---
# <a name="anypath"></a>Anypath

Der anypath-Datentyp ist eine Text Zeichenfolge, die entweder einen vollständigen Pfad oder einen relativen Pfad enthält. Wenn Sie einen relativen Pfad angeben, können Sie einen langen Dateinamen mit dem kurzen Dateinamen einschließen, indem Sie die kurz-und lange Namen durch einen senkrechten Strich ( \| ) trennen. Beachten Sie, dass auf diese Weise nicht mehrere Ebenen eines Verzeichnisses oder voll qualifizierte Pfade angegeben werden können. Der Pfad kann Eigenschaften enthalten, die in eckigen Klammern () eingeschlossen sind \[ \] .

Beispiele für gültige anypath-Daten:

-   \\\\temporäre Server \\ Freigabe \\
-   c: \\ Temp
-   \\Temp
-   PROJEC ~ 1 \| Projekt Status

Beispiele für ungültige anypath-Daten:

-   c: \\ Temp \\ PROJEC ~ 1 \| c: \\ Temp ein \\ Projekt Status
-   \\Temp- \\ PROJEC ~ 1 \| \\ Temp ein \\ Projekt Status

 

 



