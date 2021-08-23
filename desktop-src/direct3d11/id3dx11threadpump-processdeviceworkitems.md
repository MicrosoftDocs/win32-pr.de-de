---
title: ID3DX11ThreadPump ProcessDeviceWorkItems-Methode (D3DX11core.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Legt Arbeitselemente auf dem Gerät fest, nachdem sie das Laden und Verarbeiten abgeschlossen haben.
ms.assetid: 154e6ea5-0a88-4c8a-9c20-e7fbf95f1946
keywords:
- ProcessDeviceWorkItems-Methode Direct3D 11
- ProcessDeviceWorkItems-Methode Direct3D 11, ID3DX11ThreadPump-Schnittstelle
- ID3DX11ThreadPump-Schnittstelle Direct3D 11 , ProcessDeviceWorkItems-Methode
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.ProcessDeviceWorkItems
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a6918e9ecea9d66c3ebca034628387ea471e9173b4b14f24e9b7f866897325
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608670"
---
# <a name="id3dx11threadpumpprocessdeviceworkitems-method"></a>ID3DX11ThreadPump::P rocessDeviceWorkItems-Methode

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Legt Arbeitselemente auf dem Gerät fest, nachdem sie das Laden und Verarbeiten abgeschlossen haben.

## <a name="syntax"></a>Syntax


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iWorkItemCount* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Arbeitselemente, die auf das Gerät festgelegt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die unter [Direct3D 11-Rückgabecodes aufgeführt sind.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Wenn die Threadpump das Laden und Verarbeiten einer Ressource oder eines Shaders abgeschlossen hat, wird sie in einer Warteschlange gespeichert, bis diese API aufgerufen wird. An diesem Punkt werden die verarbeiteten Elemente auf das Gerät festgelegt. Dies ist nützlich, um die Verarbeitungsmenge zu steuern, die für das Binden von Ressourcen an das Gerät für jeden Frame verwendet wird.

Ein Beispiel für die Verwendung dieser API: Sie nähern sich dem Ende einer Ebene in Ihrem Spiel und möchten mit dem Vorabladen der Texturen, Shader und anderen Ressourcen für die nächste Ebene beginnen. Die Threadpump beginnt mit dem Laden, Dekomprimieren und Verarbeiten der Ressourcen und Shader in einem separaten Thread, bis sie bereit sind, auf das Gerät festgelegt zu werden. An diesem Punkt werden sie in einer Warteschlange bereinige. Möglicherweise möchten Sie nicht alle Ressourcen und Shader gleichzeitig auf das Gerät festlegen, da dies zu einer spürbaren vorübergehenden Verlangsamung der Leistung des Spiels führen kann. Diese API kann also einmal pro Frame aufgerufen werden, sodass auf jedem Frame nur eine kleine Anzahl von Arbeitselementen auf das Gerät festgelegt wird, wodurch die Arbeitslast der Bindungsressourcen auf das Gerät auf mehrere Frames übertragen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11ThreadPump](id3dx11threadpump.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

