---
title: Fog Register
description: Dieses Vertex-Shader-Ausgaberegister enthält eine Scheitelpunktfarbe pro Scheitelpunkt.
ms.assetid: b2b06aa9-ad75-48df-857d-fd8719176713
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b6aeaea0e51960f8f4bf768b855ac31236b2bb330cfda3390fd9e61dab4ec1f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854580"
---
# <a name="fog-register"></a>Fog Register

Dieses Vertex-Shader-Ausgaberegister enthält eine Scheitelpunktfarbe pro Scheitelpunkt.

Ein Register besteht aus Eigenschaften, die bestimmen, wie sich jedes Register verhält.



| Eigenschaft        | Beschreibung                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Name            | oFog                                                                                            |
| Anzahl           | Ein Vektor, von dem nur eine Komponente verwendet werden kann und die von der Komponentenmaske angegeben werden muss |
| E/A-Berechtigungen | Nur Schreibzugriff.                                                                                     |



 

Der Ausgabewert wird registriert. Der Wert ist der Zudingfaktor, der interpoliert und dann an die Tabellentabelle "Table" (Tafel) geroutet werden soll. Es wird nur die skalare x-Komponente des Skalars verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




