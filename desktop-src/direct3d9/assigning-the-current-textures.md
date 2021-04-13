---
description: Direct3D verwaltet eine Liste mit bis zu acht aktuellen Texturen. Diese Texturen werden in alle primitiven, die gerendert werden, kombiniert. Nur Texturen, die als Textur Schnittstellen Zeiger erstellt wurden, können im Satz der aktuellen Texturen verwendet werden.
ms.assetid: 5a58c915-7b67-45a7-9493-6657c75aaa10
title: Zuweisen der aktuellen Texturen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7ae6d603d9547841628f9395889095533cf3e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483982"
---
# <a name="assigning-the-current-textures-direct3d-9"></a>Zuweisen der aktuellen Texturen (Direct3D 9)

Direct3D verwaltet eine Liste mit bis zu acht aktuellen Texturen. Diese Texturen werden in alle primitiven, die gerendert werden, kombiniert. Nur Texturen, die als Textur Schnittstellen Zeiger erstellt wurden, können im Satz der aktuellen Texturen verwendet werden.

Anwendungen aufrufen die [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) -Methode, um Texturen dem Satz der aktuellen Texturen zuzuweisen. Der erste Parameter muss eine Zahl im Bereich von 0-7 (einschließlich) sein. Übergeben Sie den Textur Schnittstellen Zeiger als zweiten Parameter.

Im folgenden C++-Codebeispiel wird veranschaulicht, wie eine Textur dem Satz aktueller Texturen zugewiesen werden kann.


```
// This code example assumes that the variable lpd3dDev is a
// valid pointer to an IDirect3DDevice9 interface and pTexture
// is a valid pointer to an IDirect3DBaseTexture9 interface.

// Set the third texture.
d3dDevice->SetTexture(2, pTexture);
```



> [!Note]  
> Software Geräte unterstützen das Zuweisen einer Textur zu mehr als einer Textur Phase nicht gleichzeitig.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textur Mischung](texture-blending.md)
</dt> </dl>

 

 
