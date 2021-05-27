---
title: D1112-Gerät muss DX11 sein
ms.assetid: 39dcccaf-db56-402d-b62f-704ad4daf151
description: Das der DXGI-Oberfläche zugeordnete Gerät muss ein D3D11-Gerät sein.
keywords:
- D1112-Gerät muss DX11 Direct2D sein
topic_type:
- apiref
api_name:
- D1112 Device Must Be DX11
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 68408c56710589def033c34d20d9bac81e8d4947
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549885"
---
# <a name="d1112-device-must-be-dx11"></a>D1112: Gerät muss DX11 sein

Das der DXGI-Oberfläche zugeordnete Gerät muss ein D3D11-Gerät sein.



| &nbsp;      |  &nbsp; |
|-------------|---------|
| Fehlerstufe | Warnung |



 

## <a name="possible-causes"></a>Mögliche Ursachen

Es wurde versucht, [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) mit einer DXGI-Oberfläche zu verwenden, die von einem Nicht-Direct3D11-Gerät erstellt wurde.

 

 




