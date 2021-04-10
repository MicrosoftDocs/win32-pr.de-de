---
description: Lädt die erste Frame Hierarchie aus einer x-Datei.
ms.assetid: 1d446b23-9028-4187-b97c-a61edfe68e39
title: D3DXLoadMeshHierarchyFromX-Funktion (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 308ebf127708849bec8ee8a4f2601f029562634a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961553"
---
# <a name="d3dxloadmeshhierarchyfromx-function"></a>D3DXLoadMeshHierarchyFromX-Funktion

Lädt die erste Frame Hierarchie aus einer x-Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXLoadMeshHierarchyFromX(
  _In_  LPCTSTR                   Filename,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHierarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dateiname* \[ in\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der String-Datentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*MeshOptions* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren Flags aus der [**D3DXMESH**](./d3dxmesh.md) -Enumeration, die Erstellungs Optionen für das Mesh angeben.

</dd> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) -Schnittstelle, das dem Mesh zugeordnete Geräte Objekt.

</dd> <dt>

*palloc* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Zeiger auf eine [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) -Schnittstelle.

</dd> <dt>

*puserdataloader* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**

Von der Anwendung bereitgestellte Schnittstelle, die das Laden von Benutzerdaten ermöglicht Siehe [**ID3DXLoadUserData**](id3dxloaduserdata.md).

</dd> <dt>

*ppframehierarchy* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXFRAME**](d3dxframe.md)\***

Gibt einen Zeiger auf die geladene Frame Hierarchie zurück. Siehe [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*ppanimcontroller* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Gibt einen Zeiger auf den Animations Controller zurück, der der Animation in der x-Datei entspricht. Dies wird mit Standardspuren und-Ereignissen erstellt. Siehe [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXLoadMeshHierarchyFromXW aufgelöst. Andernfalls wird der Funktions aufrufin D3DXLoadMeshHierarchyFromXA aufgelöst.

Alle Netzen in der Datei werden in einem Ausgabe Mesh reduziert. Wenn die Datei eine Frame Hierarchie enthält, werden alle Transformationen auf das Mesh angewendet.

**D3DXLoadMeshHierarchyFromX** lädt die Animationsdaten und die Frame Hierarchie aus einer x-Datei. Er scannt die x-Datei und erstellt eine Frame Hierarchie und einen Animations Controller gemäß dem an Sie übergebenen [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)-Objekt über palloc. Zum Laden der Daten sind folgende Schritte erforderlich:

1.  Ableiten Sie [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), indem Sie jede Methode implementieren. Dadurch wird gesteuert, wie Frames und Netze zugeordnet und freigegeben werden.
2.  Ableiten Sie [**ID3DXLoadUserData**](id3dxloaduserdata.md), indem Sie jede Methode implementieren. Wenn die x-Datei keine eingebetteten benutzerdefinierten Daten enthält, oder wenn Sie Sie nicht benötigen, können Sie diesen Teil überspringen.
3.  Erstellen Sie ein Objekt der [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) -Klasse und optional ihrer loaduserdata-Klasse. Sie müssen keine Methoden dieser Objekte selbst aufzurufen.
4.  Rufen Sie **D3DXLoadMeshHierarchyFromX** auf, und übergeben Sie das [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) -Objekt und das [**ID3DXLoadUserData**](id3dxloaduserdata.md) -Objekt (oder **null**), um die Frame Hierarchie und den Animations Controller zu erstellen. Alle Animations Sätze und Frames werden automatisch beim Animations Controller registriert.

Während der Auslastung werden " [**forateframe**](id3dxallocatehierarchy--createframe.md) " und " [**loadframechilddata**](id3dxloaduserdata--loadframechilddata.md) " in jedem Frame zurück aufgerufen, um das Laden und die Zuordnung des Frames zu steuern. Die Anwendung definiert diese Methoden, um die Speicherung von Frames zu steuern. " [**Anatemeschcontainer**](id3dxallocatehierarchy--createmeshcontainer.md) " und " [**loadmeshchilddata**](id3dxloaduserdata--loadmeshchilddata.md) " werden für jedes Mesh-Objekt zurück aufgerufen, um das Laden und Zuordnen von Mesh-Objekten zu steuern. [**Loadtopleveldata**](id3dxloaduserdata--loadtopleveldata.md) wird für jedes Objekt der obersten Ebene zurückgerufen, das nicht von den anderen Methoden geladen wird.

Um diese Daten freizugeben, wenden Sie ID3DXAnimationController:: Release an, um die Animations Sätze freizugeben, und [**D3DXFRAMEDestroy**](d3dxframedestroy.md), indem Sie den Stamm Knoten der Frame Hierarchie und ein Objekt der abgeleiteten [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) -Klasse übergeben. [**Destroyframe**](id3dxallocatehierarchy--destroyframe.md) und [**destroymeschcontainer**](id3dxallocatehierarchy--destroymeshcontainer.md) werden jeweils für jedes Frame-und Mesh-Objekt in der Frame Hierarchie aufgerufen. Ihre Implementierung von **destroyframe** sollte alle von " [**kreateframe**](id3dxallocatehierarchy--createframe.md)" zugewiesenen Elemente freigeben und auch für die Mesh-Container-Methoden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Animations Funktionen](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
