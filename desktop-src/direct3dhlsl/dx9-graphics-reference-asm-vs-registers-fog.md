---
title: Nebelregister
description: Dieses Vertex-Shader-Ausgabe Register enthält eine pro-Scheitelpunkt-Nebelfarbe.
ms.assetid: b2b06aa9-ad75-48df-857d-fd8719176713
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c3f0e39c0670176b6233f61f0ba50596c92ca4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976104"
---
# <a name="fog-register"></a>Nebelregister

Dieses Vertex-Shader-Ausgabe Register enthält eine pro-Scheitelpunkt-Nebelfarbe.

Ein Register besteht aus Eigenschaften, die bestimmen, wie sich die einzelnen Register Verhalten.



| Eigenschaft        | BESCHREIBUNG                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Name            | onebel                                                                                            |
| Anzahl           | Ein Vektor, von dem nur eine Komponente verwendet werden kann und die von der Komponenten Maske angegeben werden muss |
| E/a-Berechtigungen | Nur Schreibzugriff.                                                                                     |



 

Der Ausgabe Nebel Wert wird registriert. Der Wert ist der zu interinterdende Nebel Faktor und wird dann an die Tabelle mit den Nebel geroutet. Es wird nur die skalarx-Komponente des Nebels verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Register](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




