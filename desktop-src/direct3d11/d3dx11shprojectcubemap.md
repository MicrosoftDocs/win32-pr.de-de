---
title: D3DX11SHProjectCubeMap-Funktion (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie, dass Sie die spprojectcubemap der sphärischen Harmonics-Bibliothek verwenden, anstatt diese Funktion zu verwenden.
ms.assetid: 58c741a3-dd5d-4b18-b257-5e85a9b799fd
keywords:
- D3DX11SHProjectCubeMap-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SHProjectCubeMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf773c00a649e6ace065fcf552358fbf5eeb19c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995980"
---
# <a name="d3dx11shprojectcubemap-function"></a>D3DX11SHProjectCubeMap-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, empfiehlt es sich, die für die **spprojectcubemap** verwendete [sphärischen Harmonics](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) -Bibliothek zu verwenden.

 

Projiziert eine in einer cubemap dargestellte Funktion in sphärischen Harmonics.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11SHProjectCubeMap(
   ID3D11DeviceContext *pContext,
   UINT                Order,
   ID3D11Texture2D     *pCubeMap,
   FLOAT               *pROut,
   FLOAT               *pGOut,
   FLOAT               *pBOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContext* 
</dt> <dd>

Typ: **[ **Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Ein Zeiger auf ein [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Objekt.

</dd> <dt>

*Order* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Reihenfolge der SH-Auswertung generiert Reihenfolge ^ 2-Koeffizienten, deren Grad "Order-1" ist. Der gültige Bereich liegt zwischen 2 und 6.

</dd> <dt>

*pcubemap* 
</dt> <dd>

Typ: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Ein Zeiger auf eine [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) , die eine cubemap darstellt, die in sphärischen Harmoniken projiziert werden soll.

</dd> <dt>

*Proxy* 
</dt> <dd>

Typ: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***

Ausgabe SH-Vektor für rot.

</dd> <dt>

*pgout* 
</dt> <dd>

Typ: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***

Ausgabe SH-Vektor für grün.

</dd> <dt>

*pbout* 
</dt> <dd>

Typ: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***

Ausgabe SH-Vektor für blau.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Bibliothek d3dx11. lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

