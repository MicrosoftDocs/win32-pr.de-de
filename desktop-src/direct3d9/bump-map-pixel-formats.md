---
description: Eine Bump Map ist ein IDirect3DTexture9-Objekt, das ein spezielles Pixel Format verwendet.
ms.assetid: 7f405cb9-9512-44da-8a85-4b7d22017284
title: Bump Map-Pixel Formate (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21bbe4a9999d875e43d33389f86b35d22c81b3bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041497"
---
# <a name="bump-map-pixel-formats-direct3d-9"></a>Bump Map-Pixel Formate (Direct3D 9)

Eine Bump Map ist ein [**IDirect3DTexture9**](/windows/desktop/api) -Objekt, das ein spezielles Pixel Format verwendet. Anstelle von roten, grünen und blauen Farbkomponenten speichert jedes Pixel in einer Bump-Karte die Delta Werte für Sie und v<sub>(d und d</sub> <sub>v</sub>) und manchmal eine Leuchtkraft Komponente (L). Diese Werte werden vom System angewendet, wie im Thema [Bump Mapping-Formeln (Direct3D 9)](bump-mapping-formulas.md) beschrieben.

Sie können ein Bump Map-Pixel Format angeben, indem Sie das Format auf eine der folgenden Einstellungen festlegen: D3DFMT \_ CxV8U8, D3DFMT \_ V8U8, D3DFMT \_ L6V5U5, D3DFMT \_ X8L8V8U8, D3DFMT \_ Q8W8V8U8 oder D3DFMT V16U16 \_ . Beschreibungen finden Sie unter [D3DFORMAT](d3dformat.md).

Die Komponenten d<sub>U</sub> und d<sub>V</sub> eines Pixels sind signierte Werte zwischen-1,0 und + 1,0. Bei Verwendung der "Leuchtdichte"-Komponente handelt es sich um einen ganzzahligen Wert ohne Vorzeichen, der zwischen 0 und 255 liegt.

> [!Note]  
> Überprüfen Sie vor dem Auswählen eines Kugel Karten-Pixel Formats, ob das jeweilige Format unterstützt wird. Weitere Informationen finden Sie unter [Verwenden der Bump-Zuordnung (Direct3D 9)](using-bump-mapping.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bump-Zuordnung](bump-mapping.md)
</dt> </dl>

 

 



