---
description: Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen (Component Object Model), die von der D3DX-Hilfsprogrammbibliothek in Direct3D 10 Graphics bereitgestellt werden.
ms.assetid: c57d9c39-3f30-4205-9b0a-665fe53f2b14
title: D3DX-Schnittstellen (Direct3D 10-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c064edce5d5841875eb3148bf74b18f50f93081
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408013"
---
# <a name="d3dx-interfaces-direct3d-10-graphics"></a>D3DX-Schnittstellen (Direct3D 10-Grafiken)

Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen (Component Object Model), die von der D3DX-Hilfsprogrammbibliothek bereitgestellt werden. Die folgenden Schnittstellen werden mit der D3DX-Hilfsprogrammbibliothek verwendet.



| Schnittstellen                                                     | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3DX10DataLoader-Schnittstelle**](id3dx10dataloader.md)       | Datenladeobjekt, das von [**der ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) zum asynchronen Laden von Daten verwendet wird.<br/>                                                                                                                                                                                                                                                                                                   |
| [**ID3DX10DataProcessor-Schnittstelle**](id3dx10dataprocessor.md) | Datenverarbeitungsobjekt, das von [**der ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) zum asynchronen Verarbeiten geladener Daten verwendet wird.<br/>                                                                                                                                                                                                                                                                                      |
| [**ID3DX10Font-Schnittstelle**](id3dx10font.md)                   | Die ID3DX10Font-Schnittstelle kapselt die Texturen und Ressourcen, die zum Rendern einer bestimmten Schriftart auf einem bestimmten Gerät benötigt werden.<br/>                                                                                                                                                                                                                                                                                                |
| [**ID3DX10Mesh-Schnittstelle**](id3dx10mesh.md)                   | Anwendungen verwenden die Methoden der ID3DX10Mesh-Schnittstelle, um Gitternetzobjekte zu bearbeiten.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**ID3DX10MeshBuffer-Schnittstelle**](id3dx10meshbuffer.md)       |                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**ID3DX10SkinInfo-Schnittstelle**](id3dx10skininfo.md)           | MIT ID3DX10SkinInfo können Sie die Beziehung zwischen Denkpunkten und Scheitelpunkten in Ihren Netzen optimieren, verarbeiten und manuell festlegen (siehe [Skelettanimation auf Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)). Dies ist besonders nützlich, um X-Dateien, die von DCC-Apps exportiert werden (z. B. 3DS Max und Maya), hardwarefreundlicher zu gestalten und die Rendergeschwindigkeit Ihrer skinned Meshes im Softwarerenderingmodus zu verbessern.<br/> |
| [**ID3DX10Sprite-Schnittstelle**](id3dx10sprite.md)               | Die ID3DX10Sprite-Schnittstelle stellt eine Reihe von Methoden bereit, die das Zeichnen von Sprites mit Microsoft Direct3D vereinfachen.<br/>                                                                                                                                                                                                                                                                                            |
| [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md)       | Wird verwendet, um Aufgaben asynchron auszuführen. Dieses Objekt nimmt eine beträchtliche Menge an Ressourcen in Anspruch, sodass in der Regel nur eine pro Anwendung erstellt werden sollte.<br/>                                                                                                                                                                                                                                                                  |
| [**ID3DXMatrixStack-Schnittstelle**](d3d10-id3dxmatrixstack.md)   | Anwendungen verwenden die Methoden der ID3DXMATRIXStack-Schnittstelle, um einen Matrixstapel zu bearbeiten.<br/>                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX-Referenz](d3d10-graphics-reference-d3dx10.md)
</dt> </dl>

 

 




