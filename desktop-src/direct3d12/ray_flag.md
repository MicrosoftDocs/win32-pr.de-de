---
description: Flags, die an die traceray-Funktion übergeben werden, um Transparenz, Vererbung und frühe Ausgabeverhalten zu überschreiben.
ms.assetid: ''
title: RAY_FLAG-Enumeration
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 31d6a002e5f3f4eeb5f86e671be0904d61cb916d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345625"
---
# <a name="ray_flag-enumeration"></a>Ray- \_ Flag-Enumeration

Flags, die an die [**traceray**](traceray-function.md) -Funktion übergeben werden, um Transparenz, Vererbung und frühe Ausgabeverhalten zu überschreiben.

## <a name="syntax"></a>Syntax


```
enum RAY_FLAG : uint
{
    RAY_FLAG_NONE                            = 0x00,
    RAY_FLAG_FORCE_OPAQUE                    = 0x01,
    RAY_FLAG_FORCE_NON_OPAQUE                = 0x02,
    RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH = 0x04,
    RAY_FLAG_SKIP_CLOSEST_HIT_SHADER         = 0x08,
    RAY_FLAG_CULL_BACK_FACING_TRIANGLES      = 0x10,
    RAY_FLAG_CULL_FRONT_FACING_TRIANGLES     = 0x20,
    RAY_FLAG_CULL_OPAQUE                     = 0x40,
    RAY_FLAG_CULL_NON_OPAQUE                 = 0x80,
}; 
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**Ray- \_ Flag \_ None**
</dt> <dd>

Es sind keine Optionen ausgewählt.

</dd> <dt>

<span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**Ray-Flag ist nicht transparent \_ \_ \_**
</dt> <dd>

Alle in einem Raytrace gefundenen Ray-primitive-Schnittmengen werden als nicht transparent behandelt.  Es werden also keine Treffer-Shader ausgeführt, unabhängig davon, ob die Treffer Geometrie das D3D12 \_ Raytracing \_ Geometry \_ -Flag nicht transparent angibt \_ und unabhängig von den instanzflags auf der Instanz, die getroffen wurde.

Dieses Flag schließt sich gegenseitig aus, dass die Ray \_ -Flag nicht deckend ist, dass das \_ \_ \_ Ray-Flag nicht transparent ist \_ und das \_ \_ Ray- \_ Flag \_ \_ nicht \_ deckend ist.


</dd> <dt>

<span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**Ray-Flag "nicht deckend" \_ \_ erzwingen \_ \_**
</dt> <dd>

Alle in einem Raytrace gefundenen Ray-primitive-Schnittmengen werden als nicht transparent behandelt.  Alle Treffer-Shader, falls vorhanden, werden ausgeführt, unabhängig davon, ob die Treffer Geometrie das D3D12 \_ Raytracing \_ Geometry-Flag nicht transparent angibt \_ \_ und unabhängig von den instanzflags auf der Instanz, die getroffen wurde.
Dieses Flag schließt sich gegenseitig mit dem Ray \_ \_ -Flag FORCE_ \transparent, dem Ray \_ \_ -Flag-cullflag und dem Ray \_ - \_ Flag \_ \_ nicht \_ deckend aus.


</dd> <dt>

<span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**Ray \_ -Flag " \_ \_ erste \_ Treffer \_ -und \_ \_ endsuche akzeptieren"**
</dt> <dd>

Die erste Strahl primitive Schnittmenge, die in einem Raytrace erkannt wird, bewirkt, dass " **Accept thitandendsearch** " unmittelbar nach dem beliebigen Treffer-Shader aufgerufen wird, einschließlich, wenn kein Treffer-Shader vorhanden ist. 
 
Die einzige Ausnahme ist, wenn der vorangehende Treffer-Shader **ignorehit** aufruft. in diesem Fall bleibt der Strahl unverändert, sodass der nächste Treffer zu einem anderen Kandidaten wird, der als erster Treffer fungiert.  Damit diese Ausnahme angewendet werden kann, muss der beliebige Treffer-Shader tatsächlich ausgeführt werden.  Wenn also der Treffer-Shader übersprungen wird, weil der Treffer als nicht transparent behandelt wird (z. b. weil das Flag für die ntflag-Flag "nicht transparent" \_ \_ oder " \_ D3D12 \_ Raytracing \_ Geometry Flag nicht transparent" oder das Flag " \_ \_ D3D12 \_ Raytracing- \_ \_ instanzflag nicht transparent" \_ festgelegt wird), wird " **Accepted**

Wenn beim ersten Treffer ein nächster Treffer-Shader vorhanden ist, wird er aufgerufen, es sei denn, das Ray- \_ Flag über \_ springt den \_ nächstgelegenen \_ Treffer- \_ Shader.  Der gefundene Treffer wird als "nächstgelegene" angesehen, auch wenn andere potenzielle Treffer, die möglicherweise näher am Strahl liegen, nicht besucht wurden.

Eine typische Verwendung für dieses Flag ist für Schatten, bei denen nur ein einziger Treffer gefunden werden muss.


</dd> <dt>

<span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**Ray- \_ Flag \_ Skip \_ nächster Treffer- \_ \_ Shader überspringen**
</dt> <dd>

Auch wenn für mindestens ein Treffer ein Commit ausgeführt wurde und die Treffer Gruppe für den nächstgelegenen Treffer einen nächsten Treffer-Shader enthält, überspringen Sie die Ausführung dieses Shaders. 

</dd> <dt>

<span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**Ray-Flag, das auf den \_ \_ \_ \_ \_ Dreiecke zurückgeht**
</dt> <dd>

Ermöglicht das Berechnen von zurück gerichteten Dreiecken. Siehe **D3D12 \_ Raytracing \_ - \_ instanzflags** , um auszuwählen, welche Dreiecke zurückstehen, pro Instanz.

Bei Instanzen, die D3D12 \_ Raytracing \_ instance \_ Flag- \_ Dreieck- \_ cull \_ Deaktivieren angeben, hat dieses Flag keine Auswirkungen.

Bei geometry-Typen außer D3D12 \_ Raytracing \_ Geometry \_ Type \_ Dreiecke hat dieses Flag keine Auswirkungen.

Dieses Flag schließt sich mit dem Ray-Flag für die Vorder-und-Ecke gegenseitig aus \_ \_ \_ \_ \_ .


</dd> <dt>

<span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**Ray- \_ Flag- \_ \_ Spitzen \_ \_ Ecke**
</dt> <dd>

Ermöglicht das Berechnen von Front-ELN-Dreiecke. Siehe **D3D12 \_ Raytracing \_ - \_ instanzflags** , um auszuwählen, welche Dreiecke zurückstehen, pro Instanz.

Bei Instanzen, die D3D12 \_ Raytracing \_ instance \_ Flag- \_ Dreieck- \_ cull \_ Deaktivieren angeben, hat dieses Flag keine Auswirkungen.

Bei geometry-Typen außer D3D12 \_ Raytracing \_ Geometry \_ Type \_ Dreiecke hat dieses Flag keine Auswirkungen.

Dieses Flag schließt sich mit dem Ray-Flag zurück, das auf \_ \_ \_ \_ \_ Dreiecke ausgerichtet ist.


</dd> <dt>

<span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**Das Ray-Flag ist nicht transparent. \_ \_ \_**
</dt> <dd>

Culls alle primitiven, die auf der Grundlage ihrer Geometry-und instanzflags als nicht transparent eingestuft werden.

Dieses Flag schließt sich gegenseitig aus, dass die Ray \_ \_ -Flag nicht transparent ist, dass die \_ Ray \_ -Flag nicht deckend ist und das \_ \_ \_ Ray- \_ Flag \_ \_ nicht \_ deckend ist.


</dd> <dt>

<span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**Das Ray- \_ Flag ist \_ \_ nicht \_ deckend.**
</dt> <dd>

Culls alle primitiven, die auf der Grundlage ihrer Geometry-und instanzflags als nicht transparent angesehen werden.

Dieses Flag schließt sich gegenseitig aus, wenn die Ray \_ \_ -Flag \_ \_ nicht transparent, Ray \_ -Flag nicht deckend \_ und Ray-Flag nicht transparent ist \_ \_ \_ \_ .


</dd>

## <a name="requirements"></a>Anforderungen



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




