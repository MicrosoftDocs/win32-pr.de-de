---
description: Ressourceneinschränkungskonstanten.
ms.assetid: a6bfba45-7a0c-4894-a0a6-ee468002175d
title: D3D10_REQ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e099c26706772bbb76ad6709759fa4712e22ea3bc9793b905a2050f25d0f75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118100752"
---
# <a name="d3d10_req"></a>D3D10 \_ REQ

Ressourceneinschränkungskonstanten.



| \#Definieren                                      | Wert | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ REQ \_ \_ MIP-EBENEN                       | 14    | Maximale Anzahl von Mipmapebenen, die eine Texturressource aufweisen kann.                                                                                                                                                                                                                                                                                                                                                                    |
| D3D10 \_ REQ \_ RESOURCE \_ SIZE \_ IN \_ MEGABYTES     | 128   | Maximale Größe einer Ressource in Megabyte. Apps können Ressourcen erstellen, die auf einigen Grafikhardware größer als die maximale Ressourcengröße sind. Es wird jedoch empfohlen, dass Apps Ressourcen kleiner als die maximale Ressourcengröße halten, um die maximale Kompatibilität zwischen Grafikanbietern zu erzielen. Die Runtime garantiert nur, dass Zuordnungen innerhalb der maximalen Ressourcengröße von der gesamten Direct3D 10-Hardware unterstützt werden. |
| DIMENSION DER D3D10 \_ REQ \_ TEXTURE1D-ARRAYACHSE \_ \_ \_ | 512   | Maximale Arraygröße eines 1D-Texturarrays.                                                                                                                                                                                                                                                                                                                                                                                       |
| DIMENSION DER D3D10 \_ REQ \_ TEXTURE2D-ARRAYACHSE \_ \_ \_ | 512   | Maximale Arraygröße eines 2D-Texturarrays.                                                                                                                                                                                                                                                                                                                                                                                       |
| D3D10 \_ REQ \_ TEXTURE1D \_ U \_ DIMENSION           | 8192  | Maximale Breite einer 1D-Textur.                                                                                                                                                                                                                                                                                                                                                                                                  |
| D3D10 \_ REQ \_ TEXTURE2D \_ \_ U- ODER \_ \_ V-DIMENSION    | 8192  | Maximale Breite und Höhe einer 2D-Textur.                                                                                                                                                                                                                                                                                                                                                                                       |
| D3D10 \_ REQ \_ TEXTURE3D \_ U V ODER W \_ \_ \_ \_ DIMENSION | 2048  | Maximale Breite, Höhe und Tiefe einer 3D-Textur.                                                                                                                                                                                                                                                                                                                                                                               |
| D3D10 \_ REQ \_ TEXTURECUBE \_ DIMENSION            | 8192  | Maximale Größe einer Cubetextur.                                                                                                                                                                                                                                                                                                                                                                                                 |



 

Die Konstanten werden in D3D10.h definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcenkonstanten](d3d10-graphics-reference-resource-constants.md)
</dt> <dt>

[Direct3D-Referenz](d3d10-graphics-reference-d3d10.md)
</dt> </dl>

 

 



