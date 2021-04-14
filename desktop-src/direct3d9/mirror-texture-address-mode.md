---
description: Der vom D3DTADDRESS- \_ Spiegelungs Member des D3DTEXTUREADDRESS-Enumerationstyps identifizierte Spiegel Textur Adress Modus bewirkt, dass Direct3D die Textur an allen ganzzahligen Grenzen spiegelt.
ms.assetid: 816efd4d-94b3-4b6c-9fc9-218cc2207b97
title: Spiegel Textur Adress Modus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 471ad8b715d9375947162c66474687b9d6376bec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392537"
---
# <a name="mirror-texture-address-mode-direct3d-9"></a>Spiegel Textur Adress Modus (Direct3D 9)

Der vom D3DTADDRESS- \_ Spiegelungs Member des [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) -Enumerationstyps identifizierte Spiegel Textur Adress Modus bewirkt, dass Direct3D die Textur an allen ganzzahligen Grenzen spiegelt. Angenommen, Ihre Anwendung erstellt ein quadratisches primitiv und gibt Texturkoordinaten von (0,0, 0,0), (0,0, 3.0), (3.0, 3.0) und (3.0, 0,0) an. Wenn Sie den Textur Adressierungs Modus auf D3DTADDRESS- \_ Spiegelung festlegen, wird die Textur dreimal in den u-und v-Richtungen angewendet. Jede andere Zeile und Spalte, auf die Sie angewendet wird, ist ein Spiegelbild der vorangehenden Zeile oder Spalte, wie in der folgenden Abbildung dargestellt.

![Abbildung von Spiegelbildern in einem 3X3-Raster](images/mirror.png)

Die Auswirkungen dieses Textur Adress Modus ähneln denen des Umbruch Modus, unterscheiden sich jedoch davon. Weitere Informationen finden Sie unter [Wrap Texture Address Mode (Direct3D 9)](wrap-texture-address-mode.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textur Adressierungs Modi](texture-addressing-modes.md)
</dt> </dl>

 

 
