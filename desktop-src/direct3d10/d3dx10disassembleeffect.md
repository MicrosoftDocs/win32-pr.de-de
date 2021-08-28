---
description: Hinweis Anstelle dieser Legacyfunktion wird die Verwendung der D3DDisassemble-API empfohlen. Diese Funktion, die einen kompilierten Effekt in eine Textzeichenfolge disassembliert, die Assemblyanweisungen und Registerzuweisungen enthält, ist veraltet.
ms.assetid: 218ac120-33ce-44db-84a7-99fef3281f07
title: D3DX10DisassembleEffect-Funktion (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleEffect
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 282dcbb91013e5e8bf6def540809fa3afdb3bca40e2a2fd5250c5b3c92877af5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753280"
---
# <a name="d3dx10disassembleeffect-function"></a>D3DX10DisassembleEffect-Funktion

> [!Note]  
> Anstatt diese Legacyfunktion zu verwenden, wird empfohlen, die [**D3DDisassemble-API zu**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) verwenden.

 

Diese Funktion, die einen kompilierten Effekt in eine Textzeichenfolge disassembliert, die Assemblyanweisungen und Registerzuweisungen enthält, ist veraltet. Verwenden Sie stattdessen [**D3DDisassemble10Effect.**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect)

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10DisassembleEffect(
  _In_  ID3D10Effect *pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ ID3D10Blob   **ppDisassembly
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pEffect* \[ In\]
</dt> <dd>

Typ: **[ **ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***

Ein Zeiger auf die Effektschnittstelle (siehe [**ID3D10Effect-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).

</dd> <dt>

*EnableColorCode* \[ In\]
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

Schließen Sie HTML-Tags in die Ausgabe ein, um das Ergebnis farblich zu coden.

</dd> <dt>

*ppDisassembly* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Adresse eines Puffers (siehe [**ID3D10Blob-Schnittstelle),**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)der den disassemblierten Effekt enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 10-Rückgabecodes zurück.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
