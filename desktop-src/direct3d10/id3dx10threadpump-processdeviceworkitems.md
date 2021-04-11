---
description: Legen Sie die Arbeitselemente auf das Gerät fest, nachdem das Laden und verarbeiten abgeschlossen ist.
ms.assetid: 67a9fcb2-3513-413d-ac3d-9988ef7b5a1f
title: ID3DX10ThreadPump::P rocess deviceworkitems-Methode (d3dx10. h)
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
ms.openlocfilehash: 88b98d68e4e0e47b2c8e7f9a2e095565c53e2561
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132416"
---
# <a name="id3dx10threadpumpprocessdeviceworkitems-method"></a>ID3DX10ThreadPump::P rocess deviceworkitems-Methode

Legen Sie die Arbeitselemente auf das Gerät fest, nachdem das Laden und verarbeiten abgeschlossen ist. Wenn die Thread Pumpe das Laden und Verarbeiten einer Ressource oder eines Shaders abgeschlossen hat, wird Sie in einer Warteschlange gespeichert, bis diese API aufgerufen wird. an diesem Punkt werden die verarbeiteten Elemente auf das Gerät festgelegt. Dies ist hilfreich, um die Verarbeitungs Menge zu steuern, die für die Bindung von Ressourcen an das Gerät für jeden Frame aufgewendet wird. Siehe Bemerkungen.

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

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl der Arbeitselemente, die auf das Gerät festgelegt werden sollen. Processdeviceobjectcreation erstellt höchstens iworkitemcount-Objekte. Wenn nicht genügend Arbeitselemente in der Warteschlange vorhanden sind, um iworkitemcount-Objekte zu verarbeiten, erstellt processdeviceobjectcreation so viele Geräte Objekte, wie sich Elemente in der Warteschlange befinden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen

Ein Beispiel dafür, wie Sie diese API verwenden können, ist, dass Sie das Ende einer Ebene im Spiel nähern und damit beginnen möchten, die Texturen, Shader und andere Ressourcen für die nächste Ebene vorab zu laden. Die Thread Pumpe lädt das Laden, dekomprimieren und Verarbeiten der Ressourcen und Shader in einem separaten Thread, bis Sie für die Festlegung auf das Gerät bereit sind. an diesem Punkt werden Sie in einer Warteschlange belassen. Möglicherweise möchten Sie nicht alle Ressourcen und Shader gleichzeitig auf das Gerät festlegen, da dies dazu führen kann, dass die Leistung eines temporären Benachrichtigungs verkabels verlangsamt wird. Daher könnte diese API einmal pro Frame aufgerufen werden, sodass nur eine kleine Anzahl von Arbeitsaufgaben auf das Gerät in jedem Frame festgelegt wird. Dadurch wird die Arbeitslast der Bindungs Ressourcen auf das Gerät über mehrere Frames verteilt, und die Wahrscheinlichkeit eines Benachrichtigungs Kabels in der Spielleistung wird minimiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10ThreadPump](id3dx10threadpump.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
