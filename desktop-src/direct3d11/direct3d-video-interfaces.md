---
title: Direct3D-Video Schnittstellen
description: In diesem Thema werden die Direct3D-Video Schnittstellen aufgelistet, die in Direct3D 9Ex verfügbar sind und unter Windows 7 und höheren Versionen von Windows-Client Betriebssystemen und Windows Server 2008 R2 und höheren Versionen von Windows Server-Betriebssystemen unterstützt werden.
ms.assetid: 922AC983-B9C0-494C-BADD-CEF20931FC26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d20c86e172308d4be6f4c6218a110f49b033ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473333"
---
# <a name="direct3d-video-interfaces"></a>Direct3D-Video Schnittstellen

In diesem Thema werden die Direct3D-Video Schnittstellen aufgelistet, die in Direct3D 9Ex verfügbar sind und unter Windows 7 und höheren Versionen von Windows-Client Betriebssystemen und Windows Server 2008 R2 und höheren Versionen von Windows Server-Betriebssystemen unterstützt werden. Sie können diese Schnittstellen und ihre Methoden verwenden, um die Funktionen zum Schutz von Videoinhalten des Grafik Treibers und die Überlagerungs Hardwarefunktionen eines Direct3D-Geräts zu erhalten. Sie können diese Schnittstellen und ihre Methoden auch verwenden, um Videoinhalte zu schützen. Diese Schnittstellen und ihre Methoden werden in d3d9. h definiert und im Abschnitt [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) beschrieben.



| Schnittstelle                                                                                                                                                                                                                             | BESCHREIBUNG                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)<br/>           | Fragt die Überlagerungs Hardwarefunktionen eines Direct3D-Geräts ab.<br/>                                                     |
| <span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)<br/> | Stellt einen Kommunikationskanal mit dem Grafiktreiber oder der Direct3D-Laufzeit bereit.<br/>                                  |
| <span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)<br/>                                    | Stellt eine Kryptografiesitzung dar, die für den Zugriff auf eine geschützte Oberfläche verwendet wird.<br/>                                      |
| <span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)<br/>                                              | Ermöglicht es einer Anwendung, Inhalts Schutz-und Verschlüsselungsdienste zu verwenden, die von einem Grafiktreiber implementiert werden.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Effekte (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[Programmieranleitung für Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

