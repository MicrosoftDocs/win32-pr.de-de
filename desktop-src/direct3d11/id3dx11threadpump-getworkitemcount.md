---
title: ID3DX11ThreadPump getworkitemcount-Methode (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Ruft die Anzahl der Arbeitselemente in der Thread Pumpe ab.
ms.assetid: 04883b25-64dc-41a3-849f-710a59e9d3da
keywords:
- Getworkitemcount-Methode Direct3D 11
- Getworkitemcount-Methode Direct3D 11, ID3DX11ThreadPump-Schnittstelle
- ID3DX11ThreadPump-Schnittstelle Direct3D 11, getworkitemcount-Methode
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetWorkItemCount
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29668e66dd3d8c6d29cbfc69a4ef12a2fdfd18b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982228"
---
# <a name="id3dx11threadpumpgetworkitemcount-method"></a>ID3DX11ThreadPump:: getworkitemcount-Methode

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Ruft die Anzahl der Arbeitselemente in der Thread Pumpe ab.

## <a name="syntax"></a>Syntax


```C++
UINT GetWorkItemCount();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Arbeitselemente, die sich in der Thread Pumpe in der Warteschlange befinden.

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

 

