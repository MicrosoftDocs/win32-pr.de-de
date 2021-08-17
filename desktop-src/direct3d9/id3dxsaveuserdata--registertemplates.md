---
description: Ein Rückruf für den Benutzer zum Registrieren einer X-Dateivorlage.
ms.assetid: 60568556-704c-4be3-bbde-04887583cf70
title: ID3DXSaveUserData::RegisterTemplates-Methode (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData.RegisterTemplates
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a41a43f8f319ee09f24c4f62092e4718773dc312cb7886b0fc7c95781e614c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628730"
---
# <a name="id3dxsaveuserdataregistertemplates-method"></a>ID3DXSaveUserData::RegisterTemplates-Methode

Ein Rückruf für den Benutzer zum Registrieren einer X-Dateivorlage.

## <a name="syntax"></a>Syntax


```C++
HRESULT RegisterTemplates(
  [in] LPD3DXFILE pXFileApi
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pXFileApi* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXFILE**](id3dxfile.md)**

Verwenden Sie diesen Zeiger, um benutzerdefinierte X-Dateivorlagen zu registrieren. Siehe [**ID3DXFile**](id3dxfile.md). Verwenden Sie diesen Parameter nicht, um Datenobjekte hinzuzufügen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Die Rückgabewerte dieser Methode werden von einem Anwendungsprogrammierer implementiert. Wenn kein Fehler auftritt, programmieren Sie im Allgemeinen die -Methode so, dass D3D \_ OK zurückgegeben wird. Programmieren Sie andernfalls die -Methode so, dass eine entsprechende Fehlermeldung von [D3DERR](d3derr.md) oder [**D3DXERR**](./d3dxerr.md)zurückgegeben wird, da dadurch [**auch D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) fehlschlägt und der Fehler zurückgegeben wird.

## <a name="remarks"></a>Hinweise

**ID3DXSaveUserData::RegisterTemplates** und [**ID3DXSaveUserData::SaveTemplates**](id3dxsaveuserdata--savetemplates.md) bieten einen Mechanismus zum Hinzufügen einer Vorlage zu einer X-Datei zum Speichern von Benutzerdaten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXSaveUserData](id3dxsaveuserdata.md)
</dt> </dl>

 

 
