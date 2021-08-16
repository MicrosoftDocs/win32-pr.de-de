---
description: Die aktuelle Hardware implementiert nicht notwendigerweise alle Funktionen, die die Direct3D-Schnittstelle aktiviert. Ihre Anwendung muss die Benutzerhardware testen und ihre Renderingstrategien entsprechend anpassen.
ms.assetid: 7b5f586c-616c-4351-b6b9-5c0179db5d8b
title: Hardwareüberlegungen zur Texturierung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41344d1ee091a1d2d619e366de549d58b69aebf234b89b6cf8115511703b799
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522801"
---
# <a name="hardware-considerations-for-texturing-direct3d-9"></a>Hardwareüberlegungen zur Texturierung (Direct3D 9)

Die aktuelle Hardware implementiert nicht notwendigerweise alle Funktionen, die die Direct3D-Schnittstelle aktiviert. Ihre Anwendung muss die Benutzerhardware testen und ihre Renderingstrategien entsprechend anpassen.

Viele 3D-Zugriffstastenkarten unterstützen keine diffusen iterierten Werte als Argumente für Mischungseinheiten. Ihre Anwendung kann jedoch iterierte Farbdaten einführen, wenn eine Texturmischung durchgeführt wird.

Einige 3D-Hardware verfügt möglicherweise nicht über eine Mischungsphase, die der ersten Textur zugeordnet ist. Auf diesen Adaptern muss Ihre Anwendung eine Mischung in der zweiten und dritten Texturphase der aktuellen Texturen ausführen.

Aufgrund von Einschränkungen in einem Großteil der heutigen Hardware können nur wenige Grafikkarten die trilineare Mipmap-Interpolation über die von [**IDirect3DDevice9 angebotene**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)Schnittstelle zur Texturmischung durchführen. Ihre Anwendung kann multipass texture blending verwenden, um die gleichen Effekte zu erzielen, oder sie kann auf den Mipmapfiltermodus D3DTEXF POINT heruntergestuft \_ werden, der häufig unterstützt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
