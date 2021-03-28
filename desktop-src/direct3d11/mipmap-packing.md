---
title: MipMap-Verpackung
description: Abhängig von der Ebene der Unterstützung für gekachelte Ressourcen folgen Mipmaps mit bestimmten Dimensionen nicht den standardmäßigen Kachel Formen und werden als alle in einer Weise, die für die Anwendung nicht transparent ist, in eine Weise verpackt.
ms.assetid: 3B416324-7656-495F-9BA9-8F5BE475ABC1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db4cd6f70129f46495673dfc82b5d261210ab21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036672"
---
# <a name="mipmap-packing"></a>MipMap-Verpackung

Abhängig von der [Ebene](tiled-resources-features-tiers.md) der Unterstützung für gekachelte Ressourcen folgen Mipmaps mit bestimmten Dimensionen nicht den standardmäßigen Kachel Formen und werden als alle in einer Weise, die für die Anwendung nicht transparent ist, in eine Weise verpackt. Höhere Ebenen der Unterstützung haben eine umfassendere Garantie, welche Arten von Oberflächen Dimensionen in die standardmäßigen Kachel Formen passen (und daher einzeln von Anwendungen zugeordnet werden können).

Die Unterschiede zwischen den Implementierungen bestehen darin, dass – mit den Dimensionen, dem Format, der Anzahl von Mipmaps und den Array Segmenten – eine Menge von MIPS (pro Array Slice) in einige Zahl N Kacheln gepackt werden kann. Die [**ID3D11Device2:: getresourcetielt**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) -API ist vorhanden, damit der Treiber an die Anwendung übermittelt werden kann, was M und N sind (neben anderen Details über die Oberfläche, die von dieser API als Standard und nicht vom Hardwarehersteller abweichen). Der Satz von Kacheln für den verpackten MIPS beträgt weiterhin 64 KB und kann einzeln in verschiedenen Speicherorten in einem Kachel Pool zugeordnet werden. Die Pixel Form der Kacheln und die Art und Weise, wie die Mipmaps in den Satz von Kacheln passen, ist für einen Hardware Anbieter spezifisch und zu komplex. Anwendungen müssen also entweder alle Kacheln zuordnen, die als gepackt gekennzeichnet sind, oder keine von Ihnen. Andernfalls ist das Verhalten für den Zugriff auf die gekachelte Ressource nicht definiert.

Für hochgeladene Oberflächen gilt der Satz von verpackten MIPS und die Anzahl der gepackten Kacheln, die diese MIPS speichern (M und N, die zuvor beschrieben wurden), für jeden Array Slice einzeln.

Dedizierte APIs zum Kopieren von Kacheln ([**ID3D11DeviceContext2:: copytiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) und [**ID3D11DeviceContext2:: updatetiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) können nicht auf gepackte MIPS zugreifen. Anwendungen, die Daten in und aus gepackten MIPS kopieren möchten, können dies mit allen nicht gekachelten Ressourcen spezifischen APIs zum Kopieren und Rendern von-Oberflächen tun.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kacheln eines gekachelten Ressourcenbereichs](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 




