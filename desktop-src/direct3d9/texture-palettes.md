---
description: Direct3D 9 unterstützt Palettentexturen durch eine Reihe von 256-Einträge, die mit dem IDirect3DDevice9-Objekt verknüpft sind.
ms.assetid: dea4b4bc-7eba-40fa-9c2c-0851fe7e231b
title: Textur Paletten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a0fbb1c5d6766b879b898145ec2385a41d94b8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346398"
---
# <a name="texture-palettes-direct3d-9"></a>Textur Paletten (Direct3D 9)

Direct3D 9 unterstützt Palettentexturen durch eine Reihe von 256-Einträge, die mit dem [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Objekt verknüpft sind. Eine Palette wird durch Aufrufen der [**IDirect3DDevice9:: setcurrenttexturepalette**](/windows/desktop/api) -Methode aktuell gemacht. Mit der aktuellen Palette werden alle Palettentexturen für alle aktiven Textur Stufen übersetzt. [**IDirect3DDevice9:: setpaletteentries**](/windows/desktop/api) aktualisiert alle 256-Einträge einer Palette. Jeder Eintrag ist eine [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) -Struktur im Format D3DFMT \_ A8R8G8B8. Alle Einträge werden standardmäßig auf "0xffffffff" eingestellt.

Die [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) Paletten enthalten einen Alphakanal. Dieser Alphakanal kann verwendet werden, wenn das D3DPTEXTURECAPS \_ alphapalette Device Capability-Flag festgelegt ist, was bedeutet, dass das Gerät Alpha aus der Palette unterstützt. Der palettenalpha Kanal wird verwendet, wenn das Textur Format keinen Alpha-Kanal hat. Wenn das Gerät Alpha aus der Palette nicht unterstützt und das Textur Format keinen Alphakanal aufweist, wird der Wert 0xFF für Alpha verwendet.

Es sind maximal 65.536 (0X0000FFFF) Paletten vorhanden. Da die dem Satz von Paletten zugeordneten Speicherressourcen proportional zur maximalen Palettennummer sind, auf die eine Anwendung verweist, verwenden Sie angrenzende Palettennummern, beginnend bei Null.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende Konzepte der Texturierung](basic-texturing-concepts.md)
</dt> </dl>

 

 
