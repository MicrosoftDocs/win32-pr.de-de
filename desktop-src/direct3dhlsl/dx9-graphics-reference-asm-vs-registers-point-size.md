---
title: Punktgrößenregister
description: Dieses Vertex-Shader-Ausgaberegister enthält Daten zur Größe pro Scheitelpunkt.
ms.assetid: 1aa6cd7d-9d29-4e7e-8448-8b9a6b251a02
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6de5c2fba55ce9cdfcee535ec001a89cbebcdddc5e3685224f9eb0c560870534
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119664"
---
# <a name="point-size-register"></a>Punktgrößenregister

Dieses Vertex-Shader-Ausgaberegister enthält Daten zur Größe pro Scheitelpunkt.



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Punktgrößenregister    | x    | x    | x     | x    | x    | x     |



 

Ein Register besteht aus Eigenschaften, die bestimmen, wie sich die einzelnen Register verhalten.



| Eigenschaft        | Beschreibung                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Name            | Setzt                                                                                            |
| Anzahl           | 1 Vektor, von dem nur eine Komponente verwendet werden kann und der von der Komponentenmaske angegeben werden muss. |
| E/A-Berechtigungen | Nur Schreibzugriff.                                                                                     |



 

Es wird nur die skalare x-Komponente der Punktgröße verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




