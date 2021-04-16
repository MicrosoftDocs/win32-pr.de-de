---
description: Direct3D verwendet eine Form der linearen Textur Filterung namens bilineare Filtering.
ms.assetid: vs|directx_sdk|~\linear_texture_filtering.htm
title: Lineare Textur Filterung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7940bd693ec42ef4f48920a5a362fad5f5b0bf02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521928"
---
# <a name="linear-texture-filtering-direct3d-9"></a>Lineare Textur Filterung (Direct3D 9)

Direct3D verwendet eine Form der linearen Textur Filterung namens bilineare Filtering. Wie bei der ersten [Stichprobenentnahme (Direct3D 9)](nearest-point-sampling.md)berechnet die bilineare Textur Filterung zuerst eine texturadresse, die in der Regel keine ganzzahlige Adresse ist. Die bilineare Filterung findet dann den textexaus, dessen ganzzahlige Adresse der berechneten Adresse am nächsten liegt. Außerdem berechnet das Direct3D-Renderingmodul einen gewichteten Durchschnitt der texeln direkt oberhalb von, Links von und rechts neben dem nächsten Beispiel Punkt.

Wählen Sie die bilineare Textur Filterung aus, indem Sie die [**IDirect3DDevice9:: setsamplerstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) -Methode aufrufen. Legen Sie den Wert des ersten Parameters auf die ganzzahlige Indexnummer (0-7) der Textur fest, für die Sie eine Textur Filterungs Methode auswählen. Übergeben \_ Sie D3DSAMP MagFilter, D3DSAMP \_ MinFilter oder D3DSAMP \_ MipFilter für den zweiten Parameter, um den Filter für die Vergrößerung, minifizierung oder den Mipmapping-Filter festzulegen. Übergeben Sie D3DTEXF \_ linear im dritten Parameter.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textur Filterung](texture-filtering.md)
</dt> </dl>

 

 
