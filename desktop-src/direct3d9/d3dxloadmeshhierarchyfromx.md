---
description: 'D3DXLoadMeshHierarchyFromX-Funktion: Lädt die erste Framehierarchie aus einer X-Datei.'
ms.assetid: 1d446b23-9028-4187-b97c-a61edfe68e39
title: D3DXLoadMeshHierarchyFromX-Funktion (D3dx9anim.h)
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
ms.openlocfilehash: b6f6f08e10155509df800cca3cb3788d6b27e520
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114358"
---
# <a name="d3dxloadmeshhierarchyfromx-function"></a>D3DXLoadMeshHierarchyFromX-Funktion

Lädt die erste Framehierarchie aus einer X-Datei.

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

*Dateiname* \[ In\]
</dt> <dd>

Typ: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Dateinamen angibt. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR auflösen. Andernfalls wird der Zeichenfolgendatentyp in LPCSTR auflösen. Siehe Hinweise.

</dd> <dt>

*MeshOptions* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Kombination von mindestens einem Flag aus der [**D3DXMESH-Enumeration,**](./d3dxmesh.md) die Erstellungsoptionen für das Gitternetz angeben.

</dd> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Zeiger auf eine [**IDirect3DDevice9-Schnittstelle,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) das dem Gittermodell zugeordnete Geräteobjekt.

</dd> <dt>

*pAlloc* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Zeiger auf eine [**ID3DXAllocateHierarchy-Schnittstelle.**](id3dxallocatehierarchy.md)

</dd> <dt>

*pUserDataLoader* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**

Von der Anwendung bereitgestellte Schnittstelle, die das Laden von Benutzerdaten ermöglicht. Siehe [**ID3DXLoadUserData.**](id3dxloaduserdata.md)

</dd> <dt>

*ppFrameHierarchy* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXFRAME**](d3dxframe.md)\***

Gibt einen Zeiger auf die geladene Rahmenhierarchie zurück. Siehe [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*ppAnimController* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Gibt einen Zeiger auf den Animationscontroller zurück, der der Animation in der X-Datei entspricht. Dies wird mit Standardspuren und Ereignissen erstellt. Siehe [**ID3DXAnimationController.**](id3dxanimationcontroller.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXLoadMeshHierarchyFromXW aufgelöst. Andernfalls wird der Funktionsaufruf in D3DXLoadMeshHierarchyFromXA aufgelöst.

Alle Gitternetze in der Datei werden in ein Ausgabegitternetz reduziert. Wenn die Datei eine Rahmenhierarchie enthält, werden alle Transformationen auf das Gitternetz angewendet.

**D3DXLoadMeshHierarchyFromX** lädt die Animationsdaten und die Framehierarchie aus einer X-Datei. Sie scannt die X-Datei und erstellt eine Framehierarchie und einen Animationscontroller gemäß dem von [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)abgeleiteten Objekt, das über pAlloc an sie übergeben wird. Das Laden der Daten erfordert mehrere Schritte wie folgt:

1.  Leiten Sie [**ID3DXAllocateHierarchy ab,**](id3dxallocatehierarchy.md)und implementieren Sie jede Methode. Dies steuert, wie Frames und Gitternetze zugeordnet und frei werden.
2.  Leiten Sie [**ID3DXLoadUserData ab,**](id3dxloaduserdata.md)und implementieren Sie jede Methode. Wenn Ihre X-Datei keine eingebetteten benutzerdefinierten Daten enthält oder Sie sie nicht benötigen, können Sie diesen Teil überspringen.
3.  Erstellen Sie ein Objekt ihrer [**ID3DXAllocateHierarchy-Klasse**](id3dxallocatehierarchy.md) und optional Ihrer LoadUserData-Klasse. Sie müssen keine Methoden dieser Objekte selbst aufrufen.
4.  Rufen **Sie D3DXLoadMeshHierarchyFromX** auf, und übergeben Sie ihr [**ID3DXAllocateHierarchy-Objekt**](id3dxallocatehierarchy.md) und Ihr [**ID3DXLoadUserData-Objekt**](id3dxloaduserdata.md) (oder **NULL),** um die Framehierarchie und den Animationscontroller zu erstellen. Alle Animationssätze und Frames werden automatisch beim Animationscontroller registriert.

Während des Ladevorgang werden [**CreateFrame**](id3dxallocatehierarchy--createframe.md) und [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) auf jedem Frame zurückgebewegt, um das Laden und die Zuordnung des Frames zu steuern. Die Anwendung definiert diese Methoden, um zu steuern, wie Frames gespeichert werden. [**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) und [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) werden für jedes Gittermodellobjekt zurückgebewegt, um das Laden und die Zuordnung von Gittermodellobjekten zu steuern. [**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) wird für jedes Objekt der obersten Ebene zurückgewendet, das nicht von den anderen Methoden geladen wird.

Um diese Daten frei zu geben, rufen Sie ID3DXAnimationController::Release auf, um die Animationssätze frei zu geben, und [**D3DXFRAMEDestroy**](d3dxframedestroy.md), indem Sie den Stammknoten der Framehierarchie und ein Objekt der abgeleiteten [**ID3DXAllocateHierarchy-Klasse**](id3dxallocatehierarchy.md) übergeben. [**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md) und [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) werden jeweils für jeden Frame und jedes Gittermodellobjekt in der Framehierarchie aufgerufen. Ihre Implementierung von **DestroyFrame** sollte alles freigeben, was von [**CreateFrame**](id3dxallocatehierarchy--createframe.md)zugeordnet wird, und ebenso für die Meshcontainermethoden.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Animationsfunktionen](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
