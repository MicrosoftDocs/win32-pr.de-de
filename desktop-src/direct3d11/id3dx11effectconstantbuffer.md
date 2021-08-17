---
title: ID3DX11EffectConstantBuffer-Schnittstelle (D3dx11effect.h)
description: Eine Konstantenpufferschnittstelle greifen auf konstante Puffer oder Texturpuffer zu.
ms.assetid: 2106cb51-dc0a-4ab6-adb6-2deb06922af1
keywords:
- ID3DX11EffectConstantBuffer-Schnittstelle Direct3D 11
- ID3DX11EffectConstantBuffer-Schnittstelle Direct3D 11 , beschrieben
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c5e62e6d339482123f66b7f23aae771f335392b54b9a766681dab78f6fbafa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851640"
---
# <a name="id3dx11effectconstantbuffer-interface"></a>ID3DX11EffectConstantBuffer-Schnittstelle

Eine Konstantenpufferschnittstelle greifen auf konstante Puffer oder Texturpuffer zu.

## <a name="members"></a>Member

Die **ID3DX11EffectConstantBuffer-Schnittstelle** erbt von [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectConstantBuffer** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX11EffectConstantBuffer-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                             | Beschreibung                                          |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------|
| [**GetConstantBuffer**](id3dx11effectconstantbuffer-getconstantbuffer.md)         | Hier wird ein Konstantenpuffer (Constant Buffer) erhalten.<br/>                    |
| [**GetTextureBuffer**](id3dx11effectconstantbuffer-gettexturebuffer.md)           | Hier erhalten Sie einen Texturpuffer.<br/>                     |
| [**SetConstantBuffer**](id3dx11effectconstantbuffer-setconstantbuffer.md)         | Legen Sie einen Konstantenpuffer fest.<br/>                    |
| [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md)           | Legen Sie einen Texturpuffer fest.<br/>                     |
| [**UndoSetConstantBuffer**](id3dx11effectconstantbuffer-undosetconstantbuffer.md) | Setzt einen zuvor festgelegten Konstantenpuffer zurück.<br/> |
| [**UndoSetTextureBuffer**](id3dx11effectconstantbuffer-undosettexturebuffer.md)   | Setzt einen zuvor festgelegten Texturpuffer zurück.<br/>  |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie konstante Puffer, um viele Effektkonst constants zu speichern. Gruppieren von Konstanten in Puffern basierend auf ihrer Aktualisierungshäufigkeit. Auf diese Weise können Sie die Anzahl der Zustandsänderungen minimieren und die wenigsten API-Aufrufe zum Ändern des Zustands ausführen. Beide Faktoren führen zu einer besseren Leistung.

> [!Note]  
> Das DirectX SDK stellt keine kompilierten Binärdateien für Effekte bereit. Sie müssen die Quelle Effects 11 verwenden, um Ihre Effekttypanwendung zu erstellen. Weitere Informationen zur Verwendung der Quelle Effects 11 finden Sie unter [Unterschiede zwischen Effekten 10 und Effekten 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Bibliothek<br/> | <dl> <dt>Nicht verfügbar (eine Effects 11-Bibliothek ist online als freigegebene Quelle verfügbar.)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effekte 11 Schnittstellen](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





