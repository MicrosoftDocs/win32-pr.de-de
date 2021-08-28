---
description: Direct3D verwendet eine Form der linearen Texturfilterung, die als bilineare Filterung bezeichnet wird.
ms.assetid: vs|directx_sdk|~\linear_texture_filtering.htm
title: Lineare Texturfilterung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf5177af653c74383ef87468dbb43167fa2962cd093410a6a63f85da2233e3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628530"
---
# <a name="linear-texture-filtering-direct3d-9"></a>Lineare Texturfilterung (Direct3D 9)

Direct3D verwendet eine Form der linearen Texturfilterung, die als bilineare Filterung bezeichnet wird. Wie [bei nearest-point Sampling (Direct3D 9)](nearest-point-sampling.md)berechnet die bilineare Texturfilterung zunächst eine Texeladresse, die in der Regel keine ganzzahlige Adresse ist. Die bilineare Filterung sucht dann nach dem Texel, dessen ganzzahlige Adresse der berechneten Adresse am nächsten liegt. Darüber hinaus berechnet das Direct3D-Renderingmodul einen gewichteten Durchschnitt der Texel, die sich direkt über, unten, links von und rechts vom nächsten Beispielpunkt befinden.

Wählen Sie bilineare Texturfilterung aus, indem Sie die [**IDirect3DDevice9::SetSamplerState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) aufrufen. Legen Sie den Wert des ersten Parameters auf die ganzzahlige Indexnummer (0-7) der Textur fest, für die Sie eine Texturfilterungsmethode auswählen. Übergeben Sie D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER oder D3DSAMP \_ MIPFILTER für den zweiten Parameter, um den Filter für Vergrößerung, Vergrößerung oder Mipmapping festzulegen. Übergeben Sie D3DTEXF \_ LINEAR im dritten Parameter.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturfilterung](texture-filtering.md)
</dt> </dl>

 

 
