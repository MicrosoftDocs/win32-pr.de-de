---
description: Der Umbruch-Textur Adress Modus, der durch den D3DTADDRESS \_ Wrap-Member des D3DTEXTUREADDRESS-Enumerationstyps identifiziert wird, bewirkt, dass Direct3D die Textur für jede ganzzahlige Verknüpfung wiederholt
ms.assetid: fe33c484-346d-4888-ba88-b8ab00feefbb
title: Wrap-Textur Adress Modus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721ace45599236022f32e6b0ec3723e346befbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213838"
---
# <a name="wrap-texture-address-mode-direct3d-9"></a>Wrap-Textur Adress Modus (Direct3D 9)

Der Umbruch-Textur Adress Modus, der durch den D3DTADDRESS \_ Wrap-Member des [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) -Enumerationstyps identifiziert wird, bewirkt, dass Direct3D die Textur für jede ganzzahlige Verknüpfung wiederholt Angenommen, Ihre Anwendung erstellt ein quadratisches primitiv und gibt Texturkoordinaten von (0,0, 0,0), (0,0, 3.0), (3.0, 3.0) und (3.0, 0,0) an. Wenn Sie den Textur Adressierungs Modus auf D3DTADDRESS \_ Wrap festlegen, wird die Textur dreimal in den u-und v-Richtungen angewendet, wie in der folgenden Abbildung dargestellt.

![Abbildung einer Gesichts Textur, die in der u-Richtung und der v-Richtung umschließt](images/wrap.png)

Die Auswirkungen dieses Textur Adress Modus ähneln denen des Spiegelmodus, unterscheiden sich jedoch davon. Weitere Informationen finden Sie unter [Spiegel Textur Adress Modus (Direct3D 9)](mirror-texture-address-mode.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textur Adressierungs Modi](texture-addressing-modes.md)
</dt> </dl>

 

 
