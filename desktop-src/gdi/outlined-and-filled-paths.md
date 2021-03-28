---
description: Eine Anwendung kann die Gliederung eines Pfades zeichnen, indem Sie die strokePath-Funktion aufruft. Sie kann das Innere eines Pfads durch Aufrufen der FillPath-Funktion ausfüllen und den Pfad durch Aufrufen der strokeandfillpath-Funktion umschließen und ausfüllen.
ms.assetid: e3e82676-3095-43f0-9fb4-959f925e66c2
title: Umrissene und gefüllte Pfade
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 735ee9ee5d7e69922241c5647b883e1800b525e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959306"
---
# <a name="outlined-and-filled-paths"></a>Umrissene und gefüllte Pfade

Eine Anwendung kann die Gliederung eines Pfades zeichnen, indem Sie die [**strokePath**](/windows/desktop/api/Wingdi/nf-wingdi-strokepath) -Funktion aufruft. Sie kann das Innere eines Pfads durch Aufrufen der [**FillPath**](/windows/desktop/api/Wingdi/nf-wingdi-fillpath) -Funktion ausfüllen und den Pfad durch Aufrufen der [**strokeandfillpath**](/windows/desktop/api/Wingdi/nf-wingdi-strokeandfillpath) -Funktion umschließen und ausfüllen.

Wenn eine Anwendung einen Pfad füllt, verwendet das System den aktuellen Füllmodus des Domänen Controllers. Eine Anwendung kann diesen Modus abrufen, indem Sie die [**getpolyfillmode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) -Funktion aufruft, und Sie kann einen neuen Füll Modus festlegen, indem Sie die [**setpolyfillmode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) -Funktion aufruft. Eine Beschreibung der beiden Füll Modi finden Sie unter [Regionen](regions.md).

In der folgenden Abbildung wird der Kreuz Abschnitt eines Objekts dargestellt, das von einer Anwendung mit computergestütztem Design (CAD) mithilfe von Pfaden erstellt wurde, die sowohl beschrieben als auch ausgefüllt wurden.

![Abbildung: die quer greifende Ansicht eines Objekts mit verschiedenen Teilen, die durch unterschiedliche Füllmuster angegeben werden](images/cspth-01.png)

 

 



