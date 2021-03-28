---
title: SV_InsideTessFactor
description: Definiert den Mosaik Betrag innerhalb einer patchoberfläche.
ms.assetid: f0762aca-d84d-44c0-a163-9737ef92c1e5
keywords:
- SV_InsideTessFactor HLSL
topic_type:
- apiref
api_name:
- SV_InsideTessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a05cabbb9410136d2bd82ee272ad92ff1b1f430
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104976209"
---
# <a name="sv_insidetessfactor"></a>SV \_ insidetess Factor

Definiert den Mosaik Betrag innerhalb einer patchoberfläche.

## <a name="type"></a>Typ



|            |                |
|------------|----------------|
| Typ       | Eingabe Topologie |
| float \[ 2\] | Quad-Patch     |
| float      | Tri-Patch      |
| unused     | Isolation        |



 

Mosaik Faktoren müssen als Array deklariert werden. Sie können nicht in einen einzigen Vektor gepackt werden.

## <a name="remarks"></a>Bemerkungen

Dieser Wert muss während der Funktion Patch Constant des Hull-Shaders definiert werden.

Erforderlicher Ausgabewert für den Hull-Shader bei Verwendung von Quad-oder Tri-Patches. Bei diesem Wert handelt es sich um eine erforderliche Eingabe für den Domänen-Shader, damit die Hardware die Signaturen über den Mosaik Prozess abgleichen kann.

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Semantik](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




