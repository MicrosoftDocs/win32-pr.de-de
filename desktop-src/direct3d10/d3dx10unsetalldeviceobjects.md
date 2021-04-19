---
description: Entfernt alle Ressourcen vom Gerät, indem die Zeiger auf NULL festgelegt werden. Dies sollte beim Herunterfahren der Anwendung aufgerufen werden. Dadurch wird sichergestellt, dass alle Ressourcen freigegeben werden, die nicht an das Gerät gebunden sind.
ms.assetid: f41ce97e-5a81-43a4-a8c7-7411b43c0d61
title: D3DX10UnsetAllDeviceObjects-Funktion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10UnsetAllDeviceObjects
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4d3a113be935f77dbd62b2f3fac4c16c7cac9881
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355193"
---
# <a name="d3dx10unsetalldeviceobjects-function"></a>D3DX10UnsetAllDeviceObjects-Funktion

Entfernt alle Ressourcen vom Gerät, indem die Zeiger auf **null** festgelegt werden. Dies sollte beim Herunterfahren der Anwendung aufgerufen werden. Dadurch wird sichergestellt, dass alle Ressourcen freigegeben werden, die nicht an das Gerät gebunden sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10UnsetAllDeviceObjects(
  _In_ ID3D10Device *pDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Zeiger auf das Gerät. Siehe [**ID3D10Device-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




