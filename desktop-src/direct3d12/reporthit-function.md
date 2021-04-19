---
description: Wird von einem Schnittmengen-Shader aufgerufen, um eine Strahl Überschneidung zu melden.
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
ms.openlocfilehash: 58d109f184974f76c533aaeee055f1ebf21d10eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343195"
---
# <a name="reporthit-function"></a>ReportHit-Funktion

Wird von einem [Schnittmengen-Shader](intersection-shader.md) aufgerufen, um eine Strahl Überschneidung zu melden.

## <a name="syntax"></a>Syntax
Diese intrinsische Funktionsdefinition entspricht der folgenden Funktions Vorlage:

```
template<attr_t>
bool ReportHit(float THit, uint HitKind, attr_t Attributes);
```



## <a name="parameters"></a>Parameter

`THit`

Ein float-Wert, der den parametrischen Abstand der Schnittmenge angibt.

`HitKind`

Eine Ganzzahl ohne Vorzeichen, die den Typ des aufgetretenen Treffer identifiziert.  Dies ist ein vom Benutzer angegebener Wert im Bereich von 0-127.  Der Wert kann von [jeder Treffer](any-hit-shader.md) -oder [nächster Treffer](closest-hit-shader.md) -Shader mit der systeminternen Funktion " **hitkind** " gelesen werden.

`Attributes`

Die benutzerdefinierte Schnittmengen- [**Attribut Struktur**](intersection-attributes.md) Struktur, die die Schnittmengen Attribute angibt.  

## <a name="return-value"></a>Rückgabewert

**bool** True, wenn der Treffer akzeptiert wurde.  Ein Treffer wird zurückgewiesen *, wenn der* Wert außerhalb des aktuellen Ray-Intervalls liegt oder der any Hit-Shader [**ignorehit**](ignorehit-function.md)aufruft.  Das aktuelle Ray-Intervall wird durch **raytmin** und **raytcurrent** definiert.

## <a name="remarks"></a>Bemerkungen

Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:

* [**Intersection-Shader**](intersection-shader.md)





## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




