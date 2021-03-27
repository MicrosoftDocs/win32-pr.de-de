---
title: ID3DX11ThreadPump getqueuestatus-Methode (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Ruft die Anzahl der Elemente in jeder der drei Warteschlangen innerhalb der Thread Pumpe ab.
ms.assetid: 69e1c786-6c7d-4432-bf34-3bf7606a07f6
keywords:
- Getqueuestatus-Methode Direct3D 11
- Getqueuestatus-Methode Direct3D 11, ID3DX11ThreadPump-Schnittstelle
- ID3DX11ThreadPump-Schnittstelle Direct3D 11, getqueuestatus-Methode
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
ms.openlocfilehash: c3c945cb2978af15263d3f72d34a47c5e8ca8a69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982233"
---
# <a name="id3dx11threadpumpgetqueuestatus-method"></a>ID3DX11ThreadPump:: getqueuestatus-Methode

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Ruft die Anzahl der Elemente in jeder der drei Warteschlangen innerhalb der Thread Pumpe ab.

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

*pioqueue* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***

Anzahl der Elemente in der e/a-Warteschlange.

</dd> <dt>

*pprocessqueue* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***

Anzahl der Elemente in der Verarbeitungs Warteschlange.

</dd> <dt>

*pdevicequeue* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)\***

Anzahl der Elemente in der Geräte Warteschlange.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.

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

 

