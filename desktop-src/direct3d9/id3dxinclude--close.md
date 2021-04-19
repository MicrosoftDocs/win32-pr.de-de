---
description: Eine vom Benutzer implementierte Methode zum Schließen einer Shader- \# Includedatei.
ms.assetid: de54ce56-3884-443a-9879-4e7290bcfb8d
title: 'ID3DXInclude:: Close-Methode (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Close
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b60d01d59a4e54fa0d50c16a3fc845ea4e316792
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355838"
---
# <a name="id3dxincludeclose-method"></a>ID3DXInclude:: Close-Methode

Eine vom Benutzer implementierte Methode zum Schließen einer Shader- \# Includedatei.

## <a name="syntax"></a>Syntax


```C++
HRESULT Close(
  [in] LPCVOID pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* \[ in\]
</dt> <dd>

Geben Sie Folgendes ein: **[ **lpcvoid**](../winprog/windows-data-types.md)**

Ein Zeiger auf den zurückgegebenen Puffer, der die include-Direktiven enthält. Dies ist der Zeiger, der vom entsprechenden [**ID3DXInclude:: Open**](id3dxinclude--open.md) -Befehl zurückgegeben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die vom Benutzer implementierte Methode sollte S \_ OK zurückgeben. Wenn beim Lesen der Includedatei der Rückruf fehlschlägt \# , schlägt die API fehl, die den Aufruf des Rückrufs bewirkt hat. Folgende Werte sind möglich:

-   Der HLSL-Shader erzeugt eine der D3DXCompileShader- \* \* \* Funktionen nicht.
-   Der assemblyshader führt einen der D3DXAssembleShader- \* \* \* Funktionen aus.
-   Der Effekt führt nicht zu einer der D3DXCreateEffect- \* \* \* oder D3DXCreateEffectCompiler- \* \* \* Funktionen.

## <a name="remarks"></a>Bemerkungen

Wenn [**ID3DXInclude:: Open**](id3dxinclude--open.md) erfolgreich war, wird **ID3DXInclude:: Close** garantiert aufgerufen, bevor die API, die diese Schnittstelle verwendet, zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude:: Open**](id3dxinclude--open.md)
</dt> </dl>

 

 
