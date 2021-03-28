---
title: ID3DX11EffectRasterizerVariable-Schnittstelle (D3dx11effect. h)
description: Eine Raster-Variable-Schnittstelle greift auf den Status des Rasterizers zu.
ms.assetid: d039e3c5-c066-4658-bead-92a5d705ed89
keywords:
- ID3DX11EffectRasterizerVariable-Schnittstelle Direct3D 11
- ID3DX11EffectRasterizerVariable Interface Direct3D 11, beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a19c5d529d6134ebad238be6e7c6195dc628a7f6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996259"
---
# <a name="id3dx11effectrasterizervariable-interface"></a>ID3DX11EffectRasterizerVariable-Schnittstelle

Eine Raster-Variable-Schnittstelle greift auf den Status des Rasterizers zu.

## <a name="members"></a>Member

Die **ID3DX11EffectRasterizerVariable** -Schnittstelle erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectRasterizerVariable** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectRasterizerVariable** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                   | BESCHREIBUNG                                                            |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**Getbackingstore**](id3dx11effectrasterizervariable-getbackingstore.md)               | Ein Zeiger auf eine Variable, die den rasteriser-Zustand enthält, wird angezeigt.<br/> |
| [**Getrasterizerstate**](id3dx11effectrasterizervariable-getrasterizerstate.md)         | Einen Zeiger auf eine Raster-Schnittstelle erhalten.<br/>                    |
| [**"Tartrasterizerstate"**](id3dx11effectrasterizervariable-setrasterizerstate.md)         | Legt den Status des Rasterizers fest.<br/>                                  |
| [**Undotartrasterizerstate**](id3dx11effectrasterizervariable-undosetrasterizerstate.md) | Stellt einen zuvor festgelegten Raster-Zustand wieder her.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

Eine [**ID3DX11EffectVariable**](id3dx11effectvariable.md) -Schnittstelle wird erstellt, wenn ein Effekt in den Arbeitsspeicher gelesen wird.

Effekt Variablen werden im Sicherungs Speicher im Arbeitsspeicher gespeichert. Wenn eine Technik angewendet wird, werden die Werte im Sicherungs Speicher auf das Gerät kopiert. Sie können eine dieser Methoden verwenden, um den Status zurückzugeben.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Effekte 11-Quelle verwenden, um die Effekte-Anwendung zu erstellen. Weitere Informationen zum Verwenden der Effekte 11-Quelle finden Sie [unter Unterschiede zwischen den Effekten 10 und Effekte 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>N/v (die "Effects 11"-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effekte 11-Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





