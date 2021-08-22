---
title: ID3DX11EffectUnorderedAccessViewVariable GetUnorderedAccessView-Methode (D3dx11effect.h)
description: Abrufen einer ungeordneten Zugriffsansicht.
ms.assetid: 46f61c4f-b3ee-4058-99b9-a43ca6944fb2
keywords:
- GetUnorderedAccessView-Methode Direct3D 11
- GetUnorderedAccessView-Methode Direct3D 11 , ID3DX11EffectUnorderedAccessViewVariable-Schnittstelle
- ID3DX11EffectUnorderedAccessViewVariable-Schnittstelle Direct3D 11 , GetUnorderedAccessView-Methode
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable.GetUnorderedAccessView
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02ccb890d7f03a2066cb7e01633f057e821e34c74521e1bba37f9694ba72a194
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676780"
---
# <a name="id3dx11effectunorderedaccessviewvariablegetunorderedaccessview-method"></a>ID3DX11EffectUnorderedAccessViewVariable::GetUnorderedAccessView-Methode

Abrufen einer ungeordneten Zugriffsansicht.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetUnorderedAccessView(
   ID3D11UnorderedAccessView **ppResource
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppResource* 
</dt> <dd>

Typ: **[ **ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview)\*\***

Zeiger auf einen [**ID3D11UnorderedAccessView-Zeiger,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) der bei der Rückgabe festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Gibt einen der folgenden [Direct3D 11-Rückgabecodes zurück.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte zur Verfügung. Sie müssen die Effects 11-Quelle verwenden, um ihre Effekte-Typ-Anwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/A (Eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11EffectUnorderedAccessViewVariable](id3dx11effectunorderedaccessviewvariable.md)
</dt> </dl>

 

 





