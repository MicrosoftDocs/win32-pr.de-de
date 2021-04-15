---
description: Diese Vorlage wird nur in Netzen, die exportierte skinsinformationen enthalten, pro Mesh instanziiert. Der Zweck dieser Vorlage besteht darin, Informationen über die Art der exportierten Informationen zu den zu exportierenden Informationen bereitzustellen.
ms.assetid: 95a4fa45-63d1-4931-9c91-b26807d2b043
title: Xskinmeshheader
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306f8c183086846fca020040af00b9ccef2665cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392785"
---
# <a name="xskinmeshheader"></a>Xskinmeshheader

Diese Vorlage wird nur in Netzen, die exportierte skinsinformationen enthalten, pro Mesh instanziiert. Der Zweck dieser Vorlage besteht darin, Informationen über die Art der exportierten Informationen zu den zu exportierenden Informationen bereitzustellen.

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

-   nmaxskinweightspervertex: maximale Anzahl von Transformationen, die einen Scheitelpunkt im Mesh beeinflussen.
-   nmaxskinweightsperface: maximale Anzahl eindeutiger Transformationen, die die drei Scheitel Punkte beliebiger Gesichter beeinflussen.
-   nbones: die Anzahl der Knochen, die die Scheitel Punkte in diesem Mesh beeinflussen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



