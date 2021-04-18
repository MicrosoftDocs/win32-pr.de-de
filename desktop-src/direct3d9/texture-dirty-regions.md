---
description: Anwendungen können optimieren, welche Teilmenge einer Textur kopiert wird, indem Sie &\# 0034; Dirty&\# 0034; Bereiche in Texturen angeben.
ms.assetid: 102081bc-d5d5-4ec1-b935-00d4eda8f470
title: Struktur Änderungs Bereiche (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e3f1ce350a2728c99c49455b5fb8b638c47d10
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344570"
---
# <a name="texture-dirty-regions-direct3d-9"></a>Struktur Änderungs Bereiche (Direct3D 9)

Anwendungen können optimieren, welche Teilmenge einer Textur kopiert wird, indem Sie "Dirty"-Bereiche in Texturen angeben. Nur die als geändert markierten Regionen werden durch einen [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture)-Aufrufwert kopiert. Die geänderten Bereiche können jedoch erweitert werden, um die Ausrichtung zu optimieren. Wenn eine Textur erstellt wird, wird die gesamte Textur als geändert betrachtet. Nur die folgenden Vorgänge wirken sich auf den geänderten Zustand einer Textur aus:

-   Hinzufügen eines geänderten Bereichs zu einer Textur
-   Sperren eines Puffers in der Textur. Mit diesem Vorgang wird der gesperrte Bereich als Änderungs Bereich hinzugefügt. Die Anwendung kann diese automatische Aktualisierung von Änderungs Regionen deaktivieren, wenn Sie über bessere Kenntnisse der tatsächlich geänderten Regionen verfügt.
-   Durch die Verwendung einer Oberflächenebene der Textur als Ziel in [**IDirect3DDevice9:: updatesurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) wird die gesamte Textur als geändert markiert.
-   Durch die Verwendung der Textur als Quelle in [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) werden alle geänderten Bereiche in der Quell Textur gelöscht.
-   Verwenden von [**IDirect3DSurface9:: GetDC**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdc) zum Zurückgeben eines Geräte Kontexts.
-   Durch Aufrufen von [**IDirect3DBaseTexture9:: generatemipsublevels**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-generatemipsublevels) wird die gesamte Textur als geändert markiert.
-   Durch den Aufruf von [**IDirect3DBaseTexture9:: settautogenfiltertype**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dbasetexture9-setautogenfiltertype) wird die gesamte Textur als geändert markiert.

Geänderte Bereiche werden auf der obersten Ebene einer mipzugeordneten Textur festgelegt, und [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) kann den geänderten Bereich in der MIP-Kette vergrößern, um die Anzahl der für jede Unterebene kopierten Bytes zu minimieren. Beachten Sie, dass die Koordinaten der untergeordneten Ebene für geänderte Bereiche gerundet werden, d. h., dass Ihre Bruchteile auf den nächsten Rand der Textur gerundet werden.

Da jeder Typ der Textur verschiedene Typen von Änderungs Bereichen hat, gibt es Methoden für jeden Texttyp. 2D-Texturen verwenden ein Dirty Rechteck und volumetexturen verwenden Felder.

-   [**IDirect3DCubeTexture9:: AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-adddirtyrect)
-   [**IDirect3DTexture9:: AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect)
-   [**IDirect3DVolumeTexture9:: adddirtybox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox)

Wenn **null** für die Parameter pdirtyrect oder pdirtybox für die oben genannten Methoden übergeben wird, wird der geänderte Bereich erweitert, sodass die gesamte Textur abgedeckt wird.

Jede Lock-Methode kann D3DLOCK \_ No \_ Dirty \_ Update verwenden, was Änderungen am geänderten Zustand der Textur verhindert. Weitere Informationen finden Sie unter [Sperren von Ressourcen (Direct3D 9)](locking-resources.md).

Wenn weitere Informationen über die tatsächliche Gruppe von Regionen verfügbar sind, die während eines Sperr Vorgangs geändert werden, sollten Anwendungen D3DLOCK \_ No \_ Dirty \_ Update verwenden. Beachten Sie, dass eine Sperre oder eine Kopie in eine Textur Unterebene (d. h. ohne Sperren oder Kopieren auf der obersten Ebene) nicht die geänderten Bereiche für diese Textur aktualisiert. Anwendungen nehmen die gleiche Verantwortung für die Aktualisierung von Änderungs Regionen an, wenn Sie niedrigere Ebenen sperren, ohne die oberste Ebene zu sperren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende Konzepte der Texturierung](basic-texturing-concepts.md)
</dt> </dl>

 

 
