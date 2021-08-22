---
description: Entfernt alle Ressourcen vom Gerät, indem deren Zeiger auf NULL festgelegt werden. Dies sollte beim Herunterfahren der Anwendung aufgerufen werden. Dadurch wird sichergestellt, dass beim Freigeben aller Ressourcen keines dieser Ressourcen an das Gerät gebunden ist.
ms.assetid: f41ce97e-5a81-43a4-a8c7-7411b43c0d61
title: D3DX10UnsetAllDeviceObjects-Funktion (D3DX10Core.h)
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
ms.openlocfilehash: 079c5f1b437c2755bf7125dee6be10baed1a91b4a37276997e70543c72904036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128342"
---
# <a name="d3dx10unsetalldeviceobjects-function"></a>D3DX10UnsetAllDeviceObjects-Funktion

Entfernt alle Ressourcen vom Gerät, indem deren Zeiger auf **NULL** festgelegt werden. Dies sollte beim Herunterfahren der Anwendung aufgerufen werden. Dadurch wird sichergestellt, dass beim Freigeben aller Ressourcen keines dieser Ressourcen an das Gerät gebunden ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10UnsetAllDeviceObjects(
  _In_ ID3D10Device *pDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Zeiger auf das Gerät. Siehe [**ID3D10Device-Schnittstelle.**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




