---
description: Direct3D 9 unterstützt Palettentexturen über einen Satz von 256 Eintragspaletten, die dem IDirect3DDevice9-Objekt zugeordnet sind.
ms.assetid: dea4b4bc-7eba-40fa-9c2c-0851fe7e231b
title: Texturpaletten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d755abb638ab1dd94e25edd98b2daef5e65d5a54cca7baf21a74e7d06173eed9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118291165"
---
# <a name="texture-palettes-direct3d-9"></a>Texturpaletten (Direct3D 9)

Direct3D 9 unterstützt Palettentexturen über einen Satz von 256 Eingabepaletten, die dem [**IDirect3DDevice9-Objekt zugeordnet**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) sind. Eine Palette wird durch Aufrufen der [**IDirect3DDevice9::SetCurrentTexturePalette-Methode**](/windows/desktop/api) aktuell gemacht. Die aktuelle Palette wird zum Übersetzen aller Palettentexturen für alle aktiven Texturstufen verwendet. [**IDirect3DDevice9::SetPaletteEntries**](/windows/desktop/api) aktualisiert alle 256 Einträge einer Palette. Jeder Eintrag ist eine [**PALETTEENTRY-Struktur**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) im Format D3DFMT \_ A8R8G8B8. Alle Einträge werden standardmäßig 0xFFFFFFFF.

Die [**IDirect3DDevice9-Paletten**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) enthalten einen Alphakanal. Dieser Alphakanal kann verwendet werden, wenn das Gerätefunktionsflag D3DPTEXTURECAPS ALPHAPALETTE festgelegt ist, das angibt, dass das Gerät Alpha aus der \_ Palette unterstützt. Der Paletten-Alphakanal wird verwendet, wenn das Texturformat keinen Alphakanal hat. Wenn das Gerät alpha aus der Palette nicht unterstützt und das Texturformat keinen Alphakanal hat, wird der Wert 0xFF alpha verwendet.

Es gibt maximal 65.536 Paletten (0x0000FFFF Paletten). Da speicherressourcen, die dem Satz von Paletten zugeordnet sind, proportional zur maximalen Palettennummer sind, auf die eine Anwendung verweist, verwenden Sie zusammenhängende Palettennummern, die bei 0 (null) beginnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende Texturkonzepte](basic-texturing-concepts.md)
</dt> </dl>

 

 
