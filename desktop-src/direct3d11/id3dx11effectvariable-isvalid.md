---
title: ID3DX11EffectVariable IsValid-Methode (D3dx11effect.h)
description: Vergleichen Sie den Datentyp mit den gespeicherten Daten.
ms.assetid: 3384afa3-6ae5-4c7c-b95d-4fe3c87cc2fe
keywords:
- IsValid-Methode Direct3D 11
- IsValid-Methode Direct3D 11, ID3DX11EffectVariable-Schnittstelle
- ID3DX11EffectVariable-Schnittstelle Direct3D 11 , IsValid-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e198fcd1a5dc39823df8c707d97849c5115d818b784dd78b1e960ee2463087ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117734059"
---
# <a name="id3dx11effectvariableisvalid-method"></a>ID3DX11EffectVariable::IsValid-Methode

Vergleichen Sie den Datentyp mit den gespeicherten Daten.

## <a name="syntax"></a>Syntax


```C++
BOOL IsValid();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

**TRUE,** wenn die Syntax gültig ist; **andernfalls FALSE**.

## <a name="remarks"></a>Hinweise

Diese Methode überprüft, ob der Datentyp den gespeicherten Daten entspricht, nachdem eine Schnittstelle in eine andere (mithilfe einer der As-Methoden) umgelagert wurde.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

