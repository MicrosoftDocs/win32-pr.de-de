---
title: In-Context Hook-Funktionen
ms.assetid: bf12bda6-b00e-4fbe-a576-b989aa428b54
description: 'Weitere Informationen finden Sie hier: In-Context Hook-Funktionen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe25bd64234cfbfd92f054565aa7c675328b435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218493"
---
# <a name="in-context-hook-functions"></a>In-Context Hook-Funktionen

In der folgenden Liste werden die wichtigsten Aspekte der in-context-Hook-Funktionen beschrieben:

-   In-context-Hook-Funktionen müssen sich in einer Dynamic Link Library (dll) befinden, die das System dem Adressraum des Servers zuordnet.
-   In-context-Hook-Funktionen geben den Adressraum mit dem Server frei.
-   Wenn der Server ein Ereignis auslöst, ruft das System eine Hook-Funktion ohne Marshalling auf (Verpacken und Senden von Schnittstellenparametern über Prozess Grenzen hinweg).
-   In-context-Hook-Funktionen sind tendenziell sehr schnell und empfangen Ereignis Benachrichtigungen synchron, da kein Marshalling vorhanden ist.
-   Einige Ereignisse werden möglicherweise außerhalb des Prozesses übermittelt, auch wenn Sie anfordern, dass Sie in-Process (mit dem WinEvent \_ InContext-Flag) übermittelt werden. Möglicherweise wird diese Situation mit 64-Bit-und 32-Bit-anwendungsinteroperabilitäts Problemen und mit Windows-Konsolen Ereignissen angezeigt.

 

 




