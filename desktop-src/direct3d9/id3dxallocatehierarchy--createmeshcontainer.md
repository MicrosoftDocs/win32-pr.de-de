---
description: Fordert die Zuordnung eines Mesh-Container Objekts an.
ms.assetid: ec66b393-016b-4572-94dc-5c8903b506a3
title: 'ID3DXAllocateHierarchy:: samatemeshcontainer-Methode (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0351290b8dee260d52362702d520b01e1bcb7af3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364345"
---
# <a name="id3dxallocatehierarchycreatemeshcontainer-method"></a>ID3DXAllocateHierarchy:: samatemeshcontainer-Methode

Fordert die Zuordnung eines Mesh-Container Objekts an.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateMeshContainer(
  [in]                LPCSTR              Name,
  [in]          const D3DXMESHDATA        *pMeshData,
  [in]          const D3DXMATERIAL        *pMaterials,
  [in]          const D3DXEFFECTINSTANCE  *pEffectInstances,
  [in]                DWORD               NumMaterials,
  [in]          const DWORD               *pAdjacency,
  [in]                LPD3DXSKININFO      pSkinInfo,
  [out, retval]       LPD3DXMESHCONTAINER *ppNewMeshContainer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Der Name des Netzes.

</dd> <dt>

*pmeshdata* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMESHDATA**](d3dxmeshdata.md) \***

Zeiger auf die Mesh-Datenstruktur. Siehe [**D3DXMESHDATA**](d3dxmeshdata.md).

</dd> <dt>

*pmaterials* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATERIAL**](d3dxmaterial.md) \***

Ein Array von Material, das im Mesh verwendet wird.

</dd> <dt>

" *Peer-ectinhaltungen* \[ " in\]
</dt> <dd>

Typ: **Konstanten [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***

Array von Effekt Instanzen, die im Mesh verwendet werden. Siehe [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

*Nummaterial* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Anzahl der Materialien im Material Array.

</dd> <dt>

*padjacency* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Das Array für das Mesh.

</dd> <dt>

*pskininfo* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**

Zeiger auf das Skin-Mesh-Objekt, wenn Skin-Daten gefunden werden. Siehe [**ID3DXSkinInfo**](id3dxskininfo.md).

</dd> <dt>

*ppnewmeshcontainer* \[ Out, retval\]
</dt> <dd>

Typ: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***

Gibt den erstellten Mesh-Container zurück. Siehe [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die-Methode, um D3D OK zurückzugeben \_ . Andernfalls programmieren Sie die Methode, um eine entsprechende Fehlermeldung von D3DERR oder D3DXERR zurückzugeben, da dies dazu führt, dass [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) ebenfalls fehlschlägt, und gibt den Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXAllocateHierarchy](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
