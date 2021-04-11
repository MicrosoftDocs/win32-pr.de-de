---
description: Ruft die Flags ab, die beim Erstellen eines Microsoft DirectX Graphics Infrastructure (DXGI)-Objekts verwendet wurden.
ms.assetid: 1B4A5DC9-6853-4047-B64D-BD251352AC89
title: 'IDXGIFactory3:: getkreationflags-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDXGIFactory3.GetCreationFlags
api_type:
- COM
api_location:
- dxgi1_3.h
ms.openlocfilehash: 56d1f35ea5a4ce26a0d9ccb5ee0d79035f74a0ad
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123325"
---
# <a name="idxgifactory3getcreationflags-method"></a>IDXGIFactory3:: getkreationflags-Methode

Ruft die Flags ab, die beim Erstellen eines Microsoft DirectX Graphics Infrastructure (DXGI)-Objekts verwendet wurden.

## <a name="syntax"></a>Syntax


```C++
UINT GetCreationFlags();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die erstellungsflags.

## <a name="remarks"></a>Bemerkungen

Die **getkreationflags** -Methode gibt Flags zurück, die an [**die CreateDXGIFactory2**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-createdxgifactory2) -Funktion übergeben wurden, oder wurde implizit von " [**kreatedxgifactory**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory)", " [**CreateDXGIFactory1**](/windows/desktop/api/DXGI/nf-dxgi-createdxgifactory1)", " [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice)" oder " [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain)" erstellt.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDXGIFactory3**](/windows/desktop/api/DXGI1_3/nn-dxgi1_3-idxgifactory3)
</dt> </dl>

 

 
