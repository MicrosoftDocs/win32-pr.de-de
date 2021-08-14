---
description: Definiert einen Koordinatenrahmen oder &\# 0034;Referenzrahmen.&\# 0034; Die Frame-Vorlage ist geöffnet und kann ein beliebiges Objekt enthalten. Die D3DX-Funktionen zum Laden von Gitternetzen erkennen Mesh-, FrameTransformMatrix- und Frame-Vorlageninstanzen als untergeordnete Objekte beim Laden einer Frame-Instanz.
ms.assetid: vs|directx_sdk|~\frame.htm
title: Frame (Direct3D 9-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff77cc6f4618b3ded3afc9453c12a96b115ec4bfe0f90cb83a92826378212c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523033"
---
# <a name="frame-direct3d-9-graphics"></a>Frame (Direct3D 9-Grafiken)

Definiert einen Koordinatenrahmen oder "Referenzrahmen". Die Frame-Vorlage ist geöffnet und kann ein beliebiges Objekt enthalten. Die D3DX-Mesh-Loading-Funktionen erkennen [**Mesh-,**](mesh.md) [**FrameTransformMatrix-**](frametransformmatrix.md)und Frame-Vorlageninstanzen als untergeordnete Objekte beim Laden einer  **Frame-Instanz.**

``` syntax
template Frame
{
    < 3D82AB46-62DA-11CF-AB39-0020AF71E433 >
    [...]           
} 
```

Die Framevorlage erkennt untergeordnete **Frame-** und [**Mesh-Knoten**](mesh.md) innerhalb eines Frames und kann benutzerdefinierte Vorlagen über eine Rückruffunktion erkennen.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



