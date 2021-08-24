---
description: Die Verzerrung, die in den Texeln eines 3D-Objekts sichtbar ist, dessen Oberfläche in Bezug auf die Bildschirmebene an einem Winkel ausgerichtet ist, wird als Anisotropie bezeichnet.
ms.assetid: f6c8a9e2-aab0-4f06-956e-bb86557c72e7
title: Anisotrope Texturfilterung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363aeef463f137a240602e52410260108ee4a40a1a23da7b2e7c245ed6e74a65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676940"
---
# <a name="anisotropic-texture-filtering-direct3d-9"></a>Anisotrope Texturfilterung (Direct3D 9)

Die Verzerrung, die in den Texeln eines 3D-Objekts sichtbar ist, dessen Oberfläche in Bezug auf die Bildschirmebene an einem Winkel ausgerichtet ist, wird als Anisotropie bezeichnet. Wenn ein Pixel aus einem anisotropen Primitiven texels zugeordnet wird, wird seine Form verzerrt. Direct3D misst die Anisotropie eines Pixels als Die Länge eines Bildschirmpixels, das umgekehrt dem Texturraum zugeordnet ist, d. h. länge geteilt durch Breite.

Sie können die Anisotrope Texturfilterung in Verbindung mit linearer Texturfilterung oder Mipmaptexturfilterung verwenden, um renderingergebnisse zu verbessern. Ihre Anwendung ermöglicht die Anisotrope Texturfilterung, indem sie die [**IDirect3DDevice9::SetSamplerState-Methode aufruft.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) Legen Sie den Wert des ersten Parameters auf die ganzzahlige Indexnummer (0-7) der Textur fest, für die Sie eine Texturfilterungsmethode auswählen. Übergeben Sie D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER oder D3DSAMP \_ MIPFILTER für den zweiten Parameter, um den Filter für Vergrößerung, Vergrößerung oder Mipmapping festzulegen. Legen Sie den dritten Parameter auf D3DTEXF \_ ANISOTROPE fest.

Ihre Anwendung muss auch den Grad der Anisotropie auf einen Wert größer als 1 festlegen. Rufen Sie hierzu die [**IDirect3DDevice9::SetSamplerState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) auf. Legen Sie den Wert des ersten Parameters auf die ganzzahlige Indexnummer (0-7) der Textur fest, für die Sie den Grad der Isotropie festlegen. Übergeben Sie D3DSAMP \_ MAXANISOTROPY als Wert des zweiten Parameters. Der letzte Parameter sollte der Grad der Isotropie sein.

Sie können die Isotrope Filterung deaktivieren, indem Sie den Grad der Isotropie auf eins festlegen. jeder Wert, der größer als ein Wert ist, aktiviert dies. Überprüfen Sie das MaxAnisotropy-Flag in der [**D3DCAPS9-Struktur,**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) um den möglichen Wertebereich für den Grad der Anisotropie zu bestimmen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturfilterung](texture-filtering.md)
</dt> </dl>

 

 
