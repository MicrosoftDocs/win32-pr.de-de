---
description: Eine Anwendung kann einen Pfad in einen Bereich konvertieren, indem Sie die pathtoregion-Funktion aufrufen.
ms.assetid: c4261516-7872-4118-99e2-138f0ac3c38a
title: Konvertierung von Pfaden in Regionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3a576f04035f6e29bb37a23de956322639daf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754473"
---
# <a name="conversion-of-paths-to-regions"></a>Konvertierung von Pfaden in Regionen

Eine Anwendung kann einen Pfad in einen Bereich konvertieren, indem Sie die [**pathtoregion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) -Funktion aufrufen. Wie bei [**selectclippath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath)ist **pathtor Egion** bei der Erstellung spezieller Grafikeffekte nützlich. Beispielsweise gibt es keine Funktionen, mit denen eine Anwendung einen Pfad Offset versetzen kann. Es gibt jedoch eine Funktion, die es einer Anwendung ermöglicht, einen Bereich ([**offsetrgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)) zu versetzen. Mit **pathtor Egion** , eine Anwendung kann die Wirkung der Animation einer komplexen Form erzeugen, indem Sie einen Pfad erstellt, der die Form definiert, den Pfad in einen Bereich umwandelt (durch Aufrufen von **pathtoregion**) und dann wiederholt den Bereich zeichnet, verschiebt und löscht (durch Aufrufen von Funktionen in einer Sequenz, z. [**b. fillrgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn), **offsetrgn** und **fillrgn**).

 

 



