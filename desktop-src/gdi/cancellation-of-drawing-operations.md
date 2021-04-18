---
description: Wenn komplexe Zeichen Anwendungen lange Grafik Vorgänge ausführen, verbrauchen Sie wertvolle Systemressourcen.
ms.assetid: 3beef852-27fe-4ee2-b38b-3dc50e5d2fcf
title: Abbruch von Zeichnungs Vorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e3bdb7a57c7c427e7cd15ffddb62b1c492c25b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994103"
---
# <a name="cancellation-of-drawing-operations"></a>Abbruch von Zeichnungs Vorgängen

Wenn komplexe Zeichen Anwendungen lange Grafik Vorgänge ausführen, verbrauchen Sie wertvolle Systemressourcen. Durch die Nutzung der Multitasking-Features des Systems kann eine Anwendung Threads und die [**canceldc**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc) -Funktion verwenden, um diese Vorgänge zu verwalten. Wenn z. B. der von Thread A ausgeführte Grafik Vorgang benötigte Ressourcen beansprucht, kann Thread B die canceldc-Funktion aufrufen, um diesen Vorgang zu stoppen.

 

 



