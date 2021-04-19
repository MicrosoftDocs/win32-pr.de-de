---
description: Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen (Component Object Model), die von der D3DX Utility Library bereitgestellt werden. Die folgenden Schnittstellen werden mit der D3DX Utility Library verwendet.
ms.assetid: c57d9c39-3f30-4205-9b0a-665fe53f2b14
title: D3DX-Schnittstellen (Direct3D 10-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e0fc152468efec4e33fd6a3ab467d211cfbef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346860"
---
# <a name="d3dx-interfaces-direct3d-10-graphics"></a>D3DX-Schnittstellen (Direct3D 10-Grafiken)

Dieser Abschnitt enthält Referenzinformationen zu den COM-Schnittstellen (Component Object Model), die von der D3DX Utility Library bereitgestellt werden. Die folgenden Schnittstellen werden mit der D3DX Utility Library verwendet.



| Schnittstellen                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3DX10DataLoader-Schnittstelle**](id3dx10dataloader.md)       | Datenlade Objekt, das von der [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) zum asynchronen Laden von Daten verwendet wird<br/>                                                                                                                                                                                                                                                                                                   |
| [**ID3DX10DataProcessor-Schnittstelle**](id3dx10dataprocessor.md) | Datenverarbeitungs Objekt, das von der [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md) zum asynchronen verarbeiten geladener Daten verwendet wird.<br/>                                                                                                                                                                                                                                                                                      |
| [**ID3DX10Font-Schnittstelle**](id3dx10font.md)                   | Die ID3DX10Font-Schnittstelle kapselt die Texturen und Ressourcen, die erforderlich sind, um eine bestimmte Schriftart auf einem bestimmten Gerät zu Rendering.<br/>                                                                                                                                                                                                                                                                                                |
| [**ID3DX10Mesh-Schnittstelle**](id3dx10mesh.md)                   | Anwendungen verwenden die Methoden der ID3DX10Mesh-Schnittstelle zum Bearbeiten von Mesh-Objekten.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**ID3DX10MeshBuffer-Schnittstelle**](id3dx10meshbuffer.md)       |                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**ID3DX10SkinInfo-Schnittstelle**](id3dx10skininfo.md)           | Mit ID3DX10SkinInfo können Sie die Beziehung zwischen den Knochen und Scheitel Punkten in ihren Netzen optimieren, verarbeiten und manuell festlegen (siehe " [Skelett Animation" auf Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)). Es ist besonders nützlich, wenn Sie x-Dateien, die von DCC-apps exportiert werden (z. b. 3ds Max und Maya), flexibler gestalten und die renderinggeschwindigkeit der im Software-Rendermodus gespritzelten Netze verbessern.<br/> |
| [**ID3DX10Sprite-Schnittstelle**](id3dx10sprite.md)               | Die ID3DX10Sprite-Schnittstelle stellt eine Reihe von Methoden bereit, die das Zeichnen von Sprites mithilfe von Microsoft Direct3D vereinfachen.<br/>                                                                                                                                                                                                                                                                                            |
| [**ID3DX10ThreadPump-Schnittstelle**](id3dx10threadpump.md)       | Wird verwendet, um Aufgaben asynchron auszuführen. Dieses Objekt belegt eine beträchtliche Menge an Ressourcen, sodass im Allgemeinen nur eine pro Anwendung erstellt werden sollte.<br/>                                                                                                                                                                                                                                                                  |
| [**ID3DXMatrixStack-Schnittstelle**](d3d10-id3dxmatrixstack.md)   | Anwendungen verwenden die Methoden der ID3DXMATRIXStack-Schnittstelle, um einen Matrix Stapel zu bearbeiten.<br/>                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[D3DX-Referenz](d3d10-graphics-reference-d3dx10.md)
</dt> </dl>

 

 




