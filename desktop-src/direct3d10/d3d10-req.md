---
description: Ressourcen Einschränkungs Konstanten.
ms.assetid: a6bfba45-7a0c-4894-a0a6-ee468002175d
title: D3D10_REQ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1d6bf4f72c4ef09eafba3ee50659e5e6ffc682
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342269"
---
# <a name="d3d10_req"></a>D3d10 \_ req

Ressourcen Einschränkungs Konstanten.



| \#definieren                                      | Wert | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3d10 \_ req- \_ MIP- \_ Ebenen                       | 14    | Maximale Anzahl von MipMap-Ebenen, die eine Textur Ressource aufweisen kann.                                                                                                                                                                                                                                                                                                                                                                    |
| D3d10 \_ req- \_ Ressourcen \_ Größe \_ in \_ Megabyte     | 128   | Maximal mögliche Größe einer Ressource in Megabyte. Apps können Ressourcen erstellen, die größer als die maximale Ressourcen Größe auf einigen Grafikhardware sind. Es wird jedoch empfohlen, dass apps Ressourcen kleiner als die maximale Ressourcen Größe behalten, um die maximale Menge an Kompatibilität über Grafik Anbieter hinweg zu erhalten. Die Laufzeit gewährleistet nur, dass Belegungen innerhalb der maximalen Ressourcen Größe von allen Direct3D 10-Hardware unterstützt werden. |
| D3d10 \_ req \_ TEXTURE1D \_ array \_ Achsen \_ Dimension | 512   | Maximale Array Größe eines 1D-Textur Arrays.                                                                                                                                                                                                                                                                                                                                                                                       |
| D3d10 \_ req \_ TEXTURE2D \_ array \_ Achsen \_ Dimension | 512   | Maximale Array Größe eines 2D-Textur Arrays.                                                                                                                                                                                                                                                                                                                                                                                       |
| D3d10 \_ req \_ TEXTURE1D \_ U- \_ Dimension           | 8192  | Maximale Breite einer 1D-Textur.                                                                                                                                                                                                                                                                                                                                                                                                  |
| D3d10 \_ req \_ TEXTURE2D \_ U \_ oder \_ V- \_ Dimension    | 8192  | Maximale Breite und Höhe einer 2D-Textur.                                                                                                                                                                                                                                                                                                                                                                                       |
| D3d10 \_ req \_ TEXTURE3D \_ U \_ V- \_ oder \_ W- \_ Dimension | 2048  | Maximale Breite, Höhe und Tiefe einer 3D-Textur.                                                                                                                                                                                                                                                                                                                                                                               |
| D3d10 \_ req \_ texturecube- \_ Dimension            | 8192  | Maximale Größe einer Cube-Textur.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Die Konstanten werden in d3d10. h definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen Konstanten](d3d10-graphics-reference-resource-constants.md)
</dt> <dt>

[Direct3D-Referenz](d3d10-graphics-reference-d3d10.md)
</dt> </dl>

 

 



