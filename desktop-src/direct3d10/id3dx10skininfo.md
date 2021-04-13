---
description: Mit ID3DX10SkinInfo können Sie die Beziehung zwischen den Knochen und Scheitel Punkten in ihren Netzen optimieren, verarbeiten und manuell festlegen (siehe "Skelett Animation" auf Wikipedia).
ms.assetid: bea0fe71-c201-45c6-8036-d0d76d5851fd
title: ID3DX10SkinInfo-Schnittstelle (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3216765ab9ef2ba9f2b0883c31a878a7eae6861f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354927"
---
# <a name="id3dx10skininfo-interface"></a>ID3DX10SkinInfo-Schnittstelle

Mit ID3DX10SkinInfo können Sie die Beziehung zwischen den Knochen und Scheitel Punkten in ihren Netzen optimieren, verarbeiten und manuell festlegen (siehe " [Skelett Animation" auf Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)). Es ist besonders nützlich, wenn Sie x-Dateien, die von DCC-apps exportiert werden (z. b. 3ds Max und Maya), flexibler gestalten und die renderinggeschwindigkeit der im Software-Rendermodus gespritzelten Netze verbessern.

## <a name="members"></a>Member

Die **ID3DX10SkinInfo** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **ID3DX10SkinInfo** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ID3DX10SkinInfo** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                   | BESCHREIBUNG                                                                                                                        |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**Addboneinfluences**](id3dx10skininfo-addboneinfluences.md)           | Ermöglicht, dass ein vorhandener Arbeitsspeicher eine Gruppe von Scheitel Punkten beeinflusst und festlegt, wie viel Einfluss der Knochen auf jeden Scheitelpunkt hat.<br/>     |
| [**Addbones**](id3dx10skininfo-addbones.md)                             | Speicherplatz für weitere Knochen zuweisen.<br/>                                                                                          |
| [**Addvertices**](id3dx10skininfo-addvertices.md)                       | Zuweisen von Speicherplatz für weitere Scheitel Punkte.<br/>                                                                                 |
| [**Clearboneingefluences**](id3dx10skininfo-clearboneinfluences.md)       | Löschen Sie die Liste der Scheitel Punkte, auf die sich die Schnittstelle auswirkt.<br/>                                                                     |
| [**Kompakt**](id3dx10skininfo-compact.md)                               | Begrenzen Sie die Anzahl der Knochen, die einen Scheitelpunkt beeinflussen können, und/oder schränken Sie die Menge der Auswirkungen ein, die ein Knochen auf einen Scheitelpunkt aufweisen kann.<br/> |
| [**Dosoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md)         | Führt die Software in einem Array von Vertices aus.<br/>                                                                           |
| [**Findboneinfluumceindex**](id3dx10skininfo-findboneinfluenceindex.md) | Suchen Sie nach dem Index, der angibt, wo sich ein bestimmter Scheitelpunkt in der Liste der beeinflussten Scheitel Punkte eines bestimmten Knotens befindet.<br/>                    |
| [**Getboneingefluence**](id3dx10skininfo-getboneinfluence.md)             | Gibt die Menge der Auswirkung an, die ein bestimmter Knochen über einem bestimmten Scheitelpunkt hat.<br/>                                                       |
| [**Getboneinfluercecount**](id3dx10skininfo-getboneinfluencecount.md)   | Gibt die Anzahl der Scheitel Punkte an, die von einem bestimmten Knochen beeinflusst werden.<br/>                                                                |
| [**Getboneingefluences**](id3dx10skininfo-getboneinfluences.md)           | Eine Liste der Scheitel Punkte, die von einem bestimmten Knochen beeinflusst werden, und eine Liste der Auswirkungen von Bone auf jeden Scheitelpunkt erhalten.<br/> |
| [**Getmaxboneingefluences**](id3dx10skininfo-getmaxboneinfluences.md)     | Holen Sie sich die Anzahl der Scheitel Punkte, die ein Knochen Maximum beeinflussen kann.<br/>                                                              |
| [**Getnumbones**](id3dx10skininfo-getnumbones.md)                       | Gibt die Anzahl der Knochen in ID3DX10SkinInfo an.<br/>                                                                             |
| [**Getnumvertices**](id3dx10skininfo-getnumvertices.md)                 | Holen Sie sich die Anzahl der Vertices in ID3DX10SkinInfo.<br/>                                                                          |
| [**Neu zuordnen**](id3dx10skininfo-remapbones.md)                         | Ändern Sie, welche Knochen welche Scheitel Punkte beeinflussen.<br/>                                                                            |
| [**Remapvertices**](id3dx10skininfo-remapvertices.md)                   | Ändern der zu ändernden Scheitel Punkte<br/>                                                                    |
| [**Removebone**](id3dx10skininfo-removebone.md)                         | Entfernt einen Knochen.<br/>                                                                                                          |
| [**Setboneingefluence**](id3dx10skininfo-setboneinfluence.md)             | Legen Sie den Umfang der Auswirkung fest, den ein bestimmter Knochen über einem bestimmten Scheitelpunkt hat.<br/>                                                       |



 

## <a name="remarks"></a>Bemerkungen

Erstellen Sie eine ID3DX10SkinInfo-Schnittstelle mit [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh** oder **D3DX10CreateSkinInfoFVF**.

Der LPD3DX10SKININFO-Typ wird als Zeiger auf die **ID3DX10SkinInfo** -Schnittstelle definiert.


```
typedef struct ID3DX10SkinInfo *LPD3DX10SKININFO;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
