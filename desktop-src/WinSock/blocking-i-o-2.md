---
description: Die einfachste Art von e/a in Windows Sockets 2 ist das Blockieren von e/a.
ms.assetid: 8ed7e5a8-c577-4b61-9c49-8fd065d84af4
title: Blockieren von Eingaben/Ausgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c846a22fcf9d10f562a48683c2ead723f9bd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348393"
---
# <a name="blocking-inputoutput"></a>Blockieren von Eingaben/Ausgaben

Die einfachste Art von e/a in Windows Sockets 2 ist das Blockieren von e/a. Wie in [socketattributflags und-Modi](socket-attribute-flags-and-modes-2.md)erwähnt, werden Sockets standardmäßig im Blockierungs Modus erstellt. Ein e/a-Vorgang mit einem blockierenden Socket wird erst zurückgegeben, wenn der Vorgang vollständig abgeschlossen wurde. Daher kann jeder Thread nur einen e/a-Vorgang gleichzeitig ausführen. Wenn ein Thread z. b. einen Empfangsvorgang ausgibt und derzeit keine Daten verfügbar sind, wird der Thread blockiert, bis die Daten verfügbar sind und in den Puffer des Threads eingefügt werden. Obwohl dies einfach ist, ist es nicht notwendigerweise die effizienteste Methode, e/a-Vorgänge durchzuführen (Weitere Informationen finden Sie unter [Pseudo Blockierung und echte Blockierung](pseudo-vs--true-blocking-2.md) ).

 

 



