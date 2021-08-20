---
description: Die einfachste E/A-Form in Windows Sockets 2 ist das Blockieren von E/A.
ms.assetid: 8ed7e5a8-c577-4b61-9c49-8fd065d84af4
title: Blockieren von Eingabe/Ausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c65991f4401a5069718fb39172a9d59db4536a83ab4e2f99948d7c300eb4042
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322614"
---
# <a name="blocking-inputoutput"></a>Blockieren von Eingabe/Ausgabe

Die einfachste E/A-Form in Windows Sockets 2 ist das Blockieren von E/A. Wie unter [Socketattributflags und -modi](socket-attribute-flags-and-modes-2.md)erwähnt, werden Sockets standardmäßig im Blockierungsmodus erstellt. E/A-Vorgänge mit einem blockierenden Socket werden erst zurückgegeben, wenn der Vorgang vollständig abgeschlossen wurde. Daher kann jeder Thread jeweils nur einen E/A-Vorgang ausführen. Wenn beispielsweise ein Thread einen Empfangsvorgang ausgibt und derzeit keine Daten verfügbar sind, blockiert der Thread, bis Daten verfügbar sind und im Puffer des Threads platziert werden. Dies ist zwar einfach, aber nicht unbedingt die effizienteste Methode zum E/A-Arbeiten (weitere Informationen finden Sie unter [Pseudoblockierung und True Blocking).](pseudo-vs--true-blocking-2.md)

 

 



