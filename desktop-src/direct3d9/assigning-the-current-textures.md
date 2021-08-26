---
description: Direct3D verwaltet eine Liste mit bis zu acht aktuellen Texturen. Sie kombiniert diese Texturen mit allen primitiven Texturen, die sie rendert. In den aktuellen Texturen können nur Texturen verwendet werden, die als Texturschnittstellenzeiger erstellt wurden.
ms.assetid: 5a58c915-7b67-45a7-9493-6657c75aaa10
title: Zuweisen der aktuellen Texturen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b2a9ac0b61f7a7d0a9b3ee27c7a9b7e6b8cd4d48fda33959462e26ad6958ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069420"
---
# <a name="assigning-the-current-textures-direct3d-9"></a>Zuweisen der aktuellen Texturen (Direct3D 9)

Direct3D verwaltet eine Liste mit bis zu acht aktuellen Texturen. Sie kombiniert diese Texturen mit allen primitiven Texturen, die sie rendert. In den aktuellen Texturen können nur Texturen verwendet werden, die als Texturschnittstellenzeiger erstellt wurden.

Anwendungen rufen die [**IDirect3DDevice9::SetTexture-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) auf, um textures dem Satz aktueller Texturen zuzuweisen. Der erste Parameter muss eine Zahl im Bereich von 0 bis 7 (einschließlich) sein. Übergeben Sie den Texturschnittstellenzeiger als zweiten Parameter.

Im folgenden C++-Codebeispiel wird veranschaulicht, wie eine Textur dem Satz aktueller Texturen zugewiesen werden kann.


```
// This code example assumes that the variable lpd3dDev is a
// valid pointer to an IDirect3DDevice9 interface and pTexture
// is a valid pointer to an IDirect3DBaseTexture9 interface.

// Set the third texture.
d3dDevice->SetTexture(2, pTexture);
```



> [!Note]  
> Softwaregeräte unterstützen nicht das Zuweisen einer Textur zu mehreren Texturphasen gleichzeitig.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturmischung](texture-blending.md)
</dt> </dl>

 

 
