---
description: Die einfachste E/A-Form in Windows Sockets 2 ist das Blockieren von E/A.
ms.assetid: 8ed7e5a8-c577-4b61-9c49-8fd065d84af4
title: Blockierende Eingabe/Ausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c65991f4401a5069718fb39172a9d59db4536a83ab4e2f99948d7c300eb4042
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322614"
---
# <a name="blocking-inputoutput"></a>Blockierende Eingabe/Ausgabe

Die einfachste E/A-Form in Windows Sockets 2 ist das Blockieren von E/A. Wie unter [Socketattributflags und -modi erwähnt,](socket-attribute-flags-and-modes-2.md)werden Sockets standardmäßig im Blockierungsmodus erstellt. Jeder E/A-Vorgang mit einem blockierenden Socket wird erst dann zurück, wenn der Vorgang vollständig abgeschlossen wurde. Daher kann jeder Thread nur einen E/A-Vorgang gleichzeitig ausführen. Wenn beispielsweise ein Thread einen Empfangsvorgang aus gibt und derzeit keine Daten verfügbar sind, wird der Thread blockiert, bis Daten verfügbar sind, und wird in den Puffer des Threads platziert. Obwohl dies einfach ist, ist es nicht unbedingt die effizienteste Möglichkeit, E/A zu tun (weitere Informationen finden Sie unter [Pseudoblockierung](pseudo-vs--true-blocking-2.md) und echte Blockierung).

 

 



