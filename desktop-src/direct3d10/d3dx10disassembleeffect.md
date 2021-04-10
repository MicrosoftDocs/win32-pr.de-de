---
description: Beachten Sie, dass Sie die D3DDisassemble-API verwenden, anstatt diese Legacy Funktion zu verwenden. Diese Funktion, die einen kompilierten Effekt in eine Text Zeichenfolge disassembliert, die Assemblyanweisungen und Register Zuweisungen enthält, ist veraltet.
ms.assetid: 218ac120-33ce-44db-84a7-99fef3281f07
title: D3DX10DisassembleEffect-Funktion (D3DX10Core. h)
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
ms.openlocfilehash: 67fe19365616e779bd17ab689550b34737288317
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961674"
---
# <a name="d3dx10disassembleeffect-function"></a>D3DX10DisassembleEffect-Funktion

> [!Note]  
> Anstatt diese Legacy Funktion zu verwenden, empfiehlt es sich, die [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) -API zu verwenden.

 

Diese Funktion, die einen kompilierten Effekt in eine Text Zeichenfolge disassembliert, die Assemblyanweisungen und Register Zuweisungen enthält, ist veraltet. Verwenden Sie stattdessen [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).

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

*Peer-ect* \[ in\]
</dt> <dd>

Typ: **[ **ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***

Ein Zeiger auf die Effekt Schnittstelle (siehe [**ID3D10Effect-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).

</dd> <dt>

*Enablecolorcode* \[ in\]
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

Fügen Sie HTML-Tags in die Ausgabe ein, um das Ergebnis farblich zu färben.

</dd> <dt>

*ppdisassembly* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Die Adresse eines Puffers (siehe [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)), die den disassemblierten Effekt enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
