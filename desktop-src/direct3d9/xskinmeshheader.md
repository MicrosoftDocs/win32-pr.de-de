---
description: Diese Vorlage wird pro Gitternetz nur in Gitternetzen instanziiert, die exportierte Skinninginformationen enthalten. Der Zweck dieser Vorlage besteht in der Bereitstellung von Informationen zur Art der exportierten Skinninginformationen.
ms.assetid: 95a4fa45-63d1-4931-9c91-b26807d2b043
title: XSkinMeshHeader
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c86127e46809cd1415b191a769b25e09535405e6500e511df6248e6174888d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796854"
---
# <a name="xskinmeshheader"></a>XSkinMeshHeader

Diese Vorlage wird pro Gitternetz nur in Gitternetzen instanziiert, die exportierte Skinninginformationen enthalten. Der Zweck dieser Vorlage besteht in der Bereitstellung von Informationen zur Art der exportierten Skinninginformationen.

``` syntax
template XSkinMeshHeader 
{ 
    < 3CF169CE-FF7C-44ab-93C0-F78F62D172E2 >  
    WORD nMaxSkinWeightsPerVertex; 
    WORD nMaxSkinWeightsPerFace; 
    WORD nBones; 
}
```

Hierbei gilt:

-   nMaxSkinWeightsPerVertex: Maximale Anzahl von Transformationen, die sich auf einen Scheitelpunkt im Gitternetz auswirken.
-   nMaxSkinWeightsPerFace: Maximale Anzahl eindeutiger Transformationen, die sich auf die drei Scheitelungen eines Gesichts auswirken.
-   nBones: Anzahl von Gittern, die Sich auf Scheitelungen in diesem Gitternetz auswirken.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



