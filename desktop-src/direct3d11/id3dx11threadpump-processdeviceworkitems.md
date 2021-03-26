---
title: ID3DX11ThreadPump processdeviceworkitems-Methode (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Legt Arbeitselemente auf das Gerät fest, nachdem Sie geladen und verarbeitet wurden.
ms.assetid: 154e6ea5-0a88-4c8a-9c20-e7fbf95f1946
keywords:
- Processdeviceworkitems-Methode Direct3D 11
- Processdeviceworkitems-Methode Direct3D 11, ID3DX11ThreadPump-Schnittstelle
- ID3DX11ThreadPump Interface Direct3D 11, processdeviceworkitems-Methode
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
ms.openlocfilehash: 5ad570785ac7dc36fb5dd9d464e97ef46f52ca93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982227"
---
# <a name="id3dx11threadpumpprocessdeviceworkitems-method"></a>ID3DX11ThreadPump::P rocess deviceworkitems-Methode

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Legt Arbeitselemente auf das Gerät fest, nachdem Sie geladen und verarbeitet wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT ProcessDeviceWorkItems(
  [in] UINT iWorkItemCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iworkitemcount* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Arbeitselemente, die auf das Gerät festgelegt werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen

Wenn die Thread Pumpe das Laden und Verarbeiten einer Ressource oder eines Shaders abgeschlossen hat, wird Sie in einer Warteschlange gespeichert, bis diese API aufgerufen wird. an diesem Punkt werden die verarbeiteten Elemente auf das Gerät festgelegt. Dies ist hilfreich, um die Verarbeitungs Menge zu steuern, die für die Bindung von Ressourcen an das Gerät für jeden Frame aufgewendet wird.

Ein Beispiel dafür, wie Sie diese API verwenden können, ist, dass Sie das Ende einer Ebene im Spiel nähern und damit beginnen möchten, die Texturen, Shader und andere Ressourcen für die nächste Ebene vorab zu laden. Die Thread Pumpe lädt das Laden, dekomprimieren und Verarbeiten der Ressourcen und Shader in einem separaten Thread, bis Sie für die Festlegung auf das Gerät bereit sind. an diesem Punkt werden Sie in einer Warteschlange belassen. Möglicherweise möchten Sie nicht alle Ressourcen und Shader gleichzeitig auf das Gerät festlegen, da dies zu einer merklichen vorübergehenden Verlangsamung der Spielleistung führen kann. Daher könnte diese API einmal pro Frame aufgerufen werden, sodass nur eine kleine Anzahl von Arbeitsaufgaben auf das Gerät in jedem Frame festgelegt wird. Dadurch wird die Arbeitslast der Bindungs Ressourcen über mehrere Frames auf das Gerät verteilt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Bibliothek d3dx11. lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11ThreadPump](id3dx11threadpump.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

