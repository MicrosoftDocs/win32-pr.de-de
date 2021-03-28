---
title: ID3DX11DataLoader DECOMPRESS-Methode (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Decodiert codierte Daten.
ms.assetid: 68579c86-9f77-444b-86b3-746cff745be8
keywords:
- DECOMPRESS-Methode Direct3D 11
- DECOMPRESS-Methode Direct3D 11, ID3DX11DataLoader-Schnittstelle
- ID3DX11DataLoader Interface Direct3D 11, DECOMPRESS-Methode
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Decompress
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b515eb38fb70fc31f0bbd0d02e20dcfb9f66ea5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961760"
---
# <a name="id3dx11dataloaderdecompress-method"></a>ID3DX11DataLoader::D eComPress-Methode

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Decodiert codierte Daten.

## <a name="syntax"></a>Syntax


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppData* \[ vorgenommen\]
</dt> <dd>

Typ: **void \* \***

Zeiger auf die zu entkomprimierenden Rohdaten.

</dd> <dt>

*pcbytes* \[ in\]
</dt> <dd>

Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)\***

Die Größe der Daten, auf die von ppData verwiesen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, um Ressourcen aus Dateisystemen (z. b. zip-Dateien) zu laden. Beim Laden von einer nicht komprimierten Ressource muss für die Debug-Phase keine Arbeit ausgeführt werden.

Die [**ID3DX11DataLoader-Schnittstelle**](id3dx11dataloader.md) kann geerbt werden, und die zugehörigen Member werden neu definiert, um benutzerdefinierte Dateiformate

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Bibliothek d3dx11. lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11DataLoader](id3dx11dataloader.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

