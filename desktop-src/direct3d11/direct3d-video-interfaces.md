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
# <a name="direct3d-video-interfaces"></a><span data-ttu-id="e3e30-103">Direct3D-Video Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e3e30-103">Direct3D Video Interfaces</span></span>

<span data-ttu-id="e3e30-104">In diesem Thema werden die Direct3D-Video Schnittstellen aufgelistet, die in Direct3D 9Ex verfügbar sind und unter Windows 7 und höheren Versionen von Windows-Client Betriebssystemen und Windows Server 2008 R2 und höheren Versionen von Windows Server-Betriebssystemen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e3e30-104">This topic lists the Direct3D video interfaces that are available in Direct3D 9Ex and that are supported on Windows 7 and later versions of Windows client operating systems and on Windows Server 2008 R2 and later versions of Windows server operating systems.</span></span> <span data-ttu-id="e3e30-105">Sie können diese Schnittstellen und ihre Methoden verwenden, um die Funktionen zum Schutz von Videoinhalten des Grafik Treibers und die Überlagerungs Hardwarefunktionen eines Direct3D-Geräts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e3e30-105">You can use these interfaces and their methods to obtain the video content protection capabilities of the graphics driver and the overlay hardware capabilities of a Direct3D device.</span></span> <span data-ttu-id="e3e30-106">Sie können diese Schnittstellen und ihre Methoden auch verwenden, um Videoinhalte zu schützen.</span><span class="sxs-lookup"><span data-stu-id="e3e30-106">You can also use these interfaces and their methods to protect video content.</span></span> <span data-ttu-id="e3e30-107">Diese Schnittstellen und ihre Methoden werden in d3d9. h definiert und im Abschnitt [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e3e30-107">These interfaces and their methods are defined in D3d9.h and described in the [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) section.</span></span>



| <span data-ttu-id="e3e30-108">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e3e30-108">Interface</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="e3e30-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3e30-109">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e30-110"><span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)</span><span class="sxs-lookup"><span data-stu-id="e3e30-110"><span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)</span></span><br/>           | <span data-ttu-id="e3e30-111">Fragt die Überlagerungs Hardwarefunktionen eines Direct3D-Geräts ab.</span><span class="sxs-lookup"><span data-stu-id="e3e30-111">Queries the overlay hardware capabilities of a Direct3D device.</span></span><br/>                                                     |
| <span data-ttu-id="e3e30-112"><span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)</span><span class="sxs-lookup"><span data-stu-id="e3e30-112"><span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)</span></span><br/> | <span data-ttu-id="e3e30-113">Stellt einen Kommunikationskanal mit dem Grafiktreiber oder der Direct3D-Laufzeit bereit.</span><span class="sxs-lookup"><span data-stu-id="e3e30-113">Provides a communication channel with the graphics driver or the Direct3D runtime.</span></span><br/>                                  |
| <span data-ttu-id="e3e30-114"><span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)</span><span class="sxs-lookup"><span data-stu-id="e3e30-114"><span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)</span></span><br/>                                    | <span data-ttu-id="e3e30-115">Stellt eine Kryptografiesitzung dar, die für den Zugriff auf eine geschützte Oberfläche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3e30-115">Represents a cryptographic session that is used to access a protected surface.</span></span><br/>                                      |
| <span data-ttu-id="e3e30-116"><span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)</span><span class="sxs-lookup"><span data-stu-id="e3e30-116"><span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)</span></span><br/>                                              | <span data-ttu-id="e3e30-117">Ermöglicht es einer Anwendung, Inhalts Schutz-und Verschlüsselungsdienste zu verwenden, die von einem Grafiktreiber implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="e3e30-117">Enables an application to use content protection and encryption services that are implemented by a graphics driver.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="e3e30-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e3e30-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3e30-119">Effekte (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="e3e30-119">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="e3e30-120">Programmieranleitung für Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e3e30-120">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

