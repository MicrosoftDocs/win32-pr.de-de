---
title: ID3DX11EffectGroup IsValid-Methode (D3dx11effect.h)
description: Testen Sie einen Effekt, um zu überprüfen, ob er eine gültige Syntax enthält. | ID3DX11EffectGroup IsValid-Methode (D3dx11effect.h)
ms.assetid: 05829749-cef0-40ed-beab-556a65a1ac96
keywords:
- IsValid-Methode Direct3D 11
- IsValid-Methode Direct3D 11, ID3DX11EffectGroup-Schnittstelle
- ID3DX11EffectGroup-Schnittstelle Direct3D 11 , IsValid-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectGroup.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab28c0658c45e4091233e75c6456a9446da46a5a6d4a045bf3a533d881b42ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046248"
---
# <a name="id3dx11effectgroupisvalid-method"></a>ID3DX11EffectGroup::IsValid-Methode

Testen Sie einen Effekt, um zu überprüfen, ob er eine gültige Syntax enthält.

## <a name="syntax"></a>Syntax


```C++
BOOL IsValid();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

**TRUE,** wenn die Codesyntax gültig ist; **andernfalls FALSE**.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectGroup](id3dx11effectgroup.md)
</dt> </dl>

 

