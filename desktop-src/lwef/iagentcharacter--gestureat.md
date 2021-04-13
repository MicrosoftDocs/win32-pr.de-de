---
title: Iagentcharacter gestureat
description: Iagentcharacter gestureat
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 266dc2d5e797ec0c7b30f7f827a094cd01c04195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388815"
---
# <a name="iagentcharactergestureat"></a>Iagentcharacter:: gestureat

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GestureAt(
   short x,         // x-coordinate of specified location
   short y,         // y-coordinate of specified location
   long * pdwReqID  // address of a request ID
);
```

Gibt die zugehörige Status Animation des **gesturten** Zustands basierend auf der angegebenen Position wieder.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war. Wenn die Funktion zurückgibt, enthält *pdwreqid* die ID der Anforderung.

<dl> <dt>

<span id="x"></span><span id="X"></span>*Stuben*
</dt> <dd>

Die x-Koordinate der angegebenen Position in Pixel relativ zum Bildschirm Ursprung (oben links).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Teenie*
</dt> <dd>

Die y-Koordinate der angegebenen Position in Pixel relativ zum Bildschirm Ursprung (oben links).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*
</dt> <dd>

Adresse einer Variablen, die die **gestureat** -Anforderungs-ID empfängt.

</dd> </dl>

Der Server ermittelt und gibt die entsprechende gesturinganimation automatisch basierend auf der aktuellen Position des Zeichens und der angegebenen Position wieder. Verwenden Sie bei Verwendung des HTTP-Protokolls für den Zugriff auf Zeichen-und Animationsdaten die [**Prepare**](iagentcharacter--prepare.md) -Methode, um sicherzustellen, dass die Animationen verfügbar sind, bevor Sie diese Methode aufrufen.

 

 




