---
description: Wenn komplexe Zeichnungsanwendungen lange Grafikvorgänge ausführen, nutzen sie wertvolle Systemressourcen.
ms.assetid: 3beef852-27fe-4ee2-b38b-3dc50e5d2fcf
title: Abbruch von Zeichnungsvorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2ddf90842ed7da612e046f8cc44bc8972b236232f3757bd31a295377eafab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470032"
---
# <a name="cancellation-of-drawing-operations"></a>Abbruch von Zeichnungsvorgängen

Wenn komplexe Zeichnungsanwendungen lange Grafikvorgänge ausführen, nutzen sie wertvolle Systemressourcen. Durch die Nutzung der Multitaskingfeatures des Systems kann eine Anwendung Threads und die [**CancelDC-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc) verwenden, um diese Vorgänge zu verwalten. Wenn der von Thread A ausgeführte Grafikvorgang beispielsweise die benötigten Ressourcen verbraucht, kann Thread B die CancelDC-Funktion aufrufen, um diesen Vorgang anzuhalten.

 

 



