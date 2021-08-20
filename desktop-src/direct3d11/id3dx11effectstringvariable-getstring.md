---
title: ID3DX11EffectStringVariable GetString-Methode (D3dx11effect.h)
description: Abrufen der Zeichenfolge.
ms.assetid: ce96ae18-d316-41ba-9b2a-eac084b86098
keywords:
- GetString-Methode Direct3D 11
- GetString-Methode Direct3D 11 , ID3DX11EffectStringVariable-Schnittstelle
- ID3DX11EffectStringVariable-Schnittstelle Direct3D 11 , GetString-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0edef49fd0965e06693fb995434c0579080f1e6243522ca4ea1489dedb791f5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118532998"
---
# <a name="id3dx11effectstringvariablegetstring-method"></a>ID3DX11EffectStringVariable::GetString-Methode

Abrufen der Zeichenfolge.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetString(
   LPCSTR *ppString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppString* 
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***

Ein Zeiger auf die Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectStringVariable](id3dx11effectstringvariable.md)
</dt> </dl>

 

