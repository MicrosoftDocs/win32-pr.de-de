---
title: ID3D12CommandQueueDownlevel::P Resent-Methode
description: Kopiert Inhalt aus einer Direct3D 12 Texture2D-Ressource in ein-Fenster. | ID3D12CommandQueueDownlevel::P Resent-Methode
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
ms.openlocfilehash: a6c74685911e52a671eaeb02645754a45b8d647e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350706"
---
# <a name="id3d12commandqueuedownlevelpresent-method"></a>ID3D12CommandQueueDownlevel::P Resent-Methode

Kopiert Inhalt aus einer Direct3D 12 Texture2D-Ressource in ein-Fenster.

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

Eine geöffnete Befehlsliste, in der Direct3D 12 einen aktuellen Befehl in die Warteschlange einreiht und dann geschlossen und für Sie übermittelt wird.

`pSourceTex2D`

Typ: **[ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource)\***

Eine Ressource mit den gewünschten Inhalten, die angezeigt werden sollen, mit Dimensions [**D3D12 \_ Resource \_ Dimension \_ TEXTURE2D**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_dimension)und einem Format, das einer der folgenden ist.

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

Type: **[D3D12 \_ Downlevel \_ Present \_ Flags](d3d12_downlevel_present_flags.md)**

Flags zum Ändern des **aktuellen** Vorgangs.

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg **S_OK** oder andernfalls ein fehlerhaftes HRESULT zurück.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------|------------------|
| Header | d3d12downlevel. h |
| DLL    | D3D12.dll (nur Windows 7) |

## <a name="see-also"></a>Siehe auch
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [Direct3D 12 auf Windows 7-Schnittstellen](direct3d-12on7-interfaces.md)
* [Referenz zu Direct3D 12 auf Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 unter Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
