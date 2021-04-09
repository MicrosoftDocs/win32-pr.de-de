---
description: Die aktuelle Hardware implementiert nicht notwendigerweise alle Funktionen, die von der Direct3D-Schnittstelle aktiviert werden. Die Anwendung muss die Benutzer Hardware testen und die renderingstrategien entsprechend anpassen.
ms.assetid: 7b5f586c-616c-4351-b6b9-5c0179db5d8b
title: Überlegungen zur Hardware für die Texturierung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f1ba8bea85cc3657478767aac7c7ffc2abebbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859942"
---
# <a name="hardware-considerations-for-texturing-direct3d-9"></a>Überlegungen zur Hardware für die Texturierung (Direct3D 9)

Die aktuelle Hardware implementiert nicht notwendigerweise alle Funktionen, die von der Direct3D-Schnittstelle aktiviert werden. Die Anwendung muss die Benutzer Hardware testen und die renderingstrategien entsprechend anpassen.

Viele 3D-Zugriffstasten bieten keine Unterstützung für diffuse Iterierte Werte als Argumente für das Mischen von Einheiten. Die Anwendung kann jedoch Iterierte Farbdaten einführen, wenn Sie Textur Mischungs Vorgänge durchführt.

Bei einigen 3D-Hardware ist möglicherweise keine Mischungs Stufe mit der ersten Textur verknüpft. Auf diesen Adaptern muss Ihre Anwendung in den zweiten und dritten Textur Stufen in der Menge der aktuellen Texturen gemischt werden.

Aufgrund von Einschränkungen in der heutigen Hardware können einige Anzeige Adapter eine drei lineare MipMap-interpolung durch die von [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)angebotene Schnittstelle für mehrere Textur blending ausführen. Die Anwendung kann Multipass-Textur Mischungs Zeichen verwenden, um die gleichen Effekte zu erzielen, oder Sie wird auf den D3DTEXF \_ Point Mipmap-Filter Modus herabgestuft, der häufig unterstützt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
