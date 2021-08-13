---
description: Wird von einem Schnittpunkt-Shader aufgerufen, um eine Strahlschnittmenge zu melden.
ms.assetid: ''
title: ReportHit-Funktion
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportHit
api_type:
- NA
ms.openlocfilehash: 8714cabc02f70ca12bcc78493de3a61482ba5aed5490087d309f6ec091cecf75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118528108"
---
# <a name="reporthit-function"></a>ReportHit-Funktion

Wird von einem [Schnittpunkt-Shader aufgerufen,](intersection-shader.md) um eine Schnittmenge des Strahls zu melden.

## <a name="syntax"></a>Syntax
Diese systeminterne Funktionsdefinition entspricht der folgenden Funktionsvorlage:

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a>Parameter

`THit`

Ein float-Wert, der den parametrischen Abstand der Schnittmenge an..

`HitKind`

Eine ganze Zahl ohne Vorzeichen, die den Typ des aufgetretenen Treffers angibt.  Dies ist ein vom Benutzer angegebener Wert im Bereich von 0 bis 127.  Der Wert kann von jedem Treffer- [oder](any-hit-shader.md) [nächstgelegenen](closest-hit-shader.md) Treffer-Shader mit der **Systeminternen HitKind gelesen** werden.

`Attributes`

Die benutzerdefinierte Struktur der [**Schnittmengenattributstruktur,**](intersection-attributes.md) die die Schnittmengenattribute an gibt.  

## <a name="return-value"></a>Rückgabewert

**bool** TRUE, wenn der Treffer akzeptiert wurde.  Ein Treffer wird abgelehnt, wenn *THit* außerhalb des aktuellen Rayintervalls liegt oder der beliebige Treffer-Shader [**IgnoreHit aufruft.**](ignorehit-function.md)  Das aktuelle Rayintervall wird durch **RayTMin und** **RayTCurrent definiert.**

## <a name="remarks"></a>Hinweise

Diese Funktion kann von den folgenden Raytracing-Shadertypen aufgerufen werden:

* [**Intersection-Shader**](intersection-shader.md)





## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




