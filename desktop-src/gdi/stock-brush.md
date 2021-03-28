---
description: Von der Graphics Device Interface (GDI) werden sieben vordefinierte logische Aktien Pinsel verwaltet. Es gibt auch 21 vordefinierte logische Aktien Pinsel, die von der Fenster Verwaltungsschnittstelle (User) verwaltet werden.
ms.assetid: ddbc6d54-47f6-4810-9d3a-feede80f2bed
title: Aktien Pinsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522337752c2d81a92302d4a6a8f025393db1ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980528"
---
# <a name="stock-brush"></a>Aktien Pinsel

Von der Graphics Device Interface (GDI) werden sieben vordefinierte logische Aktien Pinsel verwaltet. Es gibt auch 21 vordefinierte logische Aktien Pinsel, die von der Fenster Verwaltungsschnittstelle (User) verwaltet werden.

Die folgende Abbildung zeigt Rechtecke, die mithilfe der sieben vordefinierten Aktien Pinsel gezeichnet wurden.

![Abbildung, die sieben Felder anzeigt: ein schwarzer, drei graue Schattierungen und drei, die leer erscheinen](images/csbru-03.png)

Eine Anwendung kann ein Handle abrufen, das einen der sieben Aktien Pinsel durch Aufrufen der [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) -Funktion identifiziert, wobei der pinkentyp angegeben wird.

Die 21 Stock-Pinsel, die von der Fenster Verwaltungsschnittstelle verwaltet werden, entsprechen den Farben von Fensterelementen, z. b. Menüs, Scrollleisten und Schaltflächen. Eine Anwendung kann ein Handle abrufen, das einen dieser Pinsel identifiziert, indem Sie die [**getsyscolorbrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) -Funktion aufruft und einen System Farbwert angibt. Eine Anwendung kann die Farbe, die einem bestimmten Fensterelement entspricht, abrufen, indem die [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) -Funktion aufgerufen wird. Eine Anwendung kann die Farbe, die einem Window-Element entspricht, durch Aufrufen der [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) -Funktion festlegen.

 

 
