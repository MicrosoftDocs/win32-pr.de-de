---
description: Direct3D-Anwendungen können zahlreiche Sondereffekte erzielen, indem sie im Laufe mehrerer Renderingdurchläufe verschiedene Texturen auf einen Primitiven anwenden.
ms.assetid: 884cc928-305e-46b9-acbf-ca58dfbc05e6
title: Multipass-Texturmischung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43ec4916cb3c86c0e3aa6e2c6ab9a5e03de8304989391b9c80b1070fc7b51594
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491520"
---
# <a name="multipass-texture-blending-direct3d-9"></a>Multipass-Texturmischung (Direct3D 9)

Direct3D-Anwendungen können zahlreiche Sondereffekte erzielen, indem sie im Laufe mehrerer Renderingdurchläufe verschiedene Texturen auf einen Primitiven anwenden. Der allgemeine Begriff hierfür ist die Mehrpasstexturmischung. Eine typische Verwendung für die Mehrpass-Texturmischung besteht darin, die Auswirkungen komplexer Beleuchtungs- und Schattierungsmodelle zu emulieren, indem mehrere Farben aus mehreren verschiedenen Texturen angewendet werden. Eine solche Anwendung wird als Lichtzuordnung bezeichnet. Weitere Informationen finden Sie unter [Light Mapping with Textures (Direct3D 9) (Lichtzuordnung mit Texturen (Direct3D 9)).](light-mapping-with-textures.md)

> [!Note]  
> Einige Geräte können mehrere Texturen in einem einzigen Durchlauf auf Primitive anwenden. Weitere Informationen finden Sie unter [Texturmischung (Direct3D 9).](texture-blending.md)

 

Wenn die Hardware des Benutzers das Mischen mehrerer Texturen nicht unterstützt, kann Ihre Anwendung multipass texture blending verwenden, um die gleichen visuellen Effekte zu erzielen. Die Anwendung kann jedoch die Frameraten nicht aufrechterhalten, die möglich sind, wenn mehrere Texturmischungen verwendet werden.

So führen Sie eine Mehrfachpasstexturmischung in einer C/C++-Anwendung aus.

1.  Legen Sie eine Textur in Texturphase 0 fest, indem Sie die [**IDirect3DDevice9::SetTexture-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) aufrufen.
2.  Wählen Sie mit der [**IDirect3DDevice9::SetTextureStageState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) die gewünschten Farb- und Alphamischungsargumente und -vorgänge aus. Die Standardeinstellungen eignen sich gut für das Mischen von Mehrpasstextur.
3.  Rendert die entsprechenden Objekte in der Szene.
4.  Legen Sie die nächste Textur in Texturstufe 0 fest.
5.  Legen Sie die Renderzustände D3DRS \_ SRCBLEND und D3DRS \_ DESTBLEND fest, um die Quell- und Zielmischungsfaktoren nach Bedarf anzupassen. Das System kombiniert die neuen Texturen gemäß diesen Parametern mit den vorhandenen Pixeln auf der Renderzieloberfläche.
6.  Wiederholen Sie die Schritte 3, 4 und 5 mit so vielen Texturen wie erforderlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturmischung](texture-blending.md)
</dt> </dl>

 

 
