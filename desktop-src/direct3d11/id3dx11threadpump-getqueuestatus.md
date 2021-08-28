---
title: ID3DX11ThreadPump GetQueueStatus-Methode (D3DX11core.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Ruft die Anzahl der Elemente in jeder der drei Warteschlangen innerhalb der Threadpump ab.
ms.assetid: 69e1c786-6c7d-4432-bf34-3bf7606a07f6
keywords:
- GetQueueStatus-Methode Direct3D 11
- GetQueueStatus-Methode Direct3D 11, ID3DX11ThreadPump-Schnittstelle
- ID3DX11ThreadPump-Schnittstelle Direct3D 11 , GetQueueStatus-Methode
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetQueueStatus
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41535dba7c5abb96c132714ecbc6ee4e02f1f42fcb6a45ebe8795286d8613c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851500"
---
# <a name="id3dx11threadpumpgetqueuestatus-method"></a>ID3DX11ThreadPump::GetQueueStatus-Methode

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Ruft die Anzahl der Elemente in jeder der drei Warteschlangen innerhalb der Threadpump ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetQueueStatus(
  [in] UINT *pIoQueue,
  [in] UINT *pProcessQueue,
  [in] UINT *pDeviceQueue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pIoQueue* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)\***

Anzahl der Elemente in der E/A-Warteschlange.

</dd> <dt>

*pProcessQueue* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)\***

Anzahl der Elemente in der Prozesswarteschlange.

</dd> <dt>

*pDeviceQueue* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)\***

Anzahl der Elemente in der Gerätewarteschlange.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die unter [Direct3D 11-Rückgabecodes aufgeführt sind.](d3d11-graphics-reference-returnvalues.md)

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

 

