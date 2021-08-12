---
description: Erstellt eine X-Datei und speichert die Gitternetzhierarchie und die entsprechenden Animationen darin.
ms.assetid: 803926fe-8cb7-422a-9920-56f7d0b0d0ea
title: D3DXSaveMeshHierarchyToFile-Funktion (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshHierarchyToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 892d27e305badc2cf1b21de41a1f9d37da13f36c1521135a79a65619e31903f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118298528"
---
# <a name="d3dxsavemeshhierarchytofile-function"></a>D3DXSaveMeshHierarchyToFile-Funktion

Erstellt eine X-Datei und speichert die Gitternetzhierarchie und die entsprechenden Animationen darin.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXSaveMeshHierarchyToFile(
  _In_       LPCSTR                    pFilename,
  _In_       DWORD                     XFormat,
  _In_ const D3DXFRAME                 *pFrameRoot,
  _In_       LPD3DXANIMATIONCONTROLLER pAnimController,
  _In_       LPD3DXSAVEUSERDATA        pUserDataSaver
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFilename* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Zeiger auf eine Zeichenfolge, die den Namen der X-Datei angibt, die das gespeicherte Gitternetz identifiziert. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der Zeichenfolgendatentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*XFormat* \[ In\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Format der X-Datei (Text oder Binärdatei, komprimiert oder nicht) Siehe D3DXF \_ FILEFORMAT. D3DXF \_ FILEFORMAT \_ COMPRESSED kann (mithilfe eines logischen OR) entweder mit den D3DXF \_ FILEFORMAT \_ BINARY- oder D3DXF \_ FILEFORMAT \_ TEXT-Flags kombiniert werden, um die Größe der Ausgabedatei zu reduzieren.

</dd> <dt>

*pFrameRoot* \[ In\]
</dt> <dd>

Typ: **const [**D3DXFRAME**](d3dxframe.md) \***

Stammknoten der zu speichernden Hierarchie. Siehe [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*pAnimController* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**

Animationscontroller, der über zu speichernde Animationssätze verfügt. Siehe [**ID3DXAnimationController.**](id3dxanimationcontroller.md)

</dd> <dt>

*pUserDataSaver* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**

Von der Anwendung bereitgestellte Schnittstelle, die das Speichern von Benutzerdaten ermöglicht. Siehe [**ID3DXSaveUserData**](id3dxsaveuserdata.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Hinweise

Die Compilereinstellung bestimmt auch die Funktionsversion. Wenn Unicode definiert ist, wird der Funktionsaufruf in D3DXSaveMeshHierarchyToFileW aufgelöst. Andernfalls wird der Funktionsaufruf in D3DXSaveMeshHierarchyToFileA aufgelöst.

Diese Funktion speichert keine komprimierten Animationssätze.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Animationsfunktionen](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> <dt>

[X-Dateiverweis](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 
