---
description: Die Überprüfung wird während der Effektkompilierung ausgeführt. Um die aktuelle Technik zu überprüfen, geben Sie NULL als zu überprüfenden Technikhandle an.
ms.assetid: d1268f68-2893-4d7f-acd2-484346a20193
title: Überprüfung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d6c49f3bdf3bc0ba75f52bd8138fa6f5d777c3613d105b2706929c01b3ee4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519439"
---
# <a name="validation-direct3d-9"></a>Überprüfung (Direct3D 9)

Die Überprüfung wird während der Effektkompilierung ausgeführt. Um die aktuelle Technik zu überprüfen, geben Sie **NULL** als zu überprüfenden Technikhandle an.

Die Überprüfung schlägt für einen der folgenden Punkte fehl:

-   Wenn das angegebene Technikhandle nicht vorhanden ist.
-   Wenn die Anwendung eines Zustands in einem Durchlauf der Technik fehlschlägt.
-   Wenn die Geräteüberprüfung nach der Anwendung aller Zustände in einem Durchlauf der Technik fehlschlägt.
-   Wenn den Pixelshader- oder VERTEXSHADER-Effektzuständen ungültige Shader in einem Durchlauf der Technik zugewiesen werden.
-   Wenn die Geräteobergrenzen keine Cubezuordnung unterstützen und einem TEXTURE-Effektzustand in jedem Durchlauf der Technik ein Wert vom Typ textureCUBE zugewiesen wird.
-   Wenn die Geräteobergrenzen keine Volumezuordnung unterstützen und einem TEXTURE-Effektzustand in jedem Durchlauf der Technik ein Wert vom Typ texture3D zugewiesen wird.

Weitere Informationen finden Sie unter [Effect States (Direct3D 9)](effect-states.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effektformat](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



