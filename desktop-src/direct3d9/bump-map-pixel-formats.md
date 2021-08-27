---
description: Eine Bumpmap ist ein IDirect3DTexture9-Objekt, das ein spezielles Pixelformat verwendet.
ms.assetid: 7f405cb9-9512-44da-8a85-4b7d22017284
title: Bump Map-Pixelformate (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f627ce95151207c25e2365d2e467fb94b93cfb5c1bf54ce0c3df401891fcafc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805725"
---
# <a name="bump-map-pixel-formats-direct3d-9"></a>Bump Map-Pixelformate (Direct3D 9)

Eine Bumpmap ist ein [**IDirect3DTexture9-Objekt,**](/windows/desktop/api) das ein spezielles Pixelformat verwendet. Anstatt rote, grüne und blaue Farbkomponenten zu speichern, speichert jedes Pixel in einer Bumpmap die Deltawerte für Sie und v (D<sub>U</sub> und D<sub>V</sub>) und manchmal auch eine Leuchtdichtekomponente, L. Diese Werte werden vom System angewendet, wie im Thema [Bump Mapping Formulas (Direct3D 9)](bump-mapping-formulas.md) beschrieben.

Sie können ein Pixelformat für die Bumpzuordnung angeben, indem Sie das Format auf eines der folgenden Festlegen festlegen: D3DFMT \_ CxV8U8, D3DFMT \_ V8U8, D3DFMT \_ L6V5U5, D3DFMT \_ X8L8V8U8, D3DFMT \_ Q8W8V8U8 oder D3DFMT \_ V16U16. Beschreibungen finden Sie unter [D3DFORMAT](d3dformat.md).

Die D<sub>U-</sub> und D<sub>V-Komponenten</sub> eines Pixels sind Werte mit Vor signiert, die zwischen –1,0 und +1,0 liegen. Bei Verwendung der Luminanzkomponente handelt es sich um einen ganzzahligen Wert ohne Vorzeichen, der zwischen 0 und 255 liegt.

> [!Note]  
> Überprüfen Sie vor dem Auswählen eines Pixelformats für die Bumpzuordnung, ob das bestimmte Format unterstützt wird. Weitere Informationen finden Sie unter [Verwenden der Bumpzuordnung (Direct3D 9).](using-bump-mapping.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bump-Zuordnung](bump-mapping.md)
</dt> </dl>

 

 



