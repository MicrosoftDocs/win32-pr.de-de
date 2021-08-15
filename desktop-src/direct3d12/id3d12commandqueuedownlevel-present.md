---
title: ID3D12CommandQueueDownlevel::P resent-Methode
description: Kopiert Inhalte aus einer Direct3D 12 Texture2D-Ressource in ein Fenster. | ID3D12CommandQueueDownlevel::P resent-Methode
keywords:
- Present-Methode
- Present-Methode, ID3D12CommandQueueDownlevel-Schnittstelle
- ID3D12CommandQueueDownlevel-Schnittstelle, Present-Methode
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel.Present
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: b21a97d15d2666dcfe0a304f2393d6d14c5dbcc4142d8b42f43f295d8751614b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118529130"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a>ID3D12CommandQueueDownlevel::P resent-Methode

Kopiert Inhalte aus einer Direct3D 12 Texture2D-Ressource in ein Fenster.

## <a name="syntax"></a>Syntax

```cpp
HRESULT Present
    ID3D12GraphicsCommandList *pOpenCommandList,
    ID3D12Resource *pSourceTex2D,
    HWND hWindow,
    D3D12_DOWNLEVEL_PRESENT_FLAGS Flags
);
```

## <a name="parameters"></a>Parameter

`pOpenCommandList`

Typ: **[ID3D12GraphicsCommandList](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

Eine geöffnete Befehlsliste, in der Direct3D 12 einen Present-Befehl in die Queue einschließt und dann schließt und für Sie übermittelt.

`pSourceTex2D`

Typ: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***

Eine Ressource, die den anzuzeigenden gewünschten Inhalt mit der Dimension [**D3D12 \_ RESOURCE \_ DIMENSION \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)und einem der folgenden Formate enthält.

* DXGI_FORMAT_R16G16B16A16_FLOAT
* DXGI_FORMAT_R10G10B10A2_UNORM
* DXGI_FORMAT_R8G8B8A8_UNORM
* DXGI_FORMAT_R8G8B8A8_UNORM_SRGB
* DXGI_FORMAT_B8G8R8X8_UNORM
* DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM
* DXGI_FORMAT_B8G8R8A8_UNORM
* DXGI_FORMAT_B8G8R8A8_UNORM_SRGB

`hWindow`

Typ: **[HWND](/windows/desktop/WinProg/windows-data-types)**

Das Handle für das Fenster, in dem der Inhalt angezeigt werden soll.

`Flags`

Typ: **[D3D12 \_ DOWNLEVEL \_ PRESENT \_ FLAGS](d3d12_downlevel_present_flags.md)**

Flags zum Ändern des **Present-Vorgangs.**

## <a name="return-value"></a>Rückgabewert

Gibt **S_OK** bei Erfolg oder andernfalls ein fehlerhaftes HRESULT zurück.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------|------------------|
| Header | d3d12downlevel.h |
| DLL    | D3D12.dll (nur Windows 7) |

## <a name="see-also"></a>Weitere Informationen
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [Direct3D 12 auf Windows 7-Schnittstellen](direct3d-12on7-interfaces.md)
* [Direct3D 12 auf Windows 7-Referenz (d3d12downlevel.h)](direct3d-12on7-reference.md)
* [Direct3D 12 unter Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
