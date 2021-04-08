---
title: Mouswheel-Eingabe für Windows 8.1
description: Mouswheel-Eingabe für Windows 8.1
ms.assetid: A178E86C-16A6-4DF5-9880-CF83F62AAF04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd9480280bf5526c8cd63c0703705c7ef742bff4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855811"
---
# <a name="mousewheel-input-for-windows-81"></a>Mouswheel-Eingabe für Windows 8.1

## <a name="platform"></a>Plattform

<dl> Clients-Windows 8.1  
Server-Windows Server 2012 R2  
</dl>

## <a name="description"></a>BESCHREIBUNG

In Windows 8.1 werden mouserwheel-Ereignisse nicht mehr basierend auf dem Tastaturfokus wie in früheren Windows-Versionen bereitgestellt. Wenn in Windows 8.1 der Mauszeiger auf eine Store-App zeigt, wird Mausrad an diese APP übermittelt. aus Kompatibilitätsgründen wird Mausrad jedoch weiterhin basierend auf dem Tastaturfokus übermittelt, wenn der Mauszeiger auf eine Desktop-App zeigt.

## <a name="manifestations"></a>Kundgebungen

Wenn die Maus über Store-Apps bewegt wird, führt Mausrad einen Bildlauf für alle anwendbaren Inhalte durch, ohne dass der Benutzer auf die Store-App klicken muss. Dies gilt auch für den Startbildschirm. Dadurch wird das Scrollen durch mouswheel zu einer einfacheren Interaktion in Windows 8.1 als in Windows 8.

## <a name="mitigation"></a>Minderung

Zum größten Teil sollte diese Änderung keine Auswirkungen auf vorhandene apps haben. Wenn eine Store-App nur nach dem Registrieren eines Mausklicks auf Mausrad-Ereignisse lauscht, würde diese APP wahrscheinlich nicht auf Mausrad Antworten, bis der Benutzer Sie aktiv geklickt hat. Folglich besteht der wahrscheinlichste Nachteil darin, dass eine APP weiterhin genauso funktioniert wie in Windows 8. Bei Desktop-Apps wird der APP mit dem Tastaturfokus nicht mehr ein Monopol über Mausrad-Eingaben erteilt, aber auch diese apps werden nicht in irgendeiner Weise unterstützt. Es sind also keine kurzfristigen Maßnahmen erforderlich.

## <a name="solution"></a>Lösung

Entwickler von Store-Apps sollten mit dem Empfang von Mausrad-Ereignissen ohne ein gedrückter Mausklicks rechnen. Sie sollten z. b. nur nach dem Registrieren eines Mausklicks auf Mausrad-Ereignisse lauschen. Ebenso sollten Desktop Anwendungen nicht versuchen, Mausrad-Ereignisse zu erfassen (z. b. durch Festlegen eines Hooks auf niedriger Ebene), wenn Sie den Tastaturfokus haben.

## <a name="tests"></a>Tests

Store-App-Entwickler sollten sich auf Windows 8.1 testen, um zu überprüfen, ob alle scrollfunktionen funktionieren, wenn der Mauszeiger über die APP bewegt wird. Entwickler von Desktop-Apps sollten auf Windows 8.1 testen, um sicherzustellen, dass Sie keine Mausrad-Ereignisse erfassen (pro Leitfaden oben).

 

 




