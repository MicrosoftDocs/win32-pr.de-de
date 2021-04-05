---
title: Iagentcharacter setSize
description: Iagentcharacter setSize
ms.assetid: 8324ab84-2b59-4459-b375-700d72b621bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d39d5b33afa7ff59516b793f194a0ba186c2e002
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713187"
---
# <a name="iagentcharactersetsize"></a>Iagentcharacter:: SetSize

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetSize(
   long * lWidth,  // width of the character frame
   long * lHeight  // height of the character frame
);
```

Legt die Größe des Animations Rahmens des Zeichens fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lwidth*
</dt> <dd>

Die Breite des Animations Rahmens des Zeichens in Pixel.

</dd> <dt>

<span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lheight*
</dt> <dd>

Die Höhe des Animations Rahmens des Zeichens in Pixel.

</dd> </dl>

Wenn Sie die Frame Größe des Zeichens ändern, wird das Zeichen in die mit dieser Methode festgelegte Größe skaliert. Diese Eigenschafts Einstellung gilt für alle Clients des Zeichens.

Obwohl das Zeichen in einem unregelmäßig formatierte Regions Fenster angezeigt wird, basiert der Speicherort des Zeichens auf seinem rechteckigen Animations Rahmen.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: GetSize**](iagentcharacter--getsize.md)


 

 




