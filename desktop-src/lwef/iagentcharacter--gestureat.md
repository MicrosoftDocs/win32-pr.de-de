---
title: IAgentCharacter GestureAt
description: IAgentCharacter GestureAt
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde86f9e1e60820aa7e1bc3a3f839dc920efda001f5b15e4f1ec7df4fc0cd7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976450"
---
# <a name="iagentcharactergestureat"></a>IAgentCharacter::GestureAt

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GestureAt(
   short x,         // x-coordinate of specified location
   short y,         // y-coordinate of specified location
   long * pdwReqID  // address of a request ID
);
```

Gibt die zugeordnete **Gesturing-Zustandsanimation** basierend auf der angegebenen Position wieder.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war. Wenn die Funktion zurückgegeben wird, *enthält pdwReqID* die ID der Anforderung.

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Die x-Koordinate der angegebenen Position in Pixel relativ zum Ursprung des Bildschirms (links oben).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Die y-Koordinate der angegebenen Position in Pixel relativ zum Ursprung des Bildschirms (links oben).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse einer Variablen, die die **GestureAt-Anforderungs-ID** empfängt.

</dd> </dl>

Der Server bestimmt automatisch die entsprechende Gesturierungsanimation basierend auf der aktuellen Position des Zeichens und der angegebenen Position und gibt diese wieder. Wenn Sie das HTTP-Protokoll für den [](iagentcharacter--prepare.md) Zugriff auf Zeichen- und Animationsdaten verwenden, verwenden Sie die Prepare-Methode, um sicherzustellen, dass die Animationen verfügbar sind, bevor Sie diese Methode aufrufen.

 

 




