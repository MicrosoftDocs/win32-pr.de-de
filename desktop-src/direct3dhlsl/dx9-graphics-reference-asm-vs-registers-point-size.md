---
title: Punktgröße registrieren
description: Dieses Vertex-Shader-Ausgabe Register enthält Daten pro Scheitelpunkt Größe.
ms.assetid: 1aa6cd7d-9d29-4e7e-8448-8b9a6b251a02
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36dbc6dc20d61baf4e0820dd0b6e10d3e6e918ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388219"
---
# <a name="point-size-register"></a>Punktgröße registrieren

Dieses Vertex-Shader-Ausgabe Register enthält Daten pro Scheitelpunkt Größe.



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Punktgröße registrieren    | x    | x    | x     | x    | x    | x     |



 

Ein Register besteht aus Eigenschaften, die bestimmen, wie sich die einzelnen Register Verhalten.



| Eigenschaft        | BESCHREIBUNG                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Name            | oPts                                                                                            |
| Anzahl           | 1 Vektor, von dem nur eine Komponente verwendet werden kann und die von der Komponenten Maske angegeben werden muss. |
| E/a-Berechtigungen | Nur Schreibzugriff.                                                                                     |



 

Es wird nur die skalare x-Komponente der Punktgröße verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Register](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




