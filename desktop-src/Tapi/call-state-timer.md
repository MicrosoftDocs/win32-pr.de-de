---
description: Derzeit bleibt die gesamte Zeitsteuerung von Aufrufen den Anwendungen überlassen.
ms.assetid: 9eb98b48-4bee-4f6d-b818-2f81b36591da
title: Aufrufen des Zustandstimers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221b0cd1182e59304b13d6d276bece9f755c5dacc0215218ff5ee23aea09e532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118869994"
---
# <a name="call-state-timer"></a>Aufrufen des Zustandstimers

Derzeit bleibt die gesamte Zeitsteuerung von Aufrufen den Anwendungen überlassen. Dies kann aufwändig sein, wenn die Anwendung eine große Anzahl von Aufrufen überwacht und wenn mehrere Anwendungen vorhanden sind, möglicherweise auf mehreren Servern, kann es erforderlich sein, dass alle Timer für dieselben Aufrufe beibehalten werden. Daher ist es sinnvoller, die Zeitsteuerung für den Aufrufzustand vom Server zu behandeln.

Der **tStateEntryTime-Member** in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) ermöglicht das Melden der zeitlichen Steuerung von Aufrufen in Zuständen. Der Member (vom Typ **SYSTIME**) gibt den Zeitpunkt an, zu dem der aktuelle Zustand eingegeben wurde.

 

 



