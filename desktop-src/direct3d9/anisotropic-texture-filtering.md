---
description: Die in den texeln eines 3D-Objekts sichtbare Verzerrung, deren Oberfläche in Bezug auf die Ebene des Bildschirms an einem Winkel ausgerichtet ist, wird als Anisotropie bezeichnet.
ms.assetid: f6c8a9e2-aab0-4f06-956e-bb86557c72e7
title: Anisotrope Textur Filterung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3443696e54410c6edc6a9998d4fcfd86b537a0e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483750"
---
# <a name="anisotropic-texture-filtering-direct3d-9"></a>Anisotrope Textur Filterung (Direct3D 9)

Die in den texeln eines 3D-Objekts sichtbare Verzerrung, deren Oberfläche in Bezug auf die Ebene des Bildschirms an einem Winkel ausgerichtet ist, wird als Anisotropie bezeichnet. Wenn ein Pixel aus einem anisotrope-primitiv Texels zugeordnet wird, wird seine Form verzerrt. Direct3D misst die Anisotropie eines Pixels als Elongation, d. h. die Länge dividiert durch die Breite eines Bildschirm Pixels, das in den Textur Bereich umgekehrt zugeordnet ist.

Sie können die anisotrope Textur Filterung zusammen mit der linearen Textur Filterung oder der MipMap-Textur Filterung verwenden, um renderingergebnisse zu verbessern. Die Anwendung ermöglicht die anisotrope Textur Filterung durch Aufrufen der [**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) -Methode. Legen Sie den Wert des ersten Parameters auf die ganzzahlige Indexnummer (0-7) der Textur fest, für die Sie eine Textur Filterungs Methode auswählen. Übergeben \_ Sie D3DSAMP MagFilter, D3DSAMP \_ MinFilter oder D3DSAMP \_ MipFilter für den zweiten Parameter, um den Filter für die Vergrößerung, minifizierung oder den Mipmapping-Filter festzulegen. Legen Sie den dritten Parameter auf D3DTEXF \_ anisotrope fest.

Die Anwendung muss auch den Grad der Anisotropie auf einen Wert größer als 1 festlegen. Rufen Sie hierzu die [**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) -Methode auf. Legen Sie den Wert des ersten Parameters auf die ganzzahlige Indexnummer (0-7) der Textur fest, für die Sie den Grad der Isotropie festlegen. Übergeben Sie D3DSAMP \_ MaxAnisotropy als Wert des zweiten Parameters. Der letzte Parameter sollte der Grad der Isotropie sein.

Sie können die Isotropie Filterung deaktivieren, indem Sie den Grad der Isotropie auf einen Wert festlegen. Jeder Wert, der größer als 1 ist, aktiviert ihn. Überprüfen Sie das Flag MaxAnisotropy in der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur, um den möglichen Wertebereich für den Grad der Anisotropie zu ermitteln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textur Filterung](texture-filtering.md)
</dt> </dl>

 

 
