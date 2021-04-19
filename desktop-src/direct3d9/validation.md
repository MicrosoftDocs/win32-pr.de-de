---
description: Die Validierung wird während der Kompilierung durchgeführt. Um das aktuelle Verfahren zu überprüfen, geben Sie NULL als Technik Handle an, das überprüft werden soll.
ms.assetid: d1268f68-2893-4d7f-acd2-484346a20193
title: Validierung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc64a17aba21af4b43bd41cc060a8711e5bb4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345586"
---
# <a name="validation-direct3d-9"></a>Validierung (Direct3D 9)

Die Validierung wird während der Kompilierung durchgeführt. Um das aktuelle Verfahren zu überprüfen, geben Sie **null** als Technik Handle an, das überprüft werden soll.

Die Überprüfung kann für folgende Aktionen nicht ausgeführt werden:

-   , Wenn das angegebene Techniken Handle nicht vorhanden ist.
-   Wenn die Anwendung eines beliebigen Zustands in einem beliebigen Schritt der Technik fehlschlägt.
-   , Wenn die Gerätevalidierung nach der Anwendung aller Zustände in einem beliebigen Schritt der Technik fehlschlägt.
-   Wenn dem Pixelshader-oder dem Vertexshader-Effekt Status bei jedem Durchlauf der Technik ungültige Shader zugewiesen werden.
-   Wenn die Geräte Obergrenzen die cubezuordnung nicht unterstützen, und einem textureffekt Zustand wird ein Wert des Typs "texturecube" bei jedem Durchlauf der Technik zugewiesen.
-   Wenn die Geräte Obergrenzen die volumezuordnung nicht unterstützen und in jedem Durchlauf der Technik ein Wert vom Typ texture3D zugewiesen wird.

Weitere Informationen finden Sie unter [Effect States (Direct3D 9)](effect-states.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekt Format](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



