---
title: ID3DX11Effect GetGroupByName-Methode (D3dx11effect.h)
description: Ruft eine Effektgruppe nach Namen ab.
ms.assetid: 14b4b484-848a-409c-9a99-207ab25b7566
keywords:
- GetGroupByName-Methode Direct3D 11
- GetGroupByName-Methode Direct3D 11, ID3DX11Effect-Schnittstelle
- ID3DX11Effect-Schnittstelle Direct3D 11 , GetGroupByName-Methode
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 905fb9fb439dcf613e5abfee22f03bf968c81838c89af17d72e7f4a74d887c6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046598"
---
# <a name="id3dx11effectgetgroupbyname-method"></a>ID3DX11Effect::GetGroupByName-Methode

Ruft eine Effektgruppe nach Namen ab.

## <a name="syntax"></a>Syntax


```C++
ID3DX11EffectGroup* GetGroupByName(
   LPCSTR Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* 
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Name der Effektgruppe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***

Ein Zeiger auf eine [**ID3DX11EffectGroup-Schnittstelle.**](id3dx11effectgroup.md)

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

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

