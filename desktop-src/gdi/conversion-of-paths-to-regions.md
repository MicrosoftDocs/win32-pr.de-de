---
description: Eine Anwendung kann einen Pfad in eine Region konvertieren, indem sie die PathToRegion-Funktion aufruft.
ms.assetid: c4261516-7872-4118-99e2-138f0ac3c38a
title: Konvertierung von Pfaden in Regionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d404aa50669fe2349b3e39f172dd652ef765c9de8c615cde446e8540e6051bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062460"
---
# <a name="conversion-of-paths-to-regions"></a>Konvertierung von Pfaden in Regionen

Eine Anwendung kann einen Pfad in eine Region konvertieren, indem sie die [**PathToRegion-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) aufruft. Wie [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath)ist **PathToRegion** bei der Erstellung spezieller Grafikeffekte nützlich. Es gibt beispielsweise keine Funktionen, die es einer Anwendung ermöglichen, einen Pfad zu versetzen. Es gibt jedoch eine Funktion, die es einer Anwendung ermöglicht, einen Bereich [**(OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)) zu versetzen. Mit **PathToRegion** kann eine Anwendung den Effekt der Animation einer komplexen Form erstellen, indem sie einen Pfad erstellt, der die Form definiert, den Pfad in einen Bereich konvertiert (durch Aufrufen von **PathToRegion)** und dann den Bereich wiederholt zeichnet, bewegt und löscht (indem Funktionen in einer Sequenz aufgerufen werden, z. B. [**FillRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) **OffsetRgn** und **FillRgn**).

 

 



