---
description: Direct3D-Anwendungen können zahlreiche besondere Effekte erzielen, indem Sie im Verlauf mehrerer Renderingdurchläufen verschiedene Texturen auf ein primitiv anwenden.
ms.assetid: 884cc928-305e-46b9-acbf-ca58dfbc05e6
title: Multipass-Textur Mischung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0a042088694f686003a6dc259cf1d914db2b59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124472"
---
# <a name="multipass-texture-blending-direct3d-9"></a>Multipass-Textur Mischung (Direct3D 9)

Direct3D-Anwendungen können zahlreiche besondere Effekte erzielen, indem Sie im Verlauf mehrerer Renderingdurchläufen verschiedene Texturen auf ein primitiv anwenden. Der allgemeine Begriff hierfür ist Multipass-Textur Mischung. Eine typische Verwendung von Multipass-Textur Mischungs Modellen besteht darin, die Auswirkungen komplexer Beleuchtungs-und Schattierungs Modelle durch Anwenden mehrerer Farben aus verschiedenen Texturen zu emulieren. Eine solche Anwendung wird als "Light Mapping" bezeichnet. Weitere Informationen finden Sie unter [Light Mapping with Texturen (Direct3D 9)](light-mapping-with-textures.md).

> [!Note]  
> Einige Geräte können in einem einzigen Durchlauf mehrere Texturen auf primitive anwenden. Weitere Informationen finden Sie unter [Textur blending (Direct3D 9)](texture-blending.md).

 

Wenn die Hardware des Benutzers mehrere Textur Mischungs Möglichkeiten nicht unterstützt, kann die Anwendung Multipass-Textur blending verwenden, um die gleichen visuellen Effekte zu erzielen. Die Anwendung kann jedoch nicht die Frameraten unterstützen, die bei Verwendung mehrerer Textur Mischungs Möglichkeiten möglich sind.

Zum Durchführen einer Multipass-Textur Mischung in einer C/C++-Anwendung.

1.  Legen Sie eine Textur in Textur Phase 0 fest, indem Sie die [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) -Methode aufrufen.
2.  Wählen Sie die gewünschte Farbe und Alpha Mischung aus Argumenten und Vorgängen mit der [**IDirect3DDevice9:: settexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) -Methode aus. Die Standardeinstellungen eignen sich gut für Multipass-Textur Mischungs.
3.  Rendering der entsprechenden Objekte in der Szene.
4.  Legen Sie die nächste Textur in der Textur Phase 0 fest.
5.  Legen Sie die \_ Rendering-Zustände D3DRS srcblend und D3DRS \_ destblend so fest, dass die Quell-und Ziel-Mischungs Faktoren bei Bedarf angepasst werden. Das System kombiniert die neuen Texturen mit den vorhandenen Pixeln auf der renderzieloberfläche gemäß diesen Parametern.
6.  Wiederholen Sie die Schritte 3, 4 und 5 mit beliebig vielen Texturen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textur Mischung](texture-blending.md)
</dt> </dl>

 

 
