---
description: Erstellt eine x-Datei und speichert die Gitter Hierarchie und die dazugehörigen Animationen darin.
ms.assetid: 803926fe-8cb7-422a-9920-56f7d0b0d0ea
title: D3DXSaveMeshHierarchyToFile-Funktion (D3dx9anim. h)
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
ms.openlocfilehash: f2de65f9bc2f9e40a5bc07c6f0b4d00112f0df21
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106363134"
---
# <a name="d3dxsavemeshhierarchytofile-function"></a>D3DXSaveMeshHierarchyToFile-Funktion

Erstellt eine x-Datei und speichert die Gitter Hierarchie und die dazugehörigen Animationen darin.

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

*pfilename* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Ein Zeiger auf eine Zeichenfolge, die den Namen der x-Datei angibt, die das gespeicherte Mesh identifiziert. Wenn die Compilereinstellungen Unicode erfordern, wird der Datentyp LPCTSTR in LPCWSTR aufgelöst. Andernfalls wird der String-Datentyp in LPCSTR aufgelöst. Siehe Hinweise.

</dd> <dt>

*Xformat* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Format der x-Datei (Text oder Binär, komprimiert oder nicht). Siehe D3DXF \_ FileFormat. Das \_ komprimierte D3DXF File Format \_ kann mithilfe eines logischen OR-Werts kombiniert werden, entweder mit dem D3DXF \_ File Format \_ binary-oder D3DXF \_ FileFormat- \_ textflags, um die Größe der Ausgabedatei zu verringern.

</dd> <dt>

*pframeroot* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXFRAME**](d3dxframe.md) \***

Der Stamm Knoten der zu speichernden Hierarchie. Siehe [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*panimcontroller* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**

Animations Controller, der Animations Sätze enthält, die gespeichert werden sollen. Siehe [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> <dt>

*puserdatasaver* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**

Von der Anwendung bereitgestellte Schnittstelle, die das Speichern von Benutzerdaten ermöglicht. Siehe [**ID3DXSaveUserData**](id3dxsaveuserdata.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert lauten: D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Die Compilereinstellung bestimmt auch die Funktions Version. Wenn Unicode definiert ist, wird der Funktions aufrufin D3DXSaveMeshHierarchyToFileW aufgelöst. Andernfalls wird der Funktions aufrufin D3DXSaveMeshHierarchyToFileA aufgelöst.

Diese Funktion speichert keine komprimierten Animations Sätze.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Animations Funktionen](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> <dt>

[Verweis auf X-Datei](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 
