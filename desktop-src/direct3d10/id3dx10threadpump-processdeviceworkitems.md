---
description: Legen Sie Arbeitselemente auf das Gerät fest, nachdem sie das Laden und Verarbeiten abgeschlossen haben.
ms.assetid: 67a9fcb2-3513-413d-ac3d-9988ef7b5a1f
title: ID3DX10ThreadPump::P rocessDeviceWorkItems-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.ProcessDeviceWorkItems
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e7179cf285c056601d00df5126ba98aaa34f827cbcac15400166d8301dc143a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118301776"
---
# <a name="id3dx10threadpumpprocessdeviceworkitems-method"></a>ID3DX10ThreadPump::P rocessDeviceWorkItems-Methode

Legen Sie Arbeitselemente auf das Gerät fest, nachdem sie das Laden und Verarbeiten abgeschlossen haben. Wenn die Threadpumpe das Laden und Verarbeiten einer Ressource oder eines Shaders abgeschlossen hat, wird sie in einer Warteschlange gespeichert, bis diese API aufgerufen wird. An diesem Punkt werden die verarbeiteten Elemente auf das Gerät festgelegt. Dies ist nützlich, um die Verarbeitungsmenge zu steuern, die für das Binden von Ressourcen an das Gerät für jeden Frame aufgewendet wird. Siehe Bemerkungen.

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

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die Anzahl der Arbeitselemente, die auf das Gerät festgelegt werden sollen. ProcessDeviceObjectCreation erstellt höchstens iWorkItemCount-Objekte. Wenn nicht genügend Arbeitselemente in der Warteschlange vorhanden sind, um iWorkItemCount-Objekte zu verarbeiten, erstellt ProcessDeviceObjectCreation so viele Geräteobjekte wie Elemente in der Warteschlange.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="remarks"></a>Hinweise

Beispiel für die Verwendung dieser API: Angenommen, Sie nähern sich dem Ende einer Ebene in Ihrem Spiel und möchten mit dem Vorabladen der Texturen, Shader und anderen Ressourcen für die nächste Ebene beginnen. Die Threadpumpe beginnt mit dem Laden, Dekomprimieren und Verarbeiten der Ressourcen und Shader in einem separaten Thread, bis sie bereit sind, auf das Gerät festgelegt zu werden. An diesem Punkt verlassen sie sie in einer Warteschlange. Möglicherweise möchten Sie nicht alle Ressourcen und Shader gleichzeitig auf dem Gerät festlegen, da dies zu einer erkennbaren vorübergehenden Verlangsamung der Leistung des Spiels führen kann. Diese API kann also einmal pro Frame aufgerufen werden, sodass auf jedem Frame nur eine kleine Anzahl von Arbeitselementen auf das Gerät festgelegt wird, wodurch die Arbeitslast der Bindungsressourcen an das Gerät auf mehrere Frames verteilt wird und die Möglichkeit einer erkennbaren Verlangsamung der Leistung des Spiels minimiert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10ThreadPump](id3dx10threadpump.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
