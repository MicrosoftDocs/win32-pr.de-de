---
title: Informationen zu avifile-Funktionen und-Makros
description: Informationen zu avifile-Funktionen und-Makros
ms.assetid: 877f6759-8271-47eb-8a7f-540393e5ae89
keywords:
- Avifileingeit-Funktion
- Avifileexit-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f66bbac900b69841fd7cba814aad339731b75727
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037574"
---
# <a name="about-avifile-functions-and-macros"></a>Informationen zu avifile-Funktionen und-Makros

Die avifile-Funktionen und-Makros verarbeiten die Informationen in zeitbasierten Dateien als einen oder mehrere *Datenströme* anstelle von markierten Datenblöcken, die als Blöcke bezeichnet werden. Datenströme verweisen auf die Komponenten einer zeitbasierten Datei. Eine AVI-Datei kann mehrere verschiedene Arten von Daten enthalten, z. b. eine Videosequenz, einen englischen Sound Sound und einen französischen Sound. Mithilfe von avifile kann eine Anwendung separat auf jede dieser Komponenten zugreifen.

> [!Note]  
> Obwohl die avifile-Funktionen und-Makros mit einer beliebigen Riff Datei funktionieren, wird in dieser Übersicht ihre Verwendung nur mit AVI-Dateien veranschaulicht. AVI-Dateien sind in der Regel die zeitbasierten Dateien, die mit den avifile-Makros und-Funktionen verwendet werden.

 

Avifile-Funktionen und-Makros sind in einer Dynamic Link Library enthalten. Um die Bibliothek zu initialisieren, verwenden [**Sie die avifilinput IT**](/windows/desktop/api/Vfw/nf-vfw-avifileinit) -Funktion. Nachdem Sie die Bibliothek initialisiert haben, können Sie eine beliebige der avifile-Funktionen oder-Makros verwenden. Verwenden Sie zum Freigeben der Bibliothek die [**avifileexit**](/windows/desktop/api/Vfw/nf-vfw-avifileexit) -Funktion. Avifile verwaltet den Verweis Zähler der Anwendungen, die die Bibliothek verwenden, jedoch nicht die, die Sie freigegeben haben. Ihre Anwendungen sollten jede Verwendung von **AVIFileInit** mit einem **avifileexit** -Befehl ausgleichen, um die Bibliothek vollständig freizugeben, nachdem jede Anwendung Sie verwendet hat.

 

 




