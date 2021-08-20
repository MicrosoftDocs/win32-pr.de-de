---
title: ID3DX11EffectPass IsValid-Methode (D3dx11effect.h)
description: Testen Sie einen Durchlauf, um festzustellen, ob er eine gültige Syntax enthält.
ms.assetid: 3c6ddcef-1303-4161-889c-c3ca271b6ad0
keywords:
- IsValid-Methode Direct3D 11
- IsValid-Methode Direct3D 11 , ID3DX11EffectPass-Schnittstelle
- ID3DX11EffectPass-Schnittstelle Direct3D 11 , IsValid-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4d184f1912e3518c63e3e1720c0438acee9c84eba52b7a3a6717bbb2d9e091
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534946"
---
# <a name="id3dx11effectpassisvalid-method"></a>ID3DX11EffectPass::IsValid-Methode

Testen Sie einen Durchlauf, um festzustellen, ob er eine gültige Syntax enthält.

## <a name="syntax"></a>Syntax


```C++
BOOL IsValid();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

**TRUE,** wenn die Codesyntax gültig ist; andernfalls **FALSE**.

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

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

