---
title: IAgentCharacter SetSize
description: IAgentCharacter SetSize
ms.assetid: 8324ab84-2b59-4459-b375-700d72b621bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089226f98969594a1d19afc7f3bb529c30943e06ec4083364dc5ae2f9850c9c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848520"
---
# <a name="iagentcharactersetsize"></a>IAgentCharacter::SetSize

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT SetSize(
   long * lWidth,  // width of the character frame
   long * lHeight  // height of the character frame
);
```

Legt die Größe des Animationsframes des Zeichens fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*
</dt> <dd>

Die Breite des Animationsframes des Zeichens in Pixel.

</dd> <dt>

<span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*
</dt> <dd>

Die Höhe des Animationsframes des Zeichens in Pixel.

</dd> </dl>

Wenn Sie die Framegröße des Zeichens ändern, wird das Zeichen mit dieser Methode auf die Größe skaliert. Die Einstellung dieser Eigenschaft gilt für alle Clients des Zeichens.

Obwohl das Zeichen in einem unregelmäßig gestalteten Bereichsfenster angezeigt wird, basiert die Position des Zeichens auf seinem rechteckigen Animationsframe.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::GetSize**](iagentcharacter--getsize.md)


 

 




